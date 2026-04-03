# 17 — MARKETING OPERATIONS

## 17.1 Marketing Organization and Governance

### 17.1.1 Marketing Team Structure

```
CMO (Chief Marketing Officer, reports to CEO)
├── VP Brand & Advertising
│   ├── Brand Manager
│   ├── Creative Director
│   ├── Graphic Designers (4)
│   └── Video Producer (1)
├── VP Digital Marketing
│   ├── Digital Marketing Manager
│   ├── Social Media Specialists (3)
│   ├── SEO/SEM Specialist
│   ├── Email Marketing Specialist
│   └── Web Analytics Specialist
├── VP Loyalty & CRM
│   ├── Loyalty Program Manager
│   ├── CRM Manager
│   ├── Customer Insights Analyst
│   └── Partner Marketing Specialist
└── VP Trade Marketing
    ├── Trade Marketing Manager
    ├── Category Marketing Specialists (4)
    ├── Events Coordinator
    └── Visual Merchandising Lead
```

### 17.1.2 Oracle Fusion Roles

| Role | Oracle Fusion Security Roles |
|------|----------------------------|
| CMO | ORA_CX_MARKETING_EXECUTIVE, ORA_CX_LOYALTY_MANAGER, ORA_CX_CDP_ADMIN |
| VP Brand & Advertising | ORA_CX_MARKETING_MANAGER |
| VP Digital Marketing | ORA_CX_MARKETING_MANAGER, ORA_CX_ANALYTICS_SPECIALIST |
| VP Loyalty & CRM | ORA_CX_LOYALTY_MANAGER, ORA_CX_CDP_SPECIALIST |
| VP Trade Marketing | ORA_CX_MARKETING_SPECIALIST, ORA_CX_SALES_MANAGER |

### 17.1.3 Marketing Budget Management

| Category | Annual Budget (PHP) | % of Revenue | Allocation Method |
|----------|--------------------|-------------|-------------------|
| Digital advertising (social, SEM, display) | 225,000,000 | 0.50% | Per campaign ROI |
| Traditional advertising (TV, print, OOH) | 180,000,000 | 0.40% | Per campaign plan |
| Promotional flyers and circulars | 135,000,000 | 0.30% | Per promotional calendar |
| In-store signage and POS materials | 90,000,000 | 0.20% | Per store count |
| Loyalty program operations | 112,500,000 | 0.25% | Per member cost |
| Events and sponsorships | 67,500,000 | 0.15% | Per event plan |
| Trade marketing (supplier co-op) | 90,000,000 | 0.20% | Supplier-funded (matched) |
| Creative production (photo, video, design) | 45,000,000 | 0.10% | Per project |
| Marketing technology and tools | 22,500,000 | 0.05% | Annual subscription |
| Contingency | 32,500,000 | 0.07% | As needed |
| **Total Marketing Budget** | **PHP 1,000,000,000** | **2.22%** | |

### 17.1.4 Budget Approval Workflow

| Amount Range (PHP) | Approver | Oracle Workflow |
|---------------------|----------|-----------------|
| 0 — 500,000 | VP-level (per category) | Auto-approved in Oracle |
| 500,001 — 2,000,000 | CMO | Oracle workflow approval |
| 2,000,001 — 10,000,000 | CMO + CFO | Dual approval in Oracle |
| > 10,000,000 | CEO + CFO | Manual approval |

---

## 17.2 Brand Management

### 17.2.1 Brand Guidelines

| Element | Standard |
|---------|----------|
| Logo | Tahanan Depot wordmark in Tahanan Blue (Pantone 2945 C) or white on blue background; minimum clearance zone = height of "T" |
| Tagline | "Sa Bahay, Sa Tahanan" (At Home, At Tahanan) |
| Primary colors | Tahanan Blue (#003B73), Tahanan Orange (#FF6B00), White (#FFFFFF) |
| Secondary colors | Tahanan Light Blue (#4A90D9), Tahanan Gray (#666666), Tahanan Cream (#F5F0EB) |
| Typography | Headlines: Montserrat Bold; Body: Open Sans Regular; Filipino: Noto Sans Filipino |
| Photography style | Warm, well-lit, featuring Filipino families and homes; aspirational but relatable |
| Tone of voice | Friendly, helpful, expert, Filipino-spirited; Taglish acceptable in social media |
| Brand voice | "Kuya/Ate na eksperto sa bahay" (Helpful older sibling expert at home) |

### 17.2.2 Brand Asset Management
| Asset Type | Repository | Access | Update Frequency |
|-----------|-----------|--------|-----------------|
| Logo files (all formats) | Oracle Content Management | Brand Manager approves; all marketing has read access | Annual review or per rebrand |
| Brand guidelines PDF | Oracle Content Management | All employees via Oracle ME | Annual review |
| Photography library | Digital Asset Management (DAM) | Marketing team; agencies via limited access | Monthly additions |
| Video library | DAM | Marketing team | Per campaign |
| Templates (flyers, social, ads) | Oracle Content Management | Marketing team + stores (localized) | Per promotional calendar |
| Font licenses | Shared drive (IT managed) | Marketing team + creative | Per license renewal |

### 17.2.3 Brand Compliance
| Check | Frequency | Owner | Action for Non-Compliance |
|-------|-----------|-------|-------------------------|
| Store signage brand compliance | Monthly (store audit) | Brand Manager | Replace non-compliant signage within 5 days |
| Social media brand voice | Weekly | Social Media Specialist | Coach/correct post; update guidelines |
| Advertising material review | Per campaign | Creative Director | Revise before publication |
| Third-party brand usage | Quarterly | Brand Manager | Cease-and-desist or formalize agreement |
| Employee communication templates | Quarterly | VP Brand | Update non-compliant templates |

---

## 17.3 Campaign Planning and Execution

### 17.3.1 Annual Promotional Calendar

| Month | Campaign Type | Theme | Duration | Discount Depth |
|-------|--------------|-------|----------|----------------|
| January | New Year Home Refresh | Organize and refresh for the new year | 2 weeks | 15-25% |
| February | Valentine's Home Edition | Home improvement gifts, couple's projects | 1 week | 10-20% |
| March | Summer Ready | Aircon, fan, outdoor prep | 2 weeks | 15-30% |
| April | Build It Right | Contractor focus, building materials | 2 weeks | 10-20% |
| May | Mid-Year Sale | Store-wide clearance and promotion | 2 weeks | 20-50% |
| June | Rainy Season Prep | Roofing, waterproofing, paint | 2 weeks | 15-25% |
| July | Back-to-School DIY | Small projects, organization | 1 week | 10-15% |
| August | Independence Day Sale | Filipino pride, local products highlight | 1 week | 15-25% |
| September | Ber Months Prep | Christmas decorations, lights, paint | 2 weeks | 10-20% |
| October | Hardware Month | Tools, power tools, safety equipment | 2 weeks | 15-30% |
| November | 11.11 Mega Sale | Biggest sale of the year | 3 days | 25-50% |
| December | Holiday Home | Christmas decorations, gifts, appliances | 4 weeks | 15-30% |

### 17.3.2 Campaign Approval Workflow

| Step | Activity | Owner | SLA |
|------|----------|-------|-----|
| 1 | Campaign brief created (objective, target audience, budget, timeline, expected ROI) | Category Marketing Specialist | T-8 weeks before launch |
| 2 | Campaign brief reviewed | VP Brand or VP Trade Marketing | 3 business days |
| 3 | Creative brief developed | Creative Director | 5 business days |
| 4 | Creative materials produced | Creative team | 10 business days |
| 5 | Creative materials reviewed and approved | VP Brand + CMO | 3 business days |
| 6 | Pricing and promotions configured in Oracle Pricing | Pricing Analyst | T-2 weeks before launch |
| 7 | POS price sync verified | E-Commerce Merchandising Specialist | T-1 week before launch |
| 8 | Campaign launched | Per calendar | On schedule |
| 9 | Daily performance monitoring | Category Marketing Specialist | During campaign |
| 10 | Post-campaign performance review | VP Marketing + Category Manager | Within 5 business days of campaign end |

### 17.3.3 Campaign Budget Allocation
| Campaign Type | Budget Allocation Method | ROI Target | Measurement Period |
|--------------|------------------------|------------|-------------------|
| Seasonal sale | % of annual budget proportional to expected revenue lift | > 5:1 (revenue:spend) | Campaign duration + 1 week |
| Category promotion | Per category budget; supplier co-op eligible | > 4:1 | Campaign duration |
| Flash sale / 11.11 | Dedicated budget from promotional pool | > 8:1 | 3 days |
| Loyalty member exclusive | Funded from loyalty budget | > 3:1 (incremental revenue) | Campaign duration |
| New product launch | Per launch budget | > 2:1 (awareness + revenue) | 30 days |
| Brand awareness | Allocated from brand budget | Reach and frequency targets | 90 days |

---

## 17.4 Digital Marketing Operations

### 17.4.1 Social Media Management

| Platform | Handle | Followers (Target) | Content Frequency | Primary Audience |
|----------|--------|---------------------|-------------------|-----------------|
| Facebook | @tahanandepot | 2,000,000 | 2 posts/day | Homeowners 30-55, contractors |
| Instagram | @tahanandepot | 800,000 | 1 post/day + 5 stories/week | Homeowners 25-45, DIY enthusiasts |
| TikTok | @tahanandepot | 500,000 | 5 videos/week | Young homeowners 20-35 |
| YouTube | Tahanan Depot | 200,000 | 2 videos/week (DIY tutorials) | All DIY enthusiasts |
| X (Twitter) | @tahanandepot | 100,000 | 3 tweets/day | News, customer service, contractors |
| LinkedIn | Tahanan Depot | 50,000 | 2 posts/week | B2B, contractors, suppliers, hiring |
| Viber Community | Tahanan Depot | 300,000 | 2 broadcasts/week | Existing customers, loyalty members |

### 17.4.2 Social Media Content Calendar

| Day | Facebook | Instagram | TikTok | YouTube |
|-----|----------|-----------|--------|---------|
| Monday | Product highlight | Reel: DIY tip | — | — |
| Tuesday | Promo announcement | Carousel: project inspiration | Trending DIY hack | — |
| Wednesday | Customer story | Reel: product demo | Behind the scenes | — |
| Thursday | How-to guide link | Story: poll/quiz | — | DIY tutorial |
| Friday | Weekend project idea | Reel: room makeover | — | — |
| Saturday | Event/workshop promo | Story: live event | Weekend project challenge | Product review |
| Sunday | Inspiration board | Reel: before/after | — | — |

### 17.4.3 Social Media Response Protocol
| Scenario | Response Time | Approval Required | Response By |
|----------|--------------|-------------------|-------------|
| Product inquiry | < 1 hour | No (standard response) | Social Media Specialist |
| Store hours/location question | < 30 minutes | No | Social Media Specialist |
| Positive feedback/thank you | < 2 hours | No | Social Media Specialist |
| Complaint (product) | < 1 hour | No; escalate to CX Service | Social Media Specialist → CX Service |
| Complaint (service) | < 1 hour | Yes (if public) | Social Media Specialist → VP Customer Service |
| Pricing question | < 1 hour | No | Social Media Specialist |
| Safety concern | < 15 minutes | Yes | VP Brand → VP Store Ops + CLO |
| Negative viral post | < 30 minutes | Yes | CMO + VP Brand |
| Media inquiry via social | < 1 hour | Yes | CMO → Communications |

### 17.4.4 Email Marketing Operations

| Campaign Type | Frequency | Audience | Oracle Module | Target Metrics |
|--------------|-----------|----------|---------------|----------------|
| Weekly newsletter | Weekly (Wednesday 10 AM) | All opted-in subscribers | CX Marketing | Open rate > 25%; CTR > 3% |
| Promotional announcement | Per campaign | Segment by interest/purchase history | CX Marketing + CDP | Open rate > 30%; CTR > 5% |
| Abandoned cart recovery | Triggered (2 hours, 24 hours, 72 hours after abandon) | Cart abandoners | CX Marketing + Commerce | Recovery rate > 10% |
| Loyalty member update | Monthly | Active loyalty members | CX Loyalty + Marketing | Open rate > 35% |
| Post-purchase follow-up | Triggered (7 days after purchase) | Recent buyers | CX Marketing + CDP | Open rate > 40% |
| Birthday greeting + offer | Triggered (birthday month) | Loyalty members | CX Loyalty + Marketing | Redemption rate > 20% |
| DIY project inspiration | Bi-weekly | Engaged customers | CX Marketing + CDP | Open rate > 20%; CTR > 4% |
| Contractor/B2B newsletter | Monthly | B2B customers | CX Marketing + Sales | Open rate > 30% |
| Re-engagement (inactive 90 days) | Monthly | Inactive customers | CX Marketing + CDP | Reactivation rate > 5% |
| Win-back (inactive 180 days) | Quarterly | Lapsed customers | CX Marketing + CDP | Reactivation rate > 3% |

### 17.4.5 SEO/SEM Strategy

| Channel | Budget (Annual) | Strategy | Target |
|---------|----------------|----------|--------|
| Google Ads (Search) | PHP 60M | Category + brand keywords; local store keywords; competitor keywords | ROAS > 5:1 |
| Google Ads (Shopping) | PHP 30M | Product listing ads for top 20,000 SKUs | ROAS > 8:1 |
| Google Ads (Display) | PHP 15M | Retargeting; lookalike audiences | ROAS > 3:1 |
| Facebook/Instagram Ads | PHP 75M | Conversion campaigns; brand awareness; retargeting | ROAS > 4:1 |
| TikTok Ads | PHP 20M | Brand awareness; video views | ROAS > 2:1 |
| YouTube Ads | PHP 15M | Pre-roll on home improvement content; DIY channels | ROAS > 3:1 |
| SEO (organic) | PHP 10M (team + tools) | Content marketing; product page optimization; local SEO for 120 stores | Organic traffic +20% YoY |

### 17.4.6 Paid Advertising Approval
| Spend Level | Approval Required | Approver |
|------------|-------------------|----------|
| < PHP 100,000/campaign | VP Digital Marketing | Auto-approved |
| PHP 100,001 - 500,000/campaign | CMO | Oracle workflow |
| PHP 500,001 - 2,000,000/campaign | CMO + CFO | Oracle workflow |
| > PHP 2,000,000/campaign | CEO + CMO | Manual approval |

---

## 17.5 Traditional Marketing

### 17.5.1 Promotional Flyers and Circulars

| Publication | Frequency | Distribution | Print Run | Distribution Method |
|-------------|-----------|-------------|-----------|-------------------|
| Major seasonal flyer | 10x/year (per promotional calendar) | All 120 stores + direct mail | 500,000 per edition | Store handout, newspaper insert, direct mail (targeted ZIP codes) |
| Weekly deals circular | Weekly | All 120 stores + digital | 200,000 per week | Store handout, email, social media |
| B2B contractor catalog | Quarterly | Active B2B customers | 50,000 per edition | Direct mail, Pro Desk handout |
| New store grand opening flyer | Per opening | 20km radius from new store | 100,000 | Door-to-door, newspaper insert, store handout |

### 17.5.2 Out-of-Home (OOH) Advertising

| Format | Locations | Duration | Annual Budget | Purpose |
|--------|-----------|----------|---------------|---------|
| Billboard (large format) | 20 high-traffic Metro Manila + provincial locations | Per campaign (4-8 weeks) | PHP 40M | Brand awareness; store opening; major sale |
| Transit ads (MRT/LRT, bus) | Metro Manila rail lines + bus routes | Per campaign | PHP 15M | Brand awareness; store traffic |
| Mall signage | Partner malls (store locations) | Annual lease | PHP 10M | Store presence |
| Vehicle wrapping (delivery trucks) | Owned fleet (20 trucks) | Annual | PHP 5M | Mobile brand awareness |

### 17.5.3 TV and Radio Advertising

| Channel | Strategy | Annual Budget | Frequency |
|---------|----------|---------------|-----------|
| Free TV (GMA, ABS-CBN, TV5) | 30-second spots during major campaigns | PHP 60M | Major campaigns only (11.11, Christmas, Mid-Year) |
| Cable TV | 15-second spots on home/lifestyle channels | PHP 15M | Quarterly |
| Radio (FM stations) | 15-second spots; contest sponsorships | PHP 20M | Ongoing during campaign periods |

---

## 17.6 Trade Marketing and Supplier Co-op

### 17.6.1 Supplier Co-op Marketing Program

| Tier | Supplier Investment | Tahanan Match | Total Budget | Eligibility |
|------|--------------------|---------------|-------------|-------------|
| Platinum | Supplier invests PHP 5M+ | 100% match | PHP 10M+ | Top 10 suppliers by spend |
| Gold | Supplier invests PHP 2M-5M | 100% match | PHP 4M-10M | Top 50 suppliers by spend |
| Silver | Supplier invests PHP 500K-2M | 75% match | PHP 875K-3.5M | Top 200 suppliers |
| Bronze | Supplier invests < PHP 500K | 50% match | Up to PHP 750K | All active suppliers |

### 17.6.2 Co-op Marketing Activities

| Activity | Description | Typical Cost Share | Approval |
|----------|-------------|-------------------|----------|
| In-store display and signage | Branded display in designated area | 50/50 | Category Manager + Supplier |
| Flyer/catalog feature | Product feature in promotional flyer | 60/40 (supplier majority) | Trade Marketing Manager |
| Social media collaboration | Joint social media posts and campaigns | 50/50 | Digital Marketing Manager |
| Demo/sampling event | In-store product demonstration | 70/30 (supplier majority) | Store Manager + Trade Marketing |
| Trade discount funding | Supplier funds additional discount on their products | 100% supplier | Category Manager |
| New product launch support | Launch campaign for new product introduction | 50/50 | VP Trade Marketing + Supplier |
| Store anniversary sponsorship | Supplier sponsors store anniversary promotions | 60/40 | Regional Director + Trade Marketing |

### 17.6.3 Supplier Co-op Process

| Step | Activity | Owner | SLA |
|------|----------|-------|-----|
| 1 | Supplier submits co-op marketing proposal (via Supplier Portal) | Supplier | — |
| 2 | Trade Marketing reviews proposal alignment with promotional calendar | Trade Marketing Manager | 5 business days |
| 3 | Budget allocation confirmed and co-op agreement signed | VP Trade Marketing + Category Manager | 3 business days |
| 4 | Creative materials produced (supplier or Tahanan creative team) | Creative Director | Per timeline |
| 5 | Campaign executed per agreed timeline | Trade Marketing Manager | Per calendar |
| 6 | Post-campaign performance review and ROI analysis | Trade Marketing Manager + Category Manager | Within 10 business days |
| 7 | Supplier reimbursement/reconciliation processed | AP Manager + Trade Marketing Manager | Within 15 business days |

---

## 17.7 Loyalty Program Marketing

### 17.7.1 Member Communication Calendar

| Communication | Frequency | Segment | Channel | Oracle Module |
|--------------|-----------|---------|---------|---------------|
| Points summary | Monthly | All active members | Email + ME | CX Loyalty + Marketing |
| Tier upgrade notification | Triggered | Upgraded member | Push + email | CX Loyalty |
| Birthday offer | Triggered | Birthday month member | Email + SMS | CX Loyalty + Marketing |
| Double points weekend | Monthly | All members | Push + email + social | CX Loyalty + Marketing |
| Exclusive member sale | Quarterly | Gold + Platinum | Email + SMS | CX Loyalty + Marketing |
| Partner offer | Monthly | All members | Email | CX Loyalty + Marketing |
| Tier benefit reminder | Semi-annual | Silver members approaching next tier | Email | CX Loyalty + Marketing |
| Expiring points reminder | Triggered (90 days before expiry) | Members with points nearing expiry | Push + email | CX Loyalty + Marketing |
| Re-engagement offer | Triggered (90 days inactive) | Inactive members | Email + SMS | CX Loyalty + Marketing |
| Annual member survey | Annual | All members | Email | CX Loyalty + Marketing |

### 17.7.2 Loyalty Promotions
| Promotion | Frequency | Mechanism | Oracle Fusion Touchpoint |
|-----------|-----------|-----------|------------------------|
| Double points weekend | Monthly (1 weekend) | 2x point multiplier for all purchases | CX Loyalty (multiplier rule) |
| Category bonus points | Weekly (rotating categories) | Bonus points for specific department purchases | CX Loyalty (bonus rule) |
| Birthday bonus | Triggered | Triple points during birthday month | CX Loyalty (member event rule) |
| Referral bonus | Ongoing | 500 bonus points for referrer; 200 for new member | CX Loyalty (referral rule) |
| App download bonus | One-time | 200 points for first mobile app purchase | CX Loyalty (event rule) |
| Review bonus | Ongoing | 100 points for product review submission | CX Loyalty (event rule) |
| Store check-in bonus | Weekly | 50 points for in-store check-in via app | CX Loyalty (location rule) |

---

## 17.8 Event Marketing

### 17.8.1 Event Calendar

| Event | Frequency | Per Store | Per Region | Target Attendance | Budget/Event |
|-------|-----------|-----------|------------|-------------------|-------------|
| DIY Workshop (basic plumbing, painting, electrical safety, tiling) | Monthly | 1 per month | 12 per region per year | 20-30 attendees | PHP 15,000 |
| Pro Club Event (networking, demo, exclusive offers) | Quarterly | — | 1 per region per quarter | 50-100 attendees | PHP 150,000 |
| Product Demonstration (power tools, appliances) | Weekly (weekends) | 1 per weekend | — | 10-20 attendees | PHP 5,000 |
| Store Anniversary Celebration | Annual | 1 per store | — | 200+ attendees | PHP 200,000 |
| Community Service Event | Annual | — | 1 per region per year | Varies | PHP 100,000 |
| Kids' Workshop (birdhouse, picture frame) | Quarterly | 1 per quarter | — | 15-25 kids | PHP 10,000 |
| Contractor Appreciation Day | Semi-annual | — | 1 per region | 100+ contractors | PHP 300,000 |

### 17.8.2 DIY Workshop Operations

| Step | Activity | Owner | SLA |
|------|----------|-------|-----|
| 1 | Workshop topic selected (aligned with seasonal demand) | Store Manager + L&D Specialist | T-4 weeks |
| 2 | Materials and tools procured (per demo budget) | Stock Associate | T-2 weeks |
| 3 | Event listed on website, app, and social media | Digital Marketing Specialist | T-2 weeks |
| 4 | Registration managed via CX Commerce or Oracle ME | Customer Service Specialist | Ongoing |
| 5 | Workshop conducted by Department Supervisor or supplier trainer | Department Supervisor | Event day |
| 6 | Attendee feedback collected via Oracle ME survey | Store Manager | Same day |
| 7 | Workshop attendance tracked in Oracle Learning (if employee) or CX CDP (if customer) | L&D Specialist | Within 3 days |

---

## 17.9 Marketing Analytics and ROI

### 17.9.1 Campaign Performance Metrics

| Metric | Definition | Target | Source | Frequency |
|--------|------------|--------|--------|-----------|
| Return on Ad Spend (ROAS) | Revenue attributed to campaign / ad spend | > 5:1 | CX Analytics + ERP Analytics | Per campaign |
| Customer Acquisition Cost (CAC) | Total marketing spend / new customers acquired | < PHP 500 | CX CDP Analytics | Monthly |
| Customer Lifetime Value (LTV) | Projected total revenue from customer over relationship | > PHP 15,000 | CX CDP Analytics | Quarterly |
| LTV:CAC Ratio | LTV / CAC | > 10:1 | CX Analytics | Quarterly |
| Email open rate | Emails opened / emails sent | > 25% | CX Marketing | Per campaign |
| Email click-through rate (CTR) | Clicks / emails delivered | > 3% | CX Marketing | Per campaign |
| Social media engagement rate | (Likes + comments + shares) / impressions | > 3% | Social media analytics | Weekly |
| Flyer redemption rate | Flyer promo codes redeemed / flyers distributed | > 5% | POS Analytics | Per campaign |
| Conversion rate (e-commerce) | Orders / website visits | > 2.5% | CX Commerce Analytics | Weekly |
| Foot traffic lift (during campaign) | Store traffic vs. baseline | > 10% lift | POS Analytics + foot traffic counter | Per campaign |
| Incremental revenue during campaign | Sales lift vs. comparable non-campaign period | > 3x campaign spend | ERP Analytics | Per campaign |

### 17.9.2 Attribution Model

| Channel | Attribution Model | Lookback Window | Oracle Module |
|---------|------------------|-----------------|---------------|
| Paid search (Google/Bing) | Last-click | 30 days | CX Marketing + Analytics |
| Paid social (FB/IG/TikTok) | Last-click | 7 days | CX Marketing + Analytics |
| Email marketing | Last-click | 7 days | CX Marketing |
| Direct mail (flyer) | Promo code redemption | 14 days | POS + CX Marketing |
| Organic search | Last-click | Session-based | CX Analytics |
| Social media (organic) | Assisted (within 7 days) | 7 days | CX Analytics |
| Display/retargeting | View-through (if within 24 hours) | 1 day | CX Marketing + Analytics |
| Loyalty program | First-party data | Lifetime | CX Loyalty + CDP |
| In-store events | Attendance + purchase | 14 days | POS + CX Marketing |
| B2B referral | First-touch | 90 days | CX Sales + Analytics |

### 17.9.3 Marketing Dashboard
| Dashboard | Audience | Frequency | Key Widgets |
|-----------|----------|-----------|-------------|
| Campaign performance tracker | CMO, VPs | Daily (during campaign) | Spend, ROAS, conversions, revenue |
| Channel performance comparison | CMO, VP Digital | Weekly | ROAS by channel, CAC, LTV |
| Loyalty program health | VP Loyalty | Monthly | Enrollment rate, active rate, redemption rate, tier distribution |
| Social media analytics | VP Digital | Weekly | Engagement, reach, follower growth, sentiment |
| Email marketing performance | Digital Marketing Manager | Per campaign | Open rate, CTR, unsubscribe rate, revenue |
| Annual marketing ROI | CMO, CFO, CEO | Annual | Total spend vs. incremental revenue; LTV:CAC |

---

## 17.10 Creative Asset Management

### 17.10.1 Creative Production Process

| Step | Activity | Owner | SLA |
|------|----------|-------|-----|
| 1 | Creative brief developed from campaign brief | Creative Director | 3 business days |
| 2 | Concept development (2-3 options) | Graphic Designers / Video Producer | 5 business days |
| 3 | Concept review and selection | VP Brand + requesting VP | 2 business days |
| 4 | Final creative production | Creative team | 7 business days |
| 5 | Legal/compliance review (if required: claims, pricing, disclaimers) | CLO or delegate | 2 business days |
| 6 | Final approval | CMO (or delegate) | 1 business day |
| 7 | Assets distributed to channels | Marketing Operations | Per campaign timeline |
| 8 | Assets archived in DAM | Creative Director | Within 5 business days of campaign end |

### 17.10.2 Localization Standards

| Element | Filipino Market Standard |
|---------|------------------------|
| Language | Filipino (Tagalog) primary; English acceptable for technical terms |
| Currency display | PHP with comma separator (e.g., PHP 1,500.00) |
| Date format | Month DD, YYYY (e.g., April 15, 2026) |
| Phone format | +63 (XX) XXX-XXXX |
| Measurements | Metric system (meters, kilograms, liters) |
| Model representation | Filipino faces; diverse skin tones; family-oriented |
| Seasonal relevance | Philippine seasons (dry: December-May; wet: June-November) |
| Cultural sensitivity | Avoid imagery inconsistent with Filipino values; respect religious diversity |
| Regulatory | BIR TIN on receipts; DTI price tags; FDA for regulated products |

---

## 17.11 Public Relations and Media Relations

### 17.11.1 PR Activities

| Activity | Frequency | Owner | Oracle Module |
|----------|-----------|-------|---------------|
| Press release distribution | Per major event (store opening, major campaign, milestone) | VP Brand + CLO | Narrative Reporting (press release archive) |
| Media monitoring | Daily | Social Media Specialist | External media monitoring tool |
| Spokesperson availability | Per event | CMO (primary), CEO (major), COO (operational) | — |
| Influencer engagement | Per campaign | Digital Marketing Manager | CX Marketing |
| CSR communication | Per CSR event | VP Brand + CHRO | Narrative Reporting |
| Annual report communication | Annual | VP Finance + CMO | Narrative Reporting |

### 17.11.2 Media Inquiry Response Protocol

| Inquiry Type | Response SLA | Spokesperson | Approval |
|-------------|-------------|-------------|----------|
| Product inquiry | < 4 hours | Category Manager or VP Merchandising | No |
| Store operations | < 4 hours | VP Store Ops | No |
| Financial results | < 24 hours | CFO or VP Finance | CEO approval required |
| Crisis / negative story | < 1 hour | CLO + CEO | CEO + CLO |
| Feature / profile story | < 24 hours | CMO | CMO |
| CSR / community story | < 8 hours | CHRO or VP Brand | No |

---

## 17.12 Social Media Policy

### 17.12.1 Employee Social Media Guidelines

| Guideline | Policy |
|-----------|--------|
| Official accounts | Only authorized Social Media Specialists may post on official Tahanan Depot accounts |
| Personal social media | Employees must not represent themselves as official spokespersons; disclaimer required if discussing work |
| Confidential information | No sharing of non-public company data (sales figures, strategies, financial results) |
| Customer information | No sharing of customer data, photos, or transactions without consent |
| Store incidents | No posting of store incidents (theft, accidents, customer disputes) — refer to LP |
| Product complaints | Direct customers to official customer service channels |
| Positive mentions | Encouraged to like, share, and engage positively with official Tahanan Depot content |
| Trademark usage | Tahanan Depot logo and trademarks not to be used on personal accounts without approval |

### 17.12.2 Social Media Crisis Protocol

| Level | Trigger | Response | Owner | SLA |
|-------|---------|----------|-------|-----|
| Level 1 — Minor | Single negative post (< 100 engagements) | Standard response + monitor | Social Media Specialist | < 1 hour |
| Level 2 — Moderate | Multiple negative posts or > 500 engagements | Prepared statement + VP notification | Social Media Specialist + VP Brand | < 30 minutes |
| Level 3 — Major | Viral negative post (> 5,000 engagements) or media pickup | Crisis communication team activated; CMO approval for all responses | CMO + VP Brand + CLO | < 15 minutes |
| Level 4 — Critical | Trending topic; national media coverage; legal/safety issue | CEO + CMO + CLO crisis team; all external comms paused except approved statements | CEO | Immediate |

### 17.12.3 Content Calendar Management

| Planning Horizon | Owner | Review | Oracle Fusion Touchpoint |
|-----------------|-------|--------|------------------------|
| Annual content themes | CMO + VP Brand | Annual (November for following year) | Narrative Reporting (content calendar) |
| Monthly content plan | Digital Marketing Manager | Monthly (last week of prior month) | CX Marketing |
| Weekly content schedule | Social Media Specialists | Weekly (Friday for following week) | CX Marketing |
| Real-time content | Social Media Specialists | Post-fact review (weekly) | CX Marketing |
| Campaign-specific content | Category Marketing Specialist | Per campaign brief | CX Marketing + CDP |
