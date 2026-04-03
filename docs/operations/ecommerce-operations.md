# 23 — E-COMMERCE OPERATIONS

## 23.1 E-Commerce Organization and Governance

### 23.1.1 E-Commerce Team Structure

```
VP E-Commerce (reports to CMO, dotted line to COO)
├── Director, Online Retail
│   ├── E-Commerce Manager
│   ├── Digital Merchandising Specialists (3)
│   ├── Product Content Specialists (4)
│   └── Site Merchandising Coordinator
├── Director, E-Commerce Fulfillment
│   ├── Fulfillment Operations Manager
│   ├── Order Processing Specialists (6)
│   ├── Click-and-Collect Coordinator
│   └── Last-Mile Delivery Liaison
├── Manager, E-Commerce Technology
│   ├── Web Developers (3)
│   ├── UX/UI Designer
│   └── QA Analyst
├── Manager, Marketplace & Partnerships
│   ├── Marketplace Specialists (3 — Lazada, Shopee, Social Commerce)
│   └── Partner Integration Analyst
└── Manager, E-Commerce Analytics
    ├── E-Commerce Data Analysts (2)
    └── CRO (Conversion Rate Optimization) Specialist
```

### 23.1.2 Oracle Fusion Security Roles

| Role | Oracle Fusion Security Roles |
|------|----------------------------|
| VP E-Commerce | ORA_CX_COMMERCE_ADMIN, ORA_CX_LOYALTY_MANAGER, ORA_CX_CDP_ADMIN, ORA_OM_EXECUTIVE |
| Director, Online Retail | ORA_CX_COMMERCE_MANAGER, ORA_CX_MARKETING_MANAGER |
| Director, E-Commerce Fulfillment | ORA_OM_MANAGER, ORA_INV_TRANSACTION_MANAGER, ORA_WMS_MANAGER |
| E-Commerce Manager | ORA_CX_COMMERCE_SPECIALIST, ORA_PRICING_ANALYST |
| Manager, Marketplace | ORA_CX_COMMERCE_SPECIALIST, ORA_OM_SPECIALIST |
| Manager, E-Commerce Analytics | ORA_CX_ANALYTICS_SPECIALIST, ORA_FDI_ANALYST |

### 23.1.3 E-Commerce Budget

| Category | Annual Budget (PHP) | % of Digital Revenue | Notes |
|----------|--------------------|--------------------|-------|
| Platform licensing (Oracle CX Commerce) | 18,000,000 | 1.20% | Annual subscription |
| Web/mobile development | 15,000,000 | 1.00% | Feature development, UX improvements |
| Digital marketing (paid search, social, display) | 120,000,000 | 8.00% | Part of overall marketing budget (per Doc 17) |
| Marketplace fees and commissions | 45,000,000 | 3.00% | Lazada, Shopee commissions |
| Fulfillment and shipping subsidies | 60,000,000 | 4.00% | Free shipping promos, delivery costs |
| Product content and photography | 12,000,000 | 0.80% | Studio shoots, 360° images, video |
| Customer service (online channel) | 10,000,000 | 0.67% | Chat agents, chatbot licensing |
| Payment gateway fees | 22,500,000 | 1.50% | Card processing, e-wallet fees |
| Promotional discounts (online-only) | 35,000,000 | 2.33% | Flash sales, online exclusives |
| Technology infrastructure (hosting, CDN) | 8,500,000 | 0.57% | Cloud hosting, CDN, security |
| Contingency | 14,000,000 | 0.93% | As needed |
| **Total E-Commerce Budget** | **PHP 360,000,000** | **24.00%** | Target digital revenue: PHP 1.5B (3.3% of total) |

### 23.1.4 Budget Approval Workflow

| Amount Range (PHP) | Approver | Oracle Workflow |
|---------------------|----------|-----------------|
| 0 — 200,000 | E-Commerce Manager | Auto-approved in Oracle |
| 200,001 — 1,000,000 | VP E-Commerce | Oracle workflow approval |
| 1,000,001 — 5,000,000 | VP E-Commerce + CMO | Dual approval in Oracle |
| > 5,000,000 | CEO + CFO | Manual approval |

---

## 23.2 Platform Architecture and Operations

### 23.2.1 Oracle CX Commerce Platform Configuration

| Component | Configuration | Notes |
|-----------|--------------|-------|
| Storefront | tahanandepot.com.ph | Primary online storefront |
| Mobile App | iOS and Android native apps | Built on Oracle CX Commerce mobile SDK |
| Catalog | 80,000+ SKUs synced from Oracle PLM | Hourly sync via OIC (INT-EC-001) |
| Search | Oracle CX Commerce search engine | Auto-suggest, faceted navigation, spell correction |
| Checkout | Multi-step with guest checkout option | 3-step: shipping → payment → review |
| Cart | Persistent cart (logged-in users, 30-day expiry) | Synced across web and mobile |
| User Accounts | Optional registration; linked to Tahanan Rewards | Oracle CX CDP integration |
| Localization | Filipino/English; PHP currency | Philippines-only shipping currently |

### 23.2.2 Integration Architecture

| Integration ID | Source → Target | Data Flow | Frequency | Protocol |
|----------------|----------------|-----------|-----------|----------|
| INT-EC-001 | Oracle PLM → CX Commerce | Product catalog (items, categories, attributes, images) | Hourly batch | OIC REST |
| INT-EC-002 | Oracle Inventory → CX Commerce | Real-time inventory availability (ATP) per store/warehouse | Near-real-time (5 min) | OIC REST |
| INT-EC-003 | Oracle Pricing → CX Commerce | Price lists, promotional prices | Hourly batch + event-driven | OIC REST |
| INT-EC-004 | CX Commerce → Oracle Order Management | New online orders | Real-time (per order) | OIC REST |
| INT-EC-005 | Oracle Order Management → CX Commerce | Order status updates (confirmed, shipped, delivered) | Real-time (event-driven) | OIC REST |
| INT-EC-006 | CX Commerce → Oracle CX Loyalty | Points earning/redemption transactions | Real-time | OIC REST |
| INT-EC-007 | CX Commerce → Oracle CX CDP | Customer profile, browsing behavior, purchase history | Real-time + daily batch | OIC REST |
| INT-EC-008 | CX Commerce → Oracle AR | Payment confirmation, BIR receipt generation | Real-time (per transaction) | OIC REST via Accounting Hub |
| INT-EC-009 | POS → CX Commerce | In-store inventory for click-and-collect availability | Near-real-time (15 min) | OIC REST |
| INT-EC-010 | CX Commerce → Oracle CX Service | Customer inquiries, chat transcripts | Real-time | OIC REST |

### 23.2.3 System Availability and Monitoring

| Metric | Target | Monitoring Tool | Escalation |
|--------|--------|----------------|------------|
| Website uptime | 99.9% (max 8.7 hrs downtime/year) | Oracle Cloud Infrastructure Monitoring | L1: auto-alert to Tahanan Digital NOC |
| Page load time (homepage) | < 2 seconds | Oracle APM | > 3s: auto-alert |
| Page load time (product page) | < 2.5 seconds | Oracle APM | > 4s: auto-alert |
| Checkout completion time | < 5 seconds | Oracle APM | > 8s: auto-alert |
| Search response time | < 500ms | Oracle CX Commerce analytics | > 1s: auto-alert |
| API response time (OIC) | < 1 second | OIC Monitoring | > 2s: auto-alert |
| Mobile app crash rate | < 0.5% | Firebase Crashlytics | > 1%: alert to dev team |
| CDN cache hit ratio | > 95% | Oracle CDN analytics | < 90%: alert |

### 23.2.4 Content Management

| Content Type | Owner | Update Frequency | Approval Required |
|-------------|-------|------------------|-------------------|
| Homepage banner | Digital Merchandising | Weekly (or per promo calendar) | E-Commerce Manager |
| Category landing pages | Digital Merchandising | Monthly | E-Commerce Manager |
| Product images | Product Content Specialists | Per new item / per revision | Digital Merchandising Specialist |
| Product descriptions | Product Content Specialists | Per new item / per revision | Digital Merchandising Specialist |
| Promotional landing pages | Digital Merchandising | Per promo calendar | VP E-Commerce |
| Blog/DIY content | Marketing (per Doc 17) | Weekly | Content Manager |
| FAQ/Help pages | Customer Service (per Doc 24) | Quarterly | E-Commerce Manager |
| Store locator | Store Development (per Doc 22) | On change | E-Commerce Manager |

---

## 23.3 Product Catalog and Digital Merchandising

### 23.3.1 Catalog Structure

| Level | Count | Example | Oracle PLM Mapping |
|-------|-------|---------|-------------------|
| Department | 12 | Hardware & Tools | Department |
| Class | ~90 | Power Tools | Class |
| Subclass | ~400 | Cordless Drills | Subclass |
| Item | ~80,000 | Makita XTD01Z 18V Drill | Item |
| SKU (size/color variants) | ~120,000 | Makita XTD01Z - Blue | Item variant |

### 23.3.2 Product Content Standards

| Content Element | Standard | Compliance |
|----------------|----------|------------|
| Product title | [Brand] [Model/Name] [Key Spec] [Size/Variant] — max 150 characters | Mandatory for publish |
| Main image | White background, min 1000×1000px, JPEG/WebP, no watermark | Mandatory for publish |
| Additional images | Min 4 images (front, back, side, in-use/action shot); max 10 images | Mandatory for publish |
| 360° images | Required for appliances, power tools, faucets, lighting | Mandatory for top 5,000 SKUs |
| Product video | Demo/installation video; max 60 seconds; max 50MB | Required for top 2,000 SKUs |
| Short description | 2-3 sentence summary; key benefits | Mandatory for publish |
| Full description | Features, specifications, included accessories, material | Mandatory for publish |
| Technical specifications | Structured attributes (dimensions, weight, wattage, material, color) | Mandatory for publish |
| Safety warnings | Required for electrical, chemical (paint), power tools | Mandatory by category |
| Installation guide link | PDF download or link to CX Knowledge Management | Required for applicable categories |
| Energy efficiency label | Required for appliances (per DOE Philippine energy labeling) | Mandatory for appliances |
| Warranty information | Warranty period, coverage, claim process | Mandatory for publish |
| UPC/Barcode | Match POS/Oracle PLM barcode | Mandatory for publish |

### 23.3.3 SEO Requirements

| Element | Standard |
|---------|----------|
| URL structure | /shop/[department]/[subclass]/[product-slug] |
| Meta title | [Product Name] — Buy Online \| Tahanan Depot (max 60 chars) |
| Meta description | Product summary + price range + "Free shipping on orders above PHP 2,500" (max 155 chars) |
| H1 tag | Product name (auto-generated from title) |
| Alt text for images | [Product Name] — [View Angle] — Tahanan Depot |
| Schema markup | Product schema (name, image, price, availability, rating, reviews) |
| Breadcrumbs | Home > [Department] > [Class] > [Product Name] |
| Canonical URL | One canonical per product; no duplicates |
| Sitemap | Auto-generated daily; submitted to Google Search Console |
| Page speed | Target: Core Web Vitals "Good" (LCP < 2.5s, FID < 100ms, CLS < 0.1) |

### 23.3.4 Cross-Sell and Upsell Rules

| Rule Type | Logic | Display Location | Oracle Fusion Source |
|-----------|-------|------------------|---------------------|
| Frequently bought together | Items purchased together in > 5% of transactions (last 12 months) | Product page | CX CDP / POS analytics |
| Accessories | Pre-defined accessory relationships in PLM attributes | Product page, cart | PLM item relationships |
| Complete the project | Category-based bundles (e.g., paint + primer + brushes + tape + rollers) | Product page, cart | Merchandising-defined |
| Comparable products | Same subclass, similar price range | Product page | CX Commerce search |
| Higher-margin alternative | Better/Pro version of same product | Product page | Merchandising-defined |
| Recently viewed | Based on user browsing history | Homepage, category pages | CX CDP |
| Recommended for you | AI-powered personalization via CX CDP | Homepage, product page, email | CX CDP |

### 23.3.5 Ratings and Reviews

| Element | Policy |
|---------|--------|
| Review eligibility | Must be verified purchaser (POS or online) |
| Rating scale | 1-5 stars |
| Review moderation | Auto-publish; flagged for manual review if contains profanity, pricing, competitor mention |
| Review response | Customer Service responds within 48 hours to reviews < 3 stars |
| Photo reviews | Encouraged; 50 Tahanan Rewards bonus points for photo review |
| Review syndication | Reviews displayed on product pages, marketplace listings |
| Fake review prevention | Verified purchase flag; IP/device monitoring; no incentive for positive reviews |

---

## 23.4 Order Management and Fulfillment

### 23.4.1 Online Order Flow

| Step | Activity | System | Oracle Module |
|------|----------|--------|---------------|
| 1 | Customer adds items to cart | CX Commerce | CX Commerce |
| 2 | Real-time inventory check (ATP) | CX Commerce → Inventory | Inventory Management |
| 3 | Customer selects fulfillment method (delivery or pick-up-in-store) | CX Commerce | CX Commerce |
| 4 | Customer selects payment method and completes checkout | CX Commerce + Payment Gateway | CX Commerce |
| 5 | Payment authorized (or captured for COD) | Payment Gateway | — |
| 6 | Order created in CX Commerce; pushed to Oracle Order Management via OIC (INT-EC-004) | CX Commerce → OIC → OM | Order Management |
| 7 | Order routed to fulfillment location (warehouse or store) based on rules | Order Management | Order Management + GOP |
| 8 | Fulfillment location receives pick instruction | WMS / POS | Warehouse Management |
| 9 | Order picked, packed, and labeled | WMS / POS | Warehouse Management |
| 10 | Shipping label generated; carrier assigned | TMS | Transportation Management |
| 11 | Order status updated to "Shipped"; customer notification sent (email/SMS) | OM → CX Commerce → Customer | Order Management |
| 12 | Delivery executed; POD captured | TMS | Transportation Management |
| 13 | Order status updated to "Delivered"; customer notification sent | OM → CX Commerce → Customer | Order Management |
| 14 | BIR-compliant e-receipt/invoice generated and emailed | Accounting Hub → AR | Receivables + Accounting Hub |
| 15 | Inventory decremented; COGS recognized | Inventory + Cost Management | Inventory + Cost Management |
| 16 | Loyalty points earned (1 point per PHP 50 spent) | CX Loyalty | Customer Loyalty |
| 17 | Customer satisfaction survey triggered (24 hours after delivery) | CX Service | Service |

### 23.4.2 Fulfillment Models

| Model | Description | Eligible Items | Fulfillment Location | SLA |
|-------|-------------|---------------|---------------------|-----|
| Ship-from-Warehouse | Order picked and packed at regional DC; delivered via 3PL | All items (primary method) | Nearest DC with stock | 2-5 business days |
| Pick-Up-In-Store (Click-and-Collect) | Customer orders online; picks up at selected store | All items (except hazardous/oversized) | Selected store | Ready in 4 hours (if in-stock) |
| Ship-from-Store | Order fulfilled from store inventory when DC is out of stock | Fast-moving, non-bulky items | Nearest store with stock | 2-3 business days |
| Vendor Direct Ship | Large/specialty items shipped directly from supplier | Special-order items, large appliances | Vendor warehouse | Per vendor lead time (5-14 days) |
| Scheduled Delivery | Coordinated delivery for large/bulky items (building materials, appliances) | Lumber, cement, large appliances, kitchen cabinets | DC or store | Scheduled date (5-10 days) |

### 23.4.3 Order Fulfillment Rules Engine

| Rule | Priority | Logic |
|------|----------|-------|
| Same-region DC | 1 | Fulfill from DC in same region as delivery address (min shipping cost) |
| Click-and-Collect in-stock | 2 | If customer selected pick-up, fulfill from that store if stock available |
| Nearest DC with stock | 3 | If same-region DC OOS, route to next-nearest DC |
| Ship-from-Store | 4 | If all DCs OOS, fulfill from nearest store with stock (non-bulky only) |
| Split shipment | 5 | If order has items at multiple locations, split into sub-shipments |
| Backorder | 6 | If no location has stock, place on backorder; fulfill when replenished |

### 23.4.4 Delivery Area Coverage

| Region | Coverage | Delivery Zones | Standard Delivery SLA |
|--------|----------|---------------|----------------------|
| Metro Manila | All cities/municipalities | Zone 1 (same day), Zone 2 (next day) | Same day or next day |
| Luzon (outside MM) | Major cities and municipalities within 50km of store | Zone 3 (2-3 days) | 2-3 business days |
| Visayas | Cebu, Iloilo, Bacolod, Tacloban and surrounding areas | Zone 4 (3-5 days) | 3-5 business days |
| Mindanao | Davao, Cagayan de Oro, General Santos, Zamboanga | Zone 5 (3-5 days) | 3-5 business days |
| Remote areas | Barangays outside major cities; island municipalities | Zone 6 (7-14 days) | 7-14 business days |

### 23.4.5 Shipping Fees

| Order Value | Metro Manila | Luzon | Visayas/Mindanao | Oversized/Bulky |
|-------------|-------------|-------|------------------|-----------------|
| < PHP 2,500 | PHP 99 | PHP 149 | PHP 199 | Quoted at checkout |
| PHP 2,500 - 4,999 | PHP 49 | PHP 99 | PHP 149 | Quoted at checkout |
| ≥ PHP 5,000 | FREE | PHP 49 | PHP 99 | Quoted at checkout |
| Click-and-Collect | FREE | FREE | FREE | N/A |

### 23.4.6 Split Shipment and Backorder Handling

| Scenario | Handling | Customer Communication |
|----------|----------|----------------------|
| Partial fulfillment (some items in-stock, some not) | Ship in-stock items immediately; backorder remainder | Email at order split; email when backordered items ship |
| All items backordered | Order placed on hold; estimated ship date communicated | Email with estimated date; update when shipped |
| Backorder > 14 days | Customer offered: wait, substitute item, or cancel | Email/SMS with options |
| Backorder > 30 days | Auto-cancel with refund | Email notification of auto-cancellation |

---

## 23.5 Payment Processing

### 23.5.1 Supported Payment Methods

| Payment Method | Provider | Processing Fee | Settlement | Customer Limit |
|---------------|----------|---------------|------------|----------------|
| Visa/Mastercard (credit/debit) | BDO Payment Gateway | 2.5% per transaction | T+2 business days | Per card limit |
| GCash | GCash Business API | 2.0% per transaction | T+1 business day | PHP 500,000/month |
| Maya (PayMaya) | Maya Business API | 2.0% per transaction | T+1 business day | Per account limit |
| BPI, BDO, Metrobank online banking | PayMongo / Dragonpay | PHP 15 per transaction | T+1 business day | Per bank limit |
| PESONet bank transfer | Dragonpay | PHP 10 per transaction | T+1 business day | Per bank limit |
| Cash on Delivery (COD) | 3PL partner (collect-on-delivery) | PHP 50 + 1% per order | T+3 business days (via 3PL remittance) | PHP 50,000 max |
| Tahanan Gift Card | Internal (Oracle AR) | No fee | Immediate | Per card balance |
| Tahanan Rewards Points | Internal (CX Loyalty) | No fee | Immediate | Points balance (1 pt = PHP 1) |
| Installment (0% interest) | BDO, BPI, HSBC partner banks | 0% to customer; bank fee absorbed by Tahanan (3-5%) | Per bank settlement | 3/6/12 months; min PHP 3,000 |

### 23.5.2 Payment Reconciliation

| Step | Activity | System | Oracle Module |
|------|----------|--------|---------------|
| 1 | Payment captured at checkout | Payment Gateway | — |
| 2 | Payment confirmation sent to Oracle AR via OIC (INT-EC-008) | Payment Gateway → OIC → AR | Receivables |
| 3 | Receipt created in Oracle AR | AR | Receivables |
| 4 | Journal posted to GL via Accounting Hub | Accounting Hub | GL |
| 5 | Settlement received from payment provider (bank file) | Cash Management | Cash Management |
| 6 | Bank reconciliation auto-matched | Cash Management | Cash Management |
| 7 | Daily reconciliation: online order totals vs. payment gateway settlement vs. Oracle AR receipts | AR + Cash Mgmt + CX Commerce analytics | Receivables + Cash Management |

### 23.5.3 PCI-DSS Compliance

| Requirement | Implementation |
|------------|----------------|
| Cardholder data encryption | TLS 1.3 in transit; no storage of full card numbers (tokenized) |
| Payment page | Hosted checkout page (redirect to BDO Payment Gateway) — SAQ A compliance |
| Network security | Separate DMZ for e-commerce; WAF (Web Application Firewall) |
| Access control | Role-based access to payment configuration; 2FA required |
| Vulnerability scanning | Quarterly ASV scan; annual penetration test |
| Compliance validation | Annual PCI-DSS SAQ-A submission; QSA review |

### 23.5.4 BIR Compliance for Online Transactions

| Requirement | Implementation |
|------------|----------------|
| BIR-registered receipt/invoice | E-receipt generated per transaction; sequential numbering; BIR permit number displayed |
| VAT (12%) | Computed and displayed per item and on total; remitted per BIR schedule |
| Sales invoice format | BIR-compliant format: TIN, business name, address, item details, VAT breakdown |
| Authority to Print (ATP) | E-receipt ATP registered with BIR RDO |
| Summary of Sales | Monthly electronic summary submitted to BIR |

---

## 23.6 Customer Account and Loyalty Integration

### 23.6.1 Online Account Features

| Feature | Description | Oracle Module |
|---------|-------------|---------------|
| Registration | Email/phone registration; optional social login (Google, Facebook) | CX Commerce + CDP |
| Profile management | Name, contact, addresses, communication preferences | CX CDP |
| Order history | All online orders with status, tracking, invoices | CX Commerce + OM |
| Loyalty dashboard | Points balance, tier status, transaction history, points expiry | CX Loyalty |
| Wishlist | Save products for later; low-stock alerts for wishlisted items | CX Commerce |
| Saved addresses | Multiple delivery addresses; default address selection | CX Commerce |
| Payment methods | Saved cards (tokenized), GCash/Maya linked accounts | Payment Gateway |
| Recurring orders | Scheduled repeat orders (e.g., water filters, light bulbs) | CX Commerce + OM |

### 23.6.2 Loyalty Program Online Integration

| Feature | Online Behavior | Oracle Module |
|---------|----------------|---------------|
| Points earning | 1 point per PHP 50 spent online (same as in-store) | CX Loyalty |
| Points redemption | Redeem at checkout; 1 point = PHP 1 discount; max 50% of order value | CX Loyalty + Commerce |
| Tier progression | Silver (0-49,999 annual), Gold (50,000-149,999), Platinum (≥ 150,000) — combined online+in-store | CX Loyalty |
| Online bonus points | Double points events, birthday bonus, first online purchase bonus | CX Loyalty + Marketing |
| Points across channels | Points earned online usable in-store and vice versa | CX Loyalty + CDP |
| Loyalty member pricing | Exclusive member prices on select items | Oracle Pricing + CX Loyalty |

### 23.6.3 B2B Portal (Contractor/Developer)

| Feature | Description | Oracle Module |
|---------|-------------|---------------|
| B2B account registration | Credit application, business documents, trade references | CX Commerce + AR |
| Credit limit display | Real-time available credit; order blocking at limit | AR Credit Management |
| Contract pricing | Customer-specific price lists from Oracle Pricing | Oracle Pricing |
| Bulk ordering | CSV upload, quick-order by SKU, saved order templates | CX Commerce |
| Quote request | RFQ for large/project orders; CPQ integration | CX Sales + CPQ |
| Order approval workflow | Multi-approver for PO-based orders | Order Management |
| Project tracking | Order history by project name/PO number | CX Commerce + OM |
| Invoice management | View/download invoices; statement of account | AR + CX Commerce |
| Reorder | One-click reorder from previous orders | CX Commerce |

---

## 23.7 Marketplace and Partner Integrations

### 23.7.1 Marketplace Presence

| Marketplace | Store Name | Category Focus | Commission Rate | Monthly GMV Target |
|-------------|-----------|---------------|-----------------|-------------------|
| Lazada | Tahanan Depot Official | All categories | 2-5% (category-based) | PHP 40,000,000 |
| Shopee | Tahanan Depot Official | All categories | 2-6% (category-based) | PHP 35,000,000 |
| Facebook/Instagram Shops | Tahanan Depot | Selected categories | 0% (organic), ad spend variable | PHP 5,000,000 |

### 23.7.2 Marketplace Integration Architecture

| Component | Configuration | Frequency |
|-----------|--------------|-----------|
| Product feed | Automated XML/CSV feed from Oracle PLM to marketplace APIs | Daily (full), hourly (price/stock delta) |
| Inventory sync | Oracle Inventory ATP pushed to marketplace stock levels | Every 15 minutes |
| Order sync | Marketplace orders pulled into Oracle Order Management | Every 5 minutes |
| Shipment tracking | Tracking numbers pushed from Oracle TMS to marketplace | Per shipment |
| Price sync | Oracle Pricing pushed to marketplace; parity management | Hourly |
| Product content sync | Product titles, descriptions, images synced from CX Commerce catalog | Daily |
| Return/refund sync | Marketplace returns/refunds synced to Oracle AR | Daily batch |

### 23.7.3 Marketplace Fulfillment Models

| Model | Description | Used For |
|-------|-------------|----------|
| Fulfillment by Merchant (FBM) | Tahanan Depot picks, packs, and ships from own DC/store | Primary model for all marketplaces |
| Fulfillment by Lazada/Shopee (FBL/FBS) | Marketplace warehouse fulfillment for select fast-moving SKUs | Top 500 SKUs during major sale events (11.11, 12.12, payday sales) |
| Dropship via Marketplace | Marketplace handles delivery; Tahanan Depot provides products at DC | Bulky/heavy items (cement, lumber) — pilot program |

### 23.7.4 Channel Conflict and Pricing Parity

| Policy | Rule |
|--------|------|
| Price parity | Online prices (own site + marketplace) must match in-store prices, except for online-only promotions |
| Online-exclusive promotions | Max 10% additional discount vs. in-store; requires VP E-Commerce + VP Merchandising approval |
| Marketplace pricing | Match own-site pricing; marketplace vouchers/subsidies from marketplace platform are excluded from parity check |
| B2B pricing | B2B/contractor pricing is separate from B2C online pricing; not displayed on public marketplaces |
| Clearance pricing | Online clearance prices may differ from in-store; each channel manages own clearance |

---

## 23.8 Online Returns and Refunds

### 23.8.1 Online Return Policy

| Category | Return Window | Condition | Refund Method |
|----------|--------------|-----------|---------------|
| General merchandise | 30 days from delivery | Unused, original packaging | Original payment method or store credit |
| Appliances | 30 days from delivery | Unused, original packaging, all accessories | Original payment method |
| Building materials (per cut/piece) | 7 days from delivery | Unopened, unused | Original payment method |
| Paint and chemicals | 7 days from delivery | Unopened, sealed | Original payment method |
| Power tools | 30 days from delivery | Unused, original packaging, all accessories | Original payment method or store credit |
| Custom/special-order items | Non-returnable (unless defective) | — | — |
| Installed items (via Field Service) | Warranty claim only (per Doc 24) | — | Per warranty terms |
| Gift cards | Non-returnable | — | — |

### 23.8.2 Online Return Process

| Step | Activity | System | Oracle Module |
|------|----------|--------|---------------|
| 1 | Customer initiates return via online self-service portal or calls contact center | CX Digital Customer Service / CX Service | Service |
| 2 | System validates return eligibility (within window, correct status) | CX Commerce | CX Commerce |
| 3 | Customer selects return method: drop-off at store, or courier pick-up | CX Commerce | CX Commerce |
| 4 | Return label generated (for courier pick-up) or QR code (for in-store drop-off) | CX Commerce | CX Commerce |
| 5 | Customer ships/brings item | 3PL or in-store | — |
| 6 | Item received and inspected (quality check) | Store / DC QA | Inventory Management |
| 7 | Return approved or rejected (with reason) | Order Management | Order Management |
| 8 | If approved: credit memo created in Oracle AR | AR | Receivables |
| 9 | Refund processed to original payment method (3-7 business days for cards, 1-2 days for e-wallets) | Payment Gateway + AR | Receivables |
| 10 | Inventory returned to appropriate subinventory (resalable or damaged) | Inventory | Inventory Management |
| 11 | GL journal posted (revenue reversal, COGS reversal, inventory adjustment) | GL | General Ledger |
| 12 | Customer notified of refund completion | CX Commerce | CX Commerce |
| 13 | Customer satisfaction survey triggered | CX Service | Service |

### 23.8.3 Return Shipping Costs

| Return Reason | Shipping Cost | Deducted From Refund |
|---------------|---------------|---------------------|
| Defective/incorrect item | FREE (Tahanan Depot bears cost) | No |
| Change of mind | PHP 99 (courier) or FREE (in-store drop-off) | Yes (for courier) |
| Not as described | FREE | No |
| Damaged in transit | FREE | No |

---

## 23.9 E-Commerce Customer Service

### 23.9.1 Online Support Channels

| Channel | Availability | Response SLA | Staffing |
|---------|-------------|-------------|----------|
| Live chat (website/app) | 7:00 AM - 10:00 PM daily | < 30 seconds initial response | 8 agents (2 shifts) |
| Email (support@tahanandepot.com.ph) | 24/7 (response during operating hours) | < 4 hours | Shared with contact center (per Doc 24) |
| Phone hotline (per Doc 24) | 7:00 AM - 9:00 PM daily | < 60 seconds answer time | Shared with contact center |
| Social media (Facebook, Instagram, X) | 7:00 AM - 10:00 PM daily | < 1 hour | 3 social media support agents |
| Chatbot (AI) | 24/7 | Instant | Automated (Oracle Digital Assistant) |

### 23.9.2 Chatbot Capabilities

| Function | Capability | Handoff |
|----------|-----------|---------|
| Order status inquiry | Customer provides order number; bot returns status and tracking | Live agent if issue |
| Return initiation | Bot guides through return eligibility check and initiates return | Live agent if complex |
| Product inquiry | Bot answers FAQ about products, specs, availability | Live agent if not in knowledge base |
| Store locator | Bot provides nearest store based on customer location | — |
| Loyalty points inquiry | Bot displays points balance, tier, expiry | Live agent if discrepancy |
| Payment inquiry | Bot confirms payment status for specific order | Live agent if failed payment |
| FAQ | Bot answers top 100 FAQs from CX Knowledge Management | Live agent if unresolved |

### 23.9.3 Escalation Matrix

| Issue Type | L1 (Chat/Email Agent) | L2 (E-Commerce Specialist) | L3 (Manager/Technical) |
|------------|----------------------|---------------------------|----------------------|
| Order inquiry | Status check, tracking | Lost shipment investigation | System-level order issue |
| Payment issue | Payment status check | Failed payment troubleshooting | Payment gateway escalation |
| Return/refund | Initiate return, check status | Quality dispute, partial refund | Policy exception approval |
| Product inquiry | Specs, availability | Technical product question | Product defect report |
| Account issue | Password reset, basic profile | Account lockout, data correction | System integration issue |
| Delivery issue | Reschedule, address correction | Carrier escalation, redelivery | Warehouse fulfillment failure |
| Website/app bug | Capture details, workaround | Bug triage, ticket creation | Development team fix |
| Complaint | Apologize, offer resolution | Escalate for compensation | VP approval for high-value |

---

## 23.10 E-Commerce Analytics and Performance

### 23.10.1 Key Performance Indicators

| KPI | Definition | Target | Measurement Frequency | Oracle Source |
|-----|-----------|--------|----------------------|---------------|
| Gross Merchandise Value (GMV) | Total online sales value (before returns) | PHP 1.5B annual | Daily | CX Commerce + AR |
| Net Revenue | GMV minus returns and cancellations | PHP 1.35B annual | Daily | AR |
| Conversion Rate | Orders / total visits | ≥ 2.5% | Daily | CX Commerce analytics |
| Average Order Value (AOV) | Net revenue / orders | ≥ PHP 3,500 | Daily | CX Commerce + AR |
| Bounce Rate | Single-page visits / total visits | < 40% | Weekly | CX Commerce analytics |
| Cart Abandonment Rate | Carts created but not completed | < 65% | Weekly | CX Commerce analytics |
| Return Rate | Online returns / online orders | < 5% | Monthly | Order Management |
| Customer Acquisition Cost (CAC) | Marketing spend / new customers acquired | < PHP 350 | Monthly | Marketing + CX Commerce |
| Customer Lifetime Value (CLV) | Average 3-year revenue per customer | > PHP 15,000 | Quarterly | CX CDP + AR |
| Net Promoter Score (NPS) — Online | Online customer NPS survey | ≥ 45 | Quarterly | CX Service |
| Click-and-Collect Adoption | Click-and-collect orders / total online orders | ≥ 20% | Monthly | Order Management |
| Mobile Share | Mobile orders / total online orders | ≥ 55% | Monthly | CX Commerce analytics |
| On-Time Delivery | Orders delivered within promised SLA | ≥ 95% | Weekly | TMS |
| Order-to-Door Time | Average time from order to delivery | ≤ 3 business days | Weekly | TMS + OM |
| Marketplace GMV | Total sales via Lazada + Shopee + social | PHP 960M annual | Monthly | Marketplace dashboards |
| Product Content Completeness | % of SKUs with all mandatory content fields | ≥ 98% | Monthly | PLM + CX Commerce |

### 23.10.2 Revenue Reporting

| Report | Frequency | Audience | Oracle Source |
|--------|-----------|----------|---------------|
| Daily sales flash | Daily | VP E-Commerce, CMO, COO | CX Commerce + AR |
| Weekly performance dashboard | Weekly | E-Commerce team, Marketing | CX Commerce + FDI |
| Monthly P&L by channel | Monthly | CFO, VP E-Commerce, CMO | GL + AR + SCM Analytics |
| Category performance (online) | Monthly | Merchandising, E-Commerce | CX Commerce + Inventory |
| Marketplace performance | Weekly | Marketplace team | Marketplace APIs + OM |
| Campaign performance | Per campaign | Marketing, E-Commerce | CX Marketing + CX Commerce |
| Customer cohort analysis | Quarterly | VP E-Commerce, CMO | CX CDP + FDI |
| Fulfillment cost analysis | Monthly | E-Commerce Fulfillment, Supply Chain | TMS + Inventory + GL |

### 23.10.3 Customer Acquisition and Analytics

| Metric | Target | Budget Allocation | Channel |
|--------|--------|-------------------|---------|
| Organic search (SEO) | 35% of traffic | PHP 12M (content + technical SEO) | Google, Bing |
| Paid search (SEM) | 25% of traffic | PHP 45M (Google Ads, Bing Ads) | Google Shopping, Search |
| Social media (paid) | 15% of traffic | PHP 30M (Meta, TikTok Ads) | Facebook, Instagram, TikTok |
| Email marketing | 10% of traffic | PHP 5M (platform + creative) | Email campaigns |
| Direct/brand | 10% of traffic | — | Direct type-in, app |
| Affiliates and referral | 5% of traffic | PHP 8M (commissions) | Bloggers, influencers, affiliates |

---

## 23.11 E-Commerce Standard Operating Procedures

### SOP-EC-001: Online Order Processing

| Step | Activity | Responsible | System |
|------|----------|-------------|--------|
| 1 | Order received in Oracle Order Management via OIC (INT-EC-004) | System (automated) | OIC + OM |
| 2 | Order validated: payment confirmed, inventory allocated, pricing verified | System (automated) | OM + Inventory + Pricing |
| 3 | Fraud screening (rules-based: high-value, new account, multiple orders) | System + Order Processing Specialist | CX Commerce + OM |
| 4 | Order routed to fulfillment location per fulfillment rules engine | System (automated) | OM + GOP |
| 5 | Pick list generated at fulfillment location | System (automated) | WMS / POS |
| 6 | Order picked and packed; quality check on high-value items | Warehouse/Store Associate | WMS / POS |
| 7 | Shipping label generated; carrier assigned | System (automated) | TMS |
| 8 | Shipment confirmed; customer notified | System (automated) | OM + CX Commerce |
| 9 | Exception handling: OOS, payment failure, address issue | Order Processing Specialist | OM |
| 10 | Daily order processing report reviewed | E-Commerce Fulfillment Manager | CX Commerce + OM |

### SOP-EC-002: Click-and-Collect Operations

| Step | Activity | Responsible | System |
|------|----------|-------------|--------|
| 1 | Customer places order online; selects store for pick-up | Customer | CX Commerce |
| 2 | Order routed to selected store; inventory reserved | System | OM + Inventory |
| 3 | Store receives pick notification (POS alert + email) | System | POS + OM |
| 4 | Store associate picks items from sales floor/backroom | Store Associate | POS |
| 5 | Items placed in designated click-and-collect staging area | Store Associate | POS |
| 6 | Customer notified: "Order ready for pick-up" (email + SMS) | System | CX Commerce |
| 7 | Customer arrives at store; presents order confirmation + valid ID | Customer | — |
| 8 | Store associate verifies ID against order; releases items | Store Associate | POS |
| 9 | POS confirms order picked up; inventory decremented | Store Associate | POS + Inventory |
| 10 | If not picked up within 5 days: customer notified; items returned to shelf; order cancelled | System + Store Associate | OM + POS |
| 11 | Refund processed for uncollected orders | Order Processing Specialist | AR |

### SOP-EC-003: Product Content Upload and Maintenance

| Step | Activity | Responsible | Frequency |
|------|----------|-------------|-----------|
| 1 | New item created in Oracle PLM with all mandatory attributes | Merchandising (per Doc 25) | Per new item |
| 2 | Product data synced to CX Commerce via OIC (INT-EC-001) | System (automated) | Hourly |
| 3 | Product Content Specialist reviews auto-populated fields | Product Content Specialist | Daily |
| 4 | Product images uploaded (main + additional); SEO fields populated | Product Content Specialist | Per new item |
| 5 | Product video uploaded if required (top 2,000 SKUs) | Product Content Specialist | Per schedule |
| 6 | Product description enriched (marketing copy, features, specs) | Product Content Specialist | Per new item |
| 7 | Cross-sell/upsell relationships configured | Digital Merchandising Specialist | Per new item |
| 8 | Content quality check against content standards (section 23.3.2) | Digital Merchandising Specialist | Per new item |
| 9 | Product published to live site | Product Content Specialist | After QC pass |
| 10 | Monthly content completeness audit (target: ≥ 98%) | E-Commerce Manager | Monthly |

### SOP-EC-004: Online Promotion Setup

| Step | Activity | Responsible | System |
|------|----------|-------------|--------|
| 1 | Promotional calendar received from Marketing (per Doc 17) | E-Commerce Manager | CX Commerce + Oracle Pricing |
| 2 | Online promotion details confirmed: dates, products, discount %, mechanics | VP E-Commerce | — |
| 3 | Promotional price list created in Oracle Pricing | Pricing Analyst | Oracle Pricing |
| 4 | Promotion configured in CX Commerce: banners, landing pages, badges | Digital Merchandising Specialist | CX Commerce |
| 5 | Coupon/voucher codes generated (if applicable) | E-Commerce Manager | CX Commerce |
| 6 | Inventory pre-positioned for expected promo volume | Supply Planning (per Doc 04) | SCP + Inventory |
| 7 | QA test: verify correct pricing, banner display, checkout flow on staging | QA Analyst | CX Commerce (staging) |
| 8 | Promotion activated at scheduled time | System (scheduled) | CX Commerce + Oracle Pricing |
| 9 | Real-time monitoring during first 2 hours: traffic, conversion, errors | E-Commerce Manager | CX Commerce analytics |
| 10 | Post-promotion analysis: lift, margin impact, sell-through, new customers | E-Commerce Data Analyst | FDI + CX Analytics |

### SOP-EC-005: Marketplace Order Management

| Step | Activity | Responsible | System |
|------|----------|-------------|--------|
| 1 | Marketplace orders synced to Oracle OM (every 5 minutes) | System (automated) | Marketplace API + OIC + OM |
| 2 | Orders validated and routed to fulfillment location | System (automated) | OM |
| 3 | Pick and pack per marketplace packaging requirements | Warehouse Associate | WMS |
| 4 | Marketplace-compliant shipping label generated | System | TMS + Marketplace API |
| 5 | Shipment confirmation pushed to marketplace | System (automated) | Marketplace API |
| 6 | Tracking number updated on marketplace | System (automated) | Marketplace API |
| 7 | Marketplace returns/refunds synced to Oracle AR (daily) | System (automated) | Marketplace API + OIC + AR |
| 8 | Marketplace fees reconciled monthly | Marketplace Specialist | AR + Marketplace portal |
| 9 | Listing quality and content freshness reviewed weekly | Marketplace Specialist | Marketplace analytics |
| 10 | Monthly marketplace performance report | E-Commerce Data Analyst | FDI + Marketplace analytics |

### SOP-EC-006: Online Payment Reconciliation

| Step | Activity | Responsible | System |
|------|----------|-------------|--------|
| 1 | Daily online sales report generated from CX Commerce | System (automated) | CX Commerce |
| 2 | Daily online receipts report generated from Oracle AR | System (automated) | AR |
| 3 | Compare CX Commerce gross sales vs. Oracle AR receipts | E-Commerce Data Analyst | Excel / FDI |
| 4 | Variance analysis: identify discrepancies (failed payments, partial captures, refunds) | E-Commerce Data Analyst | AR + Payment Gateway |
| 5 | Payment gateway settlement report downloaded | E-Commerce Data Analyst | Payment Gateway portal |
| 6 | Settlement reconciled against Oracle Cash Management bank statements | Treasury (per Doc 19) | Cash Management |
| 7 | Discrepancies investigated and resolved within 3 business days | Order Processing Specialist | AR + Payment Gateway |
| 8 | Monthly reconciliation report submitted to Finance | E-Commerce Data Analyst | FDI |

---

## 23.12 E-Commerce Policies

### POL-EC-001: Online Pricing and Promotion Policy

**Effective Date:** 2026-01-01
**Applies To:** Tahanan Retail Inc., Tahanan Digital Inc.
**Oracle Fusion Module:** Oracle Pricing, CX Commerce

| Element | Policy |
|---------|--------|
| Price parity | Online prices must match in-store prices unless approved online-exclusive promotion |
| Online-exclusive discount | Max 10% additional discount; requires VP E-Commerce + VP Merchandising approval |
| Flash sales | Max 24 hours; max 30% discount; max 100 SKUs; VP E-Commerce approval |
| Coupon stacking | Max 1 coupon per order; system-enforced |
| Price matching | Online prices price-matched with in-store; not with competitor websites |
| Pricing errors | If pricing error discovered: honor orders already placed; correct immediately; notify affected customers |

### POL-EC-002: Online Order Fulfillment SLA Policy

**Effective Date:** 2026-01-01
**Applies To:** Tahanan Retail Inc., Tahanan Supply Chain Inc.
**Oracle Fusion Module:** Order Management, Warehouse Management, Transportation Management

| Fulfillment Type | SLA | Breach Protocol |
|-----------------|-----|----------------|
| Standard delivery (Metro Manila) | 2 business days | Auto-notify customer; PHP 200 store credit if > 4 days |
| Standard delivery (Luzon) | 3 business days | Auto-notify customer; PHP 200 store credit if > 5 days |
| Standard delivery (Visayas/Mindanao) | 5 business days | Auto-notify customer; PHP 200 store credit if > 7 days |
| Click-and-collect | 4 hours (if in-stock) | Auto-notify customer; PHP 100 store credit if > 24 hours |
| Scheduled delivery (bulky items) | Agreed date ± 1 day | Reschedule at no cost; PHP 500 credit if > 2 days late |

### POL-EC-003: Marketplace Management Policy

**Effective Date:** 2026-01-01
**Applies To:** Tahanan Retail Inc., Tahanan Digital Inc.
**Oracle Fusion Module:** CX Commerce, Order Management

| Element | Policy |
|---------|--------|
| Authorized marketplaces | Lazada, Shopee, Facebook/Instagram Shops only; new marketplaces require VP E-Commerce + CMO approval |
| Marketplace exclusivity | No exclusive deals with any marketplace; all platforms carry same assortment |
| Branding | "Tahanan Depot Official" store name; Tahanan Depot branding on all listings |
| Customer data | Marketplace customer data owned by marketplace; no direct marketing to marketplace customers without their consent |
| Inventory allocation | Marketplace inventory allocated from dedicated DC stock; max 30% of available inventory per SKU |
| Rating maintenance | Minimum 4.5 stars on all marketplaces; action plan required if below threshold |

---

## 23.13 Document Control

| Field | Detail |
|-------|--------|
| Document Title | E-Commerce Operations |
| Document Set | Tahanan Depot Operations Documentation |
| Document Number | Doc 23 |
| Department | E-Commerce / Marketing / Supply Chain |
| Review Cycle | Annual (or upon significant platform change) |
| Last Reviewed | March 15, 2026 |
| Next Review | March 15, 2027 |
| Owner | VP E-Commerce |
| Approved By | Chief Marketing Officer |

### Revision History

| Rev | Date | Author | Description |
|-----|------|--------|-------------|
| 1.0 | Mar 15, 2026 | L. Mendoza | Initial release |
