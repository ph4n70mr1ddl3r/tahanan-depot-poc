# 24 — CUSTOMER SERVICE & AFTER-SALES OPERATIONS

## 24.1 Customer Service Organization

### 24.1.1 Customer Service Team Structure

```
VP Customer Experience (reports to COO, dotted line to CMO)
├── Director, Contact Center Operations
│   ├── Contact Center Manager
│   │   ├── Team Leads (4 — Phone, Email, Chat, Social)
│   │   ├── Customer Service Representatives — Phone (24)
│   │   ├── Customer Service Representatives — Email/Ticket (8)
│   │   ├── Customer Service Representatives — Chat (12)
│   │   └── Social Media Support Specialists (4)
│   ├── Quality Assurance Supervisor
│   │   └── QA Analysts (3)
│   └── Workforce Management Analyst
├── Director, After-Sales Services
│   ├── Warranty Manager
│   │   └── Warranty Claims Specialists (4)
│   ├── Installation Services Manager
│   │   ├── Service Coordinators (6)
│   │   └── Service Quality Inspector (2)
│   └── Field Service Dispatchers (6)
├── Manager, Customer Insights & Feedback
│   ├── Customer Insights Analysts (2)
│   └── NPS/CSAT Program Coordinator (1)
└── Manager, Store Customer Service
    ├── Store Customer Service Trainers (4 — regional)
    └── Service Recovery Specialists (4)
```

### 24.1.2 Oracle Fusion Security Roles

| Role | Oracle Fusion Security Roles |
|------|----------------------------|
| VP Customer Experience | ORA_CX_SERVICE_EXECUTIVE, ORA_CX_CDP_ADMIN, ORA_CX_LOYALTY_MANAGER |
| Director, Contact Center | ORA_CX_SERVICE_MANAGER, ORA_CX_KNOWLEDGE_MANAGER |
| Director, After-Sales | ORA_CX_FIELD_SERVICE_MANAGER, ORA_OM_MANAGER |
| Warranty Manager | ORA_CX_SERVICE_SPECIALIST, ORA_INV_TRANSACTION_USER |
| Installation Services Manager | ORA_CX_FIELD_SERVICE_DISPATCHER, ORA_OM_SPECIALIST |
| Customer Service Representatives | ORA_CX_SERVICE_AGENT, ORA_CX_DIGITAL_CUSTOMER_SERVICE_AGENT |
| Field Service Dispatchers | ORA_CX_FIELD_SERVICE_DISPATCHER |
| Manager, Customer Insights | ORA_CX_ANALYTICS_SPECIALIST, ORA_CX_CDP_SPECIALIST |

### 24.1.3 Contact Center Staffing Model

| Channel | Staffing (FTE) | Operating Hours | Shifts |
|---------|---------------|----------------|--------|
| Phone | 24 | 7:00 AM - 9:00 PM daily (14 hours) | 2 shifts × 12 agents |
| Email/Ticket | 8 | 7:00 AM - 7:00 PM daily (12 hours) | 2 shifts × 4 agents |
| Live Chat | 12 | 7:00 AM - 10:00 PM daily (15 hours) | 2 shifts × 6 agents |
| Social Media | 4 | 7:00 AM - 10:00 PM daily (15 hours) | 2 shifts × 2 agents |
| QA Analysts | 3 | 8:00 AM - 6:00 PM (Mon-Fri) | 1 shift |
| Team Leads | 4 | Staggered to cover operating hours | Per channel |
| Contact Center Manager | 1 | 8:00 AM - 6:00 PM (Mon-Fri) | 1 shift |
| **Total Contact Center** | **56** | | |

### 24.1.4 Customer Service Budget

| Category | Annual Budget (PHP) | Notes |
|----------|--------------------|-------|
| Contact center staffing (56 FTE) | 33,600,000 | Avg PHP 50K/month × 56 × 12 |
| Technology (Oracle CX Service, telephony, chatbot) | 15,000,000 | Annual licensing + telephony |
| Installation service contractor payments | 45,000,000 | ~15,000 installations/year × PHP 3,000 avg |
| Warranty claims and replacements | 25,000,000 | Reserve for warranty costs |
| Service recovery and compensation | 8,000,000 | Goodwill gestures, store credits |
| Training and development | 3,000,000 | Product knowledge, soft skills, systems |
| Quality monitoring tools | 2,000,000 | Call recording, analytics |
| Customer satisfaction surveys | 1,500,000 | Survey platform, incentives |
| Contingency | 4,900,000 | As needed |
| **Total Customer Service Budget** | **PHP 138,000,000** | |

---

## 24.2 Contact Center Operations

### 24.2.1 Multi-Channel Support Configuration

| Channel | Platform | Queue Type | Oracle Module |
|---------|----------|-----------|---------------|
| Phone | Cloud-based IVR (Oracle CX Service + telephony) | Skills-based routing | CX Service Center |
| Email | support@tahanandepot.com.ph | Auto-triage queue | CX Service Center |
| Live Chat | Oracle CX Digital Customer Service | Real-time queue | CX Digital Customer Service |
| SMS/Viber | Oracle CX Digital Customer Service + messaging API | Queue-based | CX Digital Customer Service |
| Social Media | Oracle CX Social Engagement | Unified queue | CX Service Center |
| Walk-in (stores) | POS Service Desk module | Store-level handling | POS + CX Service |
| Self-Service | tahanandepot.com.ph/help, FAQ, chatbot | Automated | CX Knowledge + Digital Assistant |

### 24.2.2 IVR Configuration

| Menu Level | Option | Routing |
|-----------|--------|---------|
| Level 1 | Press 1: Order inquiry and tracking | → Order Support queue |
| Level 1 | Press 2: Returns, refunds, and exchanges | → Returns queue |
| Level 1 | Press 3: Warranty and repair services | → After-Sales queue |
| Level 1 | Press 4: Product information and availability | → Product Support queue |
| Level 1 | Press 5: Installation and delivery scheduling | → Field Service queue |
| Level 1 | Press 6: Loyalty program (Tahanan Rewards) | → Loyalty Support queue |
| Level 1 | Press 7: B2B/Contractor accounts | → B2B Dedicated queue |
| Level 1 | Press 8: Other inquiries | → General queue |
| Level 1 | Press 0: Speak to an agent (any time) | → Next available agent |
| Level 2 | All options: enter 10-digit loyalty card number or order number for faster service | → Auto-populate in CX Service |

### 24.2.3 Ticket Lifecycle

| Stage | Activity | System | SLA |
|-------|----------|--------|-----|
| Create | Ticket created from any channel (phone, email, chat, social, walk-in, online) | CX Service | — |
| Triage | Auto-classified by topic; priority assigned by rules engine | CX Service | < 2 minutes (automated) |
| Assign | Routed to appropriate queue/skill group | CX Service | < 1 minute (automated) |
| Acknowledge | Agent reviews and acknowledges ticket; sets expectations | CX Service | Per channel SLA (section 24.3) |
| Investigate | Agent researches issue using CX Service, Oracle OM, AR, Inventory | CX Service + Oracle ERP | Per issue SLA (section 24.3) |
| Resolve | Solution provided; action taken (refund, replacement, escalation) | CX Service + applicable modules | Per issue SLA |
| Verify | Customer confirms resolution satisfactory (for phone/chat: real-time; email: survey) | CX Service | — |
| Close | Ticket closed with resolution code and notes | CX Service | — |
| Follow-up | Post-resolution survey sent; CSAT measured | CX Service | 24 hours after close |

### 24.2.4 Knowledge Base Management

| Content Type | Owner | Update Frequency | Oracle Module |
|-------------|-------|------------------|---------------|
| Product guides and manuals | Product Content Specialists (per Doc 23) | Per new item or revision | CX Knowledge Management |
| DIY tutorials and how-tos | Marketing (per Doc 17) | Weekly | CX Knowledge Management |
| FAQ (top 200 questions) | Customer Insights Manager | Monthly review | CX Knowledge Management |
| Return and refund procedures | Customer Service Manager | Quarterly or on policy change | CX Knowledge Management |
| Warranty policies by product | Warranty Manager | Quarterly or on policy change | CX Knowledge Management |
| Troubleshooting guides (by category) | After-Sales Specialists | Quarterly | CX Knowledge Management |
| Store-specific information | Store Customer Service Trainers | On change | CX Knowledge Management |
| Pricing and promotion FAQs | Merchandising (per Doc 25) | Per promo calendar | CX Knowledge Management |

### 24.2.5 Escalation Matrix

| Tier | Role | Handles | Escalation Trigger |
|------|------|---------|-------------------|
| Tier 0 | Chatbot (AI) / Self-Service | FAQ, order status, basic product info | Customer requests live agent or issue unresolved after 2 attempts |
| Tier 1 | Customer Service Representative | General inquiries, basic complaints, order tracking, return initiation, product info | Complex issue requiring supervisor or specialized knowledge |
| Tier 2 | Senior CS Representative / Team Lead | Complex complaints, multi-channel issues, payment disputes, high-value returns | Policy exception required, legal/compliance issue, PR risk |
| Tier 3 | Customer Service Manager / Director | Policy exceptions, VIP/B2B escalations, safety/recall issues, media/social media crisis | Requires VP/C-suite decision or cross-department coordination |
| Tier 4 | VP Customer Experience / COO | Critical incidents, systemic failures, major service failures, legal matters | Board/CEO escalation or regulatory action |

### 24.2.6 Quality Assurance

| QA Activity | Frequency | Sample Size | Scoring Criteria |
|-------------|-----------|-------------|------------------|
| Call monitoring | Monthly | 4 calls per agent per month | 20-point scorecard (greeting, verification, resolution, empathy, professionalism, closure) |
| Email/ticket review | Monthly | 6 tickets per agent per month | 15-point scorecard (acknowledgment, accuracy, completeness, tone, response time) |
| Chat review | Monthly | 6 chats per agent per month | 15-point scorecard (response time, accuracy, efficiency, tone, resolution) |
| Social media review | Weekly | All social interactions | Response time, brand voice, resolution accuracy |
| Silent monitoring (live) | Weekly | Random | Real-time coaching opportunity |
| Calibration sessions | Monthly | All QA analysts + Team Leads | Align scoring standards |
| Target QA score | ≥ 85/100 | | Agent performance review trigger at < 75 |

---

## 24.3 Service Level Agreements

### 24.3.1 SLA Targets by Channel

| Channel | Metric | Target | Measurement |
|---------|--------|--------|-------------|
| Phone | Answer rate | ≥ 90% within 60 seconds | Automated (telephony) |
| Phone | Abandonment rate | < 5% | Automated (telephony) |
| Phone | First-call resolution | ≥ 75% | QA analysis |
| Email | First response time | < 4 hours (during operating hours) | CX Service SLA timer |
| Email | Resolution time | < 24 hours | CX Service SLA timer |
| Live Chat | Initial response | < 30 seconds | CX Digital CS analytics |
| Live Chat | Resolution time | < 10 minutes (avg) | CX Digital CS analytics |
| Social Media | First response | < 1 hour | Social analytics |
| Social Media | Resolution time | < 4 hours | Social analytics |
| SMS/Viber | First response | < 30 minutes | CX Digital CS analytics |
| Self-service (chatbot) | Containment rate | ≥ 60% | Chatbot analytics |
| Walk-in (store) | Wait time | < 5 minutes | Store ops (per Doc 14) |

### 24.3.2 SLA Targets by Issue Type

| Issue Type | Target Resolution Time | Oracle Module |
|-----------|----------------------|---------------|
| Order inquiry/tracking | < 5 minutes | OM + CX Service |
| Product availability check | < 5 minutes | Inventory + CX Service |
| Return initiation | < 15 minutes | CX Service + OM |
| Refund processing (standard) | 3-5 business days | AR + Payment Gateway |
| Refund processing (expedited) | 24 hours (for VIP/Platinum) | AR + Payment Gateway |
| Complaint (general) | < 24 hours | CX Service |
| Complaint (product quality) | < 48 hours | CX Service + PLM Quality |
| Complaint (service/delivery) | < 24 hours | CX Service + TMS |
| Warranty claim | 5-7 business days | CX Service + OM |
| Installation scheduling | < 24 hours to confirm schedule | CX Field Service |
| Loyalty program inquiry | < 5 minutes | CX Loyalty |
| Payment dispute | 5-7 business days | AR + Payment Gateway |
| Recall notification | < 4 hours (for affected customers) | CX Service + PLM Quality |
| B2B/Contractor inquiry | < 2 hours | CX Service + AR |

### 24.3.3 SLA Monitoring and Reporting

| Report | Frequency | Audience | Content |
|--------|-----------|----------|---------|
| Daily SLA dashboard | Daily (automated) | Team Leads, Contact Center Manager | Channel SLA performance, queue depth, wait times |
| Weekly SLA summary | Weekly | Director Contact Center, VP CX | SLA compliance %, trending issues, capacity |
| Monthly SLA report | Monthly | VP CX, COO, CMO | Full SLA performance, root cause for breaches, improvement actions |
| Quarterly business review | Quarterly | C-suite, Board (summary) | CS performance, NPS, cost per contact, strategic initiatives |

### 24.3.4 SLA Breach Protocols

| Breach Level | Condition | Action |
|-------------|-----------|--------|
| Level 1 (Minor) | Single SLA breach on one channel | Auto-alert to agent + Team Lead; agent self-corrects |
| Level 2 (Moderate) | SLA < 90% for one channel for one week | Team Lead root cause analysis; corrective action plan within 48 hours |
| Level 3 (Major) | SLA < 80% for one channel for one week | Manager review; staffing adjustment; process fix; escalation to Director |
| Level 4 (Critical) | SLA < 70% across multiple channels | VP CX review; emergency staffing; system investigation; executive briefing |

---

## 24.4 Customer Feedback and Satisfaction

### 24.4.1 NPS Program

| Element | Configuration |
|---------|--------------|
| Survey question | "On a scale of 0-10, how likely are you to recommend Tahanan Depot to a friend or colleague?" |
| Follow-up question | "What is the primary reason for your score?" |
| Survey triggers | (1) Post-purchase (in-store: 24 hours; online: 48 hours), (2) Post-service interaction, (3) Post-delivery, (4) Post-installation |
| Survey method | Email (primary), SMS (for phone customers), in-app (for mobile app users) |
| NPS calculation | % Promoters (9-10) minus % Detractors (0-6) |
| Target NPS | ≥ 50 (overall), ≥ 45 (online), ≥ 55 (in-store), ≥ 40 (post-complaint) |
| Reporting frequency | Monthly (team level), quarterly (company level) |
| Oracle module | CX Service + CX CDP + CX Marketing (survey automation) |

### 24.4.2 CSAT Measurement

| Touchpoint | Survey Question | Scale | Target | Frequency |
|-----------|----------------|-------|--------|-----------|
| Post-phone call | "How satisfied were you with today's call?" | 1-5 stars | ≥ 4.2 | Every call (IVR post-call) |
| Post-chat | "How would you rate this chat session?" | 1-5 stars | ≥ 4.3 | Every chat (auto-popup) |
| Post-email resolution | "How satisfied were you with our email response?" | 1-5 stars | ≥ 4.0 | Every email resolution |
| Post-purchase (in-store) | "How was your shopping experience today?" | 1-5 stars | ≥ 4.4 | Sampled (20% of transactions) |
| Post-purchase (online) | "How was your online shopping experience?" | 1-5 stars | ≥ 4.2 | Every online order |
| Post-delivery | "How was your delivery experience?" | 1-5 stars | ≥ 4.0 | Every delivery |
| Post-installation | "How was your installation/service experience?" | 1-5 stars | ≥ 4.3 | Every installation |
| Post-complaint resolution | "Was your issue resolved to your satisfaction?" | Yes/No | ≥ 80% Yes | Every complaint |

### 24.4.3 Customer Effort Score (CES)

| Touchpoint | Survey Question | Scale | Target |
|-----------|----------------|-------|--------|
| Post-return/refund | "How easy was it to process your return?" | 1-7 (strongly disagree to strongly agree) | ≥ 5.5 |
| Post-warranty claim | "How easy was it to file your warranty claim?" | 1-7 | ≥ 5.0 |
| Post-service appointment | "How easy was it to schedule your service?" | 1-7 | ≥ 5.5 |
| Post-online-order issue | "How easy was it to get help with your order?" | 1-7 | ≥ 5.0 |

### 24.4.4 Complaint Management Process

| Step | Activity | Responsible | System | SLA |
|------|----------|-------------|--------|-----|
| 1 | Complaint received (any channel) | CS Representative | CX Service | — |
| 2 | Complaint logged with unique reference number | CS Representative | CX Service | Immediate |
| 3 | Complaint classified: type, severity, department | CS Representative (auto-assisted) | CX Service | < 2 minutes |
| 4 | Severity assigned (Critical/High/Medium/Low) | System + CS Representative | CX Service | < 2 minutes |
| 5 | Complaint acknowledged to customer | CS Representative | CX Service | Per channel SLA |
| 6 | Investigation initiated; relevant department notified | CS Representative | CX Service + cross-module | < 4 hours |
| 7 | Root cause identified | Assigned investigator | Cross-functional | Per severity |
| 8 | Resolution proposed | CS Representative + Department | CX Service | Per severity |
| 9 | Resolution communicated to customer | CS Representative | CX Service (email/phone/chat) | Per SLA |
| 10 | Customer acceptance/rejection of resolution | Customer | CX Service | — |
| 11 | If accepted: ticket closed; if rejected: re-escalate | Team Lead | CX Service | — |
| 12 | Post-resolution survey sent | System (automated) | CX Service | 24 hours |
| 13 | Complaint data analyzed for trending issues | Customer Insights Analyst | CX Analytics | Monthly |

### 24.4.5 Complaint Severity Levels

| Severity | Definition | Examples | Target Resolution | Escalation |
|----------|-----------|---------|-------------------|------------|
| Critical | Safety risk, legal exposure, media/PR risk, affects multiple customers | Product safety hazard, data breach, viral social media complaint | < 4 hours | VP CX + COO + Legal + PR |
| High | Financial impact > PHP 10,000, affects loyalty customer (Platinum/Gold), repeated issue (3rd+ complaint) | High-value B2B dispute, warranty replacement > PHP 50K, appliance fire risk | < 8 hours | Director CX + relevant VP |
| Medium | Standard complaint, financial impact < PHP 10,000, first-time complaint | Late delivery, damaged product, rude staff, pricing dispute | < 24 hours | Team Lead |
| Low | Minor issue, suggestion, general feedback | Long queue, product suggestion, store cleanliness, signage | < 48 hours | CS Representative |

### 24.4.6 Social Media Sentiment Monitoring

| Platform | Monitoring Tool | Frequency | Alert Threshold |
|----------|----------------|-----------|----------------|
| Facebook | Oracle CX Social Engagement + Meta Business Suite | Real-time | Negative mention from account > 1,000 followers |
| Instagram | Oracle CX Social Engagement | Real-time | Negative mention with brand hashtag |
| X (Twitter) | Oracle CX Social Engagement | Real-time | Any negative mention with @TahananDepot |
| TikTok | Manual + social listening tool | Hourly (during business hours) | Viral negative video (> 1,000 views) |
| Google Reviews | Google Business Profile + CX Service | Daily | Review < 3 stars |
| YouTube | Manual monitoring | Daily | Negative video comment thread |

---

## 24.5 Warranty Administration

### 24.5.1 Warranty Periods by Product Category

| Product Category | Standard Warranty | Extended Warranty (Optional, Sold) | Warranty Provider |
|-----------------|-------------------|------------------------------------|-------------------|
| Major appliances (AC, refrigerator, washing machine) | 1 year (parts & labor) | Up to 5 years (Tahanan Protect) | Manufacturer + Tahanan |
| Small appliances | 6 months - 1 year | Up to 3 years (Tahanan Protect) | Manufacturer |
| Power tools | 6 months - 2 years (varies by brand) | Up to 3 years (Tahanan Protect) | Manufacturer |
| Hand tools | Lifetime warranty (Tahanan Essentials brand) | N/A | Tahanan |
| Paint and coatings | Per manufacturer defect warranty | N/A | Manufacturer |
| Electrical supplies | 1 year (wiring, breakers) | N/A | Manufacturer |
| Plumbing fixtures | 1-5 years (varies by brand) | N/A | Manufacturer |
| Flooring and tiles | 1 year (installation defects) | N/A | Tahanan (for installed) |
| Kitchen cabinets | 5 years (structural) | N/A | Manufacturer |
| Lighting fixtures | 1 year | N/A | Manufacturer |
| Cement and building materials | Per manufacturer standards | N/A | Manufacturer |
| Garden equipment | 6 months - 1 year | N/A | Manufacturer |

### 24.5.2 Warranty Claim Process

| Step | Activity | Responsible | System | SLA |
|------|----------|-------------|--------|-----|
| 1 | Customer contacts service (any channel) with warranty claim | Customer | CX Service | — |
| 2 | Agent verifies purchase (receipt/order number, date, product) | CS Representative | CX Service + POS/OM | < 5 minutes |
| 3 | Agent confirms warranty eligibility (within period, covered issue) | CS Representative | CX Service + CX Knowledge | < 5 minutes |
| 4 | Warranty ticket created with product details, issue description, photos | CS Representative | CX Service | < 10 minutes |
| 5 | Ticket routed: in-store repair → store; pick-up service → Field Service; replace → OM | System (automated) | CX Service | < 2 minutes |
| 6 | For repair: technician scheduled (Field Service dispatch) | Service Coordinator | CX Field Service | < 24 hours to schedule |
| 7 | For replacement: replacement order created in OM | Warranty Specialist | Order Management | < 24 hours |
| 8 | Technician performs service/repair or replacement shipped | Technician / Warehouse | Field Service / TMS | 5-7 business days |
| 9 | Service/repair completed; customer signs off | Technician | CX Field Service | — |
| 10 | Warranty ticket closed; quality data recorded | Warranty Specialist | CX Service + PLM Quality | Same day |
| 11 | Post-warranty service survey sent | System (automated) | CX Service | 24 hours |

### 24.5.3 Repair vs. Replace Decision Matrix

| Condition | Decision | Criteria |
|-----------|----------|----------|
| Product < 30 days old, manufacturing defect | Replace with new unit | Per RA 7394 Consumer Act: mandatory replacement for latent defects |
| Product < 1 year old, repairable defect | Repair at no cost to customer | Repair cost < 50% of product value |
| Product < 1 year old, non-repairable defect | Replace with same or equivalent unit | Repair cost ≥ 50% of product value or no parts available |
| Product > 1 year old, extended warranty active | Repair or replace per extended warranty terms | Per Tahanan Protect contract |
| Product damage due to customer misuse | Not covered; offer paid repair | Assessed by technician; customer informed of cost before repair |
| Product recalled (per Doc 21) | Replace or refund per recall directive | Immediate action regardless of warranty status |

### 24.5.4 Extended Warranty (Tahanan Protect)

| Plan | Coverage | Price (% of Product Price) | Sold By |
|------|----------|---------------------------|---------|
| Tahanan Protect Silver | 2 years total (1 year standard + 1 year extended); parts & labor | 5-8% | POS (in-store) and CX Commerce (online) |
| Tahanan Protect Gold | 3 years total; parts & labor; annual preventive maintenance | 10-12% | POS and CX Commerce |
| Tahanan Protect Platinum | 5 years total; parts & labor; annual PM; loaner unit during repair | 15-18% | POS and CX Commerce |

### 24.5.5 Supplier Warranty Recovery

| Step | Activity | Responsible | Oracle Module |
|------|----------|-------------|---------------|
| 1 | Warranty claim costs tracked per supplier | Warranty Manager | PLM Quality + AR |
| 2 | Monthly warranty claim report generated by supplier | Warranty Specialist | PLM Quality |
| 3 | Debit memo created for supplier warranty recovery | AP Specialist | Payables |
| 4 | Supplier notified of warranty recovery claim | Warranty Manager | Supplier Portal |
| 5 | Recovery tracked in supplier scorecard (per Doc 05, POL-SCM-002) | Procurement | Supplier Management |
| 6 | Quarterly warranty recovery reconciliation | Warranty Manager + Finance | Payables + GL |

---

## 24.6 Installation and Delivery Services

### 24.6.1 Installation Service Catalog

| Service | Category | Standard Price (PHP) | Estimated Duration | Service Partner |
|---------|----------|--------------------|--------------------|----------------|
| Aircon installation (wall-mounted, up to 2HP) | Appliances | 2,500 - 4,500 | 2-3 hours | Authorized AC brand technicians |
| Aircon installation (cassette/duct type) | Appliances | 8,000 - 15,000 | 4-6 hours | Authorized AC brand technicians |
| Water heater installation (tankless) | Plumbing | 1,500 - 2,500 | 1-2 hours | Licensed plumber |
| Water heater installation (tank type) | Plumbing | 2,500 - 4,000 | 2-3 hours | Licensed plumber |
| Kitchen cabinet installation | Kitchen & Bath | 5,000 - 20,000 | 1-3 days | Tahanan certified installer |
| Countertop installation | Kitchen & Bath | 3,000 - 8,000 | 1-2 days | Tahanan certified installer |
| Flooring installation (tiles) | Flooring & Tiles | 150 - 250 per sqm | 1-5 days | Tahanan certified installer |
| Flooring installation (vinyl/laminate) | Flooring & Tiles | 120 - 200 per sqm | 1-3 days | Tahanan certified installer |
| Ceiling fan installation | Electrical | 800 - 1,500 | 1-2 hours | Licensed electrician |
| Lighting fixture installation (chandelier) | Electrical | 1,500 - 3,000 | 2-3 hours | Licensed electrician |
| Toilet and bidet installation | Plumbing | 1,500 - 3,000 | 2-3 hours | Licensed plumber |
| Door installation | Doors & Windows | 2,000 - 5,000 | 2-4 hours | Tahanan certified installer |
| Window installation | Doors & Windows | 3,000 - 8,000 | 3-6 hours | Tahanan certified installer |
| Built-in appliance installation | Appliances | 2,000 - 5,000 | 2-4 hours | Authorized technician |

### 24.6.2 Installation Service Workflow

| Step | Activity | System | Oracle Module |
|------|----------|--------|---------------|
| 1 | Customer purchases product + installation service (POS or online) | POS / CX Commerce | POS / CX Commerce |
| 2 | Installation order created in Oracle Order Management | OM | Order Management |
| 3 | Service order created in Oracle CX Field Service | CX Field Service | Field Service |
| 4 | Service Coordinator reviews requirements (tools, parts, skills needed) | CX Field Service | Field Service |
| 5 | Service Coordinator schedules appointment with customer (phone/email) | CX Field Service | Field Service |
| 6 | Technician assigned based on skills, location, availability | CX Field Service (auto-suggest) | Field Service |
| 7 | Customer confirmation sent (email + SMS with date, time window, technician name) | CX Field Service | Field Service |
| 8 | Day-before reminder sent to customer | System (automated) | CX Field Service |
| 9 | Technician arrives; performs installation per quality standards | Technician | CX Field Service (mobile app) |
| 10 | Customer walkthrough and sign-off on completion | Technician + Customer | CX Field Service (mobile app) |
| 11 | Before/after photos uploaded to service record | Technician | CX Field Service (mobile app) |
| 12 | Service order closed; revenue recognized | OM + Revenue Management | Order Management + Revenue Management |
| 13 | Post-installation survey sent | System (automated) | CX Service |
| 14 | Warranty for installation work starts (1 year labor warranty) | CX Service | CX Service |

### 24.6.3 Service Contractor Management

| Criteria | Requirement | Verification |
|----------|-------------|-------------|
| Business registration | DTI/SEC registered; BIR-registered | Copy of registration on file |
| Technical certification | TESDA NC-II or higher in relevant trade; PRC license for engineers | Copy of certification on file |
| Insurance | Comprehensive general liability; min PHP 1M coverage | Certificate of insurance renewed annually |
| Background check | NBI clearance; barangay clearance | On file; renewed annually |
| Training completion | Tahanan Depot service standards training (8 hours) | Certificate of completion |
| Performance metrics | Min 4.0/5.0 CSAT; < 2% callback rate; on-time ≥ 90% | Monthly review |
| Tools and equipment | Own basic tools; company provides specialty tools as needed | Checklist at onboarding |

### 24.6.4 Service Contractor Performance Scorecard

| Metric | Target | Weight | Data Source |
|--------|--------|--------|-------------|
| Customer satisfaction (post-install survey) | ≥ 4.3 / 5.0 | 30% | CX Service survey |
| On-time arrival | ≥ 90% | 20% | CX Field Service mobile app |
| First-time fix rate | ≥ 95% | 20% | CX Field Service |
| Callback/rework rate | < 2% | 15% | CX Field Service |
| Safety incidents | 0 | 10% | HCM Workforce Health & Safety |
| Compliance (training, documentation) | 100% | 5% | CX Field Service admin |

### 24.6.5 Revenue Recognition for Installation Services

| Element | Treatment | Oracle Module |
|---------|-----------|---------------|
| Product + installation bundle | Two performance obligations: (1) product, (2) installation service; allocated per relative standalone selling price | Revenue Management |
| Standalone installation | Single performance obligation; recognized upon completion and customer acceptance | Revenue Management |
| Deposit/prepayment | Deferred revenue until service completed | AR + Revenue Management |
| Cancellation (customer-initiated) | Refund per cancellation policy; service fee of PHP 500 if cancelled < 24 hours before appointment | AR |

---

## 24.7 After-Sales Product Support

### 24.7.1 Product Support by Category

| Category | Support Type | Resources | Referral Network |
|----------|-------------|-----------|-----------------|
| Appliances (major) | Troubleshooting, warranty, repair, parts | Troubleshooting guides (CX Knowledge), brand hotlines | Authorized service centers (Samsung, LG, Panasonic, etc.) |
| Power tools | Troubleshooting, warranty, repair, parts, blade/bit replacement | Troubleshooting guides, brand hotlines | Authorized service centers (Makita, Bosch, DeWalt, etc.) |
| Electrical | Safety guidance, compatibility, installation advice | CX Knowledge guides, licensed electrician referral | Licensed electrician network |
| Plumbing | Troubleshooting, compatibility, parts identification | CX Knowledge guides, licensed plumber referral | Licensed plumber network |
| Paint and decorating | Color matching, product selection, application advice | CX Knowledge guides, in-store paint counter | Professional painter referral |
| Flooring and tiles | Installation guidance, material calculator, grout/adhesive selection | Online calculator, CX Knowledge guides | Certified installer network |
| Garden and outdoor | Plant care guidance, product warranty, seasonal advice | CX Knowledge guides, garden center staff | N/A |

### 24.7.2 Product Registration Program

| Element | Details |
|---------|---------|
| Registration method | Online (tahanandepot.com.ph/register), in-store (QR code on receipt), email, SMS |
| Products requiring registration | Appliances (all), power tools (≥ PHP 5,000), kitchen cabinets, water heaters |
| Data collected | Product, serial number, purchase date, store, customer name, contact, installation address |
| Benefits to customer | Extended warranty activation, recall notifications, service reminders, loyalty bonus points (50 points) |
| Oracle integration | Registration data stored in CX CDP; linked to purchase record in AR/OM |
| Recall matching | Automatic notification to registered customers if product recalled (per Doc 21) |

### 24.7.3 Parts and Accessories Ordering

| Step | Activity | System |
|------|----------|--------|
| 1 | Customer requests part/accessory (phone, chat, in-store) | CX Service / POS |
| 2 | Agent searches parts catalog in Oracle PLM | PLM + CX Knowledge |
| 3 | Part identified and availability checked (Oracle Inventory) | Inventory Management |
| 4 | If in-stock: order created in OM for pick-up or delivery | Order Management |
| 5 | If not in-stock: special order created; supplier lead time communicated | OM + Purchasing |
| 6 | Customer notified when part arrives | OM + CX Commerce |
| 7 | Parts revenue tracked per product category | AR + GL |

---

## 24.8 Customer Retention Programs

### 24.8.1 At-Risk Customer Identification

| Signal | Data Source | Trigger | Action |
|--------|-----------|---------|--------|
| Complaint (> 1 in 30 days) | CX Service | Auto-flag in CX CDP | Service recovery outreach within 24 hours |
| Return rate > 3 items in 60 days | OM + POS | Auto-flag | Personal follow-up by store or CS |
| Loyalty tier downgrade risk | CX Loyalty | Projected spend < tier threshold (90-day lookahead) | Targeted offer via marketing automation |
| No purchase in 90+ days (previously active) | CX CDP | Auto-flag | Win-back campaign (email + SMS) |
| Negative NPS/CSAT response | CX Service | Detractor score | Personal follow-up within 48 hours |
| Social media negative mention | CX Social Engagement | Flagged post | Social media response + outreach |
| Abandoned cart (online, > 3 in 30 days) | CX Commerce | Auto-flag | Cart recovery email + incentive |

### 24.8.2 Win-Back Campaigns

| Campaign | Target Segment | Offer | Channel | Frequency |
|----------|---------------|-------|---------|-----------|
| Dormant 90 days | No purchase 90-180 days | 10% discount coupon (max PHP 500) | Email + SMS | Triggered (auto) |
| Dormant 180 days | No purchase 180-365 days | 15% discount + 2x loyalty points | Email + SMS + Direct mail | Triggered (auto) |
| Dormant 365+ days | No purchase > 1 year | PHP 500 gift card on next purchase ≥ PHP 3,000 | Email + SMS + Direct mail | Quarterly batch |
| Complaint recovery | Customers with recent complaint (resolved) | 500 bonus loyalty points + personal apology | Email from VP CX | Per incident |
| Lapsed B2B | B2B account no orders in 60 days | Dedicated account manager outreach + exclusive pricing | Phone + Email | Triggered (auto) |

### 24.8.3 VIP/Platinum Customer Service

| Benefit | Platinum Tier | Gold Tier |
|---------|--------------|-----------|
| Dedicated phone line | Yes (priority routing) | No (standard queue) |
| Priority service scheduling | Same-day or next-day | 2-day priority |
| Extended return window | 60 days | 45 days |
| Free installation (qualifying purchases) | Purchases ≥ PHP 50,000 | Purchases ≥ PHP 100,000 |
| Priority delivery | Free same-day (Metro Manila) | Free next-day (Metro Manila) |
| Annual home maintenance check | Yes (complimentary) | No |
| Personal shopper/assistant | Available on request | No |
| Exclusive events | Quarterly VIP events | Annual event |

---

## 24.9 Customer Service SOPs

### SOP-CS-001: Customer Complaint Handling

| Step | Activity | Responsible | System |
|------|----------|-------------|--------|
| 1 | Receive complaint via any channel | CS Representative | CX Service |
| 2 | Listen actively; empathize; do not interrupt | CS Representative | — |
| 3 | Verify customer identity (name + loyalty number or order number) | CS Representative | CX Service + CX CDP |
| 4 | Log complaint with full details in CX Service ticket | CS Representative | CX Service |
| 5 | Classify severity (Critical/High/Medium/Low) per section 24.4.5 | CS Representative | CX Service |
| 6 | If resolvable at Tier 1: resolve immediately; if not, escalate | CS Representative | CX Service |
| 7 | Provide resolution or expected timeline to customer | CS Representative | CX Service |
| 8 | For Critical/High: notify Team Lead and escalate per matrix | CS Representative / Team Lead | CX Service |
| 9 | Follow up with customer within committed timeline | CS Representative | CX Service |
| 10 | Close ticket; send satisfaction survey | CS Representative / System | CX Service |

### SOP-CS-002: Warranty Claim Processing

| Step | Activity | Responsible | System |
|------|----------|-------------|--------|
| 1 | Customer contacts service with warranty issue | Customer | CX Service (any channel) |
| 2 | Verify purchase: receipt/order number, purchase date, product details | CS Representative | CX Service + POS/OM |
| 3 | Check warranty eligibility: within warranty period, covered defect | CS Representative | CX Knowledge + CX Service |
| 4 | Create warranty ticket; request photos of defect (if applicable) | CS Representative | CX Service |
| 5 | Determine resolution: repair, replace, or refund (per decision matrix, section 24.5.3) | Warranty Specialist | CX Service |
| 6 | If repair: schedule Field Service technician (per section 24.6.2) | Service Coordinator | CX Field Service |
| 7 | If replace: create replacement order in OM | Warranty Specialist | Order Management |
| 8 | Execute resolution; track to completion | Warranty Specialist | CX Service + OM / Field Service |
| 9 | Confirm customer satisfaction; close warranty ticket | Warranty Specialist | CX Service |
| 10 | Record warranty data in PLM Quality for supplier tracking | Warranty Specialist | PLM Quality |

### SOP-CS-003: Installation Service Scheduling

| Step | Activity | Responsible | System |
|------|----------|-------------|--------|
| 1 | Installation order received from POS or e-commerce (per section 24.6.2) | System | OM → CX Field Service |
| 2 | Service Coordinator reviews order: product, location, special requirements | Service Coordinator | CX Field Service |
| 3 | Contact customer to confirm preferred schedule (date, time window) | Service Coordinator | CX Field Service |
| 4 | Assign qualified technician based on skills and location | Service Coordinator | CX Field Service (auto-suggest) |
| 5 | Send confirmation to customer (email + SMS) | System | CX Field Service |
| 6 | Send day-before reminder to customer | System | CX Field Service |
| 7 | Send job details to technician (mobile app: address, product, special notes) | System | CX Field Service (mobile) |
| 8 | If reschedule requested by customer: reschedule and reassign | Service Coordinator | CX Field Service |
| 9 | If technician no-show: dispatch backup technician within 2 hours; PHP 500 credit to customer | Service Coordinator | CX Field Service |
| 10 | Post-installation: verify customer sign-off; close service order | Technician | CX Field Service (mobile) |

### SOP-CS-004: Product Return Assistance

| Step | Activity | Responsible | System |
|------|----------|-------------|--------|
| 1 | Customer contacts service requesting return | Customer | CX Service (any channel) |
| 2 | Verify purchase details and return eligibility per POL-RET-001 | CS Representative | CX Service + POS/OM |
| 3 | Guide customer on return method: in-store drop-off or courier pick-up | CS Representative | CX Service |
| 4 | For in-store: provide QR code and return instructions | CS Representative | CX Commerce / CX Service |
| 5 | For courier pick-up: generate return label; schedule pick-up | CS Representative | CX Commerce + 3PL |
| 6 | Track return shipment status | CS Representative | CX Service + OM |
| 7 | Upon receipt: confirm quality inspection passed | Store QA / DC QA | Inventory Management |
| 8 | Initiate refund to original payment method | CS Representative | AR |
| 9 | Confirm refund timeline to customer | CS Representative | CX Service |
| 10 | Close ticket; trigger satisfaction survey | System | CX Service |

### SOP-CS-005: Delivery Inquiry and Tracking

| Step | Activity | Responsible | System |
|------|----------|-------------|--------|
| 1 | Customer contacts service asking about delivery status | Customer | CX Service |
| 2 | Agent retrieves order using order number or customer details | CS Representative | CX Service + OM |
| 3 | Check order status in OM and TMS | CS Representative | OM + TMS |
| 4 | Provide real-time status: processing, shipped, in-transit, out-for-delivery | CS Representative | OM + TMS |
| 5 | If delayed: investigate cause; provide updated ETA; apologize | CS Representative | OM + TMS |
| 6 | If customer wants to reschedule: coordinate with TMS and dispatch | CS Representative | TMS + CX Service |
| 7 | If delivery failed: arrange redelivery within 48 hours at no cost | CS Representative | TMS + OM |
| 8 | For scheduled/bulky delivery: confirm date and time window with customer | Service Coordinator | CX Field Service + TMS |
| 9 | Log inquiry; close ticket | CS Representative | CX Service |

### SOP-CS-006: Escalation Management

| Step | Activity | Responsible | System |
|------|----------|-------------|--------|
| 1 | Agent identifies need for escalation (per tier matrix, section 24.2.5) | CS Representative | CX Service |
| 2 | Complete all required fields in ticket: issue summary, steps taken, customer expectation | CS Representative | CX Service |
| 3 | Set escalation level and target resolution time | CS Representative | CX Service |
| 4 | Warm transfer to Tier 2/3 (phone) or reassign ticket (email/chat) | CS Representative | CX Service |
| 5 | Tier 2/3 agent reviews case and takes ownership | Senior CS / Manager | CX Service |
| 6 | If policy exception needed: obtain approval per authority matrix | Manager / Director | CX Service |
| 7 | If cross-department: coordinate with relevant department (Merchandising, Supply Chain, Store Ops) | Manager / Director | CX Service + cross-module |
| 8 | Resolution communicated to customer by Tier 2/3 agent | Senior CS / Manager | CX Service |
| 9 | If unresolved at Tier 3: escalate to VP CX with full case brief | Director | CX Service |
| 10 | Post-escalation review: root cause analysis; process improvement if needed | Manager | CX Service |

### SOP-CS-007: Customer Feedback Collection

| Step | Activity | Responsible | System |
|------|----------|-------------|--------|
| 1 | Survey triggered automatically per touchpoint rules (section 24.4.1-24.4.3) | System | CX Service + CX Marketing |
| 2 | Survey responses collected and stored in CX CDP | System | CX CDP |
| 3 | Negative responses (NPS Detractor, CSAT < 3) flagged for immediate follow-up | System (automated) | CX Service |
| 4 | Follow-up outreach within 24-48 hours by CS team | CS Representative | CX Service |
| 5 | Monthly aggregation of feedback data | Customer Insights Analyst | CX Analytics + FDI |
| 6 | Monthly feedback report distributed to stakeholders | Customer Insights Manager | Narrative Reporting |
| 7 | Quarterly deep-dive analysis: trends, root causes, improvement recommendations | Customer Insights Analyst | CX Analytics + FDI |
| 8 | Action plans created for top 3 improvement areas | Cross-functional team | — |
| 9 | Action plan progress tracked monthly | Customer Insights Manager | — |

### SOP-CS-008: Service Recovery and Compensation

| Situation | Recovery Action | Authority | Max Value |
|-----------|----------------|-----------|-----------|
| Minor service failure (delay, minor error) | Verbal apology + 100 bonus loyalty points | CS Representative | PHP 100 equiv |
| Moderate service failure (wrong item, missed delivery) | Apology + replacement + 500 bonus loyalty points | Team Lead | PHP 500 equiv |
| Significant service failure (damaged product, rude behavior) | Apology + replacement/refund + PHP 500 store credit | CS Manager | PHP 1,000 |
| Major service failure (repeated failures, high-value B2B) | Personal apology (VP CX) + full refund + PHP 2,000 store credit + priority service for 6 months | Director CX | PHP 5,000 |
| Critical incident (safety, legal, PR risk) | Executive-level response + full remediation + significant compensation | VP CX + COO | Case-by-case (> PHP 5,000) |

### SOP-CS-009: Contractor/B2B Account Support

| Step | Activity | Responsible | System |
|------|----------|-------------|--------|
| 1 | B2B customer contacts dedicated B2B line or account manager | Customer | CX Service (B2B queue) |
| 2 | Agent verifies B2B account: company name, account number, authorized buyer | CS Representative | CX Service + AR |
| 3 | Check credit status: available credit limit, outstanding invoices, payment terms | CS Representative | AR |
| 4 | Handle inquiry: order status, pricing, bulk quote, delivery scheduling | CS Representative / Account Manager | OM + Pricing + TMS |
| 5 | For pricing disputes: check contract pricing in Oracle Pricing vs. invoiced price | CS Representative | Pricing + AR |
| 6 | For delivery issues: coordinate with supply chain and transportation | CS Representative | TMS + OM |
| 7 | For credit limit concerns: escalate to AR Credit Management | CS Representative | AR |
| 8 | Monthly B2B satisfaction check (account manager call) | Account Manager | CX Sales + CX Service |
| 9 | Quarterly B2B account review (with customer) | Account Manager + VP Sales | CX Sales |

### SOP-CS-010: Recall Customer Notification

| Step | Activity | Responsible | System |
|------|----------|-------------|--------|
| 1 | Recall directive received from Quality Assurance (per Doc 21) | VP CX | CX Service |
| 2 | Identify affected customers: product registrations, loyalty purchases, online orders | Customer Insights Analyst | CX CDP + POS + OM |
| 3 | Generate customer contact list with purchase details | Customer Insights Analyst | CX CDP |
| 4 | Draft customer notification (email, SMS, phone script) reviewed by Legal and QA | CX Manager + Legal | CX Service |
| 5 | Notification sent within 4 hours of recall directive (Critical) or 24 hours (Standard) | CS Representatives | CX Service + CX Marketing |
| 6 | Phone outreach to all affected customers (for Critical recalls) | CS Representatives | CX Service |
| 7 | Set up dedicated recall hotline queue | Contact Center Manager | CX Service |
| 8 | Process recall returns/exchanges per recall directive | CS Representatives + Stores | POS + OM + AR |
| 9 | Track recall response rate; follow up with non-responsive customers | Warranty Manager | CX Service |
| 10 | Close recall campaign when target response rate achieved; report to QA | VP CX | CX Service + PLM Quality |

---

## 24.10 Document Control

| Field | Detail |
|-------|--------|
| Document Title | Customer Service & After-Sales Operations |
| Document Set | Tahanan Depot Operations Documentation |
| Document Number | Doc 24 |
| Department | Customer Experience / Contact Center / After-Sales Services |
| Review Cycle | Annual (or upon regulatory change) |
| Last Reviewed | March 15, 2026 |
| Next Review | March 15, 2027 |
| Owner | VP Customer Experience |
| Approved By | Chief Operations Officer |

### Revision History

| Rev | Date | Author | Description |
|-----|------|--------|-------------|
| 1.0 | Mar 15, 2026 | R. Aquino | Initial release |
