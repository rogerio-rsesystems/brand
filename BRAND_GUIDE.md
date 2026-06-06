# RG Enterprise Consulting — Brand Guide
**Version:** 2.0 (June 2026)  
**Owner:** Rogerio Laureano Gomes, Founder & Principal Consultant  
**Website:** rgenterpriseconsulting.com  
**Email:** rogerio@rgenterpriseconsulting.com  
**Phone / WhatsApp:** +1 (310) 430-6698  
**LinkedIn (Personal):** https://www.linkedin.com/in/rogeriogomes/  
**LinkedIn (Company):** https://www.linkedin.com/company/rg-enterprise-consulting/  

---

## 1. Logo Assets

| File | Usage |
|------|-------|
| `logo.png.png` | Primary logo — currently black, works on white backgrounds |
| `logo white.png` | White version — use on dark/navy backgrounds |
| `favicon-32x32.png` | Browser favicon |
| `social-image.jpg` | Open Graph / social share image |

**Current logo notes:**
- Logo is horizontal format with company name
- Currently only available as PNG (no SVG source yet)
- TODO Phase 1: Confirm logo works well on white background; may need a navy-on-white version

---

## 2. Color Palette ✅ LOCKED

| Token Name | Hex | Usage |
|------------|-----|-------|
| `--color-primary` | `#1B2A4A` | Navy — navbar, headings, dark sections, footer |
| `--color-accent` | `#C8A84B` | Gold — CTA buttons, highlights, dividers, accent text |
| `--color-accent-light` | `#E8C96A` | Light Gold — hover states, soft accents |
| `--color-accent-cream` | `#FDFAF3` | Cream — stats bars, alternating section backgrounds |
| `--color-bg` | `#FFFFFF` | White — primary page background |
| `--color-bg-alt` | `#F7F8FC` | Light gray-blue — hero section, alternating sections |
| `--color-text` | `#1B2A4A` | Navy — primary headings (same as primary) |
| `--color-text-body` | `#4A5568` | Dark gray — body paragraphs |
| `--color-text-muted` | `#64748B` | Medium gray — secondary text, labels, captions |
| `--color-border` | `#E2E8F0` | Light border — card borders, dividers |
| `--color-navy-light` | `#2A3F6F` | Lighter navy — hover states on dark surfaces |

### Tailwind CSS custom config
```js
colors: {
  primary: '#1B2A4A',
  accent: {
    DEFAULT: '#C8A84B',
    light: '#E8C96A',
    cream: '#FDFAF3',
  },
  navy: {
    DEFAULT: '#1B2A4A',
    light: '#2A3F6F',
  }
}
```

---

## 3. Typography ✅ LOCKED

| Role | Font | Weight | Size (desktop) |
|------|------|--------|----------------|
| **Headings (H1, H2)** | Montserrat | 800 (ExtraBold) | H1: 56px, H2: 36px |
| **Headings (H3)** | Montserrat | 700 (Bold) | 24px |
| **Navigation / UI labels** | Montserrat | 600 (SemiBold) | 14px |
| **Body text** | Inter | 400 (Regular) | 16px |
| **Body emphasis** | Inter | 500 (Medium) | 16px |
| **Buttons** | Inter | 600 (SemiBold) | 14px |
| **Eyebrow / captions** | Inter | 600 (SemiBold) | 12px, uppercase, letter-spacing 0.08em |

### Google Fonts import
```html
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@600;700;800&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
```

### Tailwind fontFamily config
```js
fontFamily: {
  heading: ['Montserrat', 'sans-serif'],
  body: ['Inter', 'sans-serif'],
}
```

---

## 4. Component Specs

### Buttons
| Type | Background | Text | Border | Border Radius |
|------|-----------|------|--------|---------------|
| Primary CTA | `#C8A84B` Gold | `#1B2A4A` Navy | none | 9999px (pill) |
| Secondary / Outline | transparent | `#1B2A4A` Navy | 1.5px `#1B2A4A` | 9999px (pill) |
| Dark surface outline | transparent | `#fff` | 1.5px `#fff` | 9999px (pill) |

### Navbar
- Background: `#1B2A4A` (navy), sticky
- Logo: white variant (`logo white.png`)
- Nav links: `#93c5fd` light blue-white, hover `#fff`
- CTA button: Gold primary pill
- Height: 64px desktop, 56px mobile

### Section Backgrounds (alternating pattern)
1. White `#FFFFFF` — hero, service detail
2. Light gray-blue `#F7F8FC` — services grid, about intro
3. Cream `#FDFAF3` — stats bar, testimonials
4. Navy `#1B2A4A` — CTA sections, footer

### Dividers / Accents
- Gold horizontal rule: `2px solid #C8A84B`
- Section eyebrow text: Montserrat 600, uppercase, `#C8A84B`, letter-spacing 0.08em

---

## 5. Voice & Tone

- **Professional but direct** — Rogerio speaks plainly and confidently, not corporate-stiff
- **Credibility-first** — lead with proof (Wharton, Vistra, Equifax, Datavant), not claims
- **Action-oriented** — every section ends with a clear next step
- **Global-ready** — English primary; Rogerio is fluent in Portuguese and Spanish

### Messaging Hierarchy
1. **Who we serve:** Mid-market companies and PE-backed firms navigating M&A, AI transformation, and digital change
2. **What we do:** Program leadership and transformation advisory — we don't just advise, we execute
3. **Why us:** 15+ years of enterprise delivery, Wharton M&A credentials, active practitioner (currently leading Vistra integration)
4. **How:** On-demand consultant network — boutique flexibility, enterprise-grade rigor

---

## 6. Service Lines ✅ LOCKED

| # | Service | Short Label | Primary SEO Target |
|---|---------|------------|-------------------|
| 1 | Post-Merger Integration | PMI / M&A Integration | post-merger integration consultant |
| 2 | AI Readiness & Corporate AI Strategy | AI Readiness | AI readiness assessment consulting |
| 3 | Digital Transformation & Technology Integration | Digital Transformation | digital transformation consulting |
| 4 | Business Transformation & Organizational Strategy | Business Transformation | business transformation consulting |

---

## 7. Key Credentials (use on website)

- Wharton School, University of Pennsylvania — M&A and Corporate Development Strategy (2025)
- Georgia Institute of Technology, Scheller College — Business Analytics Graduate (2024)
- Stanford Graduate School of Business — Executive Leadership Development (2022)
- UCLA Extension — Project Management Certification (2013)
- Scrum Master & Product Owner certified
- Fluent: English, Portuguese, Spanish. Advanced: Italian

---

## 8. Key Past Employers (for social proof — naming permission TBD per BRD Q4)

- Vistra Group Asia (current — M&A Integration Consultant via The Barton Partnership)
- Equifax Inc. (Delivery Manager Consultant via UST Global)
- Datavant, Inc. (Portfolio Manager, CIO Office)
- Verifone Inc. (Global Operations PMO)
- ARRIS Group Inc.
- Pace Americas Inc.

---

## 9. Asset TODO List

- [ ] Logo SVG source file (currently PNG only)
- [ ] Confirm logo renders well on white background (currently optimized for dark)
- [ ] Professional headshot of Rogerio (locally hosted, not LinkedIn CDN)
- [ ] Real client testimonials (BRD Q3 — using placeholder quotes until available)
- [ ] Permission to name past employers on website (BRD Q4)
- [ ] Calendly URL (BRD Q6)
- [ ] Email provider decision for lead notifications (BRD Q7)
