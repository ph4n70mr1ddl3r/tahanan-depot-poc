# 10 — IMPLEMENTATION HISTORY & SYSTEM LANDSCAPE

## 10.1 Implementation Overview

Tahanan Depot successfully completed its Oracle Fusion Cloud and custom POS implementation over an 18-month phased rollout. All systems are now fully deployed and operational across all 120 stores, 4 warehouses, and corporate headquarters. This section documents the completed implementation for historical reference and onboarding purposes.

---

## 10.2 Completed Implementation Phases

### Phase 0: Foundation & Planning (Completed)

**Objective:** Established project governance, finalized requirements, prepared infrastructure.

| Activity | Duration | Owner | Deliverable |
|----------|----------|-------|-------------|
| Project charter and governance setup | 2 weeks | CEO + CIO | Signed project charter |
| Implementation partner selection | 3 weeks | CIO + Procurement | Contracted SI partner |
| Detailed requirements workshops (all modules) | 4 weeks | All VPs | BRD (Business Requirements Document) |
| Gap analysis (standard Fusion vs. requirements) | 2 weeks | SI Partner + Tahanan team | Gap/fit analysis document |
| OCI tenancy setup and environment provisioning | 1 week | VP Infrastructure | OCI environments (DEV, TEST, UAT, PROD) |
| Project plan and resource allocation | 2 weeks | PMO | Detailed project plan |
| Change management and communication plan | 2 weeks | CHRO + PMO | Change management plan |

**Key Decisions Made:**
- Oracle Fusion implementation partner selected (Tier 1 SI with retail experience).
- Internal project team identified: 15 full-time business leads + 10 IT resources.
- POS development team formed (8 developers, 2 QA, 1 DevOps).

---

### Phase 1: Core ERP & HCM (Completed)

**Objective:** Implemented foundational financial and HR systems.

#### Configuration & Setup

| Activity | Module |
|----------|--------|
| Enterprise structure configuration (enterprise, legal entities, BUs) | GL |
| Chart of accounts setup (7 segments) | GL |
| Ledger configuration (5 primary + 1 reporting) | GL |
| Tax configuration (VAT, EWT, WTA, CIT) | Tax |
| Business unit setup | All |
| Inventory organization setup (4 warehouses + 120 stores) | Inventory |
| HCM enterprise and legal employer setup | Core HR |
| Organization hierarchy and position setup | Core HR |
| Grade and salary structures | Compensation |
| Benefits setup (SSS, PhilHealth, Pag-IBIG, HMO) | Benefits |
| Absence plan setup (all leave types) | Absence Mgmt |
| Payroll setup (Philippine statutory deductions) | Payroll |

#### Process Implementation

| Activity | Module |
|----------|--------|
| GL journal processes and period close | GL |
| AP invoice processing and payment workflows | Payables |
| AR receipt processing and collections | Receivables |
| Cash management and bank reconciliation | Cash Mgmt |
| Fixed asset setup and depreciation | Assets |
| Expense management setup | Expenses |
| Accounting Hub setup for POS integration | Accounting Hub |
| Supplier portal setup | Supplier Mgmt |
| Recruiting configuration | Recruiting |
| Time and Labor setup | Time & Labor |
| Performance management configuration | Performance Mgmt |
| Learning content initial load | Learning |
| Oracle ME configuration (Journeys, Communicate, etc.) | ME |

**Go-Live Scope (Achieved):**
- General Ledger, Payables, Receivables, Cash Management, Assets, Expenses for all 5 entities
- Core HR, Payroll, Benefits, Absence Management for all entities
- Recruiting and Onboarding activated
- Time & Labor integrated with POS

---

### Phase 2: Supply Chain & Procurement (Completed)

**Objective:** Implemented supply chain planning, inventory, warehouse management, and procurement.

#### Configuration

| Activity | Module |
|----------|--------|
| Item master setup (initial load of ~10,000 top SKUs) | PLM |
| Product hierarchy configuration | PLM |
| Supplier master migration (~2,500 suppliers) | Supplier Mgmt |
| Sourcing configuration | Sourcing |
| Purchasing configuration (document types, approval rules) | Purchasing |
| Inventory configuration (organizations, subinventories, locators) | Inventory |
| Cost management setup | Cost Management |
| Warehouse management configuration (4 warehouses) | WMS |
| Transportation management setup | TMS |
| Global trade management setup | GTM |

#### Planning & Advanced Configuration

| Activity | Module |
|----------|--------|
| Demand planning model setup | SCP Demand |
| Supply planning configuration | SCP Supply |
| S&OP process design | SCP S&OP |
| Order management configuration | Order Management |
| Pricing engine setup (retail, contractor, wholesale) | Pricing |
| Warehouse mobile RF configuration | WMS Mobile |
| Barcode and label printing setup | WMS |
| Quality management setup | PLM Quality |

**Go-Live Scope (Achieved):**
- Full product lifecycle management
- Procurement (source-to-pay)
- Inventory management across all locations
- Warehouse management (4 DCs)
- Supply chain planning (demand, supply, S&OP)
- Order management (B2B and transfers)
- Transportation management
- Cost management
- Full item master expanded to ~80,000 active SKUs

---

### Phase 3: Custom POS Development & Integration (Completed)

**Objective:** Developed, tested, and deployed custom POS system integrated with Oracle Fusion.

#### POS Core Development

| Activity | Deliverable |
|----------|-------------|
| POS requirements finalization | POS BRD |
| UX/UI design (Filipino-optimized touchscreen) | Design mockups approved |
| Backend development (transaction engine, local DB) | Core transaction processing |
| Frontend development (checkout, returns, receiving) | POS screens |
| Payment gateway integration (GCash, Maya, card terminals) | Payment SDKs integrated |
| BIR receipt compliance | Receipt format approved |
| Offline mode development | Local caching and sync logic |

#### OIC Integration Development

| Activity | Deliverable |
|----------|-------------|
| OIC environment setup | OIC instances provisioned |
| All 18 integration flows | All flows built and unit tested |
| API security and authentication | OAuth 2.0, mTLS configured |

#### POS Deployment

| Activity | Duration | Scope |
|----------|----------|-------|
| POS lab testing (simulated environment) | 4 weeks | All transaction types, offline mode |
| Integration testing with Oracle Fusion | 4 weeks | All 18 integration flows end-to-end |
| Performance testing | 2 weeks | 500+ concurrent transactions |
| Security testing (penetration, PCI-DSS) | 2 weeks | Full POS security audit |
| Pilot store deployment (2 stores) | 4 weeks | Live in 2 pilot stores |
| Wave 1: 20 stores (Metro Manila) | 2 weeks | 20 stores, ~80 terminals |
| Wave 2: 30 stores (rest of South Luzon + North Luzon) | 2 weeks | 30 stores, ~120 terminals |
| Wave 3: 35 stores (Visayas + Mindanao) | 2 weeks | 35 stores, ~140 terminals |
| Wave 4: Remaining 33 stores | 2 weeks | 33 stores, ~130 terminals |

---

### Phase 4: EPM & Advanced Analytics (Completed)

**Objective:** Implemented planning, consolidation, and analytics.

| Activity | Module |
|----------|--------|
| EPM Planning: Financial planning model setup | Planning |
| EPM Planning: Workforce planning integration | Planning + HCM |
| EPM Planning: Capital planning setup | Planning |
| Financial Consolidation and Close setup | FCC |
| Account Reconciliation configuration | Account Reconciliation |
| Tax Reporting setup (Philippine taxes) | Tax Reporting |
| Narrative Reporting templates | Narrative Reporting |
| Profitability and Cost Management models | PCM |
| Enterprise Data Management setup | EDM |
| ERP, SCM, HCM, CX Analytics dashboards | Fusion Data Intelligence |
| Executive dashboard go-live | Fusion Data Intelligence |

---

### Phase 5: CX & Loyalty (Completed)

**Objective:** Implemented customer experience, loyalty, e-commerce, and marketing.

| Activity | Module |
|----------|--------|
| Customer Data Platform setup | CX CDP |
| Loyalty program configuration | CX Loyalty |
| Marketing automation setup | Marketing |
| Service center setup | CX Service |
| Knowledge management initial content | CX Knowledge |
| Field service configuration | CX Field Service |
| E-commerce platform development | CX Commerce |
| B2B portal setup | CX Sales + Commerce |
| Loyalty program full launch | CX Loyalty |
| E-commerce full launch | CX Commerce |
| Marketing automation campaigns activated | Marketing |

---

### Phase 6: Risk Management & Optimization (Completed)

**Objective:** Implemented risk management, fine-tuned all systems, and achieved operational excellence.

| Activity | Module |
|----------|--------|
| Advanced Controls: SoD rule configuration | Risk Management |
| Advanced Controls: Access certification setup | Risk Management |
| Advanced Controls: Transaction controls | Risk Management |
| Audit workflow setup | Risk Management |
| AI/ML model tuning | Demand forecasting, cash forecasting, anomaly detection |
| Process optimization | 90%+ transaction automation achieved |
| Advanced reporting | Custom reports and dashboards per user community |
| Oracle Digital Assistant deployment | AI chatbot for HR, procurement, and finance queries |

---

## 10.3 Current System Landscape

### 10.3.1 Operational Systems

| System | Status | Scope | Support Team |
|--------|--------|-------|-------------|
| Oracle Fusion Cloud ERP (GL, AP, AR, FA, Expenses, Cash Mgmt) | Production | All 5 entities | VP Enterprise Applications |
| Oracle Fusion Cloud SCM (Inventory, WMS, TMS, GTM, OM, PLM, Cost Mgmt) | Production | All locations | VP Enterprise Applications |
| Oracle Fusion Cloud SCM (SCP Demand, Supply, S&OP) | Production | All categories/locations | VP Enterprise Applications |
| Oracle Fusion Cloud HCM (Core HR, Recruiting, Learning, Performance, Comp, T&L, Absence, Payroll, ME) | Production | All 6,500 employees | VP Enterprise Applications |
| Oracle Fusion Cloud EPM (Planning, FCC, Tax, Narrative, PCM, EDM) | Production | All entities | VP Enterprise Applications |
| Oracle Fusion Cloud CX (Marketing, CDP, Loyalty, Sales, Commerce, Service, Knowledge, Field Service) | Production | All customers/channels | VP Enterprise Applications |
| Oracle Fusion Cloud Risk Management (Advanced Controls, Transaction Controls, Audit) | Production | All modules | VP Enterprise Applications |
| Oracle Integration Cloud (OIC) | Production | POS ↔ Oracle Fusion (18 flows) | Integration Team |
| Custom POS System | Production | 120 stores, ~760 terminals | VP Digital Products |

### 10.3.2 Operational Support Team

| Role | Count | Focus |
|------|-------|-------|
| Oracle Fusion Functional Leads (ERP, SCM, HCM, EPM, CX) | 5 | Module administration, configuration, optimization |
| Oracle Fusion Technical Leads (BI, Reports, Integration) | 3 | Analytics, reporting, OIC management |
| Oracle Fusion Administrators (System, Security) | 2 | System admin, role management, security |
| POS Development Team (Backend, Frontend, QA, DevOps) | 11 | POS development, deployment, L2/L3 support |
| Integration Developers (OIC) | 2 | Integration flows, API management |
| Data & Analytics Team | 4 | Data engineering, data science, BI |
| Infrastructure & Security Team | 8 | OCI, network, cybersecurity, IT support |
| **Total IT Team** | **35** | |

---

## 10.4 Lessons Learned

| Area | Lesson | Ongoing Action |
|------|--------|---------------|
| Data migration | Early data profiling prevented 80% of migration issues | Quarterly data quality audits continue |
| POS integration | Pilot store approach was critical; 2-store pilot uncovered 23 issues before rollout | New integration flows piloted before production |
| User adoption | Super-user network (change champions) drove 95% adoption within 3 months | Change champions network maintained ongoing |
| Training | Role-based, hands-on training was far more effective than module-based classroom | Refresher training uses same approach |
| Phased rollout | Sequential phases with overlap minimized business disruption | Oracle quarterly updates follow similar phased testing |

---

## 10.5 Current Performance Metrics

| Category | Metric | Current Performance | Target |
|----------|--------|-------------------|--------|
| **Financial** | Monthly close time | ≤ 5 business days | ≤ 5 business days |
| **Financial** | Transaction automation rate | 92% | > 90% |
| **Financial** | POS-to-ledger processing time (P95) | 2.1 seconds | < 3 seconds |
| **Supply Chain** | Forecast accuracy (MAPE) | 18% at category level | < 20% |
| **Supply Chain** | Fill rate | 96.2% | > 95% |
| **Supply Chain** | Inventory accuracy | 98.5% (WH), 95.8% (store) | > 98% (WH), > 95% (store) |
| **HR** | Payroll processing accuracy | 99.95% | > 99.9% |
| **HR** | Employee self-service adoption | 88% | > 80% |
| **Customer** | Loyalty enrollment | 520,000 members | > 500,000 |
| **Customer** | NPS | 52 | > 50 |
| **Technology** | System availability | 99.95% | > 99.9% |
| **Technology** | Integration availability | 99.93% | > 99.9% |
| **User Adoption** | Oracle Fusion active users | 97% of target users | > 95% |

---

## 10.6 Investment Summary

| Category | Cost (PHP) |
|----------|-----------|
| Oracle Fusion Cloud subscription (3-year) | 350,000,000 |
| OCI infrastructure (3-year) | 60,000,000 |
| OIC integration services (3-year) | 30,000,000 |
| SI partner implementation services | 180,000,000 |
| POS development (in-house, 18 months) | 80,000,000 |
| POS hardware (760 terminals/devices) | 114,000,000 |
| Change management and training | 25,000,000 |
| Contingency (15%) | 125,850,000 |
| **Total Investment** | **964,850,000** |

### Realized ROI

| Metric | Value |
|--------|-------|
| Annual efficiency gains (automation, reduced manual work) | PHP 150M/year |
| Inventory optimization (reduced dead stock, better fill rates) | PHP 200M/year |
| Procurement savings (better sourcing, volume consolidation) | PHP 100M/year |
| Revenue uplift (loyalty, e-commerce, better customer experience) | PHP 300M/year |
| **Total annual benefit** | **PHP 750M/year** |
| **Payback period achieved** | **~16 months** |
