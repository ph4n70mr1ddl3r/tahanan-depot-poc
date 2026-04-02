# 09 — ORACLE FUSION DATA MODEL & CONFIGURATION

## 9.1 Oracle Fusion Setup Summary

This section documents the Oracle Fusion Cloud configuration for Tahanan Depot.

---

## 9.2 Enterprise Structure Configuration

### 9.2.1 Enterprise

| Setting | Value |
|---------|-------|
| Enterprise Name | Tahanan Holdings, Inc. |
| Enterprise ID | TAHA-HLDG |
| Calendar | January - December (52-53 week fiscal year option) |
| Base Currency | PHP |
| Reporting Currency | PHP (USD for IFRS consolidation if needed) |
| Localized | Yes — Philippines |

### 9.2.2 Primary Ledgers

| Ledger Name | Legal Entity | Currency | Chart of Accounts | Calendar | Accounting Method |
|-------------|-------------|----------|-------------------|----------|-------------------|
| TH-Primary | Tahanan Holdings | PHP | TD-CoA | Jan-Dec | Philippine Standard (PFRS) |
| TR-Primary | Tahanan Retail | PHP | TD-CoA | Jan-Dec | Philippine Standard (PFRS) |
| TSC-Primary | Tahanan Supply Chain | PHP | TD-CoA | Jan-Dec | Philippine Standard (PFRS) |
| TP-Primary | Tahanan Property | PHP | TD-CoA | Jan-Dec | Philippine Standard (PFRS) |
| TD-Primary | Tahanan Digital | PHP | TD-CoA | Jan-Dec | Philippine Standard (PFRS) |

### 9.2.3 Reporting Currency Ledger

| Ledger Name | Source Ledger | Currency | Purpose |
|-------------|-------------|----------|---------|
| Consolidated-USD | All primary ledgers | USD | Foreign investor reporting |

### 9.2.4 Business Units (Complete List)

| Business Unit | Legal Entity | BU Type |
|---------------|-------------|---------|
| BU-Holdings-Corporate | Tahanan Holdings | Corporate |
| BU-Retail-NorthLuzon | Tahanan Retail | Revenue Center |
| BU-Retail-SouthLuzon | Tahanan Retail | Revenue Center |
| BU-Retail-Visayas | Tahanan Retail | Revenue Center |
| BU-Retail-Mindanao | Tahanan Retail | Revenue Center |
| BU-Retail-Merchandising | Tahanan Retail | Cost Center |
| BU-SCM-Procurement | Tahanan Supply Chain | Procurement |
| BU-SCM-WH-NorthLuzon | Tahanan Supply Chain | Cost Center |
| BU-SCM-WH-SouthLuzon | Tahanan Supply Chain | Cost Center |
| BU-SCM-WH-Visayas | Tahanan Supply Chain | Cost Center |
| BU-SCM-WH-Mindanao | Tahanan Supply Chain | Cost Center |
| BU-SCM-Planning | Tahanan Supply Chain | Cost Center |
| BU-Property-RealEstate | Tahanan Property | Revenue Center |
| BU-Property-Facilities | Tahanan Property | Cost Center |
| BU-Digital-POS | Tahanan Digital | Cost Center |
| BU-Digital-ECommerce | Tahanan Digital | Revenue Center |
| BU-Digital-ITServices | Tahanan Digital | Revenue Center |
| BU-Digital-Analytics | Tahanan Digital | Cost Center |

---

## 9.3 Chart of Accounts — Key Account Ranges

### 9.3.1 Natural Account Segment (6-digit)

| Range | Account Type | Examples |
|-------|-------------|----------|
| 100000-109999 | Current Assets | Cash (100100), Petty Cash (100200), AR Trade (101000), AR B2B (101100) |
| 110000-119999 | Inventory Assets | Inventory FG (110100), Inventory In-Transit (110200) |
| 120000-129999 | Other Current Assets | Prepaid Expenses, Deposits |
| 130000-139999 | Non-Current Assets | PPE - Buildings (130100), PPE - Equipment (130200), PPE - Vehicles (130300) |
| 140000-149999 | Intangible Assets | Software (140100), Leasehold Improvements (140200) |
| 200000-209999 | Current Liabilities | AP Trade (200100), AP Accrued (200200), Customer Deposits (200300) |
| 210000-219999 | Statutory Payables | SSS Payable (210100), PhilHealth Payable (210200), Pag-IBIG Payable (210300), VAT Payable (210400), WTA Payable (210500), EWT Payable (210600) |
| 220000-229999 | Other Current Liabilities | Gift Card Liability (220100), Loyalty Points Liability (220200), Deferred Revenue (220300) |
| 230000-239999 | Non-Current Liabilities | Long-term Debt, Lease Liability |
| 300000-309999 | Equity | Common Stock (300100), Additional Paid-in Capital (300200), Retained Earnings (300300) |
| 400000-409999 | Revenue | Sales Revenue (400100), Sales Returns (400200), Installation Revenue (400300) |
| 410000-419999 | Other Revenue | Rental Income (410100), IT Services Revenue (410200), Management Fee Income (410300) |
| 500000-509999 | COGS | COGS - Merchandise (500100), COGS - Services (500200), Freight-In (500300) |
| 510000-519999 | Purchases & Variances | Purchase Price Variance (510100), Landed Cost Variance (510200) |
| 600000-609999 | Selling Expenses | Salaries - Store Ops (600100), Rent Expense (600200), Utilities - Stores (600300), Marketing (600400) |
| 610000-619999 | General & Admin | Salaries - Corp (610100), Office Supplies (610200), Professional Fees (610300), Insurance (610400) |
| 620000-629999 | Depreciation & Amortization | Depr - Buildings (620100), Depr - Equipment (620200), Depr - Vehicles (620300), Amort - Software (620400) |
| 700000-709999 | Other Income/Expense | Interest Income (700100), Interest Expense (700200), FX Gain/Loss (700300), Gain/Loss on Disposal (700400) |
| 800000-809999 | Income Tax | Current Income Tax (800100), Deferred Income Tax (800200), MCIT (800300) |
| 900000-909999 | Intercompany | IC Receivable (900100), IC Payable (900200), IC Revenue (900300), IC Expense (900400) |

---

## 9.4 Tax Configuration

### 9.4.1 Tax Rates

| Tax Type | Rate | Oracle Tax Code | BIR Form |
|----------|------|----------------|----------|
| Output VAT | 12% | PH-VAT-12 | 2550M/Q |
| Input VAT | 12% | PH-INPUT-VAT-12 | 2550M/Q |
| EWT - Goods | 1% | PH-EWT-GOODS-1 | 1601-E |
| EWT - Services (Professional) | 5% | PH-EWT-SVC-5 | 1601-E |
| EWT - Services (Contractor) | 2% | PH-EWT-CONT-2 | 1601-E |
| EWT - Rental | 5% | PH-EWT-RENT-5 | 1601-E |
| EWT - Interest | 20% | PH-EWT-INT-20 | 1601-E |
| WTA - Compensation | Per TRAIN law bracket | PH-WTA-COMP | 1601-C |
| Corporate Income Tax (RCIT) | 30% (or 20% if taxable income ≤ PHP 5M, total assets ≤ PHP 100M) | PH-CIT | 1702 |
| MCIT | 2% of gross income | PH-MCIT | 1702 |

### 9.4.2 Tax Reporting Calendar

| Return | Deadline | Oracle Module |
|--------|----------|---------------|
| Monthly VAT (2550M) | 20th of following month | Tax Reporting |
| Quarterly VAT (2550Q) | 25th of month following quarter | Tax Reporting |
| Monthly WTA (1601-C) | 10th of following month | Payroll + Tax Reporting |
| Monthly EWT (1601-E) | 10th of following month | Payables + Tax Reporting |
| Quarterly Income Tax (1701Q) | 60 days after quarter end | Tax Reporting |
| Annual Income Tax (1702) | April 15 (or 15th of 4th month after year-end) | Tax Reporting |
| Annual ITR (employees 1604-C) | January 31 | Payroll + Tax Reporting |
| Annual Supplier List (1604-E) | January 31 | AP + Tax Reporting |

---

## 9.5 Product Hierarchy Configuration

### 9.5.1 Item Catalog Structure

```
Level 1: Department (12)
  └── Level 2: Class (~60)
       └── Level 3: Subclass (~300)
            └── Level 4: Item (~80,000 active SKUs)
```

| Department Code | Department Name | Class Examples |
|-----------------|----------------|----------------|
| DEPT-01 | Lumber & Building Materials | Lumber, Cement, Steel, Roofing, Hollow Blocks |
| DEPT-02 | Electrical | Wiring, Circuit Breakers, Lighting, Switches |
| DEPT-03 | Plumbing | PVC Pipes, Fittings, Faucets, Water Heaters |
| DEPT-04 | Paint & Decorating | Paint, Wallpaper, Brushes, Rollers |
| DEPT-05 | Hardware & Tools | Hand Tools, Power Tools, Fasteners, Adhesives |
| DEPT-06 | Appliances | Air Conditioners, Refrigerators, Washing Machines |
| DEPT-07 | Flooring & Tiles | Ceramic Tiles, Vinyl, Laminates |
| DEPT-08 | Kitchen & Bath | Cabinets, Countertops, Sinks, Vanities |
| DEPT-09 | Doors & Windows | Entry Doors, Interior Doors, Glass Windows |
| DEPT-10 | Garden & Outdoor | Plants, Pots, Outdoor Furniture, Grills |
| DEPT-11 | Safety & Security | Locks, CCTV, Fire Extinguishers, PPE |
| DEPT-12 | Storage & Organization | Shelving, Cabinets, Bins, Tool Storage |

### 9.5.2 Item Template Attributes

| Attribute | Required | Example |
|-----------|----------|---------|
| Item Number | Yes | ELEC-WS-00123 |
| Description | Yes | Philips LED Bulb 12W Cool White |
| Long Description | Yes | Full product description for e-commerce |
| Department | Yes | DEPT-02 |
| Class | Yes | CLS-02-03 (Lighting) |
| Subclass | Yes | SUB-02-03-01 (LED Bulbs) |
| Primary UOM | Yes | PCS |
| Secondary UOM | No | BOX (if sold in bulk) |
| Weight | Yes | 0.065 KG |
| Dimensions | No | L×W×H |
| Country of Origin | Yes | Philippines / China / etc. |
| HS Code | Yes (for imports) | 8539.50.10 |
| Barcode (EAN/UPC) | Yes | 8718696174853 |
| Lot Control | Conditional | Yes for paint, cement |
| Serial Control | Conditional | Yes for power tools, appliances |
| Shelf Life | Conditional | Yes for adhesives, chemicals |
| Hazardous Flag | Yes | Yes/No |
| Track Inventory | Yes | Yes |
| Costing Method | Yes | Moving Average / Standard |
| List Price | Yes | PHP 149.00 |
| Tax Classification | Yes | VAT-12% |
| Returnable | Yes | Yes/No |
| Warranty Months | Conditional | 24 (for appliances/tools) |

---

## 9.6 Supplier Configuration

### 9.6.1 Supplier Classification

| Classification | Definition | Typical Count |
|----------------|------------|---------------|
| Direct Importer | Imports directly from overseas manufacturers | ~200 |
| Local Manufacturer | Produces goods domestically | ~500 |
| Local Distributor | Distributes brands in the Philippines | ~1,000 |
| Service Provider | Non-merchandise suppliers | ~500 |
| One-Time | Infrequent / project-based | ~300 |

### 9.6.2 Supplier Payment Terms

| Term Code | Description | Discount |
|-----------|-------------|----------|
| NET-30 | Payment due 30 days from invoice date | — |
| NET-45 | Payment due 45 days from invoice date | — |
| NET-60 | Payment due 60 days from invoice date | — |
| 2-10-NET-30 | 2% discount if paid within 10 days, net 30 | 2% |
| COD | Cash on delivery | — |
| CBD | Cash before delivery | — |
| LC-60 | Letter of Credit, 60 days from B/L date | — |
| LC-SIGHT | Letter of Credit, at sight | — |

---

## 9.7 Customer Configuration

### 9.7.1 Customer Classification

| Classification | Definition | Payment Terms |
|----------------|------------|---------------|
| Walk-In (Retail) | Individual retail customers | Cash/Card on purchase |
| Loyalty Member | Enrolled in Tahanan Rewards | Same as Walk-In |
| B2B Contractor | Licensed contractors and builders | Credit per tier (POL-FIN-004) |
| B2B Developer | Real estate developers | Credit per tier |
| B2B Government | Government agencies | Per government procurement terms |
| B2B Institutional | Schools, hospitals, hotels | Credit per agreement |
| E-Commerce | Online customers | Pre-paid or COD |

### 9.7.2 B2B Credit Terms (in Oracle Receivables)

| Term | Description |
|------|-------------|
| B2B-NET-30 | Net 30 days (Silver tier) |
| B2B-NET-45 | Net 45 days (Gold tier) |
| B2B-NET-60 | Net 60 days (Platinum tier) |

---

## 9.8 Workflow Configuration Summary

### 9.8.1 Approval Workflows

| Workflow | Module | Trigger | Rules |
|----------|--------|---------|-------|
| PO Approval | Purchasing | PO creation | Amount-based hierarchy (POL-FIN-001) |
| PR Approval | Purchasing | Requisition submission | Amount-based hierarchy |
| AP Invoice Approval | Payables | Invoice submission | Amount + exception-based |
| Expense Approval | Expenses | Expense report submission | Amount-based hierarchy |
| Journal Approval | GL | Manual journal entry | Amount-based hierarchy |
| Returns Approval | Order Management | Return request | Amount-based (SOP-POS-004) |
| Inventory Adjustment | Inventory | Adjustment request | Amount-based (POL-SCM-003) |
| New Item Approval | PLM | Item creation request | Cross-functional review |
| New Supplier Approval | Supplier Mgmt | Supplier registration | Procurement + Finance review |
| Hiring Approval | Recruiting | Job requisition | Budget-based hierarchy |
| Leave Approval | Absence Mgmt | Leave request | Direct supervisor |
| OT Approval | Time & Labor | Overtime claim | Direct supervisor |
| Capex Approval | Projects | Capex request | Amount-based (POL-FIN-007) |

---

## 9.9 Reporting and Analytics Configuration

### 9.9.1 Key Performance Indicators (KPIs)

#### Financial KPIs

| KPI | Oracle Module | Frequency | Target |
|-----|---------------|-----------|--------|
| Revenue (total, by store, by category) | ERP Analytics | Daily | Per budget |
| Gross Margin % | ERP Analytics | Daily | 28-32% |
| EBITDA Margin | ERP Analytics | Monthly | 10-12% |
| Net Profit Margin | ERP Analytics | Monthly | 5-7% |
| Days Sales Outstanding (B2B) | AR Analytics | Weekly | < 45 days |
| Days Payable Outstanding | AP Analytics | Monthly | 35-45 days |
| Cash Conversion Cycle | Cash Mgmt Analytics | Monthly | < 30 days |
| Inventory Turnover | SCM Analytics | Monthly | 8-12x |
| SG&A as % of Revenue | ERP Analytics | Monthly | < 18% |
| Same Store Sales Growth | ERP Analytics | Monthly | > 5% YoY |

#### Supply Chain KPIs

| KPI | Oracle Module | Frequency | Target |
|-----|---------------|-----------|--------|
| Forecast Accuracy (MAPE) | SCP Analytics | Monthly | < 20% |
| Fill Rate | SCM Analytics | Weekly | > 95% |
| On-Time Delivery (WH → Store) | TMS Analytics | Weekly | > 98% |
| Inventory Accuracy | Inventory Analytics | Monthly | > 98% (WH), > 95% (Store) |
| Shrinkage | Inventory Analytics | Monthly | < 1.5% of sales |
| Warehouse Productivity (units/man-hour) | WMS Analytics | Weekly | Per target |
| Dead Stock % | Inventory Analytics | Monthly | < 3% |
| Supplier On-Time Delivery | Procurement Analytics | Monthly | > 90% |
| PO Cycle Time | Procurement Analytics | Monthly | < 3 days (standard) |

#### HR KPIs

| KPI | Oracle Module | Frequency | Target |
|-----|---------------|-----------|--------|
| Employee Turnover Rate | HCM Analytics | Monthly | < 5% annual (management), < 15% (operations) |
| Time to Fill (days) | Recruiting Analytics | Monthly | < 30 days |
| Training Completion Rate | Learning Analytics | Monthly | 100% mandatory |
| Employee Engagement Score | ME Analytics | Quarterly | > 80% |
| Labor Cost as % of Revenue | HCM Analytics | Monthly | < 12% |
| Absenteeism Rate | T&L Analytics | Monthly | < 3% |
| Open Positions | Recruiting Analytics | Weekly | < 5% of headcount |

#### Customer KPIs

| KPI | Oracle Module | Frequency | Target |
|-----|---------------|-----------|--------|
| Net Promoter Score (NPS) | CX Analytics | Monthly | > 50 |
| Customer Satisfaction (CSAT) | CX Analytics | Monthly | > 90% |
| Loyalty Member Count | CX Loyalty Analytics | Monthly | Growing 10% QoQ |
| Loyalty Active Rate | CX Loyalty Analytics | Monthly | > 60% (transacted in 90 days) |
| Repeat Purchase Rate | CX Analytics | Monthly | > 40% |
| Customer Complaints per 10K transactions | Service Analytics | Weekly | < 5 |
| E-Commerce Conversion Rate | Commerce Analytics | Weekly | > 2% |
| Average Transaction Value | POS + ERP Analytics | Daily | Growing QoQ |
