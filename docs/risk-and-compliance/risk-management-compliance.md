# 11 — RISK MANAGEMENT & COMPLIANCE

## 11.1 Enterprise Risk Management Framework

### 11.1.1 Risk Governance Structure

```
BOARD OF DIRECTORS
├── Board Audit Committee (BAC)
│   ├── Oversees enterprise risk management
│   ├── Reviews risk register quarterly
│   └── Approves risk appetite statement
│
└── RISK MANAGEMENT COMMITTEE (RMC)
    ├── Members: CFO (Chair), COO, CIO, CHRO, CLO, VP Internal Audit
    ├── Frequency: Monthly meetings; quarterly board reporting
    └── Responsibilities:
        ├── Approve risk policies and framework
        ├── Review and update enterprise risk register
        ├── Monitor risk mitigation actions
        ├── Escalate critical risks to Board
        └── Review regulatory compliance status
```

### 11.1.2 Risk Appetite Statement

| Risk Category | Appetite Level | Rationale |
|---------------|---------------|-----------|
| Financial (earnings volatility) | Low | Stable shareholder returns; < 10% earnings variance from plan |
| Operational (supply chain disruption) | Low-Medium | Accept short-term disruptions; intolerant of prolonged outages |
| Compliance / Regulatory | Very Low | Zero tolerance for regulatory non-compliance |
| Cybersecurity | Very Low | Zero tolerance for data breaches; maximum system availability |
| Strategic (new markets) | Medium | Willing to accept calculated risks in expansion |
| Reputational | Very Low | Zero tolerance for brand-damaging incidents |
| Environmental / Safety | Very Low | Zero tolerance for workplace fatalities or environmental incidents |

### 11.1.3 Risk Assessment Methodology

| Component | Scale | Definition |
|-----------|-------|------------|
| **Likelihood** | 1 - Rare | Unlikely to occur within 3 years |
| | 2 - Unlikely | May occur once in 3 years |
| | 3 - Possible | May occur once per year |
| | 4 - Likely | May occur multiple times per year |
| | 5 - Almost Certain | Expected to occur regularly |
| **Impact** | 1 - Negligible | < PHP 1M financial; no operational disruption |
| | 2 - Minor | PHP 1M - 10M; minor operational disruption (< 1 day) |
| | 3 - Moderate | PHP 10M - 50M; moderate disruption (1-3 days) |
| | 4 - Major | PHP 50M - 200M; significant disruption (3-7 days) |
| | 5 - Catastrophic | > PHP 200M; critical disruption (> 7 days); reputational damage |
| **Risk Score** | Likelihood × Impact | 1-25 scale |
| | Low (1-4) | Accept / Monitor |
| | Medium (5-9) | Mitigate with controls |
| | High (10-16) | Active mitigation; senior management oversight |
| | Critical (17-25) | Immediate action; Board escalation |

---

## 11.2 Enterprise Risk Register

### 11.2.1 Strategic Risks

| Risk ID | Risk Description | Likelihood | Impact | Score | Mitigation Strategy | Owner | Oracle Fusion Touchpoint |
|---------|-----------------|------------|--------|-------|-------------------|-------|------------------------|
| RSK-STR-001 | Failure to achieve target store count expansion on schedule | 3 | 3 | 9 | Phased rollout with contingencies; robust site selection process | COO | EPM Planning (capital planning, scenario modeling) |
| RSK-STR-002 | Market share erosion from competitors (Wilcon, Handyman, ACE) | 3 | 4 | 12 | Differentiation via loyalty, service, assortment; competitive monitoring | CMO | CX Analytics, ERP Analytics (market share tracking) |
| RSK-STR-003 | Economic downturn reducing consumer spending on home improvement | 3 | 4 | 12 | Diversified price points; value assortment; contractor B2B focus during downturns | CEO / CFO | EPM Planning (scenario modeling, rolling forecasts) |
| RSK-STR-004 | Oracle Fusion or POS integration failure | 2 | 5 | 10 | Experienced SI partner; phased pilot approach; rollback plans | CIO | OIC monitoring; POS offline mode |
| RSK-STR-005 | Foreign exchange fluctuation impacting imported goods cost | 4 | 3 | 12 | Forward contracts; diversified sourcing (local alternatives); hedging strategy | VP Treasury | Cash Management, Global Trade Management |

### 11.2.2 Operational Risks

| Risk ID | Risk Description | Likelihood | Impact | Score | Mitigation Strategy | Owner | Oracle Fusion Touchpoint |
|---------|-----------------|------------|--------|-------|-------------------|-------|------------------------|
| RSK-OPS-001 | Supply chain disruption (port congestion, typhoon, supplier failure) | 4 | 4 | 16 | Multi-supplier strategy; safety stock buffers; alternative sourcing routes | VP Supply Chain | SCP (demand/supply planning), WMS, TMS |
| RSK-OPS-002 | POS system failure causing store-level outage | 2 | 3 | 6 | Offline mode (24-hour capability); L1-L3 support tiers; redundant hardware | VP Digital Products | POS Integration (Doc 08); OIC monitoring |
| RSK-OPS-003 | Warehouse accident causing injury or fatality | 2 | 5 | 10 | Safety training; PPE enforcement; regular inspections; forklift certification | VP Distribution | HCM Workforce Health & Safety |
| RSK-OPS-004 | Inventory shrinkage exceeding target (theft, damage, administrative error) | 3 | 3 | 9 | Loss prevention program; cycle counting; surveillance; access controls | VP Store Ops | Inventory Management (cycle count, adjustments) |
| RSK-OPS-005 | Product recall or safety incident | 2 | 4 | 8 | Quality inspection; supplier quality management; recall procedure; insurance | VP Procurement | PLM Quality Management |
| RSK-OPS-006 | New store opening delays or underperformance | 3 | 3 | 9 | Rigorous site selection; phased opening; post-opening monitoring (30-day intensive) | VP Store Dev | EPM Planning, ERP Analytics |
| RSK-OPS-007 | Warehouse capacity constraints during peak seasons | 3 | 3 | 9 | Capacity planning; cross-docking; overflow arrangements; demand forecasting | VP Distribution | SCP, WMS (capacity management) |
| RSK-OPS-008 | Transportation and logistics disruption | 3 | 3 | 9 | Multi-carrier strategy; own fleet backup; route optimization; 3PL partnerships | VP Supply Chain | TMS (route planning, carrier management) |

### 11.2.3 Financial Risks

| Risk ID | Risk Description | Likelihood | Impact | Score | Mitigation Strategy | Owner | Oracle Fusion Touchpoint |
|---------|-----------------|------------|--------|-------|-------------------|-------|------------------------|
| RSK-FIN-001 | Cash flow shortage due to receivables collection delays | 2 | 4 | 8 | Strict credit policy; automated collections; cash forecasting; bank lines | VP Treasury | Cash Management (forecasting), AR (collections) |
| RSK-FIN-002 | Fraud or misappropriation of assets | 2 | 4 | 8 | SoD enforcement; transaction controls; internal audit; whistleblower hotline | VP Internal Audit | Advanced Controls, Transaction Controls |
| RSK-FIN-003 | Material financial statement misstatement | 1 | 5 | 5 | Automated reconciliation; external audit; dual review; close process controls | VP Finance | Account Reconciliation, FCC, Audit workflows |
| RSK-FIN-004 | Interest rate increase on variable-rate debt | 2 | 2 | 4 | Fixed-rate preference; interest rate monitoring; hedging where material | VP Treasury | Cash Management |
| RSK-FIN-005 | Tax assessment or penalty from BIR | 2 | 3 | 6 | Automated tax computation; external tax advisor; BIR compliance calendar; quarterly reviews | VP Tax | Tax Reporting, Payables (EWT automation) |

### 11.2.4 Compliance / Regulatory Risks

| Risk ID | Risk Description | Likelihood | Impact | Score | Mitigation Strategy | Owner | Oracle Fusion Touchpoint |
|---------|-----------------|------------|--------|-------|-------------------|-------|------------------------|
| RSK-REG-001 | BIR non-compliance (VAT, withholding, income tax) | 2 | 4 | 8 | Automated tax processing; compliance calendar; external tax firm quarterly review | VP Tax | Tax Reporting, Payables, Payroll |
| RSK-REG-002 | DOLE labor law violation (wages, benefits, termination) | 2 | 4 | 8 | Automated payroll; legal review of terminations; HR training; DOLE compliance audits | CHRO | HCM Payroll, Absence Management, Core HR |
| RSK-REG-003 | SEC reporting non-compliance | 1 | 4 | 4 | External auditor; compliance calendar; automated consolidation | VP Finance | FCC, Narrative Reporting |
| RSK-REG-004 | Data Privacy Act (RA 10173) violation | 2 | 4 | 8 | DPO appointment; privacy impact assessments; consent management; breach notification procedure | CLO / DPO | CX CDP, HCM (data access controls) |
| RSK-REG-005 | Consumer Act violation (product safety, pricing, warranties) | 2 | 3 | 6 | Quality control; compliant pricing; warranty tracking; customer complaint process | CLO | PLM Quality, Order Management (returns) |
| RSK-REG-006 | Bureau of Customs import violation | 2 | 4 | 8 | Licensed customs broker; GTM compliance checks; HS code validation; documentation retention | VP Procurement | Global Trade Management |
| RSK-REG-007 | Local government permit / zoning non-compliance | 2 | 3 | 6 | Centralized permit tracking; legal review for new locations; annual renewal calendar | CLO | Narrative Reporting (compliance tracking) |

### 11.2.5 Technology / Cybersecurity Risks

| Risk ID | Risk Description | Likelihood | Impact | Score | Mitigation Strategy | Owner | Oracle Fusion Touchpoint |
|---------|-----------------|------------|--------|-------|-------------------|-------|------------------------|
| RSK-TECH-001 | Ransomware or cyberattack on corporate systems | 2 | 5 | 10 | Endpoint protection; MFA; network segmentation; incident response plan; cyber insurance; annual penetration testing | VP Infra & Security | Oracle Security, Advanced Controls |
| RSK-TECH-002 | Data breach exposing customer or employee PII | 1 | 5 | 5 | Encryption; RBAC; DLP; breach notification procedure; cyber insurance; annual penetration testing | VP Infra & Security | All modules (data access controls) |
| RSK-TECH-003 | Oracle Fusion service outage | 2 | 4 | 8 | OCI built-in HA/DR; POS offline mode; alternative communication channels | VP Enterprise Apps | OCI infrastructure, OIC monitoring |
| RSK-TECH-004 | Insider threat (data theft, sabotage) | 2 | 4 | 8 | Background checks; SoD; access reviews; audit logging; activity monitoring | VP Infra & Security | Advanced Controls, Audit trails |
| RSK-TECH-005 | Third-party vendor security breach | 2 | 3 | 6 | Vendor security assessments; contractual security requirements; VPN access only; time-limited access | VP Infra & Security | Supplier Management, Security |

### 11.2.6 Environmental / Natural Disaster Risks

| Risk ID | Risk Description | Likelihood | Impact | Score | Mitigation Strategy | Owner | Oracle Fusion Touchpoint |
|---------|-----------------|------------|--------|-------|-------------------|-------|------------------------|
| RSK-ENV-001 | Typhoon damage to stores or warehouses | 4 | 4 | 16 | Property insurance; building codes compliance; typhoon preparedness protocol; geographically distributed operations | VP Facilities | Assets (insurance tracking), Inventory (stock redistribution) |
| RSK-ENV-002 | Earthquake damage | 2 | 5 | 10 | Building structural standards; insurance; emergency response plans | VP Facilities | Assets (insurance tracking) |
| RSK-ENV-003 | Flooding disrupting warehouse or store operations | 3 | 3 | 9 | Flood risk assessment in site selection; flood mitigation measures; stock elevation; alternative DC routing | VP Facilities | WMS (stock relocation), TMS (route diversion) |
| RSK-ENV-004 | Fire at store or warehouse | 2 | 5 | 10 | Fire suppression systems; fire drills; insurance; no-smoking policy; electrical safety inspections | VP Facilities | HCM Workforce Health & Safety, Assets (insurance) |

---

## 11.3 Regulatory Compliance Matrix

### 11.3.1 Philippine Regulatory Compliance Register

| Regulation / Agency | Applicable To | Compliance Requirement | Responsible | Frequency | Oracle Fusion Support | Evidence / Documentation |
|---------------------|--------------|----------------------|-------------|-----------|----------------------|------------------------|
| **BIR — National Internal Revenue Code** | | | | | | |
| Income Tax (RCIT/MCIT) | All entities | Corporate income tax filing (BIR Form 1702) | VP Tax | Annual (April 15) | Tax Reporting | Tax returns, financial statements |
| Monthly VAT (2550M) | All entities | Monthly VAT return filing | VP Tax | Monthly (20th) | Tax Reporting, Payables, AR | VAT returns, sales/purchase books |
| Quarterly VAT (2550Q) | All entities | Quarterly VAT return filing | VP Tax | Quarterly (25th) | Tax Reporting | VAT returns |
| Expanded WHT (1601-E) | All entities | Monthly EWT remittance | VP Tax | Monthly (10th) | Payables (auto EWT) | EWT returns, alpha list |
| Compensation WHT (1601-C) | All entities | Monthly WTA remittance | Payroll Manager | Monthly (10th) | Payroll (auto WTA) | WTA returns |
| Annual WHT on Compensation (1604-C) | All entities | Annual reconciliation and filing | Payroll Manager | Annual (Jan 31) | Payroll | 1604-C form, alphalist |
| Annual WHT on Income Payments (1604-E) | All entities | Annual supplier alphalist | AP Manager | Annual (Jan 31) | Payables | 1604-E form, alphalist |
| Quarterly Income Tax (1701Q/1702Q) | All entities | Quarterly income tax return | VP Tax | Quarterly | Tax Reporting | Quarterly returns |
| BIR Registration (0605) | All entities | Annual registration fee | VP Tax | Annual (Jan 31) | Manual + Oracle data | Registration certificates |
| BIR-registered receipts/invoices | Retail, SCM | Sequential, BIR-compliant receipts | POS Dev Manager | Ongoing | POS (receipt generation), AR | Receipt books, POS audit trail |
| **SEC — Securities and Exchange Commission** | | | | | | |
| Annual Financial Statements | Holdings (if public) | Audited FS filing | VP Finance | Annual | FCC, Narrative Reporting | Audited FS, auditor's report |
| General Information Sheet (GIS) | All entities | Annual corporate information filing | CLO | Annual | Narrative Reporting | GIS filing |
| SEC registration updates | All entities | Material changes reporting | CLO | As needed | Manual | SEC filings |
| **DOLE — Department of Labor and Employment** | | | | | | |
| Labor Standards compliance | All entities | Minimum wage, working hours, benefits | CHRO | Ongoing | HCM Payroll, T&L | Payroll records, employment contracts |
| 13th Month Pay | All entities | Mandatory 13th month computation and payment | Payroll Manager | Annual (or semi-annual) | Payroll | Payroll records |
| SSS / PhilHealth / Pag-IBIG remittances | All entities | Monthly statutory contributions | Payroll Manager | Monthly | Payroll (auto computation) | Remittance forms (R5, ER2, MCRF) |
| OSHS (DO 198) compliance | All locations | Occupational safety and health standards | VP HR / Safety | Ongoing | HCM Workforce Health & Safety | Safety inspection reports, incident records |
| Maternity Leave (RA 11210) | All entities | 105-day paid maternity leave | HRBP | Per event | Absence Management | Leave records |
| Anti-Sexual Harassment (RA 7877) | All entities | CODI establishment; policy; training | CHRO | Annual training | Core HR, Learning | CODI records, training completion |
| **DTI — Department of Trade and Industry** | | | | | | |
| Consumer Act compliance | Retail | Product safety, pricing transparency, warranties | CLO | Ongoing | PLM Quality, POS (receipt compliance) | Customer complaint records |
| Business name registration | All entities | Business name registration | CLO | As needed | Manual | DTI registration |
| **BOC — Bureau of Customs** | | | | | | |
| Import compliance | SCM | Proper customs declaration, duty payment | VP Procurement | Per importation | Global Trade Management | Import entries, customs documents |
| **NPC — National Privacy Commission** | | | | | | |
| Data Privacy Act (RA 10173) | All entities | DPO appointment; privacy impact assessment; breach notification | DPO / CLO | Ongoing | All modules (data access controls) | DPIA reports, consent records, breach logs |
| **BSP — Bangko Sentral ng Pilipinas** | | | | | | |
| Anti-Money Laundering (RA 9160) | All entities | Covered transaction reporting; CDD/EDD | VP Treasury / CLO | As needed | Cash Management, Payables | Transaction records, CDD documentation |
| **Local Government Units** | | | | | | |
| Business permits | All locations | Annual business permit renewal | VP Facilities / CLO | Annual | Narrative Reporting (calendar) | Business permits |
| Fire safety certificate | All locations | Annual fire safety inspection | VP Facilities | Annual | Manual | Fire safety certificates |
| Zoning clearance | New locations | Zoning compliance for new stores/warehouses | VP Real Estate | Per new location | Manual | Zoning clearances |

### 11.3.2 Compliance Calendar

| Month | Compliance Activity | Owner | Deadline |
|-------|-------------------|-------|----------|
| Monthly (10th) | WTA remittance (BIR 1601-C), EWT remittance (BIR 1601-E) | Payroll / AP | 10th |
| Monthly (15th) | SSS, PhilHealth, Pag-IBIG remittances | Payroll | 15th (or per agency schedule) |
| Monthly (20th) | VAT return filing (BIR 2550M) | VP Tax | 20th |
| Quarterly | Quarterly VAT (BIR 2550Q), Quarterly Income Tax (1702Q) | VP Tax | Per BIR schedule |
| January | Annual business permit renewal (LGU), Fire safety inspection | VP Facilities | Jan 31 |
| January | BIR 1604-C/W (annual compensation WHT), BIR 1604-E (annual supplier WHT) | Payroll / AP | Jan 31 |
| April | Annual Income Tax Return (BIR 1702) | VP Tax | April 15 |
| May | 13th Month Pay — First tranche | Payroll | May 15 |
| November | 13th Month Pay — Second tranche | Payroll | Nov 30 |
| December | Annual SEC filings (GIS, audited FS if applicable) | VP Finance / CLO | Per SEC schedule |

---

## 11.4 Insurance Coverage

### 11.4.1 Insurance Portfolio

| Policy Type | Coverage | Insured Value / Limit | Deductible | Insurer |
|-------------|----------|----------------------|------------|---------|
| Property All-Risk | All stores, warehouses, corporate HQ, contents, stock | PHP 25B (total insured value) | PHP 500K per event | Leading PH insurer |
| Business Interruption | Loss of income from covered events | 12-month projected revenue | 72-hour waiting period | Same as property |
| Fire & Lightning | Buildings, contents, stock | Included in Property All-Risk | Included | Same as property |
| Typhoon / Flood | Named typhoon and flood damage | Sublimit: PHP 5B | PHP 1M per event | Same as property |
| Earthquake | Earthquake damage | Sublimit: PHP 3B | PHP 2M per event | Same as property |
| General Liability | Third-party bodily injury and property damage | PHP 50M per occurrence | PHP 100K | Leading PH insurer |
| Product Liability | Product defect claims | PHP 30M per occurrence | PHP 200K | Leading PH insurer |
| Employer's Liability | Work-related injury/illness | PHP 10M per employee | PHP 50K | Leading PH insurer |
| Group Personal Accident | Employee 24-hour accident coverage | 2x annual salary per employee | None | Leading PH insurer |
| Group Life Insurance | Employee life coverage | 2x annual salary per employee | None | Leading PH insurer |
| Motor Vehicle | Company-owned fleet (trucks, cars) | PHP 5M per vehicle | PHP 25K | Leading PH insurer |
| Cash in Transit | Cash movement and in-store cash | PHP 10M per event | None | Leading PH insurer |
| Cyber Insurance | Data breach, cyber extortion, business interruption | USD 5M per event | USD 100K | International insurer |
| Directors & Officers (D&O) | Claims against directors and officers | PHP 100M per claim | PHP 500K | International insurer |
| Professional Indemnity | Professional service errors | PHP 50M per claim | PHP 200K | International insurer |
| Marine Cargo | Imported goods in transit | PHP 500M annual aggregate | PHP 100K per shipment | Leading PH insurer |

### 11.4.2 Insurance Management

| Activity | Frequency | Owner | Oracle Fusion Touchpoint |
|----------|-----------|-------|------------------------|
| Policy renewal review | Annual | VP Finance / VP Facilities | Assets (asset register for insured values) |
| Claims processing | As needed | VP Finance | Payables (claim invoices), Cash Management |
| Insured value review | Annual | VP Finance + VP Facilities | Assets (updated asset values), Inventory (stock values) |
| Safety inspection (insurance requirement) | Quarterly | VP Facilities / Safety Officer | HCM Workforce Health & Safety |

---

## 11.5 Crisis Management

### 11.5.1 Crisis Classification

| Level | Definition | Examples | Response Team |
|-------|-----------|----------|---------------|
| Level 1 — Minor | Localized incident; single store/unit affected; no media attention | Store break-in, minor equipment failure, single employee injury | Store Manager + Regional Director |
| Level 2 — Moderate | Multi-store or significant operational impact; potential media attention | Warehouse fire, multi-store system outage, product recall, employee fatality | VP-level crisis team |
| Level 3 — Major | Company-wide impact; significant financial/reputational risk; media attention likely | Major typhoon damage, data breach, CEO/C-level incident, major fraud, regulatory enforcement | Executive crisis team + Board notification |
| Level 4 — Catastrophic | Existential threat to company; national media coverage | Multiple fatalities, massive data breach, company-threatening litigation, catastrophic natural disaster | Full crisis team + Board + external advisors |

### 11.5.2 Crisis Response Team

| Role | Responsibility | Contact Method |
|------|---------------|----------------|
| Crisis Director (CEO) | Overall crisis leadership; media spokesperson for Level 3-4 | Mobile + dedicated crisis line |
| Crisis Coordinator (VP Finance) | Coordinate response activities; manage crisis log | Mobile + dedicated crisis line |
| Operations Lead (COO) | Operational response; store/warehouse coordination | Mobile + satellite phone |
| Communications Lead (CMO) | Internal and external communications; media management | Mobile + dedicated crisis line |
| Legal Lead (CLO) | Legal advice; regulatory notifications; liability assessment | Mobile |
| IT Lead (CIO) | Technology response; cybersecurity incident management | Mobile |
| HR Lead (CHRO) | Employee welfare; family notifications; counseling | Mobile |
| Finance Lead (VP Treasury) | Emergency fund access; insurance claims initiation | Mobile |

### 11.5.3 Crisis Response Procedures

#### Typhoon / Natural Disaster

| Step | Action | Responsible |
|------|--------|-------------|
| 1 | Monitor PAGASA advisories; activate preparedness protocol 48 hours before expected impact | VP Facilities |
| 2 | Pre-position emergency supplies at stores/warehouses in affected areas | VP Distribution |
| 3 | Activate store/warehouse closure decision matrix (based on signal number and local conditions) | COO + Regional Directors |
| 4 | Employee safety check-in via Oracle ME mass notification | CHRO |
| 5 | Secure inventory (elevate stock, cover merchandise, protect POS terminals) | Store Managers |
| 6 | Post-event damage assessment within 24 hours | VP Facilities + Insurance |
| 7 | Claims filing within 72 hours | VP Finance |
| 8 | Store/warehouse reopening assessment | COO + VP Facilities |
| 9 | Customer communication via social media, e-commerce, SMS | CMO |
| 10 | Supply chain rerouting if warehouses affected | VP Supply Chain |

#### Data Breach / Cybersecurity Incident

| Step | Action | Responsible |
|------|--------|-------------|
| 1 | Incident detected (monitoring alert, employee report, third-party notification) | VP Infra & Security |
| 2 | Activate Incident Response Team; isolate affected systems | CIO + VP Infra & Security |
| 3 | Assess scope: affected systems, data types, number of records | VP Infra & Security |
| 4 | Contain breach: revoke access, patch vulnerability, block attack vector | VP Infra & Security |
| 5 | Notify DPO within 4 hours | CIO |
| 6 | NPC breach notification within 72 hours (if applicable per RA 10173) | DPO / CLO |
| 7 | Notify affected individuals within 5 business days (if PII involved) | DPO / CLO / CMO |
| 8 | Engage external forensic investigator (if Level 2+) | CIO + CLO |
| 9 | Insurance claim notification (if Level 2+) | VP Finance |
| 10 | Post-incident review and remediation within 14 days | CIO + VP Infra & Security |
| 11 | Board notification (if Level 3+) | CEO |

#### Product Recall

| Step | Action | Responsible |
|------|--------|-------------|
| 1 | Product safety concern identified (customer complaint, supplier notification, regulatory notice) | VP Merchandising |
| 2 | Assess severity and scope; consult with supplier and legal | VP Merchandising + CLO |
| 3 | Decision to recall (VP Merchandising + CLO + COO for Level 1; CEO for Level 2+) | Decision committee |
| 4 | DTI notification (if required) | CLO |
| 5 | Pull affected products from all stores; quarantine in Oracle Inventory | VP Store Ops + Inventory |
| 6 | Customer notification (in-store signage, social media, direct contact for B2B) | CMO |
| 7 | Process customer returns/refunds per recall policy (override standard return window) | VP Store Ops |
| 8 | Supplier claim for costs and damages | VP Procurement + CLO |
| 9 | Post-recall review and supplier quality action | VP Procurement |

---

## 11.6 Business Continuity Planning

### 11.6.1 Business Continuity Strategy

| Critical Business Function | Maximum Tolerable Downtime | Recovery Strategy | Recovery Time Objective |
|---------------------------|---------------------------|-------------------|------------------------|
| POS / Retail Sales | 1 hour | Offline mode (24 hours); failover to backup system | 1 hour (system); immediate (offline) |
| Oracle Fusion (ERP/SCM/HCM) | 4 hours | OCI built-in HA/DR; POS offline mode bridges gap | 4 hours |
| OIC Integration | 2 hours | POS offline mode; batch sync upon recovery | 2 hours |
| Warehouse Operations | 4 hours | Manual processes with paper backup; WMS offline mode | 4 hours |
| Payroll Processing | 24 hours | Backup processing capability; manual calculation if needed | 24 hours |
| Customer Service / Call Center | 2 hours | Cloud-based (CX Service); mobile backup | 2 hours |
| E-Commerce Platform | 4 hours | OCI-hosted; auto-scaling; CDN failover | 4 hours |
| Email / Communication | 4 hours | Cloud-based email; mobile communication backup | 4 hours |
| Treasury / Banking | 4 hours | Online banking portal; manual bank communication | 4 hours |
| Supply Chain Planning | 24 hours | Data cached locally; manual planning if extended outage | 24 hours |

### 11.6.2 Business Continuity Testing Schedule

| Test Type | Scope | Frequency | Owner |
|-----------|-------|-----------|-------|
| POS offline mode activation | 2-3 stores per region | Quarterly | VP Digital Products |
| Oracle Fusion DR failover | Full system | Semi-annually | VP Enterprise Apps |
| OIC integration failover | All integration flows | Semi-annually | VP Enterprise Apps |
| Warehouse manual operations | 1 warehouse | Annually | VP Distribution |
| Crisis communication drill | All employees | Semi-annually | CHRO + CMO |
| Typhoon preparedness drill | All stores in typhoon-prone areas | Annually (before typhoon season, May) | VP Facilities |
| Fire evacuation drill | All locations | Quarterly | VP Facilities |
| Data breach tabletop exercise | Crisis response team | Semi-annually | CIO + CLO |
| Full business continuity exercise | Cross-functional | Annually | VP Finance (crisis coordinator) |

### 11.6.3 Business Continuity Documentation

| Document | Owner | Review Frequency |
|----------|-------|-----------------|
| Business Continuity Plan (BCP) | VP Finance | Annually |
| Disaster Recovery Plan (DRP) — IT | CIO | Annually |
| Crisis Management Plan | CEO Office | Annually |
| Emergency Contact List | VP Finance | Quarterly |
| Insurance Portfolio Summary | VP Finance | Annually |
| Emergency Response Procedures (per location) | VP Facilities | Annually |
| Communication Templates (crisis) | CMO | Annually |

---

## 11.7 Internal Audit Plan

### 11.7.1 Annual Audit Plan

| Audit Area | Frequency | Scope | Audit Focus |
|------------|-----------|-------|-------------|
| Financial Controls | Annual | All entities | Revenue recognition, AP/AR controls, journal entries, close process |
| Procurement & Sourcing | Annual | Supply Chain | Competitive bidding compliance, supplier selection, contract compliance |
| Inventory Management | Annual | 4 warehouses + 20 sample stores | Inventory accuracy, cycle count controls, adjustment authority, shrinkage |
| Payroll & HR Compliance | Annual | All entities | Payroll accuracy, statutory compliance, leave management, overtime |
| IT General Controls | Annual | Oracle Fusion + POS | Access management, SoD, change management, backup/recovery |
| Cybersecurity | Annual | All systems | Penetration testing, vulnerability assessment, incident response |
| POS Controls | Annual | 20 sample stores | Cash handling, transaction processing, void/refund controls, Z-reading reconciliation |
| Supplier Management | Biennial | Top 50 suppliers | Supplier qualification, scorecard accuracy, conflict of interest |
| Capital Expenditure | Biennial | All entities | Approval compliance, project tracking, asset capitalization |
| Regulatory Compliance | Annual | All entities | BIR, SEC, DOLE, NPC compliance; permit currency |
| Fraud Risk Assessment | Biennial | All entities | Fraud risk identification, control gap analysis, investigation procedures |
| Oracle Fusion Configuration | Annual | All modules | Configuration review, role/access adequacy, process compliance |
| Intercompany Transactions | Annual | All entities | Pricing compliance, elimination accuracy, documentation |
| Customer Loyalty Program | Biennial | CX | Points accuracy, tier progression, fraud detection, revenue recognition |

### 11.7.2 Audit Reporting

| Deliverable | Audience | Frequency |
|-------------|----------|-----------|
| Audit report (per engagement) | BAC + Process owner | Per audit completion |
| Quarterly audit summary | BAC + Board | Quarterly |
| Annual audit plan | BAC + Board | Annual (January) |
| Management action tracking | Process owners | Monthly |
| Follow-up audit report | BAC + Process owner | 60 days post-audit |

---

## 11.8 Oracle Fusion Risk & Compliance Module Usage

### 11.8.1 Advanced Controls Configuration

| Feature | Configuration | Purpose |
|---------|--------------|---------|
| Segregation of Duties (SoD) | 150+ SoD rules covering finance, procurement, inventory, HR | Prevent conflicting access |
| Access Certification | Quarterly campaigns for all departments | Validate user access appropriateness |
| Continuous Monitoring | Real-time alerts for high-risk transaction patterns | Detect fraud indicators |
| Transaction Controls | Rules for AP, AR, expenses, journal entries | Prevent unauthorized transactions |
| Configuration Controls | Tracking all system configuration changes | Audit system changes |
| Incident Management | Automated incident recording and resolution tracking | Manage compliance incidents |

### 11.8.2 Key SoD Rules

| Conflict | Role 1 | Role 2 | Risk |
|----------|--------|--------|------|
| Create and approve PO | ORA_PO_BUYER | ORA_PO_BUYER_APPROVER | Fictitious vendor purchases |
| Create vendor and pay vendor | ORA_SUPPLIER_MANAGER | ORA_AP_PAYMENT_SPECIALIST | Fictitious vendor payments |
| Record and approve journal entries | ORA_GL_JOURNAL_ENTRY | ORA_GL_SUPERVISOR | Financial statement manipulation |
| Create and approve expense reports | ORA_EXPENSE_EMPLOYEE | ORA_EXPENSE_APPROVER | Fictitious expense claims |
| Receive goods and approve invoice | ORA_INVENTORY_RECEIVER | ORA_AP_INVOICE_SPECIALIST | Fictitious receipt/invoice |
| Manage employees and process payroll | ORA_HCM_HR_SPECIALIST | ORA_HCM_PAYROLL_MANAGER | Ghost employee creation |
| Create customer and apply receipt | ORA_AR_CUSTOMER_MANAGER | ORA_AR_RECEIPT_SPECIALIST | Fictitious customer credits |
| Adjust inventory and approve adjustment | ORA_INVENTORY_ADJ_USER | ORA_INVENTORY_ADJ_APPROVER | Inventory theft concealment |
