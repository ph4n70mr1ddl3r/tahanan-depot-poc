# 20 — TRANSPORTATION & LOGISTICS

## 20.1 Transportation Organization

### 20.1.1 Transportation Team Structure

The Transportation function reports to the VP Distribution Operations and is responsible for all inbound, outbound, inter-facility, and customer delivery logistics across the Tahanan Depot network.

| Position | Reports To | Headcount | Key Responsibilities |
|----------|-----------|-----------|---------------------|
| VP Distribution Operations | COO | 1 | Overall supply chain distribution strategy; transportation budget PHP 3.2B annually; fleet and 3PL oversight; Oracle TMS/WMS governance |
| Director of Transportation | VP Distribution Operations | 1 | Transportation operations across all 4 regions; fleet management; 3PL relationships; cost optimization |
| National Fleet Manager | Director of Transportation | 1 | Owned fleet strategy; vehicle procurement and disposal; LTO compliance; maintenance program |
| Regional Transportation Manager — Luzon | Director of Transportation | 1 | Route planning for ~60 stores ex-Luzon warehouses; 3PL coordination; delivery performance |
| Regional Transportation Manager — Visayas | Director of Transportation | 1 | Inter-island logistics; RO-RO coordination; port operations; ~30 stores |
| Regional Transportation Manager — Mindanao | Director of Transportation | 1 | Inter-island logistics; Davao/CDO hub operations; ~30 stores |
| Fleet Supervisor (per warehouse) | National Fleet Manager | 4 | Day-to-day fleet dispatch; driver supervision; vehicle inspections |
| Route Planner (per region) | Regional Transportation Manager | 4 | Oracle TMS route optimization; delivery scheduling; load planning |
| Dispatch Coordinator (per warehouse) | Regional Transportation Manager | 4 | Daily dispatch execution; driver briefings; POD collection |
| 3PL Relationship Manager | Director of Transportation | 1 | 3PL contract management; SLA monitoring; rate negotiation; performance scorecards |
| Fuel & Toll Analyst | National Fleet Manager | 1 | Fuel card program management; consumption analysis; efficiency reporting |
| Transportation Cost Analyst | Director of Transportation | 1 | Freight cost allocation; cost-per-delivery tracking; Oracle TMS cost analytics |

### 20.1.2 Transportation Decision Authority

| Decision | Approver | Threshold |
|----------|----------|-----------|
| Routine dispatch (daily routes) | Dispatch Coordinator | Within approved route plan |
| Route deviation (unplanned) | Fleet Supervisor | < PHP 10,000 additional cost |
| Emergency rerouting (typhoon, road closure) | Regional Transportation Manager | Any amount |
| 3PL spot rate acceptance | 3PL Relationship Manager | < 15% above contracted rate |
| 3PL spot rate (above threshold) | Director of Transportation | >= 15% above contracted rate |
| New 3PL partner onboarding | Director of Transportation + VP Distribution Operations | Any |
| Vehicle purchase/disposal | VP Distribution Operations | Per approved capex budget |
| Fleet insurance renewal | VP Distribution Operations + VP Finance | Annual |
| Inter-island charter booking | Regional Transportation Manager | < PHP 500,000 |
| Inter-island charter booking (above) | Director of Transportation | >= PHP 500,000 |
| Fuel surcharge adjustment | Director of Transportation + VP Finance | Per fuel index review |

### 20.1.3 Oracle Fusion Module Touchpoints — Transportation

| Oracle Module | Transportation Usage | Integration |
|---------------|---------------------|-------------|
| Transportation Management (TMS) | Route planning, load building, carrier selection, freight cost management, shipment tracking, POD management | Core transportation platform |
| Warehouse Management (WMS) | Wave planning for pick-pack-ship (SOP-SCM-003); dock door scheduling; load confirmation; outbound shipment creation | Real-time via TMS-WMS integration |
| Inventory Management | In-transit inventory visibility; transfer order fulfillment; inventory movement tracking across locations | Real-time via supply chain orchestration |
| Order Management | Sales order fulfillment for B2B deliveries; delivery scheduling; order promising (GOP) | Real-time via order-to-ship flow |
| Supply Chain Planning | Demand-driven replenishment orders (PROC-SCM-001); transport demand forecasting | Daily batch via planning data extracts |
| Cost Management | Landed cost calculation; freight cost allocation; transportation expense analytics | Batch and real-time |
| Financials (GL/AP) | Freight invoice processing; 3PL payment; fleet expense tracking; cost center reporting | Via AP invoice matching |

---

## 20.2 Fleet Management

### 20.2.1 Owned Fleet Summary

Tahanan Depot operates a mixed fleet of owned vehicles for primary store replenishment and bulky-item last-mile delivery. The fleet is registered under Tahanan Logistics Inc., a wholly-owned subsidiary.

| Vehicle Type | Count | Capacity | Primary Use | Avg Age (years) |
|-------------|-------|----------|-------------|-----------------|
| 10-Wheeler Wing Van | 48 | 12 MT / 60 cbm | Full-store replenishment (Luzon) | 3.5 |
| 10-Wheeler Dropside | 24 | 10 MT / open bed | Lumber, steel, cement delivery | 2.8 |
| 6-Wheeler Forward Cab | 36 | 5 MT / 30 cbm | Express store replenishment; smaller stores | 4.1 |
| 6-Wheeler Flatbed | 12 | 6 MT / open bed | Heavy/bulky construction materials | 3.0 |
| 4-Wheeler Dropside (Elf) | 18 | 2 MT / 12 cbm | Urban last-mile B2B delivery; same-day | 2.5 |
| Refrigerated Van (Reefer) | 4 | 5 MT / 28 cbm | Temperature-sensitive items (paints, adhesives) | 1.5 |
| Boom Truck (with crane) | 8 | 8 MT with 5-ton crane | Heavy appliance delivery with lift | 3.2 |
| Crew Cab / Service Vehicle | 16 | — | Driver transport; supervision; emergency response | 2.0 |
| **Total** | **166** | | | |

### 20.2.2 Vehicle Specifications

| Vehicle | Make/Model | Engine | Fuel | GVW (kg) | Length (m) | Tail Lift | GPS |
|---------|-----------|--------|------|----------|------------|-----------|-----|
| 10W Wing Van | Hino 500 Series FM8J | 8.0L Diesel | Diesel | 26,000 | 9.6 | Hydraulic, 2.0T | Yes |
| 10W Dropside | Isuzu FTR33H | 7.8L Diesel | Diesel | 25,000 | 8.5 | N/A (ramps) | Yes |
| 6W Forward Cab | Mitsubishi FUSO FK61FZ | 5.2L Diesel | Diesel | 12,500 | 6.5 | Hydraulic, 1.5T | Yes |
| 6W Flatbed | Isuzu NQR | 5.2L Diesel | Diesel | 11,000 | 6.0 | N/A (ramps) | Yes |
| 4W Dropside | Mitsubishi FUSO Canter FE73S | 3.0L Diesel | Diesel | 6,500 | 4.2 | Manual ramp | Yes |
| Reefer Van | Hino 300 Series XZU | 3.0L Diesel | Diesel + reefer unit | 7,500 | 5.5 | Hydraulic, 1.0T | Yes |
| Boom Truck | Isuzu FVR34H | 7.8L Diesel | Diesel | 22,000 | 7.0 (crane: 5T reach 6.5m) | Crane | Yes |

### 20.2.3 Vehicle Registration and LTO Compliance

All vehicles are registered with the Land Transportation Office (LTO) per Republic Act 4136 and subsequent amendments.

| Requirement | Frequency | Responsible | LTO Reference |
|-------------|-----------|-------------|---------------|
| Motor Vehicle Registration (MV) | Annual | Fleet Supervisor | LTO MV Registration |
| Commercial Vehicle Inspection | Annual | Fleet Supervisor + LTO-accredited inspector | LTO MVIS |
| Emissions Testing | Annual (with registration) | Fleet Supervisor | LTO / DENR emission standard |
| Certificate of Public Convenience (CPC) — if applicable | Per franchise term | Legal + Fleet | LTFRB |
| Toll RFID Registration (Easytrip/Autosweep) | Annual reload/registration | Fuel & Toll Analyst | NLEX/SLEX/Toll operators |
| HPG Permit (over-dimensional loads) | Per trip | Dispatch Coordinator | PNP-HPG |
| Port Access Pass | Semi-annual | Regional Transportation Manager | PPA |

**LTO Registration Tracking (Oracle Fleet Extension — managed via spreadsheet register):**

| Region | Vehicles | Registration Month | Inspection Month | Next Renewal Window |
|--------|----------|--------------------|-------------------|---------------------|
| NCR / Central Luzon | 62 | Per plate ending digit (Jan-Dec) | 1 month before reg expiry | 60 days before expiry |
| Southern Luzon | 22 | Per plate ending digit | 1 month before reg expiry | 60 days before expiry |
| Visayas | 28 | Per plate ending digit | 1 month before reg expiry | 60 days before expiry |
| Mindanao | 24 | Per plate ending digit | 1 month before reg expiry | 60 days before expiry |

### 20.2.4 Fleet Maintenance Program

| Maintenance Type | Frequency | Scope | Duration | Location |
|-----------------|-----------|-------|----------|----------|
| Pre-Trip Inspection | Every dispatch | Tires, lights, brakes, fluids, belts, horn, mirrors | 15 min | Warehouse yard |
| Post-Trip Inspection | Every return | Body damage, cargo area, tire condition, leaks | 10 min | Warehouse yard |
| Preventive Maintenance A (PM-A) | Every 5,000 km or 30 days | Oil change, oil filter, air filter, brake inspection, fluid top-up | 4 hours | Regionally contracted service center |
| Preventive Maintenance B (PM-B) | Every 15,000 km or 90 days | PM-A + brake pads, fuel filter, transmission fluid, suspension check, electrical | 8 hours | Regionally contracted service center |
| Preventive Maintenance C (PM-C) | Every 30,000 km or 180 days | PM-B + coolant flush, wheel bearing repack, chassis lubrication, full electrical | 1-2 days | Authorized dealer |
| Annual Overhaul | Every 12 months | Engine tune-up, clutch inspection, underchassis overhaul, body repair, repainting as needed | 3-5 days | Authorized dealer |
| Tire Replacement | Every 60,000 km or 18 months | Full set replacement; retreads prohibited on steer axle per DOTC protocol | 4 hours | Fleet tire contractor (Goodyear PH / Bridgestone) |
| Refrigeration Unit Service (reefer) | Every 1,000 operating hours | Compressor, condenser, evaporator, thermostat calibration | 4 hours | Reefer service contractor |

**Fleet Maintenance Budget:**

| Category | Annual Budget (PHP M) | Per Vehicle Avg (PHP) |
|----------|----------------------|----------------------|
| Preventive Maintenance | 180.0 | 1,084,337 |
| Tire Replacement | 48.0 | 289,157 |
| Body and Paint | 24.0 | 144,578 |
| Major Repairs | 36.0 | 216,867 |
| Annual Overhaul | 32.0 | 192,771 |
| **Total Fleet Maintenance** | **320.0** | **1,927,711** |

---

## 20.3 Delivery Route Planning

### 20.3.1 Oracle TMS Route Optimization

Oracle Fusion Transportation Management is the primary platform for route planning, load building, and delivery scheduling. Route optimization runs are executed daily by the Route Planner in each region.

| Process Step | System | Oracle Module | Timing |
|-------------|--------|---------------|--------|
| Transfer orders released from supply planning | SCP → Inventory | Supply Chain Planning + Inventory | Day -1 (by 4:00 PM) |
| Transfer orders grouped by destination region | TMS | Transportation Management | Day -1 (by 5:00 PM) |
| Order consolidation and load building | TMS | Transportation Management | Day -1 (by 6:00 PM) |
| Route optimization engine executes (constraints applied) | TMS | Transportation Management | Day -1 (by 7:00 PM) |
| Routes reviewed and adjusted by Route Planner | TMS | Transportation Management | Day -1 (by 8:00 PM) |
| Driver and vehicle assignments made | TMS + Fleet Register | Transportation Management | Day -1 (by 9:00 PM) |
| Load plan sent to WMS for wave release | TMS → WMS | TMS + WMS | Day -1 (by 10:00 PM) |
| Pick-pack-ship executed per SOP-SCM-003 | WMS | Warehouse Management | Day 0 (starting 5:00 AM) |
| Dispatch confirmed; driver briefing completed | TMS | Transportation Management | Day 0 (starting 6:00 AM) |
| In-transit tracking activated | TMS + GPS | Transportation Management | Day 0 (upon departure) |
| Delivery confirmation and POD capture | TMS Mobile | Transportation Management | Day 0/Day 1 |

**TMS Route Optimization Constraints:**

| Constraint | Parameter | Source |
|-----------|-----------|--------|
| Vehicle capacity (weight) | Per vehicle type spec | Fleet Master Data |
| Vehicle capacity (volume) | Per vehicle type spec | Fleet Master Data |
| Delivery time windows | Per store receiving schedule | Store Master Data |
| Maximum driving hours | 10 hours per shift per DOLE | Hours of Service rules |
| Mandatory rest break | 1 hour after 5 hours driving | DOLE Labor Code |
| Road restrictions | Weight limits on provincial bridges, LGU truck bans | TMS constraint table |
| Multi-stop limit | Maximum 6 store drops per route | Operations policy |
| Priority stores | Stock-out stores; promotional stores; grand openings | Planning priority flag |
| Backhaul opportunities | Return legs loaded with vendor pickup or RTV | TMS backhaul module |

### 20.3.2 Delivery Windows by Store Type

| Store Type | Receiving Window | Notes |
|-----------|-----------------|-------|
| Flagship (urban) | 6:00 AM – 12:00 PM | Multiple deliveries per day accepted |
| Standard (suburban) | 6:00 AM – 10:00 AM | Primary window; secondary window 1:00 PM – 3:00 PM |
| Express (provincial) | 7:00 AM – 10:00 AM | Single daily delivery |
| Mall-based stores | 10:00 PM – 6:00 AM (overnight) | Per mall management regulations; noise restrictions |
| Stores in LGU truck ban zones | 9:00 AM – 3:00 PM or 9:00 PM – 5:00 AM | Per LGU ordinance (varies by city/municipality) |

### 20.3.3 Store Delivery Schedule by Region

**Luzon (from Cabuyao DC — servicing 60 stores):**

| Day | Route Zone | Stores Served | Avg Distance (km) | Avg Stops | Vehicles |
|-----|-----------|---------------|-------------------|-----------|----------|
| Monday | NCR North (QC, Caloocan, Valenzuela, Bulacan) | 8-10 | 35 | 4 | 3 wing vans + 2 forward cabs |
| Monday | Central Luzon North (Pampanga, Tarlac) | 4-5 | 120 | 3 | 2 wing vans + 1 dropside |
| Tuesday | NCR South (Makati, Pasay, Parañaque, Muntinlupa) | 8-10 | 30 | 5 | 3 wing vans + 2 forward cabs |
| Tuesday | Central Luzon South (Bataan, Zambales) | 3-4 | 150 | 3 | 2 wing vans |
| Wednesday | NCR East (Marikina, Antipolo, Rizal) | 6-8 | 40 | 4 | 3 wing vans + 1 dropside |
| Wednesday | CALABARZON North (Laguna, Cavite) | 6-8 | 65 | 4 | 3 wing vans + 1 forward cab |
| Thursday | CALABARZON South (Batangas, Quezon) | 4-6 | 130 | 3 | 2 wing vans + 1 dropside |
| Thursday | NCR Central (Manila, San Juan, Mandaluyong) | 6-8 | 25 | 5 | 2 wing vans + 2 forward cabs |
| Friday | Bicol Region (Camarines Sur, Albay) | 3-4 | 350 | 2 | 2 wing vans (overnight trip) |
| Friday | NCR overflow + urgent replenishment | 4-6 | 30 | 3 | 2 wing vans + 1 forward cab |
| Saturday | All regions — promotional / urgent restock | 10-15 | Varies | 2 | 4 wing vans (flexible) |

**Visayas (from Cebu DC — servicing 30 stores):**

| Day | Route Zone | Stores Served | Avg Distance (km) | Transport Mode |
|-----|-----------|---------------|-------------------|---------------|
| Monday | Cebu Metro | 5-6 | 25 | Direct truck |
| Monday | Cebu Province (north/south) | 3-4 | 80 | Direct truck |
| Tuesday | Iloilo + Panay Island | 4-5 | RO-RO from Cebu (8 hrs) | Truck via RO-RO |
| Wednesday | Bacolod + Negros Occidental | 3-4 | RO-RO from Cebu (6 hrs) | Truck via RO-RO |
| Thursday | Bohol | 2-3 | Fast craft + truck | Truck via RO-RO |
| Thursday | Cebu Metro (2nd delivery) | 5-6 | 25 | Direct truck |
| Friday | Leyte + Samar | 3-4 | RO-RO from Cebu (10 hrs) | Truck via RO-RO |
| Saturday | Overflow + urgent restock | 4-6 | Varies | Mixed |

**Mindanao (from Davao DC — servicing 30 stores):**

| Day | Route Zone | Stores Served | Avg Distance (km) | Transport Mode |
|-----|-----------|---------------|-------------------|---------------|
| Monday | Davao City + Metro | 5-6 | 30 | Direct truck |
| Monday | Davao del Norte, Compostela Valley | 3-4 | 100 | Direct truck |
| Tuesday | General Santos, South Cotabato | 3-4 | 150 | Direct truck |
| Wednesday | Cagayan de Oro + Misamis Oriental | 4-5 | 320 | Direct truck (overnight) |
| Thursday | Bukidnon, Lanao del Norte | 3-4 | 200 | Direct truck |
| Thursday | Davao City (2nd delivery) | 5-6 | 30 | Direct truck |
| Friday | Zamboanga Peninsula | 2-3 | 400 | Direct truck (overnight) |
| Saturday | Overflow + urgent restock | 4-6 | Varies | Mixed |

---

## 20.4 Third-Party Logistics (3PL) Management

### 20.4.1 3PL Partner Overview

Tahanan Depot supplements its owned fleet with contracted 3PL partners to handle seasonal peaks, overflow volume, and specialized transport requirements.

| 3PL Partner | Service Type | Region | Fleet Size (contracted) | Contract Term | Annual Contract Value (PHP M) |
|-------------|-------------|--------|------------------------|---------------|-------------------------------|
| 2GO Logistics | Inter-island sea freight + last mile | VisMin | 12 vessels (shared) + 50 trucks | 3 years (to Dec 2027) | 280.0 |
| Royal Cargo | Container drayage + port logistics | NCR / VisMin | 30 trucks + container handling | 2 years (to Jun 2026) | 120.0 |
| JRS Express Logistics | Last-mile B2B parcel delivery | Nationwide | 200+ vehicles (shared) | 1 year (renewable) | 45.0 |
| XDE Logistics | Metro Manila same-day and next-day delivery | NCR | 80 trucks (shared) | 2 years (to Mar 2027) | 95.0 |
| FastCat Forwarding | RO-RO inter-island transport | VisMin | 8 RO-RO vessels (shared) | 2 years (to Dec 2026) | 85.0 |
| Trans-Asia Shipping | Sea freight — Cebu/Manila/Davao corridor | VisMin | 4 vessels (shared) | 3 years (to Dec 2027) | 150.0 |
| V. Cargo | Cold chain transport | Nationwide | 15 reefer trucks | 1 year (renewable) | 28.0 |
| DM Construction Logistics | Heavy/bulky boom truck service | Nationwide | 20 boom/heavy trucks | 2 years (to Sep 2026) | 65.0 |

### 20.4.2 3PL Selection Criteria

| Criterion | Weight | Evaluation Method | Minimum Score |
|-----------|--------|-------------------|---------------|
| Service reliability (on-time delivery history) | 25% | 12-month track record; references | 90% OTD |
| Fleet adequacy and condition | 20% | Physical inspection; LTO registration verification | 85% pass rate |
| Geographic coverage | 15% | Route network map; inter-island capabilities | Covers required lanes |
| Financial stability | 10% | Audited financial statements; SEC registration | 3-year operating history |
| Insurance coverage | 10% | Certificate of insurance; cargo coverage per trip | Minimum PHP 5M per trip |
| Safety record | 10% | LTFRB/LTO violation record; accident history | < 2 incidents per 100 trips |
| Technology capability | 5% | GPS tracking; TMS integration; POD capture | Real-time GPS |
| Rate competitiveness | 5% | Benchmark against market rate; volume discount structure | Within 10% of market median |

### 20.4.3 3PL Service Level Agreements

| SLA Metric | Target | Consequence | Measurement |
|-----------|--------|-------------|-------------|
| On-time delivery (store delivery) | >= 95% | Credit of 2% of shipment cost per late delivery | TMS delivery timestamp vs. scheduled window |
| On-time pickup (at warehouse) | >= 98% | Credit of 1% of shipment cost per late pickup | TMS pickup timestamp vs. scheduled time |
| Delivery accuracy (no over/short/damage) | >= 99.5% | Full replacement value of lost/damaged goods | POD discrepancy rate |
| POD submission | Within 24 hours of delivery | PHP 500 per POD per day late | TMS POD upload timestamp |
| Vehicle GPS uptime | >= 99% | Pro-rated credit for GPS downtime days | GPS platform availability report |
| Accident/incident reporting | Within 2 hours of occurrence | PHP 5,000 penalty per late report | Incident report timestamp |
| Drug test compliance (drivers) | 100% pre-employment + random | Immediate contract suspension for non-compliance | Drug test certificates |
| Cargo insurance claims response | Within 5 business days | 1% per week delay penalty | Claims processing time |

### 20.4.4 3PL Performance Scorecard (Monthly)

| KPI | 2GO Logistics | XDE Logistics | FastCat | Trans-Asia | Target |
|-----|--------------|--------------|---------|-----------|--------|
| On-time delivery % | 93.2% | 96.1% | 91.8% | 94.5% | >= 95% |
| Delivery accuracy % | 99.7% | 99.4% | 99.1% | 99.6% | >= 99.5% |
| POD timeliness % | 97.8% | 98.5% | 95.2% | 96.0% | >= 98% |
| GPS uptime % | 99.1% | 99.5% | 98.8% | 99.2% | >= 99% |
| Claims rate (per 100 shipments) | 0.4 | 0.8 | 1.2 | 0.6 | <= 1.0 |
| Customer complaints | 2 | 1 | 4 | 1 | <= 2 |
| Overall score | 92.4 | 95.6 | 88.8 | 93.4 | >= 90 |

**Scorecard Governance:**

| Score Range | Action |
|-------------|--------|
| >= 95% | Preferred status; eligible for volume increase; annual rate lock |
| 90% – 94% | Meets expectations; corrective items tracked quarterly |
| 85% – 89% | Performance improvement plan (30 days); monthly review |
| < 85% | Formal warning; 60-day remediation; contract review |
| < 80% (2 consecutive months) | Contract termination for cause |

### 20.4.5 3PL Rate Management

| Rate Type | Basis | Review Frequency | Approval |
|-----------|-------|-------------------|----------|
| Store delivery (per drop) | Fixed per drop per zone | Annual | 3PL Relationship Manager |
| Store delivery (per km) | Variable per km + fuel surcharge | Quarterly | 3PL Relationship Manager |
| Inter-island (per TEU) | Fixed per 20ft/40ft container per lane | Annual | Director of Transportation |
| Inter-island (per MT) | Weight-based for loose cargo | Annual | Director of Transportation |
| Last-mile B2B (per delivery) | Fixed per delivery per zone | Annual | 3PL Relationship Manager |
| Heavy/bulky surcharge | % of base rate per item weight class | Annual | Director of Transportation |
| Fuel surcharge | Indexed to DOE Philippine diesel price | Monthly | Auto-applied per formula |
| Seasonal peak surcharge | Fixed % during Oct-Dec peak | Annual (pre-season) | Director of Transportation |

**Fuel Surcharge Formula:**

| Diesel Price Band (PHP/Liter) | Surcharge (% of base freight) |
|-------------------------------|-------------------------------|
| Below PHP 55.00 | 0% |
| PHP 55.00 – 59.99 | 3% |
| PHP 60.00 – 64.99 | 6% |
| PHP 65.00 – 69.99 | 9% |
| PHP 70.00 – 74.99 | 12% |
| PHP 75.00 and above | 15% |

---

## 20.5 Inter-Island and Long-Haul Logistics

### 20.5.1 Inter-Island Shipping Corridors

Tahanan Depot's Visayas and Mindanao stores are supplied via dedicated inter-island shipping lanes from the Cabuyao DC (Luzon) and cross-dock transfers between island hubs.

| Lane | Origin | Destination | Distance (nm) | Transit Time | Frequency | Annual Volume (TEU) |
|------|--------|-------------|---------------|-------------|-----------|---------------------|
| Lane 1 | Manila (South Harbor) | Cebu (CIP) | 350 | 22 hours | Daily (2 vessels) | 4,800 |
| Lane 2 | Manila (South Harbor) | Davao (Sasa Wharf) | 800 | 36 hours | 4x/week | 2,400 |
| Lane 3 | Manila (South Harbor) | Cagayan de Oro (Macabalan) | 540 | 28 hours | 3x/week | 1,800 |
| Lane 4 | Manila (South Harbor) | Iloilo (Intl Port) | 290 | 18 hours | 3x/week | 1,200 |
| Lane 5 | Manila (South Harbor) | General Santos (Makar) | 720 | 34 hours | 2x/week | 720 |
| Lane 6 | Cebu (CIP) | Davao (Sasa Wharf) | 250 | 14 hours | Daily | 1,800 |
| Lane 7 | Cebu (CIP) | Cagayan de Oro | 130 | 8 hours | 5x/week | 1,200 |
| Lane 8 | Cebu (CIP) | Iloilo | 160 | 10 hours | 4x/week | 960 |
| Lane 9 | Cebu (CIP) | Zamboanga | 280 | 16 hours | 2x/week | 480 |
| Lane 10 | Batangas Port | Calapan, Mindoro | 22 | 2.5 hours | Daily (RO-RO) | 600 |

### 20.5.2 RO-RO (Roll-On, Roll-Off) Operations

RO-RO services are used for routes where self-propelled trucks drive onto ferries, eliminating container handling and reducing transfer time.

| RO-RO Route | Operator | Distance (km by sea) | Crossing Time | Frequency | Truck Types | Annual Trips |
|-------------|----------|----------------------|---------------|-----------|-------------|-------------|
| Batangas — Calapan (Mindoro) | FastCat | 52 km | 2.5 hours | 6x/day | All types | 2,400 |
| Batangas — Roxas (Mindoro) | Starhorse | 80 km | 3.5 hours | 3x/day | Wing vans, forward cabs | 1,200 |
| Cebu — Tagbilaran (Bohol) | Lite Shipping | 72 km | 2 hours | 4x/day | All types | 1,800 |
| Cebu — Ormoc (Leyte) | Roble Shipping | 180 km | 5 hours | 2x/day | Wing vans, forward cabs | 960 |
| Cebu — Dumaguete | George & Peter Lines | 130 km | 4 hours | 2x/day | Wing vans | 720 |
| Dapitan — Dumaguete | FastCat | 140 km | 4 hours | 1x/day | All types | 360 |
| Matnog (Sorsogon) — Allen (Samar) | Montenegro Lines | 30 km | 1.5 hours | 8x/day | All types | 3,200 |
| Liloan (S. Leyte) — Lipata (Surigao) | FastCat | 25 km | 1 hour | 6x/day | All types | 2,400 |

**RO-RO Standard Operating Procedure:**

| Step | Activity | Responsible | System |
|------|----------|-------------|--------|
| 1 | Truck arrives at port; driver presents booking confirmation and cargo manifest | Driver | TMS booking |
| 2 | Port security inspects vehicle and cargo; verifies documentation | Port Security / PPA | — |
| 3 | Truck proceeds to RO-RO vessel queue; priority lane for perishable/temp-sensitive | Driver | — |
| 4 | Vessel loading — driver drives truck onto vessel deck; chocks placed on wheels | Vessel Crew | — |
| 5 | Driver disembarks to passenger deck (mandatory) | Driver | — |
| 6 | Vessel departs; GPS tracking continues via vessel AIS | — | TMS tracking |
| 7 | Vessel arrives at destination port; truck disembarks | Driver | — |
| 8 | Port exit clearance; cargo manifest validated by destination port | Port Authority | — |
| 9 | Truck proceeds to destination warehouse or store | Driver | TMS navigation |

### 20.5.3 Port Operations

| Port | Terminal Used | Monthly Container Volume (TEU) | Average Dwell Time (days) | Monthly Port Charges (PHP M) |
|------|-------------|-------------------------------|--------------------------|-----------------------------|
| Manila South Harbor | ATI / ICTSI | 400 | 1.5 | 8.5 |
| Manila North Harbor | Manila North Harbor Port Inc. | 150 | 2.0 | 4.2 |
| Batangas Port | Asian Terminal Inc. | 120 | 1.0 | 2.8 |
| Cebu International Port | Cebu Port Authority | 350 | 1.5 | 6.5 |
| Davao — Sasa Wharf | Davao Port (PPA) | 180 | 2.0 | 4.0 |
| Cagayan de Oro — Macabalan | PPA | 120 | 1.5 | 2.8 |
| Iloilo International Port | PPA | 80 | 1.5 | 2.0 |
| General Santos — Makar | PPA | 50 | 2.0 | 1.2 |

**Port Congestion Mitigation Strategies:**

| Strategy | Implementation | Responsible |
|----------|---------------|-------------|
| Advance booking (48-hour window) | All Manila and Cebu port calls booked via shipping line portal | Dispatch Coordinator |
| Off-peak scheduling | Prioritize night and early morning vessel arrivals when possible | Regional Transportation Manager |
| Container pre-staging | Stage loaded containers at off-dock CY (container yard) 24 hours before vessel loading | Fleet Supervisor |
| Direct drayage agreements | Contracted drayage operators with priority lane access at port | 3PL Relationship Manager |
| Alternative port usage | Divert to Batangas Port when Manila ports congested (>5 day dwell) | Director of Transportation |
| Buffer inventory at island DCs | Maintain 14-day safety stock at Cebu and Davao DCs vs. 7-day at Cabuyao | Supply Planning |

### 20.5.4 Container Management

| Container Type | Owned | Leased | Monthly Throughput | Lease Cost (PHP/month) |
|---------------|-------|--------|-------------------|----------------------|
| 20ft Standard (dry) | 40 | 80 | 400 units moved | 18,000 per unit |
| 40ft Standard (dry) | 20 | 30 | 150 units moved | 28,000 per unit |
| 20ft High Cube | 10 | 20 | 80 units moved | 20,000 per unit |
| 40ft High Cube | 5 | 15 | 40 units moved | 32,000 per unit |
| 20ft Open Top (for tall/bulky) | 0 | 10 | 20 units moved | 25,000 per unit |

**Container Tracking (Oracle TMS):**

| Tracking Point | Data Captured | Oracle TMS Function |
|---------------|--------------|-------------------|
| Container loaded at warehouse | Container ID, seal number, contents, weight | Shipment creation |
| Container dispatched to port | Dispatch time, truck ID, driver | Movement tracking |
| Container gated in at port | Gate-in timestamp | Event update |
| Container loaded on vessel | Vessel name, voyage number, ETD | Vessel tracking |
| Container discharged at destination port | Discharge timestamp | Event update |
| Container gated out from port | Gate-out timestamp, drayage truck ID | Movement tracking |
| Container delivered to DC | Arrival timestamp, unloading confirmation | Delivery confirmation |
| Empty container return | Return timestamp, condition assessment | Container lifecycle |

---

## 20.6 Store Delivery Operations

### 20.6.1 Delivery Confirmation Process

| Step | Activity | Responsible | System | Timing |
|------|----------|-------------|--------|--------|
| 1 | TMS generates delivery manifest and route plan | System (auto) | TMS | Day -1 |
| 2 | WMS completes pick-pack-ship per SOP-SCM-003 | Warehouse team | WMS | Day 0 (5:00 AM – 6:00 AM) |
| 3 | Driver receives dispatch packet (manifest, route, special instructions) | Dispatch Coordinator | TMS print | Day 0 (6:00 AM) |
| 4 | Driver conducts pre-trip inspection; confirms vehicle readiness | Driver | Fleet checklist | Day 0 (6:00 AM) |
| 5 | Truck departs warehouse; GPS tracking activated | Driver | TMS + GPS | Day 0 (6:30 AM) |
| 6 | Driver arrives at store; calls store receiving 15 min before arrival | Driver | Phone/TMS mobile | Per schedule |
| 7 | Store receiving team unloads goods; counts against manifest | Store Receiving Associate | POS Receiving | Within receiving window |
| 8 | Discrepancies noted on delivery manifest (over/short/damaged) | Store Receiving Associate | POS Receiving | During receiving |
| 9 | Store representative signs manifest; driver countersigns | Store Supervisor + Driver | Paper manifest | End of receiving |
| 10 | Driver photographs signed manifest and uploads via TMS mobile app | Driver | TMS Mobile | Before departure |
| 11 | Driver proceeds to next stop or returns to warehouse | Driver | TMS | Per route plan |
| 12 | POD automatically reconciled in TMS against delivery plan | System (auto) | TMS | End of day |
| 13 | Discrepancies routed to inventory control for investigation | Inventory Control Clerk | Inventory + TMS | Day 0 or Day +1 |
| 14 | In-transit inventory cleared; store inventory incremented | System (auto) | Inventory Management | Upon POD confirmation |

### 20.6.2 Proof of Delivery (POD) Management

| POD Element | Required | Format | Retention |
|------------|----------|--------|-----------|
| Signed delivery manifest (store rep signature) | Yes | Paper original + digital photo | 7 years |
| Store receiving stamp with date | Yes | Paper original + digital photo | 7 years |
| Quantity received confirmation (per line item) | Yes | TMS mobile entry + POS receiving | 7 years |
| Discrepancy documentation (photos of damage) | If applicable | Digital photo in TMS mobile | 7 years |
| GPS location stamp at delivery point | Yes (automatic) | TMS system record | 3 years |
| Delivery timestamp | Yes (automatic) | TMS system record | 3 years |
| Driver notes (access issues, refusals) | If applicable | TMS mobile text entry | 3 years |
| Returns/RTV items picked up | If applicable | TMS mobile + Inventory return order | 7 years |

**POD Processing SLA:**

| Activity | Target | Measured By |
|----------|--------|-------------|
| POD upload by driver | Within 2 hours of last delivery | TMS mobile upload timestamp |
| POD review by Dispatch Coordinator | Within 4 hours of receipt | TMS review status |
| Discrepancy escalation to Inventory Control | Within 24 hours of POD upload | TMS escalation log |
| Discrepancy resolution | Within 5 business days | TMS + Inventory case closure |
| Paper manifest return to warehouse | Within 48 hours of route completion | Physical manifest log |

### 20.6.3 Delivery Scheduling with Stores

| Scheduling Type | Trigger | System | Lead Time | Change Window |
|----------------|---------|--------|-----------|---------------|
| Regular replenishment (planned) | Supply planning auto-generates transfer order (PROC-SCM-001) | SCP → TMS | 1-2 days | Before 12:00 PM Day -1 |
| Urgent replenishment (stock-out) | Store Manager or auto-trigger from POS stock level | POS → Inventory → TMS | Same day / next day | Before 6:00 AM same day |
| Promotional stock delivery | Promotional calendar + allocation plan | SCP → TMS | 2-3 days before promo start | Before 12:00 PM Day -2 |
| Direct vendor delivery (DSD) | Vendor PO and ASN | Purchasing → TMS | Per vendor lead time | Per PO agreement |
| B2B customer delivery from store | Customer order processed at Pro Desk | Order Management → TMS | Per customer SLA | Before 12:00 PM Day -1 |

### 20.6.4 Store Receiving Window Compliance

| Metric | Target | Current Performance | Measurement |
|--------|--------|-------------------|-------------|
| Delivery within scheduled window | >= 92% | 90.4% | TMS timestamp vs. store window |
| Early arrival (before window) | <= 5% | 4.2% | TMS timestamp vs. store window |
| Late arrival (after window) | <= 8% | 9.6% | TMS timestamp vs. store window |
| Failed delivery (refused/could not receive) | <= 1% | 0.8% | POD status: refused |
| Average unloading time per store | <= 45 min | 38 min | GPS dwell time at store |

---

## 20.7 B2B Customer Delivery

### 20.7.1 B2B Delivery Segments

Tahanan Depot serves contractor and developer customers through dedicated B2B delivery operations, managed under the Pro Desk program.

| Segment | Customer Profile | Avg Order Value (PHP) | Delivery SLA | Delivery Mode |
|---------|-----------------|----------------------|-------------|---------------|
| Large Developer | Top 20 national developers (Avida, DMCI, Megaworld, etc.) | 500,000 – 5,000,000 | 48 hours from order confirmation | Dedicated truck; scheduled delivery |
| Medium Developer | Regional developers (50+ units per project) | 100,000 – 500,000 | 72 hours | Dedicated or consolidated truck |
| Small Contractor | Independent contractors; small projects | 20,000 – 100,000 | 3-5 business days | Consolidated delivery |
| Institutional | Schools, hospitals, government projects | 50,000 – 2,000,000 | Per contract terms | Dedicated truck; site delivery |
| Interior Designer / Architect | Design-build firms | 10,000 – 200,000 | 3-5 business days | Consolidated or 3PL last-mile |
| DIY Homeowner (B2B-size order) | Homeowners with large projects | 15,000 – 100,000 | 3-5 business days | Consolidated or 3PL last-mile |

### 20.7.2 B2B Delivery Process (Oracle Order Management + TMS)

| Step | Activity | System | Oracle Module |
|------|----------|--------|---------------|
| 1 | B2B customer places order via Pro Desk, B2B portal, or sales rep | CX Commerce / SFA | Commerce / Sales |
| 2 | Order entered in Order Management; credit check performed | Order Management | Order Management + Receivables |
| 3 | Order scheduled; fulfillment location determined (nearest warehouse or store) | GOP | Global Order Promising |
| 4 | Transfer/sales order released to WMS for picking | WMS | Warehouse Management |
| 5 | TMS creates delivery plan; route and vehicle assigned | TMS | Transportation Management |
| 6 | Delivery date and time window communicated to customer | TMS → CX Notification | TMS + CX |
| 7 | Customer receives pre-delivery notification (SMS/email) with ETA | CX Service | Service |
| 8 | Driver delivers to customer site; unloads per delivery instructions | TMS Mobile | Transportation Management |
| 9 | Customer signs POD; photos of delivered goods captured | TMS Mobile | Transportation Management |
| 10 | POD uploaded; delivery confirmed in Order Management | TMS → OM | Transportation Management + Order Management |
| 11 | Invoice generated and sent to customer | Receivables | Receivables |
| 12 | Delivery feedback survey sent to customer | CX Service | Service |

### 20.7.3 White-Glove Delivery Service (Appliances and High-Value Items)

White-glove delivery is provided for large appliances (refrigerators, washing machines, air conditioners, water heaters) and high-value items requiring installation.

| Item Category | Delivery Fee (PHP) | Installation Included | Service Time | Coordination |
|--------------|-------------------|----------------------|-------------|-------------|
| Window-type aircon (< 1.5 HP) | 1,500 | Yes (wall mounting) | 1-2 hours | Oracle Field Service dispatch |
| Split-type aircon | 3,500 | Yes (indoor + outdoor unit) | 3-4 hours | Oracle Field Service dispatch |
| Refrigerator (single door) | 800 | No (placement only) | 30 min | Standard delivery |
| Refrigerator (multi-door / side-by-side) | 1,200 | No (placement only) | 45 min | Standard delivery |
| Washing machine | 1,000 | Yes (water line + drain hook-up) | 1 hour | Oracle Field Service dispatch |
| Water heater | 1,500 | Yes (electrical + plumbing) | 2 hours | Oracle Field Service dispatch |
| Built-in oven / cooktop | 2,000 | Yes (electrical + gas connection) | 2-3 hours | Oracle Field Service dispatch + licensed gas fitter |
| Bathtub / shower enclosure | 2,500 | Yes (plumbing) | 3-4 hours | Oracle Field Service dispatch + licensed plumber |
| Generator set | 2,000 | Yes (electrical hook-up) | 2 hours | Oracle Field Service dispatch |

**White-Glove Delivery Coordination via Oracle Field Service:**

| Step | Activity | System |
|------|----------|--------|
| 1 | Customer purchases appliance with installation option | POS / CX Commerce |
| 2 | Order triggers Field Service work order creation | Order Management → Field Service |
| 3 | Field Service assigns technician based on skill, location, and availability | Oracle Field Service (auto-dispatch) |
| 4 | Technician confirms appointment; customer receives notification with time slot | Field Service → CX Notification |
| 5 | Delivery truck and technician coordinated for same-day arrival | TMS + Field Service scheduling |
| 6 | Technician performs installation per manufacturer specifications | Field Service mobile app |
| 7 | Customer signs installation acceptance form | Field Service mobile app |
| 8 | Photos of completed installation uploaded | Field Service mobile app |
| 9 | Work order closed; warranty start date recorded | Field Service |
| 10 | Post-installation satisfaction survey sent | CX Service |

### 20.7.4 B2B Delivery Performance Targets

| Metric | Target | Current | Measurement |
|--------|--------|---------|-------------|
| On-time delivery (within promised window) | >= 95% | 93.8% | TMS delivery vs. promised date |
| Order completeness (no backorders on delivery) | >= 97% | 96.2% | Delivered qty vs. ordered qty |
| Damage rate (B2B deliveries) | <= 0.3% | 0.25% | Claims / total deliveries |
| Customer satisfaction (delivery experience) | >= 4.5 / 5.0 | 4.3 | Post-delivery survey |
| Installation first-time completion rate | >= 92% | 89.5% | Field Service closure codes |

---

## 20.8 Special Handling

### 20.8.1 Heavy and Bulky Items

Heavy and bulky items (cement, steel bars, lumber, plywood, gypsum boards, tiles) represent approximately 25% of Tahanan Depot's volume but 55% of transportation cost due to specialized handling requirements.

| Item Category | Weight per Unit | Handling Equipment | Vehicle Type | Special Requirement |
|--------------|----------------|-------------------|-------------|-------------------|
| Portland cement (40kg bag) | 40 kg | Forklift; pallet jack | 10W Dropside / Flatbed | Keep dry; stack max 10 high on pallet; tarpaulin cover |
| Reinforcing steel bars (deformed, 12m) | 25-50 kg/pc | Boom truck crane; forklift | 10W Dropside / Flatbed with boom | Bundle with steel straps; flag for over-length per LTO |
| Structural steel (I-beam, angle bar) | Varies | Boom truck crane | 10W Flatbed with boom | Over-length permit if > 12m; red flag at rear |
| Plywood / OSB (4'x8' sheets) | 15-25 kg/pc | Manual; forklift | 10W Wing Van / Dropside | Flat stacking; edge protection; keep dry |
| Gypsum board (4'x8' sheets) | 22-28 kg/pc | Manual; suction lift | 10W Wing Van | Vertical transport stand; flat stacking |
| Ceramic tiles (box, 1 sqm) | 18-25 kg/box | Manual; forklift | 10W Wing Van | Fragile; do not stack > 5 boxes high; palletize |
| Ready-mix concrete (bagged) | 40-50 kg/bag | Forklift; pallet jack | 10W Dropside | Keep dry; FIFO; heavy-duty pallet |
| Lumber (treated, 2x4x8 to 2x12x16) | 8-40 kg/pc | Manual; boom truck | 10W Dropside / Flatbed | Over-length flag; bundle with straps; cover |
| Bathroom fixtures (toilet, sink) | 15-30 kg | Manual | 6W Forward Cab / Wing Van | Individual boxed; fragile handling |
| Bathtub (acrylic / cast iron) | 25-60 kg | Two-person lift; dolly | 6W Forward Cab / Boom truck | Fragile; boxed; white-glove for installation |

**Heavy/Bulky Loading Standards:**

| Parameter | Standard | Compliance |
|-----------|----------|-----------|
| Maximum floor loading (wing van) | 800 kg/sqm evenly distributed | Pre-load weight check |
| Maximum floor loading (flatbed) | 1,200 kg/sqm evenly distributed | Pre-load weight check |
| Axle weight limit (10-wheeler) | 13,500 kg per tandem axle set | LTO MVIS weighbridge |
| GVW limit (10-wheeler) | 26,000 kg gross vehicle weight | LTO regulation; weighbridge verification |
| Load securing | Minimum 4 ratchet straps per load; steel banding for steel bars | DOTC load securing guidelines |
| Over-length marking | Red flag/cloth at least 30cm x 30cm at rear overhang | LTO requirement for loads > vehicle length |
| Over-width marking | Red flags on both sides if > 2.6m wide | LTO requirement |
| Tarpaulin requirement | Required for cement, bagged goods, gypsum, lumber, plywood | Company policy; damage prevention |

### 20.8.2 Hazardous Materials

Tahanan Depot carries select hazardous materials classified under the Philippine Department of Environment and Natural Resources (DENR) and Department of Health (DOH) regulations.

| Item Category | UN Classification | Hazard Class | Handling Requirement | Storage Limit |
|--------------|-------------------|-------------|---------------------|---------------|
| Paint (oil-based) | UN1263 | Class 3 (Flammable) | No smoking; keep away from ignition source; ventilate | 500 liters per vehicle |
| Paint thinner / solvent | UN1263 / UN1270 | Class 3 (Flammable) | Same as paint; fire extinguisher required in vehicle | 200 liters per vehicle |
| LPG cylinders (for demo/display) | UN1075 | Class 2.1 (Flammable Gas) | Upright position only; valve cap on; ventilation | 4 cylinders per vehicle |
| Pesticides / insecticides | UN2902 / UN3082 | Class 6.1 (Toxic) / Class 9 | Segregated from food items; PPE required | Per EPA registration |
| Muriatic acid (hydrochloric acid) | UN1789 | Class 8 (Corrosive) | Acid-resistant container; spill kit required | 50 liters per vehicle |
| Pool chemicals (chlorine) | UN1845 / UN2468 | Class 5.1 (Oxidizer) / Class 9 | Keep dry; segregate from acids | 100 kg per vehicle |
| Construction adhesives | UN1133 | Class 3 (Flammable) | Keep away from heat; ventilate | 200 liters per vehicle |
| Aerosol products | UN1950 | Class 2.1 (Flammable Gas) | Keep below 50°C; no puncturing | 500 units per vehicle |

**Hazmat Transport Compliance:**

| Requirement | Regulation | Responsible | Frequency |
|------------|-----------|-------------|-----------|
| Hazmat driver training and certification | DENR AO 2015-07 + DOH AO 2016-0004 | Fleet Supervisor | Annual recertification |
| Vehicle hazmat placarding | DENR / DOTC regulations | Driver | Every hazmat trip |
| Fire extinguisher (minimum 2x 4.5kg dry chemical) | Fire Code of the Philippines (RA 9514) | Fleet Supervisor | Annual inspection + monthly visual |
| Spill kit in vehicle | DENR requirement | Driver | Pre-trip check; replenish after use |
| Emergency contact card (CHEMTREC / local emergency) | Company policy | Dispatch Coordinator | Every dispatch |
| Manifest documentation (hazmat declaration) | DENR / PPA for inter-island | Dispatch Coordinator | Every hazmat shipment |
| Storage segregation in vehicle | DENR compatibility matrix | Loader + Driver | Every load |

### 20.8.3 Fragile Items

| Item Category | Fragile Handling Protocol | Packaging Standard | Loss Rate Target |
|--------------|--------------------------|-------------------|-----------------|
| Glass sheets (4'x8') | Vertical transport in A-frame rack; no stacking; padded separators | Edge protectors; A-frame rack | <= 2% |
| Sanitary ware (toilets, sinks) | Individual boxed; no stacking above 2 units; padded in vehicle | Manufacturer double-wall carton + foam inserts | <= 1% |
| Light fixtures (chandeliers, pendant lights) | Individual boxed; top-load only; secured to prevent movement | Custom foam packaging; "FRAGILE" label on all sides | <= 0.5% |
| Mirrors | Vertical transport; blanket-wrapped; secured upright | Bubble wrap + corner protectors + "FRAGILE" label | <= 1.5% |
| Glass mosaic tiles | Palletized; no loose stacking; shrink-wrapped | Pallet + corrugated wrap + stretch film | <= 1% |
| Decorative items (vases, jars) | Individual wrap; top-load only; padded | Bubble wrap + individual carton | <= 2% |

### 20.8.4 Temperature-Sensitive Items

| Item Category | Temp Range | Transport Mode | Max Transit Time | Monitoring |
|--------------|-----------|---------------|-----------------|-----------|
| Water-based paint | 10°C – 35°C | Reefer van (if > 30°C ambient) or insulated van | 8 hours | Temp data logger per shipment |
| Construction adhesives | 5°C – 30°C | Reefer van (if > 30°C ambient) | 8 hours | Temp data logger per shipment |
| Wood stain / varnish | 10°C – 35°C | Insulated van or reefer | 8 hours | Visual inspection on delivery |
| Epoxy resins (two-part) | 10°C – 30°C | Reefer van required (Apr-Oct) | 6 hours | Temp data logger per shipment |
| Live plants (garden center) | 15°C – 30°C | Ventilated van; no direct sun | 4 hours | Visual inspection; watering schedule |

---

## 20.9 Driver Management

### 20.9.1 Driver Qualifications

| Requirement | Standard | Verification |
|------------|---------|-------------|
| Professional driver's license (LTO) | Restriction codes 1, 2, and/or 3 (heavy vehicle) | License copy on file; LTO verification |
| Minimum age | 25 years old | Government-issued ID |
| Minimum driving experience | 3 years commercial driving | Employment certificates; LTO license issue date |
| Educational attainment | At least high school graduate or K-12 completer | Diploma / ALS certificate |
| Physical fitness | Medical certificate from DOH-accredited physician; 20/40 vision or corrected | Annual medical examination |
| Drug test | Negative result from DOH-accredited laboratory | Pre-employment + annual + random |
| Background check | No criminal record; clean LTO driving record | NBI clearance + LTO driving history |
| Defensive driving certificate | LTO-accredited or Tahanan-certified defensive driving course | Certificate on file |
| Hazmat training (if assigned to hazmat routes) | DENR-accredited hazmat transport training | Certificate on file |

### 20.9.2 Driver Workforce Summary

| Region | Company Drivers | Contract Drivers (3PL) | Total | Avg Tenure (years) |
|--------|----------------|----------------------|-------|-------------------|
| Luzon | 85 | 40 | 125 | 4.2 |
| Visayas | 35 | 25 | 60 | 3.8 |
| Mindanao | 30 | 20 | 50 | 3.5 |
| **Total** | **150** | **85** | **235** | **3.9** |

### 20.9.3 Driver Training Program

| Training Module | Duration | Frequency | Provider | Oracle Module |
|----------------|----------|-----------|----------|---------------|
| Defensive Driving | 2 days | Annual | Tahanan-certified instructor | Oracle Learning |
| Vehicle Inspection and Maintenance Awareness | 4 hours | Semi-annual | Fleet Supervisor | Oracle Learning |
| Cargo Securing and Load Distribution | 4 hours | Annual | Fleet Supervisor | Oracle Learning |
| Customer Service for Delivery Drivers | 4 hours | Annual | CX Training team | Oracle Learning |
| Hazmat Transport (for designated drivers) | 1 day | Annual | DENR-accredited provider | Oracle Learning |
| Emergency Response and Accident Protocol | 4 hours | Annual | Safety Officer | Oracle Learning |
| GPS / TMS Mobile App Usage | 2 hours | Upon hire + system updates | IT + Dispatch team | Oracle Learning |
| First Aid and Basic Fire Fighting | 4 hours | Annual | Red Cross PH certified provider | Oracle Learning |
| Route Familiarization (new routes) | 1 day (ride-along) | As needed | Senior driver + Fleet Supervisor | — |
| Fuel-Efficient Driving Techniques | 2 hours | Semi-annual | Fleet Supervisor | Oracle Learning |

### 20.9.4 Hours of Service and Fatigue Management

Compliance with DOLE Department Order No. 118-12 (Rules on Overtime Work) and company fatigue management policy.

| Rule | Standard | Monitoring |
|------|----------|-----------|
| Maximum driving hours per shift | 10 hours | GPS driving time + driver log |
| Mandatory rest break | 1 hour after 5 consecutive hours driving | Driver self-report + GPS |
| Maximum on-duty hours per shift | 12 hours (driving + loading/unloading) | GPS + dispatch records |
| Minimum rest period between shifts | 9 consecutive hours off-duty | Dispatch scheduling |
| Maximum driving hours per week | 60 hours | Weekly driver log review |
| Maximum consecutive working days | 6 days (1 rest day per week per Labor Code) | Dispatch scheduling |
| Night driving restriction (inter-island RO-RO) | No RO-RO crossing after 10:00 PM without relief driver | Dispatch scheduling |
| Curfew areas (conflict zones in Mindanao) | No driving between 8:00 PM and 5:00 AM in designated areas | Route planning; security advisory |

### 20.9.5 Drug Testing Program

| Test Type | Frequency | Laboratory | Consequence of Positive Result |
|-----------|-----------|-----------|-------------------------------|
| Pre-employment | Upon hire | DOH-accredited lab | Not hired |
| Annual | Anniversary month | DOH-accredited lab | Suspension pending investigation; referral to rehabilitation; termination if confirmed |
| Random (company drivers) | 25% of drivers per quarter (random selection) | DOH-accredited lab | Same as annual |
| Random (3PL drivers) | 10% per quarter (Tahanan-initiated) | DOH-accredited lab | 3PL contract suspension for that driver |
| For-cause / reasonable suspicion | Upon incident or behavioral observation | DOH-accredited lab | Immediate suspension; termination if confirmed |
| Post-accident | Following any accident involving company or contracted vehicle | DOH-accredited lab | Suspension pending results |

### 20.9.6 Driver Safety Equipment

| Equipment | Standard | Quantity per Vehicle | Inspection |
|-----------|----------|---------------------|-----------|
| Seat belts | Functional; driver + passenger | 2 per cab | Pre-trip |
| Reflective vest | ANSI/ISEA 107 Class 2 or equivalent | 2 per vehicle | Monthly |
| Hard hat | Standards-compliant | 2 per vehicle | Monthly |
| Safety shoes | Steel toe | Per driver (personal issue) | As needed |
| Fire extinguisher | 4.5 kg dry chemical ABC | 2 per vehicle (1 cab, 1 cargo) | Monthly visual; annual professional |
| First aid kit | DOH standard kit | 1 per vehicle | Monthly |
| Warning triangles / early warning devices | LTO standard (reflective) | 3 per vehicle | Pre-trip |
| Flashlight / LED work light | Rechargeable; waterproof | 2 per vehicle | Monthly |
| Wheel chocks | Heavy-duty rubber | 2 per vehicle | Pre-trip |
| Spill kit (hazmat vehicles) | Universal spill kit (absorbent, PPE, bags) | 1 per hazmat vehicle | Monthly; replenish after use |

---

## 20.10 Fuel Management

### 20.10.1 Fuel Card Program

Tahanan Depot issues fuel cards to all company drivers through a managed fleet card program with Petron and Shell Philippines.

| Fuel Card Provider | Cards Issued | Coverage | Monthly Volume (liters) | Discount |
|-------------------|-------------|---------|------------------------|----------|
| Petron Fleet Card | 120 | Luzon, Visayas, Mindanao | 280,000 | PHP 2.00/liter |
| Shell Fleet Card | 80 | Luzon, Mindanao | 150,000 | PHP 1.75/liter |
| Caltex Star Card | 40 | Visayas, Mindanao | 60,000 | PHP 1.50/liter |
| **Total** | **240** | **Nationwide** | **490,000** | **Blended: PHP 1.83/liter** |

**Fuel Card Controls:**

| Control | Rule | Enforcement |
|---------|------|-------------|
| Vehicle-to-card binding | Each card linked to specific vehicle plate number | Fuel card system enforcement |
| Fuel type restriction | Diesel only (except crew cab gasoline) | Fuel card system enforcement |
| Daily limit | PHP 5,000 per card per day | Fuel card system enforcement |
| Monthly limit | Based on vehicle type allocation | Fuel card system + analyst review |
| Transaction location | Must be along planned route (within 5 km radius) | GPS cross-reference (monthly audit) |
| Time restriction | Fueling only between 5:00 AM and 9:00 PM (unless overnight route) | Fuel card system + analyst review |
| Odometer reading | Required at every fueling | Driver entry at pump |
| Receipt submission | Required within 24 hours via TMS mobile | TMS mobile upload |

### 20.10.2 Fuel Consumption Targets

| Vehicle Type | Target Consumption (km/liter) | Actual (LTM) | Variance | Target Monthly Liters (avg) |
|-------------|-------------------------------|--------------|----------|---------------------------|
| 10W Wing Van (loaded) | 4.0 | 3.7 | -7.5% | 3,750 |
| 10W Wing Van (empty return) | 5.5 | 5.2 | -5.5% | — |
| 10W Dropside (loaded) | 4.2 | 3.9 | -7.1% | 3,200 |
| 6W Forward Cab (loaded) | 5.5 | 5.1 | -7.3% | 2,200 |
| 6W Flatbed (loaded) | 5.0 | 4.7 | -6.0% | 2,400 |
| 4W Dropside (loaded) | 7.5 | 7.1 | -5.3% | 1,400 |
| Reefer Van | 3.5 (includes reefer unit) | 3.3 | -5.7% | 3,800 |
| Boom Truck | 3.8 | 3.5 | -7.9% | 3,600 |
| Crew Cab | 10.0 | 9.5 | -5.0% | 600 |

### 20.10.3 Fuel Efficiency Initiatives

| Initiative | Description | Expected Savings | Status |
|-----------|-------------|-----------------|--------|
| Route optimization (Oracle TMS) | Reduce total km traveled by optimizing multi-stop routes | 8% reduction in total km | Active |
| Idle reduction policy | Maximum 5 minutes idle time; automatic engine shutdown after 5 min | 3% fuel savings | Active |
| Tire pressure monitoring | Monthly tire pressure check; under-inflation increases consumption by 2% per 5 PSI | 2% fuel savings | Active |
| Driver training — eco-driving | Training module on fuel-efficient driving (smooth acceleration, anticipatory braking, optimal RPM) | 5% fuel savings per trained driver | Active (85% trained) |
| Vehicle replacement (older units) | Replace units > 7 years with fuel-efficient models | 15% improvement per replaced unit | In progress (12 units FY2026) |
| Aerodynamic improvements | Roof deflectors and side skirts on wing vans | 2% fuel savings at highway speed | Pilot (10 units) |

---

## 20.11 Transportation Cost Management

### 20.11.1 Annual Transportation Budget

| Cost Category | Budget (PHP M) | % of Total | Cost Per Unit | Notes |
|--------------|---------------|------------|--------------|-------|
| Owned fleet fuel | 720.0 | 22.5% | PHP 6.10/km | Based on 118M km annually |
| Owned fleet maintenance | 320.0 | 10.0% | PHP 1.93M/vehicle/year | Includes tires, PM, repairs |
| Owned fleet depreciation | 280.0 | 8.8% | PHP 1.69M/vehicle/year | 5-year straight line |
| Owned fleet insurance | 96.0 | 3.0% | PHP 578K/vehicle/year | Comprehensive + cargo |
| Owned fleet registration/LTO | 12.0 | 0.4% | PHP 72K/vehicle/year | Registration, inspection, permits |
| 3PL store delivery | 420.0 | 13.1% | PHP 96/drop average | ~4.4M drops/year |
| 3PL inter-island freight | 680.0 | 21.3% | PHP 18,200/TEU average | ~37,300 TEU/year |
| 3PL last-mile B2B | 118.0 | 3.7% | PHP 280/delivery average | ~421K deliveries/year |
| 3PL heavy/bulky specialized | 195.0 | 6.1% | PHP 650/delivery average | ~300K deliveries/year |
| Driver compensation (company) | 180.0 | 5.6% | PHP 120K/driver/month | Salary + benefits + OT + allowances |
| Port charges and handling | 144.0 | 4.5% | PHP 320/TEU average | Wharfage, arrastre, documentation |
| Toll fees | 72.0 | 2.2% | — | NLEX, SLEX, STAR, TPLEX, CTTEX |
| Container lease and management | 55.2 | 1.7% | PHP 23K/container/year | 2,400 leased containers |
| Safety and compliance | 18.0 | 0.6% | — | Drug tests, training, equipment |
| Transportation team salaries | 48.0 | 1.5% | — | Management and analyst staff |
| **Total Transportation** | **3,200.2** | **100%** | | **1.78% of revenue (PHP 45B)** |

### 20.11.2 Freight Cost Allocation

Freight costs are allocated to receiving locations (stores and warehouses) for accurate landed cost and margin analysis, processed through Oracle Cost Management.

| Allocation Method | Application | Oracle Module |
|------------------|-------------|---------------|
| Per-unit weight (kg) | Heavy/bulky items — cement, steel, lumber | Cost Management (landed cost rule) |
| Per-unit volume (cbm) | Voluminous lightweight items — insulation, packaging | Cost Management (landed cost rule) |
| Per-drop (flat rate) | Store replenishment deliveries — fixed per zone | Cost Management (allocation rule) |
| Per-TEU (inter-island) | Containerized shipments to VisMin | Cost Management (landed cost rule) |
| Per-delivery (B2B) | Customer deliveries — fixed per zone | Cost Management (allocation rule) |
| Proportional (weight × distance) | Mixed loads with multiple stops | Cost Management (advanced allocation) |

### 20.11.3 Cost-per-Delivery Tracking

| Delivery Type | Cost per Delivery (PHP) | Cost per KM (PHP) | Cost per KG (PHP) | Target (YoY Reduction) |
|--------------|------------------------|-------------------|-------------------|----------------------|
| Store replenishment (Luzon) | 4,200 | 28.50 | 0.42 | -3% |
| Store replenishment (Visayas, with RO-RO) | 8,500 | 42.00 | 0.85 | -2% |
| Store replenishment (Mindanao, with RO-RO) | 9,800 | 45.00 | 0.98 | -2% |
| B2B customer delivery (Luzon) | 1,800 | 22.00 | 0.55 | -3% |
| B2B customer delivery (VisMin) | 3,200 | 35.00 | 0.80 | -2% |
| Inter-island container (per TEU, Manila-Cebu) | 18,200 | — | — | -2% |
| Inter-island container (per TEU, Manila-Davao) | 25,400 | — | — | -2% |
| Heavy/bulky specialized delivery | 3,500 | 38.00 | 0.35 | -2% |

### 20.11.4 Cost Optimization Initiatives

| Initiative | Description | Annual Savings Target (PHP M) | Timeline | Status |
|-----------|-------------|-------------------------------|----------|--------|
| Oracle TMS full deployment | Complete route optimization for all 4 regions; eliminate manual route planning | 45.0 | Q2 2026 | 75% complete |
| Load consolidation improvement | Increase average truck utilization from 78% to 88% through better wave planning | 35.0 | Q3 2026 | In progress |
| 3PL rate renegotiation | Annual rate negotiation leveraging volume growth and multi-year commitment | 28.0 | Q1 2026 | Completed |
| Backhaul optimization | Fill empty return legs with vendor pickups and RTV items | 18.0 | Q4 2026 | Pilot |
| Fleet right-sizing | Replace under-utilized 10W trucks with 6W in select routes | 12.0 | Q2 2027 | Planning |
| RO-RO lane optimization | Consolidate RO-RO routes; negotiate volume discounts with ferry operators | 15.0 | Q3 2026 | In progress |
| Fuel efficiency program | Eco-driving training + idle reduction + tire pressure management | 22.0 | Ongoing | Active |
| Port dwell time reduction | Reduce average container dwell from 1.8 days to 1.2 days | 8.0 | Q4 2026 | In progress |
| Digital POD elimination | Eliminate paper POD processing through full TMS mobile adoption | 4.0 | Q2 2026 | 90% complete |
| Container lease optimization | Shift from short-term to long-term lease; increase owned containers | 6.0 | Q1 2027 | Planning |

---

## 20.12 Transportation Performance Metrics

### 20.12.1 Key Performance Indicators (KPIs)

| KPI | Definition | Target | Current (LTM) | Frequency | Data Source |
|-----|-----------|--------|---------------|-----------|-------------|
| On-Time Delivery (OTD) — Store | % of store deliveries within scheduled receiving window | >= 92% | 90.4% | Daily/Monthly | TMS |
| On-Time Delivery (OTD) — B2B | % of B2B deliveries within promised delivery window | >= 95% | 93.8% | Daily/Monthly | TMS |
| Delivery Accuracy | % of deliveries with zero quantity discrepancy | >= 99.5% | 99.2% | Monthly | TMS + Inventory |
| Cost per KM | Total transportation cost / total km driven | <= PHP 30/km | PHP 31.2/km | Monthly | TMS + GL |
| Cost per Delivery — Store | Total store delivery cost / number of store deliveries | <= PHP 4,500 | PHP 4,680 | Monthly | TMS + GL |
| Cost per Delivery — B2B | Total B2B delivery cost / number of B2B deliveries | <= PHP 2,000 | PHP 2,150 | Monthly | TMS + GL |
| Vehicle Utilization (weight) | Average load weight / vehicle capacity | >= 85% | 78% | Weekly | TMS + WMS |
| Vehicle Utilization (volume) | Average load volume / vehicle capacity | >= 85% | 82% | Weekly | TMS + WMS |
| Fleet Availability | % of owned vehicles available for dispatch (not in maintenance or repair) | >= 92% | 88% | Daily | Fleet register |
| Average Delivery Lead Time — Luzon | Warehouse dispatch to store receiving confirmation | <= 8 hours | 7.2 hours | Daily | TMS |
| Average Delivery Lead Time — VisMin | Warehouse dispatch to store receiving (incl. inter-island) | <= 48 hours | 52 hours | Daily | TMS |
| Fuel Efficiency | Average km per liter across fleet | >= 5.0 km/L | 4.6 km/L | Monthly | Fuel card + GPS |
| Delivery Incident Rate | Accidents or incidents per 100,000 km driven | <= 0.5 | 0.62 | Monthly | Safety reports |
| POD Submission Timeliness | % of PODs uploaded within 2 hours of delivery | >= 95% | 91.8% | Daily | TMS |
| Driver Attendance | % of scheduled driver shifts filled | >= 96% | 94.5% | Daily | Dispatch records |
| Container Dwell Time | Average days from port gate-in to gate-out | <= 1.5 days | 1.8 days | Monthly | Port reports |
| Backhaul Utilization | % of return trips with revenue or operational load | >= 20% | 12% | Monthly | TMS |

### 20.12.2 KPI Reporting and Review Cadence

| Report | Audience | Frequency | Content | Owner |
|--------|----------|-----------|---------|-------|
| Daily Dispatch Dashboard | Dispatch Coordinators, Fleet Supervisors | Daily (auto-generated) | Routes dispatched, vehicles utilized, deliveries completed, exceptions | System (TMS) |
| Weekly Transportation Performance | Regional Transportation Managers, Director | Weekly (Monday AM) | OTD by region, vehicle utilization, fuel efficiency, incidents | Route Planner |
| Monthly Transportation Scorecard | Director of Transportation, VP Distribution Operations | Monthly (by 5th business day) | All KPIs vs. target; 3PL scorecards; cost analysis; trends | Transportation Cost Analyst |
| Quarterly Business Review (3PL) | VP Distribution Operations, 3PL senior management | Quarterly | Scorecard trends; SLA compliance; rate review; improvement plans | 3PL Relationship Manager |
| Annual Transportation Strategy Review | COO, VP Distribution Operations, CFO | Annual (December) | Year-in-review; budget vs. actual; strategic initiatives; next-year plan | Director of Transportation |

### 20.12.3 Oracle Fusion Analytics — Transportation Dashboard

| Dashboard Component | Visualization | Data Source | Refresh |
|-------------------|--------------|-------------|---------|
| Live fleet map | Vehicle GPS positions on Philippine map | TMS + GPS | Real-time (5 min) |
| Delivery status tracker | Delivery status by store (dispatched, in-transit, delivered, exception) | TMS | Real-time (5 min) |
| OTD trend chart | Daily/weekly/monthly OTD by region | TMS + Analytics | Daily |
| Cost per km trend | Monthly cost per km by vehicle type and region | TMS + GL | Daily |
| Vehicle utilization heat map | Utilization by hour, day, week | TMS + WMS | Daily |
| Fuel consumption trend | Liters per 100 km by vehicle; total fleet consumption | Fuel card + GPS | Weekly |
| Incident tracker | Accidents, breakdowns, delays by type and region | TMS + Safety reports | Daily |
| 3PL performance summary | Scorecard summary by partner | TMS + vendor master | Monthly |
| Inter-island transit time | Average transit time by lane; vessel schedule adherence | TMS + shipping line data | Daily |
| Store delivery exception log | Failed deliveries, refusals, access issues by store | TMS + POD data | Daily |

---

## 20.13 Emergency and Contingency Transportation

### 20.13.1 Typhoon Disruption Protocol

The Philippines experiences an average of 20 typhoons per year, with approximately 5-7 directly impacting Tahanan Depot operations.

| Typhoon Signal Level (PAGASA) | Action | Authority | Timeline |
|-------------------------------|--------|-----------|----------|
| Signal No. 1 (affected areas identified) | Activate typhoon monitoring; review routes in affected regions; pre-position inventory at island DCs | Regional Transportation Manager | Upon PAGASA advisory |
| Signal No. 1 (confirmed impact) | Suspend inter-island RO-RO crossings in affected sea lanes; notify stores of potential delivery delays | Director of Transportation | 24 hours before expected landfall |
| Signal No. 2 | Suspend all truck dispatch in affected areas; recall in-transit vehicles to nearest safe point; activate 3PL contingency | Director of Transportation | Upon Signal No. 2 hoisting |
| Signal No. 3 or above | Complete fleet stand-down in affected areas; secure vehicles in warehouse compounds; driver safety check-in protocol activated | VP Distribution Operations | Upon Signal No. 3 hoisting |
| Post-typhoon (all-clear from PAGASA) | Rapid road network assessment; prioritize emergency deliveries to open stores; activate alternative routes | Regional Transportation Manager | Upon all-clear advisory |
| Post-typhoon (recovery Day 1-3) | Full fleet deployment; priority replenishment to affected stores; damage assessment for vehicles and facilities | Director of Transportation | Days 1-3 post-typhoon |

**Typhoon Season Preparedness (June – November):**

| Preparedness Action | Frequency | Responsible |
|-------------------|-----------|-------------|
| Pre-positioning of 14-day inventory at VisMin DCs (vs. normal 7-day safety stock) | Monthly review during typhoon season | Supply Planning + Director of Transportation |
| Vehicle securing plan reviewed (warehouse compound tie-down; elevated parking for flood-prone yards) | June (pre-season) + before each typhoon | Fleet Supervisor |
| Driver emergency contact list updated | Monthly during typhoon season | Dispatch Coordinator |
| 3PL contingency capacity confirmed (standby agreements for post-typhoon surge) | Quarterly during typhoon season | 3PL Relationship Manager |
| Generator fuel top-up at all DCs | Before each typhoon (upon Signal No. 1) | Warehouse Manager |
| Emergency communication channel activated (Viber group: TD Transport Emergency) | Upon typhoon advisory | Director of Transportation |

### 20.13.2 Vehicle Breakdown Procedure

| Step | Activity | Responsible | Timeline |
|------|----------|-------------|----------|
| 1 | Driver reports breakdown via TMS mobile app (GPS location auto-captured) or phone call to Dispatch | Driver | Immediate |
| 2 | Dispatch Coordinator logs incident in TMS; assigns severity level | Dispatch Coordinator | Within 10 min |
| 3 | If minor (flat tire, belt break, battery): dispatch mobile mechanic from nearest service partner | Fleet Supervisor | Within 30 min |
| 4 | If major (engine, transmission, accident): arrange tow truck and cargo transfer vehicle | Fleet Supervisor + 3PL | Within 1 hour |
| 5 | Notify receiving store(s) of delayed delivery; update TMS ETA | Dispatch Coordinator | Within 15 min of breakdown |
| 6 | If cargo transfer required: arrange alternate vehicle; transfer cargo with inventory count documentation | Fleet Supervisor + Warehouse | Within 2 hours |
| 7 | Load transferred vehicle dispatched to continue route | Dispatch Coordinator | Upon transfer completion |
| 8 | Original vehicle towed to nearest contracted service center | Fleet Supervisor | Same day |
| 9 | Repair authorized; estimated completion communicated | Fleet Supervisor | Within 24 hours |
| 10 | Vehicle returned to service; breakdown report completed in fleet register | Fleet Supervisor | Upon repair completion |
| 11 | Root cause analysis for breakdowns exceeding 24 hours or recurring issues | National Fleet Manager | Within 5 business days |

**Breakdown Severity Levels:**

| Severity | Definition | Response Time | Cargo Action |
|----------|-----------|---------------|-------------|
| Level 1 (Minor) | Flat tire, dead battery, minor electrical; vehicle can be repaired on-site | 1 hour | No transfer needed |
| Level 2 (Moderate) | Belt failure, fuel system, brake issue; requires mobile mechanic | 2 hours | Transfer if delay > 3 hours |
| Level 3 (Major) | Engine, transmission, suspension failure; requires tow | 3 hours | Mandatory cargo transfer |
| Level 4 (Accident) | Vehicle involved in accident; requires police report + insurance | Immediate | Cargo transfer + inventory count at scene |

### 20.13.3 Alternative Routing Procedures

| Scenario | Trigger | Alternative Action | Approval |
|----------|---------|-------------------|----------|
| Road closure (construction, landslide) | LGU/DOTR advisory; driver report | Reroute via TMS alternative route; notify stores of revised ETA | Dispatch Coordinator |
| Flooding (Metro Manila, provincial) | Driver report; PAGASA flood advisory | Reroute to elevated roads; delay delivery if no alternative; activate 3PL for stranded cargo | Fleet Supervisor |
| LGU truck ban (unplanned) | Local ordinance change | Reschedule delivery to permitted window; stage at nearby holding area | Regional Transportation Manager |
| Port congestion (vessel delay > 12 hours) | Shipping line advisory | Divert to alternative port (e.g., Manila → Batangas); hold cargo at origin DC if < 48 hours | Director of Transportation |
| RO-RO cancellation (mechanical, weather) | Ferry operator cancellation | Book next available sailing; if > 24 hours delay, arrange containerized sea freight instead | Regional Transportation Manager |
| Bridge weight restriction (provincial roads) | Driver report; DPWH advisory | Reroute to alternate bridge; dispatch smaller vehicle if no alternative | Dispatch Coordinator |
| Civil disturbance / security concern | PNP/LGU advisory | Avoid affected area; delay delivery; coordinate with security team | Director of Transportation + Security |
| Fuel shortage (regional) | Supplier advisory; DOE bulletin | Reroute to fuel-available areas; top up before entering shortage zone; activate fuel reserve protocol | National Fleet Manager |

### 20.13.4 Business Continuity — Transportation

| Scenario | Probability | Impact | Mitigation | Recovery Time Objective |
|----------|------------|--------|-----------|------------------------|
| Major typhoon (Signal 4-5) affecting Luzon | High (2-3x/year) | Critical (all Luzon operations halted 1-3 days) | Pre-positioned inventory; 3PL surge agreements; fleet insurance | 48 hours post-all-clear |
| Warehouse DC outage (fire, flood) | Low | Critical (regional supply disrupted) | Cross-dock from alternate DC; direct vendor delivery to stores | 72 hours |
| 3PL partner failure (bankruptcy, strike) | Low | High (capacity reduction 15-30%) | Multi-provider strategy; backup 3PL agreements; surge owned fleet | 1 week |
| Port strike (Manila) | Medium | High (VisMin supply chain disrupted) | Pre-positioned inventory (14 days); Batangas Port alternative; air freight for critical items | 2 weeks |
| Fuel supply disruption | Low | High (fleet immobilized) | Fuel reserve (3-day supply at each DC); fuel card provider diversification; priority routing | 1 week |
| IT system outage (Oracle TMS down) | Low | Medium (manual planning required) | Manual dispatch procedures; paper manifests; GPS continues independently | 4 hours (manual); 24 hours (system) |
| Major vehicle recall (safety) | Low | Medium (fleet capacity reduced) | 3PL surge capacity; prioritized store deliveries; phased repair scheduling | Per recall timeline |

---

## 20.14 Appendix — Reference Data

### 20.14.1 Warehouse-to-Store Distance Matrix (Selected, km)

| Origin \ Destination | NCR | Central Luzon | CALABARZON | Bicol | Cebu | Iloilo | Davao | CDO | GenSan | Zamboanga |
|---------------------|-----|--------------|------------|-------|------|--------|-------|-----|--------|-----------|
| Cabuyao DC | 35 | 110 | 45 | 380 | 570 (sea) | 460 (sea) | 880 (sea) | 680 (sea) | 820 (sea) | 780 (sea) |
| Cebu DC | 570 (sea) | 640 (sea) | 580 (sea) | 750 (sea) | 0 | 160 (sea) | 250 (sea) | 130 (sea) | 280 (sea) | 420 (sea) |
| Davao DC | 880 (sea) | 950 (sea) | 900 (sea) | 1050 (sea) | 250 (sea) | 380 (sea) | 0 | 320 | 150 | 400 |

### 20.14.2 Standard Transit Times

| Lane | Mode | Standard Transit Time | Max Acceptable |
|------|------|----------------------|---------------|
| Cabuyao DC → NCR stores | Truck | 4 hours | 8 hours |
| Cabuyao DC → Central Luzon stores | Truck | 6 hours | 10 hours |
| Cabuyao DC → CALABARZON stores | Truck | 5 hours | 8 hours |
| Cabuyao DC → Bicol stores | Truck | 12 hours | 16 hours |
| Cabuyao DC → Cebu DC | Sea (container) | 36 hours | 48 hours |
| Cabuyao DC → Davao DC | Sea (container) | 48 hours | 72 hours |
| Cebu DC → Cebu stores | Truck | 3 hours | 5 hours |
| Cebu DC → Bohol stores | RO-RO + truck | 8 hours | 12 hours |
| Cebu DC → Iloilo stores | RO-RO + truck | 10 hours | 14 hours |
| Cebu DC → Leyte stores | RO-RO + truck | 12 hours | 16 hours |
| Cebu DC → Davao DC | Sea (container) | 24 hours | 36 hours |
| Davao DC → Davao stores | Truck | 3 hours | 5 hours |
| Davao DC → GenSan stores | Truck | 4 hours | 6 hours |
| Davao DC → CDO stores | Truck | 6 hours | 8 hours |
| Davao DC → Zamboanga stores | Truck | 10 hours | 14 hours |

### 20.14.3 SOP and Process Code Cross-Reference

| Code | Title | This Document Section | Primary Oracle Module |
|------|-------|----------------------|----------------------|
| SOP-SCM-003 | Store Replenishment Pick-Pack-Ship | 20.3, 20.6 | WMS + TMS |
| PROC-SCM-001 | Demand-Driven Replenishment | 20.3, 20.6 | SCP + Inventory + TMS |
| PROC-SCM-004 | Import Procurement | 20.5 | TMS + Global Trade Mgmt |
| PROC-FIN-004 | Order-to-Cash (B2B) | 20.7 | Order Management + TMS |
| SOP-SCM-004 | Store Receiving Procedure | 20.6 | Inventory Management |

### 20.14.4 Toll Rate Reference (Major Expressways)

| Expressway | Operator | Class 2 (6-wheel) Rate | Class 3 (10-wheel) Rate | RFID |
|-----------|----------|------------------------|------------------------|------|
| NLEX (Balintawak – Sta. Ines) | NLEX Corp. | PHP 340 | PHP 510 | Easytrip |
| SLEX (Alabang – Calamba) | SMC Infrastructure | PHP 262 | PHP 393 | Autosweep |
| Skyway (Bicutan – Buendia) | SMC Infrastructure | PHP 260 | PHP 390 | Autosweep |
| TPLEX (Tarlac – Pozzorubio) | Private | PHP 195 | PHP 293 | Easytrip |
| STAR Tollway (Sto. Tomas – Batangas) | STAR Infrastructure | PHP 114 | PHP 171 | Autosweep |
| CAVITEX (Manila – Cavite) | CII | PHP 150 | PHP 225 | Easytrip |
| MCX (Muntinlupa – Cavite) | Ayala | PHP 65 | PHP 97 | Autosweep |
| CTTEX (Cavitex – Tagaytay) | MPCALA | PHP 100 | PHP 150 | Easytrip |

### 20.14.5 Document Revision History

| Version | Date | Author | Description |
|---------|------|--------|-------------|
| 1.0 | 2026-04-02 | VP Distribution Operations | Initial document creation — Doc 20 |
| | | | |
| | | | |

---

*This document is part of the Tahanan Depot enterprise documentation set (Document 20 of the Operations series). For related documents, refer to Doc 04 — Business Processes, Doc 06 — Standard Operating Procedures, and Doc 14 — Store Operations Guide.*
