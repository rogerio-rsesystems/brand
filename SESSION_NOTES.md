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
| `src/pages/About.jsx` | ⚠️ Needs Rewrite | Built but still too resume-focused. Needs company-first rewrite. |
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

## Next Session — Phase 2 Priorities

1. **About page rewrite** — company-first, Rogerio as founder not CV subject
2. **Services pages** — 4 sub-pages (/services/post-merger-integration, /services/ai-readiness, /services/digital-transformation, /services/business-transformation)
3. **Contact form fix** — Firebase Function + SendGrid + Firestore lead storage
4. **Enriched lead form** — new fields: company size, timeline, challenge, how they found us
5. **Calendly integration** — shown only after form submission confirmation

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
> We are on Phase 2. Start with the About page rewrite."
