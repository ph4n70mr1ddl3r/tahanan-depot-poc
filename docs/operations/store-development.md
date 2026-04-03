# 22 — STORE DEVELOPMENT SOP

## 22.1 Store Development Overview

### 22.1.1 Expansion Strategy

Tahanan Depot targets 10-15 new store openings per year, growing from 120 to 300+ stores. This document provides the standard operating procedure for the complete store development lifecycle from site identification through post-opening stabilization.

### 22.1.2 Store Development Organization

```
VP STORE DEVELOPMENT (reports to COO)
├── Site Acquisition Manager
│   ├── Site Acquisition Specialists (4, one per region)
│   └── Market Research Analyst (1)
├── Construction Manager
│   ├── Construction Project Managers (4, one per region)
│   ├── Architects (2)
│   └── Engineers (2 — electrical + structural)
├── Store Setup Manager
│   ├── Merchandising Setup Specialists (4)
│   ├── IT Setup Specialists (3)
│   └── Training Coordinator (1)
└── Store Development Analyst
```

### 22.1.3 Oracle Fusion Roles

| Role | Oracle Fusion Security Roles |
|------|----------------------------|
| VP Store Development | ORA_EPM_PLANNING_MANAGER, ORA_PJT_PROJECT_MANAGER, ORA_FA_MANAGER |
| Site Acquisition Manager | ORA_EPM_PLANNING_ANALYST |
| Construction Manager | ORA_PJT_PROJECT_MANAGER, ORA_PO_BUYER |
| Store Setup Manager | ORA_INVENTORY_MANAGER, ORA_HCM_LEARNING_SPECIALIST |
| Store Development Analyst | ORA_EPM_PLANNING_ANALYST, ORA_PJT_ANALYST |

---

## 22.2 Site Selection Process

### 22.2.1 Site Selection Criteria

| Criterion | Weight | Minimum Threshold | Data Source |
|-----------|--------|-------------------|-------------|
| Population within 5km radius | 20% | > 100,000 residents | PSA census data |
| Median household income | 15% | Above regional median | PSA + market research |
| Home ownership rate within 5km | 10% | > 60% | LGU data |
| Existing competitor proximity | 15% | No direct competitor within 3km | Field survey + Google Maps |
| Traffic count (daily vehicles) | 10% | > 15,000 vehicles/day (main road frontage) | DOTR data / traffic study |
| Visibility and signage potential | 10% | Frontage on main road; signage visible from 100m+ | Site visit assessment |
| Parking availability | 5% | Minimum 50 parking slots (Standard); 80 (Flagship) | Site plan review |
| Lot size / building area | 5% | Minimum 3,000 sqm (Express); 5,000 sqm (Standard); 8,000 sqm (Flagship) | Title / survey plan |
| Accessibility (public transport) | 5% | Within 500m of public transport route | Field survey |
| Flood risk | 5% | Not in high-risk flood zone per LGU flood map | LGU / DENR flood map |

### 22.2.2 Site Selection Workflow

| Step | Activity | Owner | SLA | Oracle Fusion Touchpoint |
|------|----------|-------|-----|------------------------|
| 1 | Market gap analysis: identify underserved areas from expansion plan | Market Research Analyst | 2 weeks | EPM Planning (expansion model) |
| 2 | Desktop screening: shortlist 5-10 potential sites per target area | Site Acquisition Specialist | 1 week | EPM Planning (site scoring) |
| 3 | Site visit and field assessment | Site Acquisition Specialist + Architect | 1 week | — |
| 4 | Preliminary site scoring against criteria matrix | Site Acquisition Specialist | 3 business days | EPM Planning |
| 5 | Top 3 sites selected for feasibility analysis | Site Acquisition Manager | 3 business days | — |
| 6 | Financial feasibility model (projected P&L, NPV, IRR, payback) | Store Development Analyst | 2 weeks | EPM Planning (Capital Planning) |
| 7 | Due diligence (title check, zoning verification, environmental assessment) | CLO + Site Acquisition Specialist | 3 weeks | Narrative Reporting (due diligence checklist) |
| 8 | Site recommendation presented to COO | VP Store Development | 1 week | EPM Planning |
| 9 | Board approval for site acquisition (per POL-FIN-007 if > PHP 20M) | CEO + Board | Per Board schedule | Narrative Reporting |

### 22.2.3 Financial Feasibility Model

| Parameter | Standard Format | Express Format | Flagship Format |
|-----------|----------------|---------------|-----------------|
| Total investment (land + building + fixtures + inventory) | PHP 80-120M | PHP 50-80M | PHP 150-250M |
| Projected annual revenue (Year 1) | PHP 250-400M | PHP 150-250M | PHP 500-800M |
| Target gross margin | 30% | 28% | 32% |
| Target EBITDA margin (stabilized, Year 2+) | 10-12% | 8-10% | 12-14% |
| Payback period target | < 4 years | < 3 years | < 5 years |
| NPV (10-year, 12% discount rate) | Positive | Positive | Positive |
| IRR target | > 15% | > 18% | > 12% |
| Break-even (monthly sales) | Month 6-9 | Month 4-6 | Month 9-12 |

---

## 22.3 Lease vs. Build Decision Framework

### 22.3.1 Decision Matrix

| Factor | Lease | Build-to-Suit | Purchase |
|--------|-------|--------------|----------|
| Initial capital outlay | Low (deposit + fit-out only) | Medium (construction cost) | High (land + construction) |
| Timeline to open | 4-6 months | 8-12 months | 12-18 months |
| Long-term cost | Higher (escalating rent) | Medium (lease with ownership option) | Lower (no rent; only maintenance) |
| Flexibility | High (can relocate at lease end) | Medium | Low (committed to location) |
| Balance sheet impact | Operating lease (off-balance sheet per PFRS 16) | Right-of-use asset | Owned asset |
| Recommended when | Testing new market; uncertain demand | Growing market; want custom design | Proven market; prime location |

### 22.3.2 Lease Terms Standards

| Parameter | Standard Terms |
|-----------|---------------|
| Lease duration | 10-15 years with 5-year renewal option |
| Annual escalation | 3-5% per annum |
| Rent-free period | 3-6 months during fit-out |
| Common Area Maintenance (CAM) | Landlord-provided; capped at PHP X/sqm/year |
| Tenant improvement allowance | Negotiate PHP 5M-20M fit-out contribution from landlord |
| Exclusivity clause | Exclusive home improvement retailer in mall/commercial center |
| Co-tenancy clause | Minimum anchor tenant requirements |
| Early termination | 12-month notice; penalty of 6 months rent |
| Rent structure | Fixed base rent + percentage rent (2-3% of gross sales above threshold) |

---

## 22.4 Store Design and Construction

### 22.4.1 Design Standards by Format

| Element | Flagship | Standard | Express |
|---------|----------|----------|---------|
| Total area | 8,000-10,000 sqm | 5,000-7,999 sqm | 3,000-4,999 sqm |
| Sales floor area | 6,000-7,500 sqm | 3,500-5,600 sqm | 2,000-3,500 sqm |
| Backroom area | 1,200-1,500 sqm | 800-1,200 sqm | 500-800 sqm |
| Receiving dock | 2 dock doors; 600 sqm | 1 dock door; 400 sqm | 1 dock door; 250 sqm |
| Garden center | 500-800 sqm outdoor | 300-500 sqm outdoor | Optional (200 sqm) |
| Lumber yard | 400-600 sqm covered outdoor | 300-400 sqm covered outdoor | 200 sqm (limited) |
| Pro Desk area | Dedicated 80 sqm with separate entrance | Dedicated 50 sqm | Shared service desk 30 sqm |
| Cash office | 20 sqm (safe room) | 15 sqm | 10 sqm |
| Break room | 50 sqm | 40 sqm | 25 sqm |
| Training room | 30 sqm | 20 sqm | None (use break room) |
| POS terminals | 6-8 | 4-5 | 3-4 |
| Checkout area | 100 sqm | 70 sqm | 50 sqm |
| Restrooms (customer) | 2 (M/F) | 1 (M/F) | 1 (unisex) |
| Restrooms (employee) | 1 (M/F) | 1 (M/F) | 1 (unisex) |

### 22.4.2 Construction Timeline

| Phase | Duration | Activities | Deliverable |
|-------|----------|------------|-------------|
| Design and Permitting | 8-12 weeks | Architecture design, MEP design, LGU building permit, fire safety permit, barangay clearance | Approved plans and permits |
| Site Preparation | 2-3 weeks | Demolition (if existing), site clearing, utility connections | Prepared site |
| Structural Construction | 12-16 weeks | Foundation, columns, roof, walls, floors | Weather-tight shell |
| MEP Installation | 8-10 weeks | Electrical, plumbing, HVAC, fire suppression, CCTV, alarm | Operational systems |
| Interior Fit-Out | 6-8 weeks | Flooring, painting, fixtures, shelving, counters, signage | Store-ready interior |
| POS and IT Installation | 2-3 weeks | POS terminals, network, OIC configuration, CCTV, access control, Wi-Fi | Operational IT systems |
| Stock Loading | 2 weeks | Initial inventory delivery and merchandising setup | Fully stocked store |
| Staff Training | 2 weeks | POS training, product knowledge, safety, customer service (per Doc 15) | Trained team |
| Pre-Opening | 1 week | Soft opening (friends & family), final adjustments | Store ready for public |
| **Total Timeline** | **41-81 weeks (10-20 months)** | | |

### 22.4.3 Construction Project Management

| Step | Activity | System | Oracle Module | Frequency |
|------|----------|--------|---------------|-----------|
| 1 | Project created in Oracle Project Management | Project Management | Projects | Once (at Board approval) |
| 2 | Budget loaded per approved feasibility model | EPM Planning | Planning + Projects | Once |
| 3 | Tasks and milestones created per construction timeline | Project Management | Projects | Once |
| 4 | Contractor POs created and approved | Purchasing | Purchasing | Per contractor |
| 5 | Progress tracked weekly against plan | Project Management | Projects | Weekly |
| 6 | Budget spent tracked against approved budget | Projects + Payables | Projects + Payables | Weekly |
| 7 | Change orders approved per threshold | Purchasing + Projects | Purchasing + Projects | As needed |
| 8 | Monthly project status report to COO | Narrative Reporting | Narrative Reporting | Monthly |
| 9 | Construction completion certificate obtained | External (engineer/architect) | — | At completion |
| 10 | Asset capitalization (building, fixtures, equipment) | Assets | Assets + Projects | At completion |
| 11 | Project closeout and post-implementation review | Project Management | Projects | Within 90 days of opening |

### 22.4.4 Change Order Approval
| Amount Range (PHP) | Approver |
|---------------------|----------|
| 0 — 100,000 | Construction Manager |
| 100,001 — 500,000 | VP Store Development |
| 500,001 — 2,000,000 | COO |
| > 2,000,000 | CEO + CFO |

---

## 22.5 Pre-Opening Systems Setup

### 22.5.1 Oracle Fusion Configuration Checklist

| Step | Activity | System | Oracle Module | SLA |
|------|----------|--------|---------------|-----|
| 1 | New inventory organization created (STORE-XXX) | Inventory Management | Inventory | T-8 weeks before opening |
| 2 | Store assigned to correct business unit and region | GL + Inventory | GL + Inventory | T-8 weeks |
| 3 | Cost center created for new store | GL | GL | T-8 weeks |
| 4 | Subinventories created (Sales Floor, Backroom, Receiving, Damaged/Returns) | Inventory Management | Inventory | T-8 weeks |
| 5 | Store location and address configured | Inventory | Inventory | T-8 weeks |
| 6 | Store assigned to supply planning (warehouse source) | SCP | SCP | T-6 weeks |
| 7 | Store replenishment parameters set (safety stock, min/max, order multiples) | SCP + Inventory | SCP + Inventory | T-6 weeks |
| 8 | OIC integration endpoints configured for new store | OIC | Integration Cloud | T-4 weeks |
| 9 | Store bank account opened per treasury policy (Doc 19) | Cash Management | Cash Management | T-4 weeks |
| 10 | Store tax registration updated (BIR branch registration if required) | Tax | Tax Reporting | T-4 weeks |

### 22.5.2 POS Provisioning Checklist

| Step | Activity | System | SLA |
|------|----------|--------|-----|
| 1 | POS terminals ordered and configured per format specification | POS Team | T-8 weeks |
| 2 | Network infrastructure installed (primary Ethernet + 4G LTE failover) | IT Infrastructure | T-4 weeks |
| 3 | Peripherals installed (barcode scanners, receipt printers, cash drawers, customer displays) | POS Team | T-3 weeks |
| 4 | Payment gateway configured (card terminal, GCash/Maya integration) | POS Team + Payment Provider | T-3 weeks |
| 5 | POS terminal registered with store inventory organization | POS Backend | T-2 weeks |
| 6 | Price and item master sync verified | OIC → POS | T-1 week |
| 7 | End-to-end transaction test (sale, return, loyalty, gift card, mixed payment) | POS QA | T-1 week |
| 8 | Offline mode tested (simulate network outage; verify sync recovery) | POS QA | T-1 week |
| 9 | CCTV and security system operational | Security Team | T-1 week |
| 10 | Biometric device installed and enrolled for timekeeping | IT Team | T-1 week |

### 22.5.3 Initial Stock Order Process

| Step | Activity | System | Oracle Module | SLA |
|------|----------|--------|---------------|-----|
| 1 | New store assortment defined by Category Manager (per format) | PLM | PLM | T-8 weeks |
| 2 | Supply planning generates initial fill purchase orders and transfer orders | SCP | SCP | T-6 weeks |
| 3 | Purchase orders and transfer orders approved | Purchasing | Purchasing | T-5 weeks |
| 4 | Initial stock delivered to store | WMS + TMS | Warehouse + Transportation | T-2 weeks |
| 5 | Stock received in POS Receiving Module | POS | POS Receiving | T-1 week |
| 6 | Merchandising setup completed (planogram, price labels, displays) | Store team | — | T-1 week |
| 7 | Pre-opening inventory count and valuation confirmed | Inventory | Inventory | T-3 days |

---

## 22.6 Staffing for New Stores

### 22.6.1 Hiring Timeline

| Position | Target Hire Date | Recruiting Start | Training Period |
|----------|-----------------|-----------------|----------------|
| Store Manager | T-12 weeks | T-16 weeks | 4 weeks (existing store immersion) |
| Assistant Store Manager(s) | T-8 weeks | T-12 weeks | 4 weeks |
| Department Supervisors | T-6 weeks | T-10 weeks | 4 weeks |
| Cashiers | T-4 weeks | T-8 weeks | 4 weeks (POS + customer service) |
| Sales Associates | T-4 weeks | T-8 weeks | 4 weeks (product knowledge + POS) |
| Stock Associates | T-4 weeks | T-8 weeks | 4 weeks (receiving + inventory) |

### 22.6.2 Training Schedule (Pre-Opening)

| Week | Training Focus | Audience | Duration |
|------|---------------|----------|----------|
| T-4 to T-3 | POS system fundamentals (cashier and supervisor training) | Cashiers, Supervisors | 40 hours |
| T-3 to T-2 | Product knowledge (department-specific) + Oracle Learning modules | All store staff | 40 hours |
| T-2 to T-1 | Store operations (receiving, inventory, merchandising, returns) | All store staff | 40 hours |
| T-1 to T-0 | Customer service, safety, LP awareness, soft opening practice | All store staff | 40 hours |

### 22.6.3 Store Manager Selection Criteria

| Criterion | Requirement |
|-----------|-------------|
| Experience | 5+ years retail management; home improvement industry preferred |
| Leadership | Demonstrated team management of 20+ employees |
| Systems | Proficiency in POS and inventory management systems |
| Financial | P&L understanding; budget management experience |
| Customer service | Track record of achieving customer satisfaction targets |
| Availability | Willing to relocate; available 2 months before opening |
| Language | Filipino and English proficiency |

---

## 22.7 Merchandising Setup

### 22.7.1 Planogram Installation

| Step | Activity | Owner | SLA |
|------|----------|-------|-----|
| 1 | Planogram received from Merchandising team (per format and store layout) | Planogram Specialist | T-6 weeks |
| 2 | Fixture installation verified against planogram | Store Setup Specialist | T-3 weeks |
| 3 | Shelf labels and price tags installed (synced with Oracle Pricing) | Department Supervisors | T-1 week |
| 4 | Product placement per planogram completed | Sales Associates + Stock Associates | T-1 week |
| 5 | Planogram compliance audit by Merchandising team | Planogram Specialist | T-3 days |
| 6 | Corrections completed | Store team | T-1 day |

### 22.7.2 Visual Merchandising Setup

| Element | Standard | Owner |
|---------|----------|-------|
| Exterior signage | Illuminated Tahanan Depot signage (per brand guidelines) | Construction Manager |
| Department signage | Department name signs; aisle markers; category labels | Store Setup Specialist |
| Promotional displays | Entrance/power aisle displays set per promotional calendar | Merchandising Setup Specialist |
| End caps | Product displays per Merchandising directive | Department Supervisors |
| Impulse area (near checkout) | Pre-packed small items, batteries, fasteners, accessories | Department Supervisors |
| Pro Desk area | Product catalog, sample displays, dedicated POS terminal | Store Manager |
| Demo/display units | Power tool displays, appliance demos (safety-compliant) | Store Setup Specialist |
| Safety signage | Fire exit, emergency, PPE requirement signs | Safety Officer |

---

## 22.8 Marketing and Grand Opening

### 22.8.1 Grand Opening Campaign Timeline

| Timing | Activity | Owner |
|--------|----------|-------|
| T-8 weeks | Grand opening date confirmed; marketing campaign brief created | VP Store Development + CMO |
| T-6 weeks | Grand opening creative materials in production | Creative Director |
| T-4 weeks | Grand opening flyer printed (100,000 copies, 20km radius distribution) | VP Brand |
| T-3 weeks | Digital advertising campaign launched (geo-targeted within 20km radius) | VP Digital Marketing |
| T-3 weeks | Social media countdown posts begin | Social Media Specialist |
| T-2 weeks | B2B contractor invitation sent (direct mail + email) | VP Sales + VP Trade Marketing |
| T-2 weeks | Local government officials and community leaders invited | CLO + VP Store Development |
| T-1 week | Local radio and OOH advertising activated | VP Brand |
| T-1 week | Store team rehearses grand opening procedures | Store Manager |
| T-3 days | Soft opening (friends, family, employees, B2B customers) | Store Manager |
| T-0 | Grand opening day | All |
| T+1 week | Post-opening performance review begins | VP Store Development |

### 22.8.2 Grand Opening Promotions

| Promotion | Description | Duration |
|-----------|-------------|----------|
| Grand opening discount | 15-25% storewide discount | Opening day + 7 days |
| First 100 customers gift | PHP 500 gift card for first 100 customers | Opening day only |
| Loyalty sign-up bonus | Double loyalty points for all purchases during opening week | Opening week |
| Free DIY workshop | Opening day workshop (basic home improvement project) | Opening day |
| Raffle draw | PHP 50,000 gift card grand prize; daily minor prizes | Opening week |
| Contractor special | Additional B2B discount + Pro Desk welcome package | Opening month |

---

## 22.9 Post-Opening Monitoring

### 22.9.1 30-Day Intensive Monitoring Plan

| Day | Focus Area | Visitors | Metrics Reviewed |
|-----|-----------|----------|-----------------|
| 1-3 | Daily store operations and POS performance | Store Manager + District Manager | Sales, transactions, POS issues, customer feedback |
| 4-7 | Inventory accuracy and replenishment | District Manager + Inventory Analyst | Stock levels, replenishment timing, receiving accuracy |
| 8-10 | Customer service and merchandising | Regional Director + Merchandising team | CSAT, planogram compliance, display condition |
| 11-14 | Financial performance vs. feasibility model | VP Finance + Store Development Analyst | Revenue vs. plan, gross margin, cash handling |
| 15-21 | Operational stability and team performance | HRBP + District Manager | Employee performance, scheduling, training gaps |
| 22-30 | Stabilization assessment | VP Store Development + Regional Director | All KPIs vs. targets; stabilization criteria check |

### 22.9.2 Stabilization Criteria

| Metric | Stabilization Target (Day 30) | Measurement |
|--------|-------------------------------|-------------|
| Daily revenue vs. feasibility model | > 80% of projected daily revenue | POS Analytics |
| Gross margin % | > 27% | ERP Analytics |
| Inventory accuracy | > 90% | Inventory Analytics |
| Customer satisfaction (CSAT) | > 85% | CX Service Analytics |
| POS transaction success rate | > 99.5% | POS Analytics |
| Employee training completion | 100% mandatory training | Oracle Learning |
| Cash variance | < PHP 200/register/day | Cash Management |
| Planogram compliance | > 85% | Store audit |
| Shrinkage (early indication) | < 2% of sales | Inventory Analytics |

### 22.9.3 Escalation Triggers (First 90 Days)

| Trigger | Escalation | Action |
|---------|-----------|--------|
| Revenue < 60% of feasibility model for 7 consecutive days | VP Store Development + COO | Emergency review; adjust strategy |
| Gross margin < 25% for 14 consecutive days | VP Finance + VP Merchandising | Pricing and assortment review |
| Customer satisfaction < 80% for 7 consecutive days | VP Customer Service + Store Manager | Service recovery plan |
| Employee turnover > 20% in first 90 days | CHRO + HRBP | Retention intervention |
| Critical system issue (POS or OIC) | CIO + VP Digital Products | Immediate technical support |
| Safety incident (any) | VP Store Ops + VP Facilities | Immediate investigation |

---

## 22.10 Store Renovation and Refresh

### 22.10.1 Renovation Triggers

| Trigger | Scope | Budget Range | Timeline |
|---------|-------|-------------|----------|
| Store age > 5 years (cosmetic refresh) | Paint, signage, lighting refresh, fixture repair | PHP 3-5M | 2-4 weeks |
| Store age > 10 years (major renovation) | Full interior renovation, layout optimization, new fixtures | PHP 15-30M | 8-12 weeks |
| Performance decline > 15% below targets | Strategic renovation to reposition store | PHP 10-25M | 6-10 weeks |
| Competitive threat (new competitor within 3km) | Assortment expansion, store modernization | PHP 10-20M | 8-12 weeks |
| Format change (e.g., Express → Standard) | Full renovation to new format specification | PHP 20-40M | 12-16 weeks |
| Emergency (fire, typhoon damage, flooding) | Restoration to operational condition | Per insurance assessment | Per scope |

### 22.10.2 Renovation Approval Workflow

| Step | Activity | Owner | SLA |
|------|----------|-------|-----|
| 1 | Renovation need identified (per trigger criteria) | Regional Director or VP Store Dev | — |
| 2 | Scope assessment and cost estimate prepared | Construction Manager | 2 weeks |
| 3 | Business case prepared (projected ROI, sales lift estimate) | Store Development Analyst | 1 week |
| 4 | Approval per POL-FIN-007 capex thresholds | VP Finance / CFO / CEO / Board | Per policy |
| 5 | Project created in Oracle Project Management | Construction Project Manager | 1 day |
| 6 | Contractor procurement (if applicable) | Purchasing | 2-4 weeks |
| 7 | Construction execution | Construction Manager | Per timeline |
| 8 | Store remains operational or temporarily closed (per scope) | Store Manager + VP Store Dev | Per plan |
| 9 | Renovation completion and asset update | Assets | At completion |
| 10 | Post-renovation performance review (30 days) | VP Store Dev | 30 days post-completion |

---

## 22.11 Store Closure Process

### 22.11.1 Closure Criteria

| Criterion | Threshold | Approval |
|-----------|-----------|----------|
| Consistent revenue < 60% of plan for 12+ months | Quantitative | COO + CFO |
| Negative EBITDA for 8+ consecutive months | Quantitative | CFO + CEO |
| Market exit strategy (region downsizing) | Strategic | CEO + Board |
| Lease expiration with no renewal | Contractual | VP Store Dev + CLO |
| Unresolvable safety or structural issues | Safety | VP Facilities + CLO |
| Force majeure (permanent damage from disaster) | Emergency | CEO + Board + Insurance |

### 22.11.2 Store Closure Process

| Step | Activity | Owner | Timeline |
|------|----------|-------|----------|
| 1 | Closure decision approved per criteria | CEO + Board | — |
| 2 | Employee notification (60-day notice per DOLE for redundancy) | CHRO + HRBP | T-60 days |
| 3 | Employee reassignment or redundancy package offered | HRBP | T-60 to T-30 days |
| 4 | Customer notification (signage, email, social media) | CMO | T-30 days |
| 5 | Inventory liquidation sale (if applicable) | VP Merchandising + Store Manager | T-30 to T-0 days |
| 6 | Remaining inventory transferred to nearby stores | Supply Planning + Inventory | T-14 to T-3 days |
| 7 | POS and IT systems decommissioned | IT Team | T-3 to T-1 days |
| 8 | Oracle Fusion inventory org deactivated | VP Enterprise Apps | T-1 day |
| 9 | Store premises turned over to landlord or secured | VP Store Dev + Tahanan Property | T-0 (closing day) |
| 10 | Final accounting: asset write-off, lease termination, closing entries | VP Finance | T+30 days |
| 11 | Post-closure report (lessons learned, financial impact) | VP Store Dev | T+60 days |

### 22.11.3 Employee Transition Options

| Option | Description | Eligibility |
|--------|-------------|-------------|
| Transfer to nearby store | Same role at nearby store (within reasonable commute) | All employees |
| Transfer to new store opening | Relocate to upcoming new store opening | All employees; relocation assistance provided |
| Voluntary separation | Enhanced separation package (above DOLE minimum) | Employees who choose not to transfer |
| Redundancy (involuntary) | DOLE-compliant separation pay (1/2 month per year of service) | Employees with no available transfer |

---

## 22.12 Store Development Performance Metrics

### 22.12.1 Development KPIs

| KPI | Target | Measurement | Frequency | Owner |
|-----|--------|-------------|-----------|-------|
| Time-to-open (Board approval to grand opening) | < 12 months (Standard); < 9 months (Express) | Project Management timeline | Per store | VP Store Development |
| Construction cost variance | < 5% over approved budget | Actual vs. approved budget in Oracle Projects | Monthly (during construction) | Construction Manager |
| Total project cost variance | < 5% over approved budget | Actual vs. approved budget | At completion | VP Store Development |
| First-year sales vs. plan | > 90% of feasibility model revenue | ERP Analytics vs. EPM Planning | Monthly (Year 1) | Store Development Analyst |
| Payback period | < 4 years (Standard); < 3 years (Express) | Cumulative net cash flow vs. investment | Quarterly | VP Finance |
| Year 1 customer satisfaction | > 85% CSAT | CX Service Analytics | Monthly | VP Customer Service |
| Year 1 employee retention | > 80% (first 12 months) | HCM Analytics | Monthly | CHRO |
| Year 1 shrinkage | < 2.0% of sales | Inventory Analytics | Monthly | VP Loss Prevention |
| Store pipeline health | > 20 sites in pipeline at any time | Pipeline tracker | Quarterly | Site Acquisition Manager |
| Permit approval cycle time | < 8 weeks | Application to approval date | Per store | CLO |

### 22.12.2 Post-Opening Performance Review Schedule

| Review | Timing | Audience | Content |
|--------|--------|----------|---------|
| 30-day stabilization check | Day 30 | VP Store Dev + Regional Director | All stabilization KPIs; go/no-go for continued investment |
| 90-day performance review | Day 90 | COO + VP Store Dev + VP Finance | Revenue, margin, customer, employee metrics vs. plan |
| 6-month performance review | Month 6 | COO + CFO | Full P&L review vs. feasibility model |
| 12-month anniversary review | Month 12 | CEO + COO + CFO | First year performance; payback progress; investment ROI |
