# Quality Management

**Document ID:** TD-OPS-021
**Revision:** 3.2
**Effective Date:** April 1, 2026
**Classification:** Internal — Operations
**Owner:** VP for Merchandising & Quality Assurance
**Approved By:** Chief Operations Officer

| Field | Detail |
|---|---|
| Document Title | Quality Management |
| Document Set | Tahanan Depot Operations Documentation |
| Document Number | Doc 21 |
| Department | Quality Assurance / Merchandising / Supply Chain |
| Review Cycle | Annual (or upon regulatory change) |
| Last Reviewed | March 15, 2026 |
| Next Review | March 15, 2027 |

---

## Revision History

| Rev | Date | Author | Description |
|---|---|---|---|
| 1.0 | Jan 10, 2022 | M. Reyes | Initial release |
| 2.0 | Jun 15, 2023 | R. Santos | Added BPS/PS mark compliance section |
| 2.5 | Feb 20, 2024 | A. Cruz | Oracle Fusion PLM Quality integration |
| 3.0 | Sep 10, 2025 | J. Villanueva | DTI DAO 2024-03 updates, recall procedure revision |
| 3.2 | Mar 15, 2026 | M. Reyes | Added SIR mark requirements, updated defect rate targets |

---

## Table of Contents

1. [Quality Management Framework](#1-quality-management-framework)
2. [Incoming Quality Inspection](#2-incoming-quality-inspection)
3. [In-Store Quality Control](#3-in-store-quality-control)
4. [Supplier Quality Management](#4-supplier-quality-management)
5. [Product Certification and Standards Compliance](#5-product-certification-and-standards-compliance)
6. [Defective Product Handling](#6-defective-product-handling)
7. [Product Recall Procedures](#7-product-recall-procedures)
8. [Customer Quality Complaints](#8-customer-quality-complaints)
9. [Quality Metrics and Reporting](#9-quality-metrics-and-reporting)
10. [Quality Training](#10-quality-training)

---

## 1. Quality Management Framework

### 1.1 Quality Policy Statement

Tahanan Depot is committed to providing safe, reliable, and standards-compliant home improvement products to Filipino households and building professionals. Every product on our shelves must meet or exceed applicable Philippine National Standards (PNS), Department of Trade and Industry (DTI) requirements, and internal quality benchmarks.

Our quality management system covers the full product lifecycle — from supplier qualification and incoming inspection through in-store display, customer delivery, and post-sale support — across our portfolio of approximately 80,000 active SKUs spanning building materials, electrical supplies, plumbing fixtures, paint and coatings, hand and power tools, and home appliances.

### 1.2 Quality Objectives

| Objective | Target | Measurement Frequency | Oracle Fusion Module |
|---|---|---|---|
| Incoming inspection pass rate | ≥ 97.5% | Monthly | PLM Quality |
| In-store defect identification rate | ≥ 95% | Quarterly | Inventory Management |
| Customer quality complaint resolution | ≤ 5 business days | Monthly | Order Management |
| Supplier quality score (weighted average) | ≥ 85/100 | Quarterly | Supplier Management |
| Product recall response time (Class I) | ≤ 24 hours | Per incident | PLM Quality |
| Regulatory compliance rate | 100% | Monthly | PLM Quality |
| Defective inventory write-off rate | ≤ 0.4% of COGS | Monthly | Inventory Management |
| Quality training completion rate | 100% annual | Semi-annual | N/A (HR system) |

### 1.3 Quality Organization Structure

| Role | Responsibility | Reporting Line | Team Size |
|---|---|---|---|
| VP, Merchandising & Quality Assurance | Executive quality oversight, policy approval | COO | 1 |
| Director, Quality Assurance | Strategic quality planning, regulatory liaison | VP Merchandising & QA | 1 |
| Quality Assurance Manager — Central | Incoming inspection, supplier audits, lab coordination | Director, QA | 1 |
| Quality Assurance Manager — Retail | In-store QC, shelf-life monitoring, customer complaints | Director, QA | 1 |
| Regional Quality Supervisors (Luzon, Visayas, Mindanao) | Regional inspection oversight, store audits | QA Manager — Retail | 3 |
| Quality Inspectors — DC (Distribution Centers) | Physical inspection, sampling, documentation | QA Manager — Central | 24 |
| Quality Inspectors — Import | Imported goods inspection, certification verification | QA Manager — Central | 8 |
| In-Store Quality Associates | Shelf checks, damaged goods tagging, FIFO verification | Store Manager (dotted to Regional QS) | 112 |
| Compliance Officer | Regulatory standards tracking, DTI/BPS liaison | Director, QA | 2 |
| Quality Data Analyst | Oracle Fusion quality dashboards, metrics reporting | Director, QA | 2 |

### 1.4 Quality Committee

The Tahanan Depot Quality Committee governs all quality-related decisions, policy changes, and escalation resolutions.

| Committee | Chair | Members | Frequency | Scope |
|---|---|---|---|---|
| Executive Quality Council | COO | VP Merchandising & QA, CFO, VP Supply Chain, VP Retail Operations | Quarterly | Strategic quality direction, major recall decisions, policy approval |
| Quality Review Board | Director, QA | QA Managers, Compliance Officer, Category Managers (rotating) | Monthly | Defect trends, supplier scorecards, inspection process improvements |
| Category Quality Working Group | QA Manager — Central | Category Specialist, Inspector Lead, Supplier Relations Rep | Bi-weekly | Category-specific quality issues, specification updates |
| Store Quality Huddle | Regional Quality Supervisor | Store Managers (regional), In-Store Quality Leads | Weekly | In-store QC findings, shelf-life alerts, customer complaints |

### 1.5 Oracle Fusion Integration Overview

All quality processes documented herein are supported by Oracle Fusion applications. The following table maps each quality process to its primary Oracle Fusion module and key features used.

| Quality Process | Oracle Fusion Module | Key Features |
|---|---|---|
| Quality planning and specification management | PLM Quality | Quality plans, inspection specifications, characteristic definitions |
| Incoming inspection execution | PLM Quality + Inventory Management | Inspection lot creation, recording results, usage decisions |
| Supplier quality scoring | Supplier Management | Supplier scorecard, quality KPIs, qualification workflow |
| Nonconformance tracking | PLM Quality | NCR logging, disposition workflow, corrective action requests |
| In-store quality checks | Inventory Management | Cycle count quality hold, lot/expiry tracking, subinventory transfer |
| Recall management | PLM Quality + Order Management | Hold processing, customer notification, traceability query |
| Customer quality complaints | Order Management + PLM Quality | Return/replacement processing, quality investigation linkage |
| Quality reporting and analytics | PLM Quality | Dashboards, defect Pareto, supplier quality trend analysis |

---

## 2. Incoming Quality Inspection

### 2.1 Inspection Process Overview

All merchandise entering Tahanan Depot distribution centers must undergo incoming quality inspection before being received into sellable inventory. The inspection process is triggered automatically in Oracle Fusion Inventory Management upon purchase order arrival notification.

| Stage | Activity | Responsible Party | Oracle Fusion Action | SLA |
|---|---|---|---|---|
| 1 | PO arrival notification | DC Receiving | Create inspection lot in PLM Quality | Within 1 hour of dock arrival |
| 2 | Sampling plan selection | Quality Inspector | Auto-assigned by item quality plan | Immediate |
| 3 | Physical inspection | Quality Inspector | Record inspection results | Within 24 hours (local), 48 hours (import) |
| 4 | Document verification | Quality Inspector / Compliance | Verify certifications, PS/ICC marks | Concurrent with Stage 3 |
| 5 | Usage decision | QA Supervisor | Approve, conditionally approve, or reject | Within 4 hours of inspection completion |
| 6 | Disposition execution | DC Operations | Move to approved stock or quarantine | Within 8 hours of decision |

### 2.2 Inspection Levels by Product Category

| Product Category | Active SKUs | Inspection Level | Sampling Plan | Critical Characteristics | Reference Standard |
|---|---|---|---|---|---|
| Cement & Concrete Products | 850 | Tightened | ANSI/ASQ Z1.4, Level II | Compressive strength, setting time, bag weight | PNS 63, PNS 131 |
| Structural Steel & Rebar | 1,200 | Tightened | ANSI/ASQ Z1.4, Level II | Tensile strength, yield point, dimensional tolerance | PNS 49, PNS 211 |
| Electrical Wiring & Cables | 2,100 | Tightened | ANSI/ASQ Z1.4, Level II | Conductor resistance, insulation thickness, voltage rating | PNS 17, PNS 35 |
| Electrical Fixtures & Fittings | 3,400 | Normal | ANSI/ASQ Z1.4, Level I | Insulation integrity, grounding continuity, heat resistance | PNS 189, IEC 60670 |
| Circuit Breakers & Protection | 950 | Tightened | ANSI/ASQ Z1.4, Level II | Tripping characteristics, short-circuit capacity | PNS 38, IEC 60898 |
| Plumbing Pipes & Fittings (PVC) | 2,800 | Normal | ANSI/ASQ Z1.4, Level I | Dimensional accuracy, pressure rating, UV resistance | PNS 14, PNS 147 |
| Plumbing Fixtures (Faucets, Valves) | 3,600 | Normal | ANSI/ASQ Z1.4, Level I | Flow rate, leak resistance, finish durability | PNS 156, PNS 596 |
| Water Pumps & Tanks | 620 | Reduced | ANSI/ASQ Z1.4, Level S-3 | Flow performance, motor insulation, tank wall thickness | PNS 125, PNS 149 |
| Paint & Coatings | 4,200 | Normal | ANSI/ASQ Z1.4, Level I | Viscosity, hiding power, lead content, VOC level | PNS 244, PNS 245 |
| Adhesives & Sealants | 1,800 | Normal | ANSI/ASQ Z1.4, Level I | Bond strength, curing time, chemical composition | PNS 158, ASTM C557 |
| Hand Tools (Hammers, Wrenches, etc.) | 5,400 | Reduced | ANSI/ASQ Z1.4, Level S-3 | Hardness, dimensional tolerance, handle attachment | PNS 134, ISO 15601 |
| Power Tools | 2,900 | Normal | ANSI/ASQ Z1.4, Level I | Motor performance, safety guards, insulation class | PNS 136, IEC 60745 |
| Safety Equipment (PPE) | 1,100 | Tightened | ANSI/ASQ Z1.4, Level II | Impact resistance, lens clarity (eye protection), filtration (respirators) | PNS 155, PNS 186 |
| Lumber & Plywood | 1,600 | Reduced | ANSI/ASQ Z1.4, Level S-3 | Moisture content, dimensional tolerance, grade marking | PNS 593, PNS 595 |
| Roofing Materials | 750 | Normal | ANSI/ASQ Z1.4, Level I | Thickness, weather resistance, fire rating | PNS 610, ASTM D3462 |
| Door & Window Hardware | 2,300 | Normal | ANSI/ASQ Z1.4, Level I | Lock mechanism function, finish quality, load rating | PNS 596, PNS 812 |
| Ceramic & Porcelain Tiles | 2,200 | Normal | ANSI/ASQ Z1.4, Level I | Dimensional tolerance, water absorption, scratch resistance | PNS 506, ISO 10545 |
| Home Appliances (Major) | 1,800 | Normal | ANSI/ASQ Z1.4, Level I | Electrical safety, performance specs, energy labeling | PNS 922, IEC 60335 |
| Home Appliances (Small) | 3,400 | Reduced | ANSI/ASQ Z1.4, Level S-3 | Electrical safety, motor performance, cord integrity | PNS 922, IEC 60335 |
| Lighting Products | 4,100 | Normal | ANSI/ASQ Z1.4, Level I | Lumen output, color temperature, driver reliability | PNS 189, IEC 60598 |
| Chemicals (Cleaners, Solvents) | 1,900 | Tightened | ANSI/ASQ Z1.4, Level II | Chemical composition, labeling compliance, packaging integrity | FDA AO 2014-0030, DENR DAO |
| Fasteners (Nails, Screws, Bolts) | 6,200 | Reduced | ANSI/ASQ Z1.4, Level S-3 | Thread quality, hardness, coating uniformity | PNS 43, PNS 44 |
| Garden & Outdoor Equipment | 2,800 | Reduced | ANSI/ASQ Z1.4, Level S-3 | Blade sharpness, engine performance, material quality | PNS 157, ISO 10517 |
| Storage & Organization | 1,800 | Reduced | ANSI/ASQ Z1.4, Level S-3 | Load capacity, material thickness, finish quality | Internal spec TD-QS-045 |
| Janitorial & Cleaning Supplies | 1,500 | Reduced | ANSI/ASQ Z1.4, Level S-3 | Packaging integrity, chemical safety, labeling | FDA requirements, DENR DAO |

### 2.3 Sampling Methodology

Tahanan Depot follows ANSI/ASQ Z1.4 (ISO 2859-1) attribute sampling procedures for all incoming inspections.

| Lot Size Range | Sample Size (Level I) | Sample Size (Level II) | Sample Size (Level S-3) |
|---|---|---|---|
| 2 – 8 | 2 | 2 | 2 |
| 9 – 15 | 2 | 3 | 2 |
| 16 – 25 | 3 | 5 | 2 |
| 26 – 50 | 5 | 8 | 3 |
| 51 – 90 | 5 | 13 | 3 |
| 91 – 150 | 8 | 20 | 3 |
| 151 – 280 | 13 | 32 | 5 |
| 281 – 500 | 20 | 50 | 5 |
| 501 – 1,200 | 32 | 80 | 8 |
| 1,201 – 3,200 | 50 | 125 | 8 |
| 3,201 – 10,000 | 80 | 200 | 13 |
| 10,001 – 35,000 | 125 | 315 | 13 |
| 35,001 – 150,000 | 200 | 500 | 20 |
| 150,001 – 500,000 | 315 | 800 | 20 |
| 500,001+ | 500 | 1,250 | 32 |

### 2.4 Acceptance / Rejection Criteria

Acceptable Quality Level (AQL) thresholds are defined per defect severity classification.

| Defect Classification | Definition | AQL | Examples |
|---|---|---|---|
| Critical | Defects that could cause unsafe conditions, regulatory non-compliance, or product failure posing safety risk | 0.0 (zero defects) | Missing PS mark on mandatory item, lead content exceeding PNS limit, broken electrical insulation |
| Major (A) | Defects that significantly affect product functionality or appearance | 0.65 | Non-functional mechanism, significant dimensional deviation (>5%), wrong product specifications |
| Major (B) | Defects that moderately affect product performance | 1.0 | Minor cosmetic imperfection on visible surface, packaging damage exposing product, incomplete accessories |
| Minor | Defects that do not affect functionality but deviate from specifications | 2.5 | Minor label misalignment, surface scratches not affecting performance, slight color variation |

### 2.5 Usage Decision Matrix

| Inspection Outcome | Usage Decision | Oracle Fusion Action | Next Steps |
|---|---|---|---|
| All samples pass (0 critical, ≤ AQL major, ≤ AQL minor) | Accept | Post goods receipt to approved subinventory | Normal putaway |
| Minor exceedances only, no critical/major | Conditional Accept | Post to approved subinventory with quality note | Supplier notification (informal), category review |
| Major defects exceed AQL | Reject | Move to quarantine subinventory, create NCR | Formal supplier notification, disposition decision within 5 days |
| Any critical defect found | Reject + Hold | Move to quarantine, create NCR, block supplier lot | Immediate category manager escalation, potential lot-by-lot inspection |
| Certification documents missing or invalid | Reject — Documentation | Hold at receiving dock, do not receive | Supplier has 10 business days to provide; after that, RTV |

### 2.6 Switching Rules for Inspection Levels

| Current Level | Condition for Switching | Target Level | Duration Before Review |
|---|---|---|---|
| Normal | 2+ rejections in 5 consecutive lots from same supplier | Tightened | Until 5 consecutive lots pass |
| Tightened | 5 consecutive lots pass with no critical defects | Normal | Immediate upon 5th pass |
| Normal | 10 consecutive lots pass, supplier quality score ≥ 90 | Reduced | Until a rejection occurs |
| Reduced | Any lot rejected | Normal | Immediate |
| Reduced | Supplier quality score drops below 80 | Normal | Immediate |

---

## 3. In-Store Quality Control

### 3.1 Shelf-Life Monitoring

Products with defined shelf life are monitored through Oracle Fusion Inventory Management lot tracking with expiry alerts.

| Product Category | Typical Shelf Life | Alert Trigger | Check Frequency | Action on Expiry |
|---|---|---|---|---|
| Paint (water-based) | 24 months from manufacture | 90 days before expiry | Monthly | Remove from shelf, markdown (if >60 days remaining) or dispose |
| Paint (oil-based) | 36 months from manufacture | 90 days before expiry | Monthly | Remove from shelf, markdown or dispose |
| Adhesives & Sealants | 12–18 months from manufacture | 60 days before expiry | Monthly | Remove from shelf, markdown or RTV |
| Chemical Cleaners & Solvents | 24 months from manufacture | 90 days before expiry | Monthly | Remove from shelf, markdown or dispose |
| PVC Cement & Primer | 12 months from opening, 24 months sealed | 60 days before expiry | Bi-weekly | Remove from shelf, dispose per DENR guidelines |
| Lubricants & Oils | 36 months from manufacture | 90 days before expiry | Quarterly | Markdown or RTV |
| Batteries (power tool) | 18 months from manufacture | 60 days before expiry | Monthly | Markdown, remove on expiry |
| Sealant Cartridges | 12 months from manufacture | 60 days before expiry | Monthly | Remove from shelf, RTV or dispose |
| Pesticides & Insecticides | 24 months from manufacture | 90 days before expiry | Monthly | Remove from shelf, dispose per DENR/FPA guidelines |
| Garden Seeds | 6–12 months (varies by variety) | 30 days before expiry | Bi-weekly during season | Remove from shelf, markdown or dispose |

### 3.2 Display Condition Checks

In-store quality associates perform systematic display condition checks using standardized checklists loaded on handheld devices integrated with Oracle Fusion Inventory Management.

| Check Type | Items Covered | Frequency | Responsible | Pass Criteria |
|---|---|---|---|---|
| Packaging Integrity | All displayed items | Daily (high-turn), Weekly (low-turn) | In-Store Quality Associate | No torn, crushed, or water-damaged packaging; labels legible |
| Price & Label Accuracy | All displayed items | Weekly | In-Store Quality Associate | Price matches POS system, required marks visible (PS, ICC) |
| Fixture & Display Safety | Shelving, hanging displays, demo units | Weekly | In-Store Quality Associate | No unstable stacks, safety chains on heavy items, demo units functional |
| Electrical Product Safety | Live demos, powered displays | Daily | Department Lead | All GFCIs functional, no exposed wiring, cords intact |
| Tool Condition | Display tools, demo units | Daily | Department Lead | Guards in place, no sharp exposed edges, safety instructions posted |
| Appliance Display | All floor model appliances | Daily | Appliances Lead | Units plugged in safely, no overheating, manuals accessible |
| Hazardous Material Storage | Chemicals, solvents, paints | Daily | Department Lead | Proper ventilation, spill containment, SDS sheets accessible, DENR-compliant storage |
| FIFO Compliance | All perishable/lot-tracked items | Weekly | In-Store Quality Associate | Oldest stock displayed first, rotation verified |

### 3.3 Damaged Goods Identification

| Damage Type | Identification Method | Flagging Action | Oracle Fusion Record |
|---|---|---|---|
| Customer-returned damaged | Return desk scan | Tag with damage code, move to QC staging | Create quality notification in PLM Quality |
| Transit damage (DC to store) | Receiving inspection | Photograph, log in receiving report | Receipt line rejection in Inventory Management |
| Shelf damage (in-store) | Daily shelf walk | Apply "Damaged — Do Not Sell" sticker | Update item status via cycle count adjustment |
| Water/humidity damage | Visual check during shelf walk | Remove from shelf immediately | Quality notification, subinventory transfer to damaged |
| Vermin/pest damage | Visual check | Remove, sanitize area | Quality notification, facility maintenance request |
| Tampering or suspected tampering | Visual check, broken seals | Remove immediately, quarantine | Quality notification, possible security alert |

### 3.4 In-Store Quality Check Schedule

| Day | Activity | Departments | Time Required |
|---|---|---|---|
| Monday | Packaging integrity walk (high-turn items) | Building Materials, Electrical, Plumbing | 2 hours |
| Tuesday | FIFO verification & shelf-life check | Paint, Chemicals, Adhesives | 1.5 hours |
| Wednesday | Electrical safety check & demo inspection | Electrical, Power Tools, Lighting | 2 hours |
| Thursday | Price & label accuracy audit | All departments (rotating 25%) | 2 hours |
| Friday | Appliance display check & hazardous material storage | Appliances, Chemicals | 1.5 hours |
| Saturday | Fixture safety & heavy item display check | Building Materials, Lumber | 1 hour |
| Sunday | Comprehensive damaged goods sweep | All departments | 1.5 hours |

---

## 4. Supplier Quality Management

### 4.1 Supplier Quality Scorecard

Supplier quality performance is measured quarterly through Oracle Fusion Supplier Management using the following weighted scorecard.

| KPI | Weight | Score Range | Data Source | Measurement |
|---|---|---|---|---|
| Incoming inspection pass rate | 30% | 0–100 | PLM Quality | (Lots accepted / Total lots inspected) × 100 |
| Critical defect incidence | 20% | 0–100 | PLM Quality | 100 − (Critical defects found × 25, min 0) |
| Documentation compliance (certs, marks) | 15% | 0–100 | PLM Quality / Compliance | (Complete docs / Total deliveries) × 100 |
| On-time delivery performance | 10% | 0–100 | Order Management | (On-time POs / Total POs) × 100 |
| Corrective action response timeliness | 10% | 0–100 | PLM Quality | (On-time CAR responses / Total CARs issued) × 100 |
| Customer complaint rate (quality-related) | 10% | 0–100 | Order Management / PLM Quality | 100 − (Complaints per 1,000 units sold × 10, min 0) |
| Recall / regulatory incident history | 5% | 0–100 | PLM Quality | 100 if no incidents in trailing 12 months; 0 if any |

**Total weighted score calculation:**
```
Supplier Quality Score = Σ (KPI Score × Weight)
```

### 4.2 Supplier Quality Tier Classification

| Tier | Score Range | Classification | Business Impact | Review Frequency |
|---|---|---|---|---|
| Platinum | 95–100 | Preferred Supplier | Priority for new SKU allocation, extended payment terms, reduced inspection (Reduced level) | Annual |
| Gold | 85–94 | Approved Supplier — Strong | Standard business relationship, Normal inspection | Semi-annual |
| Silver | 70–84 | Approved Supplier — Watch | Improvement plan required within 30 days, Normal inspection | Quarterly |
| Bronze | 50–69 | Conditional Approval | Formal corrective action plan, Tightened inspection, category manager review | Monthly |
| Probation | Below 50 | At Risk | All shipments on hold pending inspection, possible phase-out, executive review | Bi-weekly |

### 4.3 Quality-Related Claims Against Suppliers

| Claim Type | Trigger | SLA for Supplier Response | Escalation if No Response | Financial Recovery |
|---|---|---|---|---|
| Lot rejection — Major defects | Inspection rejection per Section 2.5 | 5 business days | Auto-debit from supplier account after 10 days | Cost of goods + inspection labor + disposition costs |
| Lot rejection — Critical defects | Critical defect found during inspection | 2 business days | Immediate lot hold, category manager escalation | Cost of goods + inspection + penalty per supplier agreement |
| Missing/invalid certification | Documentation failure per Section 2.5 | 10 business days | RTV initiated after deadline | Full refund + freight costs |
| In-store defect (supplier-caused) | Defect identified after receiving | 10 business days | Debit memo issued after 15 days | Cost + handling + markdown loss |
| Customer complaint (supplier-caused) | Quality complaint traced to supplier defect | 15 business days | Deduction from next payment | Full cost including customer compensation |
| Recall cost recovery | Recall triggered by supplier defect | Per recall agreement | Legal escalation | Full recall cost per contractual indemnification |

### 4.4 Supplier Corrective Action Request (SCAR) Process

| Stage | Activity | Responsible Party | SLA | Oracle Fusion Record |
|---|---|---|---|---|
| 1 | SCAR initiation (linked to NCR or complaint trend) | QA Manager — Central | Within 2 business days of triggering event | Create corrective action in PLM Quality |
| 2 | Root cause analysis request sent to supplier | Supplier Relations | Same day as SCAR creation | Notification in Supplier Management |
| 3 | Supplier acknowledgment | Supplier | 3 business days | Update corrective action status |
| 4 | Supplier root cause analysis submission | Supplier | 15 business days | Attach to corrective action record |
| 5 | Corrective action plan submission | Supplier | 20 business days | Attach to corrective action record |
| 6 | Tahanan Depot review of corrective action | QA Manager — Central | 5 business days | Approve or request revision |
| 7 | Corrective action implementation by supplier | Supplier | Per agreed timeline | Update implementation status |
| 8 | Verification inspection (next lot or audit) | Quality Inspector | Next shipment or within 30 days | Record verification result |
| 9 | SCAR closure | QA Manager — Central | After successful verification | Close corrective action |

### 4.5 Supplier Audit Program

| Audit Type | Frequency | Scope | Auditors | Reference |
|---|---|---|---|---|
| Initial qualification audit | Before first PO | Manufacturing process, quality system, certifications | QA Manager + Category Specialist | TD-SQ-010 Supplier Qualification Checklist |
| Routine quality audit | Annual (Gold+), Semi-annual (Silver and below) | Process capability, defect prevention, documentation | QA Manager + Compliance Officer | TD-SQ-020 Routine Audit Protocol |
| For-cause audit | Triggered by quality event | Specific defect area, corrective action effectiveness | QA Manager + relevant SME | TD-SQ-030 For-Cause Audit Protocol |
| Import supplier audit | Every 2 years or for-cause | Full facility tour, certifying body verification, social compliance | QA Manager + Import Specialist | TD-SQ-040 Import Supplier Audit Protocol |

---

## 5. Product Certification and Standards Compliance

### 5.1 Required Certifications by Product Category

The following table summarizes mandatory and voluntary certifications required for products sold at Tahanan Depot. Compliance is tracked in Oracle Fusion PLM Quality through item-level specification records.

| Product Category | PS Mark (BPS) Mandatory | ICC Certification | CE Marking (Imported) | SIR Mark (Structural) | Additional Requirements |
|---|---|---|---|---|---|
| Cement | Yes (PNS 63) | Yes | No | No | QPL listing required |
| Reinforcing Steel Bars | Yes (PNS 49) | Yes | No | Recommended | Mill test certificates per lot |
| Structural Steel | Yes (PNS 211) | Yes | No | Yes (for structural use) | Mill test certificates per lot |
| Electrical Wires & Cables | Yes (PNS 17) | Yes | No | No | Fire retardancy test report |
| Circuit Breakers | Yes (PNS 38) | Yes | Accepted (IEC equivalent) | No | Short-circuit test report |
| Electrical Outlets & Switches | Yes (PNS 189) | Yes | Accepted (IEC equivalent) | No | Insulation resistance test report |
| PVC Pipes (plumbing) | Yes (PNS 14) | Yes | No | No | Pressure test certificate |
| PVC Pipe Fittings | Yes (PNS 147) | Yes | No | No | Dimensional test report |
| Galvanized Iron Sheets | Yes (PNS 67) | Yes | No | Recommended | Zinc coating weight certificate |
| Plywood | Yes (PNS 595) | Yes | No | No | Formaldehyde emission test (E1 or better) |
| Paint (architectural) | Yes (PNS 244) | Yes | No | No | Lead-free certification, VOC compliance |
| Helmets (safety) | Yes (PNS 155) | Yes | Accepted (EN equivalent) | No | Impact test report per batch |
| Power Tools | Recommended | Yes | Yes (for EU-origin) | No | IEC 60745 test report |
| Home Appliances | Recommended | Yes | Yes (for EU-origin) | No | Energy label per DTI guidelines |
| Lighting Products | Recommended | Yes | Yes (for EU-origin) | No | Photometric test report |
| Water Pumps | Recommended | Yes | Accepted | No | Performance curve test report |
| Sanitary Ware (toilets, basins) | Recommended | Yes | No | No | Flush performance test, water efficiency |
| Lumber (treated) | Recommended | No | No | Recommended | Treatment certificate, moisture content |
| Fasteners | No (voluntary) | Yes | No | No | Mechanical property certificates |
| Chemicals (hazardous) | No | Yes | No | No | DENR registration, FDA notification (if applicable), SDS |
| Adhesives | Recommended | Yes | No | No | VOC compliance, bond test report |
| Tiles (ceramic) | Recommended | Yes | No | No | Slip resistance test, water absorption test |
| Door Locks & Hardware | Recommended | Yes | No | No | Security grade test report |
| Garden Equipment (powered) | Recommended | Yes | Yes (for EU-origin) | No | Emission compliance (if gasoline) |
| Solar Panels | Recommended | Yes | Yes | No | IEC 61215 / IEC 61730 certification |

### 5.2 Philippine Product Standards (PS) Mark Verification

| Verification Point | Responsible | Method | Frequency | Non-Compliance Action |
|---|---|---|---|---|
| Initial supplier qualification | Compliance Officer | Visual verification of PS mark on samples + BPS QPL database check | Per new supplier/item | Reject supplier/item until PS mark obtained |
| Incoming inspection | Quality Inspector | Visual check on every sampled unit | Every inspection lot | Reject lot, initiate NCR |
| In-store shelf check | In-Store Quality Associate | Spot-check during label accuracy audit | Weekly (rotating) | Remove from shelf, notify QA Manager |
| Customer complaint verification | Quality Data Analyst | Cross-reference complaint item against QPL | Per complaint | Escalate to Compliance Officer if PS mark absent |
| BPS QPL renewal monitoring | Compliance Officer | Quarterly review of BPS QPL database for expiring certifications | Quarterly | Notify supplier 90 days before expiry; suspend PO if lapsed |

### 5.3 Import Certification Compliance

| Requirement | Regulatory Body | Application | Validity | Responsibility |
|---|---|---|---|---|
| Import Commodity Clearance (ICC) | DTI-BPS | All imported products under mandatory certification | Per shipment (ICC sticker) or annual (ICC certificate) | Import Specialist + Compliance Officer |
| FDA Notification/Certificate of Registration | FDA | Health-related products, water contact materials, certain chemicals | 1–5 years depending on product | Compliance Officer |
| DENR Environmental Compliance | DENR-EMB | Hazardous materials, ozone-depleting substances, toxic chemicals | Per product registration | Compliance Officer |
| Philippine Mechanical Engineering Code compliance | DOLE-BWC | Pressure vessels, boilers, lifting equipment | Per installation | Compliance Officer + Facilities |
| Energy Labeling Program compliance | DTI-BPS | Air conditioners, refrigerators, lighting, motors | Per model, annual renewal | Category Manager + Compliance |

### 5.4 Certification Documentation Requirements

| Document | Required For | Retention Period | Storage Location | Oracle Fusion Record |
|---|---|---|---|---|
| PS License copy | All PS-marked products | Duration of license + 3 years | Compliance shared drive + PLM Quality | Attach to supplier qualification |
| ICC Certificate/Sticker log | All imported products | 5 years | Compliance shared drive + PLM Quality | Attach to item specification |
| Test reports (per PNS) | All certified products | 5 years | Compliance shared drive | Attach to quality plan |
| Mill test certificates | Steel, cement | 10 years | Compliance shared drive | Attach to inspection lot |
| SDS (Safety Data Sheets) | All hazardous chemicals | Duration of use + 30 years | Compliance shared drive + in-store SDS binder | Attach to item specification |
| FDA registration | Applicable products | Duration of registration + 3 years | Compliance shared drive | Attach to item specification |
| DENR registration | Hazardous materials | Duration of registration + 5 years | Compliance shared drive | Attach to item specification |
| Energy label certificate | Appliances, lighting | Duration of model listing | Compliance shared drive | Attach to item specification |

---

## 6. Defective Product Handling

### 6.1 Defective Product Identification and Segregation

| Source | Identification Method | Segregation Action | Oracle Fusion Process |
|---|---|---|---|
| Incoming inspection rejection | Inspector usage decision | Move to quarantine subinventory (DC) | Quality lot rejection → subinventory transfer |
| In-store shelf check | Associate visual inspection | Apply "Damaged — Do Not Sell" tag, move to backroom QC staging | Cycle count adjustment → quality notification |
| Customer return (quality-related) | Return desk classification per POL-RET-001 | Tag with defect code, move to QC staging | Create return with quality notification in Order Management |
| DC storage damage | Cycle count or visual inspection | Move to quarantine subinventory | Quality notification in PLM Quality |
| Transit damage (store delivery) | Store receiving check | Log on delivery receipt, photograph, move to QC staging | Receipt line rejection in Inventory Management |
| Regulatory hold | Compliance Officer directive | Immediate quarantine, seal area | Quality hold in PLM Quality, subinventory transfer |

### 6.2 Disposition Workflow

| Stage | Activity | Responsible | SLA | Oracle Fusion Action |
|---|---|---|---|---|
| 1 | Defective item logged in QC staging | In-Store Quality Associate / DC Inspector | Same day as identification | Create quality notification |
| 2 | Defect classification (Critical / Major / Minor) | Quality Inspector | Within 24 hours | Update quality notification with defect code |
| 3 | Root cause preliminary assessment | Quality Inspector | Within 48 hours | Record preliminary assessment |
| 4 | Disposition recommendation | QA Supervisor | Within 3 business days | Propose disposition in quality notification |
| 5 | Disposition approval | QA Manager (≤ ₱50,000) / Director, QA (> ₱50,000) | Within 2 business days of recommendation | Approve disposition |
| 6 | Disposition execution | DC Operations / Store Operations | Within 5 business days of approval | Execute per approved disposition |

### 6.3 Disposition Options

| Disposition Code | Description | When Used | Financial Treatment | Accounting Reference |
|---|---|---|---|---|
| RTV-01 | Return to vendor — Full credit | Supplier-caused defect, within RTV window (per POL-RET-001) | Debit memo to supplier, inventory relieved | Accounts receivable debit memo |
| RTV-02 | Return to vendor — Partial credit | Supplier-caused defect, partial recovery negotiated | Negotiated debit memo | Accounts receivable debit memo |
| SCRAP-01 | Dispose / scrap | No salvage value, hazardous, or not cost-effective to return | Write-off to shrinkage/damage expense | Inventory write-off journal |
| MKDN-01 | Markdown and sell as-is | Functional but cosmetic defect, customer safety not affected | Reduce retail price, sell from designated area | Inventory revaluation |
| DONATE-01 | Donate to qualified institution | Functional but unsellable through normal channels, safe for use | Charitable donation (tax-deductible per BIR rules) | Donation receipt, inventory relief |
| REWORK-01 | Repair / rework to sellable condition | Defect correctable with minor work | Charge rework cost to supplier or internal | Inventory adjustment, cost capture |
| HAZD-01 | Hazardous waste disposal | Hazardous material, no salvage, regulatory disposal required | Disposal cost + environmental fee | Expense, DENR documentation |

### 6.4 Write-Off Authorization Matrix

| Write-Off Value | Approver | Reporting | Documentation Required |
|---|---|---|---|
| ≤ ₱5,000 per incident | Store Manager | Monthly consolidation to Director, QA | Quality notification + photographs |
| ₱5,001 – ₱25,000 per incident | QA Manager | Monthly consolidation to Director, QA | Quality notification + photographs + root cause summary |
| ₱25,001 – ₱100,000 per incident | Director, QA | Quarterly report to Executive Quality Council | Full NCR + root cause analysis + photographs |
| ₱100,001 – ₱500,000 per incident | VP Merchandising & QA | Quarterly report to Executive Quality Council | Full NCR + CAR issued + financial impact analysis |
| > ₱500,000 per incident | COO | Immediate report to Executive Quality Council | Full investigation + supplier claim + corrective action plan |

---

## 7. Product Recall Procedures

### 7.1 Recall Classification

| Class | Risk Level | Definition | Examples | Response Time |
|---|---|---|---|---|
| Class I — Urgent | Immediate safety hazard | Product defect that could cause serious injury or death | Electrical product with electrocution risk, structural component with load failure risk, hazardous chemical with incorrect labeling | Within 24 hours |
| Class II — Priority | Potential safety hazard | Product defect that could cause injury under certain conditions | Power tool with malfunctioning safety guard, paint with undeclared hazardous substance above limit | Within 48 hours |
| Class III — Precautionary | Quality / compliance issue | Product defect not posing safety risk but failing quality or regulatory standards | Appliance with incorrect energy label, tile with incorrect slip rating, hardware with incorrect load rating | Within 5 business days |
| Voluntary | Market withdrawal | Non-safety quality issue, customer satisfaction initiative | Cosmetic defect, minor specification variance, packaging error | Within 10 business days |

### 7.2 Recall Notification Process

| Stage | Activity | Responsible | SLA | Oracle Fusion Action |
|---|---|---|---|---|
| 1 | Recall trigger identified (internal QC, supplier notification, DTI directive, customer reports) | Any employee (report to QA Manager) | Immediate | Create recall case in PLM Quality |
| 2 | Risk assessment and classification | Director, QA + Compliance Officer | Within 4 hours (Class I), 8 hours (Class II), 24 hours (Class III) | Update recall case with classification |
| 3 | Executive approval for recall | VP Merchandising & QA (Class III/Voluntary), COO (Class I/II) | Within 2 hours of classification | Approve recall case |
| 4 | Inventory hold — all DCs and stores | DC Operations + Store Operations | Within 4 hours of approval | Apply inventory hold in Inventory Management |
| 5 | Traceability query — identify affected lots, stores, customers | Quality Data Analyst | Within 8 hours of approval | Run traceability query in PLM Quality / Inventory Management |
| 6 | Supplier notification | Supplier Relations | Within 4 hours of hold | Supplier notification in Supplier Management |
| 7 | Store communication and action plan | Regional Quality Supervisors | Within 12 hours (Class I/II), 24 hours (Class III) | Oracle Fusion notification to all affected stores |
| 8 | Customer notification (if direct customer data available) | Marketing + Customer Service | Within 24 hours (Class I), 48 hours (Class II) | Customer notification via Order Management contact records |
| 9 | Public notification (Class I/II) | Marketing + Legal | Within 24 hours (Class I), 48 hours (Class II) | N/A (external communication) |
| 10 | Regulatory reporting to DTI-BPS | Compliance Officer | Within 24 hours (Class I), 48 hours (Class II), 5 days (Class III) | DTI notification per DAO requirements |
| 11 | Affected product collection / quarantine | DC Operations + Store Operations | Per recall timeline | Subinventory transfer to recall quarantine |
| 12 | Recall effectiveness check | QA Manager | 30 days after initiation | Review recovery rate in PLM Quality |
| 13 | Recall closure | Director, QA | After effectiveness check passes | Close recall case |

### 7.3 Regulatory Reporting Requirements

| Regulatory Body | When Required | Report Content | Submission Deadline | Format |
|---|---|---|---|---|
| DTI-BPS | All recalls involving PS-marked or mandatory-certified products | Product description, defect description, affected quantities, consumer advisory, corrective action | Within 24 hours (safety), 72 hours (others) | DTI Consumer Welfare Division prescribed form + supporting documents |
| FDA | Recalls involving FDA-notified products | Product name, registration number, defect, affected lots, health advisory | Within 24 hours | FDA Post-Marketing Surveillance report form |
| DENR-EMB | Recalls involving hazardous/regulated chemicals | Chemical identity, quantity, environmental risk, disposal plan | Within 48 hours | DENR incident report format |
| DOLE-BWC | Recalls affecting workplace safety equipment | Product identification, defect, affected workers if any | Within 48 hours | DOLE incident notification |
| LGU (Local Government Unit) | If required by local ordinance | As prescribed by LGU | Per local requirement | Per local format |

### 7.4 Customer Communication Templates

| Recall Class | Channel | Template | Message Tone |
|---|---|---|---|
| Class I | SMS + Email + In-store signage + Social media + Press release | TD-RC-001 (Urgent Safety Recall) | Direct, urgent, clear safety instructions |
| Class II | Email + In-store signage + Social media | TD-RC-002 (Safety Recall) | Clear, informative, action-oriented |
| Class III | Email + In-store signage | TD-RC-003 (Quality Recall) | Informative, reassuring |
| Voluntary | In-store signage + Website | TD-RC-004 (Voluntary Withdrawal) | Transparent, customer-friendly |

### 7.5 Recall Escalation Matrix

| Situation | Escalation To | Timeframe | Action |
|---|---|---|---|
| Supplier unresponsive to recall notification | VP Merchandising & QA | 24 hours after initial contact | Direct executive-to-executive contact, consider legal action |
| Recovery rate below 70% after 30 days | Executive Quality Council | At 30-day review | Extend recall communication, consider expanded public notice |
| DTI requests additional information | Compliance Officer | Per DTI deadline | Compile and submit requested data |
| Media inquiry about recall | Corporate Communications / Legal | Immediate | Follow TD media relations policy, use approved statements only |
| Customer injury reported | COO + Legal | Immediate | Activate incident response protocol, preserve evidence |

---

## 8. Customer Quality Complaints

### 8.1 Quality Complaint Handling Process

All quality-related customer complaints are tracked through Oracle Fusion Order Management (for return/replacement) and PLM Quality (for investigation and corrective action), in accordance with POL-RET-001 Returns Policy.

| Stage | Activity | Responsible | SLA | Oracle Fusion Record |
|---|---|---|---|---|
| 1 | Complaint receipt (in-store, call center, email, social media) | Customer Service Associate | Immediate | Create service request in Order Management |
| 2 | Complaint classification | Customer Service Lead | Within 1 hour | Classify as quality, non-quality, or mixed |
| 3 | Immediate customer resolution | Store Manager / Customer Service Lead | Within 4 hours (in-store), 24 hours (remote) | Process return/replacement per POL-RET-001 |
| 4 | Quality notification creation | Quality Data Analyst | Within 1 business day | Create quality notification in PLM Quality, link to service request |
| 5 | Product retrieval (if applicable) | In-Store Quality Associate | Within 2 business days | Receive returned product into QC staging |
| 6 | Defect verification | Quality Inspector | Within 3 business days | Inspect returned product, record findings |
| 7 | Investigation and root cause analysis | QA Supervisor | Within 5 business days | Complete investigation, record in quality notification |
| 8 | Corrective action determination | QA Manager | Within 7 business days | Define corrective action |
| 9 | Customer follow-up | Customer Service Lead | Within 10 business days | Confirm resolution satisfaction |
| 10 | Quality notification closure | QA Manager | After corrective action verified | Close quality notification |

### 8.2 Complaint Classification Matrix

| Classification Code | Description | Examples | Priority | Investigation Level |
|---|---|---|---|---|
| QC-SAFETY | Product safety concern | Electrical shock, fire risk, chemical exposure, structural failure | Critical | Full investigation + regulatory review |
| QC-PERF | Product performance failure | Tool breaks under normal use, pump fails, paint peels prematurely | High | Full inspection + root cause analysis |
| QC-DIM | Dimensional / specification issue | Wrong size, doesn't fit standard, threads don't match | High | Measurement verification + supplier review |
| QC-COMP | Completeness issue | Missing parts, incomplete set, wrong item in package | Medium | Documentation + supplier notification |
| QC-APPEARANCE | Cosmetic defect | Wrong color, surface defects, packaging damage | Medium | Inspection + supplier notification |
| QC-CERT | Missing or incorrect certification | No PS mark, expired ICC, wrong energy label | Critical | Immediate compliance investigation |
| QC-LABEL | Labeling accuracy | Wrong specifications on label, missing safety warnings | High | Label review + supplier correction |
| QC-DURABILITY | Premature wear or degradation | Rust within warranty, premature fading, seal failure | High | Product testing + supplier analysis |

### 8.3 Root Cause Analysis Framework

| Method | When Used | Tools | Output |
|---|---|---|---|
| 5-Why Analysis | Single defect, straightforward cause | 5-Why template in PLM Quality | Root cause statement |
| Fishbone (Ishikawa) Diagram | Multiple possible causes, complex defect | Fishbone template, cross-functional team | Prioritized cause list |
| 8D Problem Solving | Recurring defects, customer safety issues | 8D template in PLM Quality | Full 8D report with corrective actions |
| Pareto Analysis | Category-level complaint trends | Oracle Fusion PLM Quality analytics | Top defect types by frequency |
| Failure Mode and Effects Analysis (FMEA) | New product introduction, design change | FMEA template | Risk priority numbers, prevention actions |

### 8.4 Corrective and Preventive Action (CAPA)

| CAPA Type | Trigger | Approval | Implementation SLA | Verification |
|---|---|---|---|---|
| Immediate corrective action | Any quality complaint | QA Supervisor | Within 48 hours | Next inspection lot |
| Short-term corrective action | Recurring defect (3+ complaints same SKU/root cause in 30 days) | QA Manager | Within 15 business days | Next 5 inspection lots |
| Long-term preventive action | Systemic issue or category trend | Director, QA | Within 30 business days | Quarterly review for 2 quarters |
| Supplier CAPA (SCAR) | Supplier-caused defect confirmed | QA Manager | Per SCAR process (Section 4.4) | Per SCAR verification |
| Process CAPA | Internal process failure | QA Manager + affected process owner | Within 20 business days | Process audit within 30 days |

---

## 9. Quality Metrics and Reporting

### 9.1 Key Quality Performance Indicators

| KPI | Definition | Calculation | Target (FY2026) | Reporting Frequency | Oracle Fusion Source |
|---|---|---|---|---|---|
| Incoming Inspection Pass Rate | Percentage of inspection lots accepted | (Accepted lots / Total lots) × 100 | ≥ 97.5% | Monthly | PLM Quality |
| Defect Rate (Incoming) | Defective units per 10,000 units inspected | (Defective units / Total inspected) × 10,000 | ≤ 85 DPMO | Monthly | PLM Quality |
| Critical Defect Rate | Critical defects per 10,000 units inspected | (Critical defective units / Total inspected) × 10,000 | 0 | Monthly | PLM Quality |
| In-Store Defect Identification Rate | Percentage of defects caught before customer finds them | (Internally identified / Total identified) × 100 | ≥ 95% | Quarterly | PLM Quality + Inventory Management |
| Customer Quality Complaint Rate | Quality complaints per 10,000 transactions | (Quality complaints / Total transactions) × 10,000 | ≤ 12 | Monthly | Order Management |
| Return Rate — Quality-Related | Quality returns as percentage of total sales (units) | (Quality returns / Total units sold) × 100 | ≤ 0.8% | Monthly | Order Management |
| Average Complaint Resolution Time | Business days from complaint to closure | Average days across all complaints | ≤ 5 days | Monthly | PLM Quality |
| Supplier Quality Score (weighted avg) | Average supplier quality scorecard result | Σ (Score × Spend Weight) / Total Spend | ≥ 85 | Quarterly | Supplier Management |
| Certification Compliance Rate | Percentage of SKUs with current required certifications | (Compliant SKUs / Required-cert SKUs) × 100 | 100% | Monthly | PLM Quality |
| Shelf-Life Compliance Rate | Percentage of shelf-life items removed before expiry | (Proactive removals / Total removals) × 100 | ≥ 98% | Monthly | Inventory Management |
| Write-Off Rate (Quality) | Quality-related write-offs as percentage of COGS | (Quality write-offs / Total COGS) × 100 | ≤ 0.4% | Monthly | Inventory Management |
| SCAR Closure Rate | Percentage of SCARs closed within agreed timeline | (On-time closures / Total SCARs) × 100 | ≥ 90% | Quarterly | PLM Quality |
| Recall Effectiveness Rate | Recovery rate for executed recalls | (Recovered units / Affected units) × 100 | ≥ 80% | Per recall | PLM Quality |

### 9.2 Defect Rate Targets by Product Category

| Product Category | Incoming Defect Rate Target (DPMO) | Customer Complaint Rate Target (per 10K transactions) | Return Rate Target (%) |
|---|---|---|---|
| Cement & Concrete Products | ≤ 50 | ≤ 8 | ≤ 0.3 |
| Structural Steel & Rebar | ≤ 40 | ≤ 6 | ≤ 0.2 |
| Electrical Wiring & Cables | ≤ 30 | ≤ 5 | ≤ 0.2 |
| Electrical Fixtures & Fittings | ≤ 60 | ≤ 10 | ≤ 0.5 |
| Circuit Breakers & Protection | ≤ 20 | ≤ 4 | ≤ 0.2 |
| Plumbing Pipes & Fittings | ≤ 55 | ≤ 8 | ≤ 0.4 |
| Plumbing Fixtures | ≤ 65 | ≤ 10 | ≤ 0.5 |
| Paint & Coatings | ≤ 45 | ≤ 7 | ≤ 0.4 |
| Adhesives & Sealants | ≤ 50 | ≤ 6 | ≤ 0.3 |
| Hand Tools | ≤ 70 | ≤ 12 | ≤ 0.6 |
| Power Tools | ≤ 55 | ≤ 10 | ≤ 0.5 |
| Safety Equipment (PPE) | ≤ 15 | ≤ 3 | ≤ 0.1 |
| Lumber & Plywood | ≤ 80 | ≤ 12 | ≤ 0.7 |
| Home Appliances (Major) | ≤ 50 | ≤ 10 | ≤ 0.5 |
| Home Appliances (Small) | ≤ 60 | ≤ 10 | ≤ 0.5 |
| Lighting Products | ≤ 55 | ≤ 9 | ≤ 0.5 |
| Chemicals | ≤ 25 | ≤ 5 | ≤ 0.2 |
| Fasteners | ≤ 90 | ≤ 15 | ≤ 0.8 |

### 9.3 Oracle Fusion Quality Dashboards

| Dashboard | Audience | Content | Refresh Frequency | Access |
|---|---|---|---|---|
| Executive Quality Summary | Executive Quality Council | KPI summary, trend charts, recall status, top defect categories | Daily | VP+ role |
| Incoming Inspection Performance | QA Manager — Central | Inspection pass/fail rates, defect Pareto, supplier performance | Real-time | QA Manager role |
| Supplier Quality Scorecard | Supplier Relations, Category Managers | Supplier scores, trend, SCAR status | Weekly | Supplier Management role |
| In-Store Quality Dashboard | QA Manager — Retail, Regional QS | Shelf-life alerts, damage rates, complaint hot spots | Daily | Retail QA role |
| Compliance Tracker | Compliance Officer | Certification expiry, regulatory deadlines, audit schedule | Daily | Compliance role |
| Customer Quality Complaints | Customer Service, QA | Complaint volume, category, resolution time, root cause | Daily | CS Manager + QA role |
| Recall Management | Director, QA | Active recalls, recovery rates, regulatory status | Real-time during recall, otherwise weekly | QA Director role |

### 9.4 Reporting Schedule

| Report | Audience | Frequency | Prepared By | Distribution |
|---|---|---|---|---|
| Daily Quality Digest | QA Managers, DC Managers | Daily (automated) | Oracle Fusion automated report | Email distribution list |
| Weekly Quality Summary | Director, QA, Category Managers | Every Monday | Quality Data Analyst | Email + shared drive |
| Monthly Quality Review | Quality Review Board | First Thursday of month | QA Manager — Central + Retail | Meeting presentation + shared drive |
| Quarterly Supplier Quality Report | VP Merchandising & QA, Supplier Relations | End of quarter | QA Manager — Central | Formal report + Quality Review Board presentation |
| Annual Quality Performance Report | Executive Quality Council, Board | January (following year) | Director, QA | Formal report + Executive Quality Council presentation |
| Regulatory Compliance Report | Director, QA, Legal | Monthly | Compliance Officer | Confidential distribution |

### 9.5 Recall History Log

All product recalls executed by Tahanan Depot are logged with the following fields.

| Field | Description | Example |
|---|---|---|
| Recall ID | Unique identifier (TD-RC-YYYY-NNN) | TD-RC-2025-003 |
| Recall Class | I, II, III, or Voluntary | Class II |
| Product Name | Product description | 1,000W Electric Angle Grinder TD-AG1000 |
| SKU | Internal SKU number | EL-PT-88742 |
| Supplier | Supplier name and code | Jiangsu Power Tools Co. (SUP-IMP-0245) |
| Defect Description | Nature of the defect | Safety guard may detach during operation |
| Affected Quantity | Units in market / units recovered | 2,400 / 1,920 (80%) |
| Affected Stores | Number of stores carrying the product | 38 stores (Luzon, Visayas) |
| Initiation Date | Date recall was initiated | August 15, 2025 |
| Closure Date | Date recall was closed | September 30, 2025 |
| Regulatory Notification | DTI, FDA, DENR as applicable | DTI-BPS notified August 16, 2025 |
| Root Cause | Determined cause | Supplier changed guard mounting screw specification without approval |
| Corrective Action | Action taken to prevent recurrence | Supplier reverted specification, added torque check on line, Tahanan Depot added guard pull test to incoming inspection |
| Total Cost | Direct cost of recall | ₱4,200,000 |

---

## 10. Quality Training

### 10.1 Training Program Overview

| Program | Target Audience | Duration | Frequency | Delivery Method | Certification |
|---|---|---|---|---|---|
| Quality Management Fundamentals | All new hires (quality-related roles) | 8 hours | Upon hiring | Classroom + e-learning | Internal certificate |
| Incoming Inspection Procedures | DC Quality Inspectors | 24 hours (3 days) | Upon hiring + annual refresher | Classroom + hands-on | TD-QI-Inspector certification |
| Import Inspection & Certification | Import Quality Inspectors | 16 hours | Upon hiring + annual refresher | Classroom + workshop | TD-QI-Import certification |
| In-Store Quality Control | In-Store Quality Associates | 8 hours | Upon hiring + semi-annual refresher | Classroom + on-floor practice | Internal certificate |
| Product Knowledge — Building Materials | Building Materials inspectors and associates | 16 hours | Upon hiring + annual refresher | Classroom + product lab | Category certificate |
| Product Knowledge — Electrical | Electrical inspectors and associates | 16 hours | Upon hiring + annual refresher | Classroom + product lab | Category certificate |
| Product Knowledge — Plumbing | Plumbing inspectors and associates | 12 hours | Upon hiring + annual refresher | Classroom + product lab | Category certificate |
| Product Knowledge — Paint & Chemicals | Paint/chemical inspectors and associates | 12 hours | Upon hiring + annual refresher | Classroom + SDS review | Category certificate |
| Product Knowledge — Tools & Appliances | Tools/appliance inspectors and associates | 12 hours | Upon hiring + annual refresher | Classroom + product lab | Category certificate |
| Oracle Fusion PLM Quality Operations | QA Managers, Supervisors, Data Analysts | 16 hours | Upon system update or role change | Oracle-approved training partner | Oracle Fusion user certificate |
| Oracle Fusion Quality for Inspectors | Quality Inspectors | 8 hours | Upon hiring + system update | Internal IT training | Internal certificate |
| Root Cause Analysis & CAPA | QA Managers, Supervisors, Inspectors | 8 hours | Annual | Workshop with case studies | Internal certificate |
| Regulatory Compliance (Philippine Standards) | Compliance Officer, QA Managers, Category Managers | 8 hours | Annual + regulatory update | Classroom with BPS guest speaker | Internal certificate |
| Hazardous Materials Handling | DC staff handling chemicals, paint, solvents | 4 hours | Annual | Classroom + practical drill | DENR-compliant certificate |
| Recall Procedure Drill | All quality-involved personnel | 2 hours | Semi-annual | Tabletop exercise | Participation record |

### 10.2 Inspector Certification Requirements

All Tahanan Depot Quality Inspectors must hold the following certifications before independently performing inspections.

| Requirement | DC Inspector | Import Inspector | In-Store QA Associate | Renewal |
|---|---|---|---|---|
| TD-QI-Inspector (internal) | Required | Required | N/A | Annual |
| TD-QI-Import (internal) | N/A | Required | N/A | Annual |
| Category product knowledge (relevant category) | Required (assigned category) | Required (all import categories) | Required (assigned department) | Annual |
| Oracle Fusion Quality for Inspectors | Required | Required | Required | Upon system update |
| Hazardous materials awareness | Required (if handling chemicals) | Required | Required (if in chemicals/paint) | Annual |
| First aid / basic safety | Required | Required | Recommended | Annual (per DOLE requirement) |
| DTI-BPS Product Standards Awareness | Required | Required | Recommended | Annual |

### 10.3 Inspector Competency Assessment

| Assessment Type | Frequency | Passing Score | Remediation | Oracle Fusion Record |
|---|---|---|---|---|
| Written knowledge test | Annual | 80% | Retake within 30 days; if fail again, retraining required | HR system |
| Practical inspection test (blind sample) | Semi-annual | 90% (no critical misses) | Retrain and retest within 15 days | PLM Quality — inspector qualification |
| Audit of inspection records | Quarterly | ≤ 2% error rate | Coaching session + retraining if > 2% | PLM Quality — audit trail |
| Inter-inspector correlation | Semi-annual | ≥ 90% agreement | Retrain on discrepant characteristics | PLM Quality — measurement system analysis |
| Speed and throughput assessment | Annual | Meet or exceed standard times per category | Process coaching | HR system |

### 10.4 Training Records and Compliance

| Record | Retention | Storage | Access | Oracle Fusion Touchpoint |
|---|---|---|---|---|
| Training attendance logs | 5 years | HR system | HR + direct manager | N/A |
| Certification records | Duration of employment + 3 years | HR system + PLM Quality | HR + QA Manager | Inspector qualification in PLM Quality |
| Competency assessment results | 3 years | HR system + PLM Quality | HR + QA Manager | Inspector qualification update |
| Training needs analysis | 2 years | HR system | HR + QA Manager | N/A |
| External training certificates | Duration of employment + 3 years | HR system | HR + employee | N/A |

### 10.5 Annual Training Calendar

| Quarter | Focus Areas | Target Audience | Estimated Hours/Person |
|---|---|---|---|
| Q1 (Jan–Mar) | Annual refresher — Inspection procedures, Regulatory compliance update | All inspectors, QA Managers | 12–16 |
| Q2 (Apr–Jun) | Category deep dives (Building Materials, Electrical), Root cause analysis workshop | Category-specific inspectors, QA Supervisors | 8–12 |
| Q3 (Jul–Sep) | Category deep dives (Plumbing, Paint/Chemicals, Tools), Oracle Fusion system update training | Category-specific inspectors, All quality staff | 8–12 |
| Q4 (Oct–Dec) | Hazardous materials handling, Recall drill, Competency assessments, Next-year training planning | All quality staff | 6–8 |

### 10.6 Training Effectiveness Measurement

| Metric | Measurement Method | Target | Frequency |
|---|---|---|---|
| Training completion rate | Attendance logs vs. required audience | 100% | Quarterly |
| Knowledge retention (post-test vs. pre-test) | Written test scores | ≥ 20% improvement | Annual |
| Inspection accuracy improvement | Defect miss rate before and after training | ≥ 10% reduction in miss rate | Semi-annual |
| Time-to-competency for new inspectors | Weeks from hire to independent inspection | ≤ 6 weeks | Per new hire |
| Employee satisfaction with training | Post-training survey (1–5 scale) | ≥ 4.0 | Per training event |
| CAPA effectiveness linked to training | % of CAPAs where training was corrective action and no recurrence | ≥ 90% | Annual |

---

## Appendix A: Quality Code Reference

| Code | Description | Section Reference |
|---|---|---|
| TD-QS-001 | Quality Management Framework Manual | Section 1 |
| TD-QS-010 | Incoming Inspection Standard Operating Procedure | Section 2 |
| TD-QS-020 | In-Store Quality Control Checklist | Section 3 |
| TD-QS-030 | Supplier Quality Management Procedure | Section 4 |
| TD-QS-040 | Product Certification Compliance Matrix | Section 5 |
| TD-QS-050 | Defective Product Handling and Disposition SOP | Section 6 |
| TD-QS-060 | Product Recall Procedure | Section 7 |
| TD-QS-070 | Customer Quality Complaint Handling SOP | Section 8 |
| TD-QS-080 | Quality Metrics and Reporting Standard | Section 9 |
| TD-QS-090 | Quality Training Program Guide | Section 10 |
| POL-SCM-002 | Supplier Management Policy | Sections 4, 5 |
| POL-RET-001 | Returns Policy | Sections 6, 8 |

## Appendix B: Philippine Regulatory Reference

| Regulation / Standard | Issuing Body | Applicability | Key Requirement |
|---|---|---|---|
| Republic Act 7394 (Consumer Act of the Philippines) | Congress / DTI | All consumer products | Product safety, labeling, warranties, recall provisions |
| DAO 2024-03 (Product Standards Enforcement) | DTI-BPS | Mandatory certified products | PS/ICC mark requirements, surveillance, penalties |
| PNS Series (various by product) | DTI-BPS / PNS Technical Committees | Product-specific | Technical specifications and test methods |
| DENR DAO 2016-08 (Toxic Chemicals) | DENR-EMB | Hazardous chemicals | Registration, SDS, labeling, storage requirements |
| FDA AO 2014-0030 | FDA | Health-related products | Product registration, labeling, post-market surveillance |
| DO (Department Order) series on product safety | DTI | Consumer products | Safety standards, certification, market surveillance |
| Philippine Energy Labeling Program (PELP) | DTI-BPS / DOE | Appliances, lighting, motors | Energy efficiency labeling requirements |
| Republic Act 9003 (Ecological Solid Waste Management) | DENR | Product disposal | Proper disposal of defective/damaged goods |
| DOLE Department Order 198-18 | DOLE-BWC | Occupational safety | Workplace safety standards, PPE requirements |
| Bureau of Philippine Standards QPL | DTI-BPS | All PS-marked products | Qualified supplier listing, license validity |

## Appendix C: Glossary

| Term | Definition |
|---|---|
| AQL | Acceptable Quality Level — maximum defect rate considered acceptable for sampling inspection |
| BPS | Bureau of Philippine Standards — DTI agency responsible for product standards |
| CAPA | Corrective and Preventive Action |
| CAR | Corrective Action Request |
| CE | Conformité Européenne — European conformity marking |
| DPMO | Defects Per Million Opportunities |
| DTI | Department of Trade and Industry |
| FIFO | First In, First Out — inventory rotation method |
| ICC | Import Commodity Clearance — DTI certification for imported products |
| NCR | Nonconformance Report |
| PELP | Philippine Energy Labeling Program |
| PLM | Product Lifecycle Management |
| PNS | Philippine National Standard |
| PS | Philippine Standard (mark) — BPS product quality certification mark |
| QPL | Qualified Products List — BPS list of certified products/suppliers |
| RTV | Return to Vendor |
| SCAR | Supplier Corrective Action Request |
| SDS | Safety Data Sheet |
| SIR | Structural Inspection Report — mark for structural steel compliance |
| SKU | Stock Keeping Unit |

---

**End of Document TD-OPS-021 — Quality Management**
**© 2026 Tahanan Depot Inc. — All Rights Reserved**
**Unauthorized reproduction or distribution of this document is prohibited.**
