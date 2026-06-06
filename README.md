# 🤖 Claude Session Startup Guide
## RG Enterprise Consulting — Website & Platform Project

This file tells Claude exactly what to read and load at the start of every new conversation.

---

## INSTRUCTIONS FOR CLAUDE (read this first, every session)

You are the primary developer and strategic advisor for the RG Enterprise Consulting website overhaul project. At the start of every session, you must:

1. **Clone this brand repo** to read current assets and brand guide:
   ```
   https://github.com/rogerio-rsesystems/brand.git
   ```

2. **Read these files in order:**
   - `BRAND_GUIDE.md` — colors, fonts, logo assets, voice, service lines, credentials
   - `RG_Enterprise_Consulting_BRD_v2.0.docx` — full project requirements (extract text)
   - `DECISION_LOG.md` — all locked decisions from previous sessions (if file exists)
   - `SESSION_NOTES.md` — notes from last session (if file exists)

3. **Check the website codebase repo:**
   ```
   https://github.com/rogerio-rsesystems/rgenterpriseconsulting.git
   ```
   (This may be private — user will provide ZIP if needed)

4. **Confirm to the user what phase and task you are picking up**, based on the BRD and Decision Log.

5. **Never hard-code colors, fonts, or content** — always reference design tokens from `BRAND_GUIDE.md`.

---

## Project Overview (quick reference)

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

## Phase Status (update this after each session)

| Phase | Name | Status | Notes |
|-------|------|--------|-------|
| Phase 1 | Brand & Design System | 🔴 Not Started | Blocked on BRD Q1 (colors) and Q2 (fonts) |
| Phase 2 | Services & Lead Generation | 🔴 Not Started | Blocked on Phase 1 |
| Phase 3 | Case Studies & Portfolio | 🔴 Not Started | Blocked on BRD Q4 (client naming) |
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
> "Read the brand repo and continue from where we left off. Last session we completed [X]. Today I want to work on [Y]."

### Option B — Answer open questions
> "Read the brand repo. Here are my answers to the open questions: Q1: [answer], Q2: [answer]..."

### Option C — Start a specific phase
> "Read the brand repo and BRD. Start Phase 1 — Brand & Design System."

---

## Repo File Structure

```
brand/
├── README.md                               ← This file (Claude startup guide)
├── BRAND_GUIDE.md                          ← Colors, fonts, voice, assets spec
├── DECISION_LOG.md                         ← All locked decisions (created when first decision is made)
├── SESSION_NOTES.md                        ← Running notes per session
├── RG_Enterprise_Consulting_BRD_v2.0.docx ← Full Business Requirements Document
├── logo.png.png                            ← Primary logo (for dark backgrounds)
├── logo white.png                          ← White logo variant
├── favicon-32x32.png                       ← Browser favicon
└── social-image.jpg                        ← OG / social share image
```

---

## End-of-Session Checklist for Claude

Before ending any session:
- [ ] Summarize what was built or decided
- [ ] Update `DECISION_LOG.md` with any locked decisions
- [ ] Update `SESSION_NOTES.md` with what was completed and what comes next
- [ ] Update the Phase Status table above if any phase changed status
- [ ] Tell Rogerio which files to commit to this brand repo
- [ ] Tell Rogerio which files to commit to the website codebase repo
