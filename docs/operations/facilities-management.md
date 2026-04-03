# Tahanan Depot Facilities Management

**Document ID:** TD-OPS-018
**Classification:** Internal — Confidential
**Owner:** Tahanan Property, Inc. (Facilities Management Division)
**Effective Date:** January 1, 2026
**Review Cycle:** Annual (next review: January 2027)
**Approved By:** Maria Consuelo A. Reyes, VP — Facilities & Property Management

---

## Table of Contents

1. [Facilities Management Overview](#1-facilities-management-overview)
2. [Building Maintenance Standards](#2-building-maintenance-standards)
3. [Reactive Maintenance Process](#3-reactive-maintenance-process)
4. [Lease Management](#4-lease-management)
5. [Energy Management](#5-energy-management)
6. [Safety and Compliance](#6-safety-and-compliance)
7. [Janitorial and Cleaning Standards](#7-janitorial-and-cleaning-standards)
8. [Pest Control Management](#8-pest-control-management)
9. [Renovation and Capital Improvement Projects](#9-renovation-and-capital-improvement-projects)
10. [Environmental Management](#10-environmental-management)
11. [Facility Performance Metrics](#11-facility-performance-metrics)
12. [Store Closure and Relocation](#12-store-closure-and-relocation)

---

## 1. Facilities Management Overview

### 1.1 Scope

Tahanan Property, Inc. (TPI) is the real estate and facilities management arm of the Tahanan Depot group. TPI owns, leases, and manages all physical assets used by Tahanan Depot, Inc. (TDI) for retail operations. This document governs the end-to-end facilities management practices across the following portfolio:

| Asset Category | Count | Size Range (sqm) | Total Area (sqm) | Ownership |
|---|---|---|---|---|
| Retail Stores — Large Format | 42 | 8,000–10,000 | 378,000 | Owned / Ground Lease |
| Retail Stores — Standard Format | 58 | 5,000–7,999 | 348,000 | Owned / Ground Lease |
| Retail Stores — Mall Tenants | 20 | 3,000–5,000 | 80,000 | Leased from Mall Developers |
| Regional Warehouses | 4 | 20,000–30,000 | 100,000 | Owned |
| Corporate HQ | 1 | 12,500 | 12,500 | Owned |
| Training Center (within HQ) | 1 | 1,500 | 1,500 | Owned |
| **Total Portfolio** | **126** | — | **920,000** | — |

TPI provides facilities management services to TDI under an intercompany service agreement (ICSA-PROP-2024-001). All maintenance, safety, and capital improvement costs are allocated to TDI via a shared services chargeback model processed monthly through Oracle Fusion Cloud.

### 1.2 Organizational Structure

TPI operates under the following reporting hierarchy:

| Role | Headcount | Reports To | Primary Responsibility |
|---|---|---|---|
| VP — Facilities & Property Management | 1 | TPI President / TDI CFO | Strategic oversight, capital planning, lease negotiations |
| Director — Building Operations | 1 | VP — Facilities | Day-to-day building operations across portfolio |
| Director — Safety & Compliance | 1 | VP — Facilities | Fire safety, LGU permits, regulatory compliance |
| Director — Energy & Sustainability | 1 | VP — Facilities | Energy procurement, solar program, waste management |
| Regional Facilities Manager — North/Central Luzon | 1 | Director — Building Ops | 38 stores, 1 warehouse (Clark) |
| Regional Facilities Manager — South Luzon | 1 | Director — Building Ops | 35 stores, 1 warehouse (Calamba) |
| Regional Facilities Manager — Visayas | 1 | Director — Building Ops | 27 stores, 1 warehouse (Cebu) |
| Regional Facilities Manager — Mindanao | 1 | Director — Building Ops | 20 stores, 1 warehouse (Davao) |
| Facilities Manager — Corporate HQ | 1 | Director — Building Ops | HQ complex, training center |
| Maintenance Supervisors | 120 | Regional Facilities Managers | 1 per store/warehouse; on-site oversight |
| Maintenance Technicians | 240 | Maintenance Supervisors | 2 per store; 5 per warehouse; 8 at HQ |
| Administrative & Lease Coordinators | 6 | Director — Building Ops | Lease admin, vendor coordination, Oracle data entry |
| Safety Officers (DOSH-accredited) | 8 | Director — Safety & Compliance | 2 per region; fire drill coordination, incident response |
| Energy Analysts | 4 | Director — Energy & Sustainability | 1 per region; utility monitoring, solar panel tracking |

**Total TPI Headcount:** 385

### 1.3 Oracle Fusion Cloud Integration

All facilities management activities are tracked within Oracle Fusion Cloud across the following modules:

| Oracle Fusion Module | Application in Facilities Management |
|---|---|
| Assets | Fixed asset registration, depreciation scheduling, asset lifecycle tracking for all building systems and equipment |
| Projects (PJT) | Capital improvement project creation, budget allocation, milestone tracking, cost collection, and project closeout |
| HCM Workforce Health & Safety (WH&S) | Safety incident reporting, fire drill records, workplace inspections, incident investigation workflows |
| Procurement (POR) | Purchase requisitions for maintenance supplies, vendor contracts for outsourced services, blanket purchase agreements |
| General Ledger (GL) | Cost center allocation for maintenance expenses, intercompany chargebacks from TPI to TDI |
| Payables (AP) | Vendor payment processing for maintenance contractors, utility bill payments |
| Maintenance (Cloud Maintenance) | Preventive maintenance scheduling, work order management, asset condition monitoring |

### 1.4 Intercompany Service Agreement Summary

| Parameter | Detail |
|---|---|
| Agreement Number | ICSA-PROP-2024-001 |
| Effective Period | January 1, 2025 – December 31, 2027 |
| Chargeback Basis | Occupied floor area (PHP/sqm/month) + actual utility costs + proportional share of capital projects |
| Standard Chargeback Rate | PHP 185/sqm/month (owned properties) |
| Mall Tenant Surcharge | PHP 45/sqm/month (for TPI-managed fitout maintenance at mall locations) |
| Warehouse Rate | PHP 140/sqm/month |
| Billing Frequency | Monthly, net 30 days |
| Dispute Resolution | Escalation to TDI CFO and TPI President within 15 business days |

---

## 2. Building Maintenance Standards

### 2.1 Preventive Maintenance Philosophy

TPI follows a reliability-centered maintenance (RCM) approach for all building systems. Preventive maintenance (PM) is scheduled in Oracle Fusion Cloud — Maintenance module and tracked against asset records in Oracle Assets. Every piece of building equipment is registered as a fixed asset with a unique asset tag, installation date, warranty expiry, and assigned PM program.

### 2.2 Asset Registration Standards

All building systems and equipment with a unit cost exceeding PHP 15,000 or a useful life exceeding 2 years must be registered in Oracle Assets with the following attributes:

| Field | Requirement |
|---|---|
| Asset Number | Auto-generated by Oracle; format: TPI-ASSET-[YYYY]-[SEQ] |
| Asset Description | Standardized naming: [Building System] — [Equipment Type] — [Location] — [Store Code] |
| Asset Category | Mapping to Oracle asset category: Buildings, Building Improvements, Machinery & Equipment, Vehicles |
| Store Code | TDI store code (e.g., TD-MKT-001 for Market! Market! Taguig) |
| Installation Date | Actual commissioning date |
| Warranty Expiry | Per vendor warranty certificate |
| Depreciation Method | Straight-line, per TPI depreciation policy |
| Useful Life | Per asset class table below |
| Assigned PM Program | Oracle Maintenance PM schedule reference |
| Replacement Cost | Current estimated replacement value (updated annually) |

**Asset Class — Useful Life and Depreciation Schedule:**

| Asset Class | Example Equipment | Useful Life (Years) | Residual Value (%) |
|---|---|---|---|
| HVAC — Chillers | 200-TR centrifugal chiller | 20 | 5 |
| HVAC — Split Units | 2.0 HP wall-mounted split type | 8 | 0 |
| HVAC — Package Units | 20-TR rooftop package unit | 15 | 5 |
| Electrical — Transformers | 500 kVA oil-immersed transformer | 30 | 5 |
| Electrical — Generators | 500 kVA diesel generator set | 20 | 5 |
| Electrical — ATS/Panels | Automatic transfer switch, MDB | 20 | 0 |
| Electrical — UPS | 30 kVA online UPS | 7 | 0 |
| Plumbing — Pumps | Booster pump set, submersible pump | 12 | 0 |
| Plumbing — Water Tanks | GRP panel water tank, 10,000 gal | 20 | 5 |
| Fire Protection — Pumps | Fire pump set (jockey, main, stand-by) | 20 | 5 |
| Fire Protection — Sprinklers | Wet pipe sprinkler system | 25 | 0 |
| Fire Protection — Alarm | Addressable fire alarm panel | 15 | 0 |
| Elevators | Passenger elevator, 15-person capacity | 20 | 5 |
| Escalators | Commercial escalator, 30° incline | 20 | 5 |
| Structural — Racking | Heavy-duty pallet racking (warehouse) | 15 | 0 |
| Solar Panels | 450W monocrystalline PV module | 25 | 10 |
| Solar Inverters | 100 kW string inverter | 12 | 0 |

### 2.3 Preventive Maintenance Schedules

#### 2.3.1 HVAC Systems

| Maintenance Activity | Frequency | Responsible Party | Estimated Duration | Oracle PM Code |
|---|---|---|---|---|
| Chiller — Refrigerant charge check | Quarterly | HVAC Contractor (JSR Aircon) | 4 hours | PM-HVAC-CH-001 |
| Chiller — Condenser tube cleaning | Semi-annually | HVAC Contractor (JSR Aircon) | 8 hours | PM-HVAC-CH-002 |
| Chiller — Compressor oil analysis | Annually | OEM Service (Carrier/Trane) | 6 hours | PM-HVAC-CH-003 |
| Chiller — Full overhaul including bearings, seals | Every 5 years | OEM Service (Carrier/Trane) | 3 days | PM-HVAC-CH-004 |
| AHU — Filter replacement (MERV 13) | Monthly | In-house technician | 1 hour per unit | PM-HVAC-AH-001 |
| AHU — Belt inspection and tensioning | Quarterly | In-house technician | 30 min per unit | PM-HVAC-AH-002 |
| AHU — Coil cleaning (evaporator/condenser) | Semi-annually | HVAC Contractor | 2 hours per unit | PM-HVAC-AH-003 |
| AHU — Bearing lubrication, motor check | Annually | HVAC Contractor | 1 hour per unit | PM-HVAC-AH-004 |
| Split Unit — Filter cleaning | Bi-weekly | In-house technician | 15 min per unit | PM-HVAC-SP-001 |
| Split Unit — Full service (gas check, coil clean) | Quarterly | HVAC Contractor | 45 min per unit | PM-HVAC-SP-002 |
| Package Unit — Comprehensive PM | Quarterly | HVAC Contractor | 2 hours per unit | PM-HVAC-PK-001 |
| Cooling Tower — Water treatment and blowdown | Weekly | Water treatment vendor (Nalco) | 1 hour | PM-HVAC-CT-001 |
| Cooling Tower — Mechanical inspection | Monthly | HVAC Contractor | 2 hours | PM-HVAC-CT-002 |
| FCU — Drain pan cleaning, biocide treatment | Monthly | In-house technician | 20 min per unit | PM-HVAC-FC-001 |

#### 2.3.2 Electrical Systems

| Maintenance Activity | Frequency | Responsible Party | Estimated Duration | Oracle PM Code |
|---|---|---|---|---|
| Transformer — Oil sampling and DGA test | Annually | Licensed electrical contractor (BERA licensed) | 4 hours | PM-ELEC-TR-001 |
| Transformer — Visual inspection, thermography | Quarterly | In-house technician | 1 hour | PM-ELEC-TR-002 |
| Generator — Load bank test (100% rated load) | Monthly | Generator contractor (FG Wilson Phils.) | 2 hours | PM-ELEC-GN-001 |
| Generator — Oil and filter change | Every 250 operating hours | Generator contractor | 1.5 hours | PM-ELEC-GN-002 |
| Generator — Full service (coolant, belts, injectors) | Annually | OEM Service | 8 hours | PM-ELEC-GN-003 |
| ATS — Automatic transfer test | Monthly | In-house technician | 30 min | PM-ELEC-AT-001 |
| ATS — Contact inspection, torque check | Annually | Licensed electrical contractor | 2 hours | PM-ELEC-AT-002 |
| MDB/Panelboards — Thermographic scan | Quarterly | Licensed electrical contractor | 2 hours per panel | PM-ELEC-MD-001 |
| MDB/Panelboards — Breaker testing and calibration | Annually | Licensed electrical contractor | 4 hours per panel | PM-ELEC-MD-002 |
| UPS — Battery load test | Quarterly | UPS vendor (Eaton/APC) | 1 hour | PM-ELEC-UP-001 |
| UPS — Battery replacement | Every 3 years | UPS vendor | 2 hours | PM-ELEC-UP-002 |
| Lightning Protection — Resistance testing | Annually | Licensed electrical contractor | 3 hours | PM-ELEC-LP-001 |
| Emergency Lighting — Functional test | Monthly | In-house technician | 30 min (all units) | PM-ELEC-EL-001 |
| Emergency Lighting — 90-minute discharge test | Annually | In-house technician | 2 hours | PM-ELEC-EL-002 |

#### 2.3.3 Plumbing Systems

| Maintenance Activity | Frequency | Responsible Party | Estimated Duration | Oracle PM Code |
|---|---|---|---|---|
| Booster pump — Pressure switch calibration | Quarterly | Plumbing contractor | 30 min per pump | PM-PLMB-BP-001 |
| Booster pump — Motor bearing lubrication | Semi-annually | Plumbing contractor | 30 min per pump | PM-PLMB-BP-002 |
| Booster pump — Seal replacement, full overhaul | Every 5 years | OEM Service | 4 hours | PM-PLMB-BP-003 |
| Water tank — Interior inspection and cleaning | Semi-annually | Water tank cleaning vendor (PhilHygiene) | 4 hours | PM-PLMB-WT-001 |
| Water tank — Refurbishment (GRP panel replacement) | Every 10 years | OEM Service | 2 days | PM-PLMB-WT-002 |
| Grease trap — Pumping and cleaning | Monthly | Septic/grease trap vendor | 1 hour | PM-PLMB-GT-001 |
| Septic tank — Desludging | Quarterly | Licensed hauler (DENR-accredited) | 2 hours | PM-PLMB-ST-001 |
| Sewer lines — CCTV inspection | Annually | Plumbing contractor | 4 hours | PM-PLMB-SL-001 |
| Faucets/flushometers — Leak check and cartridge replacement | Quarterly | In-house technician | 1 hour (all units) | PM-PLMB-FA-001 |
| Water heater — Anode rod inspection | Annually | Plumbing contractor | 30 min per unit | PM-PLMB-WH-001 |
| Backflow preventer — Test and certification | Annually | Licensed plumber (PRC-registered) | 1 hour | PM-PLMB-BF-001 |

#### 2.3.4 Fire Protection Systems

| Maintenance Activity | Frequency | Responsible Party | Estimated Duration | Oracle PM Code |
|---|---|---|---|---|
| Fire pump — Weekly churn test (no-flow) | Weekly | In-house technician | 15 min | PM-FIRE-FP-001 |
| Fire pump — Annual flow test | Annually | Fire protection contractor (APi Phils.) | 4 hours | PM-FIRE-FP-002 |
| Fire pump — Full service (bearings, seals, packing) | Every 3 years | Fire protection contractor | 8 hours | PM-FIRE-FP-003 |
| Sprinkler system — Visual inspection | Monthly | In-house technician | 1 hour | PM-FIRE-SP-001 |
| Sprinkler system — Full trip test (main drain) | Quarterly | Fire protection contractor | 2 hours | PM-FIRE-SP-002 |
| Sprinkler system — Internal pipe inspection (obstruction) | Every 5 years | Fire protection contractor | 6 hours | PM-FIRE-SP-003 |
| Fire alarm — Panel test and visual inspection | Monthly | In-house technician | 30 min | PM-FIRE-FA-001 |
| Fire alarm — Detector sensitivity test (100% coverage) | Annually | Fire alarm contractor (Honeywell/Notifier) | 8 hours | PM-FIRE-FA-002 |
| Fire alarm — Battery backup test | Quarterly | In-house technician | 30 min | PM-FIRE-FA-003 |
| Fire extinguisher — Visual inspection (all units) | Monthly | In-house technician | 1 hour | PM-FIRE-FE-001 |
| Fire extinguisher — Annual service and hydrostatic test | Annually | Licensed fire extinguisher contractor | 4 hours | PM-FIRE-FE-002 |
| Fire hose cabinets — Visual and hose inspection | Quarterly | In-house technician | 1 hour | PM-FIRE-HC-001 |
| Smoke exhaust / stairwell pressurization — Functional test | Semi-annually | Fire protection contractor | 2 hours | PM-FIRE-SE-001 |
| FM-200 / clean agent system — Inspection and weight check | Quarterly | Fire protection contractor | 1 hour | PM-FIRE-CA-001 |
| Fire dampers — Functional test | Annually | Fire protection contractor | 2 hours | PM-FIRE-FD-001 |

#### 2.3.5 Elevators and Escalators

| Maintenance Activity | Frequency | Responsible Party | Estimated Duration | Oracle PM Code |
|---|---|---|---|---|
| Elevator — Monthly service visit (MSV) | Monthly | Elevator contractor (Kone/OTIS/Mitsubishi) | 2 hours per unit | PM-ELEV-EL-001 |
| Elevator — Quarterly comprehensive PM | Quarterly | Elevator contractor | 4 hours per unit | PM-ELEV-EL-002 |
| Elevator — Annual load test and safety device check | Annually | Elevator contractor + TESDA-certified inspector | 4 hours | PM-ELEV-EL-003 |
| Elevator — Controller and drive modernization | Every 15 years | Elevator contractor | 2 weeks | PM-ELEV-EL-004 |
| Escalator — Monthly service visit | Monthly | Elevator contractor | 2 hours per unit | PM-ELEV-ES-001 |
| Escalator — Step chain tension and comb plate inspection | Quarterly | Elevator contractor | 2 hours per unit | PM-ELEV-ES-002 |
| Escalator — Annual safety device test | Annually | Elevator contractor + inspector | 3 hours | PM-ELEV-ES-003 |
| Escalator — Full refurbishment (steps, chains, handrails) | Every 12 years | Elevator contractor | 4 weeks | PM-ELEV-ES-004 |

#### 2.3.6 Structural and Building Envelope

| Maintenance Activity | Frequency | Responsible Party | Estimated Duration | Oracle PM Code |
|---|---|---|---|---|
| Roof — Visual inspection for leaks, ponding, membrane damage | Quarterly | In-house technician | 2 hours | PM-STR-RF-001 |
| Roof — Comprehensive condition survey | Annually | Structural engineer (PRC-licensed) | Full day | PM-STR-RF-002 |
| Roof — Waterproofing recoating | Every 5 years | Waterproofing contractor | 3–5 days | PM-STR-RF-003 |
| Facade / exterior wall — Visual crack survey | Semi-annually | In-house technician | 2 hours | PM-STR-FW-001 |
| Facade — Sealant replacement | Every 7 years | Waterproofing contractor | 5 days | PM-STR-FW-002 |
| Floor slab — Condition assessment (cracks, settlement) | Annually | Structural engineer | Full day | PM-STR-FS-001 |
| Parking area — Line repainting | Annually | Parking contractor | 2 days | PM-STR-PK-001 |
| Parking area — Waterproofing membrane check (basement) | Semi-annually | Waterproofing contractor | 4 hours | PM-STR-PK-002 |
| Windows and glazing — Seal and hardware check | Annually | Glazing contractor | 2 hours | PM-STR-WG-001 |
| Expansion joints — Inspection and replacement | Every 5 years | Structural contractor | 3 days | PM-STR-EJ-001 |
| Racking (warehouse) — Bolt torque and alignment check | Quarterly | In-house technician | 4 hours | PM-STR-RK-001 |
| Racking — Full structural certification | Annually | Structural engineer | 1 day | PM-STR-RK-002 |
| Doors and roll-up shutters — Lubrication and alignment | Monthly | In-house technician | 1 hour | PM-STR-DR-001 |

---

## 3. Reactive Maintenance Process

### 3.1 Work Order Lifecycle

All reactive maintenance requests are processed through Oracle Fusion Cloud Maintenance. The lifecycle proceeds as follows:

| Stage | Action | Responsible Party | System Record |
|---|---|---|---|
| 1. Request Submission | Any TDI or TPI employee submits a work request via Oracle Maintenance self-service portal or scans QR code posted at each store's maintenance room | Requestor | Work Request (WR) created in Oracle |
| 2. Triage | On-site Maintenance Supervisor reviews and assigns priority classification within 30 minutes of submission | Maintenance Supervisor | WR status → Reviewed; Priority assigned |
| 3. Work Order Creation | Supervisor converts WR to Work Order (WO), assigns technician or external vendor, estimates materials and labor | Maintenance Supervisor | WO created in Oracle; Asset linked |
| 4. Dispatch | Technician receives WO notification via Oracle mobile app; vendor receives PO if external service required | Technician / Vendor | WO status → In Progress |
| 5. Execution | Work performed; parts consumed from on-site inventory or procured via emergency PO | Technician / Vendor | Labor hours and material usage logged |
| 6. Quality Check | Maintenance Supervisor inspects completed work before sign-off | Maintenance Supervisor | WO status → Pending Review |
| 7. Closure | Supervisor closes WO; requestor receives notification; satisfaction rating optional | Maintenance Supervisor | WO status → Closed; Oracle Asset condition updated |
| 8. Analysis | Regional Facilities Manager reviews WO data monthly for trends, repeat failures, and PM gaps | Regional Facilities Manager | Oracle reports and dashboards |

### 3.2 Priority Classification and SLAs

| Priority Level | Definition | Response Time | Resolution Target | Examples |
|---|---|---|---|---|
| P1 — Emergency | Immediate threat to life safety, major structural failure, or complete store/warehouse shutdown | 15 minutes (technician on-site) | 2 hours (temporary measures); 24 hours (permanent fix) | Fire alarm activation, roof collapse, main power failure, burst water main, gas leak |
| P2 — Urgent | Significant operational disruption affecting >25% of selling area or critical building system failure | 30 minutes (technician on-site) | 4 hours (temporary); 48 hours (permanent) | Partial HVAC failure (sales floor >32°C), escalator breakdown, section power outage, elevator entrapment |
| P3 — Standard | Operational issue with limited impact; does not affect core operations | 4 hours (technician on-site) | 3 business days | Leaking faucet, cracked floor tile, exterior lighting failure, minor wall damage |
| P4 — Scheduled | Non-urgent improvement or aesthetic issue; can be batched with next PM visit | 24 hours (acknowledgment) | 10 business days | Repainting scuff marks, replacing ceiling tiles, sign replacement, shelving adjustment |

**SLA Escalation Matrix:**

| Missed Milestone | Escalation Level | Notified Party | Required Action |
|---|---|---|---|
| Response SLA breached | Level 1 | Regional Facilities Manager | Reassign WO; deploy backup technician or emergency vendor |
| Resolution SLA breached (P1/P2) | Level 2 | Director — Building Operations | Authorize emergency contractor engagement; report to VP within 1 hour |
| Resolution SLA breached (P3/P4) | Level 2 | Regional Facilities Manager | Vendor follow-up; adjust PM schedule if systemic issue |
| Repeated failures (same asset, 3x in 90 days) | Level 3 | Director — Building Operations | Trigger asset replacement review in Oracle Assets; cost-benefit analysis |

### 3.3 Vendor Management for Maintenance Services

TPI maintains an approved vendor list (AVL) for all outsourced maintenance services. Vendors are onboarded through Oracle Procurement and evaluated annually.

#### 3.3.1 Key Maintenance Vendor Categories

| Service Category | Primary Vendor(s) | Contract Type | Annual Contract Value (est.) | Coverage |
|---|---|---|---|---|
| HVAC Maintenance | JSR Airconditioning Systems, Inc. | Blanket Purchase Agreement | PHP 48,000,000 | All 120 stores + 4 warehouses + HQ |
| Elevator/Escalator Maintenance | Kone Philippines, OTIS Elevator Philippines | Per-unit annual contract | PHP 36,000,000 | 185 elevators + 92 escalators portfolio-wide |
| Electrical (High Voltage) | Philelec Engineering, MERALCO Industrial | Time & materials (call-out) | PHP 12,000,000 | Transformer and HV switchgear maintenance |
| Generator Maintenance | FG Wilson Power Systems Philippines | Annual service contract | PHP 9,500,000 | 130 generator sets portfolio-wide |
| Fire Protection | APi Fire Protection Philippines | Annual service contract | PHP 18,000,000 | All fire suppression and alarm systems |
| Plumbing | Regional plumbing contractors (4 firms) | Time & materials (call-out) | PHP 8,000,000 | Reactive plumbing services |
| Waterproofing | Taeya Waterproofing Solutions | Project-based | PHP 6,000,000 | Roof and basement waterproofing |
| Solar Panel O&M | SunPower Philippines / First Philec Solar | Annual O&M contract | PHP 4,200,000 | 45 store solar installations |

#### 3.3.2 Vendor Performance Scorecard

Vendors are assessed quarterly using the following scorecard, maintained in Oracle Procurement:

| Criterion | Weight | Scoring (1–5) | Description |
|---|---|---|---|
| Response Time Compliance | 30% | 5 = 100% within SLA; 1 = <60% within SLA | Measured against SLA response and resolution targets |
| Quality of Work | 25% | 5 = Zero callbacks in quarter; 1 = >3 callbacks per store | Based on Maintenance Supervisor inspection and callback rate |
| Safety Compliance | 20% | 5 = Zero safety incidents; 1 = Serious incident or violation | Per POL-HR-007 workplace health and safety standards |
| Documentation & Reporting | 15% | 5 = All reports submitted on time in Oracle; 1 = Chronic late reporting | Service reports uploaded to Oracle WO within 24 hours |
| Cost Control | 10% | 5 = Within ±5% of quote; 1 = >20% over quote | Actual costs vs. estimated costs |

**Minimum acceptable score:** 3.0 weighted average. Vendors scoring below 3.0 for two consecutive quarters are placed on probation. Vendors scoring below 2.5 or causing a safety incident are subject to immediate contract review.

---

## 4. Lease Management

### 4.1 Tenant-Landlord Framework

TPI and TDI operate under a tenant-landlord relationship governed by the intercompany service agreement (ICSA-PROP-2024-001). This framework also applies to the 20 mall-based stores where TDI is the tenant and external mall developers are the landlord.

| Relationship | TPI Role | Counterparty | Key Agreement |
|---|---|---|---|
| TPI → TDI (owned properties) | Landlord / Facilities Manager | Tahanan Depot, Inc. (tenant) | ICSA-PROP-2024-001 |
| TPI → External landlord (mall stores) | Tenant coordinator | SM Prime, Ayala Malls, Robinsons Land, Gaisano, etc. | Individual lease contracts (20 locations) |
| TPI → Ground lessors (select sites) | Lessee | Private landowners, government agencies | Ground lease agreements (12 locations) |

### 4.2 Lease Administration Process

| Task | Frequency | Responsible Party | Oracle Module |
|---|---|---|---|
| Lease abstract preparation (new leases) | Per transaction | Lease Coordinator | N/A — Managed in lease abstract database (Excel/SharePoint) |
| Rent schedule verification | Monthly | Lease Coordinator | Oracle Payables (AP) |
| Common Area Maintenance (CAM) charge reconciliation | Quarterly | Lease Coordinator + Finance | Oracle General Ledger (GL) |
| Lease renewal review | 12 months before expiry | Director — Building Ops + VP Facilities | Oracle Assets (for leasehold improvements) |
| Security deposit tracking | Per lease term | Lease Coordinator | Oracle Payables |
| Insurance certificate tracking | Annually | Safety & Compliance team | N/A — Certificate tracking in SharePoint |
| Percentage rent calculation (mall stores) | Monthly | Lease Coordinator + TDI Finance | Oracle GL |
| Ground lease escalation processing | Per escalation schedule | Lease Coordinator | Oracle AP |

### 4.3 Common Area Maintenance (CAM) Charges

CAM charges are assessed for all owned properties where TPI manages shared spaces (parking areas, loading docks, common corridors, exterior grounds, security infrastructure). The following cost components are included:

| CAM Component | Allocation Basis | Estimated Annual Cost/Store (PHP) | Cost Driver |
|---|---|---|---|
| Parking area maintenance (sweeping, line repainting, lighting) | Per parking slot | 420,000 | 150–300 slots per store |
| Exterior grounds (landscaping, drainage maintenance) | Per sqm of lot area | 180,000 | 2,000–5,000 sqm lot area |
| Security infrastructure (CCTV, boom barriers, guard house) | Fixed per store | 360,000 | Shared security systems |
| Common corridor lighting and HVAC (mall-adjacent stores) | Per sqm of corridor | 120,000 | Proportional to store footprint |
| Loading dock maintenance (dock levelers, canopy, drainage) | Fixed per dock | 95,000 | 2–4 docks per store |
| Waste collection area and compactor maintenance | Fixed per store | 85,000 | Solid waste management infrastructure |
| Fire pump room and common fire protection | Per sqm of selling area | 150,000 | Proportional to protected area |
| Building insurance (property and liability) | Per sqm of floor area | 280,000 | Insured value per store |

**Total estimated CAM per standard store:** PHP 1,690,000/year (approximately PHP 141,000/month)

### 4.4 Lease Renewal Process

| Step | Timeline | Action | Approver |
|---|---|---|---|
| 1 | 12 months before expiry | Lease Coordinator generates renewal calendar report from lease database | N/A (automated) |
| 2 | 11 months before expiry | Regional Facilities Manager conducts store condition assessment; building condition score recorded in Oracle Assets | Director — Building Ops |
| 3 | 10 months before expiry | VP Facilities reviews store performance data (sales per sqm, foot traffic, lease terms vs. market) with TDI Retail Operations | VP Facilities + TDI VP Retail |
| 4 | 9 months before expiry | Decision: renew, renegotiate, or relocate. If renew, VP Facilities authorizes negotiation parameters | TPI President + TDI CFO |
| 5 | 7 months before expiry | Lease terms negotiated with landlord (external) or ICSA amendment drafted (internal) | VP Facilities + Legal |
| 6 | 5 months before expiry | Final lease agreement or ICSA amendment executed | TPI President + TDI President |
| 7 | 3 months before expiry | Oracle lease records updated; new rent schedule entered; any leasehold improvement projects initiated in Oracle Projects | Lease Coordinator |

---

## 5. Energy Management

### 5.1 Energy Consumption Profile

TPI tracks energy consumption across all properties via Oracle Fusion and utility provider billing data. The following table summarizes the portfolio energy profile:

| Property Type | Avg. Monthly Consumption (kWh) | Avg. Monthly Cost (PHP) | Primary Energy Source | Peak Demand (kW) |
|---|---|---|---|---|
| Large Format Store (owned) | 280,000 | 2,912,000 | MERALCO / DU (Distribution Utility) | 650 |
| Standard Format Store (owned) | 195,000 | 2,028,000 | MERALCO / DU | 450 |
| Mall Tenant Store | 85,000 | 1,020,000 | Mall sub-metered supply | 200 |
| Regional Warehouse | 145,000 | 1,508,000 | DU | 380 |
| Corporate HQ | 210,000 | 2,184,000 | MERALCO | 520 |
| **Total Portfolio** | **~23,500,000** | **~~244,400,000** | — | — |

**Annual Portfolio Energy Spend:** Approximately PHP 2.93 billion

### 5.2 Electricity Management

| Initiative | Status | Target | Current Performance | Oracle Tracking |
|---|---|---|---|---|
| LED lighting retrofit (sales floor, backroom, parking) | 95% complete (114 of 120 owned stores) | 100% by Q2 2026 | 38% reduction in lighting energy vs. 2022 baseline | Oracle Assets — retrofit project tracking |
| Occupancy sensors (restrooms, backroom, stockroom) | 70% complete | 100% by Q4 2026 | 15% reduction in unoccupied-area lighting | Oracle Maintenance — sensor maintenance schedule |
| Inverter-type HVAC replacement program | 45% complete | 80% by 2028 | 22% energy savings per replaced unit | Oracle Projects — capital project PJT-HVAC-INV-01 |
| Power factor correction (capacitor banks) | 100% complete (all owned stores) | Maintain PF >0.95 | Average PF: 0.97 | Monthly utility bill review |
| Peak shaving (generator paralleling during peak hours) | Pilot in 8 stores | Evaluate ROI for portfolio rollout | PHP 180,000/month savings per store during peak | Oracle GL — cost center analysis |
| Time-of-use optimization (load shifting to off-peak) | Implemented in all MERALCO-served stores | Shift 15% of load to off-peak | 12% average shift achieved | Oracle GL — utility cost tracking |

### 5.3 Water Management

| Parameter | Detail |
|---|---|
| Water Sources | Manila Water (Metro Manila), Local Water Districts (provincial), Deep wells (8 warehouse/store locations) |
| Average Monthly Consumption (per owned store) | 450 cubic meters |
| Average Monthly Cost (per owned store) | PHP 67,500 |
| Annual Portfolio Water Spend | PHP 89,100,000 |

**Water Conservation Initiatives:**

| Initiative | Status | Target | Savings |
|---|---|---|---|
| Dual-flush toilet retrofit | 100% complete | Maintain | 35% reduction in restroom water use |
| Sensor-activated faucets | 85% complete | 100% by Q3 2026 | 25% reduction per faucet |
| Rainwater harvesting (warehouse irrigation and truck washing) | Installed at 3 of 4 warehouses | 4 of 4 by 2027 | 200 cu.m./month per warehouse |
| Sub-metering by zone (sales floor, backroom, landscape) | 60% complete | 100% by Q4 2026 | Leak detection and accountability |

### 5.4 Solar Panel Program

TPI has committed to installing rooftop solar photovoltaic systems across viable owned properties under the Renewable Energy Act of 2008 (RA 9513) and the net-metering program administered by the Energy Regulatory Commission (ERC).

| Metric | Current (2025) | Target (2028) |
|---|---|---|
| Stores with solar installations | 45 of 100 owned stores | 80 of 100 owned stores |
| Warehouses with solar installations | 4 of 4 | 4 of 4 (complete) |
| Total installed capacity | 12.4 MWp | 22.0 MWp |
| Annual energy generation | 16,740 MWh | 29,700 MWh |
| Portfolio energy offset | 5.9% | 10.5% |
| Annual cost savings | PHP 153,900,000 | PHP 273,200,000 |
| Capital invested to date | PHP 744,000,000 | PHP 1,320,000,000 (cumulative) |
| Average payback period | 4.8 years | — |

**Solar project lifecycle in Oracle Projects:**

| Stage | Oracle Activity | Responsible |
|---|---|---|
| Feasibility study | Project created (PJT-SOL-[STORE]-FY) | Director — Energy & Sustainability |
| Engineering design | Cost collected against project | Solar engineering contractor |
| Procurement (panels, inverters, mounting) | PO created in Oracle Procurement | TPI Procurement team |
| Installation | Progress billed against Oracle Project milestone | Solar contractor |
| Commissioning and grid connection | Asset created in Oracle Assets; net-metering registration | Director — Energy + MERALCO/DU |
| Ongoing O&M | PM schedule in Oracle Maintenance | Solar O&M vendor |

### 5.5 Sustainability Targets

| Target | Baseline (2022) | 2026 Target | 2028 Target | 2030 Target |
|---|---|---|---|---|
| Energy intensity reduction (kWh/sqm) | 31.5 kWh/sqm/year | 26.8 kWh/sqm/year (−15%) | 23.6 kWh/sqm/year (−25%) | 22.1 kWh/sqm/year (−30%) |
| Water intensity reduction (cu.m./sqm) | 0.58 cu.m./sqm/year | 0.49 cu.m./sqm/year (−15%) | 0.43 cu.m./sqm/year (−25%) | 0.41 cu.m./sqm/year (−30%) |
| Renewable energy share | 2.1% | 6.0% | 10.5% | 15.0% |
| Waste diversion rate (from landfill) | 32% | 50% | 65% | 75% |
| Carbon emissions reduction (Scope 1 & 2) | Baseline year | −10% | −20% | −35% |

---

## 6. Safety and Compliance

### 6.1 Regulatory Framework

All TPI-managed facilities must comply with the following Philippine regulations and standards:

| Regulation / Standard | Issuing Authority | Applicability | Key Requirements |
|---|---|---|---|
| National Building Code (PD 1096) | DPWH / Local Building Official (LBO) | All owned and leased properties | Building permits, occupancy permits, annual inspection |
| Fire Code of the Philippines (RA 9514) | BFP (Bureau of Fire Protection) | All properties | Fire safety inspection certificate (FSIC), fire drill, fire suppression |
| Occupational Safety and Health Standards (OSHS) | DOLE | All workplaces | Safety officer, safety committee, incident reporting |
| Clean Water Act (RA 9275) | DENR-EMB | All properties with wastewater discharge | Wastewater discharge permit, effluent standards |
| Ecological Solid Waste Management Act (RA 9003) | DENR-EMB / LGU | All properties | Waste segregation, collection, disposal, LGU permit |
| Toxic Substances and Hazardous and Nuclear Wastes Control Act (RA 6969) | DENR-EMB | Properties handling hazardous materials | Registration, proper storage, DENR-accredited transport and disposal |
| Renewable Energy Act (RA 9513) | DOE / ERC | Properties with solar installations | Net-metering registration, compliance with distribution utility requirements |
| Accessibility Law (BP 344) | National Council on Disability Affairs | All public-facing properties | Ramps, accessible restrooms, parking, signage |
| Philippine Electrical Code (PEC 2017) | Board of Electrical Engineering / PRC | All properties | Electrical installation standards, BERA inspections |
| Structural Code of the Philippines (NSCP 2015, 7th Edition) | ASEP / DPWH | All owned structures | Earthquake and wind load design, structural inspection |
| Local Government Tax Ordinances | LGU (City/Municipal Treasurer) | All properties | Real property tax (RPT), business tax, local permits |

### 6.2 Fire Safety Program

#### 6.2.1 Fire Safety Certificates and Permits

| Document | Issuing Authority | Renewal Frequency | Responsible Party | Tracking Method |
|---|---|---|---|---|
| Fire Safety Inspection Certificate (FSIC) | BFP — City/Municipal Fire Station | Annually | Safety Officer | SharePoint calendar + Oracle HCM WH&S |
| Certificate of Annual Inspection (CAI) — Fire Alarm | BFP-accredited testing agency | Annually | Fire alarm contractor | Oracle Maintenance — PM completion record |
| FSIC — Occupancy (new or modified spaces) | BFP | Per construction/renovation | Director — Safety & Compliance | Oracle Projects — project closeout checklist |
| Fire Insurance Certificate | Insurance provider | Annually | TPI Finance + Safety team | SharePoint |

#### 6.2.2 Fire Drill Schedule

Fire drills are conducted per POL-HR-007 (Workplace Health and Safety) requirements and documented in Oracle HCM WH&S:

| Facility Type | Drill Frequency | Minimum Participants | Drill Duration Target | Evacuation Time Target |
|---|---|---|---|---|
| Retail Stores (owned) | Semi-annually (Q1 and Q3) | 100% of on-duty staff | 45 minutes (including debrief) | <5 minutes (full evacuation) |
| Mall Tenant Stores | Annually (coordinated with mall management) | 100% of on-duty staff | 30 minutes | <3 minutes (to mall assembly point) |
| Regional Warehouses | Quarterly | 100% of on-duty staff + active contractors | 60 minutes | <6 minutes |
| Corporate HQ | Semi-annually (Q2 and Q4) | 100% of HQ employees | 45 minutes | <4 minutes |
| Night shift drills (24/7 warehouse) | Annually (night shift only) | 100% of night shift staff | 45 minutes | <6 minutes |

**Fire drill documentation requirements (Oracle HCM WH&S):**

| Data Point | Entered By | Timing |
|---|---|---|
| Drill date and time | Safety Officer | Within 24 hours of drill |
| Total participants and headcount reconciliation | Safety Officer | Within 24 hours |
| Evacuation time (from alarm to all-clear) | Safety Officer | Within 24 hours |
| Deficiencies observed (blocked exits, malfunctioning alarms, etc.) | Safety Officer | Within 24 hours |
| Corrective actions required | Safety Officer | Within 48 hours |
| Corrective actions completed | Maintenance Supervisor | Upon completion |
| BFP notification (as required by Fire Code) | Safety Officer | Within 5 days of drill |

### 6.3 Building Permits and LGU Compliance

#### 6.3.1 Annual LGU Permit Tracker

| Permit / License | Issuing LGU Office | Renewal Period | Cost Range (PHP) | Penalty for Non-Compliance |
|---|---|---|---|---|
| Business Permit / Mayor's Permit | Business Permits and Licensing Office (BPLO) | January 1–20 annually | 5,000–25,000 per store | Closure order, surcharges up to 25% |
| Real Property Tax (RPT) Clearance | City/Municipal Treasurer | Quarterly payments | Varies by assessed value (PHP 200K–1.5M per store annually) | 2%/month surcharge, auction of property |
| Sanitary/Health Permit | City Health Office | Annually | 1,500–5,000 | Closure order |
| Environmental Compliance Certificate (ECC) or CNC | DENR-EMB | One-time (with conditions) | 10,000–50,000 (filing fee) | Cease and desist order, fines |
| Zoning Clearance | City/Municipal Zoning Office | One-time or per renovation | 2,000–10,000 | Demolition order, business permit revocation |
| Sign/Billboard Permit | City Engineering Office / DPWH | Annually | 3,000–15,000 per sign | Removal of sign, fine |
| Mechanical Permit (elevators, boilers) | LBO | Per installation/replacement | 5,000–20,000 per unit | Stop work order |
| Electrical Permit | LBO | Per installation/renovation | 3,000–15,000 | Stop work order, disconnect |

#### 6.3.2 Building Condition Inspection Schedule

| Inspection Type | Frequency | Inspector | Standard Reference | Documentation |
|---|---|---|---|---|
| Annual structural integrity inspection | Annually (pre-typhoon season, March–April) | PRC-licensed structural engineer | NSCP 2015 | Report filed in Oracle Assets |
| Annual electrical safety inspection | Annually | BERA-licensed electrical engineer | PEC 2017 | Certificate filed in Oracle Assets |
| Annual fire safety inspection (BFP) | Annually | BFP fire marshal | RA 9514 | FSIC filed in SharePoint |
| Semi-annual general building inspection | Semi-annually | Regional Facilities Manager | TPI internal standards | Inspection checklist in Oracle Maintenance |
| Post-typhoon damage assessment | After each typhoon signal hoisted at store location | Maintenance Supervisor + Safety Officer | TPI Emergency Response Plan | Assessment report in Oracle HCM WH&S |
| Post-earthquake damage assessment | After earthquake of Intensity IV or above (PHIVOLCS scale) at store location | Structural engineer | NSCP 2015 | Assessment report in Oracle Assets |

---

## 7. Janitorial and Cleaning Standards

### 7.1 Service Delivery Model

TPI uses a hybrid model for janitorial services:

| Location Type | Delivery Model | Provider | Headcount per Location | Annual Cost per Location (PHP) |
|---|---|---|---|---|
| Large Format Store (owned) | Outsourced | Contracted janitorial agency (e.g., ISS Philippines, Magsaysay Care) | 8–12 personnel | 3,200,000 |
| Standard Format Store (owned) | Outsourced | Contracted janitorial agency | 5–8 personnel | 2,100,000 |
| Mall Tenant Store | Mall-provided | Mall operator (included in CAM charges to TDI) | N/A | Included in rent |
| Regional Warehouse | Outsourced + in-house | Janitorial agency (common areas) + in-house (warehouse floor) | 6–10 personnel | 2,400,000 |
| Corporate HQ | Outsourced | ISS Philippines (primary contractor) | 25 personnel | 9,000,000 |

### 7.2 Cleaning Frequency by Area

| Area / Zone | Daily Tasks | Weekly Tasks | Monthly Tasks | Quarterly Tasks |
|---|---|---|---|---|
| **Sales Floor — Hard Flooring (Tiles/Polished Concrete)** | Damp mop all aisles (before opening); Spot clean spills (continuous during operating hours); Sweep entrance mats | Machine scrub with neutral detergent; Buff polished surfaces | Deep strip and re-wax (polished surfaces only) | Full floor restoration (grout cleaning, chip repair) |
| **Sales Floor — Carpeted Areas (HQ, select offices)** | Vacuum all carpeted areas | Spot treatment for stains | Hot water extraction cleaning | Full carpet deep clean and deodorizing |
| **Restrooms (Public)** | Clean and disinfect all fixtures hourly during store hours; Restock supplies (soap, paper towels, tissue); Empty trash | Descale urinals and toilet bowls; Clean grout and tile walls; Inspect and clean exhaust fans | Replace deodorizer blocks; Clean mirror frames and partitions; Check caulking | Full deep clean including ceiling vents, behind fixtures |
| **Restrooms (Employee)** | Clean and disinfect twice daily (opening and midday); Restock supplies | Descale and scrub; Clean walls and partitions | Replace consumables in bulk; Check caulking | Full deep clean |
| **Loading Dock / Receiving Area** | Sweep and collect debris; Power hose loading area floor | Degrease dock levelers and surrounding floor; Clean dock bumpers | Inspect and clean drainage grates; Power wash walls | Full dock area restoration; Paint touch-up |
| **Parking Area (Open)** | Collect litter; Empty trash receptacles (3x daily) | Sweep all parking levels; Clean parking signage | Power wash parking floor; Repaint faded lines (if needed) | Full parking area deep clean including drainage |
| **Parking Area (Basement)** | Same as open + run exhaust fans continuously during operating hours | Clean ventilation louvers; Check sump pumps | Power wash walls and columns; Clean light fixtures | Full deep clean; Check waterproofing |
| **Exterior — Storefront and Canopy** | Sweep entrance area; Clean glass doors and windows | Power wash canopy underside; Clean exterior signage | Clean facade (where accessible); Touch up paint | Full exterior assessment; High-reach glass cleaning |
| **Break Room / Pantry** | Wipe tables and counters; Empty trash; Sweep/mop floor | Clean appliances (microwave, refrigerator); Descale water dispenser | Deep clean pantry cabinets; Sanitize refrigerator | Full deep clean |
| **Warehouse Floor** | Sweep aisles (2x daily); Spot clean spills immediately | Machine scrub main aisles; Clean around racking bases | Full floor machine scrub (all areas) | Assess floor coating condition; Re-coat if needed |
| **Office Areas (HQ)** | Empty trash; Wipe desks (if cleared); Vacuum/sweep | Dust all surfaces; Clean glass partitions | Clean light fixtures; Vacuum upholstery | Deep clean carpets; Clean HVAC diffusers |

### 7.3 Quality Standards and Inspection

| Inspection Type | Frequency | Inspector | Scoring System | Minimum Score |
|---|---|---|---|---|
| Daily opening inspection (pre-store opening) | Daily (6:00 AM) | Maintenance Supervisor | 20-point checklist; each item scored 0–5 | 85/100 |
| Random spot check | 2x per week (unannounced) | Regional Facilities Manager | 15-point checklist; each item scored 0–5 | 80/100 |
| Monthly comprehensive inspection | Monthly | TPI Quality Assurance team | 50-point checklist; each item scored 0–5 | 90/100 |
| Customer complaint tracking | Continuous | Store Manager → TPI | Number of cleanliness-related complaints per month | <5 per store per month |
| Vendor performance review (outsourced janitorial) | Quarterly | Regional Facilities Manager | Scorecard (response time, quality, staffing compliance, documentation) | 3.5/5.0 weighted average |

---

## 8. Pest Control Management

### 8.1 Program Overview

TPI contracts licensed pest control operators (PCOs) registered with the Fertilizer and Pesticide Authority (FPA) for all properties. Pest control services are managed under POL-SCM-004 (Warehouse Safety) for warehouses and POL-HR-007 (Workplace Health and Safety) for all occupied spaces.

### 8.2 Pest Control Service Providers

| Region | Provider | FPA License No. | Contract Period | Annual Value (PHP) |
|---|---|---|---|---|
| North/Central Luzon | Societas Pest Control Services | FPA-PCO-NCR-2019-0412 | Jan 2025 – Dec 2027 | 8,200,000 |
| South Luzon | Termite and Pest Control Experts, Inc. | FPA-PCO-4A-2020-0187 | Jan 2025 – Dec 2027 | 7,600,000 |
| Visayas | Citipest Control Corp. | FPA-PCO-7-2018-0095 | Jan 2025 – Dec 2027 | 5,100,000 |
| Mindanao | Davao Pest Control Services | FPA-PCO-11-2021-0033 | Mar 2025 – Feb 2028 | 4,300,000 |
| Corporate HQ | Societas Pest Control Services | FPA-PCO-NCR-2019-0412 | Jan 2025 – Dec 2027 | 960,000 |

### 8.3 Preventive Treatment Schedule

| Pest Type | Treatment Method | Frequency (Store) | Frequency (Warehouse) | Frequency (HQ) | Chemical(s) Used |
|---|---|---|---|---|---|
| Cockroaches | Residual spray + gel bait | Monthly | Bi-weekly | Bi-weekly | Cypermethrin (0.1%), Fipronil gel (0.01%) |
| Rodents (rats/mice) | Bait stations + trapping + exclusion | Monthly inspection; quarterly external baiting | Weekly inspection; monthly external baiting | Weekly inspection | Bromadiolone blocks (0.005%) |
| Termites | Soil treatment (pre-construction); Spot treatment (post-construction) | Annual inspection; treatment as needed | Annual inspection | Annual inspection | Imidacloprid (0.05%); Fipronil (0.06%) |
| Mosquitoes | Larvicidal treatment (standing water); ULV fogging (perimeter) | Monthly (larvicide); Quarterly (fogging) | Monthly (larvicide) | Monthly (larvicide) | Temephos (1%); Deltamethrin (0.05% ULV) |
| Flies | Fly bait stations; insect light traps (ILT) | Monthly ILT maintenance; quarterly bait replacement | Bi-weekly ILT maintenance | Monthly ILT maintenance | Azamethiphos (1%); UV light traps |
| Ants | Residual spray + bait stations | Monthly | Bi-weekly | Bi-weekly | Cypermethrin + hydramethylnon bait |
| Stored product insects (warehouse) | Fumigation (as needed); residual spray | N/A | Monthly fogging; semi-annual fumigation | N/A | Phosphine (fumigation); Cypermethrin |
| Birds (pigeons, sparrows) | Bird spikes, netting, deterrent gel | As needed (inspection quarterly) | As needed | As needed | Physical deterrents only (no chemicals) |

### 8.4 Treatment Protocols and Safety Requirements

| Requirement | Standard | Reference |
|---|---|---|
| Treatment timing | All chemical treatments performed outside store operating hours (before 9:00 AM or after 9:00 PM) | POL-HR-007 Section 4.3 |
| Worker PPE | Full PPE: chemical-resistant gloves, N95 mask or half-face respirator, safety goggles, long-sleeved coveralls | FPA label requirements |
| Re-entry interval | Minimum 2 hours after residual spray; minimum 4 hours after fogging; minimum 24 hours after fumigation | FPA label requirements + POL-HR-007 |
| Notification | 48-hour advance notice to Store Manager and Safety Officer before any scheduled treatment | TPI internal policy |
| Chemical storage | All pest control chemicals stored in locked, ventilated cabinet at PCO vehicle or service room; not stored in selling area | RA 6969 + FPA regulations |
| MSDS availability | Material Safety Data Sheets for all chemicals maintained at store maintenance room and uploaded to Oracle HCM WH&S | POL-HR-007 Section 6.1 |
| Incident reporting | Any pest control-related exposure or incident reported in Oracle HCM WH&S within 2 hours | POL-HR-007 Section 5.2 |
| Service documentation | PCO submits service report with chemical used, dosage, areas treated, and technician name within 24 hours; uploaded to Oracle Maintenance WO | TPI vendor requirements |

---

## 9. Renovation and Capital Improvement Projects

### 9.1 Project Classification

| Project Category | Budget Range (PHP) | Approval Authority | Oracle Project Type | Examples |
|---|---|---|---|---|
| Minor Renovation | < 2,000,000 | Regional Facilities Manager | Capital (minor) | Restroom renovation, break room upgrade, office partition |
| Standard Renovation | 2,000,000 – 10,000,000 | Director — Building Operations | Capital (standard) | Partial store refresh, new department build-out, dock expansion |
| Major Renovation | 10,000,000 – 50,000,000 | VP — Facilities & Property Management | Capital (major) | Full store renovation, warehouse expansion, structural retrofit |
| Strategic Capital Project | > 50,000,000 | TPI President + TDI Board approval | Capital (strategic) | New store build, warehouse construction, solar farm installation |
| Emergency Repair | Any amount (subject to retro-justification) | Regional Facilities Manager (up to PHP 5M); Director (up to PHP 20M); VP (> PHP 20M) | Emergency | Typhoon damage repair, fire restoration, structural emergency |

### 9.2 Project Lifecycle in Oracle Projects

| Phase | Stage | Oracle Activity | Deliverable | Responsible |
|---|---|---|---|---|
| **1. Initiation** | 1.1 Business case | Create project in Oracle Projects with preliminary budget and timeline | Project Charter | Requestor (Regional Facilities Manager or Director) |
| | 1.2 Feasibility | Collect cost estimates; attach engineering study costs to project | Feasibility Report | Director — Building Ops |
| | 1.3 Approval | Route project for approval per authority matrix (see 9.1) | Approved Project Charter | Approver per matrix |
| **2. Planning** | 2.1 Design | Add design consultant costs to project; create sub-projects for disciplines | Design drawings and specs | Director + Design Consultant |
| | 2.2 Budget finalization | Finalize project budget in Oracle; assign cost centers | Approved Budget | VP Facilities (for major/strategic) |
| | 2.3 Procurement planning | Create requisitions in Oracle Procurement; issue RFQs | PO / Contract | TPI Procurement team |
| | 2.4 Permit application | Submit building permit, fire safety permit, LGU permits | Approved permits | Director — Safety & Compliance |
| **3. Execution** | 3.1 Contractor mobilization | Issue PO to contractor; set project milestone dates | Mobilization notice | Project Manager |
| | 3.2 Construction | Track costs against project in real-time; approve progress billing | Progress reports (bi-weekly) | Project Manager |
| | 3.3 Quality inspections | Conduct inspections at key milestones (structural, electrical, fire) | Inspection reports | Director — Safety + LBO inspector |
| | 3.4 Change orders | Process change orders in Oracle Projects; re-route for approval if >10% of budget | Approved change orders | Approver per matrix |
| **4. Closeout** | 4.1 Punch list | Conduct final walkthrough; issue punch list to contractor | Punch list report | Regional Facilities Manager |
| | 4.2 Final acceptance | Accept completed work; release retention payment | Certificate of Completion | Director — Building Ops |
| | 4.3 Asset capitalization | Capitalize project costs into fixed assets in Oracle Assets | Asset register update | TPI Finance + Oracle Assets |
| | 4.4 As-built documentation | Upload as-built drawings, O&M manuals, warranty certificates to Oracle Assets and SharePoint | As-built package | Project Manager |
| | 4.5 Project close | Close Oracle Project; transfer to operations (PM schedules set up) | Project closure report | Project Manager |

### 9.3 Capital Budget Tracking

| Metric | Tracking Method | Frequency | Report Recipient |
|---|---|---|---|
| Project budget vs. actual cost | Oracle Projects — Budget vs. Actual report | Real-time (dashboard); monthly (formal) | VP Facilities, Director — Building Ops |
| Committed costs (open POs) | Oracle Projects — Committed Cost report | Weekly | Project Manager, TPI Finance |
| Cost variance (>10% of approved budget) | Oracle Projects — Exception report | Upon occurrence | Approver authority per matrix |
| Milestone completion vs. plan | Oracle Projects — Gantt chart / milestone tracking | Bi-weekly | VP Facilities |
| Retention and warranty tracking | Oracle Projects — Retention register | Monthly | TPI Finance |
| Capitalized asset value | Oracle Assets — Capitalization report | Per project closeout | TPI Finance, VP Facilities |

### 9.4 2026 Capital Improvement Plan (Summary)

| Project ID | Description | Location | Category | Budget (PHP) | Target Completion |
|---|---|---|---|---|---|
| PJT-2026-001 | Full renovation — TD-NCR-008 (Cubao) | Quezon City | Major Renovation | 42,000,000 | Q2 2026 |
| PJT-2026-002 | Warehouse expansion — WH-VIS-001 (Cebu) | Cebu City | Strategic Capital | 85,000,000 | Q3 2026 |
| PJT-2026-003 | Solar installation — 15 stores (Batch 3) | Various | Strategic Capital | 225,000,000 | Q4 2026 |
| PJT-2026-004 | HVAC replacement program (12 stores) | Various | Standard Renovation | 60,000,000 | Q3 2026 |
| PJT-2026-005 | Restroom renovation — 25 stores (Batch 2) | Various | Minor Renovation | 37,500,000 | Q2 2026 |
| PJT-2026-006 | Fire protection upgrade (8 stores, BFP compliance) | Various | Standard Renovation | 24,000,000 | Q2 2026 |
| PJT-2026-007 | Parking area resurfacing — 6 stores | Various | Standard Renovation | 18,000,000 | Q3 2026 |
| PJT-2026-008 | Elevator modernization — 4 units (2 stores) | Metro Manila | Major Renovation | 28,000,000 | Q4 2026 |
| PJT-2026-009 | HQ cafeteria renovation | Taguig City | Standard Renovation | 8,500,000 | Q1 2026 |
| PJT-2026-010 | LED lighting completion (remaining 6 stores) | Various | Minor Renovation | 12,000,000 | Q2 2026 |
| **Total 2026 Capital Plan** | | | | **539,500,000** | |

---

## 10. Environmental Management

### 10.1 Waste Management

#### 10.1.1 Waste Classification and Disposal

| Waste Category | Source | Segregation Method | Disposal Method | Transporter | Approx. Volume (per store/month) | Cost (PHP/month/store) |
|---|---|---|---|---|---|---|
| General solid waste (non-recyclable) | Sales floor, office, break room | Black bags; labeled bins | LGU-accredited hauler to sanitary landfill | LGU-accredited waste hauler | 8–15 cu.m. | 15,000–25,000 |
| Recyclable — Cardboard / cartons | Merchandise packaging, displays | Baled or bundled; yellow bins | Sold to recycling buyers | Recycling buyer (e.g., TIPCO) | 3–6 cu.m. | Revenue: 5,000–12,000 |
| Recyclable — Plastics (PE film, PET) | Merchandise packaging | Clear bags; segregated by plastic type | Sold to recycling buyers | Recycling buyer | 1–3 cu.m. | Revenue: 2,000–5,000 |
| Recyclable — Metals (steel, aluminum) | Damaged fixtures, pallets, displays | Collected in scrap bin | Sold to junk shops | Junk shop collector | 0.5–1.5 cu.m. | Revenue: 3,000–8,000 |
| Food waste | Employee cafeteria, break room | Green bins with lids | Composting or LGU collection | Composting partner (HQ) / LGU hauler | 0.5–1 cu.m. | 2,000–4,000 |
| Hazardous waste — Used batteries (lead-acid) | UPS systems, generator starting batteries | Labeled containers; stored in spill containment | DENR-accredited transporter to TSD facility | DENR-accredited hazardous waste transporter | 50–100 kg/year | 15,000–25,000/year |
| Hazardous waste — Used oil | Generator maintenance, HVAC compressors | Drums with spill containment | DENR-accredited recycler | DENR-accredited used oil recycler | 200–500 liters/year | 8,000–15,000/year |
| Hazardous waste — Fluorescent tubes / LED panels | Lighting replacement | Sealed containers (prevents mercury release) | DENR-accredited TSD facility | DENR-accredited transporter | 100–200 units/year | 10,000–20,000/year |
| Hazardous waste — Paint and solvent containers | Maintenance and renovation activities | Labeled drums | DENR-accredited TSD facility | DENR-accredited transporter | 50–100 liters/year | 5,000–10,000/year |
| E-waste | Obsolete POS equipment, computers, monitors | E-waste bin; tracked by IT | DENR-accredited e-waste recycler | DENR-accredited recycler | Varies | Cost borne by TDI IT |

#### 10.1.2 DENR Compliance Requirements

| Requirement | Standard | Compliance Activity | Frequency | Responsible |
|---|---|---|---|---|
| Hazardous waste generator registration | RA 6969 (DENR AO 2013-22) | Maintain valid DENR registration as hazardous waste generator | Renew every 3 years | Director — Safety & Compliance |
| Manifest system | DENR AO 2013-22 | Complete hazardous waste manifest for every shipment; retain copies for 5 years | Per shipment | Safety Officer |
| Effluent discharge permit | RA 9275 (DENR AO 2021-19) | Apply for and maintain discharge permit; submit quarterly monitoring reports | Quarterly monitoring; annual renewal | Director — Energy & Sustainability |
| Self-Monitoring Report (SMR) | DENR-EMB requirement | Submit monthly/bi-monthly SMR to EMB regional office | Bi-monthly | Director — Energy & Sustainability |
| Environmental Management System (EMS) audit | TPI internal standard | Conduct internal EMS audit per ISO 14001-aligned framework | Annually | Director — Energy & Sustainability |

### 10.2 Typhoon Preparedness

The Philippines experiences an average of 20 typhoons annually. TPI follows a tiered preparedness protocol based on PAGASA storm signal warnings:

| PAGASA Signal | Trigger | Preparedness Actions | Responsible |
|---|---|---|---|
| Signal No. 1 (30–60 km/h winds expected in 36 hours) | PAGASA raises Signal No. 1 over store/warehouse LGU | Inspect roof for loose materials; clear drainage; check generator fuel; pre-position sandbags; secure outdoor signage; notify all store staff | Maintenance Supervisor + Store Manager |
| Signal No. 2 (61–120 km/h winds expected in 24 hours) | PAGASA raises Signal No. 2 | Execute full typhoon checklist (48 items); activate emergency vendor contracts; cover vulnerable windows; shut down non-essential electrical systems; reduce store inventory on floor | Regional Facilities Manager |
| Signal No. 3 (121–170 km/h winds expected in 18 hours) | PAGASA raises Signal No. 3 | Close store to public; secure all building openings; activate emergency communication plan; evacuate warehouse personnel to designated shelter | Director — Safety & Compliance + VP Facilities |
| Signal No. 4 (>170 km/h winds expected in 12 hours) | PAGASA raises Signal No. 4 | Full lockdown; all personnel in designated safe rooms; emergency generators on standby; continuous monitoring of building structural sensors (if equipped) | VP Facilities + TPI President |

**Post-typhoon damage assessment protocol:**

| Step | Action | Timeline | Responsible | Documentation |
|---|---|---|---|---|
| 1 | Initial visual drive-by or drone survey (if safe) | Within 6 hours of all-clear | Regional Facilities Manager | Photos and preliminary damage notes in Oracle HCM WH&S |
| 2 | Detailed on-site damage assessment | Within 24 hours of all-clear | Maintenance Supervisor + Safety Officer | Full damage assessment report in Oracle Maintenance (emergency WO) |
| 3 | Structural safety determination | Within 48 hours | PRC-licensed structural engineer (for Signal 3/4 impact) | Structural safety certificate |
| 4 | Emergency repairs authorization | Within 48 hours | VP Facilities (up to PHP 20M); TPI President (> PHP 20M) | Emergency PO in Oracle Procurement |
| 5 | Insurance claim filing | Within 72 hours | TPI Finance + Insurance broker | Claim documentation package |
| 6 | Store reopening clearance | After all safety criteria met | Director — Safety & Compliance + BFP inspection (if required) | Reopening clearance certificate in Oracle HCM WH&S |

### 10.3 Earthquake Preparedness

The Philippines is located within the Pacific Ring of Fire. TPI facilities are designed and maintained to withstand seismic loads per NSCP 2015 Zone classifications:

| Region | NSCP Seismic Zone | Key Fault Lines | Special Provisions |
|---|---|---|---|
| Metro Manila (HQ + 28 stores) | Zone 4 (highest) | West Valley Fault, East Valley Fault | Annual structural integrity inspection mandatory; retrofit assessment for pre-2000 buildings |
| Central Luzon (12 stores + Clark warehouse) | Zone 4 | Philippine Fault (Digdig segment), Manila Trench | Same as Metro Manila |
| Southern Luzon (35 stores + Calamba warehouse) | Zone 2–4 | Philippine Fault, Lubang Fault | Zone-specific design verification |
| Visayas (27 stores + Cebu warehouse) | Zone 2–4 | Central Philippines Fault, Negros Trench | Post-2013 Bohol earthquake: enhanced seismic inspection for Cebu/Bohol stores |
| Mindanao (20 stores + Davao warehouse) | Zone 2–4 | Philippine Fault (Mindanao segment), Cotabato Trench | Post-2019 Davao earthquakes: enhanced structural monitoring for Davao stores |

**Post-earthquake response protocol:**

| PHIVOLCS Intensity | Response |
|---|---|
| Intensity I–III (Weak to Weak) | No automatic action; Maintenance Supervisor conducts visual check of building systems |
| Intensity IV–V (Moderately Strong to Strong) | Evacuate building; Maintenance Supervisor + Safety Officer conduct full inspection before re-entry; check fire protection, electrical, gas, and structural systems |
| Intensity VI–VII (Very Strong to Destructive) | Full evacuation; PRC-licensed structural engineer must inspect before re-entry; all stores in affected area closed until cleared |
| Intensity VIII+ (Very Destructive) | Full evacuation; emergency response team activated; await PHIVOLCS guidance; structural engineer mandatory before any re-entry |

---

## 11. Facility Performance Metrics

### 11.1 Key Performance Indicators (KPIs)

TPI tracks facility performance using the following KPIs, reported monthly via Oracle Fusion Cloud dashboards:

| KPI | Definition | Target | Measurement Source | Report Frequency |
|---|---|---|---|---|
| PM Completion Rate | % of scheduled PM work orders completed on time | ≥ 95% | Oracle Maintenance — PM compliance report | Monthly |
| Reactive WO Response SLA Compliance | % of reactive WOs where technician responded within SLA (by priority) | P1: 100%; P2: ≥ 98%; P3: ≥ 95%; P4: ≥ 90% | Oracle Maintenance — WO SLA report | Monthly |
| Reactive WO Resolution SLA Compliance | % of reactive WOs resolved within target resolution time | P1: ≥ 95%; P2: ≥ 90%; P3: ≥ 85%; P4: ≥ 80% | Oracle Maintenance — WO SLA report | Monthly |
| Building Condition Score | Composite score (1–100) based on structural, electrical, HVAC, plumbing, fire protection, and aesthetic assessments | ≥ 85 (all facilities) | Oracle Assets — condition assessment + semi-annual inspection | Semi-annually |
| Energy Intensity | kWh consumed per sqm of floor area per year | ≤ 26.8 kWh/sqm/year (2026 target) | Oracle GL — utility cost tracking + floor area data | Monthly (tracking); annual (benchmark) |
| Water Intensity | Cubic meters consumed per sqm of floor area per year | ≤ 0.49 cu.m./sqm/year (2026 target) | Utility billing data + floor area data | Monthly (tracking); annual (benchmark) |
| Safety Incident Rate | Number of facility-related safety incidents per 200,000 work hours (OSHA incidence rate) | < 2.0 | Oracle HCM WH&S — incident tracking | Monthly |
| Fire Drill Compliance | % of required fire drills conducted on schedule with ≥ 95% participation | 100% | Oracle HCM WH&S — drill records | Semi-annually (per drill cycle) |
| Janitorial Quality Score | Average monthly inspection score across all stores | ≥ 90/100 | TPI QA inspection records | Monthly |
| Vendor Performance Score | Average weighted score on vendor performance scorecard | ≥ 3.5/5.0 | Oracle Procurement — vendor evaluation | Quarterly |
| Capital Project On-Budget Delivery | % of capital projects completed within ±5% of approved budget | ≥ 85% | Oracle Projects — budget vs. actual | Per project closeout; annually (aggregate) |
| Capital Project On-Time Delivery | % of capital projects completed within approved timeline | ≥ 80% | Oracle Projects — milestone tracking | Per project closeout; annually (aggregate) |
| Work Order Backlog | Number of open reactive WOs older than SLA resolution target | < 15 portfolio-wide at any time | Oracle Maintenance — WO aging report | Weekly |
| Equipment Uptime — HVAC | % of time HVAC systems are operational during store operating hours | ≥ 99.0% | Oracle Maintenance — downtime tracking | Monthly |
| Equipment Uptime — Elevators/Escalators | % of time elevators and escalators are operational during store operating hours | ≥ 99.5% | Oracle Maintenance — downtime tracking | Monthly |
| Waste Diversion Rate | % of total waste diverted from landfill (recycled, composted, reused) | ≥ 50% (2026 target) | Waste hauler reports + recycling revenue records | Monthly (tracking); annual (benchmark) |
| LGU Permit Compliance | % of required LGU permits and licenses current and valid | 100% | Lease Coordinator permit tracker | Monthly |

### 11.2 Building Condition Score Methodology

| Component | Weight | Assessment Method | Scoring Criteria |
|---|---|---|---|
| Structural (foundation, columns, beams, roof structure) | 20% | Visual inspection + structural engineer report (annual) | 100: No defects; 80: Minor cracks/cosmetic; 60: Moderate (requires repair within 6 months); 40: Significant (requires repair within 30 days); 20: Critical (immediate action required) |
| Electrical (transformer, panels, wiring, grounding) | 15% | Thermography + visual inspection + PEC compliance | Same scale as structural |
| HVAC (chillers, AHUs, split units, cooling towers) | 15% | PM records + performance test + age of equipment | Same scale |
| Plumbing (pipes, pumps, tanks, fixtures) | 10% | Leak survey + pressure test + water quality | Same scale |
| Fire Protection (alarms, sprinklers, extinguishers, pumps) | 15% | BFP inspection + functional tests + PM records | Same scale (minimum 80 required for any facility) |
| Elevators/Escalators | 5% | Contractor PM records + downtime logs + annual inspection | Same scale |
| Building Envelope (roof, walls, windows, waterproofing) | 10% | Visual inspection + leak log + thermography | Same scale |
| Aesthetic (paint, flooring, signage, landscaping) | 10% | Visual inspection + customer feedback | Same scale |

### 11.3 Reporting Cadence

| Report | Audience | Frequency | Source System | Delivery Method |
|---|---|---|---|---|
| Facilities Dashboard (real-time) | VP Facilities, Directors | Real-time | Oracle Fusion dashboards | Oracle BI Publisher / embedded analytics |
| Monthly Facilities Performance Report | VP Facilities, TPI President, TDI CFO | Monthly (by 5th business day) | Oracle Fusion consolidated | PDF via email + Oracle report center |
| Regional Facilities Summary | Regional Facilities Managers | Weekly (Monday) | Oracle Maintenance | Oracle BI Publisher scheduled report |
| Safety Incident Report | VP Facilities, Director — Safety, DOLE (if required) | Per incident (within 24 hours) | Oracle HCM WH&S | Oracle workflow notification + email |
| Capital Project Status Report | VP Facilities, TPI President, TDI CFO | Bi-weekly (during active projects) | Oracle Projects | Oracle BI Publisher |
| Annual Facilities Condition Assessment | TPI Board, TDI Board, Insurance providers | Annually (Q1) | Oracle Assets + inspection reports | Formal printed report + presentation |
| Energy and Sustainability Report | VP Facilities, Director — Energy, TDI CSR Committee | Quarterly | Oracle GL + utility data | PDF report + presentation |

---

## 12. Store Closure and Relocation

### 12.1 Closure and Relocation Triggers

A store may be closed or relocated for the following reasons:

| Trigger | Description | Decision Authority | Typical Timeline |
|---|---|---|---|
| Lease expiry (no renewal) | Landlord does not renew or terms are unacceptable | TPI President + TDI CFO | 12 months notice |
| Underperformance | Store consistently below financial thresholds for 8 consecutive quarters | TDI Board (upon recommendation of TDI VP Retail + TPI VP Facilities) | 6–12 months |
| Redevelopment | Landlord redevelops property; or TPI-owned site identified for higher-value use | TPI President + TDI Board | 12–24 months |
| Natural disaster (permanent) | Store damaged beyond economic repair by typhoon, earthquake, or flood | TPI President + TDI Board + Insurance | 3–6 months (temporary closure); 12–24 months (relocation) |
| Safety — structural failure | Building deemed unsafe and repair cost exceeds 60% of replacement value | VP Facilities (emergency closure); TPI President (permanent closure) | Immediate (temporary); 6–12 months (relocation) |
| Market exit | Strategic decision to exit a geographic market | TDI Board | 12 months |
| LGU regulatory action | LGU orders closure due to zoning change, right-of-way acquisition, or eminent domain | TPI President + Legal | Per LGU timeline; typically 6–12 months |

### 12.2 Store Closure Process

| Phase | Step | Action | Responsible Party | Timeline |
|---|---|---|---|---|
| **1. Decision** | 1.1 Performance/strategic review | Present closure business case with financial analysis | TDI VP Retail + TPI VP Facilities | D-12 months |
| | 1.2 Board approval | Obtain TDI and TPI Board resolution for closure | TDI Board + TPI Board | D-11 months |
| | 1.3 Employee consultation | Conduct employee consultation per DOLE requirements and TDI HR policy; provide relocation, redundancy, or retirement options | TDI HR Director + TPI HR | D-10 to D-6 months |
| **2. Wind-down** | 2.1 Customer notification | Post closure notice in-store and online at least 60 days before closure | TDI Marketing + Store Manager | D-60 days |
| | 2.2 Inventory liquidation | Execute clearance sale; transfer remaining inventory to nearest stores | TDI Merchandising + Supply Chain | D-60 to D-14 days |
| | 2.3 Fixture and equipment disposition | Assess fixtures for reuse (transfer to other stores), sale (to surplus buyers), or disposal | TPI Maintenance Supervisor + TDI Store Manager | D-45 to D-14 days |
| | 2.4 Vendor contract termination | Provide contractual notice to maintenance vendors, pest control, janitorial, security | TPI Procurement + Lease Coordinator | D-60 to D-30 days |
| | 2.5 Utility disconnection | Schedule final meter readings and disconnection with MERALCO/DU, water district, telecommunications | TPI Lease Coordinator | D-14 days |
| **3. Physical Closeout** | 3.1 Building handover (leased) | Conduct joint inspection with landlord; document condition; agree on restoration obligations | TPI Director — Building Ops + Legal | D-7 to D-0 |
| | 3.2 Building securing (owned) | Board up openings; deactivate electrical systems; maintain fire protection and security alarm; continue RPT payments | TPI Maintenance Supervisor | D-0 |
| | 3.3 Asset disposal in Oracle | Write off or transfer fixed assets in Oracle Assets; close cost centers in Oracle GL | TPI Finance | D-30 to D-0 |
| | 3.4 Permit cancellations | Cancel business permit, sanitary permit, FSIC, and other LGU permits | TPI Lease Coordinator + Safety Officer | D-30 to D-0 |
| **4. Post-Closure** | 4.1 Lease close-out | Final rent payment; security deposit return; claim landlord share of restoration costs (if leased) | TPI Lease Coordinator + Legal | D+30 to D+90 |
| | 4.2 Insurance claim (if disaster-related) | File and follow up on property insurance claim | TPI Finance + Insurance broker | D+0 to D+180 |
| | 4.3 Owned property disposition | Market property for sale or lease to third party; or hold for future redevelopment | VP Facilities + TPI President | D+0 to D+365 |
| | 4.4 Lessons learned | Document closure reasons, costs, and recommendations for future site selection | VP Facilities + TDI VP Retail | D+30 to D+60 |

### 12.3 Store Relocation Process

Relocation follows the closure process for the old site combined with the standard capital project process (Section 9) for the new site, with the following additional considerations:

| Relocation Step | Additional Action | Responsible |
|---|---|---|
| New site selection | Conduct site feasibility study (demographics, traffic, competition, lease terms, building condition) | TDI VP Retail + TPI VP Facilities |
| New site lease negotiation | Negotiate tenant improvement allowance, rent-free period, CAM exclusions with new landlord | VP Facilities + Legal |
| Permit acquisition for new site | Apply for all LGU permits, building permits (for fitout), BFP fire safety permit, ECC (if required) | Director — Safety & Compliance |
| Fitout construction | Execute fitout via Oracle Projects (PJT-RELOC-[STORE CODE]); track budget and milestones | Director — Building Ops |
| Oracle asset transfer | Transfer applicable equipment (POS, racking, fixtures) from old store asset records to new store | TPI Finance + TDI Finance |
| Overlap period management | Manage costs during overlap period (old store lease + new store rent); minimize overlap to <60 days | VP Facilities + TDI CFO |
| Grand opening coordination | Coordinate with TDI Marketing for grand opening event; ensure all safety compliance in place before opening | TDI Marketing + TPI Safety |
| Customer migration | Execute customer notification, redirect mail/deliveries, update store locator and online listings | TDI Marketing + TDI IT |

### 12.4 Financial Impact Tracking

All closure and relocation costs are tracked in dedicated Oracle Projects:

| Cost Category | Oracle Cost Collection Method | Typical Range (PHP) |
|---|---|---|
| Employee separation pay (redundancy) | Charged to TDI HR cost center (per DOLE requirements) | 2,000,000 – 15,000,000 per store |
| Inventory markdown and write-off | Charged to TDI Merchandising cost center | 1,500,000 – 8,000,000 per store |
| Lease termination penalties | Charged to Oracle Project (PJT-CLOSE-[STORE]) | 500,000 – 5,000,000 per store |
| Restoration / make-good costs | Charged to Oracle Project (PJT-CLOSE-[STORE]) | 1,000,000 – 10,000,000 per store |
| Fixture removal and disposal | Charged to Oracle Project (PJT-CLOSE-[STORE]) | 200,000 – 800,000 per store |
| New site fitout (relocation only) | Charged to Oracle Project (PJT-RELOC-[STORE]) | 15,000,000 – 50,000,000 per store |
| Overlap rent (relocation only) | Charged to Oracle Project (PJT-RELOC-[STORE]) | 1,000,000 – 4,000,000 per month of overlap |
| Legal and professional fees | Charged to Oracle Project | 300,000 – 1,500,000 per store |
| Asset write-off (non-transferable equipment) | Charged to TPI Finance via Oracle Assets disposal | 500,000 – 5,000,000 per store |

---

## Appendix A: Glossary

| Term | Definition |
|---|---|
| ATS | Automatic Transfer Switch |
| AHU | Air Handling Unit |
| AVL | Approved Vendor List |
| BERA | Board of Electrical Engineering (PRC) |
| BFP | Bureau of Fire Protection |
| CAM | Common Area Maintenance |
| CAI | Certificate of Annual Inspection |
| DENR | Department of Environment and Natural Resources |
| DOLE | Department of Labor and Employment |
| DOSH | Department of Occupational Safety and Health |
| DU | Distribution Utility (electricity provider) |
| ECC | Environmental Compliance Certificate |
| EMB | Environmental Management Bureau (DENR) |
| FCU | Fan Coil Unit |
| FPA | Fertilizer and Pesticide Authority |
| FSIC | Fire Safety Inspection Certificate |
| HCM WH&S | Human Capital Management — Workforce Health & Safety (Oracle Fusion) |
| ICSA | Intercompany Service Agreement |
| ILT | Insect Light Trap |
| KONE/OTIS | Elevator manufacturers |
| LGU | Local Government Unit (city/municipality) |
| LBO | Local Building Official |
| MDB | Main Distribution Board (electrical panel) |
| MERALCO | Manila Electric Railroad and Light Company (Metro Manila DU) |
| MSV | Monthly Service Visit |
| NSCP | National Structural Code of the Philippines |
| OSHS | Occupational Safety and Health Standards |
| PAGASA | Philippine Atmospheric, Geophysical and Astronomical Services Administration |
| PCO | Pest Control Operator |
| PEC | Philippine Electrical Code |
| PHIVOLCS | Philippine Institute of Volcanology and Seismology |
| PM | Preventive Maintenance |
| PRC | Professional Regulation Commission |
| RCM | Reliability-Centered Maintenance |
| RPT | Real Property Tax |
| TDI | Tahanan Depot, Inc. (retail operating entity) |
| TPI | Tahanan Property, Inc. (real estate and facilities entity) |
| TSD | Treatment, Storage, and Disposal (DENR-licensed facility) |
| ULV | Ultra-Low Volume (fogging) |
| UPS | Uninterruptible Power Supply |
| WO | Work Order |
| WR | Work Request |

## Appendix B: Reference Documents

| Document ID | Title | Owner |
|---|---|---|
| POL-SCM-004 | Warehouse Safety Policy | TDI Supply Chain |
| POL-HR-007 | Workplace Health and Safety Policy | TDI Human Resources |
| ICSA-PROP-2024-001 | Intercompany Service Agreement (TPI → TDI) | TPI Finance / TDI Finance |
| TD-OPS-001 | Store Operations Guide | TDI Retail Operations |
| TD-OPS-005 | Standard Operating Procedures | TDI Retail Operations |
| TD-FIN-003 | Fixed Asset Capitalization and Depreciation Policy | TPI Finance |
| TD-IT-009 | Oracle Fusion Cloud User Access and Procedures | TDI Information Technology |
| TPI-EMER-001 | Emergency Response Plan (Typhoon, Earthquake, Fire) | TPI Safety & Compliance |
| TPI-PROC-002 | Vendor Onboarding and Performance Management | TPI Procurement |

## Appendix C: Oracle Fusion Module Quick Reference for Facilities

| Task | Oracle Module | Transaction | User Role |
|---|---|---|---|
| Create a preventive maintenance schedule | Maintenance | Define PM program; assign to asset | Maintenance Supervisor |
| Submit a reactive work request | Maintenance (Self-Service) | Create work request | Any TDI/TPI employee |
| Convert work request to work order | Maintenance | Create WO; assign technician/vendor | Maintenance Supervisor |
| Order maintenance supplies | Procurement | Create requisition → PO | Maintenance Supervisor / Regional Facilities Manager |
| Track capital project budget | Projects | Create project; collect costs; run budget vs. actual | Project Manager |
| Report a safety incident | HCM WH&S | Create incident report; initiate investigation | Safety Officer / any employee |
| Record fire drill results | HCM WH&S | Log safety activity (drill) | Safety Officer |
| Capitalize completed renovation | Assets | Add asset; link to project costs | TPI Finance |
| Depreciate building equipment | Assets | Run depreciation; post to GL | TPI Finance |
| Pay maintenance vendor invoice | Payables | Enter invoice; match to PO; schedule payment | TPI Finance / AP team |
| Allocate facilities costs to TDI | General Ledger | Process intercompany allocation; post journal | TPI Finance |
| Run facilities performance dashboard | BI Publisher / OTBI | Execute standard report or custom analysis | VP Facilities / Directors |

---

*End of Document TD-OPS-018 — Facilities Management*
*Document maintained by Tahanan Property, Inc. — Facilities Management Division*
*For questions or clarifications, contact: facilities@tahanandepot.com.ph*
