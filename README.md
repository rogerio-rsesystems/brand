# 🤖 Claude Session Startup Guide
## RG Enterprise Consulting — Website & Platform Project

This file tells Claude exactly what to read and load at the start of every new conversation.

---

## INSTRUCTIONS FOR CLAUDE (read this first, every session)

You are the primary developer and strategic advisor for the RG Enterprise Consulting website overhaul project. At the start of every session, you must:

1. **Clone this brand repo. The GitHub token is stored in CLAUDE_PRIVATE.md (never commit that file):**
   ```bash
   git clone https://[TOKEN]@github.com/rogerio-rsesystems/brand.git
   git config user.email "rogerio@rgenterpriseconsulting.com"
   git config user.name "Claude (RG Consulting)"
   ```
   Read CLAUDE_PRIVATE.md (it is gitignored) to get the token. If it doesn't exist, ask Rogerio for the GitHub PAT.

2. **Read these files in order:**
   - `BRAND_GUIDE.md` — colors, fonts, logo assets, voice, service lines, credentials
   - `RG_Enterprise_Consulting_BRD_v2.0.docx` — full project requirements
   - `DECISION_LOG.md` — all locked decisions from previous sessions
   - `SESSION_NOTES.md` — notes from last session

3. **Website codebase repo (may be private — request ZIP if needed):**
   ```
   https://github.com/rogerio-rsesystems/rgenterpriseconsulting.git
   ```

4. **Confirm to Rogerio what phase and task you are picking up.**

5. **Never hard-code colors, fonts, or content** — always reference design tokens from `BRAND_GUIDE.md`.

6. **At the end of every session**, commit and push all updates to this repo:
   - Update `DECISION_LOG.md` with any locked decisions
   - Update `SESSION_NOTES.md` with what was done and what comes next
   - Update the Phase Status table below
   - Commit with message: `Session N: [brief summary]`
   - Push to main branch

---

## Project Overview

| Item | Detail |
|------|--------|
| **Client** | Rogerio Laureano Gomes |
| **Company** | RG Enterprise Consulting LLC |
| **Website** | rgenterpriseconsulting.com |
| **Stack** | React 18, Vite, Tailwind CSS, Firebase (Hosting, Firestore, Auth, Functions) |
| **BRD Version** | 2.0 (June 2026) |
| **Current Site Version** | 1.4 (November 2025, built in Windsurf) |
| **New Dev Tool** | Claude (you) — Windsurf no longer used |

---

## Phase Status (update after each session)

| Phase | Name | Status | Notes |
|-------|------|--------|-------|
| Phase 1 | Brand & Design System | 🟡 In Progress | Colors & fonts locked. Starting build next session. |
| Phase 2 | Services & Lead Generation | 🔴 Not Started | Blocked on Phase 1 |
| Phase 3 | Case Studies & Portfolio | 🔴 Not Started | Blocked on Q4 (client naming) |
| Phase 4 | Insights Platform & SEO | 🔴 Not Started | — |
| Phase 5 | Client Portal v2 | 🔴 Not Started | — |
| Phase 6 | Super-Admin CMS | 🔴 Not Started | — |

**Status key:** 🔴 Not Started | 🟡 In Progress | 🟢 Complete | ⏸️ Blocked

---

## Open Questions (from BRD Section 8)

| # | Question | Blocks | Status |
|---|----------|--------|--------|
| Q1 | Brand color direction (Navy+Gold vs other options) | Phase 1 | ❓ Open |
| Q2 | Typography preference (Playfair Display + Inter?) | Phase 1 | ❓ Open |
| Q3 | Real client testimonials available? | Phase 1 | ❓ Open |
| Q4 | Can we name Vistra, Equifax, Datavant, Verifone? | Phase 3 | ❓ Open |
| Q5 | AI partner branding — name them or keep anonymous? | Phase 2 | ❓ Open |
| Q6 | Calendly account — do you have one? | Phase 2 | ❓ Open |
| Q7 | Email provider for lead notifications (SendGrid/SES/Gmail)? | Phase 2 | ❓ Open |
| Q8 | LinkedIn company page URL confirmed active? | Phase 1 | ❓ Open |
| Q9 | WhatsApp number +1 (310) 430-6698 still correct? | Phase 1 | ❓ Open |
| Q10 | Client portal — rebuild in-house or use 3rd party? | Phase 5 | ❓ Open |

---

## How to Start a Session

### Option A — Continue from last session
> "Read the brand repo and continue from where we left off."

### Option B — Answer open questions
> "Read the brand repo. Here are my answers: Q1: [answer], Q2: [answer]..."

### Option C — Start a specific phase
> "Read the brand repo and start Phase 1."

---

## Repo File Structure

```
brand/
├── README.md                               ← This file (Claude startup guide)
├── BRAND_GUIDE.md                          ← Colors, fonts, voice, assets spec
├── DECISION_LOG.md                         ← All locked decisions
├── SESSION_NOTES.md                        ← Running notes per session
├── RG_Enterprise_Consulting_BRD_v2.0.docx ← Full Business Requirements Document
├── logo.png.png                            ← Primary logo (dark backgrounds)
├── logo white.png                          ← White logo variant
├── favicon-32x32.png                       ← Browser favicon
├── social-image.jpg                        ← OG / social share image
└── CLAUDE_PRIVATE.md                       ← GITIGNORED — contains GitHub token
```

---

## End-of-Session Checklist for Claude

- [ ] Summarize what was built or decided
- [ ] Update `DECISION_LOG.md` with locked decisions
- [ ] Update `SESSION_NOTES.md` with what was completed and what comes next
- [ ] Update Phase Status table if any phase changed
- [ ] Commit and push all changes to this repo
