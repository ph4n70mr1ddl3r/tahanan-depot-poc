# 06 — STANDARD OPERATING PROCEDURES

## 6.1 SOP Index

| SOP ID | Title | Domain | Process Owner |
|-----------|-------|--------|---------------|
| SOP-POS-001 | POS Daily Opening Procedure | POS/Retail | Store Manager |
| SOP-POS-002 | POS Transaction Processing | POS/Retail | Store Manager |
| SOP-POS-003 | POS Daily Closing and Z-Reading | POS/Retail | Store Manager |
| SOP-POS-004 | POS Returns and Exchanges | POS/Retail | Store Manager |
| SOP-POS-005 | POS Offline Mode Operation | POS/IT | Store Manager |
| SOP-SCM-001 | Warehouse Receiving Procedure | Supply Chain | Warehouse Manager |
| SOP-SCM-002 | Warehouse Put-Away Procedure | Supply Chain | Warehouse Manager |
| SOP-SCM-003 | Store Replenishment Pick-Pack-Ship | Supply Chain | Warehouse Manager |
| SOP-SCM-004 | Store Receiving Procedure | Supply Chain/Retail | Store Manager |
| SOP-SCM-005 | Cycle Count Procedure | Supply Chain | Inventory Control Clerk |
| SOP-SCM-006 | Inventory Adjustment Procedure | Supply Chain | Controller |
| SOP-FIN-001 | Daily Cash Reconciliation | Finance | Store Finance Analyst |
| SOP-FIN-002 | Monthly Financial Close Procedure | Finance | Controller |
| SOP-FIN-003 | Supplier Invoice Processing | Finance | AP Manager |
| SOP-FIN-004 | B2B Customer Billing | Finance | AR Manager |
| SOP-HR-001 | New Hire Onboarding Procedure | HR | HR Coordinator |
| SOP-HR-002 | Payroll Processing Procedure | HR/Payroll | Payroll Manager |
| SOP-HR-003 | Leave Application and Approval | HR | Employee/Manager |
| SOP-HR-004 | Employee Separation Procedure | HR | HR Business Partner |
| SOP-CX-001 | Customer Complaint Handling | Customer Service | Service Manager |
| SOP-CX-002 | Loyalty Point Adjustment | CX | Loyalty Manager |
| SOP-IT-001 | POS Incident Escalation | IT | L1/L2 Support |

---

## 6.2 POS Standard Operating Procedures (Detail)

### SOP-POS-001: POS Daily Opening Procedure

**Responsible:** Assigned Cashier / Store Supervisor  
**Timing:** 30 minutes before store opening  
**Systems:** Custom POS, Oracle Time & Labor

| Step | Action | Detail |
|------|--------|--------|
| 1 | Clock in | Cashier clocks in at POS terminal or biometric device; auto-recorded in Oracle Time & Labor |
| 2 | Log in to POS | Cashier logs in with unique credentials; POS verifies active shift assignment from Workforce Scheduling |
| 3 | Verify terminal readiness | Confirm network connectivity indicator (green = online to Oracle Fusion via OIC), printer status, scanner function |
| 4 | Count opening float | Count assigned cash drawer; enter opening amount in POS; must match standard float (PHP 5,000) |
| 5 | Confirm start-of-day sync | Verify POS displays "Synced" status confirming latest prices, promotions, and item data from Oracle |
| 6 | Begin accepting transactions | Store opens; cashier processes transactions per SOP-POS-002 |

**Exception Handling:**
- If POS cannot connect to Oracle: Enter offline mode per SOP-POS-005.
- If cash drawer count mismatch: Report to Store Supervisor immediately; document variance.

---

### SOP-POS-002: POS Transaction Processing

**Responsible:** Cashier  
**Systems:** Custom POS, Oracle Fusion (via OIC real-time)

| Step | Action | Detail |
|------|--------|--------|
| 1 | Greet customer | Standard greeting script |
| 2 | Scan items | Scan barcode; POS validates item against Oracle item master (via local cache + real-time verification). If item not found, manually enter SKU or call supervisor |
| 3 | Verify quantity and pricing | Display running total; customer can verify on customer-facing display |
| 4 | Apply promotions | POS auto-applies promotions from Oracle Pricing rules; manual discount requires supervisor override with reason code |
| 5 | Apply loyalty card | Scan or enter loyalty number; POS retrieves points balance from Oracle CX Loyalty (via OIC); display earned points |
| 6 | Process payment | Select payment method: |
| | | **Cash:** Enter amount tendered; POS calculates change; drawer opens |
| | | **Debit/Credit:** Card terminal processes; POS awaits approval; signature/waiver per card type |
| | | **E-Wallet (GCash/Maya):** Generate QR or enter mobile number; await confirmation |
| | | **Gift Card:** Scan/enter gift card number; validate balance from Oracle Revenue Mgmt; deduct amount |
| | | **Loyalty Points:** Enter points to redeem; validate balance; convert to PHP discount (1 pt = PHP 1) |
| | | **Mixed Payment:** Process multiple payment methods on single transaction |
| 7 | Generate receipt | POS prints BIR-compliant Official Receipt or Sales Invoice with: Tahanan TIN, BIR permit number, sequential receipt number, VAT breakdown, item detail |
| 8 | Complete transaction | POS posts transaction to OIC within 30 seconds; OIC routes to Oracle AR + GL + Inventory + Loyalty |

**Price Override Rules:**
- Cashier cannot override prices.
- Supervisor override allowed for: ad price match (with proof), damaged goods markdown (per POL-RET-002).
- All overrides logged with reason code, supervisor ID, and timestamp.

**Void/Cancel Rules:**
- Current transaction void: Cashier can void entire transaction before payment (requires supervisor if > PHP 5,000).
- Post-payment void: Treated as return per SOP-POS-004.

---

### SOP-POS-003: POS Daily Closing and Z-Reading

**Responsible:** Cashier + Store Supervisor  
**Timing:** At end of cashier's shift or store closing  
**Systems:** Custom POS, Oracle Cash Management

| Step | Action | Detail |
|------|--------|--------|
| 1 | Stop accepting transactions | Cashier disables terminal for new transactions |
| 2 | Generate Z-reading | POS generates end-of-day Z-reading report: total sales, transaction count, payment method breakdown, voids, returns, discounts, VAT |
| 3 | Count cash drawer | Cashier counts physical cash; compare to Z-reading expected cash amount |
| 4 | Record variance | Enter actual count in POS; system calculates variance; auto-flags if > PHP 100 |
| 5 | Prepare bank deposit | Supervisor prepares deposit slip matching cash total; separates checks and card settlement batch |
| 6 | Non-cash reconciliation | Verify card settlement batch total matches POS card total; verify e-wallet settlement reports |
| 7 | Supervisor sign-off | Supervisor reviews and approves Z-reading; signs off in POS |
| 8 | Upload deposit slip | Scan deposit slip and upload to Oracle Cash Management via store portal |
| 9 | Make bank deposit | Deposit made to assigned bank branch same day (or next morning if after bank hours) |
| 10 | Close shift in POS | Cashier logs out; shift record closed; data queued for OIC synchronization |
| 11 | Oracle reconciliation | Next morning: Finance team reconciles POS Z-readings against Oracle AR receipts (via automated reconciliation report) |

---

### SOP-POS-004: POS Returns and Exchanges

**Responsible:** Store Associate + Supervisor (for approval)  
**Systems:** Custom POS, Oracle Order Management, Receivables, Inventory

| Step | Action | Detail |
|------|--------|--------|
| 1 | Verify return eligibility | Check return policy (POL-RET-001): item condition, receipt, timeframe |
| 2 | Initiate return in POS | Select "Return" function; scan receipt barcode or enter receipt number; POS retrieves original transaction from local cache or Oracle (via OIC) |
| 3 | Scan returned items | Verify each item matches original transaction; check condition |
| 4 | Select resolution | Refund (to original payment method), exchange (select replacement item), or store credit (issue store credit note) |
| 5 | Supervisor approval | Supervisor authorizes return (mandatory for refunds > PHP 5,000; exchanges > PHP 10,000) |
| 6 | Process return | POS processes return; generates return receipt (BIR-compliant credit memo format) |
| 7 | Update inventory | Returned item inventory incremented in POS; synced to Oracle Inventory (resalable → Sales Floor; damaged → Damaged subinventory) |
| 8 | Financial update | OIC routes return to Oracle: AR credit memo, GL reversal journal, COGS reversal |
| 9 | Refund execution | Cash refund from drawer, card refund initiated, or store credit issued |
| 10 | Log return reason | Cashier selects reason code from dropdown: Defective, Wrong Item, Changed Mind, Other (specify) |
| 11 | Offer survey | Prompt customer satisfaction survey (optional) |

---

### SOP-POS-005: POS Offline Mode Operation

**Responsible:** Store Manager + IT Support  
**Systems:** Custom POS (offline mode), Oracle Fusion (deferred sync)

| Step | Action | Detail |
|------|--------|--------|
| 1 | Detect connectivity loss | POS auto-detects loss of OIC connection; displays "OFFLINE MODE" banner on all terminals |
| 2 | Continue operations | POS continues to process transactions using local item cache, price file, and loyalty data (last synced) |
| 3 | Local data storage | All transactions stored in local encrypted database; transaction numbers generated with offline prefix ("O-") |
| 4 | Queue for sync | POS maintains sync queue; auto-retries connection every 60 seconds |
| 5 | Monitor duration | If offline > 2 hours, Store Manager contacts IT per SOP-IT-001 |
| 6 | Connectivity restored | POS auto-syncs all queued transactions to Oracle via OIC; processes sequentially with conflict resolution |
| 7 | Reconciliation | Post-sync: Supervisor runs offline transaction reconciliation report; matches local Z-reading with Oracle-posted transactions |
| 8 | Exception handling | Any sync failures flagged for manual review by IT; transactions never lost (durable local storage) |

**Offline Mode Limitations:**
- Loyalty points earned/redeemed are estimates; reconciled upon reconnection.
- Gift card balance verification uses last-known balance; negative balance prevented by local floor limit.
- Real-time inventory not updated in Oracle until sync completes.

---

## 6.3 Supply Chain SOPs (Detail)

### SOP-SCM-001: Warehouse Receiving Procedure

**Responsible:** Receiving Clerk + Warehouse Supervisor  
**Systems:** Oracle WMS Mobile, Inventory Management

| Step | Action | Detail |
|------|--------|--------|
| 1 | Receive ASN notification | Oracle WMS displays expected inbound shipment with PO number, supplier, items, and expected quantities |
| 2 | Schedule dock door | Assign dock door via Yard Management; confirm truck arrival |
| 3 | Verify shipping documents | Check delivery receipt against PO and ASN; verify supplier, PO number, item count |
| 4 | Unload and stage | Unload goods to receiving staging area |
| 5 | Scan and verify | Using RF handheld, scan each item/pallet; system compares against PO/ASN quantities |
| 6 | Quality inspection | For designated items (per PLM quality rules): inspect for damage, check specifications, sample testing |
| 7 | Record discrepancies | Enter overages, shortages, damages in WMS; system auto-creates discrepancy report |
| 8 | Confirm receipt | Accept full or partial receipt in Oracle; inventory incremented; AP receipt created for 3-way match |
| 9 | Route to put-away | WMS generates put-away suggestions based on zone, velocity, and space availability |
| 10 | Discrepancy resolution | Notify supplier and buyer of discrepancies; file claim if damage; adjust PO as needed |

---

### SOP-SCM-002: Warehouse Put-Away Procedure

**Responsible:** Put-Away Clerk  
**Systems:** Oracle WMS Mobile, Inventory Management

| Step | Action | Detail |
|------|--------|--------|
| 1 | Receive put-away task | WMS assigns put-away task to clerk based on priority and location |
| 2 | Scan item/pallet | Clerk scans item barcode; system confirms item identity |
| 3 | Navigate to suggested location | WMS suggests optimal bin location based on item velocity, zone, and capacity |
| 4 | Confirm put-away | Scan bin barcode to confirm placement; WMS updates locator inventory |
| 5 | Complete task | Task marked complete; inventory subinventory updated from Receiving to Finished Goods |

---

### SOP-SCM-003: Store Replenishment Pick-Pack-Ship

**Responsible:** Picker, Packer, Shipping Clerk  
**Systems:** Oracle WMS Mobile, Inventory Management, TMS

| Step | Action | Detail |
|------|--------|--------|
| 1 | Wave release | WMS releases daily replenishment wave based on transfer orders generated by supply planning |
| 2 | Pick tasks assigned | WMS assigns pick tasks to pickers based on zone and priority |
| 3 | Pick items | Picker scans item and bin location; system verifies correct pick |
| 4 | Pack into store totes/cases | Packer verifies items against packing list; scans into store-labeled containers |
| 5 | Generate shipping documents | System generates bill of lading, packing list, store delivery manifest |
| 6 | Load truck | Shipping clerk confirms loading; TMS records shipment |
| 7 | Ship confirmation | WMS confirms shipment; inventory decremented at warehouse; in-transit inventory created |
| 8 | Track delivery | TMS tracks delivery to store; ETA visible to store team |

---

### SOP-SCM-004: Store Receiving Procedure

**Responsible:** Receiving Associate + Store Supervisor  
**Systems:** Custom POS (Receiving Module), Oracle Inventory Management

| Step | Action | Detail |
|------|--------|--------|
| 1 | Receive delivery notification | Store notified of incoming shipment via Oracle (email + store portal) |
| 2 | Verify delivery documents | Check delivery manifest against expected transfer orders |
| 3 | Unload and count | Unload goods; count each item against manifest |
| 4 | Enter receipt in POS | POS Receiving Module: scan or enter received quantities per item |
| 5 | Flag discrepancies | Note over/short/damaged items; enter discrepancy in POS with photo evidence |
| 6 | Put away | Move goods to designated subinventory (sales floor or backroom) |
| 7 | Confirm receipt | POS syncs receipt to Oracle via OIC; inventory incremented at store; in-transit cleared |
| 8 | Discrepancy resolution | Receiving supervisor reviews discrepancies; initiates claim or adjustment per POL-SCM-003 |

---

### SOP-SCM-005: Cycle Count Procedure

**Responsible:** Inventory Control Clerk + Supervisor  
**Systems:** Oracle Inventory Management, POS

| Step | Action | Detail |
|------|--------|--------|
| 1 | Generate count list | Oracle generates cycle count list based on ABC classification and schedule |
| 2 | Print or load to mobile | Count list distributed to counters (printed or on POS mobile device) |
| 3 | Physical count | Two-person count team counts items independently |
| 4 | Enter counts | Counts entered into Oracle or POS; system compares to system quantity |
| 5 | Recount variances | Items with variance > tolerance recount by different team |
| 6 | Approve adjustments | Supervisor reviews and approves adjustments; controller approves if > PHP 10,000 |
| 7 | Post adjustments | Inventory adjusted; GL journal created for variance |
| 8 | Analyze root cause | Recurring variances investigated; shrinkage report generated monthly |

---

### SOP-SCM-006: Inventory Adjustment Procedure

**Responsible:** Store/Warehouse Inventory Control + Controller  
**Systems:** Oracle Inventory Management

| Step | Action | Detail |
|------|--------|--------|
| 1 | Identify adjustment need | From cycle count, damage, theft, write-off, or system correction |
| 2 | Create adjustment request | Submitter creates adjustment in Oracle Inventory with reason code and supporting documentation |
| 3 | Approval workflow | Auto-routed per threshold: |
| | | < PHP 5,000: Store/Warehouse Supervisor |
| | | PHP 5,001 - 50,000: Regional Director / VP Supply Chain |
| | | > PHP 50,000: VP Finance + VP Supply Chain |
| 4 | Post adjustment | Upon approval, inventory adjusted; GL journal auto-created |
| 5 | Document and file | Supporting documents attached to transaction in Oracle |
| 6 | Monthly review | Controller reviews all adjustments monthly for patterns and control effectiveness |

---

## 6.4 Finance SOPs (Detail)

### SOP-FIN-001: Daily Cash Reconciliation

**Responsible:** Store Finance Analyst + Store Supervisor  
**Timing:** Daily, before 10:00 AM following business day  
**Systems:** Oracle Cash Management, Receivables

| Step | Action | Detail |
|------|--------|--------|
| 1 | Collect all POS Z-readings | Gather Z-reading reports from all terminals across all shifts |
| 2 | Import bank statement | Auto-import bank statement via Cash Management bank feed |
| 3 | Match POS receipts to bank deposits | System auto-matches using reference numbers (store code + date + terminal sequence) |
| 4 | Review unmatched items | Investigate unmatched deposits or receipts; resolve within 2 business days |
| 5 | Record cash variances | Document and investigate variances > PHP 100 per terminal |
| 6 | Confirm reconciliation | Store Finance Analyst confirms daily reconciliation in Oracle |
| 7 | Escalate exceptions | Unresolved items > PHP 1,000 escalated to VP Finance |

---

### SOP-FIN-002: Monthly Financial Close Procedure

**Responsible:** Controller + Finance Team  
**Timing:** First 5 business days of following month  
**Systems:** Oracle Financial Consolidation & Close, GL, all subledgers

| Day | Activity | Owner |
|-----|----------|-------|
| Day 1 | Close all subledgers (POS, AP, AR, Assets); complete intercompany matching | Subledger Teams |
| Day 1 | Complete all store cash reconciliations | Store Finance |
| Day 2 | Post all manual journals (reclassifications, adjustments) | Controller |
| Day 2 | Complete account reconciliations (auto-matched accounts) | Account Reconciliation |
| Day 3 | Complete manual account reconciliations; resolve exceptions | Account Reconciliation |
| Day 3 | Run depreciation; review asset additions and disposals | Fixed Asset Accountant |
| Day 4 | Intercompany elimination and consolidation run | Consolidation Team |
| Day 4 | Tax provision computed; VAT return data prepared | Tax Team |
| Day 5 | Management review of consolidated P&L and Balance Sheet | CFO + VP Finance |
| Day 5 | Close GL periods for all entities | Controller |
| Day 6-7 | Variance analysis and management reporting | FP&A |
| Day 10 | Board-level financial summary distributed | CFO |

---

### SOP-FIN-003: Supplier Invoice Processing

**Responsible:** AP Specialist + AP Manager  
**Systems:** Oracle Payables, Supplier Portal

| Step | Action | Detail |
|------|--------|--------|
| 1 | Receive invoice | Supplier submits via Supplier Portal (preferred) or AP captures from email (AI OCR) |
| 2 | Validate invoice | AP validates: supplier active, PO reference valid, invoice within PO terms |
| 3 | 3-way match | System auto-matches: PO price × qty = Invoice; PO qty ≥ Receipt qty ≥ Invoice qty |
| 4 | Resolve exceptions | Match failures routed to buyer/receiving for resolution |
| 5 | Compute EWT | System auto-computes expanded withholding tax per BIR rate table based on expense type |
| 6 | Approval routing | Matched invoice routed per approval matrix (POL-FIN-001) |
| 7 | Schedule payment | Approved invoice scheduled for payment per supplier terms (Net 30/45/60) |
| 8 | Generate payment | Payment batch generated; bank file created for PESONet/check |
| 9 | Record payment | Payment recorded; GL updated; supplier balance reduced |
| 10 | File BIR Form 1601 | Monthly EWT remittance to BIR compiled from withholding data |

---

### SOP-FIN-004: B2B Customer Billing

**Responsible:** AR Specialist + AR Manager  
**Systems:** Oracle Receivables, Order Management

| Step | Action | Detail |
|------|--------|--------|
| 1 | Order fulfilled and confirmed | Order Management confirms delivery; POD captured |
| 2 | Generate invoice | Oracle AR generates BIR-compliant Sales Invoice from sales order |
| 3 | Send invoice | Invoice sent to customer via email + customer portal |
| 4 | Apply credit terms | Terms applied per customer credit tier (Net 30/45/60) |
| 5 | Monitor aging | AR aging report monitored weekly; auto-dunning per collections policy (POL-FIN-004) |
| 6 | Receive payment | Customer payment received via bank transfer or check |
| 7 | Apply receipt | Payment applied to invoice in AR; GL updated |
| 8 | Reconcile | Monthly reconciliation of AR subledger to GL |

---

## 6.5 HR SOPs (Detail)

### SOP-HR-001: New Hire Onboarding Procedure

**Responsible:** HR Coordinator + Hiring Manager  
**Systems:** Oracle HCM, Oracle ME

| Day | Activity | System |
|-----|----------|--------|
| Pre-Day 1 | Complete pre-boarding requirements checklist (sent via Oracle ME Journeys) | Oracle ME Journeys |
| Pre-Day 1 | IT provisions accounts (email, Oracle Fusion, POS, building access) | IT + HCM |
| Pre-Day 1 | Workspace/cashier station prepared; uniform issued | Facilities / Store Ops |
| Day 1 | Employee reports; HR verifies documents (NBI, medical, credentials) | Core HR |
| Day 1 | Employee record activated in Oracle Core HR | Core HR |
| Day 1 | Benefits enrollment completed (SSS, PhilHealth, Pag-IBIG, HMO) | Benefits |
| Day 1 | Safety orientation and tour (mandatory) | Learning |
| Day 1 | Oracle Fusion and POS system access training | Learning |
| Week 1 | Department-specific training program begins | Learning |
| Week 1 | Probationary goals set in Performance Management | Performance Mgmt |
| Day 30 | 30-day check-in (manager + HR) via Oracle Touchpoints | ME Touchpoints |
| Day 60 | 60-day check-in; training completion review | ME Touchpoints |
| Day 90 | 90-day review; confirm fit for role | ME Touchpoints |
| Month 5 | Probationary evaluation completed; regularization decision | Performance Mgmt |
| Month 6 | If passed: Regularized; compensation confirmed; notice issued | Core HR |

---

### SOP-HR-002: Payroll Processing Procedure

**Responsible:** Payroll Manager + HR + Finance  
**Timing:** Semi-monthly (cut-off: 10th and 25th; pay date: 15th and 30th)  
**Systems:** Oracle Payroll, Time & Labor, Absence Management

| Step | Timing | Activity |
|------|--------|----------|
| 1 | Cut-off day | All timecards must be approved by supervisors |
| 2 | Cut-off + 1 | Payroll Manager validates timecard data, absences, OT, adjustments |
| 3 | Cut-off + 1 | Run payroll calculation in Oracle Payroll |
| 4 | Cut-off + 2 | Generate payroll register; review by HR Manager and Finance Controller |
| 5 | Cut-off + 2 | Approve payroll batch |
| 6 | Cut-off + 2 | Generate bank files per bank format |
| 7 | Cut-off + 2 | Transmit bank files to respective banks |
| 8 | Pay date | Employee receives salary in bank account |
| 9 | Pay date | Digital payslips available in Oracle ME |
| 10 | Pay date + 1 | GL journal posted for payroll expense and liabilities |
| 11 | Monthly | Statutory remittances prepared (SSS Form R5, PhilHealth ER2, Pag-IBIG MCRF, BIR 1601-C/W) |
| 12 | Monthly | BIR Form 1604-C (annual withholding on compensation) reconciliation |

---

### SOP-HR-003: Leave Application and Approval

**Responsible:** Employee + Direct Supervisor + HR  
**Systems:** Oracle Absence Management, Oracle ME

| Step | Action | Detail |
|------|--------|--------|
| 1 | Employee submits leave request | Via Oracle ME mobile app or web; selects leave type, dates, reason |
| 2 | System validates balance | Oracle Absence Management checks leave balance and work schedule |
| 3 | Auto-routing | Request routed to direct supervisor for approval |
| 4 | Supervisor approves/rejects | Approve: Leave deducted from balance; team calendar updated. Reject: Reason provided to employee |
| 5 | Notification | Employee and team notified of approved leave |
| 6 | Emergency leave | Retroactive application allowed within 3 days; requires HRBP approval |
| 7 | Special leave (maternity, etc.) | Requires HR documentation (medical cert, marriage cert, etc.) uploaded to Oracle HCM |

---

### SOP-HR-004: Employee Separation Procedure

**Responsible:** HR Business Partner + Hiring Manager + Finance + IT  
**Systems:** Oracle HCM, Oracle ME, all modules

| Step | Action | Detail |
|------|--------|--------|
| 1 | Initiate separation | Manager or HR creates separation action in Core HR (resignation, termination, retirement, end of contract) |
| 2 | Due process (if applicable) | For termination: Written notices, hearing, decision per POL-HR-006 |
| 3 | Offboarding journey initiated | Oracle ME Journey triggers: clearance checklist, return of assets, knowledge transfer tasks |
| 4 | Clearance process | Employee obtains clearances from: department, IT, finance, library, HR |
| 5 | Asset return | All company assets returned (uniform, ID, laptop, keys, etc.); documented in Core HR |
| 6 | System access revocation | IT deactivates all system access within 24 hours of separation effective date |
| 7 | Final pay computation | Payroll computes final pay: last salary + proportionate 13th month + unused VL conversion + separation pay (if applicable) per DOLE rules |
| 8 | Final pay approval | Controller approves final pay computation |
| 9 | Final pay release | Released within 30 days of separation per DOLE; deposited to bank or check |
| 10 | COE and employment documents | Certificate of Employment issued; final pay slip available in ME for 30 days |
| 11 | Exit interview | Conducted by HRBP; data captured in HCM for analytics |
| 12 | Archival | Employee record archived in HCM; retained per data retention policy (10 years for tax purposes) |

---

## 6.6 Customer Experience SOPs (Detail)

### SOP-CX-001: Customer Complaint Handling

**Responsible:** Store Associate → Store Supervisor → Customer Service Manager  
**Systems:** Oracle CX Service, Knowledge Management

| Step | Action | Detail |
|------|--------|--------|
| 1 | Receive complaint | In-person (store), phone, email, social media, or e-commerce chat |
| 2 | Log in Oracle Service | Create service request with customer details, issue description, and channel |
| 3 | Classify severity | Level 1 (product inquiry), Level 2 (product issue), Level 3 (safety/compliance), Level 4 (legal/media) |
| 4 | First response | Within 4 hours (Level 1-2), within 1 hour (Level 3-4) |
| 5 | Investigate | Store Associate resolves Level 1; Supervisor resolves Level 2; Service Manager resolves Level 3-4 |
| 6 | Resolve | Offer solution per policy (exchange, refund, repair, apology, escalation to supplier) |
| 7 | Confirm resolution | Customer confirms satisfaction; service request closed with resolution code |
| 8 | Follow-up | Satisfaction survey sent within 24 hours for Level 2-4 |
| 9 | Analyze | Monthly complaint analysis by category, store, severity; root cause addressed |
| 10 | Knowledge update | Recurring issues added to Knowledge Management for future reference |

---

### SOP-CX-002: Loyalty Point Adjustment

**Responsible:** Loyalty Manager + Finance  
**Systems:** Oracle Customer Loyalty, Receivables

| Step | Action | Detail |
|------|--------|--------|
| 1 | Receive adjustment request | Customer contacts store or customer service regarding points discrepancy |
| 2 | Verify in Oracle Loyalty | Check transaction history, points earned, points redeemed, current balance |
| 3 | Determine cause | System error, missing transaction, fraudulent activity, or customer misunderstanding |
| 4 | Process adjustment | Loyalty Manager adjusts points with documented reason and evidence |
| 5 | Approval | Adjustments > 500 points require Loyalty Manager approval; > 2,000 points require VP Marketing approval |
| 6 | Notify customer | SMS/email confirmation of adjustment |
| 7 | Revenue impact | Points adjustment recorded for deferred revenue liability tracking |

---

## 6.7 IT SOPs (Detail)

### SOP-IT-001: POS Incident Escalation

**Responsible:** L1 Support → L2 POS Team → VP Digital Products  
**Systems:** Oracle CX Service, POS monitoring tools

| Level | Response Time | Scope | Examples |
|-------|--------------|-------|----------|
| L1 — Store | Immediate | Basic troubleshooting | Restart terminal, check cables, clear paper jam, re-login |
| L1 — IT Hotline | 15 minutes | Guided troubleshooting | Network reconnection, printer reset, peripheral swap, offline mode activation |
| L2 — POS Team | 1 hour | Application-level | Software bug, data sync issue, configuration error, database error |
| L3 — Architecture | 4 hours | Infrastructure-level | Server issue, OIC integration failure, Oracle Fusion connectivity, database corruption |
| Escalation to VP | 8 hours | Major incident | Store-wide outage, multi-store outage, data integrity concern |

**Rules:**
- All incidents logged in Oracle CX Service with severity level and timestamp.
- Severity 1 (store down): VP IT notified immediately; bridge call within 30 minutes.
- Post-incident review required for all Severity 1 incidents within 48 hours.
- Knowledge base updated for every resolved incident.
