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
| Phase 4 — Visual Identity (Higgsfield AI) | 🔴 Not Started | Corporate imagery, hero animations, service section visuals |
| Phase 5 — Insights Platform & SEO | 🔴 Not Started | Blog/articles, SEO meta tags, structured data |
| Phase 6 — Client Portal v2 | 🔴 Not Started | Rebuild in-house |
| Phase 7 — Super-Admin CMS | 🔴 Not Started | |

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
| Phase 4 — Visual Identity (Higgsfield AI) | 🔴 Not Started | Corporate imagery, hero animations, service section visuals — Higgsfield AI platform |
| Phase 5 — Insights Platform & SEO | 🔴 Not Started | Blog/articles section, SEO meta tags, structured data |
| Phase 6 — Client Portal v2 | 🔴 Not Started | Rebuild in-house |
| Phase 7 — Super-Admin CMS | 🔴 Not Started | |

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

---

## Phase 4 — Visual Identity & Higgsfield AI Production ✏️ Planned

### Decision: Use Higgsfield AI for Corporate Visual Production

| Date | Decision | Detail |
|------|----------|--------|
| Jun 2026 | **Platform: Higgsfield AI** | Selected for corporate animation and image generation. Higgsfield specializes in cinematic video generation, motion effects, and professional corporate imagery — appropriate for a boutique consulting brand. |
| Jun 2026 | **Goal** | Elevate the site from professional text-heavy to visually compelling. Corporate imagery and subtle animations will differentiate RG from competitors whose sites are primarily text and stock photography. |
| Jun 2026 | **Tone** | Executive. Cinematic. Navy + Gold color grading to match brand. No generic office stock. Think: boardrooms, data visualizations, integration war rooms, global deal maps. |
| Jun 2026 | **Hero section priority** | The Hero slideshow is the highest-priority visual upgrade. Currently uses 4 Unsplash stock photos with navy overlay. Replace with Higgsfield-generated branded cinematic images or subtle looping animations. |
| Jun 2026 | **Services sections priority** | Each service sub-page hero should have a bespoke visual — PMI should feel different from AI Readiness should feel different from Project Management. |

### Higgsfield Setup Steps (Pre-Production Checklist)

| Step | Action | Notes |
|------|--------|-------|
| 1 | **Create Higgsfield account** | https://higgsfield.ai — sign up with professional email |
| 2 | **Select plan** | Review Pro vs. Studio tier — Studio recommended for commercial use and full resolution exports |
| 3 | **Download brand kit** | From brand repo: `logo.png.png`, `logo-white-transparent.png`, Montserrat + Inter fonts, hex values: Navy `#1B2A4A`, Gold `#C8A84B` |
| 4 | **Headshot prep** | Export Rogerio headshot at high resolution for any Higgsfield portrait animations |
| 5 | **Prompt library** | Build a set of reusable prompt templates (see planned asset list below) before starting generation to ensure visual consistency |
| 6 | **Color grading brief** | All outputs: cool dark tones, navy shadows, gold accent light sources. Avoid warm/orange tones. Cinematic widescreen (16:9). |
| 7 | **Export format** | Video: MP4 (H.264), max 10 seconds for web. Images: PNG or WebP, minimum 1920×1080. |
| 8 | **Asset naming** | Follow pattern: `hf-[section]-[variant]-[vN].mp4` e.g. `hf-hero-boardroom-v1.mp4`, `hf-services-pmi-v1.png` |

### Planned Asset List

#### Hero Section (Highest Priority)
| Asset ID | Description | Format | Placement |
|----------|-------------|--------|-----------|
| `hf-hero-01` | Executive boardroom, dark navy atmosphere, subtle light movement | MP4 loop or PNG | Hero slide 1 |
| `hf-hero-02` | Global deal map / network of connected nodes, gold accent lines | MP4 loop or PNG | Hero slide 2 |
| `hf-hero-03` | Data transformation visualization — fragmented data becoming unified | MP4 loop or PNG | Hero slide 3 |
| `hf-hero-04` | Corporate handshake / deal close moment, cinematic framing | PNG | Hero slide 4 |

#### Services Sub-Pages (Each page gets a unique hero visual)
| Asset ID | Service | Description | Format |
|----------|---------|-------------|--------|
| `hf-svc-pmi` | Post-Merger Integration | Two org charts merging into one, Day 1 countdown board | PNG or MP4 |
| `hf-svc-ai` | AI Readiness | Data silos breaking apart and flowing into a unified stream | PNG or MP4 |
| `hf-svc-digital` | Digital Transformation | Legacy stack dissolving into cloud architecture | PNG or MP4 |
| `hf-svc-bizxform` | Business Transformation | Strategy pyramid being built, executive team in silhouette | PNG |
| `hf-svc-pm` | Project Management | Gantt chart / program dashboard, controlled execution energy | PNG |

#### About Page
| Asset ID | Description | Format | Placement |
|----------|-------------|--------|-----------|
| `hf-about-01` | Rogerio headshot animated — subtle professional motion effect | MP4 | About hero panel |
| `hf-about-02` | Global map with Latin America + North America highlighted in gold | PNG | About geography section |

#### General / Reusable
| Asset ID | Description | Format | Placement |
|----------|-------------|--------|-----------|
| `hf-og-default` | Default Open Graph image — navy bg, gold logo, tagline | PNG 1200×630 | og:image meta tag |
| `hf-og-services` | Services OG image | PNG 1200×630 | Services page og:image |
| `hf-og-contact` | Contact page OG image | PNG 1200×630 | Contact page og:image |

### Implementation Notes for Claude (when Phase 4 begins)

- All Higgsfield assets stored in `/public/media/` folder in the website repo
- Hero slideshow in `Home.jsx` currently uses `backgroundImage: url(...)` inline CSS — update to reference `/media/hf-hero-*.png` or convert to `<video autoPlay muted loop playsInline>` for MP4 animations
- Service sub-page heroes currently use CSS `background: #1B2A4A` — update to use `hf-svc-*` assets as background images with the existing navy overlay preserved (opacity ~0.7 so text remains legible)
- About.jsx headshot section: if using animated headshot, swap `<img>` for `<video autoPlay muted loop playsInline>` with poster fallback to static headshot
- OG images: update `<meta property="og:image">` in each page's `<Helmet>` block
- Performance: all video assets must be compressed to under 5MB for web. Images: use WebP format with PNG fallback.
- Lazy loading: service sub-page hero images should use `loading="lazy"` to not block initial page render

### Phase 4 Exit Criteria (Definition of Done)

- [ ] Higgsfield account created and plan selected
- [ ] All hero assets (hf-hero-01 through 04) generated, approved, and committed
- [ ] All 5 service page visuals generated and deployed
- [ ] About page animated headshot or geography visual in place
- [ ] 3 OG images generated (default, services, contact)
- [ ] All assets compressed, WebP-converted, and committed to `/public/media/`
- [ ] Mobile performance verified — no layout shift, no loading delay
- [ ] Rogerio final visual approval before Phase 5

---

## Known Issues — Logged June 9, 2026

| # | Issue | Priority | Phase |
|---|-------|----------|-------|
| 1 | **Mobile responsiveness broken** | 🔴 HIGH | Pre-launch — fix before go-live. All pages need mobile CSS review. Grid layouts collapse incorrectly on narrow viewports (<768px). Affects all pages built in Phase 2 and 3. |
| 2 | **Client portal dark theme** | 🟡 MED | Phase 6 (Client Portal rebuild). Login page, ClientDashboard, ClientProjects, DocumentPortal all use old dark gray Tailwind theme from v1.4. Rebuild to Navy+Gold brand system when portal is rebuilt in Phase 6. |
| 3 | **Admin portal dark theme** | 🟡 MED | Phase 6. AdminDashboard and AdminProjects use old dark Tailwind theme. AdminInsights was built new (Navy+Gold). Standardize all admin pages to match AdminInsights style when portal is rebuilt. |
| 4 | **Firestore articles permissions** | 🔴 FIXED | Firestore rules required `users_roles` admin document before allowing article writes. Fixed June 9 — rule now also checks `request.auth.token.email` directly for admin emails. Deploy with `firebase deploy --only firestore:rules`. |

---

## Phase 3 — Complete ✅ June 9, 2026

### Case Studies / Portfolio

| Decision | Detail |
|----------|--------|
| **Anonymized case studies** | No client names. Described by industry + size + geography only. All metrics are factual RGE outcomes. Standard boutique consulting practice. |
| **4 case study pages** | /portfolio/post-merger-integration-latam, /portfolio/ai-automation-fintech, /portfolio/digital-transformation-saas, /portfolio/business-transformation-fintech |
| **Portfolio overview** | /portfolio — card grid with confidentiality disclaimer bar. Each card shows tag, anonymized client, headline, 4 metrics, "Read full case study" link. |
| **Case study structure** | Hero + meta strip (client/geography/duration/service) → outcomes stats bar → challenge → numbered approach steps → sidebar (technologies, related services, CTA, confidentiality note) → related case studies |
| **Home page teasers** | Updated to link directly to individual case study pages (not just /portfolio) |

### Insights / Blog

| Decision | Detail |
|----------|--------|
| **Firestore-backed blog** | Articles stored in `articles` Firestore collection. No code push needed to publish. |
| **Admin write/publish** | /admin/insights — write title, slug (auto-generated), category, excerpt, body, author, references. Save as Draft or Publish instantly. |
| **Markdown support** | Full Markdown rendering via marked.js — headings, bold, italic, lists, links, images (by URL), blockquotes (gold left border), tables, code blocks. |
| **Paste & auto-convert** | Gold "✨ Paste & auto-convert" button in admin. Paste any raw text/HTML from any source. Claude API cleans and converts to Markdown in ~5 seconds. Ctrl+C Ctrl+V workflow. |
| **Article structure** | Hero → rendered Markdown body → references → LinkedIn share button. Sticky sidebar: CTA, related articles, About RGE. |
| **Firestore rules** | Published articles readable by everyone. Writes allowed for authenticated admin emails (rogerio@ and admin@rgenterpriseconsulting.com). Self-bootstrap on first login. |
| **LinkedIn share** | Every article has a LinkedIn share button. /insights page has Follow on LinkedIn CTA. |
| **Article publishing confirmed** | admin@rgenterpriseconsulting.com confirmed working. DaimlerChrysler article published and visible. |

### Phase 3 Status

| Item | Status |
|------|--------|
| Portfolio overview page (/portfolio) | ✅ Complete |
| 4 case study detail pages | ✅ Complete |
| Home page teasers linked to pages | ✅ Complete |
| Insights overview page (/insights) | ✅ Complete |
| Article detail page (/insights/[slug]) | ✅ Complete |
| Admin write/publish interface | ✅ Complete |
| Markdown rendering | ✅ Complete |
| Paste & auto-convert (AI) | ✅ Complete |
| Firebase rules deployed | ✅ Complete |

---

## Updated Project Phase Roadmap — June 9, 2026

| Phase | Name | Status |
|-------|------|--------|
| Phase 1 | Brand & Design System | ✅ Complete |
| Phase 2 | Services & Lead Generation | ✅ Complete |
| Phase 3 | Case Studies, Portfolio & Insights Blog | ✅ Complete |
| Phase 4 | Visual Identity — Higgsfield AI | 🔴 Not Started |
| Phase 5 | Mobile Responsiveness | 🔴 Not Started — HIGH priority pre-launch |
| Phase 6 | Insights Platform & SEO | 🟡 Partial — blog built, SEO meta tags pending |
| Phase 7 | Client Portal v2 | 🔴 Not Started |
| Phase 8 | Super-Admin CMS | 🔴 Not Started |

### Pre-Launch Checklist (before firebase deploy --only hosting)
- [ ] Phase 4: Higgsfield visual production
- [ ] Phase 5: Mobile responsiveness fix — all pages
- [ ] WhatsApp floating button review (v1.4 → v2.0)
- [ ] Node.js 20 → 22 upgrade (before Oct 2026)
- [ ] Testimonials — replace placeholders with real quotes
- [ ] Firebase App Check enforcement — enable after go-live
- [ ] GitHub Actions CI/CD workflow scope

---

## Session 4 Decisions & Fixes — June 9, 2026

### Mobile Responsiveness ✅ Complete

| Item | Detail |
|------|--------|
| **Approach** | Shared `useIsMobile()` hook at `src/hooks/useIsMobile.js` — watches window resize, returns boolean at 768px breakpoint |
| **Scope** | 14 files updated: Home, About, Contact, Services, Portfolio, Insights, CaseStudyDetail, ArticleDetail, Footer, Navbar, all 5 service sub-pages |
| **Grid rules** | 2-col → 1-col on mobile. 3-col → 1-col. 4-col → 2-col. Content+sidebar → stacked. |
| **Padding** | Section padding reduced 80px → 48px on mobile. Form cards 40px → 16px. |
| **Sticky sidebars** | Disabled on mobile — position switches to static |
| **Contact page** | Hardcoded `1fr 340px` grid fixed to `isMobile ? '1fr' : '1fr 340px'`. Form stacks above sidebar on mobile. Confirmed working. |

### Auth Pages Rebranded ✅

| Page | Change |
|------|--------|
| `/login` — ClientLogin.jsx | Full rebrand: dark gray → Navy+Gold white card, RG logo at top, brand typography, gold links |
| `/forgot-password` — ForgotPassword.jsx | Same rebrand treatment. Clean, consistent with public site. |
| ClientSignup.jsx | Still old dark theme — deferred to Phase 7 (Client Portal rebuild) |

### Insights Blog — Issues Fixed ✅

| Issue | Fix |
|-------|-----|
| Firestore permissions error on publish | Firestore rules updated — articles writable by `admin@rgenterpriseconsulting.com` and `rogerio@rgenterpriseconsulting.com` directly via `request.auth.token.email` check. No `users_roles` doc required. |
| "Loading articles" forever on public page | Removed composite index requirement — now fetches all articles and filters client-side |
| Publish button saving as draft | Fixed setState race condition — status passed directly to `handleSave(status)` as parameter |
| Markdown rendering | Added `marked.js` — full Markdown support: headings, bold, italic, lists, links, images, blockquotes, tables, code blocks |
| Paste & auto-convert | Claude API converts any pasted text/HTML to clean Markdown in ~5 seconds |
| First article published | DaimlerChrysler PMI case study live at /insights |

### Updated Pre-Launch Checklist

| Item | Status |
|------|--------|
| Phase 3: Portfolio & Case Studies | ✅ Complete |
| Phase 3: Insights Blog (Firestore) | ✅ Complete |
| Mobile responsiveness | ✅ Complete |
| Login / Forgot Password rebrand | ✅ Complete |
| Phase 4: Higgsfield visual production | 🔴 Pending |
| ClientSignup rebrand | 🟡 Deferred to Phase 7 |
| WhatsApp floating button v2.0 | 🟡 Pending pre-launch |
| Node.js 20 → 22 upgrade | 🟡 Before Oct 2026 |
| Firebase App Check enforcement | 🟡 Post go-live |
| Testimonials — real quotes | 🟡 When available |
| SEO meta tags & sitemap | 🟡 Phase 6 |

---

## Careers Feature ✅ Built — June 2026

| Decision | Detail |
|----------|--------|
| **Platform** | Built on same Firebase stack — Firestore for positions/applications, Storage for resumes, Functions for email |
| **Admin write** | /admin/careers — post/edit/close positions with full Markdown JD. Same pattern as Insights admin. |
| **Public listing** | /careers — open positions card list. Empty state with direct email CTA. |
| **Job detail page** | /careers/[slug] — Markdown JD rendered, LinkedIn Share in hero, sticky application form |
| **Application form** | Name, email, phone, LinkedIn URL, resume upload (PDF/Word max 5MB), optional cover note |
| **Resume storage** | Firebase Storage — resumes/ folder. Download URL stored in Firestore applications collection. |
| **Notification email** | Sent to talent@rgenterpriseconsulting.com with all candidate details + gold Download Resume button |
| **Auto-reply** | Sent to candidate with reference number (RGE-APP-XXXXXX) and confirmation |
| **Firebase Function** | sendApplicationEmail — deployed alongside sendContactEmail in functions/index.js |
| **Firestore rules** | positions: open ones public-readable, admin-writable. applications: anyone can create (submit), admin-readable only. |
| **Navigation** | Careers added to both navbar and footer |
| **LinkedIn workflow** | Each job page has LinkedIn Share button. URL posted on LinkedIn auto-pulls og:title and og:description from meta tags. |
| **Reference number format** | RGE-APP-XXXXXX (6-digit timestamp suffix) |
| **Talent email** | talent@rgenterpriseconsulting.com — must be created as Ionos mailbox before go-live |

### Pre-Launch: Create Talent Email
Before going live, create `talent@rgenterpriseconsulting.com` as an Ionos mailbox. Same process as `leads@rgenterpriseconsulting.com`. Otherwise application notifications will bounce.

---

## Careers Feature — Issues Fixed & Final State (June 2026)

| Issue | Root Cause | Fix |
|-------|-----------|-----|
| Careers page blank | Route `/careers` was imported but never added to App.jsx Routes | Added public routes `/careers` and `/careers/:slug` |
| Login page hanging | `setLoading(false)` ran after successful login but `useEffect` navigated away first — button stayed disabled forever | `setLoading(false)` now only runs on error, not on success |
| Resume upload CORS error | Firebase Storage bucket didn't exist yet, then CORS rules weren't set | Created Storage bucket in Firebase Console, ran `gcloud storage buckets update` with cors.json |
| Resume upload permission denied | No `storage.rules` file existed — Firebase defaulted to deny all | Created storage.rules allowing public PDF/Word uploads under 5MB to resumes/ folder |
| Sign Out missing from admin | No logout button existed in AdminDashboard | Added red Sign Out button — logs out and redirects to /login |
| CSP blocking Firestore | index.html CSP missing `firebasestorage.googleapis.com`, `securetoken.googleapis.com`, `*.firestore.googleapis.com` | Updated CSP in index.html to include all required Firebase domains |

### Security Rules — Final State

| Surface | Rule |
|---------|------|
| Storage resumes/ | Public create: PDF/Word only, max 5MB, no overwrites. Read/delete: authenticated only. |
| Firestore applications | Public create with field validation (must have fullName, email, positionId, size limits). Read: admin only. |
| Firestore articles | Published status readable publicly. Drafts: admin only. |
| Firestore positions | Public read (for listing). Write: admin only. |
| Firestore leads/meta | Completely locked — Firebase Functions only. |
| Everything else | Default deny. |

### Careers Feature — Confirmed Working
- Admin posts position at /admin/careers → appears in Firestore `positions` collection
- Public sees position at /careers → clicks → /careers/[slug] with full JD
- Applicant fills form, uploads PDF resume → Firebase Storage `resumes/` folder
- Application saved to Firestore `applications` collection
- Email notification sent to talent@rgenterpriseconsulting.com with download link
- Auto-reply sent to applicant with reference number
- LinkedIn Share button on each job page

---

## Phase 4 — Visual Identity & Site Beautification (June 2026)

### Hero Redesign — Approved & Implemented

| Decision | Detail |
|----------|--------|
| **Headshot removed from homepage** | Headshot completely removed from hero — firm-first brand |
| **Hero background** | Animated canvas: gold circuit grid lines + travelling signal pulses. Nodes pulse at grid intersections. Rotating dashed rings orbit the logo center. |
| **Hero logo** | `logo-white-transparent.png` — 442px, opacity 15%, CSS filter `invert(1) sepia(1) saturate(0)` = pure white ghost. Gentle float animation (4s sine wave). |
| **Logo direction rejected** | Wireframe/outline SVG rejected — `FinalCorrigido.svg` confirmed as raster PNG embedded in SVG shell (no vector paths). True outline not technically possible without original .ai/.eps file. |
| **Logo watermark rationale** | Logo is decorative support element, not competing with headline. Left side (text) is the primary message. |
| **Glow/rings** | Canvas draws 3 pulsing gold rings + 2 rotating dashed rings around logo center — animated energy without altering the logo itself |
| **How We Work section** | 3 Unsplash photos at full visibility below fold (between Trusted By and Services). M&A Integration / AI & Digital / Transformation. Gold tag badges. Approved. |
| **"Senior Practitioners" text** | Corrected — removed false claim about senior-only staffing. New copy: "Every RGE engagement is staffed with experienced professionals committed to delivery. We don't just advise — we execute alongside your team and own the outcomes." |
| **Track Record section** | Removed from About page — too personally focused on Rogerio, not firm-first |

### Inner Page Heroes — Each Unique

| Page | Visual Treatment | Headline |
|------|-----------------|----------|
| Services | Interconnected node graph SVG (background, 6% opacity) | "Enterprise Services. Built to Execute." |
| About | Globe/longitude lines SVG watermark — communicates global reach | "The Firm Behind Every Program We Lead." |
| Portfolio | Rising bar chart elements (bottom-right, 8% opacity) | "Real Programs. Measurable Outcomes." |
| Insights | Horizontal editorial rule lines (4% opacity) | "Perspectives From Practitioners Who Lead." |
| Careers | Globe arc with dashed flight path + city dots | "Work on Programs That Actually Matter." |
| Contact | Diagonal gold accent lines (right side, 6% opacity) | "Your Toughest Challenge Deserves a Real Answer." |

All heroes: navy `#1B2A4A`, gold `#C8A84B`, Montserrat 800 headlines, consistent eyebrow pattern.

### Contact Page — Full Conversion Redesign

| Element | Decision |
|---------|----------|
| **Hero layout** | Split — headline + 3 trust badges left, proof strip ($30M+/15yr/3 continents/24h) right |
| **Trust badges** | ⚡ 24h response guarantee · 🔒 Strictly confidential · 🤝 No pitch — just a conversation |
| **Photo strip** | Same 3 Unsplash cards as homepage How We Work section — replaces redundant dark text strip |
| **Step micro-copy** | Reassuring one-liner under each step title explaining why we ask |
| **Sidebar** | "What Happens Next" upgraded: numbered circles with gold borders + subtitle per step |
| **Calendly strategy** | Calendly LOCKED behind form submission — zero Calendly links visible anywhere on site before form is filled |
| **Calendly CTA** | Appears ONLY on thank-you screen after submission + in confirmation email to submitter |
| **Navbar CTA** | "Schedule a Call" → points to /contact (not Calendly directly) |
| **About page CTA** | Points to /contact |
| **Rationale** | Forces every prospect to submit form first — Rogerio enters every Calendly call fully briefed |

### Careers Page Improvements

| Change | Detail |
|--------|--------|
| Hero globe arc | SVG globe with dashed flight path arc — communicates cross-border work |
| Icon upgrade | Emoji icons in "Why RGE" cards replaced with proper inline SVG icons |
| Hero copy | "Work on Programs That Actually Matter." |

---

## Lead Intelligence System — Phase 4 (June 2026)

### Architecture

| Component | Location | Editable Without Code |
|-----------|----------|----------------------|
| Numeric scoring weights | `functions/index.js` `scoreLead()` | ❌ Requires code edit |
| Free email domain list | `functions/index.js` `FREE_EMAIL_DOMAINS[]` | ❌ Requires code edit |
| High-risk country list | `functions/index.js` `HIGH_RISK_COUNTRIES[]` | ❌ Requires code edit |
| AI analysis prompt | Firestore `config/leadIntelligencePrompt` | ✅ Admin UI at /admin/prompt |

### Lead Scoring — Quantitative (scoreLead function)

| Signal | Points |
|--------|--------|
| Budget $150K+ | +25 |
| Budget $75K-$150K | +20 |
| Budget $25K-$75K | +12 |
| Budget Under $25K | +5 |
| Timeline ASAP | +25 |
| Timeline 1-3 months | +20 |
| Timeline 3-6 months | +12 |
| Timeline Just exploring | +5 |
| Company 1000+ employees | +20 |
| Company 201-1000 | +16 |
| Company 51-200 | +10 |
| Company 1-50 | +5 |
| CEO/President/Owner | +15 |
| COO/CTO/CFO | +14 |
| VP/Vice President | +12 |
| Director | +10 |
| Manager/Head of | +7 |
| Analyst/Associate | +3 |
| Company website provided | +10 |
| Phone number provided | +5 |
| Free email (gmail etc.) | −10 |
| High-risk country origin | −20 |
| VPN/Proxy detected | −15 |

Score labels: 🔥 HOT (75+) · ⚡ WARM (50+) · ❄️ COLD (25+) · 👀 UNSCORED

### IP Intelligence (ip-api.com)
- Country name + country code on every submission
- ISP/network provider identified
- Proxy/VPN detection
- High-risk country flag (27 countries listed in code)
- Local/dev IPs automatically skipped

### Free Email Detection
Domains flagged: gmail.com, yahoo.com, hotmail.com, outlook.com, live.com, aol.com, icloud.com, me.com, msn.com, ymail.com, protonmail.com, mail.com, zoho.com, gmx.com, inbox.com

### AI Intelligence — Claude Analysis (qualitative)
Claude analyzes every submission across 5 dimensions and returns structured JSON:
1. **Email domain** — corporate vs free, domain-to-company match
2. **Job title** — seniority, economic buyer vs influencer vs researcher
3. **Geographic risk** — country, proxy/VPN, high-risk flag with explicit warning
4. **Content** — free-text fields analyzed for authenticity, coherence, specificity
5. **Company** — known context, legitimacy check, size/industry match

Output fields: `credibilityScore` (0-100), `credibilityRating`, `emailAnalysis`, `titleAnalysis`, `geoRiskAnalysis`, `contentAnalysis`, `companyAnalysis`, `redFlags[]`, `greenFlags[]`, `recommendedAction`, `actionRationale`, `openingTalkingPoint`

Recommended actions: `CALL_TODAY` / `FOLLOW_UP_48H` / `NURTURE` / `DO_NOT_ENGAGE`

### Admin Prompt Editor — /admin/prompt
- Full textarea UI to edit the Claude prompt live
- 20 `{{variables}}` available (all form fields + IP data)
- Changes saved to Firestore `config/leadIntelligencePrompt`
- Firebase Function reads from Firestore on every submission
- Falls back to hardcoded default if Firestore unavailable
- Save/Reset to Default / last-saved timestamp shown
- Variable reference panel: click to insert at cursor

### reCAPTCHA Fixes
- Localhost bypass: requests from localhost skip reCAPTCHA entirely (always scores low in dev)
- Production threshold lowered 0.4 → 0.3 (still blocks bots at 0.1-0.2)
- Logic bug fixed: inverted if/else was blocking localhost instead of skipping it

### Contact Form Bug Fixes
- **Auto-submit bug**: `<form onSubmit>` replaced with plain `<div>` — Submit button is `type="button"` with `onClick`. Physically impossible to auto-submit now.
- **Step guard**: `handleSubmit` previously had no check for current step — could fire on Enter key from any step. Now only callable via explicit button click.

---

## Pre-Launch Checklist — Updated June 2026

| Item | Status | Notes |
|------|--------|-------|
| Phase 3: Portfolio & Case Studies | ✅ Complete | |
| Phase 3: Insights Blog (Firestore) | ✅ Complete | |
| Phase 3: Careers feature | ✅ Complete | talent@rgenterpriseconsulting.com confirmed created |
| Phase 4: Hero redesign | ✅ Complete | Animated canvas, white ghost logo, no headshot |
| Phase 4: Inner page heroes | ✅ Complete | 6 unique visual treatments |
| Phase 4: Contact page redesign | ✅ Complete | Conversion-focused, Calendly gated behind form |
| Phase 4: Lead intelligence | ✅ Complete | IP + email + AI analysis, admin prompt editor |
| Mobile responsiveness | ✅ Complete | All pages |
| Login / Forgot Password rebrand | ✅ Complete | |
| About page Track Record | ✅ Removed | |
| Senior Practitioners copy | ✅ Fixed | |
| talent@ Ionos mailbox | ✅ Confirmed created | |
| PPT template + Word letterhead | 🟡 Post-launch | Rogerio requested — deferred |
| Higgsfield service page visuals | 🟡 Non-blocking | OG images + service page heroes |
| WhatsApp button v2.0 | 🟡 Pre-launch | |
| Node.js 20 → 22 upgrade | 🟡 Before Oct 2026 | |
| Firebase App Check | 🟡 Post go-live | |
| SEO meta tags & sitemap | 🟡 Phase 5 | |
| ClientSignup rebrand | 🔴 Phase 7 | |
| `firebase deploy --only hosting` | 🔴 DO NOT RUN | Until Rogerio approves go-live |

---

## Phase 5 — SEO & Go-Live (June 2026)

### SEO Implementation — Complete

| Page | Title Tag | Keywords Targeted |
|------|-----------|-------------------|
| Homepage | RG Enterprise Consulting — M&A Integration, AI Readiness & Digital Transformation Consulting | post-merger integration consultant, M&A integration, boutique consulting |
| Services | M&A Integration, AI Readiness & Digital Transformation Consulting Services — RGE | PMI consulting, AI readiness assessment, digital transformation |
| PMI service | Post-Merger Integration (PMI) Consulting — RG Enterprise Consulting | post merger integration consultant, IMO setup, M&A integration LATAM |
| AI Readiness | AI Readiness Assessment & Corporate AI Strategy Consulting — RGE | AI readiness assessment enterprise, corporate AI strategy |
| Digital Transformation | Digital Transformation & Technology Integration Consulting — RGE | digital transformation consulting, ERP implementation program management |
| Business Transformation | Business Transformation & Organizational Strategy Consulting — RGE | business transformation consulting, organizational strategy |
| Project Management | PMO Consulting & Program Management Services — RGE | PMO consulting, program management consulting, PMO setup |
| About | About RG Enterprise Consulting — Boutique M&A & Transformation Consulting Firm | boutique consulting firm, consulting partnerships, LATAM expansion |
| Portfolio | M&A Integration & Transformation Case Studies — RGE | M&A integration case studies, transformation outcomes |
| Insights | M&A Integration & AI Readiness Insights — RGE Blog | thought leadership, M&A integration insights |
| Careers | Consulting Careers — Join RGE | consulting careers, PMI consultant jobs |
| Contact | Contact RGE — Start Your Transformation Engagement | contact consulting firm, M&A integration consultant contact |

### Technical SEO Implemented
- Canonical URLs on all 14 pages
- `sitemap.xml` — all 14 public URLs with priorities (service pages 0.9, contact 0.8)
- `robots.txt` — admin/login/portal blocked, public pages allowed
- Organization JSON-LD structured data on homepage — ProfessionalService schema
- Service JSON-LD on all 5 service pages
- Geo targeting meta tags — Johns Creek GA, USA primary
- Full Open Graph tags (og:image, og:title, og:description, og:locale) on all pages
- GA4 Measurement ID `G-BFEV07JWC2` implemented
- `generate_lead` conversion event fires on every contact form submission

### Partnership & European Geo Signals Added
- About page: Global Reach strip — Geographic Reach / Consulting Partnerships / Languages
- About page: 4th card added to Agency Model — "Strategic Partnerships"
- Services hero: mentions North America, Latin America, UK, Europe
- JSON-LD areaServed expanded: + United Kingdom + Spain
- Meta keywords: + consulting firm partnership, M&A integration Latin America, LATAM expansion consulting
- PMI page: "Trusted partner for consulting firms co-delivering M&A programs"
- Target audiences: (1) Corporate M&A executives USA, (2) PE-backed mid-market, (3) UK/Spain firms expanding to LATAM, (4) Consulting firm partners

### SEO Strategy — Decisions Locked
- No broad keyword targeting — precision over volume
- Content strategy: 1 Insights article/month minimum (highest ROI SEO action)
- Google Ads: defer to months 3–6 after organic baseline established
- LinkedIn: primary lead channel months 1–6 (faster than organic search)
- Target timeline: page 1 for niche long-tail keywords in 3–6 months

---

## Pre-Launch Security Audit (June 2026)

### Penetration Assessment Results
Overall rating: B+ — Strong foundation, 3 gaps fixed

| Vector | Finding | Action |
|--------|---------|--------|
| CORS | origin: true — any domain could call Firebase Functions | FIXED — locked to rgenterpriseconsulting.com + localhost |
| Input sanitization | No server-side sanitization on form fields | FIXED — HTML stripping, length limits, email regex on all 14 fields |
| Admin role bootstrap | Email match could be exploited | FIXED — explicit ADMIN_EMAILS whitelist |
| Firebase API key | Committed to git history in early commit | FIXED — removed from tracking; fallback values in firebase.js |
| .env file | Accidentally committed to git | FIXED — removed from git tracking |
| Firestore rules | Already hardened | PASS |
| HTTP security headers | HSTS, X-Frame-Options, CSP, Permissions-Policy | PASS |
| reCAPTCHA | Active with localhost bypass | PASS |
| Rate limiting | 5 submissions/IP/hour | PASS |
| Server secrets | In Firebase Secret Manager | PASS |

### Firebase API Key Restriction — Decision
- HTTP referrer restriction was attempted but broke Firebase Auth (`auth/invalid-api-key`)
- Root cause: Firebase Auth initializes from multiple internal Google domains not easily whitelisted
- Resolution: Set Application restrictions to "None" — acceptable because Firestore Security Rules protect data at the collection level
- Proper solution: Firebase App Check (deferred to post-launch — see Phase 7)
- Firebase API keys for web apps are intentionally semi-public — real security is at the rules layer

### Security Files Deployed
- `firestore.rules` — hardened with field validation, draft article protection, admin whitelist
- `storage.rules` — resumes: public upload (PDF/Word, max 5MB, no overwrites), admin read only
- `firebase.json` — full HTTP security headers, CSP, HSTS
- `functions/index.js` — CORS lock, input sanitization, rate limiting, reCAPTCHA, IP intelligence

---

## Go-Live — June 11, 2026

### Launch Sequence
1. `npm run build` → `firebase deploy --only functions` → `firebase deploy --only hosting`
2. Domain: `https://rgenterpriseconsulting.com` — LIVE ✅
3. `www.rgenterpriseconsulting.com` — configured via Firebase Hosting custom domain (SSL provisioning)
4. Google Search Console — property added, sitemap submitted
5. GA4 linked to Search Console
6. Request indexing submitted for homepage + 5 money pages

### Post-Launch Issues Resolved
| Issue | Root Cause | Fix |
|-------|-----------|-----|
| Blank page on load | `auth/invalid-api-key` — .env removed from git, env vars undefined in build | Added fallback values to firebase.js and firebase-config.js |
| CSP blocking GA4/GTM | Google Tag Manager not in Content Security Policy | Added googletagmanager, analytics, firebaseinstallations, wss to CSP |
| www subdomain SSL error | www not configured as Firebase Hosting custom domain | Added www.rgenterpriseconsulting.com as custom domain in Firebase Console |

### Post-Launch Checklist
| Item | Status |
|------|--------|
| Site live at rgenterpriseconsulting.com | ✅ |
| www redirect configured | ✅ |
| Sitemap submitted to Search Console | ✅ |
| GA4 linked to Search Console | ✅ |
| Index requests submitted for money pages | ✅ |
| functions deployed (CORS + security) | 🟡 Run: firebase deploy --only functions |
| Firebase App Check | 🔴 Next session |
| Node.js 20 → 22 upgrade | 🔴 Before Oct 2026 |
| First Insights article published | 🔴 This week |
| LinkedIn announcement post | 🔴 Today |

---

## Updated Master Checklist — Post-Launch

| Phase | Item | Status |
|-------|------|--------|
| Phase 1 | Brand & Design | ✅ Complete |
| Phase 2 | Services & Leads | ✅ Complete |
| Phase 3 | Portfolio, Insights, Careers | ✅ Complete |
| Phase 4 | Visual Identity + Lead Intelligence | ✅ Complete |
| Phase 5 | SEO & Go-Live | ✅ Complete |
| Phase 6 | Client Portal v2 | 🔴 Next |
| Phase 7 | Super-Admin CMS + App Check | 🔴 Future |
| — | PPT template + Word letterhead | 🟡 Post-launch |
| — | Higgsfield service visuals | 🟡 Non-blocking |
| — | Node.js 20 → 22 | 🟡 Before Oct 2026 |
| — | SEO summary in BRD | 🟡 Next session |
