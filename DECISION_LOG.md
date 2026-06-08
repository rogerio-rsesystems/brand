# Decision Log
## RG Enterprise Consulting — Website & Platform Project

All locked decisions are recorded here. Claude reads this at the start of every session.
Last updated: June 8, 2026

---

## Design & Brand ✅ All Locked

| Date | # | Decision | Detail |
|------|---|----------|--------|
| Jun 2026 | Q1 | **Colors: Navy + Gold on white** | Primary `#1B2A4A`, Accent `#C8A84B`, BG `#FFFFFF`, Alt BG `#F7F8FC`, Cream `#FDFAF3`, Dark footer `#111D33` |
| Jun 2026 | Q2 | **Fonts: Montserrat + Inter** | Headings: Montserrat 800. Body: Inter 400/500/600. Playfair Display rejected ("too 80s"). |
| Jun 2026 | Q3 | **Testimonials: realistic placeholders** | 3 anonymized placeholder quotes in use. Replace with real quotes when available. |
| Jun 2026 | Q4 | **Case studies: anonymized by industry + size** | No company names. Fortune 500 / sector / geography only. Zero fabrication. |
| Jun 2026 | Q4b | **Trusted By: real PNG logos** | All 9 logos in `/public/logos/`. Vistra + Boa Vista whitespace-cropped for proportion fix. |
| Jun 2026 | Q5 | **AI Readiness: 100% RG brand** | Specialist partner not named. Presented as RG Enterprise Consulting service. |
| Jun 2026 | Q6 | **Calendly confirmed** | https://calendly.com/rogerio-rgenterpriseconsulting/1-on-1-with-rogerio |
| Jun 2026 | Q7 | **Email: Ionos SMTP + Nodemailer** | SendGrid rejected (Twilio acquisition, unreliable free tier). Own SMTP via Ionos. smtp.ionos.com port 587. From: leads@rgenterpriseconsulting.com → To: rogerio@rgenterpriseconsulting.com. Credentials in Firebase secrets. |
| Jun 2026 | Q8 | **LinkedIn company page** | https://www.linkedin.com/company/rg-enterprise-consulting/ |
| Jun 2026 | Q9 | **WhatsApp Business: +1 (310) 430-6698** | Keep floating button. Future: automation, bots, multi-language EN/PT/ES. |
| Jun 2026 | Q10 | **Client portal: rebuild in-house** | Firebase Auth + Firestore. Full rebuild Phase 5. |

---

## Logo Decisions ✅ Locked

| Date | Decision | Detail |
|------|----------|--------|
| Jun 2026 | **Navbar + Footer: white transparent logo** | `logo-white-transparent.png` — programmatically generated from `logo.png.png` by inverting black pixels to white while preserving transparency and anti-aliasing. `logo white.png` rejected (solid white background box). |
| Jun 2026 | **Light backgrounds: black transparent logo** | `logo.png.png` — 712x560px, transparent background, black logo. Used wherever background is white or light. |
| Jun 2026 | **logo white.png: DO NOT USE** | Has solid white background (0% transparency). Looks terrible on any non-white background. |
| Jun 2026 | **Ticker: uniform 138×50px slots** | All 9 company logos display in uniform slots. Vistra and Boa Vista whitespace-cropped June 2026 for proportion fix. |

---

## UX & Content Decisions ✅ Locked

| Date | Decision | Detail |
|------|----------|--------|
| Jun 2026 | **Lead flow: form first, Calendly second** | "Contact Us" → `/contact` form. Calendly shown ONLY after form submitted on thank-you screen. Never on homepage. |
| Jun 2026 | **CTA language** | Primary: "Contact Us". Bottom CTA: "Let us solve your problem." |
| Jun 2026 | **Contact email: footer only** | `contact@rgenterpriseconsulting.com` in footer ONLY. Not on hero, not next to CTAs. |
| Jun 2026 | **Company-first branding** | Promotes RG Enterprise Consulting as boutique agency. Rogerio = "Founder & Principal Consultant" — not the headline. |
| Jun 2026 | **Social media** | LinkedIn: company page. X: @rgeconsulting. WhatsApp Business. All in footer. |
| Jun 2026 | **Trusted By ticker** | Auto-scrolling, grayscale 45% opacity, full color on hover, fade masks, 138×50px uniform slots. |
| Jun 2026 | **Hero: background slideshow** | 4 Unsplash photos fade every 5s behind navy overlay. Rogerio headshot right panel (desktop only). |
| Jun 2026 | **Headshot** | `/public/photos/rogerio-headshot.jpg` — professional executive photo uploaded June 2026. |
| Jun 2026 | **"What Happens Next" step 02** | "A member of our team reaches out to schedule a discovery call" — NOT "Rogerio personally." Company-first, institutional, scalable language. |

---

## About Page ✅ Rewritten Phase 2

| Date | Decision | Detail |
|------|----------|--------|
| Jun 2026 | **Firm-first H1** | "About RG Enterprise Consulting" — not "About Rogerio Gomes" |
| Jun 2026 | **Section order** | Why We Exist → Agency Model → Founder → Multilingual → Career Timeline → CTA |
| Jun 2026 | **Founder framing** | Eyebrow: "The Experience Behind the Firm". Rogerio = proof of firm capability, not primary subject. |
| Jun 2026 | **Local headshot** | `/photos/rogerio-headshot.jpg` — LinkedIn CDN URL removed (expires and breaks). |

---

## Services Architecture ✅ Phase 2 Complete

| Date | Decision | Detail |
|------|----------|--------|
| Jun 2026 | **5 service lines** | PMI, AI Readiness, Digital Transformation, Business Transformation, **Project Management** (added Phase 2). |
| Jun 2026 | **Project Management as 5th service** | Covers full delivery spectrum: PMO Design & Implementation, Program Management, Portfolio Management, Project Management, PMO Rescue & Recovery, Project Coordination. Reflects Rogerio's core career expertise across 9 industries and 3 continents. |
| Jun 2026 | **Services overview page** | `/services` — 5 service cards with icon, tagline, description, 3 bullets, "Explore this service" CTA. |
| Jun 2026 | **PMI sub-page** | Expanded: Day-1/100/Post-100 framework, 3 synergy types (cost/revenue/strategic), cultural integration (absorption/preservation/hybrid models), carve-out & TSA section, accordion FAQ, stats strip. |
| Jun 2026 | **AI Readiness sub-page** | Expanded: 2025/2026 research stats (7% readiness, 42% project abandonment, 80% failure), 4 real-world industry examples, 5-level AI Maturity Model with color coding, accordion FAQ. |
| Jun 2026 | **Digital Transformation sub-page** | Challenge/solution, 8 service checklist, case study ($10M+ IT portfolio), 4 FAQs. |
| Jun 2026 | **Business Transformation sub-page** | Challenge/solution, 8 service checklist, case study ($6M savings, 70+ initiatives), 4 FAQs. |
| Jun 2026 | **Project Management sub-page** | 6 capability levels, 4 delivery frameworks (Waterfall/Agile/Hybrid/SAFe), 9 industries, case study ($6M savings, 70+ initiatives), 5 accordion FAQs. |
| Jun 2026 | **All sub-pages structure** | Back arrow → /services. Eyebrow tag. Hero + stats. Challenge vs. approach split. What's Included checklist. Real anonymized case study with metrics. Accordion FAQ. Navy CTA to /contact. |

---

## Firebase Backend ✅ Fully Deployed Phase 2

| Date | Decision | Detail |
|------|----------|--------|
| Jun 2026 | **Firebase Functions runtime** | Node.js 20 (upgrade to 22 before Oct 2026 deprecation) |
| Jun 2026 | **Email library** | Nodemailer via Ionos SMTP — no third-party service |
| Jun 2026 | **Lead storage** | Every submission saved to Firestore `leads` collection — never lose a lead even if email fails |
| Jun 2026 | **Opportunity ID** | Sequential human-readable format: RGE-YYYY-NNNN. Firestore atomic transaction counter at `meta/leadCounter`. Resets annually. Appears in email subject, notification body, client auto-reply, thank-you screen. |
| Jun 2026 | **Lead scoring** | 0-100: budget (25pts) + timeline (25pts) + company size (20pts) + job title seniority (15pts) + has website (10pts) + phone provided (5pts) |
| Jun 2026 | **Score labels** | 🔥 HOT (75+) / ⚡ WARM (50-74) / ❄️ COLD (25-49) / 👀 UNSCORED (<25) |
| Jun 2026 | **AI enrichment** | Claude API (claude-sonnet-4-5) generates 150-200 word company intelligence paragraph per lead |
| Jun 2026 | **Notification email subject** | `{OpportunityId} \| {label} New Lead: {service} — {name} ({company}) \| Score: {n}/100` |
| Jun 2026 | **Auto-reply to client** | Sent to lead with inquiry summary, Opportunity ID, and Calendly booking button |
| Jun 2026 | **Function deployed** | URL: https://us-central1-rgenterpriseconsulting-d90fa.cloudfunctions.net/sendContactEmail |
| Jun 2026 | **Public access** | allUsers invoker role granted via gcloud IAM |

---

## Firebase Secrets in Production ✅

| Secret | Purpose |
|--------|---------|
| `SMTP_HOST` | smtp.ionos.com |
| `SMTP_PORT` | 587 |
| `SMTP_USER` | leads@rgenterpriseconsulting.com |
| `SMTP_PASSWORD` | [secured] — Ionos mailbox password |
| `ANTHROPIC_API_KEY` | [secured] — Claude API for AI enrichment |
| `RECAPTCHA_SECRET` | [secured] — Google reCAPTCHA v3 secret |

---

## Contact Form ✅ Complete Phase 2

| Date | Decision | Detail |
|------|----------|--------|
| Jun 2026 | **3-step form flow** | Step 1: Who are you (name, title, email, phone, company, website). Step 2: What do you need (service, industry, size, challenge, timeline, budget). Step 3: Final (how found us, optional notes, summary card, submit). |
| Jun 2026 | **Form endpoint** | Posts directly to Firebase Function HTTPS endpoint. No /api/ proxy. |
| Jun 2026 | **Thank-you screen** | Shows Opportunity ID (RGE-YYYY-NNNN) in gold. Calendly button appears here ONLY. "Submit another inquiry" link. |
| Jun 2026 | **End-to-end tested** | RGE-2026-0001 through 0003 confirmed. Email received, AI enrichment generated, Firestore saved. |

---

## Security Stack ✅ Phase 2

| Date | Decision | Detail |
|------|----------|--------|
| Jun 2026 | **reCAPTCHA v3** | Invisible, score-based. Site Key: `6LcfqhItAAAAACmRAnAmBDoklGo77ohebIbd3eJy`. Threshold: 0.4. No token = blocked. Approved domains: rgenterpriseconsulting.com, www, rgenterpriseconsulting-d90fa.web.app, localhost. |
| Jun 2026 | **Rate limiting** | 5 submissions per IP per hour. Firestore-backed atomic transaction. Resets after 1 hour. Fails open. |
| Jun 2026 | **Firestore rules** | leads: no public access (Functions only). meta: completely locked. users: own profile only. projects/documents: assigned client only. articles: published readable, write admin-only. Default: deny all. |
| Jun 2026 | **HTTP security headers** | X-Frame-Options: DENY. HSTS 1 year. X-Content-Type-Options: nosniff. Referrer-Policy: strict-origin-when-cross-origin. Permissions-Policy: camera/mic/geo/payment disabled. CSP whitelist. |
| Jun 2026 | **reCAPTCHA badge position** | Repositioned to `bottom: 90px` on contact page via CSS useEffect to avoid overlapping WhatsApp button. |
| Jun 2026 | **No Cloudflare for now** | DNS stays on Ionos. Firebase Hosting = Google-level DDoS protection. Revisit post-launch. |

---

## Competitive Intelligence ✅ Completed June 2026

| Date | Decision | Detail |
|------|----------|--------|
| Jun 2026 | **Competitor analysis completed** | 25-firm report produced covering direct competitors, benchmarks, and partners. Stored as `RGE_Competitor_Partner_Analysis_2026_v2.docx` in project files. |
| Jun 2026 | **Key competitive finding** | E78 Partners (acquired GPMIP USA 2024, PE-backed, Inc. 5000 ×7) is the fastest-escalating competitive threat. Monitor closely. |
| Jun 2026 | **RG differentiated position** | Technology-enabled PMI + multilingual Latin America delivery + boutique senior access. No competitor in the 25-firm set combines all three. |
| Jun 2026 | **Priority referral channels** | The Barton Partnership (existing), CrossCountry, Accordion, Riveron, SolomonEdwards — all serve PE CFO layer and refer operational PMI work. |

---

## Phase Status ✅ Current as of June 8, 2026

| Phase | Status | Notes |
|-------|--------|-------|
| Phase 1 — Brand & Design System | 🟢 Complete | Navbar, Footer, Home v3, About v2 (company-first), all logos, headshot, design tokens. |
| Phase 2 — Services & Lead Generation | 🟢 Complete | About ✅, Firebase backend ✅, Contact form ✅, Security ✅, Services overview ✅, 5 service sub-pages ✅ |
| Phase 3 — Case Studies & Portfolio | 🔴 Not Started | Next priority |
| Phase 4 — Insights Platform & SEO | 🔴 Not Started | |
| Phase 5 — Client Portal v2 | 🔴 Not Started | |
| Phase 6 — Super-Admin CMS | 🔴 Not Started | |

---

## Open Items / Pending (Phase 3+)

| Priority | Item |
|----------|------|
| 🔴 HIGH | **DO NOT deploy hosting yet** — site not ready for public. Run `npm run build && firebase deploy --only hosting` only when all pages complete and reviewed. |
| 🔴 HIGH | **Phase 3: Case Studies** — 3-4 anonymized case study pages. Portfolio page v2. |
| 🟡 MED | **GitHub Actions PAT `workflow` scope** — add at github.com/settings/tokens for CI/CD auto-deploy |
| 🟡 MED | **Firebase Hosting auto-deploy** — connect version-2.0 branch once site is ready |
| 🟡 MED | **Node.js 20 deprecation** — upgrade Firebase Functions to Node.js 22 before Oct 2026 |
| 🟡 MED | **WhatsApp floating button** — review v1.4 component, update to v2.0 standards |
| 🟢 LOW | **Firebase App Check enforcement** — enable after site goes live and traffic baseline established |
| 🟢 LOW | **Testimonials** — replace 3 placeholder quotes with real client quotes when available |
| 🟢 LOW | **Smart Techlink logo** — not uploaded yet. Using SVG placeholder. Upload PNG when available. |

---

## WhatsApp Future Roadmap
- Automated greeting message
- Lead qualification bot
- Appointment booking via WhatsApp
- Multi-language: EN / PT / ES

---

## Services Pages ✅ Complete — Phase 2 (June 2026)

| Date | Decision | Detail |
|------|----------|--------|
| Jun 2026 | **5th service line added: Project Management** | PMO design/implementation, program management, portfolio management, project delivery, rescue/recovery, coordination. Full-page at /services/project-management. |
| Jun 2026 | **Services overview page** | /services — 5-card grid, gold hover animation, stats bar, CTA. Each card shows icon, tagline, 3 bullets, "Explore" link. |
| Jun 2026 | **PMI sub-page expanded** | Added: Day-1/100 framework (4-phase visual), 3 synergy types (cost/revenue/strategic), cultural integration section (3 models: absorption/preservation/hybrid), carve-out & TSA section, accordion FAQ. 14 service checklist items. |
| Jun 2026 | **AI Readiness sub-page expanded** | Added: 3 stats from 2025/2026 research (7% enterprise AI-ready, 42% abandon AI initiatives, 80% fail), 4 real-world industry examples (manufacturer, healthcare, PE-backed fintech, global logistics), 5-level AI Maturity Model with color coding. |
| Jun 2026 | **Digital Transformation sub-page** | Challenge/solution split, 8-item checklist, case study ($10M+ IT portfolio), FAQ accordion. CTA: "Have a transformation program in flight?" |
| Jun 2026 | **Business Transformation sub-page** | Challenge/solution split, 8-item checklist, case study ($6M savings, 70+ initiatives), FAQ accordion. CTA: "At an inflection point?" |
| Jun 2026 | **Project Management sub-page** | 6 capability levels (PMO → coordination), 4 delivery frameworks (Waterfall/Agile/Hybrid/SAFe), 9 industry tags, case study ($6M savings, 70+ initiatives), FAQ accordion. |
| Jun 2026 | **FAQ style: accordion** | All service sub-pages use interactive accordion FAQ (useState) — collapsed by default, gold chevron rotates on open. |
| Jun 2026 | **Service page structure** | All pages follow: navy hero (with back arrow, eyebrow, stats strip) → challenge/solution split → extra content sections → what's included checklist → case study → FAQ accordion → navy CTA. |
| Jun 2026 | **Logo fix** | `logo white.png` (solid background) removed from Navbar and Footer. Replaced with programmatically-generated `logo-white-transparent.png` (white pixels, transparent background, same anti-aliasing). `logo.png.png` (black transparent) used for light backgrounds. `logo white.png` — DO NOT USE. |
| Jun 2026 | **Services routing** | All 5 service sub-pages routed in App.jsx: /services/post-merger-integration, /services/ai-readiness, /services/digital-transformation, /services/business-transformation, /services/project-management |

---

## Updated Phase Status — June 8, 2026

| Phase | Status | Notes |
|-------|--------|-------|
| Phase 1 — Brand & Design System | 🟢 Complete | Navbar, Footer, Home v3, About v2 (company-first), all logos fixed, headshot, design tokens. |
| Phase 2 — Services & Lead Generation | 🟢 Complete | About ✅, Firebase backend ✅, Contact form (3-step) ✅, Security (reCAPTCHA/rate limiting/Firestore rules/HTTP headers) ✅, Services overview ✅, 5 service sub-pages ✅ |
| Phase 3 — Case Studies & Portfolio | 🔴 Not Started | **Next priority** — 3-4 anonymized case study pages + Portfolio v2 |
| Phase 4 — Insights Platform & SEO | 🔴 Not Started | Blog/articles section, SEO meta tags |
| Phase 5 — Client Portal v2 | 🔴 Not Started | Rebuild in-house |
| Phase 6 — Super-Admin CMS | 🔴 Not Started | |

---

## Complete File Inventory — version-2.0 branch (June 8, 2026)

### Core Config
- `tailwind.config.js` — design token system
- `src/theme.js` — central content file: 5 services, contact info, stats, trustedBy logos, credentials, career timeline
- `src/index.css` — Google Fonts (Montserrat + Inter), white base, utility classes
- `src/main.jsx` — HelmetProvider wrapper
- `src/App.jsx` — all routes including 5 service sub-routes
- `firebase.json` — security headers, node20, rewrites
- `firestore.rules` — full lockdown rules (deployed)
- `functions/index.js` — Firebase Function (all features, deployed)

### Components
- `src/components/Navbar.jsx` — navy, white transparent logo, gold CTA→/contact, mobile overlay
- `src/components/Footer.jsx` — dark navy, LinkedIn/X/WhatsApp, contact@ footer-only

### Pages
- `src/pages/Home.jsx` — hero slideshow, stats, ticker, services grid, case teasers, testimonials, CTA
- `src/pages/About.jsx` — company-first, firm leads, Rogerio as proof, career timeline
- `src/pages/Contact.jsx` — 3-step form, reCAPTCHA v3, rate limiting, Opportunity ID on thank-you, Calendly post-form only
- `src/pages/Services.jsx` — 5-card overview grid

### Service Sub-Pages
- `src/pages/services/PostMergerIntegration.jsx` — expanded: culture, carve-outs, TSA, synergy types, Day-1/100 framework
- `src/pages/services/AIReadiness.jsx` — expanded: real-world examples, AI maturity model, 2025/2026 stats
- `src/pages/services/DigitalTransformation.jsx` — cloud migrations, ERP/CRM/HRIS, case study
- `src/pages/services/BusinessTransformation.jsx` — operating model, strategy, case study
- `src/pages/services/ProjectManagement.jsx` — PMO/Program/Portfolio/Project/Rescue/Coordination — NEW

### Public Assets
- `public/logo.png.png` — black transparent logo (light backgrounds)
- `public/logo-white-transparent.png` — white transparent logo (dark navbar/footer)
- `public/photos/rogerio-headshot.jpg` — professional headshot
- `public/logos/*.png` — 9 Trusted By logos (Barton, UST, SmartTechlink, Vistra, Equifax, Datavant, Ciox, BoaVista, BizLatinHub)
