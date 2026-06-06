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
| Jun 2026 | Q7 | **Email: SendGrid** | From: `leads@rgenterpriseconsulting.com` → To: `rogerio@rgenterpriseconsulting.com` |
| Jun 2026 | Q8 | **LinkedIn company page** | https://www.linkedin.com/company/rg-enterprise-consulting/ |
| Jun 2026 | Q9 | **WhatsApp Business: +1 (310) 430-6698** | Keep floating button. Future phase: automation, bots, multi-language (EN/PT/ES) |
| Jun 2026 | Q10 | **Client portal: rebuild in-house** | Firebase Auth + Firestore. Full rebuild in Phase 5. |

---

## UX & Content Decisions ✅ Locked During Build

| Date | Decision | Detail |
|------|----------|--------|
| Jun 2026 | **Lead flow: Contact form first, Calendly second** | "Contact Us" button → `/contact` form. Calendly only shown AFTER form is submitted. No Calendly link on homepage. |
| Jun 2026 | **CTA language** | Primary: "Contact Us". Bottom CTA: "Let us solve your problem." NOT "Send us a message" or "Schedule a Call" as primary. |
| Jun 2026 | **Contact email: footer only** | `contact@rgenterpriseconsulting.com` shown in footer only. Not on hero, not next to CTA buttons. |
| Jun 2026 | **Company-first branding** | Website promotes RG Enterprise Consulting as a boutique agency. Rogerio is "Founder & Principal Consultant" — not the headline. Personal credentials (Wharton, GT, Stanford) belong on About page only. |
| Jun 2026 | **About page: company-first** | About page needs to lead with the firm, not Rogerio's resume. Career timeline and credentials in supporting role. TODO: still needs rewrite. |
| Jun 2026 | **Social media on website** | LinkedIn: company page. X/Twitter: @rgeconsulting. WhatsApp: Business number. All in footer. |
| Jun 2026 | **Trusted By ticker** | Auto-scrolling infinite ticker. Grayscale 45% opacity, full color on hover. Fade masks on edges. Uniform 138×50px slots for all logos. |
| Jun 2026 | **Hero: background slideshow** | 4 Unsplash office/business photos fade in/out every 5s behind navy overlay. Slide dot indicators. Rogerio headshot on right panel (desktop only). |
| Jun 2026 | **Headshot** | File: `/public/photos/rogerio-headshot.jpg` — professional photo uploaded by Rogerio (Jun 2026). |

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
| Phase 2 — Services & Lead Generation | 🔴 Not Started | Next priority |
| Phase 3 — Case Studies & Portfolio | 🔴 Not Started | |
| Phase 4 — Insights Platform & SEO | 🔴 Not Started | |
| Phase 5 — Client Portal v2 | 🔴 Not Started | |
| Phase 6 — Super-Admin CMS | 🔴 Not Started | |

---

## Open Items / TODO

| Priority | Item |
|----------|------|
| 🔴 HIGH | About page needs rewrite — currently too resume-focused. Must lead with the company, not Rogerio's biography. |
| 🔴 HIGH | Contact form is still broken (posts to dead endpoint) — P0 bug, all leads lost. Fix in Phase 2. |
| 🔴 HIGH | Firebase Functions never deployed — SendGrid integration not built yet. Fix in Phase 2. |
| 🔴 HIGH | GitHub Actions workflow blocked — needs `workflow` scope added to PAT token. |
| 🟡 MED | Firebase hosting not yet connected to auto-deploy from `version-2.0` branch. Manual deploy needed. |
| 🟡 MED | Services pages — 4 individual sub-pages not built yet. |
| 🟡 MED | Boa Vista logo uploaded as `boa_vistra.png` — renamed to `boavista.png` in repo. |
| 🟢 LOW | Rogerio headshot: LinkedIn CDN URL still used in About.jsx — should reference `/photos/rogerio-headshot.jpg` locally. |
| 🟢 LOW | reCAPTCHA: upgrade from v2 checkbox to v3 invisible (Phase 2). |

---

## WhatsApp Future Roadmap
- Automated greeting message
- Lead qualification bot
- Appointment booking via WhatsApp
- Multi-language: EN / PT / ES
