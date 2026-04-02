# 01 — EXECUTIVE SUMMARY

## 1.1 Company Overview

**Tahanan Depot** is a hypothetical Philippine home improvement and construction materials retail chain modeled after The Home Depot (USA) and Wilcon Depot (Philippines). The company operates 120 retail stores, 4 regional distribution warehouses, and 1 corporate headquarters, all within the Philippines.

The word "Tahanan" means "Home" in Filipino, reflecting the company's mission to be the nation's premier destination for home building, improvement, and furnishing needs.

### Mission Statement
To empower every Filipino family and builder with quality products, expert service, and innovative solutions for building, improving, and maintaining homes and commercial spaces — delivered through world-class operational excellence.

### Vision Statement
To be the Philippines' most trusted and efficient home improvement retailer, setting the standard for technology-driven retail operations in Southeast Asia.

## 1.2 Scale of Operations

| Parameter | Value |
|-----------|-------|
| Retail Stores | 120 (across Luzon, Visayas, Mindanao) |
| Distribution Warehouses | 4 (North Luzon, South Luzon, Visayas, Mindanao) |
| Corporate Headquarters | 1 (Taguig City, Metro Manila) |
| SKU Count | ~80,000 active SKUs |
| Suppliers | ~2,500 active |
| Employees | ~6,500 |
| Projected Annual Revenue | PHP 45 billion |
| Store Average Size | 5,000-10,000 sqm |
| Warehouse Average Size | 20,000-30,000 sqm |

## 1.3 Product Categories

Following the Home Depot / Wilcon model, Tahanan Depot sells:

| Department | Examples |
|------------|----------|
| Lumber & Building Materials | Plywood, cement, steel bars, hollow blocks, roofing |
| Electrical | Wiring, circuit breakers, lighting fixtures, switches |
| Plumbing | PVC pipes, fittings, faucets, water heaters, toilets |
| Paint & Decorating | Interior/exterior paint, wallpaper, brushes, rollers |
| Hardware & Tools | Hand tools, power tools, fasteners, adhesives |
| Appliances | Air conditioners, refrigerators, washing machines |
| Flooring & Tiles | Ceramic tiles, vinyl planks, laminates, adhesives |
| Kitchen & Bath | Cabinets, countertops, sinks, vanities, fixtures |
| Doors & Windows | Entry doors, interior doors, glass windows, screens |
| Garden & Outdoor | Plants, pots, outdoor furniture, grills, fertilizers |
| Safety & Security | Locks, CCTV systems, fire extinguishers, PPE |
| Storage & Organization | Shelving, cabinets, bins, tool storage |

## 1.4 Strategic Technology Decision

Tahanan Depot has made a strategic decision to:

1. **Adopt Oracle Fusion Cloud Suite** as the enterprise backbone for ERP, SCM, HCM, EPM, CX, and analytics — maximizing every available feature and module that adds value to the retail operation.

2. **Develop a custom POS system in-house** tailored to Philippine retail requirements (BIR compliance, local payment methods, Filipino UX), which will be integrated with Oracle Fusion via Oracle Integration Cloud (OIC).

This hybrid approach provides the enterprise-grade backbone of Oracle Fusion with the flexibility and localization of a custom POS solution.

## 1.5 Oracle Fusion Cloud Suite — Modules in Scope

The following Oracle Fusion Cloud modules will be fully deployed:

### Core ERP
| Module | Purpose |
|--------|---------|
| General Ledger | Multi-ledger, multi-currency accounting |
| Payables | Supplier invoice processing and payments |
| Receivables | Customer billing and collections |
| Assets | Fixed asset tracking and depreciation |
| Expenses | Employee expense management |
| Revenue Management | Revenue recognition (ASC 606/IFRS 15) |
| Cash Management | Bank reconciliation and cash positioning |
| Accounting Hub | Subledger accounting for POS transactions |

### Supply Chain Management (SCM)
| Module | Purpose |
|--------|---------|
| Supply Chain Planning | Demand forecasting, supply planning, S&OP |
| Inventory Management | Multi-location inventory, costing, transfers |
| Order Management | Omnichannel order orchestration |
| Warehouse Management | DC/warehouse operations |
| Transportation Management | Freight and delivery management |
| Global Trade Management | Import compliance, customs, duties |
| Product Lifecycle Management | Item master, quality management |
| Cost Management | Product costing and margin analysis |

### Procurement
| Module | Purpose |
|--------|---------|
| Supplier Management | Supplier qualification and evaluation |
| Sourcing | RFQ, bidding, supplier selection |
| Purchasing | Purchase orders, automated requisitions |
| Procurement Contracts | Supplier agreements and terms |
| Self-Service Procurement | Store-level requisitions |

### Human Capital Management (HCM)
| Module | Purpose |
|--------|---------|
| Core HR | Employee records, organization management |
| Recruiting | Talent acquisition |
| Onboarding | New hire orientation |
| Learning | Training and certifications |
| Performance Management | Goals, reviews, feedback |
| Compensation | Salary, incentives, benefits |
| Succession Planning | Leadership pipeline |
| Time and Labor | Timekeeping, attendance |
| Absence Management | Leaves and absences |
| Payroll | Philippine payroll processing |
| Workforce Scheduling | Store staff scheduling |
| Dynamic Skills | Skills tracking and gap analysis |
| Oracle ME | Employee experience platform |
| HR Help Desk | Employee support |

### Enterprise Performance Management (EPM)
| Module | Purpose |
|--------|---------|
| Planning | Budgeting, forecasting, scenario modeling |
| Financial Consolidation & Close | Multi-entity consolidation |
| Account Reconciliation | Automated reconciliation |
| Tax Reporting | Philippine tax compliance |
| Narrative Reporting | Management and regulatory reports |
| Profitability & Cost Management | Margin analysis by store/category |
| Enterprise Data Management | Master data governance |

### Customer Experience (CX)
| Module | Purpose |
|--------|---------|
| Marketing Automation | Campaign management |
| Customer Data Platform | 360-degree customer profiles |
| Customer Loyalty | Loyalty program management |
| Sales Force Automation | B2B sales (contractors, developers) |
| Commerce | E-commerce platform |
| Field Service | Installation and delivery scheduling |
| Service Center | Customer support |
| Digital Customer Service | Self-service portal |
| Knowledge Management | FAQ, product guides |

### Integration & Analytics
| Module | Purpose |
|--------|---------|
| Oracle Integration Cloud (OIC) | POS integration, API management |
| Process Automation | Workflow automation |
| Fusion Data Intelligence | Cross-domain analytics |
| ERP Analytics | Financial dashboards |
| SCM Analytics | Supply chain dashboards |
| HCM Analytics | Workforce analytics |
| CX Analytics | Customer analytics |

### Risk Management & Compliance
| Module | Purpose |
|--------|---------|
| Advanced Controls | Segregation of duties, access monitoring |
| Transaction Controls | Automated fraud detection |
| Audit & Compliance | SOX/ICFR workflows, audit trails |

## 1.6 Key Design Principles

1. **Single Source of Truth** — Oracle Fusion serves as the authoritative system for all financial, supply chain, HR, and customer data.
2. **Maximum Automation** — Leverage Oracle's AI agents and automation capabilities to minimize manual processes (target: 90%+ transaction automation).
3. **Real-Time Operations** — POS transactions propagate to Oracle Fusion in near-real-time via OIC.
4. **Data-Driven Decisions** — Embedded analytics, AI predictions, and dashboards at every level.
5. **Compliance by Design** — BIR, SEC, DOLE, and Philippine regulations built into workflows.
6. **Scalability** — Architecture supports growth to 300+ stores without structural changes.
