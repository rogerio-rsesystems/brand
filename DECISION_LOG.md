# Decision Log
## RG Enterprise Consulting — Website & Platform Project

All locked decisions are recorded here. Claude reads this at the start of every session.

---

## Design & Brand ✅ All Locked

| Date | # | Decision | Detail |
|------|---|----------|--------|
| Jun 2026 | Q1 | **Colors: Navy + Gold on white** | Primary `#1B2A4A`, Accent `#C8A84B`, BG `#FFFFFF`, Alt BG `#F7F8FC`, Cream `#FDFAF3`, Dark footer `#111D33` |
| Jun 2026 | Q2 | **Fonts: Montserrat + Inter** | Headings: Montserrat 800. Body: Inter 400/500/600. Playfair Display rejected ("too 80s"). |
| Jun 2026 | Q3 | **Testimonials: realistic placeholders** | 3 anonymized placeholder quotes in use. Replace with real quotes when available. |
| Jun 2026 | Q4 | **Case studies: anonymized by industry + size** | No company names. Fortune 500 / sector / geography descriptions only. Zero fabrication. |
| Jun 2026 | Q4b | **Trusted By: real PNG logos** | All 9 logos in `/public/logos/`. Vistra + Boa Vista whitespace-cropped for proportion fix. |
| Jun 2026 | Q5 | **AI Readiness: 100% RG brand** | Specialist partner not named. Presented as RG Enterprise Consulting service. |
| Jun 2026 | Q6 | **Calendly confirmed** | https://calendly.com/rogerio-rgenterpriseconsulting/1-on-1-with-rogerio |
| Jun 2026 | Q7 | **Email: Ionos SMTP + Nodemailer** | SendGrid rejected. Own SMTP via Ionos. smtp.ionos.com port 587. From: leads@rgenterpriseconsulting.com → To: rogerio@rgenterpriseconsulting.com. Credentials in Firebase secrets. |
| Jun 2026 | Q8 | **LinkedIn company page** | https://www.linkedin.com/company/rg-enterprise-consulting/ |
| Jun 2026 | Q9 | **WhatsApp Business: +1 (310) 430-6698** | Keep floating button. Future: automation, bots, multi-language EN/PT/ES. |
| Jun 2026 | Q10 | **Client portal: rebuild in-house** | Firebase Auth + Firestore. Full rebuild Phase 5. |

---

## UX & Content Decisions ✅ Locked

| Date | Decision | Detail |
|------|----------|--------|
| Jun 2026 | **Lead flow: Contact form first, Calendly second** | "Contact Us" → `/contact` form. Calendly shown ONLY after form submitted on thank-you screen. Never on homepage. |
| Jun 2026 | **CTA language** | Primary: "Contact Us". Bottom CTA: "Let us solve your problem." |
| Jun 2026 | **Contact email: footer only** | `contact@rgenterpriseconsulting.com` in footer ONLY. Not on hero, not next to CTAs. |
| Jun 2026 | **Company-first branding** | Promotes RG Enterprise Consulting as boutique agency. Rogerio = "Founder & Principal Consultant" — not the headline. |
| Jun 2026 | **Social media** | LinkedIn: company page. X: @rgeconsulting. WhatsApp Business. All in footer. |
| Jun 2026 | **Trusted By ticker** | Auto-scrolling, grayscale 45% opacity, full color on hover, fade masks, 138×50px uniform slots. |
| Jun 2026 | **Hero: background slideshow** | 4 Unsplash photos fade every 5s behind navy overlay. Rogerio headshot right panel (desktop). |
| Jun 2026 | **Headshot** | `/public/photos/rogerio-headshot.jpg` — professional photo uploaded Jun 2026. |

---

## About Page ✅ Rewritten Phase 2

| Date | Decision | Detail |
|------|----------|--------|
| Jun 2026 | **Firm-first H1** | "About RG Enterprise Consulting" — not "About Rogerio Gomes" |
| Jun 2026 | **Section order** | Why We Exist → Agency Model → Founder → Multilingual → Career Timeline → CTA |
| Jun 2026 | **Founder framing** | Eyebrow: "The Experience Behind the Firm". Rogerio = proof of firm capability. |
| Jun 2026 | **Local headshot** | `/photos/rogerio-headshot.jpg` — LinkedIn CDN URL removed (expires and breaks). |
| Jun 2026 | **JSON-LD** | Organization schema with nested founder Person. Not Person schema. |

---

## Firebase Backend ✅ Fully Deployed — Phase 2

| Date | Decision | Detail |
|------|----------|--------|
| Jun 2026 | **Firebase Functions runtime** | Node.js 20 (Node 18 decommissioned Oct 2025) |
| Jun 2026 | **Email library** | Nodemailer via Ionos SMTP — no third-party service |
| Jun 2026 | **Lead storage** | Every submission saved to Firestore `leads` collection — never lose a lead |
| Jun 2026 | **Lead scoring** | 0–100 score: budget (25pts) + timeline (25pts) + company size (20pts) + job title seniority (15pts) + has website (10pts) + provided phone (5pts) |
| Jun 2026 | **Score labels** | 🔥 HOT (75+) / ⚡ WARM (50-74) / ❄️ COLD (25-49) / 👀 UNSCORED (<25) |
| Jun 2026 | **AI enrichment** | Claude API (claude-sonnet-4-5) generates company intelligence paragraph per lead — appears in notification email |
| Jun 2026 | **AI enrichment content** | Company description, recent M&A/PE activity, digital/AI initiatives, why they need RG now, key talking point for first call |
| Jun 2026 | **Notification email** | To: rogerio@rgenterpriseconsulting.com. Subject: `{label} New Lead: {service} — {name} ({company}) | Score: {n}/100` |
| Jun 2026 | **Auto-reply email** | Sent to lead confirming receipt. Includes inquiry summary + Calendly button. |
| Jun 2026 | **Public function access** | `allUsers` invoker role granted via gcloud IAM for HTTPS callable endpoint |

---

## Firebase Secrets in Production ✅

| Secret Name | Value | Purpose |
|------------|-------|---------|
| `SMTP_HOST` | smtp.ionos.com | Ionos SMTP server |
| `SMTP_PORT` | 587 | STARTTLS port |
| `SMTP_USER` | leads@rgenterpriseconsulting.com | Sender address |
| `SMTP_PASSWORD` | [secured] | Ionos mailbox password |
| `ANTHROPIC_API_KEY` | [secured] | Claude API for AI enrichment |

---

## Firestore Lead Schema ✅ Live

Collection: `leads` — fields per document:

| Field | Type | Notes |
|-------|------|-------|
| fullName | string | Required |
| jobTitle | string | For lead scoring |
| email | string | Required |
| phoneNumber | string | Optional — +5pts score |
| companyName | string | Required |
| companyWebsite | string | For AI enrichment lookup |
| industry | string | Dropdown — 10 sectors |
| companySize | string | Dropdown |
| serviceOfInterest | string | Required — 4 RG services |
| challenge | string | Open text |
| timeline | string | Dropdown |
| projectBudget | string | Dropdown |
| howFoundUs | string | Attribution |
| message | string | Optional extra text |
| status | string | new/contacted/qualified/proposal/won/lost |
| source | string | contact_form |
| score | number | 0–100 |
| scoreLabel | string | 🔥 HOT / ⚡ WARM / ❄️ COLD |
| assignedTo | string | rogerio@rgenterpriseconsulting.com |
| followUpDate | timestamp | null initially |
| notes | array | Internal notes array |
| enrichment.status | string | complete/failed |
| enrichment.summary | string | AI paragraph |
| enrichment.runAt | string | ISO timestamp |
| timestamp | timestamp | Server timestamp |

---

## Logo Assets ✅ All in `/public/logos/`

| File | Company | Type |
|------|---------|------|
| `barton.png` | The Barton Partnership | Consulting partner |
| `ust.png` | UST Global | Consulting partner |
| `smarttechlink.png` | Smart Techlink Solutions | Consulting partner |
| `vistra.png` | Vistra Group Asia | End client |
| `equifax.png` | Equifax Inc. | End client |
| `datavant.png` | Datavant Inc. | End client |
| `ciox.png` | Ciox Health | End client |
| `boavista.png` | Boa Vista Serviços | End client |
| `bizlatinhub.png` | BizLatinHub | End client |

---

## Phase Status

| Phase | Status | Notes |
|-------|--------|-------|
| Phase 1 — Brand & Design System | 🟢 Complete | All files on version-2.0 branch |
| Phase 2 — Services & Lead Generation | 🟡 In Progress | About ✅, Firebase backend ✅, Contact form TODO, Services pages TODO |
| Phase 3 — Case Studies & Portfolio | 🔴 Not Started | |
| Phase 4 — Insights Platform & SEO | 🔴 Not Started | |
| Phase 5 — Client Portal v2 | 🔴 Not Started | |
| Phase 6 — Super-Admin CMS | 🔴 Not Started | |

---

## Open Items / TODO

| Priority | Item |
|----------|------|
| 🔴 HIGH | **Contact.jsx — 3-step form** — build the frontend form that posts to the Firebase Function. Must include all new fields: jobTitle, companyWebsite, industry, companySize, challenge, timeline, howFoundUs. 3-step flow for better conversion. |
| 🔴 HIGH | **firebase.json rewrite fix** — currently routes `/api/sendContactEmail` to function. Must verify the rewrite matches the deployed function name exactly. |
| 🔴 HIGH | **Services sub-pages** — 4 pages: /services/post-merger-integration, /services/ai-readiness, /services/digital-transformation, /services/business-transformation |
| 🟡 MED | **GitHub Actions PAT `workflow` scope** — add at github.com/settings/tokens |
| 🟡 MED | **Firebase Hosting auto-deploy** — connect version-2.0 branch |
| 🟢 LOW | **reCAPTCHA v2 → v3 upgrade** — invisible reCAPTCHA on contact form |
| 🟢 LOW | **Node.js 20 deprecation** — upgrade to Node.js 22 before Oct 2026 |

---

## WhatsApp Future Roadmap
- Automated greeting message
- Lead qualification bot
- Appointment booking via WhatsApp
- Multi-language: EN / PT / ES
