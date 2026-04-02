# 13 — LOSS PREVENTION & PHYSICAL SECURITY

## 13.1 Loss Prevention Strategy

### 13.1.1 Shrinkage Targets

| Location Type | Shrinkage Target (% of Sales) | Industry Benchmark | Measurement Method |
|---------------|------------------------------|--------------------|--------------------|
| Stores (overall) | < 1.5% | 1.5 - 2.5% | Annual physical inventory vs. book inventory |
| Stores (high-risk: Metro Manila) | < 2.0% | 2.0 - 3.0% | Same |
| Warehouses | < 0.5% | 0.5 - 1.0% | Cycle count accuracy |
| Overall company | < 1.2% | 1.5 - 2.0% | Consolidated inventory adjustment analysis |

### 13.1.2 Shrinkage Categories and Root Causes

| Category | Definition | Common Examples | Prevention Strategy |
|----------|-----------|-----------------|---------------------|
| External Theft (Shoplifting) | Theft by customers/consumers | Concealment, price switching, sweep theft, organized retail crime (ORC) | Surveillance, EAS, customer service approach, high-value item protection |
| Internal Theft (Employee) | Theft by employees | Cash theft, merchandise theft, fictitious returns, sweet-hearting, time theft | SoD, cash controls, audit, background checks, surveillance |
| Vendor Fraud | Theft or fraud by suppliers | Short deliveries, phantom deliveries, substitution, invoice fraud | Receiving controls, 3-way match, supplier audits, camera at receiving |
| Administrative Error | Unintentional errors | Data entry errors, receiving errors, pricing errors, miscounts | Training, system controls, cycle counting, dual verification |
| Damage / Spoilage | Product damage or expiration | Handling damage, water damage, expired goods, pest damage | Proper storage, FEFO rotation, pest control, handling training |
| Process Failure | Systemic process gaps | Unrecorded transfers, missed returns, receiving shortcuts | Process adherence, SOP compliance, system controls |

---

## 13.2 Loss Prevention Organization

### 13.2.1 Loss Prevention Team

```
VP Loss Prevention & Security (reports to COO, dotted line to CFO)
│
├── Regional Loss Prevention Managers (4 regions)
│   ├── North Luzon LP Manager
│   ├── South Luzon LP Manager
│   ├── Visayas LP Manager
│   └── Mindanao LP Manager
│
├── LP Investigators (6 — handle complex cases, ORC, employee investigations)
│
├── LP Analysts (4 — data analytics, exception reporting, CCTV monitoring)
│
├── Security Operations Center (SOC)
│   ├── SOC Operators (8 — 24/7 monitoring of CCTV, alarms)
│   └── SOC Supervisor
│
└── LP Coordinators (120 — 1 per store, dual role with store operations)
```

### 13.2.2 LP Coordinator (Per Store) — Key Responsibilities

| Responsibility | Frequency | Oracle Fusion Touchpoint |
|---------------|-----------|------------------------|
| Review daily exception reports (voids, refunds, discounts, no-sales) | Daily | POS reports, Oracle AR |
| Monitor CCTV for suspicious activity | Ongoing | POS (transaction-CCTV linkage) |
| Conduct LP awareness briefings for store team | Weekly | — |
| Review shrinkage reports and trends | Monthly | Inventory Analytics |
| Investigate incidents (theft, fraud, damage) | As needed | POS data, Oracle Inventory |
| Coordinate with regional LP Manager on investigations | As needed | — |
| Audit cash handling compliance | Weekly | POS Z-readings, Cash Management |
| Audit receiving compliance | Weekly | POS Receiving Module, Inventory |
| Monitor high-shrink departments and SKUs | Daily | POS analytics, Inventory |
| Report and track LP incidents | Per incident | HCM Workforce Health & Safety (for injuries) |

---

## 13.3 Physical Security Measures

### 13.3.1 Store Security Systems

| System | Specification | Coverage |
|--------|--------------|----------|
| CCTV Surveillance | IP-based, 1080p minimum, 30-day recording (90 days for high-risk areas) | All sales floor areas, entrances/exits, receiving dock, cash office, backroom |
| Electronic Article Surveillance (EAS) | RF or AM EAS tags on high-value/high-shrink items | High-value items (power tools, appliances, electrical) |
| Burglar Alarm | Monitored alarm system with motion, door contacts, glass break | All entry/exit points, cash office, high-value cage |
| Access Control | Electronic key card or PIN-based | Cash office, server room, backroom restricted areas |
| Safe / Cash Office | TL-30 rated safe; dual-lock (two-person access); time-lock | Cash office in every store |
| Lighting | Adequate exterior and interior lighting; parking lot illumination | Perimeter, parking, receiving dock, sales floor |
| Fencing / Barriers | Perimeter fencing where applicable; bollards at entrances | Warehouse yards, store perimeters (where applicable) |
| Anti-Shoplifting Mirrors | Convex mirrors in blind spots | Aisles with limited CCTV coverage |
| Security Signage | Visible signage: "CCTV in operation", "Shoplifters will be prosecuted" | Entrances, exits, high-risk departments |

### 13.3.2 Warehouse Security Systems

| System | Specification | Coverage |
|--------|--------------|----------|
| CCTV Surveillance | IP-based, 4K resolution, 30-day recording | All dock doors, staging areas, high-value storage zones, perimeter |
| Access Control | Electronic key card + PIN; separate zones | Warehouse floor, high-value cage, administrative offices |
| Perimeter Security | Fencing, gate control, guard house | Warehouse yard, truck parking |
| Vehicle Tracking | Gate log with vehicle registration, driver ID, purpose | All vehicle entry/exit |
| Visitor Management | Visitor registration, escort required, badge system | All visitors |
| Inventory Cage / High-Value Area | Locked cage for high-value items (power tools, appliances) | Separate secured storage area |
| Guard Service | 24/7 security guard (own or contracted) | Perimeter, dock doors, main entrance |

### 13.3.3 Corporate HQ Security

| System | Specification |
|--------|--------------|
| Access Control | Card + biometric; zone-based access |
| CCTV | All common areas, server room, parking |
| Visitor Management | Registration, escort, temporary badge |
| Reception | Staffed reception with ID verification |
| Server Room | Biometric access, fire suppression, environmental monitoring, CCTV |

---

## 13.4 Cash Protection

### 13.4.1 Cash Handling Controls

| Control | Description | Oracle Fusion Touchpoint |
|---------|-------------|------------------------|
| Starting float verification | Cashier counts and verifies PHP 5,000 float at shift start | POS (opening procedure) |
| Cash drawer assignment | One cashier per drawer per shift; no sharing | POS (login-based) |
| Cash drops | Cashier performs mid-shift safe drops when drawer exceeds PHP 20,000 | POS (recorded) |
| End-of-day count | Cashier counts drawer; supervisor verifies against Z-reading | POS Z-reading vs. Cash Management |
| Variance threshold | PHP 100 per register per day; investigation triggered above threshold | Cash Management alert |
| Dual control (cash office) | Two-person access to safe; dual key/combination | Physical procedure |
| Armored car pickup | Mandatory for stores with daily cash receipts > PHP 500,000 | Cash Management (deposit tracking) |
| Bank deposit reconciliation | Same-day or next-morning deposit; auto-matched in Cash Management | Cash Management |
| Cash variance trending | Monthly cash variance report by store, cashier, and shift | POS Analytics, Cash Management |
| Cashier rotation | Cashiers rotated across terminals and shifts to detect patterns | Workforce Scheduling |

### 13.4.2 Cash Loss Investigation Triggers

| Trigger | Action | Owner |
|---------|--------|-------|
| Single variance > PHP 100 | Document; supervisor review | Store Supervisor |
| 3 variances > PHP 100 in 30 days (same cashier) | Formal investigation; possible retraining or disciplinary action | LP Coordinator + Store Manager |
| Variance > PHP 1,000 (single occurrence) | Immediate investigation; LP notified | LP Coordinator + Store Manager |
| Pattern of small shortages (same cashier over 30 days) | Data analysis; LP investigation | LP Analyst + Store Manager |
| Missing deposit or deposit discrepancy | Immediate investigation; VP Finance notified | LP Coordinator + VP Finance |

---

## 13.5 Fraud Prevention

### 13.5.1 Fraud Risk Matrix

| Fraud Type | Description | Indicators | Prevention / Detection | Oracle Fusion Control |
|-----------|-------------|-----------|----------------------|----------------------|
| Sweet-hearting | Cashier doesn't scan items for accomplice | High void rate; low transaction value vs. item count | Exception-based reporting; CCTV-POS integration; basket analysis | POS analytics, AR analytics |
| Fictitious returns | Employee processes fake returns and pockets cash | High return rate by cashier; returns without customer present; returns for high-value items | Return authorization controls; supervisor approval for > PHP 5K; CCTV at returns desk; return-to-sale ratio monitoring | POS (return controls), AR (credit memo), Advanced Controls |
| Gift card fraud | Employee issues or loads gift cards fraudulently | Gift card issued without corresponding transaction; balance discrepancies | Gift card audit log; dual control for high-value issuance; reconciliation | POS (gift card audit), Revenue Management (liability tracking) |
| Time theft | Employee clocks in/out incorrectly; buddy punching | Clock-in/out anomalies; overtime without approval | Biometric clock-in; POS-based timekeeping; supervisor approval of timecards | Time & Labor (exception reporting), Workforce Scheduling |
| Vendor collusion | Employee receives kickbacks for favorable treatment | Single-source without justification; preferential supplier treatment; lifestyle indicators | Competitive bidding enforcement; vendor diversity; SoD between procurement and receiving | Sourcing, Supplier Management, Advanced Controls |
| Expense fraud | Employee submits false or inflated expense claims | Duplicate receipts; round amounts; unusual vendors; pattern of claims just below approval threshold | Policy enforcement automation; OCR receipt verification; random audits | Expenses (policy rules, AI anomaly detection) |
| Inventory theft | Employee steals merchandise from store or warehouse | Unexplained shrinkage; broken seals; inventory adjustments | Cycle counting; CCTV; access restrictions; LP awareness | Inventory Management (adjustment tracking, cycle count), POS analytics |
| Payroll fraud | Ghost employees, inflated hours, unauthorized pay changes | Employees without system activity; pay rate changes without approval; duplicate bank accounts | HR-Payroll reconciliation; manager approval of timecards; SoD between HR and payroll | Payroll, Core HR, Advanced Controls (SoD) |

### 13.5.2 Exception-Based Reporting (EBR)

| Report | Frequency | Audience | Key Metrics |
|--------|-----------|----------|-------------|
| Void Analysis | Daily | LP Coordinator, Store Manager | Void count by cashier, void amount, void-to-sale ratio, void after payment |
| Return Analysis | Daily | LP Coordinator, Store Manager | Return count by cashier, return amount, return-to-sale ratio, no-receipt returns |
| Discount Analysis | Daily | LP Coordinator, Store Manager | Manual discount count, discount amount, override frequency by supervisor |
| No-Sale (Drawer Open) | Daily | LP Coordinator, Store Manager | No-sale frequency by cashier, no-sale timing patterns |
| Refund Pattern Analysis | Weekly | LP Analyst, Regional LP Manager | Refunds by store, cashier, time of day, payment method, item category |
| Transaction Anomaly | Weekly | LP Analyst | Transactions outside normal patterns: unusually high/low values, unusual item combinations, rapid sequential transactions |
| Cash Variance Trending | Weekly | LP Analyst | Cumulative cash variance by store, cashier, shift |
| Gift Card Activity | Weekly | LP Analyst, Loyalty Manager | Gift cards issued vs. redeemed, high-value issuances, dormant card reactivation |
| Inventory Adjustment Analysis | Weekly | LP Analyst, Inventory Data Steward | Adjustment volume, value, and reason by store/warehouse; pattern analysis |
| Overtime Analysis | Monthly | HR, LP | Overtime hours by employee vs. schedule vs. store activity; unauthorized OT patterns |

---

## 13.6 Investigation Procedures

### 13.6.1 Investigation Classification

| Classification | Description | Examples | Investigator | Target Resolution |
|---------------|-------------|----------|-------------|-------------------|
| Level 1 — Minor | Low-value incident; process violation | Cash variance, small shrinkage, policy non-compliance | LP Coordinator + Store Manager | 5 business days |
| Level 2 — Moderate | Significant value or pattern | Employee theft (< PHP 50K), ORC case, vendor short-delivery | Regional LP Manager + LP Investigator | 15 business days |
| Level 3 — Major | High-value, organized, or multi-location | Organized retail crime ring, major employee fraud (> PHP 50K), vendor collusion | VP LP + LP Investigator + Legal | 30 business days |
| Level 4 — Critical | Company-wide impact or criminal activity | Systemic fraud, executive-level fraud, external break-in with violence | VP LP + CLO + CEO + law enforcement | Immediate response; investigation per timeline |

### 13.6.2 Investigation Process

| Step | Action | Documentation |
|------|--------|---------------|
| 1 | Incident reported or exception detected | Incident report (in LP case management system) |
| 2 | Preliminary assessment — determine classification and assign investigator | Case file created |
| 3 | Evidence gathering — POS data, CCTV footage, transaction logs, interviews | Evidence log; chain of custody maintained |
| 4 | Analysis — review data, identify patterns, corroborate evidence | Analysis report |
| 5 | Interview (if applicable) — conducted per due process; witness present; documented | Interview transcript / summary |
| 6 | Conclusion — substantiated, unsubstantiated, or inconclusive | Investigation report |
| 7 | Action — disciplinary, recovery, process improvement, law enforcement referral | Action memo |
| 8 | Closure — case closed; lessons learned documented | Case closure report |
| 9 | Recovery — civil recovery demand or deduction from final pay (per legal advice) | Recovery documentation |

### 13.6.3 Evidence Handling

| Evidence Type | Retention | Handling |
|--------------|-----------|----------|
| CCTV footage (incident-related) | 2 years from case closure | Downloaded, labeled, stored in secure case file |
| POS transaction data | Per data retention policy (10 years) | Screenshot / export preserved in case file |
| Witness statements | 2 years from case closure | Signed statements in case file |
| Physical evidence (if applicable) | Until case resolution + 1 year | Photographed; secured in LP office |
| Investigation reports | 5 years from case closure | Secure LP case management system |

---

## 13.7 Store Opening and Closing Security

### 13.7.1 Store Opening Procedure (Security)

| Step | Action | Responsible |
|------|--------|-------------|
| 1 | Arrive 30 minutes before store opening (minimum 2 employees) | Opening Manager + Associate |
| 2 | Exterior check — check doors, windows, signage, parking lot for suspicious activity or damage | Opening Manager |
| 3 | Enter via designated entrance; disarm alarm using authorized code | Opening Manager |
| 4 | Interior check — walk through store checking for signs of break-in, damage, or unauthorized presence | Opening Manager + Associate |
| 5 | Verify all high-value cages/cabinets locked and intact | Opening Manager |
| 6 | If alarm triggered or signs of intrusion — do NOT enter; call police and LP Manager | Opening Manager |
| 7 | Activate POS systems and verify camera feeds | Opening Manager |
| 8 | Open safe; verify cash inventory matches closing count | Opening Manager |
| 9 | Unlock customer entrance at scheduled store opening time | Opening Manager |
| 10 | Document opening in store security log | Opening Manager |

### 13.7.2 Store Closing Procedure (Security)

| Step | Action | Responsible |
|------|--------|-------------|
| 1 | Announce store closing 15 minutes before closing time | Closing Manager |
| 2 | Walk sales floor to ensure all customers have left | Closing Manager + Associates |
| 3 | Lock customer entrance | Closing Manager |
| 4 | Complete all POS closing procedures (Z-readings, cash counts, deposits) | Cashiers + Closing Manager |
| 5 | Secure cash in safe; verify safe is locked | Closing Manager |
| 6 | Close and lock all high-value cages/cabinets | Closing Manager |
| 7 | Verify receiving dock door is closed and locked | Closing Manager |
| 8 | Walk through backroom — ensure no unauthorized persons present | Closing Manager |
| 9 | Shut down non-essential equipment; verify POS terminals locked | Closing Manager |
| 10 | Final walkthrough — lights (leave security lights on), HVAC, fire suppression status | Closing Manager |
| 11 | Set burglar alarm | Closing Manager |
| 12 | Exit through designated exit; verify door locked | Closing Manager (last to leave) |
| 13 | Exterior check — verify all doors secured, no suspicious activity | Closing Manager |
| 14 | Document closing in store security log | Closing Manager |

---

## 13.8 Annual Loss Prevention Plan

### 13.8.1 LP Calendar

| Activity | Frequency | Scope | Owner |
|----------|-----------|-------|-------|
| Shrinkage review (physical inventory results) | Annual | All locations | VP LP + VP Finance |
| LP awareness training for all store staff | Semi-annual | All stores | LP Coordinators |
| Cash handling audit | Monthly (random 20% of stores) | Rotating | LP Analysts |
| Receiving compliance audit | Monthly (random 20% of stores) | Rotating | LP Analysts |
| Exception report review | Daily | All stores | LP Coordinators |
| CCTV review (random) | Weekly (10% of stores) | Rotating | SOC + LP Analysts |
| Organized retail crime monitoring | Ongoing | Company-wide | LP Investigators |
| Background check (new hires in sensitive positions) | Per hire | Cashiers, inventory, LP | HR + LP |
| Vendor delivery audit (surprise) | Quarterly | Top 20 suppliers | LP Investigators |
| Annual LP plan review and update | Annual | Company-wide | VP LP |
| LP technology review (CCTV, EAS, alarm upgrades) | Annual | All locations | VP LP + VP Infrastructure |
