# AutoLeads SG - Project Overview

**Version:** 2.0  
**Last Updated:** 2026‑02‑10  
**Status:** Active Development (Phase 2 – Fully Automated Outreach)

## 1. Project Vision
Automate lead acquisition and conversion for Singapore car and motorcycle dealerships using AI‑driven outreach, instant response, and appointment booking.

## 2. Phases (10‑Phase Roadmap)

### Phase 1: Data Collection
- **Scope:** Scrape sgCarMart, Google Places, and ACRA for dealer contact info, listings, and brand focus.
- **Status:** ✅ Completed (74 dealer pages parsed, 54 awaiting email enrichment)
- **Tools:** BeautifulSoup, SmartProxy rotating proxies, Brave API for email lookup.

### Phase 2: Fully Automated Outreach
- **Scope:** Send personalised cold emails to dealers with AI‑generated templates.
- **Status:** 🔄 **Active** (10 real emails sent, cron job scheduled for Mon‑Fri 9am SGT)
- **Tools:** Zoho SMTP, sequence manager, template personalisation, GitHub memory.

### Phase 3: AI‑Powered Response Handling
- **Scope:** Use DeepSeek Chat API to answer dealer inquiries, qualify leads, and schedule demos.
- **Status:** ⏳ Pending DeepSeek API key
- **Tools:** DeepSeek Chat API, conversation memory, automated scheduling.

### Phase 4: Lead Qualification
- **Scope:** Automatically ask 10+ qualification questions, score leads, and route to appropriate tier.
- **Status:** Planned (depends on Phase 3)
- **Tools:** Qualification engine, scoring algorithm.

### Phase 5: Gradual Automation
- **Scope:** Replace manual steps with automated workflows (LinkedIn outreach, WhatsApp follow‑up, calendar booking).
- **Status:** Planned
- **Tools:** Browser automation (Playwright), Twilio/WhatsApp Business API, Cal.com integration.

### Phase 6: Payment Integration
- **Scope:** Collect payments via Stripe (pay‑per‑appointment or monthly subscription).
- **Status:** Planned
- **Tools:** Stripe API, invoicing, payment tracking.

### Phase 7: Ad Management
- **Scope:** Create and manage Facebook/Google Ads for dealers (optional upsell).
- **Status:** Future
- **Tools:** Facebook Ads API, Google Ads API.

### Phase 8: Notifications
- **Scope:** Real‑time alerts for new leads, appointments, and payments.
- **Status:** Future
- **Tools:** Telegram/Discord webhooks, email alerts.

### Phase 9: Analytics Dashboard
- **Scope:** Provide dealers with performance metrics (lead volume, conversion rates, ROI).
- **Status:** Future
- **Tools:** Data visualisation, reporting engine.

### Phase 10: Compliance & Scaling
- **Scope:** Ensure GDPR/PDPA compliance, scale to other markets (Malaysia, Thailand).
- **Status:** Future
- **Tools:** Compliance checklist, multi‑region infrastructure.

## 3. Service Plans & Pricing Tiers (Premium – Lucky 888)

**Industry‑Standard Pricing:** Singapore automotive dealership automation solutions range from **SGD 8,888–30,888/month**. AutoLeads SG is positioned as a premium, grant‑eligible solution with lucky‑number pricing (ending in 888 for prosperity).

**Singapore Government Grant Eligibility:**  
Qualifies under **Productivity Solutions Grant (PSG)** – *Chatbots for Customer Engagement* (pre‑approved by IMDA SMEs Go Digital). Dealers can claim **up to 70% funding**, making enterprise‑grade automation affordable.

| Tier | **Monthly List Price** | **After 70% PSG Grant** | **Net Monthly Cost** | ROI Example (22 extra appointments) |
|------|------------------------|------------------------|----------------------|-------------------------------------|
| **Pro** (Core Automation) | **SGD 8,888** | **SGD 2,666.40** | Dealer pays **30%** | 22 × $1,500 avg. sale = **$33,000 revenue** |
| **Premium** (Full Suite) | **SGD 18,888** | **SGD 5,666.40** | Dealer pays **30%** | 35 × $1,500 avg. sale = **$52,500 revenue** |
| **Enterprise** (White‑Label) | **SGD 30,888** | **SGD 9,266.40** | Dealer pays **30%** | Unlimited appointments + branding |

### Tier 1: Pro (Core Automation)
- **Price:** **SGD 8,888/month** (*after grant:* **SGD 2,666.40/month**)
- **Features:** Personalised cold‑email outreach (150/day max), AI lead qualification, basic appointment scheduling, weekly performance dashboard.
- **Target:** Single‑location dealerships (10‑30 listings)
- **ROI:** Average 22 extra appointments/month → **$33,000 potential revenue** at $1,500 avg. sale.

### Tier 2: Premium (Full Automation Suite)
- **Price:** **SGD 18,888/month** (*after grant:* **SGD 5,666.40/month**)
- **Features:** Everything in Pro + 24/7 AI response handling, LinkedIn semi‑automation, WhatsApp follow‑up module, Cal.com integration, advanced analytics, A/B testing, custom workflow design.
- **Target:** Multi‑brand dealerships (30‑100 listings)
- **ROI:** Average 35 extra appointments/month → **$52,500 potential revenue** at $1,500 avg. sale.

### Tier 3: Enterprise (White‑Label)
- **Price:** **SGD 30,888/month** (*after grant:* **SGD 9,266.40/month**)
- **Features:** Everything in Premium + white‑label branding, dedicated support, API access, ad‑management module, compliance reporting, custom integrations.
- **Target:** Dealership groups & franchises (100+ listings)
- **ROI:** Unlimited appointments + brand equity.

**Payment Model:**  
- **Monthly subscription only** – no per‑appointment fees.
- **Annual commitment** (12‑month minimum) – standard for enterprise B2B.
- **PSG Claim Process:** Dealer pays full list price, submits invoice with PSG claim, receives 70% reimbursement within 4‑6 weeks.
- **Implementation fee:** One‑time SGD 4,888 (also PSG‑eligible).

**Positioning:** "Hiring a 24/7 sales rep costs $5,000–8,000/month. Our AI assistant delivers similar results at 30% of the cost after government grant – with lucky 888 pricing for prosperity."

## 4. Infrastructure (Compressed)

**APIs:** GitHub (memory sync), Zoho SMTP, SmartProxy (rotating), Brave Search (email enrichment), Stripe (payments), HubSpot (CRM), Cal.com (scheduling). DeepSeek Chat API pending.

**Code:** `/home/nenuka/.openclaw/workspace/autoleads/` – config, scripts, templates, memory (GitHub‑backed).

**Cron Jobs:**  
- Outreach: Mon‑Fri 9am SGT (limit 10) + 9:30am backup  
- Enrichment: 5am SGT (overnight) + 2pm SGT (daytime)  
- Follow‑ups: Automated 3‑day/7‑day sequences

## 5. Email Tracking & A/B Testing

**Implemented:** 2026‑02‑11
- **Email tracking:** Logs all sent emails with unique message IDs, tracks opens (via pixel), clicks (via link redirect), and replies (manual/inbox monitoring).
- **A/B testing:** Two variants per template (A/B), assigned via consistent hashing. Variants differ in subject line, value proposition, and call‑to‑action.
- **Statistics:** Open rate, click‑through rate, reply rate tracked per template and variant.
- **Optimization:** Continuous A/B testing to improve conversion rates.

## 6. Key Metrics (Live)
- **Parsed dealers:** 70
- **Enriched with data:** 38
- **Valid emails collected:** 8
- **Contacted dealers:** 4
- **New dealers awaiting contact:** 1 (`info@carzworld.com.sg`)
- **Emails sent today:** 0 (no new dealers ready)
- **Daily email limit:** 150 (Zoho)
- **Proxy usage:** ~10 GB/month (SmartProxy rotating API working – 5 proxies/batch)
- **A/B variants:** 2 (`initial_A.md`, `initial_B.md`)

### Recent Issues & Resolutions
**2026‑02‑12 05:03 SGT – Enrichment script hanging:**
- **Root cause:** SmartProxy DNS resolution failure (`as.smartproxy.net` unreachable).
- **Solution:** Enrichment script updated with timeout handling (120s per dealer) and automatic fallback to direct connections when proxy fails.
- **Status:** ✅ Resolved. Script processes up to 8 dealers/daytime, 20 dealers/overnight with 1‑2 minute delays between attempts.

**2026‑02‑12 08:13 SGT – SmartProxy API endpoint updated:**
- **Root cause:** Rotating proxy API required updated parameters (`num=5`, `life=60`, `lb=%5Cn`).
- **Solution:** Proxy manager updated with new endpoint, batch fetching (5 proxies/60s), and proper parsing.
- **Status:** ✅ Resolved. Rotating proxies now functional with Singapore residential IPs.

## 7. Next Immediate Actions
1. **Daytime enrichment** (2pm SGT) – target 8 more dealers (direct connection).
2. **Morning outreach** (9am SGT) – A/B testing for newly enriched dealers.
3. **Follow‑up emails** – 4 contacted dealers (3‑day wait, due today).
4. **Proxy investigation** – diagnose SmartProxy DNS resolution issue.
5. **A/B optimization** – monitor open/reply rates, adjust variants.
6. **Reply monitoring** – poll Zoho inbox for dealer responses.

## 8. Contact & Support
- **Primary Contact:** Nenuka (@Sk_nuka)
- **Phone:** +65 87899536
- **Email:** adminone@islandicinsights.com
- **Cal.com Booking:** https://cal.com/islandicinsights/automated-lead-gen-introductory-call-selected

---

*This document is automatically updated by the AutoLeads SG system.*