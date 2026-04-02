# 02 — ORGANIZATIONAL STRUCTURE

## 2.1 Corporate Structure

Tahanan Depot operates under a holding company model with legally separate subsidiaries, each registered with the Philippine Securities and Exchange Commission (SEC). This structure enables:
- Clear legal and financial separation of business lines
- Independent financial reporting per entity
- Optimized tax planning within BIR regulations
- Focused management per business unit
- Risk isolation

```
TAHANAN HOLDINGS, INC. (Holding Company)
├── Tahanan Retail, Inc.          (Retail Operations)
├── Tahanan Supply Chain, Inc.    (Warehousing & Distribution)
├── Tahanan Property, Inc.        (Real Estate & Facilities)
└── Tahanan Digital, Inc.         (E-Commerce, POS, IT Services)
```

### 2.1.1 Entity Details

| Entity | SEC Registration | BIR TIN | Primary Activity |
|--------|-----------------|---------|------------------|
| Tahanan Holdings, Inc. | CS202600001 | 000-000-001-000 | Investment holding, strategic governance |
| Tahanan Retail, Inc. | CS202600002 | 000-000-002-000 | Retail sales of home improvement products |
| Tahanan Supply Chain, Inc. | CS202600003 | 000-000-003-000 | Warehousing, distribution, procurement |
| Tahanan Property, Inc. | CS202600004 | 000-000-004-000 | Real estate leasing, facilities management |
| Tahanan Digital, Inc. | CS202600005 | 000-000-005-000 | E-commerce, POS development, IT managed services |

### 2.1.2 Intercompany Relationships

| From Entity | To Entity | Transaction Type | Oracle Fusion Mechanism |
|-------------|-----------|------------------|------------------------|
| Tahanan Retail | Tahanan Supply Chain | Inventory replenishment orders | Intercompany Sales Orders / Transfer Orders |
| Tahanan Retail | Tahanan Property | Store rent payments | Intercompany Invoices (Payables/Receivables) |
| Tahanan Retail | Tahanan Digital | IT services fee | Intercompany Service Agreements |
| Tahanan Supply Chain | Tahanan Property | Warehouse rent payments | Intercompany Invoices |
| Tahanan Supply Chain | Tahanan Digital | IT services fee | Intercompany Service Agreements |
| Tahanan Holdings | All Subsidiaries | Management fees | Intercompany Invoices |
| All Subsidiaries | Tahanan Holdings | Dividend remittances | Intercompany Journal Entries |

## 2.2 Functional Organization Chart

### 2.2.1 Tahanan Holdings, Inc. — Corporate Headquarters (Taguig City)

```
BOARD OF DIRECTORS
│
├── CHAIRMAN OF THE BOARD
│
└── PRESIDENT & CEO (Chief Executive Officer)
    │
    ├── CFO (Chief Financial Officer)
    │   ├── VP Finance & Controllership
    │   ├── VP Treasury
    │   ├── VP Financial Planning & Analysis
    │   ├── VP Tax & Compliance
    │   └── VP Internal Audit
    │
    ├── COO (Chief Operating Officer)
    │   ├── VP Store Operations
    │   ├── VP Merchandising
    │   ├── VP Supply Chain
    │       ├── VP Store Development
    │   ├── VP Loss Prevention & Security
    │   └── VP Customer Service
    │
    ├── CHRO (Chief Human Resources Officer)
    │   ├── VP Talent Acquisition
    │   ├── VP Total Rewards
    │   ├── VP Learning & Development
    │   ├── VP Employee Relations
    │   └── VP HR Business Partners
    │
    ├── CIO (Chief Information Officer)
    │   ├── VP Enterprise Applications (Oracle Fusion)
    │       ├── VP Product Development (POS, E-Commerce)
    │   ├── VP Infrastructure & Security
    │   └── VP Data & Analytics
    │
    ├── CMO (Chief Marketing Officer)
    │   ├── VP Brand & Advertising
    │   ├── VP Digital Marketing
    │   ├── VP Loyalty & CRM
    │   └── VP Trade Marketing
    │
    └── Chief Legal Officer
        ├── Corporate Secretary
        ├── Legal Counsel
        └── Compliance Officer
```

### 2.2.2 Tahanan Retail, Inc.

```
PRESIDENT — Tahanan Retail, Inc.
│
├── Regional Directors (4 regions)
│   ├── North Luzon Regional Director
│   ├── South Luzon Regional Director
│   ├── Visayas Regional Director
│   └── Mindanao Regional Director
│       │
│       └── District Managers (3 per region = 12 total)
│           │
│           └── Store Managers (10 per district = 120 total)
│               ├── Assistant Store Managers (2 per store = 240)
│               ├── Department Supervisors (6 per store = 720)
│               ├── Sales Associates (15 per store = 1,800)
│               ├── Cashiers (6 per store = 720)
│               └── Stock Associates (4 per store = 480)
│
│               *(Note: Per-store counts shown above are averages. Actual counts vary by store format; see Doc 14 — Store Operations Guide for format-specific staffing.)*
│
├── VP Merchandising Operations
│   ├── Category Managers (12 categories)
│   ├── Pricing Analysts
│   └── Planogram Specialists
│
├── VP Retail Finance
│   ├── Controllers
│   └── Store Finance Analysts
│
└── VP Retail HR
    ├── HR Business Partners
    └── Store HR Coordinators
```

### 2.2.3 Tahanan Supply Chain, Inc.

```
PRESIDENT — Tahanan Supply Chain, Inc.
│
├── VP Procurement
│   ├── Sourcing Managers (by product category)
│   ├── Buyer Planners
│   ├── Supplier Development Specialists
│   └── Import Specialists
│
├── VP Distribution Operations
│   ├── Warehouse Managers (4 warehouses)
│   │   ├── Warehouse Supervisors
│   │   ├── Receiving Clerks
│   │   ├── Put-away Clerks
│   │   ├── Pickers
│   │   ├── Packers
│   │   ├── Shipping Clerks
│   │   └── Inventory Control Clerks
│   └── Transportation Coordinators
│
├── VP Supply Chain Planning
│   ├── Demand Planners
│   ├── Supply Planners
│   └── S&OP Analysts
│
└── VP Supply Chain Finance
    └── Controllers
```

### 2.2.4 Tahanan Property, Inc.

```
PRESIDENT — Tahanan Property, Inc.
│
├── VP Real Estate Development
│   ├── Site Acquisition Managers
│   ├── Construction Project Managers
│   └── Architects & Engineers
│
├── VP Facilities Management
│   ├── Regional Facility Managers
│   ├── Maintenance Teams
│   └── Safety & Compliance Officers
│
└── VP Property Finance
    └── Controllers
```

### 2.2.5 Tahanan Digital, Inc.

```
PRESIDENT — Tahanan Digital, Inc.
│
├── VP Product Development
│   ├── POS Development Manager
│   │   ├── POS Backend Developers
│   │   ├── POS Frontend Developers
│   │   ├── POS QA Engineers
│   │   └── POS DevOps Engineers
│   ├── E-Commerce Manager
│   │   ├── Web Developers
│   │   ├── Mobile Developers
│   │   └── UX/UI Designers
│   └── API & Integration Manager
│       ├── Integration Developers (OIC)
│       └── API Engineers
│
├── VP Enterprise Applications
│   ├── Oracle Fusion Functional Leads
│   │   ├── ERP Lead
│   │   ├── SCM Lead
│   │   ├── HCM Lead
│   │   ├── EPM Lead
│   │   └── CX Lead
│   ├── Oracle Fusion Technical Leads
│   │   ├── BI / Analytics Developer
│   │   ├── Report Developers
│   │   └── Integration Developers
│   └── Oracle Fusion Administrators
│       ├── System Administrators
│       └── Security Administrators
│
├── VP Infrastructure & Cybersecurity
│   ├── Network Engineers
│   ├── Cloud Engineers (OCI)
│   ├── Cybersecurity Analysts
│   └── IT Support Specialists
│
├── VP Data & Analytics
│   ├── Data Engineers
│   ├── Data Scientists
│   └── BI Analysts
│
└── VP Digital Finance
    └── Controllers
```

## 2.3 Geographic Organization

### 2.3.1 Store Distribution by Region

| Region | Stores | Districts | Key Cities |
|--------|--------|-----------|------------|
| North Luzon | 30 | 3 | Baguio, Angeles, Dagupan, Cabanatuan, Tuguegarao |
| South Luzon (including Metro Manila) | 40 | 3 | Makati, Quezon City, Taguig, Calamba, Lucena, Legazpi |
| Visayas | 25 | 3 | Cebu, Iloilo, Bacolod, Tacloban, Dumaguete |
| Mindanao | 25 | 3 | Davao, Cagayan de Oro, General Santos, Zamboanga |
| **TOTAL** | **120** | **12** | |

### 2.3.2 Warehouse Locations

| Warehouse | Location | Coverage | Size (sqm) |
|-----------|----------|----------|------------|
| WH-NL | Clark Freeport Zone, Pampanga | North Luzon | 25,000 |
| WH-SL | Calamba, Laguna | South Luzon + Metro Manila | 30,000 |
| WH-VIS | Mandaue City, Cebu | Visayas | 25,000 |
| WH-MIN | Davao City | Mindanao | 20,000 |

## 2.4 Oracle Fusion Organizational Model

### 2.4.1 Enterprise Structure

```
ENTERPRISE: Tahanan Holdings, Inc.
│
├── LEGAL ENTITY: Tahanan Holdings, Inc.
│   ├── LEDGER: TH-Primary Ledger (PHP, Philippine Standards)
│   └── BUSINESS UNIT: BU-Holdings-Corporate
│
├── LEGAL ENTITY: Tahanan Retail, Inc.
│   ├── LEDGER: TR-Primary Ledger (PHP, Philippine Standards)
│   └── BUSINESS UNITS:
│       ├── BU-Retail-NorthLuzon
│       ├── BU-Retail-SouthLuzon
│       ├── BU-Retail-Visayas
│       ├── BU-Retail-Mindanao
│       └── BU-Retail-Merchandising
│
├── LEGAL ENTITY: Tahanan Supply Chain, Inc.
│   ├── LEDGER: TSC-Primary Ledger (PHP, Philippine Standards)
│   └── BUSINESS UNITS:
│       ├── BU-SCM-Procurement
│       ├── BU-SCM-WH-NorthLuzon
│       ├── BU-SCM-WH-SouthLuzon
│       ├── BU-SCM-WH-Visayas
│       ├── BU-SCM-WH-Mindanao
│       └── BU-SCM-Planning
│
├── LEGAL ENTITY: Tahanan Property, Inc.
│   ├── LEDGER: TP-Primary Ledger (PHP, Philippine Standards)
│   └── BUSINESS UNITS:
│       ├── BU-Property-RealEstate
│       └── BU-Property-Facilities
│
└── LEGAL ENTITY: Tahanan Digital, Inc.
    ├── LEDGER: TD-Primary Ledger (PHP, Philippine Standards)
    └── BUSINESS UNITS:
        ├── BU-Digital-POS
        ├── BU-Digital-ECommerce
        ├── BU-Digital-ITServices
        └── BU-Digital-Analytics
```

### 2.4.2 Chart of Accounts Structure (Flexfield)

| Segment | Name | Format | Example Values |
|---------|------|--------|----------------|
| 1 | Company | 3 alphanumeric | 100=Holdings, 200=Retail, 300=SCM, 400=Property, 500=Digital |
| 2 | Region | 2 numeric | 01=North Luzon, 02=South Luzon, 03=Visayas, 04=Mindanao, 05=Corporate |
| 3 | Cost Center | 5 alphanumeric | 10000=Store-001, 20000=WH-NL, 30000=Corp-HR |
| 4 | Natural Account | 6 numeric | 100100=Cash-Peso, 400100=Sales Revenue, 500100=COGS |
| 5 | Product Category | 4 alphanumeric | 1000=Lumber, 2000=Electrical, 3000=Plumbing |
| 6 | Intercompany | 3 alphanumeric | 100=Holdings, 200=Retail, 300=SCM, 400=Property, 500=Digital |
| 7 | Future Use | 2 alphanumeric | Reserved for future requirements |

### 2.4.3 Inventory Organization Hierarchy

```
ITEM MASTER ORGANIZATION (Tahanan Supply Chain Corp)
│
├── WH-NL (North Luzon Distribution Center)
│   ├── Subinventory: Finished Goods
│   ├── Subinventory: Raw Materials
│   ├── Subinventory: Staging
│   ├── Subinventory: Receiving
│   └── Subinventory: Returns
│
├── WH-SL (South Luzon Distribution Center)
│   └── (same subinventory structure)
│
├── WH-VIS (Visayas Distribution Center)
│   └── (same subinventory structure)
│
├── WH-MIN (Mindanao Distribution Center)
│   └── (same subinventory structure)
│
└── STORE-001 through STORE-120 (120 Store Organizations)
    ├── Subinventory: Sales Floor
    ├── Subinventory: Backroom
    ├── Subinventory: Receiving
    └── Subinventory: Damaged/Returns
```

### 2.4.4 HCM Organization Hierarchy

```
ENTERPRISE: Tahanan Holdings, Inc.
│
├── LEGAL EMPLOYER: Tahanan Holdings, Inc.
│   └── Department: Corporate Office
│
├── LEGAL EMPLOYER: Tahanan Retail, Inc.
│   ├── Department: North Luzon Region
│   │   └── Departments per Store (30 stores)
│   ├── Department: South Luzon Region
│   │   └── Departments per Store (40 stores)
│   ├── Department: Visayas Region
│   │   └── Departments per Store (25 stores)
│   ├── Department: Mindanao Region
│   │   └── Departments per Store (25 stores)
│   └── Department: Merchandising
│
├── LEGAL EMPLOYER: Tahanan Supply Chain, Inc.
│   ├── Department: Procurement
│   ├── Department: WH-North Luzon
│   ├── Department: WH-South Luzon
│   ├── Department: WH-Visayas
│   ├── Department: WH-Mindanao
│   └── Department: Supply Chain Planning
│
├── LEGAL EMPLOYER: Tahanan Property, Inc.
│   ├── Department: Real Estate Development
│   └── Department: Facilities Management
│
└── LEGAL EMPLOYER: Tahanan Digital, Inc.
    ├── Department: Product Development
    ├── Department: Enterprise Applications
    ├── Department: Infrastructure & Security
    └── Department: Data & Analytics
```

## 2.5 Headcount Summary

| Entity | Management | Professional | Operations | Total |
|--------|-----------|-------------|------------|-------|
| Tahanan Holdings | 15 | 25 | 10 | 50 |
| Tahanan Retail | 160 | 120 | 3,780 | 4,060 |
| Tahanan Supply Chain | 25 | 50 | 350 | 425 |
| Tahanan Property | 10 | 30 | 200 | 240 |
| Tahanan Digital | 15 | 110 | 50 | 175 |
| Cross-Entity Shared | — | 15 | — | 15 |
| **Total** | **225** | **350** | **4,390** | **4,965** |
| Contractual / Agency Staff | — | — | — | **~1,535** |
| **Grand Total** | | | | **~6,500** |

> **Note:** The 1,535 contractual/agency workers are primarily for warehouse operations, store promotions, and project-based construction. They are tracked in Oracle HCM as contingent workers.
