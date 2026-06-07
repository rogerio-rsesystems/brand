# Decision Log
## RG Enterprise Consulting — Website & Platform Project

All locked decisions are recorded here. Claude Code reads this at the start of every session.

---

## Design & Brand ✅ All Locked

| Date | # | Decision | Detail |
|------|---|----------|--------|
| Jun 2026 | Q1 | **Colors: Navy + Gold on white** | Primary `#1B2A4A`, Accent `#C8A84B`, BG `#FFFFFF`, Alt BG `#F7F8FC`, Cream `#FDFAF3`, Dark footer `#111D33` |
| Jun 2026 | Q2 | **Fonts: Montserrat + Inter** | Headings: Montserrat 800. Body: Inter 400/500/600. Playfair Display rejected ("too 80s"). |
| Jun 2026 | Q3 | **Testimonials: realistic placeholders** | 3 anonymized placeholder quotes in use. Replace with real quotes when available. |
| Jun 2026 | Q4 | **Case studies: anonymized by industry + size** | No company names. Fortune 500 / sector / geography descriptions only. Zero fabrication. |
| Jun 2026 | Q4b | **Trusted By: real PNG logos** | All 9 logos uploaded and in `/public/logos/`. See asset list below. |
| Jun 2026 | Q5 | **AI Readiness: 100% RG brand** | Specialist partner not named. Presented as RG Enterprise Consulting service. |
| Jun 2026 | Q6 | **Calendly confirmed** | https://calendly.com/rogerio-rgenterpriseconsulting/1-on-1-with-rogerio |
| Jun 2026 | Q7 | **Email: IONOS SMTP + Nodemailer** | IONOS SMTP + Nodemailer abandoned (Phase 2 decision change). Use IONOS SMTP relay via Nodemailer in the Firebase Function. From: `leads@rgenterpriseconsulting.com` -> To: `rogerio@rgenterpriseconsulting.com` |
| Jun 2026 | Q8 | **LinkedIn company page** | https://www.linkedin.com/company/rg-enterprise-consulting/ |
| Jun 2026 | Q9 | **WhatsApp Business: +1 (310) 430-6698** | Keep floating button. Future phase: automation, bots, multi-language (EN/PT/ES) |
| Jun 2026 | Q10 | **Client portal: rebuild in-house** | Firebase Auth + Firestore. Full rebuild in Phase 5. |

---

## UX & Content Decisions ✅ Locked During Build

| Date | Decision | Detail |
|------|----------|--------|
| Jun 2026 | **Lead flow: Contact form first, Calendly second** | "Contact Us" button → `/contact` form. Calendly only shown AFTER form is submitted. No Calendly link on homepage. |
| Jun 2026 | **CTA language** | Primary: "Contact Us". Bottom CTA: "Let us solve your problem." NOT "Send us a message" or "Schedule a Call" as primary. |
| Jun 2026 | **Contact email: footer only** | `contact@rgenterpriseconsulting.com` shown in footer only. Not on hero, not next to CTA buttons, not on About page. |
| Jun 2026 | **Company-first branding** | Website promotes RG Enterprise Consulting as a boutique agency. Rogerio is "Founder & Principal Consultant" — not the headline. Personal credentials (Wharton, GT, Stanford) belong on About page only. |
| Jun 2026 | **Social media on website** | LinkedIn: company page. X/Twitter: @rgeconsulting. WhatsApp: Business number. All in footer. |
| Jun 2026 | **Trusted By ticker** | Auto-scrolling infinite ticker. Grayscale 45% opacity, full color on hover. Fade masks on edges. Uniform 138×50px slots for all logos. |
| Jun 2026 | **Hero: background slideshow** | 4 Unsplash office/business photos fade in/out every 5s behind navy overlay. Slide dot indicators. Rogerio headshot on right panel (desktop only). |
| Jun 2026 | **Headshot** | File: `/public/photos/rogerio-headshot.jpg` — professional photo uploaded by Rogerio (Jun 2026). |

---

## About Page Decisions ✅ Locked — Phase 2 Rewrite (Jun 2026)

| Date | Decision | Detail |
|------|----------|--------|
| Jun 2026 | **Page title: firm-first** | `<title>` is "About RG Enterprise Consulting — Boutique Management Consulting". NOT "About Rogerio Gomes". |
| Jun 2026 | **H1: firm-first** | H1 reads "About RG Enterprise Consulting". No personal name in the hero heading. |
| Jun 2026 | **Section order** | Why We Exist → Agency Model → Founder → Multilingual → Career Timeline → CTA. Agency model promoted above founder bio. |
| Jun 2026 | **Founder section framing** | Eyebrow: "The Experience Behind the Firm". Rogerio is positioned as proof of firm capability, not the subject of the page. |
| Jun 2026 | **Personal statement included** | Authentic quote block from Rogerio: "I built this firm because too many organizations get sold strategy they can't execute..." Required by BRD Section 5.1.4. |
| Jun 2026 | **Multilingual section** | Dedicated navy callout banner for EN / PT / ES / IT. BRD requirement. Positioned between Founder and Timeline sections. |
| Jun 2026 | **Career timeline reframed** | Section eyebrow: "The Track Record". Heading: "15+ Years of Enterprise Delivery". Subtext: "The depth of experience that powers every RG Enterprise Consulting engagement." |
| Jun 2026 | **Photo: local file only** | `src="/photos/rogerio-headshot.jpg"` — the LinkedIn CDN URL was removed. LinkedIn CDN URLs expire and can break. |
| Jun 2026 | **JSON-LD schema** | Changed from `Person` to `Organization` with nested `founder: Person`. Matches BRD company-first positioning. |
| Jun 2026 | **Contact card simplified** | Removed email from the under-photo card (footer-only rule). Kept: name, title, location, LinkedIn link. |
| Jun 2026 | **CTA: company-centric** | Headline: "Ready to Start Your Transformation?" Subtext: "We work with a select number of clients at a time — let's see if we're the right fit." Primary button: "Contact Us" → /contact (NOT Calendly as primary). |

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

Note: Vistra and Boa Vista logos were whitespace-cropped in Jun 2026 to fix proportion issues.

---

## Phase Status

| Phase | Status | Notes |
|-------|--------|-------|
| Phase 1 — Brand & Design System | 🟢 Complete | All files pushed to `version-2.0` branch |
| Phase 2 — Services & Lead Generation | 🟡 In Progress | About page ✅ done. Contact form fix + services pages + enriched form still TODO. |
| Phase 3 — Case Studies & Portfolio | 🔴 Not Started | |
| Phase 4 — Insights Platform & SEO | 🔴 Not Started | |
| Phase 5 — Client Portal v2 | 🔴 Not Started | |
| Phase 6 — Super-Admin CMS | 🔴 Not Started | |

---

## Open Items / TODO

| Priority | Item | Added |
|----------|------|-------|
| 🔴 CRITICAL | **Contact form dead endpoint** — posts to `/api/sendContactEmail`, never wired. ALL LEADS LOST. | Phase 1 |
| (red)CRITICAL | **Firebase Functions not deployed** -- IONOS SMTP + Nodemailer integration not built. | Phase 1 |
| 🔴 HIGH | **Services sub-pages** — 4 pages: /services/post-merger-integration, /services/ai-readiness, /services/digital-transformation, /services/business-transformation | Phase 1 |
| 🔴 HIGH | **Enriched lead form** — company size, timeline, challenge, how they found us, lead scoring | Phase 1 |
| 🟡 MED | **GitHub Actions PAT needs `workflow` scope** — add at github.com/settings/tokens | Phase 1 |
| 🟡 MED | **Firebase Hosting auto-deploy** — connect version-2.0 branch | Phase 1 |
| 🟡 MED | **Calendly post-form** — show Calendly only on thank-you page after form submit | Phase 1 |
| 🟢 LOW | **reCAPTCHA v2 → v3 upgrade** — invisible reCAPTCHA on contact form | Phase 1 |

### ✅ Resolved Open Items
| Item | Resolved | How |
|------|----------|-----|
| About page rewrite — company-first | ✅ Phase 2 Session 2 | Full rewrite committed to version-2.0 (commit 8f83c70) |
| LinkedIn CDN photo in About.jsx | ✅ Phase 2 Session 2 | Changed to `/photos/rogerio-headshot.jpg` |

---

## WhatsApp Future Roadmap
- Automated greeting message
- Lead qualification bot
- Appointment booking via WhatsApp
- Multi-language: EN / PT / ES