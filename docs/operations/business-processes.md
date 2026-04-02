# 04 — BUSINESS PROCESSES

## 4.1 Process Inventory

This section documents all end-to-end business processes, their Oracle Fusion touchpoints, and integration points with the custom POS system.

---

## 4.2 Core Business Processes

### PROC-FIN-001: Store-to-Ledger Revenue Recognition

**Trigger:** Customer completes a transaction at any POS terminal.  
**Frequency:** Real-time (per transaction) + daily batch reconciliation.

| Step | Activity | System | Oracle Module |
|------|----------|--------|---------------|
| 1 | Customer selects products and proceeds to checkout | Custom POS | — |
| 2 | Cashier scans items; POS calculates totals, VAT (12%), discounts | Custom POS | — |
| 3 | Customer pays (cash, card, GCash/Maya, loyalty points, gift card) | Custom POS | — |
| 4 | POS generates BIR-compliant receipt/invoice (Official Receipt or Sales Invoice) | Custom POS | — |
| 5 | POS pushes transaction to OIC via REST API (within 30 seconds) | Custom POS → OIC | Integration Cloud |
| 6 | OIC transforms and routes transaction to Oracle Receivables as a receipt/invoice | OIC → AR | Receivables |
| 7 | OIC routes to Accounting Hub for subledger journalization | OIC → GL | Accounting Hub |
| 8 | Journal posted to GL with full segment coding (company-region-store-account-category-IC) | GL | General Ledger |
| 9 | Inventory decremented at store organization level | Inventory | Inventory Management |
| 10 | COGS recognized (moving average cost × quantity sold) | Cost Management | Cost Management |
| 11 | Loyalty points earned and recorded in CX Customer Data Platform | CX | Customer Loyalty |
| 12 | Daily reconciliation: POS Z-reading totals vs. Oracle AR receipts | POS + AR | Receivables |
| 13 | Cash deposit confirmed via bank statement import | Cash Management | Cash Management |
| 14 | Bank reconciliation auto-matched | Cash Management | Cash Management |

**Key Controls:**
- POS transaction cannot be posted without complete item and pricing data.
- Every POS transaction generates a unique Oracle AR receipt number.
- Daily reconciliation variance threshold: PHP 100 per terminal; >threshold triggers exception workflow.
- BIR sequential receipt numbering maintained in POS; cross-referenced in Oracle.

---

### PROC-FIN-002: Procure-to-Pay (Merchandise)

**Trigger:** Replenishment requirement identified by supply planning or buyer.  
**Frequency:** Daily (automated from planning) + ad hoc.

| Step | Activity | System | Oracle Module |
|------|----------|--------|---------------|
| 1 | Demand Planning generates store-level demand forecast | SCP | Supply Chain Planning |
| 2 | Supply Planning creates planned orders based on demand, inventory, lead times | SCP | Supply Chain Planning |
| 3 | Buyer reviews and converts planned orders to purchase requisitions | Purchasing | Purchasing |
| 4 | PR routes through approval workflow (amount-based) | Purchasing | Purchasing |
| 5 | Approved PR auto-creates PO; assigned to best supplier per sourcing rules | Purchasing | Purchasing + Sourcing |
| 6 | PO sent to supplier via Supplier Portal or email | Supplier Portal | Supplier Portal |
| 7 | Supplier acknowledges PO with expected ship date | Supplier Portal | Supplier Portal |
| 8 | ASN (Advanced Shipping Notice) received from supplier | WMS | Warehouse Management |
| 9 | Goods received at warehouse; receiving clerk confirms quantities and quality | WMS | Warehouse Management |
| 10 | Receipt recorded in Oracle; inventory incremented | Inventory | Inventory Management |
| 11 | Supplier submits invoice via Supplier Portal or AP captures from email (AI OCR) | Payables | Payables |
| 12 | 3-way match: PO-Receipt-Invoice (automated) | Payables | Payables |
| 13 | Matched invoice approved per workflow; EWT computed per BIR table | Payables | Payables |
| 14 | Payment scheduled per supplier terms (Net 30/45/60) | Payables | Payables |
| 15 | Payment batch processed via PESONet/check; bank file generated | Payables + Cash Mgmt | Payables + Cash Management |
| 16 | GL journal posted for expense, liability, payment, and tax | GL | General Ledger |
| 17 | Landed cost finalized (product + freight + duty + handling) | Cost Management | Cost Management |

**Key Controls:**
- 3-way match enforced for all merchandise invoices > PHP 5,000.
- PO approval thresholds: Manager < PHP 50K, Director < PHP 500K, VP < PHP 5M, CFO > PHP 5M.
- EWT rates auto-applied per BIR withholding tax table (1%, 2%, 5%, 20% per goods/service type).
- Supplier payment holds automatically applied for overdue deliveries or quality issues.

---

### PROC-FIN-003: Procure-to-Pay (Non-Merchandise / Expenses)

**Trigger:** Employee identifies need for non-merchandise purchase.  
**Frequency:** Ad hoc.

| Step | Activity | System | Oracle Module |
|------|----------|--------|---------------|
| 1 | Employee creates self-service requisition | Self-Service Procurement | Self-Service Procurement |
| 2 | Requisition routes through approval workflow (amount + department based) | Purchasing | Purchasing |
| 3 | Approved requisition auto-creates PO or routes to catalog punch-out | Purchasing | Purchasing |
| 4 | PO approved and sent to supplier | Purchasing | Purchasing |
| 5 | Goods/services received; receipt confirmed | Receiving | Purchasing |
| 6 | Invoice processed; 2-way match (PO-Invoice) | Payables | Payables |
| 7 | Payment processed per terms | Payables | Payables |

---

### PROC-FIN-004: Order-to-Cash (B2B / Contractor Sales)

**Trigger:** Contractor/developer places order via sales rep, phone, or e-commerce B2B portal.  
**Frequency:** Ad hoc.

| Step | Activity | System | Oracle Module |
|------|----------|--------|---------------|
| 1 | B2B customer places order (phone, email, B2B portal, sales rep) | CX Commerce / SFA | Commerce / Sales |
| 2 | Sales rep creates opportunity/quote in Oracle CX | CX Sales + CPQ | Sales + CPQ |
| 3 | Credit check performed against customer credit limit | Receivables | Receivables |
| 4 | Sales order created in Order Management | Order Management | Order Management |
| 5 | Order scheduled for fulfillment from nearest warehouse or store | Order Management + GOP | Order Management |
| 6 | Warehouse picks, packs, and ships (or store picks for will-call) | WMS | Warehouse Management |
| 7 | Delivery scheduled and executed; POD captured | TMS | Transportation Mgmt |
| 8 | Invoice generated (BIR-compliant Sales Invoice) | Receivables | Receivables |
| 9 | Customer payment received (check, bank transfer) | Receivables | Receivables |
| 10 | Payment applied to invoice; GL updated | Receivables + GL | Receivables + GL |

---

### PROC-FIN-005: Financial Close and Consolidation

**Trigger:** End of accounting period.  
**Frequency:** Monthly (5 business day close target).

| Step | Activity | System | Oracle Module |
|------|----------|--------|---------------|
| 1 | Period close checklist initiated in Financial Consolidation & Close | FCC | Financial Consolidation & Close |
| 2 | All subledger processes completed (POS, AP, AR, Assets, Projects) | All | All |
| 3 | Intercompany transactions reconciled and matched | AR/AP | Receivables/Payables |
| 4 | Intercompany elimination entries generated | FCC | Financial Consolidation & Close |
| 5 | Account reconciliations performed (auto-matched + manual) | Account Reconciliation | Account Reconciliation |
| 6 | Reclassification and adjustment journal entries posted | GL | General Ledger |
| 7 | Foreign currency revaluation (if applicable) | GL | General Ledger |
| 8 | Asset depreciation run completed | Assets | Assets |
| 9 | Revenue recognition review (gift cards, loyalty, services) | Revenue Management | Revenue Management |
| 10 | Consolidation of 5 legal entities completed | FCC | Financial Consolidation & Close |
| 11 | Consolidated P&L and Balance Sheet generated | FCC + Narrative Reporting | FCC + Narrative Reporting |
| 12 | Tax provision computed | Tax Reporting | Tax Reporting |
| 13 | Management reports and variance analysis produced | Narrative Reporting + ERP Analytics | Narrative Reporting + Analytics |
| 14 | Close period in GL | GL | General Ledger |

---

### PROC-SCM-001: Demand-Driven Replenishment

**Trigger:** Daily MRP run or sales velocity trigger.  
**Frequency:** Daily automated + weekly review.

| Step | Activity | System | Oracle Module |
|------|----------|--------|---------------|
| 1 | POS sales data flows into demand planning engine (via OIC) | SCP | Supply Chain Planning |
| 2 | Demand planning generates updated store-level forecast | SCP | Supply Chain Planning |
| 3 | Supply planning calculates net requirements (demand - on-hand - in-transit - on-order) | SCP | Supply Chain Planning |
| 4 | Planned replenishment orders generated | SCP | Supply Chain Planning |
| 5 | Buyer/planner reviews and approves planned orders | Purchasing | Purchasing + Planning |
| 6 | Approved orders become purchase requisitions → POs | Purchasing | Purchasing |
| 7 | Warehouse replenishment transfer orders created (WH → Store) | Inventory | Inventory Management |
| 8 | Wave plan created in WMS for store replenishment picks | WMS | Warehouse Management |
| 9 | Goods picked, packed, loaded for delivery | WMS | Warehouse Management |
| 10 | In-transit shipment tracked | TMS | Transportation Mgmt |
| 11 | Store receives goods; POS system updated with new stock | Inventory | Inventory Management |
| 12 | Transfer order closed; inventory balances updated across all locations | Inventory | Inventory Management |

---

### PROC-SCM-002: Store Receiving

**Trigger:** Delivery truck arrives at store from warehouse or direct vendor.  
**Frequency:** Multiple times daily per store.

| Step | Activity | System | Oracle Module |
|------|----------|--------|---------------|
| 1 | Store receives ASN notification (advance shipping notice) | Inventory | Inventory Management |
| 2 | Delivery truck arrives; receiving clerk verifies documents | WMS Mobile / POS Receiving | Inventory Management |
| 3 | Clerk scans/enters received quantities against ASN | WMS Mobile / POS Receiving | Inventory Management |
| 4 | Discrepancies flagged for resolution (over/short/damaged) | Inventory | Inventory Management |
| 5 | Goods put away to backroom or sales floor (subinventory) | POS Receiving | Inventory Management |
| 6 | Receipt confirmed; inventory incremented at store level | Inventory | Inventory Management |
| 7 | AP receipt matched for vendor direct deliveries | Payables | Payables |

---

### PROC-SCM-003: Store-to-Store Stock Transfer

**Trigger:** Store requests stock from another store (stock balancing).  
**Frequency:** Ad hoc.

| Step | Activity | System | Oracle Module |
|------|----------|--------|---------------|
| 1 | Store Manager or system identifies stock-out with available stock at nearby store | SCP + Inventory | Supply Chain Planning + Inventory |
| 2 | Transfer order created (originating store requests from supplying store) | Order Management | Order Management |
| 3 | Approval routed (Auto-approve if < PHP 10K; Store Manager if < PHP 50K; Regional Director if > PHP 50K) | Order Management | Order Management |
| 4 | Supplying store picks and packs goods | POS + Inventory | Inventory Management |
| 5 | Goods shipped via internal logistics or 3PL | TMS | Transportation Mgmt |
| 6 | Receiving store confirms receipt | POS + Inventory | Inventory Management |
| 7 | Inventory decremented at supplying store, incremented at receiving store | Inventory | Inventory Management |
| 8 | Intercompany journal if cross-entity transfer | GL | General Ledger |

---

### PROC-HR-001: Recruitment-to-Onboarding

**Trigger:** Approved headcount requisition.  
**Frequency:** Ad hoc (ongoing for stores).

| Step | Activity | System | Oracle Module |
|------|----------|--------|---------------|
| 1 | Hiring manager submits headcount requisition | HCM Recruiting | Recruiting |
| 2 | Requisition approved per budget (HRBP → VP HR → CHRO for new positions) | HCM Recruiting | Recruiting |
| 3 | Job posting created (internal + external: JobStreet, LinkedIn, company career site) | HCM Recruiting | Recruiting |
| 4 | Applications received; AI-powered candidate screening and ranking | HCM Recruiting | Recruiting |
| 5 | HR and hiring manager shortlist candidates | HCM Recruiting | Recruiting |
| 6 | Interviews scheduled and conducted (assessment scores recorded) | HCM Recruiting | Recruiting |
| 7 | Background check and pre-employment requirements collection | HCM Recruiting | Recruiting |
| 8 | Job offer created and extended | HCM Recruiting | Recruiting |
| 9 | Candidate accepts offer | HCM Recruiting | Recruiting |
| 10 | Pre-boarding journey initiated via Oracle ME | Oracle ME Journeys | ME Journeys |
| 11 | Employee record created in Core HR (assignment, salary, benefits enrollment) | Core HR | Core HR |
| 12 | Day 1 onboarding journey begins: IT setup, orientation, safety training, system access | Oracle ME Journeys | ME Journeys + Learning |
| 13 | 30/60/90-day check-in tasks scheduled | Oracle ME Touchpoints | ME Touchpoints |
| 14 | Probationary period review completed at 5th month (6-month probation per DOLE) | Performance Management | Performance Management |

---

### PROC-HR-002: Timekeeping-to-Payroll

**Trigger:** Payroll cutoff (15th and 30th of month).  
**Frequency:** Semi-monthly.

| Step | Activity | System | Oracle Module |
|------|----------|--------|---------------|
| 1 | Employees clock in/out via POS terminal or biometric device | POS/Biometric → Time & Labor | Time and Labor |
| 2 | Time entries validated against scheduled shifts | Time & Labor | Workforce Scheduling + T&L |
| 3 | Exceptions flagged (late, undertime, missing punches, overtime) | Time & Labor | Time and Labor |
| 4 | Manager reviews and approves timecards | Time & Labor | Time and Labor |
| 5 | Overtime premium calculated per Philippine labor law (125%-200%) | Time & Labor | Time and Labor |
| 6 | Absences and leaves applied from Absence Management | Absence Mgmt + T&L | Absence + T&L |
| 7 | Approved timecards flow to Payroll | Payroll | Payroll |
| 8 | Payroll calculated: basic + OT + holiday pay + night differential + allowances | Payroll | Payroll |
| 9 | Statutory deductions computed: SSS, PhilHealth, Pag-IBIG, WTA (TRAIN law) | Payroll | Payroll |
| 10 | Other deductions: HMO, loans, savings, union dues | Payroll | Payroll |
| 11 | Payroll register reviewed and approved by HR + Finance | Payroll | Payroll |
| 12 | Bank file generated and transmitted | Payroll + Cash Mgmt | Payroll + Cash Management |
| 13 | Digital payslips available via Oracle ME | Oracle ME | ME |
| 14 | GL journal posted for payroll expense and liabilities | GL | General Ledger |

---

### PROC-CX-001: Loyalty Program Lifecycle

**Trigger:** Customer enrolls in Tahanan Rewards.  
**Frequency:** Ongoing.

| Step | Activity | System | Oracle Module |
|------|----------|--------|---------------|
| 1 | Customer enrolls in-store (POS) or online (e-commerce) | POS / Commerce | Customer Loyalty + CDP |
| 2 | Customer profile created in Customer Data Platform | CX CDP | Customer Data Platform |
| 3 | Loyalty card/number assigned | Customer Loyalty | Customer Loyalty |
| 4 | Customer earns points on purchases (1 point per PHP 50 spent) | POS → CX | Customer Loyalty |
| 5 | Points accumulated and tracked in real-time | Customer Loyalty | Customer Loyalty |
| 6 | Tier progression tracked (Silver → Gold → Platinum based on annual spend) | Customer Loyalty | Customer Loyalty |
| 7 | Personalized offers generated via marketing automation | Marketing Automation | Marketing |
| 8 | Points redemption at POS (1 point = PHP 1 discount) | POS → CX | Customer Loyalty |
| 9 | Revenue recognition for points liability (deferred revenue for unredeemed points) | Revenue Management | Revenue Management |
| 10 | Annual points expiration processing | Customer Loyalty | Customer Loyalty |

---

### PROC-CX-002: Customer Returns and Refunds

**Trigger:** Customer requests return or refund.  
**Frequency:** Ad hoc.

| Step | Activity | System | Oracle Module |
|------|----------|--------|---------------|
| 1 | Customer presents item and receipt at store | Custom POS | — |
| 2 | Store associate verifies return eligibility per return policy | Custom POS | — |
| 3 | Return processed in POS; credit memo generated | Custom POS → OIC | — |
| 4 | OIC routes to Order Management for RMA creation | OIC → OM | Order Management |
| 5 | Inventory returned to appropriate subinventory (resalable or damaged) | Inventory | Inventory Management |
| 6 | Credit memo posted in Receivables | Receivables | Receivables |
| 7 | Refund processed (cash, card reversal, or store credit) | POS + AR | Receivables |
| 8 | GL journal posted (revenue reversal, COGS reversal, inventory adjustment) | GL | General Ledger |
| 9 | Customer satisfaction survey triggered | CX Service | Service |

---

### PROC-IT-001: POS System Support and Incident Management

**Trigger:** POS system issue reported by store.  
**Frequency:** Ad hoc.

| Step | Activity | System | Oracle Module |
|------|----------|--------|---------------|
| 1 | Store reports POS issue via help desk ticket (Oracle Service or internal system) | Service | Service |
| 2 | Ticket triaged by Tahanan Digital L1 support | Service | Service |
| 3 | L1 resolves common issues (restart, network, printer) | Service | Service |
| 4 | Complex issues escalated to L2 (POS development team) | Service | Service |
| 5 | L2 diagnoses and applies fix/hotfix | POS Dev Team | — |
| 6 | Fix tested and deployed to affected terminals | POS Dev Team | — |
| 7 | Ticket closed; knowledge base updated | Service | Knowledge Management |
| 8 | Recurring issues analyzed for root cause; permanent fix planned | Analytics | CX Analytics |

---

### PROC-PROP-001: New Store Opening

**Trigger:** Board approves new store location.  
**Frequency:** As per expansion plan (~10-15 stores per year).

| Step | Activity | System | Oracle Module |
|------|----------|--------|---------------|
| 1 | Market analysis and site selection | EPM Planning | Planning |
| 2 | Financial feasibility model (capex, projected P&L, payback period) | EPM Planning | Planning + Capital Planning |
| 3 | Board approval obtained | Narrative Reporting | Narrative Reporting |
| 4 | Lease/purchase agreement executed (Tahanan Property) | Procurement Contracts | Contracts |
| 5 | Store buildout project created | Project Management | Project Management |
| 6 | Capex tracked against budget | Project Management + Assets | Projects + Assets |
| 7 | New inventory organization created in Oracle (STORE-XXX) | Inventory | Inventory Management |
| 8 | New business unit or cost center created | GL | General Ledger |
| 9 | Initial stock order generated from supply planning | SCP + Purchasing | SCP + Purchasing |
| 10 | Hiring requisitions created for new store staff | HCM Recruiting | Recruiting |
| 11 | Store staff hired and trained | HCM + Learning | Recruiting + Learning |
| 12 | POS terminals provisioned and configured | POS Team | — |
| 13 | OIC integration endpoints configured for new store | OIC | Integration Cloud |
| 14 | Pre-opening inventory loaded | Inventory | Inventory Management |
| 15 | Store opens for business | All | All |
| 16 | Post-opening performance tracked (daily for first 30 days) | ERP Analytics | Analytics |

---

### PROC-SCM-004: Import Procurement

**Trigger:** Purchase requirement for imported goods.  
**Frequency:** Monthly/quarterly based on lead times.

| Step | Activity | System | Oracle Module |
|------|----------|--------|---------------|
| 1 | Demand for imported items identified; supply plan generates planned order | SCP | Supply Chain Planning |
| 2 | Import specialist creates import PO with international supplier | Purchasing | Purchasing |
| 3 | Import documentation prepared (commercial invoice, packing list, Bill of Lading) | Global Trade Mgmt | Global Trade Management |
| 4 | Letter of Credit or TT arranged with bank | Treasury + Cash Mgmt | Cash Management |
| 5 | Goods shipped; vessel/flight tracked | TMS | Transportation Mgmt |
| 6 | Pre-arrival customs declaration filed with BOC | Global Trade Mgmt | Global Trade Management |
| 7 | Duties and taxes calculated and paid | Global Trade Mgmt | Global Trade Management |
| 8 | Goods cleared and delivered to warehouse | WMS | Warehouse Management |
| 9 | Landed cost finalized (product + freight + insurance + duty + brokerage + port charges) | Cost Management | Cost Management |
| 10 | Inventory valued at full landed cost | Inventory | Inventory Management |
| 11 | AP invoice matched and processed (including customs broker invoices) | Payables | Payables |

---

### PROC-EPM-001: Annual Budget Cycle

**Trigger:** Annual budget season (October - December for following year).  
**Frequency:** Annual with monthly rolling updates.

| Step | Activity | System | Oracle Module |
|------|----------|--------|---------------|
| 1 | Strategic priorities and targets communicated by CEO/Board | Narrative Reporting | Narrative Reporting |
| 2 | Revenue targets set by store/region/category (top-down + bottom-up) | EPM Planning | Planning |
| 3 | COGS budget based on planned product mix and target margins | EPM Planning | Planning |
| 4 | OpEx budget by department (labor, rent, utilities, marketing, admin) | EPM Planning | Planning |
| 5 | Capex budget (new stores, renovations, IT projects) | EPM Planning Capital Planning | Planning |
| 6 | Headcount and compensation budget | EPM Workforce Planning + HCM | Planning + HCM |
| 7 | Budget consolidated and reviewed by CFO | EPM Planning | Planning |
| 8 | Board approves budget | Narrative Reporting | Narrative Reporting |
| 9 | Budget loaded into Oracle ERP as control budgets | GL + Budget Control | General Ledger |
| 10 | Monthly actual-vs-budget variance reporting begins | ERP Analytics | Analytics |
| 11 | Monthly rolling reforecast (if actuals deviate >5% from plan) | EPM Planning | Planning |

---

### PROC-RMC-001: Quarterly Access Review and Compliance

**Trigger:** End of quarter.  
**Frequency:** Quarterly.

| Step | Activity | System | Oracle Module |
|------|----------|--------|---------------|
| 1 | Access certification campaign initiated | Advanced Controls | Risk Management |
| 2 | Managers review their team's Oracle Fusion access rights | Advanced Controls | Risk Management |
| 3 | SoD violations identified and remediated | Advanced Controls | Risk Management |
| 4 | Orphan accounts and unused access removed | Advanced Controls | Risk Management |
| 5 | Certification completed and documented | Advanced Controls | Risk Management |
| 6 | Audit report generated for internal audit review | Advanced Controls | Risk Management |
