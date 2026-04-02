# 03 — ORACLE FUSION CLOUD MODULE MAPPING

## 3.1 Module-to-Business Function Matrix

This section maps every Oracle Fusion Cloud module to specific Tahanan Depot business functions, showing how each feature is utilized.

---

## 3.2 Financial Management (Oracle Cloud ERP — Financials)

### 3.2.1 General Ledger

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Multi-ledger | Primary ledger per legal entity (5 ledgers), all in PHP, PFRS (Philippine Financial Reporting Standards) |
| Chart of Accounts | 7-segment flexfield (Company-Region-CostCenter-Account-ProductCat-IC-Future) |
| Journal Entry | Automated from subledgers (POS via Accounting Hub, AP, AR, Assets, Projects); manual for adjustments |
| Period Close | Monthly close process with automated task manager; 5 working day close target |
| Consolidation | Monthly consolidation via EPM Financial Consolidation; intercompany elimination |
| Allocations | Store rent allocation from Property to Retail; IT cost allocation from Digital to all entities |
| Reporting | Financial statements (PFRS-compliant), management reports by store/region/category |
| AI Capabilities | Anomaly detection on journal entries; AI-suggested allocations |

### 3.2.2 Payables

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Supplier Invoices | 3-way match (PO-Receipt-Invoice) for merchandise; 2-way match for services |
| Payments | Batch payments via PESONet, InstaPay, checks; scheduled payment runs |
| Expense Reports | Integration with Expenses module; corporate credit card feeds |
| Supplier Onboarding | Self-service supplier portal for registration and document submission |
| Invoice Automation | AI-powered invoice scanning (OCR), auto-coding, exception handling |
| Payment Terms | Standard terms: Net 30/45/60 per supplier contract; early payment discount capture |
| Withholding Tax | Automated expanded withholding tax (EWT) per BIR rules ( varies by expense type) |
| Aging Analysis | Weekly AP aging reports; AI-predicted cash requirements |

### 3.2.3 Receivables

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Customer Invoices | Auto-generated from POS (BIR-registered receipts/invoices via Accounting Hub) |
| Credit Memos | Returns processing, promotional allowances |
| Collections | Automated dunning for B2B accounts (contractor credit accounts) |
| Customer Statements | Monthly statements for B2B credit customers |
| Receipt Application | Cash application from POS daily deposits, bank statement integration |
| Credit Management | Credit limits for contractor/B2B accounts; automated credit scoring |
| Revenue Recognition | IFRS 15 compliance for gift cards, loyalty points, installation services, promotions |
| Aging Analysis | AR aging for B2B receivables; bad debt provisioning |

### 3.2.4 Cash Management

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Bank Accounts | 5 major banks (BDO, BPI, Metrobank, PNB, Security Bank); 120+ store collection accounts |
| Bank Reconciliation | Daily auto-reconciliation via bank statement imports |
| Cash Positioning | Real-time cash visibility across all entities and accounts |
| Cash Forecasting | AI-powered 13-week rolling cash forecast |
| Cash Pooling | Zero-balance sweeping from store accounts to concentration accounts |

### 3.2.5 Assets

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Fixed Assets | Store fixtures, warehouse equipment, IT hardware, vehicles |
| Depreciation | Straight-line per Philippine tax rules; different useful lives per asset category |
| Asset Capitalization | Automated from AP invoices and Projects (store buildout projects) |
| Asset Transfers | Between stores/departments with automatic recalculation |
| Impairment | Annual impairment review per PFRS requirements |
| Asset Retirement | Disposal processing with gain/loss recognition |

### 3.2.6 Expenses

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Expense Reports | Travel, entertainment, business development expenses |
| Per Diems | Philippine per diem rates by city classification |
| Corporate Cards | Fuel cards, corporate credit cards; automatic feed integration |
| Policy Enforcement | Automated policy checks per expense type; approval routing |
| Receipt Capture | Mobile receipt scanning with OCR |

### 3.2.7 Accounting Hub

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Subledger Accounting | POS transaction journalization; custom subledger accounting rules |
| Transaction Source | POS system as external transaction source via OIC integration |
| Journal Mapping | POS transaction types mapped to GL accounts automatically |
| Tax Determination | BIR VAT (12%), EWT calculations from POS transactions |

---

## 3.3 Procurement

### 3.3.1 Supplier Management

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Supplier Registration | Self-service portal; BIR, SEC, DTI document collection |
| Supplier Qualification | Scoring based on quality, delivery, price competitiveness |
| Supplier Classification | Local importer, direct manufacturer, distributor, service provider |
| Supplier Evaluation | Quarterly scorecard: on-time delivery, quality, fill rate, invoice accuracy |
| Supplier Blacklist | Compliance-based disqualification management |

### 3.3.2 Sourcing

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| RFQ | Competitive bidding for major categories; minimum 3 quotes per requirement |
| Bid Analysis | Total cost of ownership evaluation; landed cost simulation |
| Award Decision | Committee-based award for purchases >PHP 5M; auto-award below threshold |
| Negotiation | Online negotiation events for annual supply agreements |

### 3.3.3 Purchasing

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Purchase Orders | Automated from MRP/supply planning; blanket orders for recurring items |
| Blanket Agreements | Annual supply agreements with scheduled releases |
| Requisitioning | Self-service requisitions for non-merchandise items (store supplies, capex) |
| Approval Workflow | Multi-tier: Store Manager < PHP 50K, Regional Director < PHP 500K, VP < PHP 5M, CFO < PHP 20M |
| Auto-Create PO | From approved requisitions; auto-assignment to best supplier per sourcing rules |
| Change Orders | Version-controlled change management for PO modifications |

### 3.3.4 Procurement Contracts

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Contract Repository | Centralized contract database with renewal alerts |
| Standard Terms | Pre-approved T&C templates per supplier category |
| Rebate Management | Volume rebate tracking; quarterly rebate reconciliation |
| Contract Compliance | Automated matching of PO terms against contract terms |

---

## 3.4 Supply Chain Management (SCM)

### 3.4.1 Supply Chain Planning

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Demand Planning | AI-driven demand forecasting at store-SKU level; seasonal patterns (typhoon season, Christmas) |
| Supply Planning | MRP-based replenishment planning; min-max for slow movers |
| Sales & Operations Planning | Monthly S&OP meetings; what-if scenarios for promotions, new store openings |
| Supply Chain Collaboration | Supplier collaboration portal for forecast sharing and order visibility |
| Promotional Planning | Forecast uplift for flyers, seasonal events, store anniversary sales |

### 3.4.2 Inventory Management

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Item Master | Centralized in PLM; ~80,000 active SKUs with full attribute classification |
| Inventory Organizations | 4 warehouses + 120 stores as inventory organizations |
| Subinventory Management | Sales floor, backroom, receiving, damaged/returns per store/warehouse |
| Locator Control | Bin/shelf location tracking in warehouses; zone-based in stores |
| Lot/Serial Control | Lot tracking for paint, cement; serial tracking for power tools, appliances |
| Shelf Life Management | FEFO for perishable goods (garden, adhesives with expiry) |
| Cycle Counting | Continuous cycle counting; ABC classification-based frequency |
| Physical Inventory | Annual wall-to-wall count per BIR requirements |
| Transfer Orders | Inter-org transfers (warehouse-to-store, store-to-store) |
| Inventory Valuation | Moving average cost; standard cost for imported items with variance tracking |

### 3.4.3 Order Management

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Sales Orders | B2B orders from contractors/developers; B2C orders from e-commerce |
| Fulfillment | Ship-from-warehouse or pick-up-in-store; transfer for stock balancing |
| Pricing | Multi-tier pricing: retail, contractor, wholesale, promotional |
| Returns | RMA processing; credit memo generation; restocking |
| Backorder Management | Automated backorder fulfillment when stock arrives |
| Global Order Promising | Available-to-promise and capable-to-promise across all locations |

### 3.4.4 Warehouse Management

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Inbound Operations | ASN-based receiving; put-away optimization |
| Outbound Operations | Wave planning, pick-pack-ship; store replenishment waves |
| Cross-Docking | Direct-to-store for fast-moving items without put-away |
| Value-Added Services | Kitting (tool sets), labeling, price sticker application |
| Returns Processing | Vendor returns and customer returns processing |
| Yard Management | Dock door scheduling for inbound/outbound trucks |
| Mobile RF | Handheld device integration for all warehouse activities |

### 3.4.5 Transportation Management

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Route Planning | Optimized delivery routes from warehouses to stores |
| Carrier Management | Own fleet + 3PL partners; rate comparison and selection |
| Freight Costing | Actual vs. planned freight cost analysis |
| Proof of Delivery | Digital POD capture; delivery confirmation integration |
| Fleet Management | Company-owned truck tracking and maintenance scheduling |

### 3.4.6 Global Trade Management

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Import Management | Import declaration, customs documentation for imported products |
| Duty Management | Automated duty calculation; preferential tariff (ASEAN FTA) |
| Compliance | BOC (Bureau of Customs) compliance; restricted goods screening |
| Landed Cost | Full landed cost calculation (product + freight + duty + insurance + handling) |

### 3.4.7 Product Lifecycle Management

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Item Setup | New item introduction workflow; cross-functional approval |
| Product Classification | UNSPSC-based classification; department-class-subclass-item hierarchy |
| Quality Management | Incoming quality inspection; vendor quality tracking |
| Product Phase-Out | Discontinuation workflow with sell-through planning |
| Master Data Management | Golden record for items across all systems (POS, WMS, ERP) |
| Specification Management | Product specs, safety data sheets, installation guides |

---

## 3.5 Human Capital Management (HCM)

### 3.5.1 Core HR

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Person Management | Employee and contingent worker records across all 5 legal employers |
| Organization Management | Position-based hierarchy; 6,500 headcount across all entities |
| Assignment Management | Multi-assignment support for employees working across entities |
| Person Gallery | Photo, documents, certificates, training records |
| Workforce Modeling | What-if modeling for new store openings, restructuring |
| Strategic Workforce Planning | Headcount planning aligned with expansion targets |
| Benefits | SSS, PhilHealth, Pag-IBIG, HMO (Maxicare/Medicard), life insurance, 13th month, de minimis benefits |
| Work Life | Employee self-service for personal info, payslips, tax documents |

### 3.5.2 Talent Management

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Recruiting | Internal and external job postings; AI-powered candidate matching |
| Onboarding | Structured 30-60-90 day onboarding journeys via Oracle ME Journeys |
| Learning | Mandatory trainings (safety, compliance), product knowledge, leadership development |
| Career Development | Career paths by role family; internal mobility marketplace |
| Performance Management | Quarterly check-ins + annual performance review; cascading goals |
| Compensation | Market-based salary structures; merit increases; variable pay (store bonus) |
| Succession Planning | Key position succession plans; talent reviews (9-box grid) |
| Dynamic Skills | Skills taxonomy; skills gap analysis; recommended learning paths |
| Opportunity Marketplace | Internal gig opportunities across entities and departments |

### 3.5.3 Workforce Management

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Time and Labor | Clock-in/clock-out via POS terminals or biometric devices; OT calculation per Philippine labor law |
| Absence Management | Vacation leave, sick leave, special leave (maternity, paternity, bereavement, solo parent, VAWC) per DOLE |
| Workforce Scheduling | AI-optimized store scheduling based on traffic patterns, sales forecasts, labor budgets |
| Workforce Health & Safety | Incident reporting, safety inspections, COVID/health protocols |
| Workforce Labor Optimization | Labor cost vs. sales productivity analysis |

### 3.5.4 Payroll

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Payroll Processing | Semi-monthly payroll (15th and 30th); Philippine statutory deductions |
| Statutory Deductions | SSS (employee + employer), PhilHealth, Pag-IBIG, Withholding Tax (TRAIN law brackets) |
| Final Pay | Separation pay computation per Philippine labor law |
| 13th Month Pay | Mandatory 13th month computation and scheduling |
| Bank Files | Payroll bank file generation for major banks |
| Payslips | Digital payslips via Oracle ME |

### 3.5.5 Oracle ME (Employee Experience Platform)

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Communicate | Company announcements, policy updates, store-level communications |
| Journeys | Onboarding, offboarding, promotion, transfer, compliance workflows |
| Grow | Career development plans, skill recommendations, mentorship connections |
| Celebrate | Peer recognition, service awards, birthday/work anniversary celebrations |
| Touchpoints | Manager-employee 1-on-1 scheduling, engagement pulse surveys |
| Connections | Employee networking, interest groups, communities of practice |
| HR Help Desk | Employee inquiries (benefits, payroll, policies); ticket-based resolution |
| Digital Assistant | AI chatbot for common HR queries (leave balance, payslip, policies) |

---

## 3.6 Enterprise Performance Management (EPM)

### 3.6.1 Planning

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Financial Planning | Annual budget (revenue, COGS, OpEx, capex) by entity/region/store/category |
| Workforce Planning | Headcount and labor cost planning aligned with expansion |
| Capital Planning | Store buildout, renovation, IT infrastructure capex planning |
| Project Planning | ROI modeling for new stores, warehouse expansions |
| Sales Planning | Revenue forecast by store/category with AI-driven predictions |
| Scenario Modeling | What-if for economic downturns, supply chain disruption, typhoon impact |
| Rolling Forecasts | Monthly reforecast with actual-vs-plan variance analysis |

### 3.6.2 Financial Consolidation and Close

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Multi-Entity Consolidation | Monthly consolidation of 5 legal entities |
| Intercompany Elimination | Automated IC elimination for intercompany transactions |
| Currency Translation | PHP functional currency; USD reporting for foreign stakeholders |
| Close Tasks | Orchestrated close checklist with task assignments and deadlines |
| Journal Entries | Automated elimination, adjustment, and consolidation journals |

### 3.6.3 Account Reconciliation

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Balance Sheet Reconciliation | Monthly reconciliation of all balance sheet accounts |
| Transaction Matching | Auto-matching of intercompany, bank, and POS transactions |
| Risk Rating | Auto-profiling of reconciliation risk (high/medium/low) |
| Compliance | Audit-ready reconciliation documentation |

### 3.6.4 Tax Reporting

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Income Tax Provision | Quarterly corporate income tax provision per TRAIN law (RCIT 30% or MCIT 2%) |
| VAT Reporting | Monthly VAT returns (BIR Form 2550Q/2550M) data preparation |
| Withholding Tax | Expanded withholding tax tracking and reporting (BIR Form 1601-E/Q) |
| Country-by-Country Reporting | Not applicable (domestic only) |
| Tax Compliance Calendar | Automated tax filing reminders per BIR deadlines |

### 3.6.5 Narrative Reporting

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Management Reports | Monthly management discussion and analysis (MD&A) |
| Board Reports | Quarterly board of directors' reports |
| Regulatory Reports | SEC annual report, BIR compliance reports |
| Narrative Analysis | Store performance narratives with embedded data |

### 3.6.6 Profitability and Cost Management

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Store Profitability | P&L by store (revenue, COGS, gross margin, labor, rent, OpEx, net margin) |
| Category Profitability | Margin analysis by product department/class/subclass |
| Channel Profitability | In-store vs. e-commerce vs. B2B contractor channel |
| Customer Profitability | B2B customer profitability including cost-to-serve |
| Cost Allocation | Shared services cost allocation (IT, HR, Finance) to business units |
| Transfer Pricing | Intercompany pricing between entities at arm's length |

### 3.6.7 Enterprise Data Management

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Master Data Governance | Approval workflows for new items, customers, suppliers, cost centers |
| Hierarchy Management | Org hierarchy, product hierarchy, cost center hierarchy management |
| Change Visualization | Impact analysis for master data changes |
| Data Quality | Automated data quality checks and cleansing |

---

## 3.7 Customer Experience (CX)

### 3.7.1 Marketing

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Campaign Management | Monthly promotional campaigns (flyers, digital ads, SMS) |
| Marketing Automation | Triggered campaigns: abandoned cart, post-purchase, birthday offers |
| Customer Data Platform | Unified customer profiles from POS, e-commerce, loyalty program |
| Behavioral Intelligence | Website and app analytics; in-store purchase pattern analysis |
| Loyalty Management | Tahanan Rewards loyalty program (points-based, tiered membership) |

### 3.7.2 Sales

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Sales Force Automation | B2B sales team management for contractor/developer accounts |
| Sales Planning | Territory planning, quota management for B2B team |
| CPQ (Configure-Price-Quote) | Custom project quoting (e.g., complete kitchen buildout packages) |
| Commerce | E-commerce platform (tahanandepot.com.ph) with product catalog |
| Partner Relationship Management | Dealer/installer partner program management |
| Subscription Management | Tool rental subscriptions, maintenance service contracts |

### 3.7.3 Service

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Field Service | Delivery scheduling and tracking; installation service dispatch |
| Service Center (Contact Center) | Customer support hotline, email, chat |
| Digital Customer Service | Self-service portal for order tracking, returns initiation, FAQ |
| Knowledge Management | Product guides, DIY tutorials, FAQ database |

---

## 3.8 Risk Management and Compliance

### 3.8.1 Advanced Controls

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Segregation of Duties | SoD rules for all finance and procurement roles |
| Access Certification | Quarterly user access review and certification |
| Continuous Monitoring | Real-time monitoring of high-risk transactions |
| Configuration Controls | Track and validate system configuration changes |
| Transaction Controls | Automated fraud detection on AP, AR, expense transactions |
| Audit Workflows | Audit trail for SOX-equivalent (ICFR) compliance |

---

## 3.9 Integration & Analytics

### 3.9.1 Oracle Integration Cloud (OIC)

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| Application Integration | POS-to-Oracle Fusion real-time integration |
| Process Automation | Automated approval workflows across modules |
| Prebuilt Adapters | REST/SOAP adapters for POS, bank, logistics providers |
| API Management | API gateway for POS integration, partner APIs |
| B2B Integration | EDI with major suppliers; AS2 for large retailer formats |

### 3.9.2 Fusion Data Intelligence

| Feature | Tahanan Depot Usage |
|---------|---------------------|
| ERP Analytics | Financial dashboards, P&L by entity/store/category |
| SCM Analytics | Inventory turnover, fill rate, on-time delivery, warehouse productivity |
| HCM Analytics | Turnover, time-to-fill, labor cost, training completion, diversity |
| CX Analytics | Customer acquisition cost, lifetime value, NPS, campaign ROI |
| Cross-Domain | Revenue per employee, inventory per sqm, customer satisfaction vs. revenue |
| Augmented Analytics | AI-powered anomaly detection, trend prediction, natural language queries |
