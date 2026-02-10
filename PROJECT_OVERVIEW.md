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

## 3. Service Plans & Pricing Tiers

### Tier 1: Basic (Outreach‑Only)
- **Price:** SGD 0 upfront + **SGD 20 per booked appointment**
- **Features:**
  - Personalised cold‑email outreach (max 150 emails/day)
  - Lead qualification via AI chatbot
  - Basic appointment scheduling
  - Weekly performance report
- **Target:** Small dealerships (<10 listings)

### Tier 2: Premium (Full Automation)
- **Price:** **SGD 299/month** + SGD 15 per booked appointment
- **Features:**
  - Everything in Basic
  - AI‑powered response handling (24/7)
  - LinkedIn semi‑automation
  - WhatsApp follow‑up module
  - Cal.com integration (direct calendar booking)
  - Advanced analytics dashboard
  - A/B testing of messaging
- **Target:** Mid‑size dealerships (10‑50 listings)

### Tier 3: Enterprise (White‑Label)
- **Price:** **SGD 999/month** (unlimited appointments)
- **Features:**
  - Everything in Premium
  - White‑label branding
  - Custom workflow design
  - Priority support
  - API access
  - Ad‑management module (optional add‑on)
- **Target:** Large dealership groups & franchises

**Payment Model:**  
- **Pay‑per‑appointment:** Charged only when a demo/appointment is booked.
- **Monthly subscription:** Fixed fee plus reduced per‑appointment rate.
- **No contract;** cancel anytime.

## 4. Current Infrastructure

### API Keys & Services
- **GitHub:** Memory sync (`automated‑lead‑gen‑dealership` repo)
- **Zoho Mail:** SMTP sending (app‑specific password)
- **SmartProxy:** Rotating proxies for scraping (IP whitelisted)
- **Brave Search API:** Email enrichment (rate‑limited)
- **Stripe:** Payment processing (key available)
- **HubSpot:** CRM integration (key available)
- **Cal.com:** Meeting scheduling (key available)
- **DeepSeek Chat API:** Required for Phase 3 (pending key)

### Codebase
- **Location:** `/home/nenuka/.openclaw/workspace/autoleads`
- **Modules:**
  - `config/` – Secure key management
  - `scripts/` – Core automation scripts
  - `templates/` – Email templates (initial, follow‑up, breakup)
  - `memory/` – Local JSON storage (synced to GitHub)
  - `memory_repo/` – GitHub‑backed persistent memory

### Cron Jobs
1. **Morning outreach batch:** Mon‑Fri 9am SGT (limit 10 emails)
2. **Enrichment resumption:** After Brave API cooldown

## 5. Key Metrics (Live)
- **Total dealers in database:** 74
- **Dealers contacted (today):** 4 (status: contacted)
- **Emails sent (today):** 10 (8 real, 2 mock)
- **Invalid emails/bounces:** 0
- **Daily email limit:** 150 (Zoho)
- **Proxy usage:** ~10 GB/month (SmartProxy)

## 6. Next Immediate Actions
1. Resume Brave API enrichment (54 dealers pending)
2. Send follow‑up emails to contacted dealers (3‑day wait)
3. Implement LinkedIn semi‑automation (Phase 5)
4. Integrate Cal.com for direct booking
5. Obtain DeepSeek Chat API key for Phase 3

## 7. Contact & Support
- **Primary Contact:** Nenuka (@Sk_nuka)
- **Phone:** +65 87899536
- **Email:** adminone@islandicinsights.com
- **Cal.com Booking:** https://cal.com/islandicinsights/automated-lead-gen-introductory-call-selected

---

*This document is automatically updated by the AutoLeads SG system.*