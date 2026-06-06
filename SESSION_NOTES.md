# Session Notes
## RG Enterprise Consulting — Website & Platform Project

---

## Session 1 — June 2026

### What was accomplished
- Uploaded and fully audited v1.4 codebase
- Conducted market research (Stonehill Innovation, Airiodion Group, 733Park)
- Defined 4 service lines: PMI, AI Readiness, Digital Transformation, Business Transformation
- Created BRD v2.0 (Word document, 9 sections)
- Set up brand repo at https://github.com/rogerio-rsesystems/brand with GitHub PAT for autonomous push
- Locked ALL 10 BRD open questions (see DECISION_LOG.md)
- Established complete brand system: Navy+Gold palette, Montserrat+Inter fonts

### All decisions locked this session
- ✅ Colors: Navy `#1B2A4A` + Gold `#C8A84B` on white
- ✅ Fonts: Montserrat 800 headings + Inter body
- ✅ Testimonials: realistic placeholders
- ✅ Case studies: anonymized by industry/size, zero fabrication
- ✅ Trusted By bar: real logos (The Barton Partnership, UST Global, Smart Techlink Solutions, Vistra, Equifax, Datavant, Ciox Health, Boa Vista Serviços, BizLatinHub)
- ✅ AI Readiness: presented as 100% RG
- ✅ Calendly: confirmed, link TBD (share at start of Session 2)
- ✅ Email: SendGrid from leads@ to rogerio@
- ✅ LinkedIn: https://www.linkedin.com/company/rg-enterprise-consulting/
- ✅ WhatsApp: +1 (310) 430-6698, WhatsApp Business, keep + expand later
- ✅ Client portal: rebuild in-house (Phase 5)

### Critical bugs to fix in Phase 1/2
1. Contact form posts to dead endpoint — all leads lost
2. Zero SEO on any page
3. Fake "Jane Doe" testimonial on homepage
4. Footer links to /client-login (wrong path)
5. Firebase credentials likely in Git

### What comes next — Session 2
**Start of session:** Rogerio shares Calendly link
**Phase 1 build order:**
1. `tailwind.config.js` — design token system (colors, fonts, spacing)
2. `src/theme.js` — central token file
3. `Navbar.jsx` — v2 (navy bg, gold CTA, Montserrat logo)
4. `Footer.jsx` — v2 (navy bg, all correct links, WhatsApp, LinkedIn)
5. `Home.jsx` — v2 (new hero, trusted-by bar, services, stats, placeholder testimonials, CTA)
6. `About.jsx` — v2 (Rogerio's story, credentials, career timeline)
7. SEO foundation — react-helmet-async on all pages

### How to start Session 2
> "Read the brand repo at https://github.com/rogerio-rsesystems/brand — token in CLAUDE_PRIVATE.md. All decisions are locked. Here is my Calendly link: [link]. Start Phase 1 build."

---

## Session 1 — Continued (Phase 1 Build)

### Phase 1 files built and delivered
All files are drop-in replacements for the existing v1.4 files.

| File | Path in project | What it does |
|------|----------------|--------------|
| `tailwind.config.js` | root | Full design token system — Navy+Gold palette, Montserrat+Inter fonts, shadows, animations |
| `src/theme.js` | src/ | Central JS token export — colors, fonts, contact info, services, stats, trustedBy, credentials, career timeline. Import in any component — never hard-code content again. |
| `src/index.css` | src/ | New base styles — imports Google Fonts, resets dark body, defines btn-gold, btn-navy-outline, card, eyebrow utilities |
| `src/components/Navbar.jsx` | src/components/ | New navbar — navy bg, white logo, gold CTA, sticky + scroll shadow, mobile overlay menu, Client Portal link moved to footer |
| `src/components/Footer.jsx` | src/components/ | New footer — dark navy, 4-column layout, correct links, WhatsApp + LinkedIn icons, gold CTA button |
| `src/pages/Home.jsx` | src/pages/ | Full homepage — hero, stats bar, trusted-by, 4 service cards, 2 case study teasers, rotating testimonials, CTA section. SEO meta tags via react-helmet-async. |
| `src/pages/About.jsx` | src/pages/ | Full about page — bio, credentials grid, career timeline, agency model section, CTA. JSON-LD Person schema. |

### Installation steps for Rogerio
1. Unzip `phase1_files.zip`
2. Replace the following files in your project with the new versions:
   - `tailwind.config.js`
   - `src/index.css`
   - `src/theme.js` (new file — add to src/)
   - `src/components/Navbar.jsx`
   - `src/components/Footer.jsx`
   - `src/pages/Home.jsx`
   - `src/pages/About.jsx`
3. Install react-helmet-async: `npm install react-helmet-async`
4. Wrap your app in `<HelmetProvider>` in `src/main.jsx`
5. Run `npm run dev` to preview

### What comes next — Phase 2
- Services pages (4 sub-pages)
- Contact form fix — Firebase Function + SendGrid
- Enriched lead form
- Calendly embed integration
