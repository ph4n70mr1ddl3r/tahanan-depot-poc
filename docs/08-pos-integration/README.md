# 08 — CUSTOM POS INTEGRATION ARCHITECTURE

## 8.1 Architecture Overview

The custom POS system is developed in-house by Tahanan Digital, Inc. and integrates with Oracle Fusion Cloud via Oracle Integration Cloud (OIC). This section documents the complete integration architecture, data flows, API contracts, and error handling.

### 8.1.1 High-Level Architecture Diagram

```
┌─────────────────────────────────────────────────────────────────┐
│                        CUSTOM POS SYSTEM                        │
│                    (120 Stores, ~500 Terminals)                  │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌────────────────┐  │
│  │ Frontend  │  │ Backend  │  │ Local DB │  │ Offline Cache  │  │
│  │ (React)   │  │ (Java/   │  │ (Postgres│  │ (Encrypted)    │  │
│  │           │  │  Spring)  │  │  /SQLite)│  │                │  │
│  └─────┬─────┘  └─────┬────┘  └──────────┘  └────────────────┘  │
│        │              │                                           │
│        └──────┬───────┘                                           │
│               │ REST API (Internal)                               │
└───────────────┼───────────────────────────────────────────────────┘
                │
                │ HTTPS/TLS 1.3
                ▼
┌─────────────────────────────────────────────────────────────────┐
│              ORACLE INTEGRATION CLOUD (OIC)                      │
│  ┌──────────────┐  ┌──────────────┐  ┌───────────────────────┐ │
│  │ API Gateway  │  │ Integration  │  │ Process Automation    │ │
│  │ (Rate Limit, │  │ Flows        │  │ (Approval Workflows)  │ │
│  │  Auth, Log)  │  │ (Transform,  │  │                       │ │
│  │              │  │  Route)      │  │                       │ │
│  └──────────────┘  └──────┬───────┘  └───────────────────────┘ │
│                           │                                      │
└───────────────────────────┼──────────────────────────────────────┘
                            │
          ┌─────────────────┼─────────────────┐
          │                 │                  │
          ▼                 ▼                  ▼
┌──────────────┐  ┌──────────────┐  ┌──────────────────┐
│ Oracle ERP   │  │ Oracle SCM   │  │ Oracle CX        │
│ (AR, GL,     │  │ (Inventory,  │  │ (Loyalty, CDP,   │
│  Accounting  │  │  Cost Mgmt)  │  │  Marketing)      │
│  Hub)        │  │              │  │                  │
└──────────────┘  └──────────────┘  └──────────────────┘
          │                 │                  │
          └─────────────────┼─────────────────┘
                            │
                            ▼
                 ┌──────────────────┐
                 │ Oracle HCM       │
                 │ (Time & Labor)   │
                 └──────────────────┘
```

---

## 8.2 Integration Flows

### 8.2.1 Integration Flow Inventory

| Flow ID | Name | Direction | Frequency | OIC Pattern | Priority |
|---------|------|-----------|-----------|-------------|----------|
| INT-001 | POS Sales Transaction | POS → Oracle | Real-time (per txn) | Orchestration | Critical |
| INT-002 | POS Return Transaction | POS → Oracle | Real-time (per txn) | Orchestration | Critical |
| INT-003 | Price & Promotion Sync | Oracle → POS | Every 15 minutes | Scheduled | High |
| INT-004 | Item Master Sync | Oracle → POS | Every 30 minutes | Scheduled | High |
| INT-005 | Inventory Receipt | POS → Oracle | Real-time | Orchestration | High |
| INT-006 | Inventory Adjustment | POS → Oracle | Real-time | Orchestration | Medium |
| INT-007 | Loyalty Point Inquiry | POS ↔ Oracle | Real-time | Request-Reply | High |
| INT-008 | Loyalty Point Earn/Redeem | POS → Oracle | Real-time (per txn) | Orchestration | High |
| INT-009 | Gift Card Balance Inquiry | POS ↔ Oracle | Real-time | Request-Reply | High |
| INT-010 | Gift Card Issue/Redeem | POS → Oracle | Real-time (per txn) | Orchestration | High |
| INT-011 | Customer Enrollment | POS → Oracle | Real-time | Orchestration | Medium |
| INT-012 | Employee Time Clock | POS → Oracle | Real-time (per event) | Orchestration | Medium |
| INT-013 | Daily Z-Reading Summary | POS → Oracle | Daily (end of day) | Scheduled | High |
| INT-014 | Offline Batch Sync | POS → Oracle | Upon reconnection | Orchestration | Critical |
| INT-015 | Credit Customer Lookup | POS ↔ Oracle | Real-time | Request-Reply | Medium |
| INT-016 | Store Receiving Confirmation | POS → Oracle | Real-time | Orchestration | High |
| INT-017 | Stock Transfer Request | POS → Oracle | As needed | Orchestration | Medium |
| INT-018 | BIR Receipt Number Validation | POS → Oracle | Per transaction | Request-Reply | High |

---

## 8.3 Detailed Integration Specifications

### INT-001: POS Sales Transaction

**Purpose:** Send every completed sales transaction from POS to Oracle Fusion for financial recording, inventory decrement, and analytics.

**Source:** Custom POS Backend  
**Target:** Oracle AR (receipt/invoice), Oracle GL (journal via Accounting Hub), Oracle Inventory (decrement), Oracle CX Loyalty (points), Oracle Cost Management (COGS)

**Protocol:** HTTPS REST POST  
**OIC Adapter:** REST Adapter (inbound) → Oracle ERP Adapter (outbound)  
**Authentication:** OAuth 2.0 (client credentials)  
**Payload Format:** JSON  
**Timeout:** 30 seconds  
**Retry:** 3 retries with exponential backoff (5s, 15s, 45s)

**POS Request Payload (JSON):**

```json
{
  "transactionId": "POS-SL-00123-20260402-00001",
  "storeId": "STORE-001",
  "terminalId": "T-001",
  "cashierId": "EMP-20145",
  "transactionDateTime": "2026-04-02T14:30:25+08:00",
  "transactionType": "SALE",
  "birReceiptNumber": "SI-20260402-000001",
  "customer": {
    "customerId": null,
    "customerName": "WALK-IN",
    "loyaltyCardNumber": "TD-LOY-0045621",
    "tin": null
  },
  "lines": [
    {
      "lineNumber": 1,
      "itemSku": "ELEC-WS-00123",
      "itemName": "Philips LED Bulb 12W",
      "quantity": 5,
      "unitOfMeasure": "PCS",
      "unitPrice": 149.00,
      "grossAmount": 745.00,
      "discountAmount": 0.00,
      "netAmount": 745.00,
      "vatAmount": 89.40,
      "vatExclusiveAmount": 655.60,
      "unitCost": 98.50
    }
  ],
  "totals": {
    "totalGrossAmount": 745.00,
    "totalDiscountAmount": 0.00,
    "totalNetAmount": 745.00,
    "totalVatAmount": 89.40,
    "totalItemsCount": 5
  },
  "payments": [
    {
      "paymentMethod": "CASH",
      "amount": 800.00,
      "referenceNumber": null
    }
  ],
  "changeAmount": 55.00,
  "loyaltyPointsEarned": 14,
  "loyaltyPointsRedeemed": 0,
  "giftCardNumber": null,
  "promotionIds": [],
  "voidFlag": false
}
```

**OIC Transformation Logic:**

1. Parse POS transaction JSON.
2. Validate store ID and terminal ID against Oracle inventory organizations.
3. Create AR receipt in Oracle Receivables:
   - Customer: Map loyalty card → Oracle customer ID; or use walk-in generic customer.
   - Receipt method: Map POS payment method to Oracle receipt method.
   - Lines: Map POS lines to AR receipt lines with item, quantity, amount.
4. Trigger Accounting Hub:
   - Generate subledger journal with full CoA coding (Company-Region-CostCenter-Account-ProductCat-IC).
   - Post to GL.
5. Decrement inventory in Oracle Inventory Management:
   - Organization: Store inventory org matching storeId.
   - Subinventory: Sales Floor.
   - Items: Decrement quantities per line.
6. Calculate COGS:
   - COGS = sum of (unitCost × quantity) per line.
   - COGS journal posted to GL.
7. Process loyalty in Oracle CX:
   - If loyaltyCardNumber present: add earned points.
   - If pointsRedeemed > 0: deduct points and record redemption.
8. Return success response to POS with Oracle transaction reference.

**Success Response (HTTP 200):**

```json
{
  "status": "SUCCESS",
  "oracleReceiptNumber": "AR-RCPT-2026-00004567",
  "oracleJournalBatch": "JB-20260402-STORE-001-001",
  "loyaltyPointsBalance": 1456,
  "processedAt": "2026-04-02T14:30:26+08:00"
}
```

**Error Response (HTTP 4xx/5xx):**

```json
{
  "status": "ERROR",
  "errorCode": "ORA_ITEM_NOT_FOUND",
  "errorMessage": "Item SKU ELEC-WS-00123 not found in inventory org STORE-001",
  "transactionId": "POS-SL-00123-20260402-00001",
  "retryable": true
}
```

---

### INT-003: Price & Promotion Sync

**Purpose:** Push updated retail prices and promotions from Oracle Pricing to POS local cache.

**Source:** Oracle Order Management (Pricing)  
**Target:** Custom POS Backend  
**Direction:** Oracle → POS  
**Frequency:** Every 15 minutes (scheduled)  
**Protocol:** HTTPS REST POST from OIC to POS API

**Oracle → OIC Payload:**

```json
{
  "priceListId": "PL-RETAIL-2026",
  "effectiveDateTime": "2026-04-02T00:00:00+08:00",
  "prices": [
    {
      "itemSku": "ELEC-WS-00123",
      "unitPrice": 149.00,
      "currency": "PHP",
      "startDate": "2026-04-02",
      "endDate": null,
      "priceListType": "RETAIL"
    },
    {
      "itemSku": "PLMB-PVC-00456",
      "unitPrice": 85.00,
      "currency": "PHP",
      "startDate": "2026-04-01",
      "endDate": "2026-04-30",
      "priceListType": "PROMOTION",
      "promotionName": "April Plumbing Sale",
      "originalPrice": 120.00
    }
  ],
  "totalCount": 1523
}
```

---

### INT-004: Item Master Sync

**Purpose:** Push item master data (new items, updates, discontinuations) from Oracle PLM to POS.

**Source:** Oracle Product Lifecycle Management  
**Target:** Custom POS Backend  
**Frequency:** Every 30 minutes (scheduled)

**Payload:**

```json
{
  "items": [
    {
      "itemSku": "ELEC-WS-00123",
      "itemName": "Philips LED Bulb 12W Cool White",
      "itemDescription": "12W LED bulb, E27 base, 1055 lumens, 25000 hours",
      "department": "Electrical",
      "class": "Lighting",
      "subclass": "LED Bulbs",
      "barcode": "8718696174853",
      "unitOfMeasure": "PCS",
      "weight": 0.065,
      "weightUOM": "KG",
      "activeFlag": true,
      "lotControlFlag": false,
      "serialControlFlag": false,
      "shelfLifeDays": null,
      "hazardousFlag": false
    }
  ],
  "totalCount": 45
}
```

---

### INT-007: Loyalty Point Inquiry

**Purpose:** Real-time lookup of loyalty card points balance for display at POS.

**Source:** Custom POS → Oracle CX Loyalty  
**Pattern:** Request-Reply (synchronous)

**Request:**

```json
{
  "loyaltyCardNumber": "TD-LOY-0045621",
  "storeId": "STORE-001"
}
```

**Response:**

```json
{
  "loyaltyCardNumber": "TD-LOY-0045621",
  "customerName": "Juan Dela Cruz",
  "tier": "GOLD",
  "pointsBalance": 1442,
  "pointsValue": 1442.00,
  "multiplier": 1.5,
  "status": "ACTIVE"
}
```

---

## 8.4 Offline Mode Architecture

### 8.4.1 Offline Capabilities

When a POS terminal loses connectivity to OIC:

| Feature | Online | Offline |
|---------|--------|---------|
| Sales transaction processing | Full functionality | Full functionality (local cache) |
| Price lookup | Real-time from Oracle | Last synced price cache |
| Item lookup | Real-time from Oracle | Last synced item cache (~80K items) |
| Loyalty point inquiry | Real-time | Last known balance (with local floor limit) |
| Loyalty point earn/redeem | Real-time | Estimated; reconciled on reconnect |
| Gift card balance | Real-time | Last known balance (with floor limit) |
| Credit card processing | Via payment gateway | Via payment gateway (separate network) |
| Cash transactions | Normal | Normal |
| Inventory decrement | Real-time | Local only; synced on reconnect |
| Time clock | Real-time | Local; synced on reconnect |
| Receiving | Real-time | Local; synced on reconnect |

### 8.4.2 Sync Recovery Process

1. POS continuously monitors OIC connectivity (heartbeat every 30 seconds).
2. When connection restored, POS initiates batch sync of all queued transactions.
3. Transactions synced in chronological order with original timestamps.
4. OIC processes each transaction with conflict detection:
   - Inventory: Accept POS decrement; reconcile with any concurrent Oracle adjustments.
   - Pricing: Transaction uses price at time of sale (from local cache).
   - Loyalty: Points adjusted based on final reconciled transaction.
5. Sync completion confirmed to POS; POS clears local queue.
6. Reconciliation report generated for manual review of any discrepancies.

---

## 8.5 Error Handling and Monitoring

### 8.5.1 Error Categories

| Error Code | Description | Action |
|------------|-------------|--------|
| ERR_NETWORK | Network connectivity failure | Queue for offline sync |
| ERR_AUTH | Authentication failure | Re-authenticate; alert IT |
| ERR_VALIDATION | Data validation failure | Log error; alert store support |
| ERR_ORACLE_DOWN | Oracle Fusion unavailable | Queue for retry; escalate if > 30 min |
| ERR_ITEM_NOT_FOUND | SKU not in Oracle item master | Block transaction; alert merchandising |
| ERR_PRICE_MISMATCH | Price discrepancy > 5% | Flag for review; use Oracle price |
| ERR_INVENTORY_NEG | Would cause negative inventory | Allow with warning; flag for investigation |
| ERR_LOYALTY_FAIL | Loyalty system unavailable | Process without points; retroactively credit |

### 8.5.2 Monitoring Dashboards

| Metric | Target | Alert Threshold |
|--------|--------|-----------------|
| Integration availability (uptime) | 99.9% | < 99.5% |
| Transaction processing time (P95) | < 3 seconds | > 5 seconds |
| Daily sync failure rate | < 0.1% | > 0.5% |
| Offline mode activations per store/week | < 2 | > 5 |
| Queue depth (pending sync) | < 100 | > 500 |
| API rate limit hits per hour | 0 | > 10 |

---

## 8.6 Security Architecture

### 8.6.1 Authentication and Authorization

| Layer | Mechanism |
|-------|-----------|
| POS Terminal → POS Backend | mTLS (mutual TLS) with device certificates |
| POS Backend → OIC | OAuth 2.0 (client credentials grant) |
| OIC → Oracle Fusion | Oracle Cloud native authentication |
| API Gateway | API key + OAuth token validation |
| User authentication (POS) | Individual login (employee ID + PIN/biometric) |

### 8.6.2 Data Security

| Measure | Description |
|---------|-------------|
| Encryption in transit | TLS 1.3 for all API calls |
| Encryption at rest (POS local) | AES-256 encryption for offline cache |
| PII handling | Customer PII minimized at POS; full data in Oracle |
| PCI-DSS | Cardholder data handled by certified payment gateway; never stored in POS |
| Tokenization | Gift card and loyalty data tokenized |
| Audit logging | All integration calls logged with timestamp, user, payload hash |
| Data retention | POS local data purged after 90 days (post-sync confirmation) |

---

## 8.7 POS System Technical Specifications

### 8.7.1 Technology Stack

| Component | Technology |
|-----------|-----------|
| POS Frontend | React.js ( touchscreen-optimized UI ) |
| POS Backend | Java 21 + Spring Boot 3.x |
| Local Database | PostgreSQL (primary); SQLite (offline fallback per terminal) |
| Mobile Companion | React Native (for stock associates and supervisors) |
| Payment Integration | Payment gateway SDK (BDO, BPI, GCash, Maya) |
| Barcode Scanner | HID integration (USB/Bluetooth scanners) |
| Receipt Printer | ESC/POS protocol (thermal printers) |
| Cash Drawer | RS-232 trigger from receipt printer |
| Customer Display | Serial/USB secondary display |
| BIometric (time clock) | Integration with biometric device API |

### 8.7.2 POS Hardware Specification (Per Terminal)

| Component | Specification |
|-----------|--------------|
| Terminal | Intel NUC or equivalent (i5, 16GB RAM, 256GB SSD) |
| Touchscreen | 15.6" capacitive touchscreen (IP54 rated for retail) |
| Barcode Scanner | 2D imager (1D/2D barcode support) |
| Receipt Printer | Thermal 80mm, auto-cutter, ESC/POS |
| Cash Drawer | 4-bill 8-coin, RJ12 trigger |
| Customer Display | 9.7" LCD customer-facing display |
| Card Terminal | Separate POS terminal (PCI-certified) |
| UPS | 650VA UPS for power backup (15 min runtime) |
| Network | Ethernet (primary) + 4G LTE failover |

### 8.7.3 Terminal Deployment Estimate

| Location | Terminals | Purpose |
|----------|-----------|---------|
| 120 Stores × 4 terminals average | 480 | Sales checkout |
| 120 Stores × 1 receiving terminal | 120 | Receiving and inventory |
| 120 Stores × 1 supervisor terminal | 120 | Management, receiving, timekeeping |
| 4 Warehouses × 10 RF handhelds | 40 | Warehouse operations |
| **Total** | **760** | |

---

## 8.8 OIC Integration Design Patterns

### 8.8.1 Pattern: Real-Time Orchestration (INT-001, INT-002, INT-005)

```
POS → OIC REST Endpoint → OIC Orchestration Flow:
  ├── Step 1: Validate & Transform (Mapper)
  ├── Step 2: Fork (parallel)
  │   ├── Branch A: Create AR Receipt (ERP Adapter)
  │   ├── Branch B: Decrement Inventory (SCM Adapter)
  │   └── Branch C: Process Loyalty (CX Adapter)
  ├── Step 3: Accounting Hub Journal (ERP Adapter) [depends on Branch A]
  ├── Step 4: COGS Recognition (SCM/Cost Mgmt Adapter) [depends on Branch B]
  └── Step 5: Aggregate response → POS
```

### 8.8.2 Pattern: Scheduled Sync (INT-003, INT-004)

```
OIC Scheduled Flow (cron-based):
  ├── Step 1: Query Oracle Pricing/PLM for changes since last sync
  ├── Step 2: Transform to POS format
  ├── Step 3: Batch POST to POS Backend API
  ├── Step 4: POS acknowledges receipt
  └── Step 5: Log sync results; alert on failures
```

### 8.8.3 Pattern: Request-Reply (INT-007, INT-009, INT-015)

```
POS → OIC REST Endpoint → OIC Request-Reply Flow:
  ├── Step 1: Parse request
  ├── Step 2: Invoke Oracle CX/ERP synchronous API
  ├── Step 3: Transform response to POS format
  └── Step 4: Return to POS (within 3 seconds)
```

---

## 8.9 BIR Compliance Integration

### 8.9.1 Receipt Requirements

Every POS receipt must comply with BIR requirements:

| Field | Source | Oracle/Fusion |
|-------|--------|---------------|
| TIN of seller | Static (per store) | N/A (POS configuration) |
| Business name | Static (per store) | N/A (POS configuration) |
| Address | Static (per store) | N/A (POS configuration) |
| BIR Permit Number | Static (per store) | N/A (POS configuration) |
| Receipt number (sequential) | POS-generated (per terminal) | Cross-referenced in AR |
| Date and time | POS system clock | Validated in OIC |
| Item description | POS item cache (from Oracle PLM) | PLM → POS sync |
| Quantity and unit price | POS transaction | Validated against Oracle Pricing |
| Total amount | POS transaction | Validated in OIC |
| VAT amount | POS calculation (12%) | Validated against Oracle tax engine |
| Cashier name/ID | POS login | Mapped to Oracle HCM employee |

### 8.9.2 BIR-Required Reports

| Report | Frequency | Source |
|--------|-----------|--------|
| Sales journal (Sales Book) | Monthly | Oracle AR + POS data |
| Purchase journal (Purchase Book) | Monthly | Oracle AP |
| Monthly VAT return (BIR Form 2550M) | Monthly | Oracle Tax Reporting |
| Quarterly VAT return (BIR Form 2550Q) | Quarterly | Oracle Tax Reporting |
| Quarterly Income Tax Return (BIR Form 1701Q) | Quarterly | Oracle Tax Reporting |
| Annual Income Tax Return (BIR Form 1701/1702) | Annual | Oracle Tax Reporting |
| Annual Registration (BIR Form 0605) | Annual | Manual + Oracle data |
| List of suppliers (BIR Form 1604-E) | Annual | Oracle AP |
| List of employees (BIR Form 1604-C/W) | Annual | Oracle Payroll |
| Alphalist of payees | Annual | Oracle Payroll |
