# 10 — IMPLEMENTATION ROADMAP

## 10.1 Phased Implementation Plan

The Oracle Fusion Cloud implementation for Tahanan Depot follows a phased approach over 18 months, with the custom POS system developed in parallel.

---

## 10.2 Implementation Phases

### Phase 0: Foundation & Planning (Months 1-2)

**Objective:** Establish project governance, finalize requirements, prepare infrastructure.

| Activity | Duration | Owner | Deliverable |
|----------|----------|-------|-------------|
| Project charter and governance setup | 2 weeks | CEO + CIO | Signed project charter |
| Implementation partner selection | 3 weeks | CIO + Procurement | Contracted SI partner |
| Detailed requirements workshops (all modules) | 4 weeks | All VPs | BRD (Business Requirements Document) |
| Gap analysis (standard Fusion vs. requirements) | 2 weeks | SI Partner + Tahanan team | Gap/fit analysis document |
| OCI tenancy setup and environment provisioning | 1 week | VP Infrastructure | OCI environments (DEV, TEST, UAT, PROD) |
| Project plan and resource allocation | 2 weeks | PMO | Detailed project plan |
| Change management and communication plan | 2 weeks | CHRO + PMO | Change management plan |

**Key Decisions:**
- Oracle Fusion implementation partner selected (Tier 1 SI with retail experience).
- Internal project team identified: 15 full-time business leads + 10 IT resources.
- POS development team formed (8 developers, 2 QA, 1 DevOps).

---

### Phase 1: Core ERP & HCM (Months 3-8)

**Objective:** Implement foundational financial and HR systems.

#### Month 3-4: Configuration & Setup

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

#### Month 5-6: Process Implementation

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

#### Month 7-8: Testing & Go-Live (Core)

| Activity | Duration |
|----------|----------|
| System Integration Testing (SIT) | 3 weeks |
| User Acceptance Testing (UAT) | 2 weeks |
| Data migration (chart of accounts, opening balances, employees, suppliers) | 2 weeks |
| End-user training | 2 weeks |
| Cutover and go-live | 1 week |
| Hypercare support | 4 weeks |

**Go-Live Scope:**
- General Ledger, Payables, Receivables, Cash Management, Assets, Expenses for all 5 entities
- Core HR, Payroll, Benefits, Absence Management for all entities
- Recruiting and Onboarding activated
- Time & Labor (basic, without POS integration initially)

---

### Phase 2: Supply Chain & Procurement (Months 6-11)

**Objective:** Implement supply chain planning, inventory, warehouse management, and procurement.

> **Note:** Phase 2 runs in parallel with Phase 1 testing/go-live.

#### Month 6-7: Supply Chain Configuration

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

#### Month 8-9: Planning & Advanced Configuration

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

#### Month 10-11: Testing & Go-Live (Supply Chain)

| Activity | Duration |
|----------|----------|
| System Integration Testing | 3 weeks |
| User Acceptance Testing (warehouse + planning) | 2 weeks |
| Data migration (full item master, inventory balances, open POs) | 2 weeks |
| Warehouse team training | 2 weeks |
| RF device deployment (40 handhelds across 4 warehouses) | 1 week |
| Cutover and go-live (warehouses first, then stores) | 1 week |
| Hypercare support | 4 weeks |

**Go-Live Scope:**
- Full product lifecycle management
- Procurement (source-to-pay)
- Inventory management across all locations
- Warehouse management (4 DCs)
- Supply chain planning (demand, supply, S&OP)
- Order management (B2B and transfers)
- Transportation management
- Cost management

---

### Phase 3: Custom POS Development & Integration (Months 3-14)

**Objective:** Develop, test, and deploy custom POS system integrated with Oracle Fusion.

> **Note:** POS development starts in parallel with Phase 1.

#### Month 3-6: POS Core Development

| Activity | Deliverable |
|----------|-------------|
| POS requirements finalization | POS BRD |
| UX/UI design (Filipino-optimized touchscreen) | Design mockups approved |
| Backend development (transaction engine, local DB) | Core transaction processing |
| Frontend development (checkout, returns, receiving) | POS screens |
| Payment gateway integration (GCash, Maya, card terminals) | Payment SDKs integrated |
| BIR receipt compliance | Receipt format approved |
| Offline mode development | Local caching and sync logic |

#### Month 7-9: OIC Integration Development

| Activity | Deliverable |
|----------|-------------|
| OIC environment setup | OIC instances provisioned |
| INT-001: Sales transaction flow | Integration flow built and unit tested |
| INT-002: Return transaction flow | Integration flow built and unit tested |
| INT-003: Price sync flow | Integration flow built and unit tested |
| INT-004: Item master sync flow | Integration flow built and unit tested |
| INT-007: Loyalty point inquiry | Integration flow built and unit tested |
| INT-012: Time clock integration | Integration flow built and unit tested |
| INT-013: Daily Z-reading sync | Integration flow built and unit tested |
| All remaining integration flows | All 18 flows completed |
| API security and authentication | OAuth 2.0, mTLS configured |

#### Month 10-12: POS Pilot & Testing

| Activity | Duration | Scope |
|----------|----------|-------|
| POS lab testing (simulated environment) | 4 weeks | All transaction types, offline mode |
| Integration testing with Oracle Fusion | 4 weeks | All 18 integration flows end-to-end |
| Performance testing | 2 weeks | 500+ concurrent transactions |
| Security testing (penetration, PCI-DSS) | 2 weeks | Full POS security audit |
| Pilot store deployment (2 stores) | 4 weeks | Live in 2 pilot stores |
| Pilot store monitoring and fixes | 4 weeks | Daily monitoring and rapid iteration |
| UAT with store teams | 2 weeks | Cashiers and supervisors trained |

#### Month 13-14: POS Rollout

| Activity | Duration | Scope |
|----------|----------|-------|
| Wave 1: 20 stores (Metro Manila) | 2 weeks | 20 stores, ~80 terminals |
| Wave 2: 30 stores (rest of South Luzon + North Luzon) | 2 weeks | 30 stores, ~120 terminals |
| Wave 3: 35 stores (Visayas + Mindanao) | 2 weeks | 35 stores, ~140 terminals |
| Wave 4: Remaining 33 stores | 2 weeks | 33 stores, ~130 terminals |
| Hypercare support | 4 weeks | Dedicated support per region |

---

### Phase 4: EPM & Advanced Analytics (Months 10-14)

**Objective:** Implement planning, consolidation, and analytics.

#### Month 10-12: EPM Configuration

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

#### Month 13-14: Analytics & Go-Live

| Activity | Module |
|----------|--------|
| ERP Analytics dashboards | Fusion Data Intelligence |
| SCM Analytics dashboards | Fusion Data Intelligence |
| HCM Analytics dashboards | Fusion Data Intelligence |
| EPM first budget cycle | Planning |
| First consolidation run | FCC |
| First tax reporting cycle | Tax Reporting |
| Executive dashboard go-live | Fusion Data Intelligence |

---

### Phase 5: CX & Loyalty (Months 12-16)

**Objective:** Implement customer experience, loyalty, e-commerce, and marketing.

#### Month 12-14: CX Configuration

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

#### Month 15-16: CX Launch

| Activity | Duration |
|----------|----------|
| Loyalty program soft launch (pilot stores) | 2 weeks |
| Loyalty program full launch | 1 week |
| E-commerce beta launch | 2 weeks |
| E-commerce full launch | 1 week |
| Marketing automation campaigns activated | 2 weeks |
| CX Analytics dashboards | 1 week |

---

### Phase 6: Risk Management & Optimization (Months 14-18)

**Objective:** Implement risk management, fine-tune all systems, and achieve operational excellence.

#### Month 14-16: Risk Management

| Activity | Module |
|----------|--------|
| Advanced Controls: SoD rule configuration | Risk Management |
| Advanced Controls: Access certification setup | Risk Management |
| Advanced Controls: Transaction controls | Risk Management |
| Audit workflow setup | Risk Management |
| First access certification campaign | Risk Management |

#### Month 16-18: Optimization

| Activity | Description |
|----------|-------------|
| AI/ML model tuning | Refine demand forecasting, cash forecasting, anomaly detection |
| Process optimization | Identify and eliminate manual steps; target 90% automation |
| Advanced reporting | Build custom reports and dashboards per user community |
| Oracle Digital Assistant deployment | AI chatbot for HR, procurement, and finance queries |
| Full item master expansion | Scale from initial 10K to full 80K SKUs |
| Performance benchmarking | Ensure all KPIs meet targets |
| Knowledge transfer and documentation | Complete all operational documentation |
| Steady-state operations transition | Handoff from implementation to BAU teams |

---

## 10.3 Resource Requirements

### 10.3.1 Implementation Team

| Role | Internal Count | External (SI Partner) Count |
|------|---------------|----------------------------|
| Project Director | 1 | 1 |
| Project Managers | 2 | 2 |
| ERP Functional Leads | 3 | 3 |
| SCM Functional Leads | 2 | 2 |
| HCM Functional Leads | 2 | 2 |
| EPM Functional Lead | 1 | 1 |
| CX Functional Lead | 1 | 1 |
| Technical Architects | 1 | 2 |
| Integration Developers | 2 | 2 |
| Report Developers | 1 | 2 |
| Data Migration Specialists | 1 | 3 |
| Basis/Administrators | 2 | 1 |
| Change Management Lead | 1 | 1 |
| Training Specialists | 2 | 1 |
| QA/Test Leads | 2 | 2 |
| POS Development Team | 11 | 0 |
| **Total** | **35** | **26** |

### 10.3.2 Key Stakeholder Commitment

| Stakeholder | Commitment |
|-------------|-----------|
| CEO | Monthly steering committee; major decisions |
| CFO | Weekly check-ins; finance process ownership |
| COO | Weekly check-ins; operations process ownership |
| CHRO | Bi-weekly check-ins; HCM process ownership |
| CIO | Daily involvement; technical oversight |
| CMO | Bi-weekly check-ins; CX process ownership |
| Business Process Owners | 50% time dedication during their module's phase |
| Super Users (per module) | Full-time during UAT and go-live; part-time ongoing |

---

## 10.4 Risk Mitigation

| Risk | Probability | Impact | Mitigation |
|------|------------|--------|------------|
| Scope creep | High | High | Strict change control board; phase-gated approach |
| Data migration issues | Medium | High | Early data profiling; mock migration cycles |
| POS integration failures | Medium | Critical | Extensive lab testing; pilot store approach |
| User resistance | High | Medium | Comprehensive change management; early involvement |
| Resource availability | Medium | Medium | Backfill planning; SI partner flexibility |
| Oracle quarterly update impact | Low | Medium | Test all updates in non-production first |
| Business disruption during cutover | Medium | High | Phased rollout; weekend cutovers; rollback plans |
| Philippine regulatory changes | Low | Medium | Monitor BIR/DOLE/SEC updates; configurable tax/rules |

---

## 10.5 Success Criteria

| Category | Metric | Target |
|----------|--------|--------|
| **Go-Live** | All Phase 1 modules live | Month 8 |
| **Go-Live** | POS in all 120 stores | Month 14 |
| **Go-Live** | All modules fully operational | Month 18 |
| **Financial** | Monthly close time | ≤ 5 business days |
| **Financial** | Transaction automation rate | > 90% |
| **Financial** | POS-to-ledger processing time | < 3 seconds (P95) |
| **Supply Chain** | Forecast accuracy (MAPE) | < 20% at category level |
| **Supply Chain** | Fill rate | > 95% |
| **Supply Chain** | Inventory accuracy | > 98% (WH), > 95% (store) |
| **HR** | Payroll processing accuracy | > 99.9% |
| **HR** | Employee self-service adoption | > 80% within 3 months |
| **Customer** | Loyalty enrollment (Year 1) | > 500,000 members |
| **Customer** | NPS | > 50 |
| **Technology** | System availability | > 99.9% |
| **Technology** | Integration availability | > 99.9% |
| **User Adoption** | Oracle Fusion active users | > 95% of target users within 3 months |

---

## 10.6 Estimated Investment

| Category | Estimated Cost (PHP) |
|----------|---------------------|
| Oracle Fusion Cloud subscription (3-year) | 350,000,000 |
| OCI infrastructure (3-year) | 60,000,000 |
| OIC integration services (3-year) | 30,000,000 |
| SI partner implementation services | 180,000,000 |
| POS development (in-house, 18 months) | 80,000,000 |
| POS hardware (760 terminals/devices) | 114,000,000 |
| Change management and training | 25,000,000 |
| Contingency (15%) | 125,850,000 |
| **Total Estimated Investment** | **964,850,000** |

> **Note:** These are indicative estimates for the proof of concept. Actual costs will vary based on Oracle pricing, SI partner rates, and final scope.

### ROI Projection

| Metric | Value |
|--------|-------|
| Annual efficiency gains (automation, reduced manual work) | PHP 150M/year |
| Inventory optimization (reduced dead stock, better fill rates) | PHP 200M/year |
| Procurement savings (better sourcing, volume consolidation) | PHP 100M/year |
| Revenue uplift (loyalty, e-commerce, better customer experience) | PHP 300M/year |
| **Total annual benefit (conservative)** | **PHP 750M/year** |
| **Payback period** | **~16 months** |
