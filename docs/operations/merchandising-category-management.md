# 25 — MERCHANDISING & CATEGORY MANAGEMENT

## 25.1 Merchandising Organization

### 25.1.1 Merchandising Team Structure

```
VP Merchandising & Quality Assurance (reports to COO, dotted line to CFO)
├── Director, Category Management
│   ├── Category Manager — Building Materials & Lumber
│   ├── Category Manager — Electrical & Lighting
│   ├── Category Manager — Plumbing & Water Systems
│   ├── Category Manager — Paint & Decorating
│   ├── Category Manager — Hardware & Tools
│   ├── Category Manager — Appliances
│   ├── Category Manager — Flooring & Tiles
│   ├── Category Manager — Kitchen & Bath
│   ├── Category Manager — Doors & Windows
│   ├── Category Manager — Garden & Outdoor
│   ├── Category Manager — Safety & Security
│   └── Category Manager — Storage & Organization
├── Director, Merchandise Planning & Analytics
│   ├── Merchandise Planners (12 — 1 per category)
│   ├── Pricing Analysts (3)
│   ├── Assortment Analyst (2)
│   └── Space Planning Manager
│       ├── Planogram Specialists (4)
│       └── Space Planning Analysts (2)
├── Director, Merchandise Buying
│   ├── Senior Buyers (6 — 2 per region: Local, Import, Private Label)
│   ├── Buyers (12 — assigned per category)
│   └── Assistant Buyers / Merchandise Coordinators (8)
├── Director, Quality Assurance (per Doc 21)
│   └── [See Doc 21 — Quality Management for full QA org structure]
└── Manager, Merchandise Operations
    ├── Merchandise Systems Specialist (2)
    └── Merchandise Administration (3)
```

### 25.1.2 Oracle Fusion Security Roles

| Role | Oracle Fusion Security Roles |
|------|----------------------------|
| VP Merchandising & QA | ORA_PO_BUYER_VP, ORA_INV_EXECUTIVE, ORA_PRICING_MANAGER, ORA_PLM_ADMIN, ORA_SCM_ANALYTICS |
| Director, Category Management | ORA_PO_BUYER_MANAGER, ORA_PRICING_ANALYST, ORA_PLM_SPECIALIST, ORA_SCM_ANALYTICS |
| Director, Merchandise Planning | ORA_SCP_PLANNER, ORA_PRICING_ANALYST, ORA_INV_ANALYST, ORA_SCM_ANALYTICS |
| Director, Merchandise Buying | ORA_PO_BUYER_MANAGER, ORA_SOURCING_SPECIALIST, ORA_PO_CONTRACT_SPECIALIST |
| Category Managers | ORA_PO_BUYER, ORA_PRICING_ANALYST, ORA_PLM_SPECIALIST, ORA_INV_TRANSACTION_USER |
| Merchandise Planners | ORA_SCP_PLANNER, ORA_INV_ANALYST, ORA_SCM_ANALYTICS |
| Buyers | ORA_PO_BUYER, ORA_SOURCING_SPECIALIST, ORA_SUPPLIER_SPECIALIST |
| Planogram Specialists | ORA_INV_TRANSACTION_USER, ORA_PLM_SPECIALIST |
| Pricing Analysts | ORA_PRICING_ANALYST, ORA_PRICING_MANAGER |

### 25.1.3 Merchandising Council

| Committee | Members | Frequency | Decision Authority |
|-----------|---------|-----------|-------------------|
| Merchandising Executive Committee | VP Merchandising, Directors (Category, Planning, Buying, QA), VP Marketing | Monthly | Strategic assortment decisions, new category launches, major vendor changes, margin target changes |
| Category Review Board | Category Managers, Merchandise Planners, Buyers, Marketing (Trade Marketing rep) | Monthly per category (rotating) | SKU rationalization, promotional calendar, pricing strategy |
| New Product Committee | Category Manager, QA Manager, Buyer, Planner, Marketing (per category) | Bi-weekly | New item approvals, discontinuations |
| Private Label Committee | VP Merchandising, Director Category, Director QA, Director Buying, VP Marketing | Quarterly | Private label strategy, new brand launches, supplier selection for PL |
| Vendor Review Board | Director Buying, Category Manager, QA Manager, Planner | Quarterly (per vendor tier) | Vendor scorecards, negotiation outcomes, vendor exit decisions |

### 25.1.4 Merchandising P&L Ownership

| Category Manager | Revenue Responsibility | Gross Margin Target | Inventory Budget |
|------------------|----------------------|--------------------|-----------------|
| Building Materials & Lumber | PHP 7,200,000,000 | 22-26% | PHP 1,800,000,000 |
| Electrical & Lighting | PHP 5,400,000,000 | 28-32% | PHP 1,080,000,000 |
| Plumbing & Water Systems | PHP 4,500,000,000 | 27-31% | PHP 900,000,000 |
| Paint & Decorating | PHP 4,050,000,000 | 30-35% | PHP 810,000,000 |
| Hardware & Tools | PHP 5,850,000,000 | 30-34% | PHP 1,170,000,000 |
| Appliances | PHP 4,950,000,000 | 20-24% | PHP 1,485,000,000 |
| Flooring & Tiles | PHP 3,600,000,000 | 25-29% | PHP 900,000,000 |
| Kitchen & Bath | PHP 3,150,000,000 | 28-33% | PHP 787,500,000 |
| Doors & Windows | PHP 2,250,000,000 | 24-28% | PHP 562,500,000 |
| Garden & Outdoor | PHP 1,800,000,000 | 32-37% | PHP 450,000,000 |
| Safety & Security | PHP 1,350,000,000 | 33-38% | PHP 337,500,000 |
| Storage & Organization | PHP 900,000,000 | 34-39% | PHP 225,000,000 |
| **Total** | **PHP 45,000,000,000** | **28% blended** | **PHP 10,500,000,000** |

---

## 25.2 Category Management Framework

### 25.2.1 Product Hierarchy

| Level | Count | Example | UNSPSC Level |
|-------|-------|---------|-------------|
| Department | 12 | Hardware & Tools | Segment |
| Class | ~90 | Power Tools | Family |
| Subclass | ~400 | Cordless Drills | Class |
| Item | ~80,000 | Makita XTD01Z 18V Drill | Commodity |
| SKU (variants) | ~120,000 | Makita XTD01Z 18V — Blue | Product |

### 25.2.2 Category Roles

| Role | Definition | Categories | Strategy |
|------|-----------|------------|----------|
| Destination | Primary reason customers visit Tahanan Depot; differentiate vs. competitors | Hardware & Tools, Paint & Decorating, Building Materials | Maximum assortment depth; competitive pricing; strong in-stock; prominent placement |
| Routine | Regular purchase items; drive frequency | Electrical, Plumbing, Safety & Security, Storage | Good assortment; EDLP; convenient placement; high availability |
| Seasonal | Peak during specific periods; drive traffic during those periods | Garden & Outdoor, Appliances (summer AC) | Deep seasonal assortment; aggressive promo during peak; minimized off-season |
| Convenience | Fill-in items; impulse purchase; add to basket | Cleaning supplies, adhesives, fasteners, extension cords | Adequate assortment; higher margins; cross-merchandised near destination categories |
| Complementary | Support and complete projects from destination categories | Kitchen & Bath (with Appliances), Flooring & Tiles (with Building Materials) | Curated assortment; bundled offers; project-based merchandising |

### 25.2.3 Category Scorecard

| Metric | Target | Measurement Frequency | Oracle Source |
|--------|--------|----------------------|---------------|
| Sales growth (YoY) | ≥ 8% | Monthly | AR + GL Analytics |
| Gross margin % | Per category target (see 25.1.4) | Monthly | GL + Cost Management |
| GMROI (Gross Margin Return on Inventory) | ≥ PHP 2.00 per PHP 1 invested | Monthly | GL + Inventory Analytics |
| Sell-through rate | ≥ 85% of bought quantity | Monthly | Inventory + OM |
| Inventory turns | ≥ 6x annually (higher for routine, lower for destination) | Monthly | Inventory Analytics |
| Stock-to-sales ratio | 1.5 - 2.0 (varies by category) | Monthly | Inventory + AR |
| SKU productivity (% of SKUs generating 80% of sales) | Top 20% of SKUs ≥ 80% of sales | Quarterly | Inventory + AR Analytics |
| Out-of-stock rate (store level) | < 3% | Weekly | Inventory + POS |
| Customer satisfaction (per category) | ≥ 4.0 / 5.0 | Quarterly | CX Service survey |
| Shrinkage | < 1.5% of sales (per Doc 13) | Monthly | Inventory Adjustments |
| New item hit rate (new SKUs meeting sales target) | ≥ 60% | Quarterly | Inventory + AR |

### 25.2.4 Space Allocation by Store Format

| Category | Flagship (sqm) | Standard (sqm) | Express (sqm) | % of Total Sales Floor |
|-----------|---------------|----------------|---------------|----------------------|
| Lumber & Building Materials | 1,200 | 900 | 500 | 16% |
| Electrical & Lighting | 700 | 550 | 350 | 11% |
| Plumbing & Water Systems | 600 | 450 | 300 | 10% |
| Paint & Decorating | 650 | 500 | 350 | 10% |
| Hardware & Tools | 900 | 700 | 450 | 14% |
| Appliances | 700 | 500 | 300 | 11% |
| Flooring & Tiles | 550 | 400 | 250 | 8% |
| Kitchen & Bath | 450 | 350 | 200 | 7% |
| Doors & Windows | 350 | 250 | 150 | 5% |
| Garden & Outdoor | 500 | 300 | 150 | 5% |
| Safety & Security | 200 | 150 | 100 | 2% |
| Storage & Organization | 200 | 150 | 100 | 1% |
| **Total Sales Floor** | **7,000** | **5,200** | **3,200** | **100%** |

---

## 25.3 Assortment Planning

### 25.3.1 Assortment Strategy by Category Role

| Category Role | Breadth Strategy | Depth Strategy | SKU Target Range |
|--------------|-----------------|---------------|-----------------|
| Destination | Maximum breadth (all relevant subcategories) | Maximum depth (good-better-best per subcategory) | 15,000 - 25,000 |
| Routine | Full breadth of core subcategories | Moderate depth (2-4 options per subcategory) | 8,000 - 12,000 |
| Seasonal | Full breadth in-season; reduced off-season | Moderate in-season; minimal off-season | 3,000 - 8,000 (varies by season) |
| Convenience | Selected breadth (top-selling subcategories) | Limited depth (1-2 options per subcategory) | 2,000 - 4,000 |
| Complementary | Project-based breadth | Curated depth (coordinated with destination categories) | 5,000 - 8,000 |

### 25.3.2 SKU Rationalization Process

| Step | Activity | Responsible | Criteria |
|------|----------|-------------|----------|
| 1 | Run SKU performance report (sales, margin, turns, weeks of supply) | Merchandise Planner | All SKUs reviewed |
| 2 | Flag underperforming SKUs (bottom 10% by sales, < 1 turn/year, negative margin) | Merchandise Planner | Automated in Oracle SCP |
| 3 | Category Manager reviews flagged SKUs for strategic importance | Category Manager | Brand requirement, project completion, customer expectation |
| 4 | Recommend: keep, markdown, or discontinue | Category Manager + Planner | Decision within 5 business days |
| 5 | For discontinuation: create exit plan (sell-through timeline, markdown schedule, replacement if any) | Buyer + Planner | Per SOP-MD-002 |
| 6 | Approval: Category Manager < PHP 500K impact, Director < PHP 2M, VP > PHP 2M | Per authority matrix | Oracle approval workflow |
| 7 | Execute discontinuation; monitor sell-through | Buyer + Planner | Weekly tracking |
| 8 | Post-exit: update planograms, remove from active assortment | Planogram Specialist | Within 2 weeks of last sale |

### 25.3.3 Private Label Strategy

| Brand | Positioning | Categories | Target Margin | Revenue Target (Annual) |
|-------|------------|------------|--------------|----------------------|
| Tahanan Essentials | Value/entry-level; quality basics for everyday DIY | Hardware, electrical, plumbing, cleaning, storage, paint accessories | 35-40% | PHP 1,800,000,000 |
| Tahanan Pro | Professional-grade; for contractors and serious builders | Power tools, hand tools, safety equipment, fasteners, adhesives | 30-35% | PHP 900,000,000 |
| Tahanan Garden | Garden and outdoor products | Plants (sourced locally), pots, soil, fertilizers, garden tools | 38-42% | PHP 450,000,000 |
| Tahanan Home | Home decor, organization, and lifestyle products | Storage, organizers, decorative hardware, small furniture | 36-40% | PHP 350,000,000 |

### 25.3.4 Regional Assortment Differences

| Region | Unique Assortment Needs | SKUs Unique to Region | Rationale |
|--------|------------------------|----------------------|-----------|
| North Luzon | Heavy building materials (Ilocos, Cagayan Valley construction boom); typhoon-resilient products | +500 SKUs | Higher construction activity; typhoon belt |
| South Luzon (including Metro Manila) | Full assortment; maximum depth; premium and imported products | Baseline (all SKUs) | Highest population density; highest purchasing power |
| Visayas | Marine-grade materials (Cebu, Iloilo coastal); tropical garden products | +300 SKUs | Coastal construction needs; tropical climate |
| Mindanao | Agricultural and rural building products; value-oriented assortment | +200 SKUs | Agricultural economy; price-sensitive market |

### 25.3.5 New Store Assortment Planning

| Store Format | Initial SKU Count | Ramp-Up Period | Full Assortment Target |
|-------------|------------------|----------------|----------------------|
| Flagship | ~42,000 SKUs | 6 months | ~50,000 SKUs |
| Standard | ~35,000 SKUs | 4 months | ~40,000 SKUs |
| Express | ~22,000 SKUs | 3 months | ~25,000 SKUs |

---

## 25.4 Pricing Strategy and Management

### 25.4.1 Pricing Philosophy

| Element | Strategy | Rationale |
|---------|----------|-----------|
| Overall approach | EDLP (Everyday Low Price) on key value items (KVI); promotional pricing on select items | Competitive positioning; customer trust; margin optimization |
| KVI items | ~2,000 SKUs across all categories priced at or below competitor | Drive perception of value; basket-building items |
| Good-Better-Best | 3-tier pricing within each subcategory | Serve all customer segments (DIY homeowner, serious DIYer, professional) |
| Price image | Target: ranked #1 or #2 in local competitive set on KVI basket | Customer price perception survey (quarterly) |

### 25.4.2 Price Architecture — Good-Better-Best Tiers

| Tier | Price Position | Target Customer | Margin Target | Example (Cordless Drill) |
|------|---------------|----------------|--------------|-------------------------|
| Good (Entry) | Lowest price point; acceptable quality | Casual DIYer, budget-conscious | 25-30% | Tahanan Essentials 12V Drill — PHP 1,299 |
| Better (Mid) | Mid-price; reliable performance; brand name | Regular DIYer, homeowner | 28-33% | Bosch PSR 18V Drill — PHP 3,499 |
| Best (Premium) | Highest price; professional-grade; premium brand | Professional contractor, serious DIYer | 22-27% | DeWalt 20V XR Drill — PHP 7,999 |

### 25.4.3 Oracle Pricing Configuration

| Component | Configuration | Oracle Module |
|-----------|--------------|---------------|
| Base price list | Retail price list — all items; updated per pricing cycle | Oracle Pricing |
| Promotional price list | Separate promotional price lists per event; overlaid on base | Oracle Pricing |
| Contractor price list | B2B price list; typically 5-15% below retail per negotiation | Oracle Pricing |
| Wholesale price list | B2B bulk price list; tiered by volume | Oracle Pricing |
| Loyalty member price | Select SKUs with loyalty-exclusive pricing (2-5% below retail) | Oracle Pricing + CX Loyalty |
| Store-specific pricing | Regional pricing adjustments (max ±5% from base) for specific markets | Oracle Pricing |
| Pricing rules | Automated rules: cost-change pass-through, competitor match, margin floor enforcement | Oracle Pricing |
| Price approval workflow | Price changes > 3% require Category Manager approval; > 10% require Director approval | Oracle Pricing + BPM |

### 25.4.4 Margin Targets by Category

| Category | Gross Margin Target | Markup Range | Competitive Sensitivity |
|----------|--------------------|-------------|------------------------|
| Building Materials & Lumber | 22-26% | 28-35% | High (commoditized) |
| Electrical & Lighting | 28-32% | 39-47% | Medium-High |
| Plumbing & Water Systems | 27-31% | 37-45% | Medium-High |
| Paint & Decorating | 30-35% | 43-54% | Medium (brand-driven) |
| Hardware & Tools | 30-34% | 43-52% | Medium |
| Appliances | 20-24% | 25-32% | High (price-transparent) |
| Flooring & Tiles | 25-29% | 33-41% | Medium |
| Kitchen & Bath | 28-33% | 39-49% | Medium-Low (project-based) |
| Doors & Windows | 24-28% | 32-39% | Medium |
| Garden & Outdoor | 32-37% | 47-59% | Low-Medium (impulse) |
| Safety & Security | 33-38% | 49-61% | Low (specialty) |
| Storage & Organization | 34-39% | 52-64% | Low (convenience) |

### 25.4.5 Competitive Price Monitoring

| Activity | Frequency | Method | Coverage |
|----------|-----------|--------|---------|
| KVI basket price check | Weekly | Mystery shopping + online scraping | Top 10 competitors in each region |
| Full category price audit | Monthly | Third-party price research firm | Top 5 competitors; top 500 SKUs |
| Online price monitoring | Daily | Automated web scraping tool | Competitor websites + Lazada + Shopee |
| Market basket analysis | Quarterly | External market research firm | 50-item basket across 5 competitors |
| Price positioning report | Monthly | Internal Merchandise Planning | All categories; flag items outside target position |

### 25.4.6 Price Change Workflow

| Step | Activity | Responsible | System |
|------|----------|-------------|--------|
| 1 | Price change trigger identified (cost change, competitive, promotional, margin) | Pricing Analyst / Category Manager | Oracle Pricing |
| 2 | Impact analysis: margin impact, revenue impact, competitive positioning | Pricing Analyst | Oracle Pricing + GL Analytics |
| 3 | Price change entered in Oracle Pricing with effective date | Pricing Analyst | Oracle Pricing |
| 4 | Approval routed per thresholds (< 3%: auto; 3-10%: Category Manager; > 10%: Director) | Per authority | Oracle BPM |
| 5 | Approved price pushed to POS via OIC (INT-003, per Doc 08) | System (automated) | OIC + POS |
| 6 | Approved price pushed to CX Commerce for online (INT-EC-003, per Doc 23) | System (automated) | OIC + CX Commerce |
| 7 | Shelf labels updated (auto-printed at store or electronic shelf labels) | Store Associate / System | POS + Store Operations |
| 8 | Price change effective at configured date/time | System | Oracle Pricing + POS |
| 9 | Post-change margin monitoring (first 7 days) | Pricing Analyst | Oracle Pricing + GL Analytics |

---

## 25.5 Planogram and Space Management

### 25.5.1 Planogram Creation Process

| Step | Activity | Responsible | Timeline |
|------|----------|-------------|----------|
| 1 | Category Manager defines assortment and product adjacencies | Category Manager | Ongoing |
| 2 | Space Planning Manager allocates space per category based on sales/sqm data | Space Planning Manager | Annual (major) + quarterly (adjustments) |
| 3 | Planogram Specialist creates planogram using space planning tool | Planogram Specialist | Per category schedule |
| 4 | Planogram reviewed by Category Manager for product placement accuracy | Category Manager | 3 days after draft |
| 5 | Planogram reviewed by Store Operations for operational feasibility | Regional Operations Manager | 3 days after CM review |
| 6 | Planogram approved by Director Category Management | Director Category Management | 2 days after ops review |
| 7 | Planogram published to stores via Oracle CX Knowledge / POS system | Planogram Specialist | Per planogram calendar |
| 8 | Store executes planogram reset | Store Associates (per Doc 14) | Within 5 business days of publication |
| 9 | Compliance photo submitted by store | Store Manager | Within 7 days of reset |
| 10 | Compliance audit (target: 95% adherence) | Planogram Specialist | Monthly |

### 25.5.2 Fixture Standards by Category

| Category | Primary Fixture Type | Shelving Height | Depth | Notes |
|-----------|---------------------|----------------|-------|-------|
| Building Materials | Bulk rack / pallet rack | Up to 4m | 1.0-1.2m | Heavy-duty; forklift-accessible lower bays |
| Electrical | Gondola shelving | 1.8m | 0.4-0.5m | Pegboard for small items; bins for fasteners |
| Plumbing | Gondola + pipe rack | 1.8m | 0.5m | Pipe display rack for long items |
| Paint | Gondola + paint display wall | 1.8m | 0.5m | Color sample wall; mixing station |
| Hardware & Tools | Gondola + pegboard | 1.8m | 0.4-0.5m | Tool display hooks; locked cabinet for high-value |
| Appliances | Appliance pad / display platform | Floor display | 1.5m×1.5m per unit | Live demos for select models; power outlets |
| Flooring & Tiles | Tile display rack + sample boards | 2.0m | 0.15m | Sample boards on wall; full-tile display racks |
| Kitchen & Bath | Room vignettes + gondola | Varies | Varies | Mock kitchen/bath displays + accessory gondola |
| Doors & Windows | Vertical door rack + wall display | Up to 2.4m | Door depth | Vertical rack for entry doors; wall for interior |
| Garden & Outdoor | Nursery bench + outdoor display | Floor/bench | Varies | Seasonal rotation; outdoor/garden center area |
| Safety & Security | Gondola + locked cabinet | 1.8m | 0.4-0.5m | Locked cabinet for CCTV and high-value locks |
| Storage & Organization | Gondola + floor display | 1.8m-2.0m | 0.5-0.6m | Assembled shelving units on display |

### 25.5.3 Space Productivity Targets

| Category | Sales per sqm Target (PHP/year) | GMROI Target | Review Frequency |
|-----------|-------------------------------|-------------|-----------------|
| Building Materials | 6,000,000 | ≥ 2.0 | Quarterly |
| Electrical | 7,714,000 | ≥ 2.5 | Quarterly |
| Plumbing | 7,500,000 | ≥ 2.3 | Quarterly |
| Paint | 6,231,000 | ≥ 2.8 | Quarterly |
| Hardware & Tools | 8,357,000 | ≥ 2.5 | Quarterly |
| Appliances | 7,071,000 | ≥ 1.8 | Quarterly |
| Flooring & Tiles | 6,545,000 | ≥ 2.0 | Quarterly |
| Kitchen & Bath | 7,000,000 | ≥ 2.2 | Quarterly |
| Doors & Windows | 6,429,000 | ≥ 2.0 | Quarterly |
| Garden & Outdoor | 3,600,000 | ≥ 2.5 | Quarterly |
| Safety & Security | 6,750,000 | ≥ 2.8 | Quarterly |
| Storage & Organization | 4,500,000 | ≥ 2.8 | Quarterly |

### 25.5.4 Seasonal Planogram Rotations

| Season | Period | Key Categories | Reset Window |
|--------|--------|---------------|-------------|
| Christmas/Holiday | October - January | Garden (Christmas trees, lights), Paint (holiday colors), Appliances (gift items), Storage (organization) | September reset |
| Summer/Dry Season | March - June | Garden & Outdoor, Appliances (AC), Paint, Flooring | February reset |
| Back-to-School | June - August | Storage & Organization, Safety (school supplies), Hardware (basic tools) | May reset |
| Typhoon Season | June - November | Safety & Security, Building Materials (repair), Electrical (emergency lighting, generators) | May reset |
| Chinese New Year | January - February | Paint (red/gold), Decorative hardware, Garden (lucky plants) | January reset |

### 25.5.5 Cross-Merchandising Placement Rules

| Primary Category | Cross-Merchandise | Placement | Rationale |
|-----------------|-------------------|-----------|-----------|
| Paint | Brushes, rollers, trays, tape, drop cloths, primer | Adjacent gondola endcap | One-stop paint project shopping |
| Power tools | Drill bits, blades, batteries, safety glasses, tool belts | Adjacent pegboard + endcap | Accessory attachment |
| Plumbing (faucets) | Supply lines, plumbers tape, drain assemblies, sealant | Below/beside faucet display | Complete installation needs |
| Appliances (AC) | Copper tubing, electrical wire, brackets, drain hose | Adjacent to AC display | Installation components |
| Flooring | Adhesive, grout, spacers, trowel, underlayment | Adjacent to flooring display | Project completion |
| Electrical (switches) | Wire, wire nuts, electrical tape, wall plates | Adjacent to switch display | Complete wiring needs |
| Lumber | Nails, screws, brackets, wood glue, sandpaper | Endcap near lumber yard | Hardware fasteners for building |
| Garden (plants) | Soil, pots, fertilizer, watering can, gardening gloves | Adjacent to plant bench | Plant care needs |
| Doors | Hinges, locks, door knobs, weather stripping, door frame | Adjacent to door display | Complete door installation |

---

## 25.6 Vendor and Supplier Collaboration

### 25.6.1 Vendor Tiering

| Tier | Criteria | Vendor Count | % of Purchases | Management Approach |
|------|----------|-------------|----------------|-------------------|
| Strategic (Tier 1) | Top 50 vendors by spend; > PHP 200M annual; exclusive or dominant brands | 50 | ~60% | Quarterly business reviews; dedicated Buyer; joint business planning; co-investment in promotions |
| Key (Tier 2) | Top 200 vendors by spend; PHP 50M - 200M annual; significant category presence | 150 | ~25% | Semi-annual reviews; assigned Buyer; standard promotional support |
| Standard (Tier 3) | Remaining active vendors; < PHP 50M annual; commodity or niche suppliers | ~2,300 | ~15% | Annual review; shared Buyer; minimal promotional support |

### 25.6.2 Vendor Negotiation Framework

| Negotiation Element | Strategic Vendors | Key Vendors | Standard Vendors |
|---------------------|------------------|-------------|-----------------|
| Cost negotiation | Annual cost-down target 2-5%; joint efficiency programs | Annual cost review; competitive benchmark | Market-rate pricing; competitive bid |
| Volume rebate | 1-3% annual rebate on total purchases | 0.5-1.5% on qualifying volumes | Per-order discounts only |
| Promotional support (co-op) | 50% co-fund on promotions; vendor-funded endcaps | 30% co-fund on select promotions | Limited or none |
| Payment terms | Net 60 (extended); early payment discount 2/10 | Net 45; early payment discount 2/10 | Net 30; standard terms |
| Returns/defective allowance | 2-3% defective allowance; vendor pickup | 1-2% defective allowance | Customer return per POL-RET-001 |
| New product development | Joint product development; exclusive launches | Advance product samples; early access | Standard new product process |
| Minimum order value | Blanket orders with scheduled releases | Min order per PO | Min order per PO |

### 25.6.3 Volume Rebate Management

| Step | Activity | Responsible | Oracle Module |
|------|----------|-------------|---------------|
| 1 | Annual rebate agreement negotiated and documented in Procurement Contracts | Buyer | Procurement Contracts |
| 2 | Rebate terms configured in Oracle: threshold, rate, qualifying categories | Buyer + Merch Systems Specialist | Procurement Contracts |
| 3 | Purchases tracked against rebate thresholds in real-time | System (automated) | Procurement Contracts + Purchasing |
| 4 | Quarterly rebate reconciliation: actual purchases vs. agreement | Buyer + Finance | Procurement Contracts + GL |
| 5 | Rebate credit memo created and applied to AP | AP Specialist | Payables |
| 6 | Annual rebate true-up at contract anniversary | Buyer + Finance | Procurement Contracts + Payables |

### 25.6.4 Supplier Scorecard

| Metric | Weight | Target | Data Source | Frequency |
|--------|--------|--------|-----------|-----------|
| On-time delivery | 25% | ≥ 95% | WMS / Inventory | Monthly |
| Quality (defect rate) | 20% | < 1.5% | PLM Quality | Monthly |
| Fill rate | 20% | ≥ 97% | Purchasing + Inventory | Monthly |
| Invoice accuracy | 15% | ≥ 99% | Payables | Monthly |
| Cost competitiveness | 10% | Within 3% of market benchmark | Sourcing + Pricing | Quarterly |
| Responsiveness | 5% | < 24 hours response time | Buyer assessment | Quarterly |
| Merchandising support | 5% | Per agreement | Category Manager assessment | Quarterly |

### 25.6.5 Import Vendor Management

| Element | Policy |
|---------|--------|
| Import vendor qualification | Must have Philippine importer of record or partner with licensed customs broker; verified business registration in country of origin |
| Minimum order | Container-load (20ft or 40ft) minimum for direct import |
| Lead time commitment | Documented lead time per product; penalty for late shipment per contract |
| Quality pre-shipment | Pre-shipment inspection required for new vendors (first 3 shipments); random inspection thereafter |
| Payment terms | Letter of Credit (LC) or Telegraphic Transfer (TT); per Incoterms (FOB or CIF) |
| Customs compliance | Per POL-SCM-005 (Import and Customs Compliance); GTM integration (per Doc 03) |

---

## 25.7 Promotional Merchandising

### 25.7.1 Promotional Calendar

| Month | Major Promotion | Category Focus | Discount Depth |
|-------|----------------|---------------|----------------|
| January | New Year Sale | Storage & Organization, Paint | 10-20% |
| February | Chinese New Year / Love Your Home | Paint (red/gold), Decor, Kitchen | 10-15% |
| March | Summer Kick-Off Sale | Garden, Outdoor, Appliances (AC) | 15-25% |
| April | Summer Super Sale | All categories (flagship event) | 15-30% |
| May | Builder's Month | Building Materials, Tools, Safety | 10-20% |
| June | Mid-Year Clearance + Back-to-School | Clearance, Storage, Basic Tools | 20-40% |
| July | Rainy Season Prep | Safety, Electrical, Plumbing (waterproofing) | 10-15% |
| August | National Heroes Day Sale | Appliances, Kitchen & Bath | 10-20% |
| September | —Ber Months Kickoff (Christmas Preview) | Christmas Trees, Lights, Decor | 10-15% |
| October | Anniversary Sale (founding month) | All categories (flagship event) | 15-35% |
| November | 11.11 Sale + Christmas Prep | All categories; gift items | 15-25% |
| December | Christmas Mega Sale | Appliances, Tools, Decor, Gift Items | 10-30% |

### 25.7.2 Flyer/Circular Planning

| Element | Details |
|---------|---------|
| Frequency | Monthly major flyer (8-12 pages); bi-weekly mini flyer (4 pages) |
| Distribution | Inserted in major newspapers (Philippine Daily Inquirer, Philippine Star); in-store pickup; email; social media; website |
| Print run | 500,000 copies (major); 200,000 copies (mini) |
| Lead time | Final artwork: 3 weeks before distribution; product selection: 5 weeks before |
| Approval chain | Category Manager selects items → Marketing designs → VP Merchandising approves pricing → VP Marketing approves creative → Print |
| Oracle integration | Promotional price list created in Oracle Pricing per event; linked to flyer items |

### 25.7.3 Promotional Inventory Planning

| Step | Activity | Responsible | System |
|------|----------|-------------|--------|
| 1 | Category Manager selects promotional items and estimated lift (50-200% above normal) | Category Manager | SCP + Pricing |
| 2 | Merchandise Planner calculates incremental inventory needed | Merchandise Planner | SCP |
| 3 | Buyer ensures purchase orders placed with adequate lead time | Buyer | Purchasing |
| 4 | Supply planning adjusts allocation to stores based on store tier and historical promo performance | Planner | SCP + Inventory |
| 5 | Pre-promo inventory check (7 days before): confirm stock at DC and stores | Planner | Inventory |
| 6 | If stock risk: expedite shipment, substitute item, or reduce promo scope | Buyer + Planner | Purchasing + SCP |
| 7 | During promo: daily sell-through monitoring | Planner | POS + Inventory Analytics |
| 8 | Post-promo: sell-through analysis, remaining stock disposition | Planner + Buyer | Inventory + GL |

### 25.7.4 Promotional Performance Analysis

| Metric | Target | Measurement | Frequency |
|--------|--------|-------------|-----------|
| Sales lift (vs. baseline) | ≥ 100% lift on featured items | POS data (AR Analytics) | Per promo event |
| Gross margin on promo items | ≥ 50% of normal margin | GL + Cost Management | Per promo event |
| Cannibalization (on non-promo items in same category) | < 15% of lift | Inventory Analytics | Per promo event |
| Halo effect (lift on adjacent/complementary categories) | Track positive halo | POS basket analysis | Per promo event |
| New customer acquisition | Track % of promo buyers who are new to loyalty program | CX CDP | Per promo event |
| Promotional ROI | Revenue lift minus promo cost ≥ 3:1 | GL + Marketing budget | Per promo event |
| Post-promo return to baseline | Sales return to baseline within 2 weeks | POS data | Per promo event |

---

## 25.8 New Product Introduction

### 25.8.1 New Product Request and Evaluation

| Step | Activity | Responsible | Timeline |
|------|----------|-------------|----------|
| 1 | New product idea generated (vendor proposal, market trend, customer request, competitor gap) | Any (vendor, buyer, category manager, customer) | Ongoing |
| 2 | Buyer creates New Product Request (NPR) in Oracle PLM | Buyer | Day 0 |
| 3 | Initial screening: fits category strategy, no direct conflict with existing SKU, margin potential | Category Manager | Day 1-3 |
| 4 | If passes screening: sample requested from vendor | Buyer | Day 3-5 |
| 5 | Sample evaluated for quality (QA per Doc 21), specifications, and compliance | QA Inspector | Day 5-15 |
| 6 | Merchandise Planner creates sales forecast and initial buy quantity | Merchandise Planner | Day 10-15 |
| 7 | Pricing Analyst determines pricing (Good-Better-Best positioning) | Pricing Analyst | Day 10-15 |
| 8 | New Product Committee reviews and approves/rejects | Committee (per 25.1.3) | Day 15-20 |
| 9 | If approved: Buyer negotiates terms with vendor; creates first PO | Buyer | Day 20-30 |
| 10 | Product setup in Oracle PLM (all attributes, images, specs) | Merch Systems Specialist | Day 20-30 |
| 11 | Product content created for online (per Doc 23, SOP-EC-003) | Product Content Specialist | Day 25-35 |
| 12 | Planogram updated to include new item | Planogram Specialist | Day 25-35 |
| 13 | Marketing briefed for launch support (flyer, signage, digital) | Category Manager → Marketing | Day 30 |
| 14 | Product arrives at DC; distributed to stores per allocation | Supply Chain | Day 30-45 |
| 15 | Launch date; product available in-store and online | All | Day 45 |

### 25.8.2 New Product Performance Tracking

| Timeframe | Metric | Target | Action if Below Target |
|-----------|--------|--------|----------------------|
| First 7 days | Units sold vs. forecast | ≥ 50% of weekly forecast | Review pricing, placement, marketing support |
| First 30 days | Units sold vs. forecast | ≥ 80% of monthly forecast | Investigate root cause; adjust forecast or marketing |
| First 60 days | Units sold vs. forecast | ≥ 90% of forecast | Markdown trigger if < 50% |
| First 90 days | Gross margin vs. target | ≥ target margin | Discontinuation evaluation if both sales and margin below target |
| Fail-fast trigger | < 30% of forecast at 30 days | — | Immediate discontinuation review; markdown or exit |

---

## 25.9 Markdown and Clearance Management

### 25.9.1 Markdown Triggers

| Trigger | Criteria | Markdown Level | Approval |
|---------|----------|---------------|----------|
| Slow-moving inventory | < 1 inventory turn in 6 months; > 26 weeks of supply | 15-25% off | Category Manager |
| End-of-season | Seasonal items past peak selling period | 25-40% off | Category Manager |
| Discontinued by vendor | Vendor notifies product end-of-life | 25-50% off | Director Category |
| Damaged packaging | Product intact but packaging damaged | 10-20% off | Store Manager (in-store) |
| New model replacement | Previous model being replaced by updated version | 20-40% off | Category Manager |
| Clearance (last chance) | Item marked down previously but still unsold after 60 days | 50-75% off | Director Category |
| Write-off | Damaged, expired, or unsellable | 100% (dispose/donate) | VP Merchandising |

### 25.9.2 Markdown Approval Workflow

| Markdown Level | Authority | Oracle Workflow |
|---------------|-----------|-----------------|
| 10-15% off retail | Store Manager (for damaged display items only) | POS markdown code |
| 15-25% off retail | Category Manager | Oracle Pricing (promotional price list) |
| 25-40% off retail | Director Category Management | Oracle Pricing + approval workflow |
| 40-50% off retail | VP Merchandising | Oracle Pricing + dual approval |
| > 50% off retail | VP Merchandising + CFO | Manual approval + Oracle Pricing |
| Write-off (dispose) | VP Merchandising + CFO | GL journal + Inventory adjustment |

### 25.9.3 Markdown Cadence

| Phase | Timing | Discount | Action |
|-------|--------|----------|--------|
| Phase 1 (Alert) | Item identified for markdown | Original price | Flag in system; Category Manager notified |
| Phase 2 (First markdown) | Week 1 | 15-25% off | Price reduced; clearance signage applied |
| Phase 3 (Second markdown) | Week 4 (if unsold) | 30-40% off | Deeper discount; moved to clearance section |
| Phase 4 (Final markdown) | Week 8 (if unsold) | 50-75% off | Last chance; prominent clearance display |
| Phase 5 (Exit) | Week 12 (if unsold) | Write-off | Donate (per Doc 26, POL-CSR-005) or dispose |

### 25.9.4 Markdown Reporting

| Report | Frequency | Audience | Content |
|--------|-----------|----------|---------|
| Markdown liability report | Weekly | Category Managers, Merch Planners | Total markdown exposure by category; aging of markdown items |
| Markdown execution report | Weekly | Store Operations | Markdown compliance at stores; clearance section status |
| Markdown margin impact | Monthly | VP Merchandising, CFO | Actual margin impact of markdowns vs. budget; write-off rates |
| Post-season clearance report | Per season | Merchandising Committee | Clearance sell-through rate, recovery rate, lessons learned |

---

## 25.10 Merchandising Analytics

### 25.10.1 Key Metrics Dashboard

| Metric | Definition | Target | Frequency | Oracle Source |
|--------|-----------|--------|-----------|---------------|
| Total revenue | Total sales across all channels | PHP 45B annual | Daily | AR + GL |
| Gross margin % | (Revenue - COGS) / Revenue | 28% blended | Monthly | GL + Cost Management |
| GMROI | Gross margin / average inventory cost | ≥ PHP 2.00 per PHP 1 | Monthly | GL + Inventory |
| Inventory turns | COGS / average inventory | ≥ 6x annually | Monthly | Inventory + GL |
| Weeks of supply | On-hand inventory / avg weekly sales | 8-12 weeks (varies by category) | Weekly | Inventory + SCP |
| Sell-through rate | Units sold / units available | ≥ 85% | Monthly | Inventory + AR |
| Stock-to-sales ratio | Month-end inventory / monthly sales | 1.5 - 2.0 | Monthly | Inventory + AR |
| Out-of-stock rate | SKUs with zero on-hand at store | < 3% | Weekly | Inventory + POS |
| SKU productivity | % of active SKUs contributing to 80% of sales | Top 20% ≥ 80% of sales | Quarterly | AR + Inventory Analytics |
| Shrinkage | Inventory adjustment / total sales | < 1.2% (per Doc 13) | Monthly | Inventory |
| Markdown rate | Markdown value / total sales | < 3% | Monthly | Pricing + GL |
| New item success rate | New items meeting sales target in first 90 days | ≥ 60% | Quarterly | AR + Inventory |

### 25.10.2 Vendor Performance Reporting

| Report | Frequency | Audience | Content |
|--------|-----------|----------|---------|
| Vendor scorecard (individual) | Monthly | Buyer, Category Manager | OTD, fill rate, quality, invoice accuracy, cost competitiveness |
| Vendor tier summary | Quarterly | VP Merchandising, Director Buying | Scorecard averages by tier; vendors at risk; vendor exit recommendations |
| Vendor rebate tracking | Monthly | Buyer, Finance | Rebate accrual vs. actual; threshold progress |
| Vendor new product pipeline | Monthly | Category Managers | New products in pipeline; launch dates; expected impact |
| Vendor payment aging | Weekly | Finance, Buyers | Overdue payments; disputed invoices; vendor hold status |

### 25.10.3 Space Productivity Analytics

| Report | Frequency | Audience | Content |
|--------|-----------|----------|---------|
| Sales per sqm by category | Monthly | Space Planning, Category Managers | Sales/sqm vs. target; category space efficiency ranking |
| Space-to-sales ratio | Quarterly | VP Merchandising | Space allocation vs. sales contribution by category |
| Planogram compliance audit results | Monthly | Category Managers, Store Ops | Compliance % by store and category; photo audit results |
| Fixture productivity | Quarterly | Space Planning | Sales per fixture type; optimal fixture mix recommendations |
| Department adjacency analysis | Annually | Space Planning | Cross-department sales correlation; optimal layout recommendations |

### 25.10.4 Competitive Intelligence

| Activity | Frequency | Source | Deliverable |
|----------|-----------|--------|-------------|
| Competitor price audit (KVI basket) | Weekly | Mystery shopping + web scraping | Price comparison report |
| Competitor assortment tracking | Monthly | Store visits + online monitoring | New items, discontinued items, exclusive products |
| Competitor promotional tracking | Per event | Flyer capture + online monitoring | Promotional comparison; response recommendations |
| Market share estimation | Quarterly | External research (Nielsen/Kantar) | Category market share trend |
| Industry trend briefing | Quarterly | Trade publications, trade shows, global trend reports | Category trend report with action items |

---

## 25.11 Merchandising Standard Operating Procedures

### SOP-MD-001: New Item Introduction

| Step | Activity | Responsible | System |
|------|----------|-------------|--------|
| 1 | New Product Request (NPR) created in Oracle PLM | Buyer | PLM |
| 2 | Initial screening by Category Manager | Category Manager | PLM |
| 3 | Sample requested and evaluated by QA | QA Inspector | PLM Quality |
| 4 | Sales forecast and initial buy quantity by Planner | Merchandise Planner | SCP |
| 5 | Pricing determined by Pricing Analyst | Pricing Analyst | Oracle Pricing |
| 6 | New Product Committee review and approval | Committee | PLM approval workflow |
| 7 | Vendor terms negotiated; first PO created | Buyer | Purchasing |
| 8 | Product setup in PLM (all attributes) | Merch Systems Specialist | PLM |
| 9 | Planogram updated | Planogram Specialist | Space Planning tool |
| 10 | Marketing launch support coordinated | Category Manager → Marketing | CX Marketing |
| 11 | Product received at DC and distributed to stores | Supply Chain | WMS + Inventory |
| 12 | 30/60/90-day performance tracking | Merchandise Planner | SCP + AR Analytics |

### SOP-MD-002: Product Discontinuation

| Step | Activity | Responsible | System |
|------|----------|-------------|--------|
| 1 | Discontinuation trigger identified (poor performance, vendor exit, replacement) | Category Manager / Planner | SCP + Inventory Analytics |
| 2 | Discontinuation impact analysis: sales, margin, customer impact, inventory on hand | Merchandise Planner | GL + Inventory |
| 3 | Discontinuation proposal submitted for approval | Category Manager | PLM |
| 4 | Approval: Category Manager < PHP 500K, Director < PHP 2M, VP > PHP 2M | Per authority | PLM approval workflow |
| 5 | Replacement item identified (if applicable) and staged | Buyer + Planner | PLM + Purchasing |
| 6 | Remaining inventory disposition plan: sell-through, markdown, transfer, return to vendor, write-off | Buyer + Planner | Inventory + Pricing |
| 7 | All open POs cancelled or modified | Buyer | Purchasing |
| 8 | Item status changed to "Discontinued" in PLM | Merch Systems Specialist | PLM |
| 9 | Planogram updated; discontinued item removed from shelf plan | Planogram Specialist | Space Planning tool |
| 10 | Stores notified; execute removal and markdown per schedule | Store Ops + Category Manager | POS + CX Knowledge |
| 11 | Monitor sell-through of remaining inventory weekly | Merchandise Planner | Inventory |
| 12 | Final write-off or donation of unsold inventory | Finance + Merchandising | GL + Inventory |

### SOP-MD-003: Price Change Management

| Step | Activity | Responsible | System |
|------|----------|-------------|--------|
| 1 | Price change triggered (cost change, competitive, promotional, margin review) | Pricing Analyst / Category Manager | Oracle Pricing |
| 2 | Impact analysis: margin, revenue, competitive position | Pricing Analyst | Oracle Pricing + GL Analytics |
| 3 | New price entered in Oracle Pricing with effective date | Pricing Analyst | Oracle Pricing |
| 4 | Approval workflow executed per thresholds (section 25.4.6) | Per authority | Oracle BPM |
| 5 | Price synced to POS (INT-003) and CX Commerce (INT-EC-003) | System (automated) | OIC |
| 6 | Shelf labels updated at stores | Store Associate | POS label printer |
| 7 | Price change effective; margin monitoring (7 days) | Pricing Analyst | Oracle Pricing + GL |
| 8 | Post-change review: actual vs. projected margin impact | Pricing Analyst | GL Analytics |

### SOP-MD-004: Promotional Setup

| Step | Activity | Responsible | System |
|------|----------|-------------|--------|
| 1 | Promotional items selected per promotional calendar (section 25.7.1) | Category Manager | SCP + Pricing |
| 2 | Promotional pricing determined; margin checked against floor | Pricing Analyst | Oracle Pricing |
| 3 | Promotional price list created in Oracle Pricing | Pricing Analyst | Oracle Pricing |
| 4 | Promotional inventory confirmed with Planner and Buyer | Planner + Buyer | SCP + Purchasing |
| 5 | Marketing brief submitted (flyer, signage, digital, social) | Category Manager → Marketing | CX Marketing |
| 6 | Store communication: promo details, dates, display requirements | Merch Ops → Store Ops | CX Knowledge |
| 7 | Promotional price activated at scheduled date/time | System (automated) | Oracle Pricing → POS → CX Commerce |
| 8 | Daily sell-through monitoring during promo | Merchandise Planner | POS + Inventory Analytics |
| 9 | Post-promo analysis (per section 25.7.4) | Planner + Pricing Analyst | GL + AR + FDI |
| 10 | Post-promo price reversion to base; remaining stock disposition | Pricing Analyst + Buyer | Oracle Pricing + Inventory |

### SOP-MD-005: Planogram Compliance Audit

| Step | Activity | Responsible | System |
|------|----------|-------------|--------|
| 1 | Monthly planogram compliance audit schedule published | Space Planning Manager | Space Planning tool |
| 2 | Planogram Specialist reviews planogram compliance photos submitted by stores | Planogram Specialist | CX Knowledge / Store portal |
| 3 | Store visit audit conducted (rotating: 20 stores/month across all regions) | Planogram Specialist | Audit checklist |
| 4 | Compliance scored: product placement, shelf positioning, signage, cross-merchandising | Planogram Specialist | Audit form |
| 5 | Compliance report generated per store and per category | Planogram Specialist | FDI + Space Planning |
| 6 | Non-compliance issues communicated to Store Manager with corrective action timeline | Space Planning Manager | Email + Store portal |
| 7 | Corrective actions verified within 10 business days | Planogram Specialist | Follow-up photo review |
| 8 | Monthly compliance dashboard published to VP Merchandising and Store Ops | Space Planning Manager | FDI |
| 9 | Target: ≥ 95% compliance; stores below 90% flagged for remediation | VP Merchandising | FDI |

### SOP-MD-006: Vendor Negotiation and Cost Management

| Step | Activity | Responsible | System |
|------|----------|-------------|--------|
| 1 | Annual negotiation calendar prepared (per vendor tier) | Director Buying | Procurement Contracts |
| 2 | Pre-negotiation analysis: vendor performance, spend analysis, market pricing, cost breakdown | Buyer + Pricing Analyst | Purchasing + Pricing + GL |
| 3 | Negotiation objectives set: cost-down target, payment terms, volume rebate, promotional support | Category Manager + Buyer | Procurement Contracts |
| 4 | Negotiation conducted with vendor (in-person or virtual) | Buyer + Category Manager | — |
| 5 | Negotiation outcome documented; new terms entered in Procurement Contracts | Buyer | Procurement Contracts |
| 6 | New cost reflected in Oracle Cost Management | Merch Systems Specialist | Cost Management |
| 7 | Price review: determine if cost savings passed to retail price or retained as margin | Pricing Analyst + Category Manager | Oracle Pricing |
| 8 | Quarterly vendor performance review meeting | Buyer + Category Manager | Vendor scorecard (per 25.6.4) |

### SOP-MD-007: Private Label Product Development

| Step | Activity | Responsible | Timeline |
|------|----------|-------------|----------|
| 1 | Market opportunity identified (gap in assortment, margin improvement, brand building) | Category Manager | Ongoing |
| 2 | Business case developed: sales projection, margin target, development cost, payback | Planner + Category Manager | 2 weeks |
| 3 | Private Label Committee approval | Committee (per 25.1.3) | 1 week |
| 4 | Product specifications developed | QA Manager + Category Manager | 2-4 weeks |
| 5 | Vendor sourcing for PL manufacturing (RFQ per POL-SCM-001) | Buyer | 2-4 weeks |
| 6 | Vendor samples obtained and tested | QA Inspector | 2-4 weeks |
| 7 | Packaging design (Tahanan brand guidelines per Doc 17) | Marketing + Buyer | 2-3 weeks |
| 8 | Final vendor selection and contract negotiation | Buyer + Director Buying | 2 weeks |
| 9 | First production order placed | Buyer | 1 week |
| 10 | Pre-shipment quality inspection at factory | QA Inspector (or third-party) | Per lead time |
| 11 | Product received at DC; quality sampling | QA Inspector | 1-2 days |
| 12 | Product launched (per SOP-MD-001 steps 8-12) | All | Per schedule |

### SOP-MD-008: Markdown Approval and Execution

| Step | Activity | Responsible | System |
|------|----------|-------------|--------|
| 1 | Markdown candidate identified (per triggers, section 25.9.1) | Planner / Category Manager | SCP + Inventory |
| 2 | Markdown proposal: items, current price, proposed markdown %, inventory on hand, margin impact | Planner | Inventory + Pricing + GL |
| 3 | Approval per authority matrix (section 25.9.2) | Per authority | Oracle Pricing + BPM |
| 4 | Markdown price list created in Oracle Pricing | Pricing Analyst | Oracle Pricing |
| 5 | Price synced to POS and CX Commerce | System (automated) | OIC |
| 6 | Markdown signage sent to stores; clearance section updated | Store Ops | Store portal |
| 7 | Markdown execution at store: signage placed, labels updated, items moved to clearance if Phase 3+ | Store Associate | POS |
| 8 | Weekly sell-through tracking | Planner | Inventory + POS |
| 9 | Next phase trigger evaluation (per cadence, section 25.9.3) | Planner | Inventory |
| 10 | Final disposition for unsold items (donate or dispose) | Finance + Merchandising | GL + Inventory |

### SOP-MD-009: Assortment Review and Optimization

| Step | Activity | Responsible | Frequency |
|------|----------|-------------|-----------|
| 1 | Category Review Board schedule published (monthly rotating categories) | Director Category Management | Annual |
| 2 | Pre-review data package prepared: sales trends, margin trends, inventory health, SKU productivity, competitive landscape | Merchandise Planner | 1 week before review |
| 3 | Category review meeting: Category Manager presents performance, strategy, proposed changes | Category Manager + Planner + Buyer + Marketing | Per schedule |
| 4 | Decisions made: SKU adds, SKU removes, price adjustments, space reallocation, promotional plans | Committee consensus | During meeting |
| 5 | Action items assigned with owners and deadlines | Director Category Management | During meeting |
| 6 | Action items tracked to completion | Merch Ops Coordinator | Ongoing |
| 7 | Quarterly assortment scorecard published | Merchandise Planner | Quarterly |

### SOP-MD-010: Competitive Price Monitoring

| Step | Activity | Responsible | Frequency |
|------|----------|-------------|-----------|
| 1 | KVI basket list maintained (top 2,000 items, reviewed quarterly) | Pricing Analyst | Quarterly update |
| 2 | Weekly price check executed (mystery shopping + automated web scraping) | Pricing Analyst + third-party | Weekly |
| 3 | Price comparison report generated: Tahanan vs. competitors by item | Pricing Analyst | Weekly |
| 4 | Items where Tahanan is > 5% above competitor average flagged | System (automated) | Weekly |
| 5 | Category Manager reviews flagged items; determines response (match, accept gap, adjust value proposition) | Category Manager | Within 3 business days |
| 6 | If price match: initiate price change per SOP-MD-003 | Pricing Analyst | Per decision |
| 7 | Monthly competitive positioning summary report | Pricing Analyst | Monthly |
| 8 | Quarterly market basket analysis (external research firm) | Pricing Analyst + external | Quarterly |

---

## 25.12 Document Control

| Field | Detail |
|-------|--------|
| Document Title | Merchandising & Category Management |
| Document Set | Tahanan Depot Operations Documentation |
| Document Number | Doc 25 |
| Department | Merchandising / Category Management / Buying |
| Review Cycle | Annual (or upon significant market change) |
| Last Reviewed | March 15, 2026 |
| Next Review | March 15, 2027 |
| Owner | VP Merchandising & Quality Assurance |
| Approved By | Chief Operations Officer |

### Revision History

| Rev | Date | Author | Description |
|-----|------|--------|-------------|
| 1.0 | Mar 15, 2026 | A. Dela Cruz | Initial release |
