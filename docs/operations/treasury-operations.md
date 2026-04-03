# 19 — TREASURY & CASH MANAGEMENT OPERATIONS

## 19.1 Treasury Overview

### 19.1.1 Purpose

This document establishes the standard operating procedures for treasury and cash management operations across all Tahanan Depot entities. It covers daily cash positioning, bank account management, cash forecasting, payment processing, foreign exchange management, investment of surplus funds, debt management, bank relationship management, and treasury controls.

### 19.1.2 Scope

- All 5 legal entities (Holdings, Retail, Supply Chain, Property, Digital)
- 120+ store collection bank accounts
- 4 warehouse operating accounts
- Corporate disbursement accounts
- All payment channels (PESONet, InstaPay, check, cash)

- Foreign exchange exposure from imported goods

### 19.1.3 Treasury Organization

```
VP TREASURY (reports to CFO)
├── Treasury Manager
│   ├── Cash Management Analysts (2)
│   ├── Bank Reconciliation Specialists (2)
│   └── Treasury Associate (1)
├── FX and Investment Analyst
└── Treasury Analyst (1)
```

### 19.1.4 Oracle Fusion Roles

| Role | Oracle Fusion Security Roles |
|------|----------------------------|
| VP Treasury | ORA_CASH_MANAGEMENT_EXECUTIVE, ORA_GL_EXECUTIVE |
| Treasury Manager | ORA_CASH_MANAGEMENT_MANAGER, ORA_AR_MANAGER |
| Cash Management Analyst | ORA_CASH_MANAGEMENT_ANALYST, ORA_AR_SPECIALIST |
| Bank Reconciliation Specialist | ORA_CASH_MANAGEMENT_SPECIALIST, ORA_GL_ANALYST |
| FX and Investment Analyst | ORA_CASH_MANAGEMENT_ANALYST, ORA_GL_ANALYST |
| Treasury Analyst | ORA_CASH_MANAGEMENT_SPECIALIST, ORA_AP_SPECIALIST |

---

## 19.2 Daily Cash Management

### 19.2.1 Morning Cash Position Process

| Step | Timing | Activity | System | Oracle Module |
|------|--------|----------|--------|---------------|
| 1 | 7:00 AM | Import previous day bank statements (auto-feed from 5 major banks) | Cash Management | Cash Management |
| 2 | 7:30 AM | Compile store deposit reports from all 120 stores (POS Z-readings uploaded per POL-FIN-003) | Cash Management | Cash Management |
| 3 | 8:00 AM | Calculate opening cash position by entity and bank account | Cash Management | Cash Management |
| 4 | 8:30 AM | Review cash position dashboard; identify surplus or deficit by entity | Cash Management | Cash Management |
| 5 | 9:00 AM | Execute intercompany fund transfers if any entity has deficit (per POL-FIN-006 pricing) | Cash Management + GL | Cash Management + GL |
| 6 | 9:30 AM | Confirm all intercompany transfers posted and reconciled | Cash Management + GL | Cash Management + GL |
| 7 | 10:00 AM | Distribute morning cash position report to CFO and VP Finance | Cash Management | Cash Management (reporting) |

### 19.2.2 Cash Position Report Format
| Section | Content |
|---------|---------|
| Opening balance (previous day close) | Total PHP across all banks |
| + Store deposits (yesterday) | Total deposits by entity |
| + Customer payments received (B2B) | Collections per PROC-FIN-004 |
| + Intercompany receipts | IC transfers received |
| - Supplier payments (yesterday) | AP payment batch per SOP-FIN-003 |
| - Payroll disbursements | Semi-monthly payroll per SOP-HR-002 |
| - Operating disbursements | Utilities, rent, other |
| - Intercompany payments | IC transfers sent |
| - FX settlements | Forward contract settlements (if any) |
| = Projected closing balance | Total PHP across all banks |
| - Minimum cash reserve requirement | Per entity threshold |
| = Available surplus for investment | Excess above reserve |

### 19.2.3 Store Deposit Monitoring

| Metric | Target | Alert Threshold | Action |
|--------|--------|-----------------|--------|
| Store deposit posted same day | > 95% of stores | < 90% | LP Coordinator contacts store; VP Finance notified |
| Deposit amount vs. Z-reading variance | < PHP 100 per store | > PHP 500 | Investigation by Store Finance Analyst |
| Unbanked deposits (no bank statement match) | < 5 per day | > 10 per day | Treasury Analyst investigates |
| Armored car pickup compliance | 100% for stores > PHP 500K daily | Any miss | LP Coordinator + Treasury Manager notified |

---

## 19.3 Bank Account Management

### 19.3.1 Bank Account Structure

| Account Type | Purpose | Bank | Count | Signatories |
|-------------|---------|------|-------|-------------|
| Concentration Account (Main) | Central fund pooling | BDO | 1 | VP Treasury + CFO (dual) |
| Concentration Account (Secondary) | Central fund pooling | BPI | 1 | VP Treasury + CFO (dual) |
| Store Collection Account | Daily store deposits | BDO, BPI, Metrobank | 120 (one per store) | Store Manager + Asst. Manager |
| Disbursement Account (AP) | Supplier payments | BDO, BPI | 2 | VP Treasury or Treasury Manager + AP Manager |
| Payroll Account | Salary disbursements | BDO, BPI, Metrobank, PNB, Security Bank | 5 (one per bank) | Payroll Manager + VP Finance |
| Petty Cash Account | Small expenses | BDO | 5 (regional) | Regional Director + controller |
| FX Settlement Account | Foreign exchange settlements | BDO | 1 | VP Treasury + CFO |
| Investment Account | Surplus fund investment | BDO, BPI | 2 | VP Treasury + CFO |
| Escrow Account | Vendor deposits and guarantees | BDO | 1 | VP Treasury + CLO |
| Credit Facility Account | Revolving credit line | BDO, BPI, Metrobank | 3 | VP Treasury + CFO |

### 19.3.2 Bank Account Opening/Closing Procedure
| Step | Activity | Approval | Timeline |
|------|----------|----------|----------|
| 1 | Treasury identifies need for new account or account closure | Treasury Manager | — |
| 2 | Business case prepared (purpose, expected activity, signatories) | VP Treasury | 1 business day |
| 3 | Bank package prepared (documents, board resolution, specimen signatures) | VP Treasury | 1 business day |
| 4 | Bank application submitted | Treasury Associate | — |
| 5 | Bank processes application | Bank | 5-10 business days |
| 6 | Account confirmed in Oracle Cash Management | Cash Management Analyst | Same day |
| 7 | Signatory cards issued and distributed | Treasury Associate | Same day |
| 8 | Bank Mandate/amendment filed with BSP (if required) | Treasury Manager | Per BSP schedule |

### 19.3.3 Authorized Signatories
| Account Type | Primary Signatory | Secondary Signatory | Threshold |
|-------------|-------------------|--------------------|-----------|
| Concentration accounts | VP Treasury | CFO | All amounts |
| Store collection accounts | Store Manager | Asst. Store Manager | Up to PHP 500K per deposit |
| Disbursement accounts | Treasury Manager | AP Manager | Per approval matrix |
| Payroll accounts | Payroll Manager | VP Finance | All amounts |
| FX accounts | VP Treasury | CFO | All amounts |
| Investment accounts | VP Treasury | CFO | All amounts |
| Petty cash | Regional Director | Controller | Up to PHP 50K |

---

## 19.4 Cash Concentration and Pooling

### 19.4.1 Zero-Balance Sweeping Schedule
| Sweep Type | Frequency | Source Accounts | Target Account | Threshold |
|-----------|-----------|-----------------|----------------|-----------|
| Store deposit sweep | Daily (overnight) | 120 store collection accounts | Concentration account (BDO) | All balances > PHP 0 |
| Regional concentration sweep | Daily (overnight) | BPI, Metrobank store accounts | BDO concentration account | All balances > PHP 0 |
| Payroll funding sweep | Semi-monthly (T-1 before payday) | Concentration account | Payroll accounts (per bank) | Exact payroll amount |
| AP funding sweep | Per payment batch | Concentration account | Disbursement accounts | Exact payment batch amount |
| Surplus investment sweep | Weekly (Friday) | Concentration account | Investment accounts | Balances > PHP 100M threshold |

### 19.4.2 Funding Requirements Process
| Funding Need | Trigger | Approval | Process |
|-------------|---------|----------|---------|
| Payroll funding | Semi-monthly (10th and 25th cutoff) | Payroll Manager | Auto-sweep from concentration to payroll accounts |
| AP payment run | Per payment schedule (SOP-FIN-003) | AP Manager | Auto-sweep from concentration to disbursement accounts |
| Store change order funding | Per approved capex | VP Finance (per POL-FIN-007) | Manual transfer from concentration to store account |
| FX settlement | Per forward contract maturity | VP Treasury | Manual transfer from concentration to FX account |
| Intercompany funding | Entity deficit identified (daily cash position) | VP Treasury | Intercompany transfer per POL-FIN-006 |
| Emergency funding | Unplanned cash need > PHP 10M | CFO | Wire transfer or credit facility drawdown |

---

## 19.5 Cash Forecasting

### 19.5.1 Forecasting Framework

| Forecast Type | Horizon | Frequency | Method | Owner |
|--------------|---------|-----------|--------|-------|
| Daily cash forecast | 5 business days | Daily (by 10 AM) | Receipts and disbursements matching | Cash Management Analyst |
| Weekly cash forecast | 4 weeks | Weekly (Monday) | Historical trends + known flows | Treasury Manager |
| 13-week rolling forecast | 13 weeks | Weekly (updated Friday) | AI-powered forecast in Oracle Cash Management | VP Treasury |
| Annual cash budget | 12 months | Annual (part of EPM Planning) | Bottom-up by entity + top-down targets | VP Treasury + VP FP&A |

### 19.5.2 13-Week Rolling Forecast Components

| Component | Source | Frequency | Oracle Module |
|-----------|--------|-----------|---------------|
| Store sales receipts (cash, card, e-wallet) | POS daily sales + payment mix | Daily | Cash Management + POS Analytics |
| B2B collections | AR aging + expected payments | Weekly | Receivables + Cash Management |
| AP disbursements | Payment schedule + due dates | Weekly | Payables + Cash Management |
| Payroll disbursements | Semi-monthly payroll schedule | Semi-monthly | Payroll + Cash Management |
| Capex outflows | Approved capex projects | Monthly | Projects + Cash Management |
| Tax payments | BIR tax calendar (Doc 11 compliance calendar) | Monthly | Tax Reporting + Cash Management |
| Statutory remittances | SSS, PhilHealth, Pag-IBIG schedule | Monthly | Payroll + Cash Management |
| Intercompany flows | Transfer pricing schedule | Monthly | Cash Management + GL |
| FX settlements | Forward contract maturities | Per maturity | Cash Management |
| Rent payments | Lease payment schedule | Monthly | Payables + Cash Management |
| Dividend payments | Board-approved dividends | Per approval | GL + Cash Management |
| Loan repayments | Debt maturity schedule | Per schedule | Cash Management |

### 19.5.3 Forecast Accuracy Targets
| Metric | Target | Measurement |
|--------|--------|-------------|
| Daily forecast variance (1-week horizon) | < 5% | Actual vs. forecast daily cash position |
| Weekly forecast variance (4-week horizon) | < 10% | Actual vs. forecast weekly net cash flow |
| 13-week forecast variance | < 15% | Actual vs. forecast monthly net cash flow |
| Directional accuracy (surplus vs. deficit) | > 95% | Correct prediction of net cash flow direction |

---

## 19.6 Payment Processing

### 19.6.1 Payment Methods and Routing

| Payment Type | Method | Bank Channel | Processing Time | Max Amount |
|-------------|--------|-------------|-----------------|------------|
| Supplier payments (< PHP 500K) | PESONet batch | BDO, BPI | Same day (if before cutoff) | PHP 500,000 |
| Supplier payments (> PHP 500K) | PESONet batch | BDO, BPI | Same day (if before cutoff) | No limit |
| Supplier payments (urgent) | InstaPay | BDO, BPI | Real-time | PHP 500,000 |
| Payroll | PESONet batch | All 5 banks | Same day (if before cutoff) | No limit |
| Employee reimbursements | InstaPay | BDO, BPI | Real-time | PHP 50,000 |
| Intercompany transfers | Internal journal | Oracle Fusion | Real-time | No limit |
| Tax payments | PESONet / bank Over-the-Counter | BDO | Per BIR deadline | Per assessment |
| Statutory remittances | PESONet / employer portal | Per agency | Per deadline | Per assessment |
| Foreign currency payments | SWIFT wire transfer | BDO (FX account) | 1-2 business days | Per FX contract |
| Dividend payments | PESONet batch | BDO | Per schedule | Per board approval |

### 19.6.2 Payment Batch Processing Schedule
| Batch | Day | Cutoff Time | Payment Date | Scope |
|-------|-----|-------------|-------------|-------|
| Weekly AP Run 1 | Monday | 10:00 AM | Tuesday | Standard supplier payments (Net 30/45) |
| Weekly AP Run 2 | Wednesday | 10:00 AM | Thursday | Standard supplier payments |
| Bi-weekly AP Run | 15th and 30th | 10:00 AM | Next business day | Time-sensitive payments |
| Payroll Run 1 | 14th | 10:00 AM | 15th | First half payroll |
| Payroll Run 2 | 29th | 10:00 AM | 30th | Second half payroll |
| Tax Payments | Per BIR calendar | 10:00 AM | Due date | Monthly/quarterly taxes |
| Statutory Payments | 10th of month | 10:00 AM | Due date | SSS, PhilHealth, Pag-IBIG |
| Urgent Payments | As needed | Immediate | Same day | Emergency purchases, critical vendor payments |

### 19.6.3 Payment Approval Workflow
| Amount Range (PHP) | Approver Level | Oracle Workflow |
|---------------------|---------------|-----------------|
| 0 — 500,000 | Treasury Manager | Auto-route |
| 500,001 — 5,000,000 | VP Treasury | Auto-route |
| 5,000,001 — 20,000,000 | CFO | Auto-route |
| > 20,000,000 | CEO + CFO | Manual approval |

| Payment Type | Additional Approval |
|-------------|-------------------|
| Foreign currency payments | VP Treasury (all amounts) |
| Loan repayments | CFO |
| Dividend payments | CEO + CFO |
| Intercompany payments (non-routine) | VP Finance |
| Tax payments | VP Tax |

---

## 19.7 Receivables Management

### 19.7.1 Cash Application Process
| Step | Activity | System | Oracle Module | SLA |
|------|----------|--------|---------------|-----|
| 1 | Bank statement imported daily | Cash Management | Cash Management | 7:00 AM daily |
| 2 | Auto-matching: bank receipt to AR invoice | Cash Management | Cash Management + Receivables | < 1 hour |
| 3 | Auto-matching: store deposit to POS Z-reading | Cash Management | Cash Management | < 1 hour |
| 4 | Review unmatched receipts | Treasury Analyst | Cash Management | Same day |
| 5 | Manual application of unmatched receipts | Treasury Analyst | Receivables | < 2 business days |
| 6 | Investigate unapplied cash > 30 days | Treasury Manager | Receivables | Weekly review |
| 7 | Write off unapplied cash > 90 days (with approval) | VP Finance | Receivables + GL | Per approval |

### 19.7.2 B2B Collections Process
| Step | Activity | System | Oracle Module |
|------|----------|--------|---------------|
| 1 | Weekly AR aging review | AR Aging Report | Receivables |
| 2 | Identify overdue accounts per POL-FIN-004 collections process | Collections | Receivables + Collections |
| 3 | Auto-dunning emails sent per aging bucket | Collections | Collections |
| 4 | Collections specialist follows up on 31+ day overdue | Collections | Collections |
| 5 | Collections manager escalates 61+ day overdue to VP Finance | Collections | Collections |
| 6 | AR Manager initiates legal demand for 90+ day overdue | Receivables | Receivables + Legal |
| 7 | Bad debt provision calculated monthly | GL | Receivables + GL |
| 8 | Write-off approval per CFO for > 180 days | Receivables | Receivables + GL |

### 19.7.3 Store Deposit Reconciliation
| Reconciliation Step | Frequency | System | SLA |
|---------------------|-----------|--------|-----|
| POS Z-reading vs. AR receipt match | Daily | Cash Management | < 1 day |
| Bank deposit vs. POS Z-reading match | Daily | Cash Management | < 1 day |
| Unmatched deposit investigation | Daily | Cash Management | < 2 business days |
| Card settlement vs. POS card total | Daily | Cash Management | < 1 day |
| E-wallet settlement vs. POS e-wallet total | Daily | Cash Management | < 1 day |
| Cash variance trending analysis | Weekly | Cash Management Analytics | Weekly review |

---

## 19.8 Foreign Exchange Management

### 19.8.1 FX Exposure Profile
| Exposure Type | Estimated Annual Volume | Primary Currencies | Hedging Strategy |
|--------------|----------------------|-------------------|-----------------|
| Import payments | ~USD 30M (PHP 1.7B) | USD, CNY | Forward contracts for 50-70% of exposure |
| Equipment purchases (foreign) | ~USD 5M (PHP 280M) | USD, JPY, EUR | Forward contracts for 100% of committed exposure |
| Oracle subscription (USD) | ~USD 2M (PHP 112M) | USD | Natural hedge (PHP revenue) |
| Software licenses | ~USD 500K (PHP 28M) | USD | Spot purchase |

### 19.8.2 FX Hedging Policy
| Parameter | Policy |
|-----------|--------|
| Minimum exposure to hedge | USD 100,000 per transaction |
| Hedging instrument | Forward contracts only (no options, no swaps) |
| Hedging horizon | Up to 12 months forward |
| Hedge ratio target | 50-70% of projected exposure (imports); 100% of committed capital expenditure |
| Counterparty limit | Maximum 20% of total hedging with any single bank |
| Hedge documentation | Trade confirmation, FX deal ticket, proof of underlying exposure |
| Mark-to-market review | Monthly; reported to CFO |
| Gain/loss recognition | PFRS-compliant; hedging gains/losses in P&L (no hedge accounting) |

### 19.8.3 FX Transaction Process
| Step | Activity | Approval | Oracle Module |
|------|----------|----------|---------------|
| 1 | Import specialist identifies upcoming FX requirement (from confirmed POs) | — | Purchasing + Cash Management |
| 2 | Treasury reviews FX exposure report and determines hedging need | VP Treasury | Cash Management |
| 3 | Forward contract obtained from bank (minimum 3 quotes) | VP Treasury (< USD 500K), CFO (> USD 500K) | Cash Management |
| 4 | Forward contract confirmed and booked in Oracle | VP Treasury | Cash Management + GL |
| 5 | Mark-to-market adjustment posted monthly | Treasury Manager | GL |
| 6 | Settlement at maturity | VP Treasury | Cash Management + GL |

---

## 19.9 Investment of Surplus Funds

### 19.9.1 Investment Policy

| Parameter | Policy |
|-----------|--------|
| Investment objective | Capital preservation; liquidity; yield enhancement |
| Minimum surplus for investment | PHP 100,000,000 (balances above this in concentration account swept to investment account) |
| Approved instruments | Philippine Treasury Bills (T-bills), BSP Special Deposit Accounts, Bank Time Deposits (maximum 90 days), Money Market Funds (BAP, BDO, Metrobank) |
| Prohibited instruments | Equities, corporate bonds, derivatives. real estate. cryptocurrency |
| Maximum single bank deposit | 25% of total investment portfolio |
| Maximum single instrument exposure | 40% of total investment portfolio |
| Maturity limits | Minimum 7 days; maximum 180 days |
| Investment authority | VP Treasury (up to PHP 200M per placement), CFO (PHP 200M-500M), CEO + CFO (> PHP 500M) |
| Performance benchmark | 91-day T-bill rate (benchmark yield must exceed overnight rate by at least 50 bps) |

### 19.9.2 Investment Decision Process
| Step | Activity | Approval | SLA |
|------|----------|----------|-----|
| 1 | Friday: Review concentration account balances; identify investable surplus | Treasury Manager | Weekly |
| 2 | Friday: Analyze interest rate outlook and instrument availability | FX and Investment Analyst | Weekly |
| 3 | Friday: Recommend investment placements (amount, instrument, bank, maturity) | VP Treasury | Same day |
| 4 | Friday: Execute approved placements via bank portal | Treasury Associate | Same day |
| 5 | Friday: Record investment in Oracle Cash Management | Cash Management Analyst | Same day |
| 6 | Monday: Confirm placement and update investment tracker | Treasury Associate | Next business day |
| 7 | Ongoing: Monitor maturity dates; initiate rollover or return to concentration account | FX and Investment Analyst | Continuous |

### 19.9.3 Investment Portfolio Reporting
| Report | Frequency | Audience | Content |
|--------|-----------|----------|---------|
| Investment portfolio summary | Weekly | VP Treasury | Current holdings, yields, maturities |
| Investment income report | Monthly | CFO | Interest income, yield vs. benchmark |
| Investment performance review | Quarterly | CFO + CEO | Portfolio returns, strategy effectiveness |
| Counterparty exposure report | Monthly | VP Treasury | Concentration by bank and instrument |

---

## 19.10 Debt Management

### 19.10.1 Credit Facilities
| Facility | Type | Bank | Limit (PHP) | Interest Rate | Purpose |
|----------|------|------|------------|--------------|---------|
| Revolving Credit Line 1 | Uncommitted | BDO | 2,000,000,000 | PHLREF + 150 bps | Working capital (inventory, operations) |
| Revolving Credit Line 2 | Uncommitted | BPI | 1,500,000,000 | PHLREF + 175 bps | Working capital backup |
| Term Loan 1 | Term (5 years) | BDO | 3,000,000,000 | Fixed 6.5% | Store expansion capex |
| Term Loan 2 | Term (3 years) | Metrobank | 1,000,000,000 | Fixed 6.25% | Warehouse expansion |
| LC Facility | Standby LC | BDO | 500,000,000 | PHLREF + 100 bps | Import letters of credit |

### 19.10.2 Loan Covenant Compliance
| Covenant | Requirement | Monitoring | Reporting |
|----------|-------------|-----------|-----------|
| Debt-to-Equity ratio | < 2.0x | Monthly (auto-calculated in Oracle) | Quarterly to banks |
| Current ratio | > 1.5x | Monthly | Quarterly to banks |
| Interest coverage ratio | > 3.0x | Quarterly | Quarterly to banks |
| Capital expenditure limit | Per annual budget approved by Board | Monthly | Quarterly to banks |
| Negative pledge | No asset pledges without bank consent | Ongoing | Annual to banks |
| Financial statement submission | Audited FS within 120 days of fiscal year end | Annual | Annual to banks |

### 19.10.3 Debt Maturity Schedule
| Year | Principal Repayment | Interest (Est.) | Total Debt Service | Facility |
|------|--------------------|----------------|-------------------|----------|
| 2026 | PHP 800M | PHP 420M | PHP 1,220M | Term Loan 1 + 2 |
| 2027 | PHP 1,200M | PHP 380M | PHP 1,580M | Term Loan 1 + 2 |
| 2028 | PHP 1,500M | PHP 310M | PHP 1,810M | Term Loan 1 + 2 |
| 2029 | PHP 1,000M | PHP 250M | PHP 1,250M | Term Loan 1 |
| 2030 | PHP 1,000M | PHP 190M | PHP 1,190M | Term Loan 1 (final year) |

---

## 19.11 Bank Relationship Management

### 19.11.1 Bank Scorecard
| Criteria | Weight | Scoring (1-5) | Review Frequency |
|----------|--------|---------------|-----------------|
| Service quality (transaction processing, responsiveness) | 25% | Quarterly survey by Treasury team | Quarterly |
| Fee competitiveness (versus market rates) | 20% | Annual fee benchmarking | Annually |
| Technology (digital banking, API integration, reporting) | 20% | IT + Treasury assessment | Annually |
| Branch network (coverage for store deposits) | 15% | Store feedback survey | Annually |
| Credit facility terms (interest rates, covenants, flexibility) | 20% | Negotiation outcome review | Annually |

### 19.11.2 Bank Fee Management
| Fee Type | Bank | Annual Estimate | Negotiation Frequency |
|----------|------|-----------------|---------------------|
| Account maintenance fees | All 5 banks | PHP 2.4M | Annual |
| Transaction fees (PESONet, InstaPay) | All 5 banks | PHP 8.5M | Annual |
| Cash management platform fee | BDO, BPI | PHP 3.6M | Annual |
| LC issuance fees | BDO | PHP 1.8M | Per transaction |
| FX deal fees | BDO, BPI | PHP 1.2M | Per transaction |
| Lockbox / deposit processing | BDO, BPI | PHP 2.0M | Annual |
| **Total bank fees** | | **PHP 19.5M** | |

### 19.11.3 Bank Relationship Review
| Activity | Frequency | Owner | Deliverable |
|----------|-----------|-------|-------------|
| Quarterly business review meeting | Quarterly | VP Treasury + Bank Relationship Manager | Meeting minutes; action items |
| Annual strategy review | Annually | CFO + VP Treasury | Bank strategy plan; fee renegotiation targets |
| Service level monitoring | Monthly | Treasury Manager | SLA scorecard |
| Fee benchmarking | Annually | Treasury Analyst | Fee comparison report |
| Credit facility review | Annually | CFO + VP Treasury | Facility renewal/renegotiation decision |

---

## 19.12 Treasury Controls and Compliance

### 19.12.1 Segregation of Duties
| Function | Create | Approve | Execute | Reconcile |
|----------|--------|---------|---------|-----------|
| Payment batch | AP Specialist | Treasury Manager | Treasury Associate (bank file) | Bank Reconciliation Specialist |
| Intercompany transfer | Treasury Analyst | VP Treasury | Treasury Associate | Cash Management Analyst |
| FX deal | Treasury Analyst | VP Treasury / CFO | Treasury Associate | FX and Investment Analyst |
| Investment placement | FX and Investment Analyst | VP Treasury / CFO | Treasury Associate | Treasury Manager |
| Bank account opening | Treasury Associate | VP Treasury | Bank (external) | Cash Management Analyst |

### 19.12.2 Dual Authorization Matrix
| Activity | Threshold | Authorization Required |
|----------|-----------|----------------------|
| Payment release | Any amount | Treasury Manager approval in Oracle + Bank file authorized by Treasury Associate |
| Payment release > PHP 5M | > PHP 5,000,000 | VP Treasury approval in Oracle + Treasury Manager bank release |
| Payment release > PHP 20M | > PHP 20,000,000 | CFO approval in Oracle + VP Treasury bank release |
| Bank account signatory change | Any | VP Treasury + CFO approval |
| New bank account opening | Any | VP Treasury + CFO approval |
| FX deal execution | Any amount | VP Treasury approval + Treasury Associate execution |
| Investment placement | Any amount | VP Treasury approval + Treasury Associate execution |

### 19.12.3 Bank Reconciliation Controls
| Control | Frequency | Owner | Threshold |
|---------|-----------|-------|-----------|
| Bank statement auto-import | Daily (7:00 AM) | System | All accounts |
| Auto-matching of bank transactions | Daily | Cash Management | All matched items |
| Manual matching review | Daily | Bank Reconciliation Specialist | Unmatched items |
| Unmatched item aging review | Weekly | Treasury Manager | Items > 7 days |
| Unmatched item escalation | Monthly | VP Finance | Items > 30 days |
| GL-to-bank reconciliation confirmation | Daily | Cash Management Analyst | All accounts |
| Bank reconciliation sign-off | Daily | Treasury Manager | All accounts |

### 19.12.4 Anti-Money Laundering (AML) Compliance
| Requirement | Policy | Oracle Fusion Touchpoint |
|-------------|--------|------------------------|
| Customer Due Diligence (CDD) | Per RA 9160 (AML Act) for B2B customers | Customer master in Receivables |
| Enhanced Due Diligence (EDD) | For high-risk customers (PEP, complex structures) | Customer master in Receivables |
| Covered transaction reporting | Cash transactions > PHP 500K in a single day | Cash Management monitoring |
| Suspicious transaction reporting | Per AMLC guidelines | Cash Management alerts + manual review |
| Record retention | 5 years from transaction date | Per data retention schedule (Doc 12) |
| AML training | Annual for all treasury and finance staff | Oracle Learning |

### 19.12.5 Treasury Audit Trail
| Activity | Logged In | Retention | Reviewable By |
|----------|-----------|-----------|---------------|
| Payment creation and approval | Oracle Payables / Cash Management | 10 years | Internal Audit, VP Finance |
| Bank file generation and transmission | Oracle Cash Management | 10 years | Treasury Manager, Internal Audit |
| Intercompany transfer | Oracle Cash Management + GL | 10 years | VP Finance, Internal Audit |
| FX deal execution | Oracle Cash Management + bank portal | 10 years | VP Treasury, Internal Audit |
| Investment placement | Oracle Cash Management + bank portal | 10 years | CFO, Internal Audit |
| Bank reconciliation | Oracle Cash Management | 10 years | Treasury Manager, Internal Audit |
| Bank account changes | Oracle Cash Management + bank records | 10 years | VP Treasury, Internal Audit |

---

## 19.13 Treasury Performance Metrics

### 19.13.1 Key Performance Indicators

| KPI | Target | Measurement | Frequency | Owner |
|-----|--------|-------------|-----------|-------|
| Days Sales Outstanding (B2B) | < 45 days | (AR Balance / Revenue) × 365 | Monthly | AR Manager |
| Days Payable Outstanding | 35-45 days | (AP Balance / COGS) × 365 | Monthly | AP Manager |
| Cash Conversion Cycle | < 30 days | DSO + DIO - DPO | Monthly | VP Treasury |
| Cash forecast accuracy (weekly) | > 90% | 1 - (|Actual - Forecast| / Forecast) | Weekly | Treasury Manager |
| Cash forecast accuracy (13-week) | > 85% | Same | Monthly | VP Treasury |
| Idle cash (average daily) | < PHP 50M | Average uninvested surplus above reserve | Daily | Treasury Manager |
| Bank fee as % of revenue | < 0.05% | Total bank fees / total revenue | Monthly | Treasury Analyst |
| FX hedging effectiveness | > 80% | Reduction in FX variance vs. unhedged position | Quarterly | FX and Investment Analyst |
| Investment yield vs. benchmark | > Benchmark + 50 bps | Portfolio yield vs. 91-day T-bill rate | Quarterly | FX and Investment Analyst |
| Payment processing accuracy | > 99.9% | Correct payments / total payments | Monthly | Treasury Manager |
| Bank reconciliation timeliness | 100% same-day | Reconciliations completed by 5 PM / total accounts | Daily | Cash Management Analyst |
| Unapplied cash > 30 days | < PHP 5M | Total unapplied receipts > 30 days aging | Monthly | Treasury Manager |

### 19.13.2 Treasury Dashboard
| Widget | Visualization | Audience | Frequency |
|--------|--------------|----------|-----------|
| Consolidated cash position | Gauge + trend | CFO, VP Treasury | Real-time |
| Cash forecast vs. actual | Line chart | VP Treasury, Treasury Manager | Daily |
| AR aging distribution | Stacked bar chart | VP Treasury, AR Manager | Weekly |
| AP payment schedule | Gantt / timeline | Treasury Manager, AP Manager | Weekly |
| FX exposure and hedging | Pie chart (hedged vs. unhedged) | VP Treasury, CFO | Weekly |
| Investment portfolio | Table + yield metrics | VP Treasury | Weekly |
| Bank fee trend | Line chart | Treasury Manager | Monthly |
| Cash conversion cycle trend | Line chart | CFO | Monthly |
| Store deposit compliance heat map | Geographic heat map | VP Finance, VP Store Ops | Daily |
| Debt maturity profile | Timeline / bar chart | CFO, VP Treasury | Monthly |
