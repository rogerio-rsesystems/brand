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
