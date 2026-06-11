# Session Notes
## RG Enterprise Consulting — Website & Platform Project

---

## Session 1 — June 2026 (Full Session — Planning + Build)

### Planning Phase
- Audited v1.4 codebase in full (all pages, components, Firebase config)
- Conducted market research: Stonehill Innovation, Airiodion Group, 733Park
- Defined 4 service lines: PMI, AI Readiness, Digital Transformation, Business Transformation
- Created BRD v2.1 (Word doc, 9 sections, all decisions locked)
- Set up brand repo + GitHub PAT for autonomous Claude push access
- Locked all 10 BRD open questions

### Build Phase — Phase 1 Complete
All files pushed to `version-2.0` branch of website repo.

**Files created/modified:**

| File | Status | Notes |
|------|--------|-------|
| `tailwind.config.js` | ✅ Done | Navy+Gold tokens, Montserrat+Inter, custom shadows/animations |
| `src/theme.js` | ✅ Done | Central content/token file — all contact info, services, stats, logos, timeline |
| `src/index.css` | ✅ Done | Google Fonts import, white base (removed dark body), utility classes |
| `src/main.jsx` | ✅ Done | Added HelmetProvider for SEO |
| `src/App.jsx` | ✅ Done | Added /insights placeholder route |
| `src/components/Navbar.jsx` | ✅ Done | Navy, white logo, gold CTA → /contact, mobile overlay, Client Portal in footer |
| `src/components/Footer.jsx` | ✅ Done | Dark navy, 4-col layout, company LinkedIn, X (@rgeconsulting), WhatsApp, contact email footer-only |
| `src/pages/Home.jsx` | ✅ Done v3 | Hero slideshow, stats, animated ticker, services, case teasers, testimonials, CTA |
| `src/pages/About.jsx` | ✅ Done — Phase 2 Rewrite | Company-first rewrite complete. See Session 2 below. |
| `package.json` | ✅ Done | Added react-helmet-async |
| `.github/workflows/firebase-deploy.yml` | ⚠️ Blocked | PAT needs `workflow` scope to push this file |
| `firebase.json` | ✅ Done | Updated with cache headers, node18 runtime |
| `public/logos/*.png` | ✅ Done | All 9 real logos: Barton, UST, SmartTechlink, Vistra, Equifax, Datavant, Ciox, BoaVista, BizLatinHub |
| `public/photos/rogerio-headshot.jpg` | ✅ Done | Professional headshot uploaded by Rogerio |

### Design Decisions Made During Build
- Rejected: Playfair Display (too old-fashioned), dark-only theme, Calendly as primary CTA
- Rejected: Personal credentials in hero section
- Approved: Navy+Gold palette, Montserrat 800 headings, company-first language
- Approved: "Contact Us" → form as primary CTA. "Let us solve your problem" as bottom CTA
- Approved: contact@ email in footer only, not shown elsewhere
- Approved: Ticker with grayscale logos (color on hover), uniform 138×50px slots
- Fixed: Vistra + Boa Vista logo proportions (whitespace cropped, 15% size increase)

### Critical Bugs Still Open (fix in Phase 2)
1. **Contact form dead endpoint** — posts to `/api/sendContactEmail`, never wired. ALL LEADS LOST.
2. **Firebase Functions not deployed** — SendGrid integration not built
3. **GitHub Actions PAT needs `workflow` scope** — go to github.com/settings/tokens → add `workflow` scope to the Claude RG Consulting token

### Development Setup (Rogerio's computer)
- OS: Windows
- Git: installed ✅
- Node.js: installed ✅
- Project cloned to Desktop: `rgenterpriseconsulting/`
- Active branch: `version-2.0`
- Local preview confirmed working at `http://localhost:5173`
- Moving to Claude Code for future development

---

## Session 2 — June 2026 (Phase 2 — About Page Rewrite)

### What Was Done
- Read full BRD v2.2 for context (previously was v2.1; Rogerio updated it)
- Confirmed plan with Rogerio before writing any code (company-first structure)
- Rewrote `src/pages/About.jsx` completely — see change log below
- Committed and pushed to `version-2.0` branch
- Updated brand repo docs (SESSION_NOTES.md, DECISION_LOG.md) with full change record

### About.jsx — What Changed

| Element | Before (Phase 1 draft) | After (Phase 2 rewrite) |
|---------|----------------------|------------------------|
| Page `<title>` | "About Rogerio Gomes — RG Enterprise Consulting" | "About RG Enterprise Consulting — Boutique Management Consulting" |
| H1 | "Meet Rogerio Gomes" | "About RG Enterprise Consulting" |
| Hero eyebrow | "About" | "About the Firm" |
| JSON-LD schema | `Person` (Rogerio) | `Organization` with nested `Person` (founder) |
| Section order | Bio → Credentials → Career Timeline → How We Work → CTA | Why We Exist → Agency Model → Founder → Multilingual → Timeline → CTA |
| Opening copy | Rogerio's personal career narrative | Firm mission, founding story (2017), gap in the market |
| Stats block | None | 4-stat grid: Founded 2017, 15+ yrs, $30M+, 4 service lines |
| Agency model | Buried at bottom | Promoted above founder bio (BRD requirement) |
| Founder section eyebrow | n/a (was the hero) | "The Experience Behind the Firm" |
| Personal statement | None | Authentic quote block: "I built this firm because..." |
| Multilingual section | Inline in contact card only | Dedicated navy callout banner (BRD requirement) |
| Career timeline eyebrow | "Career Journey" | "The Track Record" |
| Career timeline subtitle | "From São Paulo to the World" | "15+ Years of Enterprise Delivery" |
| Timeline subtext | None | "The depth of experience that powers every RG Enterprise Consulting engagement." |
| CTA headline | "Let's Build the Future, Together" | "Ready to Start Your Transformation?" |
| CTA subtext | "Connect with Rogerio to discuss..." | "We work with a select number of clients at a time — let's see if we're the right fit." |
| Contact card (under photo) | Showed email + LinkedIn + location | Removed email (footer-only rule); kept LinkedIn + location |
| Photo src | LinkedIn CDN URL (external, can expire) | `/photos/rogerio-headshot.jpg` (local, permanent) |
| CTA primary button | "Schedule a Free Consultation" (Calendly) | "Contact Us" (→ /contact) — matches locked CTA decision |

### Correction — Email Provider Decision (Same Session)
Rogerio reviewed the About page rewrite and flagged two things:
1. **About page still too Rogerio-centric** — even after the company-first rewrite, it leans too much on the founder. OPEN — revisit in a future session with a sharper edit pass (reduce founder section length / visual weight relative to firm sections).
2. **Email provider decision was recorded incorrectly** — DECISION_LOG.md and the BRD said "SendGrid" (Q7), but that was abandoned during Phase 2 planning. The actual decision: **use IONOS SMTP relay via Nodemailer** inside the Firebase Function (not SendGrid). DECISION_LOG.md Q7 corrected accordingly (commit `cab1021`). NOTE: the BRD .docx (Section 8 Q7 + Section 10.1 Q7) still says SendGrid — should be corrected there too when the BRD is next opened for editing, so the documents stay consistent. DECISION_LOG.md is the authoritative source going forward.
### Commit Reference
- Branch: `version-2.0`
- Commit: `8f83c70`
- Message: "Phase 2: Rewrite About.jsx -- company-first, not resume-first"

### Phase 2 — Remaining Items

| Priority | Item | Status |
|----------|------|--------|
| 🔴 CRITICAL | Contact form dead endpoint (ALL LEADS LOST) | Not started |
| 🔴 CRITICAL | Firebase Functions + SendGrid | Not started |
| 🔴 HIGH | Services sub-pages (4 pages) | Not started |
| 🔴 HIGH | Enriched lead form (new fields) | Not started |
| 🟡 MED | Calendly shown after form submission | Not started |
| 🟡 MED | GitHub Actions PAT — add `workflow` scope | Blocked on Rogerio |
| 🟡 MED | Firebase Hosting auto-deploy from version-2.0 | Not started |
| 🟢 LOW | reCAPTCHA v2 → v3 upgrade | Not started |

---

## Next Session — Phase 2 Priorities (Continue)

1. **Contact form fix** — Firebase Function + SendGrid + Firestore lead storage (P0 — all leads lost)
2. **Services sub-pages** — 4 pages: /services/post-merger-integration, /services/ai-readiness, /services/digital-transformation, /services/business-transformation
3. **Enriched lead form** — company size, timeline, challenge, how they found us, lead scoring
4. **Calendly integration** — shown only after form submission confirmation

### How to Start in Claude Code
```
cd Desktop/rgenterpriseconsulting
git checkout version-2.0
git pull
claude
```
Then say:
> "Read https://github.com/rogerio-rsesystems/brand — this is my brand and project reference.
> Token: [TOKEN-IN-CLAUDE-PRIVATE-MD]
> We are on Phase 2. The About page is done. Next is the contact form fix."
---

## Session 1 — Continued (Phase 2 Started)

### Email decision change
- **SendGrid dropped** — sold to Twilio, free tier concerns
- **Ionos SMTP + Nodemailer confirmed** — Rogerio hosts DNS and email on Ionos
- SMTP: smtp.ionos.com, port 587
- From: leads@rgenterpriseconsulting.com → To: rogerio@rgenterpriseconsulting.com
- Credentials to be stored as Firebase environment secrets — never in code
- Firestore backup on every form submission confirmed (recommended approach accepted)

### Phase 2 now active in Claude Code
Claude Code started on Rogerio's Windows machine. Phase 2 priorities:
1. About page rewrite — company-first, not resume-first
2. 4 service sub-pages
3. Contact form fix — Firebase Function + Ionos SMTP + Nodemailer
4. Enriched lead form (new fields)
5. Calendly shown post-form only (on confirmation page)

### Important notes for Claude Code session
- Do NOT use SendGrid — use Ionos SMTP via Nodemailer
- Ionos SMTP credentials to be provided by Rogerio and stored as Firebase secrets
- leads@rgenterpriseconsulting.com must exist as a mailbox in Ionos before deploying
- All work on version-2.0 branch only

---

## Session 1 — Continued (Firebase Functions Complete)

### What was completed
- Firebase CLI installed and configured on Rogerio's Windows machine
- 5 Firebase secrets set via `firebase functions:secrets:set`:
  - SMTP_HOST, SMTP_PORT, SMTP_USER, SMTP_PASSWORD (Ionos SMTP)
  - ANTHROPIC_API_KEY (Claude API for AI enrichment)
- functions/index.js fully rewritten with:
  - Ionos SMTP via Nodemailer (replaces broken SendGrid approach)
  - Lead scoring 0-100 (budget + timeline + company size + job title + website + phone)
  - AI company intelligence via Claude API (claude-sonnet-4-5)
  - Firestore lead backup on every submission
  - Rich HTML notification email to rogerio@ with score badge and AI paragraph
  - Auto-reply to client with Calendly booking link
- Function deployed to Firebase (Node.js 20, us-central1)
- gcloud CLI installed, function made publicly invocable (allUsers invoker)
- End-to-end test confirmed: ✅ Firestore save, ✅ AI enrichment, ✅ emails sent
- Bug fixed: wrong Claude model name (claude-sonnet-4-20250514 → claude-sonnet-4-5)

### Firebase secrets in production
| Secret | Purpose |
|--------|---------|
| SMTP_HOST | smtp.ionos.com |
| SMTP_PORT | 587 |
| SMTP_USER | leads@rgenterpriseconsulting.com |
| SMTP_PASSWORD | Ionos mailbox password |
| ANTHROPIC_API_KEY | Claude API for AI company enrichment |

### What comes next — Phase 2 continued
1. Build Contact.jsx — 3-step form with all new fields
2. Wire Contact.jsx to the Firebase Function endpoint
3. Update firebase.json rewrite rule to point to correct function URL
4. Build Services sub-pages (4 pages)
5. Fix GitHub Actions PAT scope for auto-deploy

---

## Session 1 — Continued (Contact Form + Security Complete)

### What was completed
- Contact.jsx fully rebuilt — 3-step form, Navy+Gold design, all new fields
- Connected to live Firebase Function endpoint
- Opportunity ID displayed on thank-you screen
- Calendly shown post-form only (never before)
- Institutional language throughout ("a member of our team")
- reCAPTCHA v3 wired invisibly — score threshold 0.4
- Rate limiting: 5 submissions per IP per hour (Firestore-backed)
- Firestore security rules fully locked down
- HTTP security headers deployed (CSP, HSTS, X-Frame-Options, etc.)
- reCAPTCHA badge repositioned above WhatsApp button
- End-to-end tested: form → reCAPTCHA → Firebase Function → AI enrichment → Firestore → email notification with Opportunity ID ✅

### Security stack confirmed
- reCAPTCHA v3 (invisible, score-based) — Site Key: 6LcfqhItAAAAACmRAnAmBDoklGo77ohebIbd3eJy
- RECAPTCHA_SECRET stored as Firebase secret
- Rate limiting: 5/IP/hour
- Firestore rules: full lockdown
- HTTP headers: CSP, HSTS, X-Frame-Options, Permissions-Policy

### Phase 2 status
- ✅ About page rewrite (company-first)
- ✅ Firebase Functions (Ionos SMTP, AI enrichment, lead scoring, Opportunity ID)
- ✅ Contact form (3-step, all fields, security, fully tested)
- 🔴 Services sub-pages (4 pages) — NEXT
- 🔴 WhatsApp floating button review
- 🔴 firebase.json rewrite rule audit

### What comes next — Services Pages
4 sub-pages to build:
- /services/post-merger-integration
- /services/ai-readiness
- /services/digital-transformation
- /services/business-transformation

Each page: hero, challenge/solution framing, sub-services checklist, case study teaser, FAQ, CTA to /contact

---

## Session 2 — Services Pages Complete + Competitor Analysis (June 8, 2026)

### What was completed this session

**Services Pages (Phase 2 — now fully complete)**
- Built `/services` overview page — 5-card grid with gold hover, stats bar, CTA
- Built 4 original service sub-pages: PMI, AI Readiness, Digital Transformation, Business Transformation
- Added 5th service line: **Project Management** (PMO/Program/Portfolio/Project/Rescue/Coordination)
- Expanded PMI sub-page significantly: Day-1/100 framework, 3 synergy types, cultural integration models (absorption/preservation/hybrid), carve-out & TSA section, accordion FAQ
- Expanded AI Readiness sub-page: 4 real-world industry examples, 5-level AI Maturity Model, 2025/2026 stats
- All 5 service sub-pages follow consistent structure: navy hero → challenge/solution → extra sections → checklist → case study → FAQ accordion → CTA
- App.jsx routing updated for all 5 sub-pages

**Logo Fix**
- Identified `logo white.png` had solid white background box — wrong on navy backgrounds
- Generated `logo-white-transparent.png` programmatically from `logo.png.png` (flipped black pixels to white, kept transparency)
- Updated Navbar.jsx and Footer.jsx to use `logo-white-transparent.png`
- Uploaded `logo-white-transparent.png` to brand repo

**Security (completed previous session, documented here)**
- reCAPTCHA v3 invisible (score 0.4 threshold)
- Rate limiting: 5/IP/hour (Firestore-backed)
- Firestore rules: full lockdown
- HTTP security headers: CSP, HSTS, X-Frame-Options, Permissions-Policy
- reCAPTCHA badge repositioned to bottom: 90px (above WhatsApp button)
- All tested end-to-end: RGE-2026-0001 through RGE-2026-0003 confirmed working

**Competitor & Partner Analysis**
- Original report: 15 firms
- Expanded report: 25 firms (v2)
- Saved as `RGE_Competitor_Partner_Analysis_2026_v2.docx`
- Key finding: E78 Partners (acquired GPMIP USA 2024) is fastest-escalating competitive threat
- RG differentiated position confirmed: technology-enabled PMI + multilingual Latin America + boutique senior access

### Phase 2 — COMPLETE ✅
All Phase 2 deliverables are done:
- About page (company-first rewrite) ✅
- Firebase Function (Ionos SMTP, AI enrichment, lead scoring, Opportunity ID) ✅
- Contact form (3-step, all fields, security, fully tested) ✅
- Services overview + 5 sub-pages ✅
- Security layer (4 layers deployed) ✅

### What comes next — Phase 3: Case Studies & Portfolio
- 3-4 anonymized case study pages
- Portfolio v2 page
- Each case study: industry tag, challenge, approach, outcome metrics
- Routes: /portfolio, /portfolio/[slug]

### Still pending (not urgent)
- WhatsApp floating button review (v1.4 component needs v2.0 update)
- Node.js 20 → 22 upgrade (before Oct 2026 deadline)
- Firebase App Check enforcement (after go-live)
- GitHub Actions workflow scope for CI/CD auto-deploy
- Testimonials: replace 3 placeholders with real client quotes

---

## Session 3 — Phase 3 Complete (June 9, 2026)

### What was completed

**Portfolio / Case Studies**
- Rewrote Portfolio.jsx — card grid, confidentiality disclaimer, 4 anonymized case studies
- Built CaseStudyDetail.jsx — reusable template, all 4 cases, outcomes strip, numbered approach, sidebar
- Added all 4 case studies + 3 seed insights articles to theme.js as data
- Updated Home.jsx teasers to link to individual case study pages

**Insights Blog — Firestore-backed**
- Rebuilt Insights.jsx to read from Firestore `articles` collection (no code push to publish)
- Rebuilt ArticleDetail.jsx with full Markdown rendering via marked.js
- Built AdminInsights.jsx — write/edit/publish/draft/delete articles from admin panel
- Added Markdown cheat sheet inline in admin form
- Added "✨ Paste & auto-convert" — paste any text, Claude API converts to clean Markdown
- Fixed Firestore rules — articles writable by admin emails without needing users_roles doc
- Deployed rules, confirmed publishing works with admin@rgenterpriseconsulting.com
- First real article published: DaimlerChrysler PMI case study

**Markdown features supported**
- ## headings (navy, Montserrat), **bold**, *italic*, - lists, 1. numbered lists
- [links](url) open in new tab, ![image](url) full-width with caption
- > blockquotes render as gold left-border callouts
- Tables, inline code, code blocks, --- horizontal rules

### Known issues logged (not blocking)
1. Mobile responsiveness — all Phase 2/3 pages broken on narrow viewports
2. Client portal dark theme — Phase 7 (rebuild)
3. Admin portal dark theme — Phase 7 (rebuild)
4. WhatsApp floating button — needs v2.0 update before launch

### What comes next
- Phase 4: Higgsfield AI visual production (hero animations, service page visuals)
- Phase 5: Mobile responsiveness — full pass across all pages (HIGH priority pre-launch)
- Rogerio to add more Insights articles via admin panel (no dev needed)

---

## Session 5 — Phase 4 Visual Identity + Lead Intelligence (June 2026)

### Participants
Rogerio Laureano Gomes + Claude

### What Was Built

**Hero Redesign**
- Removed headshot from homepage hero entirely — firm-first decision locked
- Animated canvas background: gold circuit grid, travelling signal pulses, pulsing nodes
- Real logo (`logo-white-transparent.png`) — 442px, 15% opacity, white ghost filter, float animation
- Rotating gold dashed rings orbit logo center via canvas
- Logo direction explored: FinalCorrigido.svg confirmed as raster-in-SVG (no vector paths) — true outline not possible
- White ghost (CSS filter) approved as final direction

**Inner Page Heroes — all 6 public pages rebuilt**
- Services, About, Portfolio, Insights, Careers, Contact — each unique visual
- All share: navy #1B2A4A, gold #C8A84B, Montserrat 800, eyebrow pattern

**Contact Page — Full Conversion Redesign**
- New hero: split layout with proof strip + trust badges
- Calendly completely locked behind form — only appears on thank-you screen
- Photo cards strip replaces redundant dark text strip
- Step micro-copy added to each form step
- Sidebar "What Happens Next" upgraded with gold numbered circles + subtitles

**Lead Intelligence System — full rebuild**
- IP geolocation via ip-api.com (country, ISP, proxy/VPN detection)
- Free email domain detection (-10 pts)
- High-risk country list (-20 pts), proxy/VPN (-15 pts)
- Claude AI analyzes all 5 dimensions: email, title, geo, content, company
- Structured JSON output: credibilityScore, rating, flags, action, talking point
- Rich email report with color-coded panels

**Admin Prompt Editor (/admin/prompt)**
- Full textarea UI — edit Claude prompt without coding
- Saved to Firestore config/leadIntelligencePrompt
- 20 {{variables}} with click-to-insert reference panel
- Firebase Function reads Firestore on every submission
- Reset to Default safety net

**Bug Fixes**
- Contact form auto-submit: `<form>` replaced with `<div>`, submit is onClick only
- reCAPTCHA localhost bypass + inverted logic fix
- About page Track Record section removed
- "Senior Practitioners" copy corrected — no false staffing claims

### Decisions Locked
1. No headshot anywhere on homepage — ever
2. No Calendly link visible before form submission — anywhere on site
3. Logo identity preserved — no redesign, animation wraps around real logo
4. Prompt editor in admin — Rogerio owns prompt changes going forward
5. talent@rgenterpriseconsulting.com confirmed created — Careers email active

### What Comes Next (Phase 5)
- SEO: meta tags, sitemap, robots.txt, OG images for all pages
- Higgsfield service visuals (non-blocking for launch)
- WhatsApp button v2.0
- Node.js 20 → 22 upgrade (before Oct 2026 deadline)
- Go-live approval from Rogerio → `firebase deploy --only hosting`
