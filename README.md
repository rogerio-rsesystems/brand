# 🤖 Claude Session Startup Guide
## RG Enterprise Consulting — Website & Platform Project

---

## INSTRUCTIONS FOR CLAUDE (read this first, every session)

You are the primary developer for the RG Enterprise Consulting website. At the start of every session:

1. **Clone the brand repo for full context:**
   ```bash
   git clone https://[TOKEN]@github.com/rogerio-rsesystems/brand.git
   cd brand
   # Token is in CLAUDE_PRIVATE.md (gitignored) or provided by Rogerio
   ```

2. **Read in order:**
   - `BRAND_GUIDE.md` — colors, fonts, voice, service lines
   - `DECISION_LOG.md` — ALL locked decisions + open TODO items
   - `SESSION_NOTES.md` — what was built, what's next

3. **Clone the website repo and check out the active branch:**
   ```bash
   git clone https://[TOKEN]@github.com/rogerio-rsesystems/rgenterpriseconsulting.git
   cd rgenterpriseconsulting
   git checkout version-2.0
   ```

4. **Confirm to Rogerio what you're picking up and what's next.**

5. **Rules:**
   - Never hard-code colors, fonts, or contact info — always use `src/theme.js`
   - Always work on `version-2.0` branch — never commit to `main` or `version-1.4`
   - Push to GitHub at end of every session
   - Update `DECISION_LOG.md` and `SESSION_NOTES.md` after each session

---

## Project Overview

| Item | Detail |
|------|--------|
| Client | Rogerio Laureano Gomes |
| Company | RG Enterprise Consulting LLC |
| Website | rgenterpriseconsulting.com |
| Stack | React 18 + Vite + Tailwind CSS + Firebase (Hosting, Firestore, Auth, Functions) |
| Active branch | `version-2.0` |
| Old branch (backup) | `version-1.4` — DO NOT TOUCH |
| BRD | `RG_Enterprise_Consulting_BRD_v2.1.docx` in this repo |
| GitHub Token | In `CLAUDE_PRIVATE.md` (gitignored) — ask Rogerio if missing |
| Dev tool | Claude Code (moved from claude.ai chat Jun 2026) |

---

## Phase Status

| Phase | Name | Status | Notes |
|-------|------|--------|-------|
| Phase 1 | Brand & Design System | 🟢 Complete | Pushed to version-2.0 |
| Phase 2 | Services & Lead Generation | 🔴 Not Started | **Next priority** |
| Phase 3 | Case Studies & Portfolio | 🔴 Not Started | |
| Phase 4 | Insights Platform & SEO | 🔴 Not Started | |
| Phase 5 | Client Portal v2 | 🔴 Not Started | |
| Phase 6 | Super-Admin CMS | 🔴 Not Started | |

---

## Immediate TODO (start here)

1. 🔴 **About page rewrite** — company-first, not Rogerio's CV
2. 🔴 **Contact form fix** — Firebase Function + SendGrid (P0 — all leads currently lost)
3. 🔴 **Services sub-pages** — 4 pages under /services/
4. 🟡 **GitHub Actions** — add `workflow` scope to PAT at github.com/settings/tokens
5. 🟡 **Firebase hosting** — connect to auto-deploy from version-2.0 branch

---

## Repo Structure

```
brand/
├── README.md                               ← This file
├── BRAND_GUIDE.md                          ← Colors, fonts, voice, service lines
├── DECISION_LOG.md                         ← All locked decisions + open TODOs
├── SESSION_NOTES.md                        ← Build log + what comes next
├── RG_Enterprise_Consulting_BRD_v2.1.docx ← Full Business Requirements Document
├── logo.png.png                            ← Primary logo (black, for light backgrounds)
├── logo white.png                          ← White logo (for dark/navy backgrounds)
├── favicon-32x32.png                       ← Browser favicon
├── social-image.jpg                        ← OG social share image
├── .gitignore                              ← Excludes CLAUDE_PRIVATE.md
└── CLAUDE_PRIVATE.md                       ← GITIGNORED — GitHub token
```

---

## End-of-Session Checklist

- [ ] All code committed and pushed to `version-2.0`
- [ ] `DECISION_LOG.md` updated with new decisions
- [ ] `SESSION_NOTES.md` updated with what was done + what's next
- [ ] Phase Status table updated above
- [ ] Brand repo committed and pushed
