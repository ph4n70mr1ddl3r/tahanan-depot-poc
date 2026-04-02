# 05 — COMPANY POLICIES

---

## 5.2 Financial Policies (Detail)

### POL-FIN-001: Financial Authority and Approval Limits

**Effective Date:** 2026-01-01  
**Applies To:** All entities  
**Oracle Fusion Module:** Approval Workflow Engine, Purchasing, Payables, Expenses

#### Approval Matrix — Purchase Requisitions / Purchase Orders

| Amount Range (PHP) | Approver Level | Oracle Role |
|---------------------|---------------|-------------|
| 0 — 10,000 | Auto-approve (system) | FND_AUTO_APPROVE |
| 10,001 — 50,000 | Department Supervisor / Store Manager | ORA_PO_BUYER_SUPERVISOR |
| 50,001 — 200,000 | Department Manager / District Manager | ORA_PO_BUYER_MANAGER |
| 200,001 — 500,000 | Regional Director / VP | ORA_PO_BUYER_DIRECTOR |
| 500,001 — 5,000,000 | SVP / COO / CFO | ORA_PO_BUYER_VP |
| > 5,000,000 | CEO + CFO (joint) | ORA_PO_BUYER_CFO + ORA_PO_BUYER_CEO |

#### Approval Matrix — Journal Entries

| Amount Range (PHP) | Approver Level |
|---------------------|---------------|
| 0 — 100,000 | GL Supervisor |
| 100,001 — 1,000,000 | Controller |
| > 1,000,000 | VP Finance + CFO |

#### Approval Matrix — Expense Reports

| Amount Range (PHP) | Approver Level |
|---------------------|---------------|
| 0 — 5,000 | Direct Supervisor |
| 5,001 — 20,000 | Department Manager |
| 20,001 — 100,000 | VP |
| > 100,000 | CFO |

#### Approval Matrix — Capital Expenditure

| Amount Range (PHP) | Approver Level |
|---------------------|---------------|
| 0 — 500,000 | VP Finance |
| 500,001 — 5,000,000 | CFO |
| 5,000,001 — 20,000,000 | CEO |
| > 20,000,000 | Board of Directors |

**Rules:**
- No employee may approve their own requisition, expense, or journal entry.
- SoD enforced: requester ≠ approver ≠ receiver for all merchandise transactions.
- Emergency approvals (weekends/holidays) processed via mobile approval with subsequent review.
- All approvals timestamped and auditable in Oracle Fusion.

---

### POL-FIN-002: Expense Reimbursement Policy

**Effective Date:** 2026-01-01  
**Applies To:** All employees across all entities  
**Oracle Fusion Module:** Expenses

#### Allowable Expenses

| Category | Limit / Rule | Receipt Required |
|----------|-------------|-----------------|
| Air travel (domestic) | Economy class only; advance booking preferred | Yes |
| Air travel (international) | Economy class; business class requires VP approval | Yes |
| Hotel (Manila) | PHP 5,000/night max | Yes |
| Hotel (Provincial) | PHP 3,500/night max | Yes |
| Hotel (International) | USD 150/night max | Yes |
| Meals (Manila) | PHP 1,000/meal max | Yes (if > PHP 300) |
| Meals (Provincial) | PHP 800/meal max | Yes (if > PHP 300) |
| Transportation (Taxi/Grab) | Actual cost; PHP 500/trip max within Metro Manila | Yes (if > PHP 100) |
| Transportation (Rental car) | Requires pre-approval | Yes |
| Client entertainment | PHP 2,000/person max; VP pre-approval required | Yes |
| Mobile phone/internet | PHP 2,000/month (reimbursement or corporate plan) | Yes |
| Training and certifications | Pre-approved per L&D budget | Yes |

#### Rules
- Expenses must be submitted within 30 days of incurrence.
- Receipts uploaded via mobile app with OCR capture.
- Corporate credit card transactions auto-populate expense reports.
- Per diem (instead of receipts) allowed for multi-day provincial travel: PHP 2,000/day.
- Violations auto-flagged by Oracle Expenses policy rules; escalation to manager.

---

### POL-FIN-003: Cash Handling and Store Deposits

**Effective Date:** 2026-01-01  
**Applies To:** All 120 retail stores  
**Oracle Fusion Module:** Cash Management, Receivables

1. Each POS terminal performs end-of-day (EOD) closing; Z-reading generated.
2. Cashier counts drawer and reconciles to Z-reading; variance reported immediately.
3. Store supervisor verifies count and prepares bank deposit slip.
4. Cash deposit made to assigned bank branch within same business day (or next morning for late shifts).
5. Deposit slip scanned and uploaded to Oracle Cash Management.
6. Bank statement imported daily; auto-matched to POS receipts and deposit records.
7. Cash variance threshold: PHP 100 per register per day. Exceeding triggers investigation.
8. Three occurrences of cash variance >threshold in 30 days results in retraining and formal notice.
9. Cash in transit insured per corporate insurance policy.
10. Armored car service mandatory for stores with daily cash receipts > PHP 500,000.

---

### POL-FIN-004: Credit and Collections Policy (B2B)

**Effective Date:** 2026-01-01  
**Applies To:** Contractor and developer credit accounts  
**Oracle Fusion Module:** Receivables, Collections

#### Credit Terms

| Customer Tier | Credit Limit (PHP) | Payment Terms | Requirements |
|---------------|-------------------|---------------|--------------|
| Silver | Up to 500,000 | Net 30 | Trade references, SEC/DTI registration |
| Gold | 500,001 — 2,000,000 | Net 45 | 1-year trade history, audited FS |
| Platinum | 2,000,001 — 10,000,000 | Net 60 | 2-year trade history, audited FS, bank guarantee |

#### Collections Process

| Aging Bucket | Action | Responsible |
|-------------|--------|-------------|
| 1-30 days past due | Auto reminder email | System |
| 31-60 days past due | Phone call by collections specialist | AR Collections |
| 61-90 days past due | Formal demand letter; account placed on credit hold | AR Manager |
| > 90 days past due | Legal demand letter; account suspended | Legal + AR |
| > 180 days past due | Write-off consideration; legal action | CFO + Legal |

---

### POL-FIN-005: Revenue Recognition Policy

**Effective Date:** 2026-01-01  
**Applies To:** All revenue streams  
**Oracle Fusion Module:** Revenue Management

All revenue recognized in accordance with PFRS 15 / IFRS 15:

| Revenue Stream | Recognition Point |
|---------------|-------------------|
| In-store product sales | At point of sale (POS transaction completion) |
| E-commerce product sales | Upon delivery to customer (control transferred) |
| B2B product sales | Upon delivery or customer acceptance per contract |
| Gift cards | Deferred; recognized upon redemption |
| Loyalty points | Deferred; recognized upon redemption or expiry |
| Installation services | Over time as services are rendered |
| Tool rental | Ratably over rental period |
| Extended warranties | Deferred; recognized over warranty period |

---

### POL-FIN-006: Intercompany Transaction Pricing Policy

**Effective Date:** 2026-01-01  
**Applies To:** All intercompany transactions  
**Oracle Fusion Module:** Intercompany, Payables, Receivables

| Transaction Type | Pricing Basis |
|-----------------|---------------|
| Goods (SCM → Retail) | Cost + 8% markup |
| IT Services (Digital → Others) | Cost + 12% markup |
| Property Lease (Property → Others) | Market rate (appraised annually) |
| Management Fees (Holdings → Others) | 2% of revenue |
| Shared Services (HR, Finance) | Allocated by headcount ratio |

---

### POL-FIN-007: Capital Expenditure Approval Policy

**Effective Date:** 2026-01-01  
**Applies To:** All capex across all entities  
**Oracle Fusion Module:** Project Management, Assets, Planning

1. All capex requires pre-approval via EPM Capital Planning module.
2. Business case required for projects > PHP 1M (NPV, IRR, payback period).
3. Board approval required for individual projects > PHP 20M.
4. Monthly capex tracking against approved budget with variance reporting.
5. Project closeout and post-implementation review required within 90 days of completion.
6. Asset capitalization threshold: PHP 20,000 per unit; items below threshold expensed.
7. Construction-in-progress (CIP) accounts reviewed monthly; assets capitalized upon useful service.

---

## 5.3 Supply Chain Policies (Detail)

### POL-SCM-001: Procurement and Sourcing Policy

**Effective Date:** 2026-01-01  
**Applies To:** All procurement across all entities  
**Oracle Fusion Module:** Sourcing, Purchasing

1. Competitive bidding required for all purchases > PHP 100,000 (minimum 3 quotations).
2. Single/sole source justification required and documented in Oracle Sourcing when competitive bidding is not feasible.
3. Procurement from related parties requires CLO approval and arm's length pricing certification.
4. All suppliers must be registered in Oracle Supplier Management with complete BIR, SEC/DTI documentation.
5. No employee may receive gifts > PHP 2,000 per year from any single supplier (per Code of Conduct).
6. Emergency purchases (> PHP 50K) require verbal approval from VP followed by written confirmation within 24 hours.
7. All purchase orders tracked in Oracle Purchasing; no off-system procurement allowed.

---

### POL-SCM-002: Supplier Management Policy

**Effective Date:** 2026-01-01  
**Applies To:** All suppliers  
**Oracle Fusion Module:** Supplier Management

1. All suppliers undergo qualification process before first purchase order.
2. Minimum requirements: BIR registration, business permit, product quality certifications.
3. Supplier scorecards reviewed quarterly (on-time delivery, quality, price competitiveness, responsiveness).
4. Suppliers scoring below 60% for two consecutive quarters placed on probation.
5. Suppliers on probation for 6 months without improvement are deactivated.
6. Annual supplier business review conducted for top 50 suppliers by spend.
7. Supplier diversity program: minimum 10% procurement from MSMEs (per DTI guidelines).

---

### POL-SCM-003: Inventory Management Policy

**Effective Date:** 2026-01-01  
**Applies To:** All inventory locations  
**Oracle Fusion Module:** Inventory Management

1. Target inventory accuracy: 98% at SKU level, measured by cycle counting.
2. Cycle counting schedule:
   - A items (top 20% by value): Monthly
   - B items (next 30% by value): Quarterly
   - C items (remaining 50% by value): Semi-annually
3. Inventory adjustments > PHP 10,000 require controller approval.
4. Dead stock (no sales in 180 days) reviewed monthly; markdown or disposition action required within 30 days.
5. Damaged goods disposition within 14 days; vendor claims filed within 7 days of discovery.
6. Annual physical inventory conducted in Q1 per BIR requirements.
7. Safety stock levels reviewed monthly by supply planning; min/max parameters updated quarterly.
8. Inventory write-off approval: Store Manager < PHP 5K, Regional Director < PHP 50K, VP > PHP 50K.

---

### POL-SCM-004: Warehouse Safety Policy

**Effective Date:** 2026-01-01  
**Applies To:** All 4 distribution warehouses  
**Oracle Fusion Module:** HCM Workforce Health & Safety

1. All warehouse personnel must complete safety orientation before assignment.
2. PPE (hard hat, safety shoes, high-visibility vest, gloves) mandatory at all times in warehouse.
3. Forklift operators must be certified; annual recertification required.
4. Maximum stacking height: 5 pallets (or as rated by racking system).
5. Incident reporting within 1 hour of occurrence in Oracle HCM Workforce Health & Safety.
6. Monthly safety inspection by warehouse safety officer.
7. Quarterly safety committee meeting with documented minutes and action items.
8. Zero tolerance for working under the influence of alcohol or drugs.

---

### POL-SCM-005: Import and Customs Compliance Policy

**Effective Date:** 2026-01-01  
**Applies To:** All imported goods  
**Oracle Fusion Module:** Global Trade Management

1. All imports must comply with Bureau of Customs (BOC) regulations.
2. HS (Harmonized System) codes validated at item setup; reviewed annually.
3. Restricted goods (chemicals, certain building materials) require BIR/BOC permits before importation.
4. Licensed customs broker engaged for all import entries.
5. Duty savings opportunities (ASEAN FTA, special economic zone incentives) actively pursued.
6. Accurate valuation declared on all imports; transfer pricing documentation maintained.
7. Import documentation retained for 10 years per BOC requirements.

---

## 5.4 Retail Policies (Detail)

### POL-RET-001: Customer Return and Refund Policy

**Effective Date:** 2026-01-01  
**Applies To:** All retail stores  
**Oracle Fusion Module:** Order Management, Receivables, Inventory

| Condition | Policy |
|-----------|--------|
| Unused, with receipt, within 30 days | Full refund or exchange |
| Unused, with receipt, 31-60 days | Store credit only |
| Used but defective, with receipt | Full refund or exchange within warranty period |
| No receipt | Store credit at lowest sale price (last 90 days) |
| Special order / cut material | No return unless defective |
| Plants and live goods | 1-year guarantee (replacement only) |
| Appliances and power tools | Per manufacturer warranty; store facilitates |
| Clearance items | Final sale; no returns |
| Gift cards | Non-refundable; no expiration per Philippine law |

**Rules:**
- Refund to original payment method.
- Returns > PHP 10,000 require supervisor override.
- Returns > PHP 50,000 require Store Manager approval.
- Fraudulent return attempts flagged in POS system and Oracle.

---

### POL-RET-002: Store Pricing and Markdown Policy

**Effective Date:** 2026-01-01  
**Applies To:** All retail stores  
**Oracle Fusion Module:** Order Management (Pricing), SCM

1. All retail prices set centrally by Merchandising team in Oracle Pricing.
2. Store-level price overrides not permitted; all pricing changes originate from Merchandising.
3. Price match policy: Match competitor's verified current price for identical items within 7 days of purchase.
4. Markdown schedule:
   - Seasonal markdowns approved by Category Manager quarterly.
   - Clearance markdowns for discontinuation approved by VP Merchandising.
   - Damaged goods markdown up to 50% by Store Manager; >50% by Regional Director.
5. Promotional pricing created as separate price lists with defined start/end dates.
6. All price changes reflected in POS via real-time sync with Oracle Pricing.

---

### POL-RET-003: Store Inventory Accuracy Policy

**Effective Date:** 2026-01-01  
**Applies To:** All 120 retail stores  
**Oracle Fusion Module:** Inventory Management

1. Target store inventory accuracy: 95% at SKU level.
2. Daily spot checks: 20 high-value/high-shrink SKUs per store per day.
3. Weekly cycle count: Department-level rotation covering all departments monthly.
4. Shrinkage target: < 1.5% of sales.
5. Shrinkage > 2% triggers formal investigation by Loss Prevention team.
6. All inventory movements (sales, transfers, adjustments, damages) recorded in real-time via POS and Oracle.

---

### POL-RET-004: Gift Card Policy

**Effective Date:** 2026-01-01  
**Applies To:** All retail stores and e-commerce  
**Oracle Fusion Module:** Revenue Management, Receivables

1. Gift cards sold at face value; no discount on gift card purchases.
2. Gift cards have no expiration date (per Philippine Consumer Act).
3. Gift cards not redeemable for cash (except balances < PHP 100 per BSP guidelines).
4. Lost/stolen gift cards not replaceable unless registered.
5. Revenue from gift card sales deferred; recognized upon redemption.
6. Monthly gift card liability report reviewed by Finance.

---

## 5.5 HR Policies (Detail)

### POL-HR-001: Recruitment and Hiring Policy

**Effective Date:** 2026-01-01  
**Applies To:** All entities  
**Oracle Fusion Module:** HCM Recruiting

1. All positions filled through Oracle Recruiting; no off-system hiring.
2. Internal candidates given preference; minimum 3-day internal-only posting period.
3. Pre-employment requirements: NBI clearance, police clearance, medical exam, SSS/PhilHealth/Pag-IBIG numbers, TIN, diploma/transcript.
4. Probationary employment: 6 months per Philippine Labor Code.
5. Background checks mandatory for positions handling cash, inventory, or sensitive data.
6. Equal opportunity employer; no discrimination per Philippine Labor Code.
7. Nepotism: Relatives within 2nd degree of consanguinity may not hold positions in direct reporting line or in internal audit.

---

### POL-HR-002: Compensation and Benefits Policy

**Effective Date:** 2026-01-01  
**Applies To:** All regular employees  
**Oracle Fusion Module:** HCM Compensation, Benefits, Payroll

#### Compensation Structure

| Component | Description |
|-----------|-------------|
| Basic Salary | Market-positioned; reviewed annually; compliant with regional minimum wage orders |
| 13th Month Pay | Mandatory; paid in two tranches (May and November) |
| Allowances | Rice subsidy (PHP 2,000/mo), transportation (PHP 1,500/mo), laundry (for store ops) |
| Variable Pay | Store performance bonus (quarterly, based on sales target achievement) |
| Overtime | Per Philippine Labor Code: 125% (ordinary), 130% (rest day), 200% (holiday) |

#### Statutory Benefits

| Benefit | Employee Share | Employer Share |
|---------|---------------|----------------|
| SSS | Per SSS table | Per SSS table (EC for rank-and-file) |
| PhilHealth | Per PhilHealth table | Per PhilHealth table |
| Pag-IBIG | PHP 100 (for salary ≤ PHP 1,500) or 2% | 2% (max PHP 100) |
| Withholding Tax | Per TRAIN law brackets | Employer remits |

#### Company Benefits

| Benefit | Coverage |
|---------|----------|
| HMO | Maxicare Prima (employee + 2 dependents) |
| Group Life Insurance | 2x annual basic salary |
| Accident Insurance | 24-hour coverage |
| Retirement Plan | BIR-approved retirement plan; 1/2 month per year of service |

---

### POL-HR-003: Time and Attendance Policy

**Effective Date:** 2026-01-01  
**Applies To:** All employees  
**Oracle Fusion Module:** Time and Labor, Workforce Scheduling

1. All employees must clock in/out at start and end of shift.
2. Clock-in methods: POS terminal (store staff), biometric (warehouse/HQ), Oracle ME mobile (field/remote).
3. Grace period: 10 minutes from shift start. Beyond 10 minutes = late (docked proportionally).
4. Undertime: Requires supervisor approval; minimum 4-hour work for half-day credit.
5. Overtime: Must be pre-approved by supervisor; auto-calculated in Time & Labor.
6. Schedule changes: Manager posts to Workforce Scheduling; employee notified via Oracle ME.
7. Missed punch: Must be reported same day; supervisor enters manual correction with reason code.

---

### POL-HR-004: Leave Management Policy

**Effective Date:** 2026-01-01  
**Applies To:** All regular employees  
**Oracle Fusion Module:** Absence Management

| Leave Type | Entitlement | Carry Over | Remarks |
|------------|------------|------------|---------|
| Vacation Leave (VL) | 15 days/year (after 1 year) | Up to 5 days | Pro-rated in first year |
| Sick Leave (SL) | 15 days/year (after 1 year) | Up to 5 days | Pro-rated in first year |
| Maternity Leave | 105 days (per RA 11210) | No | Single mothers: +15 days |
| Paternity Leave | 7 days (per RA 8187) | No | For first 4 deliveries |
| Solo Parent Leave | 7 days/year (per RA 8972) | No | Solo parent ID required |
| Special Leave for Women (VAWC) | 10 days/year (per RA 9262) | No | |
| Bereavement Leave | 3-5 days (per relationship) | No | |
| Special Privilege Leave | 3 days/year | No | Personal reasons |
| Study Leave | Per HRBP approval | No | Job-related courses |
| Force Leave | 5 days mandatory VL use | No | Must use within year |

---

### POL-HR-005: Performance Management Policy

**Effective Date:** 2026-01-01  
**Applies To:** All regular employees  
**Oracle Fusion Module:** Performance Management, Goals

1. Annual performance cycle: January - December.
2. Goal setting: Cascading from company → department → individual by January 31.
3. Quarterly check-ins documented in Oracle Touchpoints.
4. Mid-year review: Informal check-in by July 31.
5. Annual performance review: Completed by January 15 of following year.
6. Rating scale: 5-point (5=Exceptional, 4=Exceeds, 3=Meets, 2=Below, 1=Unsatisfactory).
7. Calibration sessions at regional and departmental levels.
8. Performance improvement plan (PIP) for ratings of 2 or below; 90-day improvement period.
9. Merit increase based on performance rating and market position; approved by CHRO.
10. Variable pay (store bonus) based on store sales target achievement and individual rating.

---

### POL-HR-006: Disciplinary Action and Termination Policy

**Effective Date:** 2026-01-01  
**Applies To:** All employees  
**Oracle Fusion Module:** Core HR, Document Records

1. Progressive discipline for performance/behavior issues:
   - First offense: Verbal warning (documented)
   - Second offense: Written warning
   - Third offense: Suspension (3-30 days per DOLE guidelines)
   - Fourth offense: Termination (with due process per Labor Code)
2. Gross misconduct: Immediate preventive suspension pending investigation (maximum 30 days per Labor Code).
3. Due process: Written notice of charges, opportunity to respond (within 5 days), hearing, written decision.
4. Clearance process: All company properties returned; final pay computed per DOLE requirements.
5. Final pay released within 30 days of separation per DOLE Advisory.
6. All disciplinary actions documented in Oracle HCM Document Records.

---

### POL-HR-007: Workplace Health and Safety Policy

**Effective Date:** 2026-01-01  
**Applies To:** All locations  
**Oracle Fusion Module:** Workforce Health & Safety

1. All workplace incidents reported within 1 hour in Oracle Workforce Health & Safety.
2. First aid kits maintained at every store and warehouse; inspected monthly.
3. Fire drills conducted quarterly at every location.
4. Safety committee established per location; includes employee representatives.
5. Ergonomic assessments for office workers annually.
6. Annual medical examination for all employees (company-provided).
7. Mental health support: Employee Assistance Program (EAP) available.
8. Compliance with DOLE Department Order 198 (OSHS).

---

### POL-HR-008: Code of Conduct and Ethics

**Effective Date:** 2026-01-01  
**Applies To:** All employees, officers, and directors  
**Oracle Fusion Module:** Advanced Controls, Narrative Reporting

1. Honest and ethical conduct in all business dealings.
2. Compliance with all applicable laws and regulations.
3. No conflicts of interest; disclosed annually via conflict of interest form.
4. No solicitation or acceptance of gifts > PHP 2,000/year from any business partner.
5. Protection and proper use of company assets.
6. Confidentiality of company information and trade secrets.
7. Whistleblower protection: Anonymous reporting via Integrity Helpline.
8. Violations reported to Ethics Committee; serious violations to Board Audit Committee.
9. Annual Code of Conduct certification by all employees via Oracle Learning.

---

### POL-HR-009: Anti-Sexual Harassment Policy

**Effective Date:** 2026-01-01  
**Applies To:** All employees, contractors, visitors  
**Oracle Fusion Module:** Core HR, Document Records

1. Zero tolerance for sexual harassment (per RA 7877, Safe Spaces Act RA 11313).
2. Committee on Decorum and Investigation (CODI) established per legal requirements.
3. Confidential reporting channels: HR, CODI, Integrity Helpline.
4. Investigation completed within 30 days; due process for all parties.
5. Mandatory annual anti-sexual harassment training for all employees via Oracle Learning.
6. Retaliation against complainants is a terminable offense.

---

### POL-HR-010: Data Privacy Policy

**Effective Date:** 2026-01-01  
**Applies To:** All personal data (employees, customers, suppliers)  
**Oracle Fusion Module:** All modules, Security

1. Compliance with the Philippine Data Privacy Act of 2012 (RA 10173) and NPC regulations.
2. Data Protection Officer (DPO) appointed; reports to CLO.
3. Personal data collected only for legitimate business purposes; consent obtained.
4. Access to personal data restricted on need-to-know basis; enforced by Oracle role-based access.
5. Data retention periods defined per data category; automated purge per schedule.
6. Data breach notification within 72 hours per NPC requirements.
7. Annual privacy impact assessment for new systems and processes.
8. Employee data processed in Oracle HCM with appropriate consent and legal basis.
9. Customer data processed in Oracle CX with consent; managed via CDP privacy controls.

---

## 5.6 IT Policies (Detail)

### POL-IT-001: Information Security Policy

**Effective Date:** 2026-01-01  
**Applies To:** All systems, data, and users  
**Oracle Fusion Module:** Security, Advanced Controls

1. All access to Oracle Fusion via SSO with MFA (multi-factor authentication).
2. Role-based access control (RBAC); minimum access principle enforced.
3. Password policy: Minimum 12 characters, complexity rules, 90-day rotation.
4. No sharing of user accounts; individual accountability.
5. Segregation of duties enforced via Oracle Advanced Controls.
6. Quarterly access review and certification by department heads.
7. Encryption at rest and in transit for all data.
8. Security incident response plan tested annually.
9. Third-party access via VPN and time-limited accounts only.
10. Annual penetration testing and vulnerability assessment.

---

### POL-IT-002: POS System Usage Policy

**Effective Date:** 2026-01-01  
**Applies To:** All POS terminal users  
**Oracle Fusion Module:** Integration with POS

1. Only authorized users may operate POS terminals; individual login required.
2. No unauthorized software may be installed on POS terminals.
3. POS terminals used exclusively for sales transactions and approved functions (receiving, inventory, timekeeping).
4. No personal use of POS terminals.
5. Cash drawer opened only by assigned cashier; supervisor override logged.
6. POS data is company property; no extraction or copying without authorization.
7. POS terminals locked when unattended; auto-lock after 5 minutes of inactivity.
8. Any suspected tampering reported immediately to IT Security.

---

### POL-IT-003: Change Management Policy

**Effective Date:** 2026-01-01  
**Applies To:** All system changes (Oracle Fusion, POS, integrations)  
**Oracle Fusion Module:** All

1. All changes follow the change management process: Request → Assessment → Approval → Build → Test → Deploy → Review.
2. Emergency changes: Verbal approval from VP IT + post-implementation review within 48 hours.
3. Standard changes: Approved by Change Advisory Board (CAB) weekly.
4. No production changes on Fridays, weekends, or peak sales days (month-end, payday weekends).
5. Rollback plan required for all changes.
6. POS changes tested in staging environment replicating all terminal types before production.
7. Oracle Fusion quarterly updates reviewed in test instance before production activation.

---

### POL-IT-004: Business Continuity and Disaster Recovery Policy

**Effective Date:** 2026-01-01  
**Applies To:** All systems  
**Oracle Fusion Module:** All (infrastructure level)

1. RPO (Recovery Point Objective): 1 hour for all critical systems.
2. RTO (Recovery Time Objective): 4 hours for Oracle Fusion; 1 hour for POS (with offline mode).
3. POS designed to operate offline for up to 24 hours; transactions cached and synced upon reconnection.
4. Oracle Fusion hosted on OCI with built-in HA/DR.
5. Disaster recovery plan tested semi-annually.
6. Business continuity plan maintained for each critical business function.
7. Alternative communication channels established for system outage notifications.

---

## 5.7 Customer Experience Policies (Detail)

### POL-CX-001: Customer Data Privacy and Protection Policy

**Effective Date:** 2026-01-01  
**Applies To:** All customer data  
**Oracle Fusion Module:** CX Customer Data Platform, Marketing

1. Customer data collected only with consent; purpose clearly communicated.
2. Customer data used only for stated purposes (order processing, loyalty, marketing opt-in).
3. Customers may opt out of marketing communications at any time.
4. Customer data retained per retention schedule; deleted upon request per DPA.
5. No sale of customer data to third parties.
6. Customer data access requests fulfilled within 15 days per DPA.
7. Loyalty program data used to personalize offers; transparent to customers.

---

### POL-CX-002: Loyalty Program Terms and Conditions

**Effective Date:** 2026-01-01  
**Applies To:** Tahanan Rewards members  
**Oracle Fusion Module:** Customer Loyalty, CDP

1. Membership is free; open to individuals 18 years and above.
2. Points earned at 1 point per PHP 50 spent (net of discounts, excluding gift card purchases).
3. Points redeemed at 1 point = PHP 1 discount on future purchase.
4. Tier system:
   - Silver: 0-49,999 annual spend
   - Gold: 50,000-149,999 annual spend (1.5x point multiplier)
   - Platinum: 150,000+ annual spend (2x point multiplier + exclusive perks)
5. Points do not expire for active members (transaction within 12 months).
6. Points are non-transferable and have no cash value until redemption.
7. Fraudulent point accumulation results in account suspension.
8. Program terms may be modified with 30-day notice to members.
