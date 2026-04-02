# 12 — MASTER DATA GOVERNANCE

## 12.1 Data Governance Framework

### 12.1.1 Data Governance Vision

Tahanan Depot recognizes master data as a strategic enterprise asset. The Data Governance Framework establishes accountability, standards, and processes to ensure data accuracy, completeness, consistency, and timeliness across all systems — Oracle Fusion Cloud, custom POS, and third-party applications.

### 12.1.2 Data Governance Organization

```
DATA GOVERNANCE COUNCIL
├── Chair: VP Data & Analytics
├── Members: VP Finance, VP Procurement, VP Store Ops, VP Enterprise Apps, VP HR, VP Merchandising
├── Frequency: Monthly meetings; quarterly reviews with executive steering committee
└── Responsibilities:
    ├── Approve data governance policies and standards
    ├── Resolve cross-functional data disputes
    ├── Prioritize data quality improvement initiatives
    ├── Review data quality scorecards
    └── Approve master data lifecycle decisions
│
DATA STEWARDS (by domain)
├── Financial Data Steward (GL CoA, cost centers, entities)
├── Product Data Steward (item master, product hierarchy, pricing)
├── Supplier Data Steward (supplier master, qualifications)
├── Customer Data Steward (customer master, loyalty data)
├── HR Data Steward (employee master, organization data)
├── Inventory Data Steward (inventory orgs, locators, subinventories)
└── Integration Data Steward (POS-Oracle mapping tables, API contracts)
│
DATA CUSTODIANS (IT)
├── Oracle Fusion Administrator (system configuration, access)
├── POS Database Administrator (POS data management)
├── OIC Administrator (integration data flows)
└── BI/Analytics Administrator (reporting data)
```

### 12.1.3 Data Governance Principles

1. **Single Source of Truth** — Oracle Fusion Cloud is the authoritative master data source for financial, supply chain, HR, and customer data.
2. **Data Ownership** — Every data domain has a named business owner (steward) accountable for data quality.
3. **Standardized Entry** — All master data creation follows standardized templates and approval workflows.
4. **Change Control** — All master data changes are tracked, approved, and auditable.
5. **Quality Measurement** — Data quality KPIs are monitored and reported monthly.
6. **Minimal Redundancy** — Data is captured once and reused across systems; no parallel manual records.
7. **Privacy by Design** — Personal data handling follows Data Privacy Act (RA 10173) requirements.

---

## 12.2 Master Data Domains

### 12.2.1 Domain Overview

| Domain | Master System | Consumer Systems | Volume | Steward |
|--------|-------------|-----------------|--------|---------|
| Chart of Accounts | Oracle GL | All Oracle modules, POS (mapped) | ~500 active accounts | VP Finance |
| Legal Entities | Oracle GL | All Oracle modules | 5 entities | VP Finance |
| Business Units | Oracle GL | All Oracle modules | 18 BUs | VP Finance |
| Item Master | Oracle PLM | POS, WMS, Purchasing, Inventory, Order Mgmt | ~80,000 active SKUs | VP Merchandising |
| Product Hierarchy | Oracle PLM | POS, WMS, Analytics | 12 depts, ~60 classes, ~300 subclasses | VP Merchandising |
| Supplier Master | Oracle Supplier Mgmt | Payables, Purchasing, Sourcing | ~2,500 active | VP Procurement |
| Customer Master | Oracle CX CDP + AR | POS, Order Mgmt, Loyalty, Commerce | ~1M+ (B2C loyalty + B2B) | VP Customer Service |
| Employee Master | Oracle HCM Core HR | Payroll, T&L, Expenses, Learning | ~6,500 active | CHRO |
| Organization Hierarchy | Oracle HCM + GL | All modules | Updated per org changes | VP Finance + CHRO |
| Inventory Organizations | Oracle Inventory | WMS, POS, SCM | 4 warehouses + 120 stores | VP Supply Chain |
| Pricing / Price Lists | Oracle Pricing | POS (synced), Order Mgmt | Multiple price lists | VP Merchandising |
| Cost Centers | Oracle GL | All modules | ~200 active | VP Finance |
| Locations / Warehouses | Oracle Inventory + TMS | All SCM modules | 125 physical locations | VP Supply Chain |
| Tax Codes | Oracle Tax | Payables, AR, POS (mapped) | ~15 active tax codes | VP Tax |
| Payment Terms | Oracle Payables/AR | Purchasing, AR | ~8 standard terms | VP Finance |
| Loyalty Program | Oracle CX Loyalty | POS, Commerce, Marketing | Rules, tiers, point values | VP Loyalty & CRM |
| POS Mapping Tables | POS (local) + Oracle (source) | POS, OIC | Item-price-customer maps | POS Dev Manager |

---

## 12.3 Data Quality Standards

### 12.3.1 Data Quality Dimensions

| Dimension | Definition | Measurement Method | Target |
|-----------|-----------|-------------------|--------|
| **Completeness** | Percentage of required fields populated | Automated null/empty check on required fields | > 99% |
| **Accuracy** | Percentage of records matching verified source | Sample-based audit; cross-system reconciliation | > 98% |
| **Consistency** | Percentage of records identical across systems | Cross-system comparison (Oracle vs. POS vs. supplier portal) | > 99% |
| **Timeliness** | Percentage of records updated within SLA | Timestamp analysis (creation vs. availability) | > 95% within SLA |
| **Uniqueness** | Percentage of records with no duplicates | Duplicate detection algorithms; matching rules | > 99.5% |
| **Validity** | Percentage of records conforming to format rules | Validation rules (format, range, referential integrity) | > 99% |

### 12.3.2 Data Quality KPIs by Domain

| Domain | KPI | Target | Measurement Frequency | Owner |
|--------|-----|--------|----------------------|-------|
| Item Master | Completeness of mandatory attributes | > 99% | Weekly | Product Data Steward |
| Item Master | Barcode validity | > 99.5% | Weekly | Product Data Steward |
| Item Master | Oracle-POS sync consistency | > 99% | Daily | Integration Data Steward |
| Supplier Master | BIR/SEC/DTI documentation completeness | 100% | Monthly | Supplier Data Steward |
| Supplier Master | Bank account accuracy | > 99% | Monthly | Supplier Data Steward |
| Customer Master | Loyalty card uniqueness | > 99.9% | Monthly | Customer Data Steward |
| Customer Master | B2B customer credit data completeness | > 98% | Monthly | Customer Data Steward |
| Employee Master | Personal data completeness | > 99% | Monthly | HR Data Steward |
| Employee Master | Assignment data accuracy | > 99% | Monthly | HR Data Steward |
| Inventory | Oracle-POS inventory sync variance | < 2% | Daily | Inventory Data Steward |
| Pricing | Price consistency (Oracle vs. POS) | 100% | Daily (per sync cycle) | Product Data Steward |
| GL | Account reconciliation auto-match rate | > 90% | Monthly | Financial Data Steward |
| GL | Intercompany matching rate | > 95% | Monthly | Financial Data Steward |

---

## 12.4 Master Data Lifecycle Management

### 12.4.1 Item Master Lifecycle

| Stage | Process | Approval | Oracle Module | SLA |
|-------|---------|----------|---------------|-----|
| **Creation** | New item request submitted via PLM with all mandatory attributes | Category Manager → VP Merchandising | PLM | 3 business days |
| **Enrichment** | Add extended attributes (specs, images, safety data, barcodes) | Product Data Steward | PLM | 2 business days |
| **Classification** | Assign to department/class/subclass; assign tax code, costing method | Product Data Steward | PLM + Tax + Cost Mgmt | 1 business day |
| **Pricing** | Set list price, contractor price, wholesale price | Pricing Analyst → Category Manager | Pricing | 1 business day |
| **Sourcing** | Assign to supplier; set lead time, MOQ, order multiples | Buyer Planner | Purchasing + SCP | 2 business days |
| **Distribution** | Assign to warehouses and stores; set safety stock, min/max | Demand Planner | SCP + Inventory | 1 business day |
| **POS Sync** | Push to POS via INT-004 (item master sync) | Automatic (upon approval) | OIC | < 30 minutes |
| **Active** | Item available for sale and replenishment | — | All | — |
| **Review** | Periodic review of performance (sales, margin, inventory turns) | Category Manager | Analytics | Monthly |
| **Phase-Out** | Discontinuation decision; stop replenishment; sell through existing stock | Category Manager → VP Merchandising | PLM + SCP | Per sell-through plan |
| **Deactivation** | Mark as inactive; no further transactions; retain for historical reporting | Product Data Steward | PLM | Upon sell-through completion |

### 12.4.2 Supplier Master Lifecycle

| Stage | Process | Approval | Oracle Module | SLA |
|-------|---------|----------|---------------|-----|
| **Registration** | Supplier self-registers via Supplier Portal with BIR, SEC/DTI documents | Procurement + Finance review | Supplier Mgmt | 5 business days |
| **Qualification** | Background check, trade reference verification, product sampling | Sourcing Manager | Supplier Mgmt | 5 business days |
| **Activation** | Approve supplier for purchasing; assign payment terms, tax classification | VP Procurement + AP Manager | Supplier Mgmt + Payables | 2 business days |
| **Onboarding** | Set up in sourcing events; assign to categories; share forecast data | Buyer Planner | Sourcing + SCP | 3 business days |
| **Active** | Supplier eligible for POs and payments | — | All | — |
| **Evaluation** | Quarterly scorecard review (delivery, quality, price, responsiveness) | Sourcing Manager | Supplier Mgmt | Quarterly |
| **Probation** | Below-threshold scorecard; corrective action plan | VP Procurement | Supplier Mgmt | Per evaluation |
| **Deactivation** | Remove from active supplier list; close outstanding obligations | VP Procurement + VP Finance | Supplier Mgmt | Per procedure |

### 12.4.3 Customer Master Lifecycle

| Stage | Process | Approval | Oracle Module | SLA |
|-------|---------|----------|---------------|-----|
| **Walk-In** | No record created; generic customer used in POS | — | AR (generic customer) | — |
| **Loyalty Enrollment** | Customer enrolls in-store or online; profile created in CDP | Automatic (self-service) | CX CDP + Loyalty | Real-time |
| **B2B Application** | Contractor/developer applies for credit account; submits documents | AR Manager + VP Finance | AR + CX Sales | 5 business days |
| **Credit Approval** | Credit check, trade reference verification, credit limit assignment | VP Finance (per POL-FIN-004) | AR (credit management) | 3 business days |
| **Active** | Customer eligible for transactions, loyalty points, credit (if B2B) | — | All | — |
| **Review** | Annual credit review (B2B); loyalty tier recalculation | AR Manager / Loyalty Manager | AR + Loyalty | Annual |
| **Deactivation** | Account closed; outstanding balances settled; data retained per policy | AR Manager + DPO approval | AR + CDP | Per procedure |

### 12.4.4 Employee Master Lifecycle

| Stage | Process | Approval | Oracle Module | SLA |
|-------|---------|----------|---------------|-----|
| **Pre-Hire** | Candidate data captured in Recruiting | Recruiting Specialist | Recruiting | Per hiring process |
| **Onboarding** | Employee record created; assignment, compensation, benefits enrolled | HR Coordinator | Core HR + Compensation + Benefits | Day 1 |
| **Active** | Employee assigned to department, position, location | — | All HCM modules | — |
| **Transfer** | Department, location, or position change | HRBP + receiving manager | Core HR | 3 business days |
| **Separation** | Offboarding initiated; system access revoked; final pay processed | HRBP + IT + Finance | Core HR + Payroll | Per SOP-HR-004 |
| **Archival** | Record archived; retained per data retention policy (10 years for tax) | Automatic | Core HR | Upon separation |

---

## 12.5 Data Migration Strategy

### 12.5.1 Migration Approach

| Data Domain | Source | Migration Method | Validation | Cutover Timing |
|-------------|--------|-----------------|------------|----------------|
| Chart of Accounts | Excel templates | Manual upload via FBDI | Cross-foot validation; trial balance match | Phase 1 cutover |
| Supplier Master | Legacy supplier list | FBDI import + manual enrichment | BIR/DTI doc verification; bank account validation | Phase 1 cutover |
| Customer Master (B2B) | Legacy CRM | FBDI import | Credit limit review; outstanding balance reconciliation | Phase 1 cutover |
| Item Master (initial) | Excel templates | FBDI import via PLM | Attribute completeness check; barcode validation | Phase 2 cutover |
| Item Master (full) | Phased load | FBDI import in batches | Per-batch validation; POS sync verification | Phase 6 |
| Employee Master | Legacy HR / Excel | HCM Data Loader | Employee self-verification; statutory deduction validation | Phase 1 cutover |
| Opening Balances | Legacy GL trial balance | Manual journal entries | Trial balance reconciliation; external auditor review | Phase 1 cutover |
| Inventory Balances | Physical count at cutover | Manual entry + import | Cycle count reconciliation; valuation verification | Phase 2 cutover |
| Open Purchase Orders | Legacy system extract | Manual re-entry or import | Supplier confirmation; value match | Phase 2 cutover |
| Historical Transactions | Not migrated | Reporting from legacy (read-only) | N/A — dual system for 12 months | — |

### 12.5.2 Data Migration Rules

1. **No historical transaction migration** — Only master data and open transactions migrated to Oracle Fusion.
2. **Legacy system access** — Legacy system maintained in read-only mode for 12 months post go-live for historical reporting.
3. **Cutover inventory count** — Wall-to-wall physical inventory count at all locations during cutover weekend.
4. **Employee self-verification** — All employees verify personal data in Oracle HCM within first week of go-live.
5. **Supplier re-registration** — All active suppliers invited to register via Oracle Supplier Portal; existing data pre-populated.
6. **Validation sign-off** — Each data domain migration signed off by data steward and VP before go-live.

---

## 12.6 Data Retention and Purging

### 12.6.1 Data Retention Schedule

| Data Category | Retention Period | Legal Basis | Purging Method |
|--------------|-----------------|-------------|----------------|
| Financial transactions (GL, AP, AR) | 10 years | BIR (NIRC requires 10-year retention) | Oracle Fusion data archival; not purged during active years |
| Tax returns and supporting documents | 10 years | BIR | Document archival |
| Employee records (active) | Duration of employment | DOLE | Active in Oracle HCM |
| Employee records (separated) | 10 years from separation | BIR (tax), DOLE (labor) | Archived in Oracle HCM; purged after retention period |
| Payroll records | 10 years | BIR | Oracle Payroll archival |
| Supplier records | Duration of relationship + 5 years | BIR, commercial law | Supplier deactivated; retained for reference |
| Customer records (B2B) | Duration of relationship + 3 years | Commercial law, Data Privacy Act | Anonymized after retention |
| Customer records (B2C / Loyalty) | Duration of membership + 2 years (or per consent withdrawal) | Data Privacy Act (RA 10173) | Anonymized upon request or after retention |
| POS transaction data (local) | 90 days (post-sync confirmation) | Data minimization | Auto-purge from POS local storage |
| Integration logs (OIC) | 1 year | Operational monitoring | Auto-purge |
| Audit trails | 10 years | SOX-equivalent, BIR | Retained in Oracle |
| Camera / surveillance footage | 30 days (90 days for incidents) | Security | Auto-overwrite |
| Customer CCTV footage | 30 days | Data Privacy Act | Auto-overwrite |

---

## 12.7 Data Quality Monitoring and Reporting

### 12.7.1 Data Quality Dashboard

| Metric | Visualization | Frequency | Owner |
|--------|--------------|-----------|-------|
| Master data completeness by domain | Stacked bar chart | Weekly | Data Stewards |
| Data quality score by dimension | Radar chart | Monthly | VP Data & Analytics |
| Sync consistency (Oracle ↔ POS) | Trend line | Daily | Integration Data Steward |
| Duplicate records detected | Count + trend | Weekly | Data Stewards |
| Data quality incidents (open) | Table + aging | Weekly | Data Governance Council |
| Stale data records (not updated per policy) | Count by domain | Monthly | Data Stewards |
| Data governance initiative progress | Kanban | Monthly | VP Data & Analytics |

### 12.7.2 Data Quality Issue Management

| Severity | Definition | Response Time | Resolution Target | Escalation |
|----------|-----------|---------------|-------------------|------------|
| Critical | Data issue causing business process failure or financial impact | 4 hours | 24 hours | VP-level + Data Governance Council |
| High | Data issue affecting multiple users or reports | 8 hours | 3 business days | Data Steward + Domain VP |
| Medium | Data quality below target but not blocking operations | 24 hours | 5 business days | Data Steward |
| Low | Minor data quality improvement opportunity | 3 business days | 10 business days | Data Steward |
