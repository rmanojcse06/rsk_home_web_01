# RSK Enterprises Website — Design Spec
**Date:** 2026-06-30  
**Author:** Copilot (brainstorming session)  
**Status:** Approved

---

## 1. Purpose & Audience

Build a futuristic, minimal single-page website for **RSK Enterprises** to engage **Business Development Executives (BDEs)** in the **US and Canada**. The goal is to present RSK's healthcare BPO services (AR Management, Record Review, Medical Transcription) and convert BDE visits into qualified leads via contact form and live chat.

---

## 2. Services to Promote

RSK Enterprises offers three core services:

1. **Accounts Receivable Management** — Invoice monitoring, payment follow-ups, aging reports, reconciliation, dispute tracking, monthly performance reporting.
2. **Record Review & Documentation Audit** — Verification, gap identification, data extraction, indexing, chronological summaries, compliance checks.
3. **Medical Transcription** — Clinical documentation services for US/Canada healthcare providers.

---

## 3. Architecture & Deployment

| Item | Choice | Rationale |
|---|---|---|
| Structure | Single `index.html` | No build step, zero dependencies, instant deploy |
| Hosting | GitHub Pages (free) | Permanent free hosting, git-based updates |
| CDN | Cloudflare (free) | Global edge, HTTPS, DDoS protection |
| Fonts | Google Fonts CDN | Inter (body) + Space Grotesk (headings) |
| Icons | Inline SVGs | No external library needed |
| Contact Form | Formspree (free) | No backend; email swappable via one ID |
| Chat Widget | Tawk.to (free forever) | Live push notification to Rajkumar's phone |

---

## 4. Visual Design Language

| Token | Value | Usage |
|---|---|---|
| Background | `#FFFFFF` | Page background |
| Surface | `#F0F7FF` | Card backgrounds |
| Primary Blue | `#0057D9` | Headings, buttons, active links |
| Accent Cyan | `#00B4D8` | Highlights, borders, stat glows |
| Text | `#1A1A2E` | Body copy |
| Muted | `#64748B` | Subtext, captions |

**Futuristic minimal touches:**
- Animated gradient bar at top of hero
- Glassmorphism stat cards (blue drop-shadow, subtle border)
- Scroll-triggered fade-in on each section (Intersection Observer)
- Animated number counters on stats
- Thin `1px` blue divider lines between sections
- Sticky nav with `backdrop-filter: blur` on scroll

---

## 5. Page Sections (in order)

### 5.1 Sticky Navigation
- Left: "RSK Enterprises" logo text
- Right: links — Services · Process · Why Us · Contact
- CTA button: "Get a Free Consult" (scrolls to contact form)
- On scroll: nav gains `background: rgba(255,255,255,0.9)` + blur

### 5.2 Hero
- Headline: **"Accelerate Cash Flow. Reduce Risk."**
- Subheadline: "Specialized AR Management, Record Review & Medical Transcription for US & Canadian healthcare providers."
- Two CTAs: "Explore Services" (scroll down) + "Talk to Us" (scroll to contact)
- Background: animated blue gradient blob (CSS keyframe animation)

### 5.3 Stats Bar
Four animated counters, triggered on scroll into view:
- **98%** Documentation Accuracy
- **24hr** Response SLA
- **10 Days** Max Delivery
- **$0** Setup Fee

### 5.4 Services (3 cards)
Each card: icon (inline SVG) + title + 4–5 bullet points + "Learn More" anchor
1. AR Management
2. Record Review & Documentation Audit
3. Medical Transcription

### 5.5 Process (6-step timeline)
Horizontal stepper (vertical on mobile):
1. Secure Data Intake → 2. Account Segmentation → 3. Analytical Review → 4. Exception Identification → 5. Reporting & Insights → 6. Continuous Improvement

### 5.6 Why Choose RSK (5 pillars)
Icon cards in a 5-col grid:
- Dedicated AR Specialists
- Structured Methodology
- Cost-Efficient Outsourcing
- HIPAA/NDA Compliance
- Transparent Reporting

### 5.7 KPIs
Six metric cards with label + description:
- Days Sales Outstanding (DSO)
- Collection Effectiveness Index (CEI)
- Aging Receivable Reduction (30/60/90)
- Invoice Accuracy Rate
- Record Review Accuracy
- Reporting Timeliness

### 5.8 Contact Form
Fields: Full Name · Company · Role/Title · Email · Phone · Message  
Submit button → POST to Formspree endpoint  
Below form: direct contact details (email + phone from PDF)  
**Placeholder comment:** `<!-- REPLACE: Formspree form ID here -->`

### 5.9 Footer
- Left: Logo + tagline "Precision. Performance. Partnership."
- Center: Quick nav links
- Right: Address (Ennore, Chennai-600057) + email + phone
- Bottom: Copyright RSK Enterprises 2026

### 5.10 Tawk.to Live Chat Widget
- Floating chat bubble, bottom-right
- **Placeholder comment:** `<!-- REPLACE: Paste Tawk.to script here -->`
- Fallback instructions: Link to tawk.to signup + 2-step embed guide

---

## 6. Contact Details (from PDF)

```
Rajkumar Singaram — Managing Director
Email: Rajkumarsingaram91@gmail.com
Phone: +91-9900957819
Address: Office No.5, 8th Street, Annai Sivagami Nagar, Ennore, Chennai-600057
```

---

## 7. Updateability

Two clearly marked `<!-- REPLACE -->` comments in the HTML:
1. Formspree form action URL (swap email/form ID)
2. Tawk.to embed script (paste from tawk.to dashboard)

A `README.md` ships alongside with:
- GitHub Pages deployment steps (5 steps)
- Cloudflare CDN setup steps
- How to update Formspree email
- How to embed Tawk.to

---

## 8. Out of Scope

- CMS / blog functionality
- Multi-language support
- Backend / database
- Paid services / e-commerce
- Dark mode toggle (possible future enhancement)

---

## 9. Success Criteria

- Page loads in < 2 seconds (no heavy libraries)
- Works on mobile, tablet, desktop
- All contact form submissions reach Rajkumar's email
- Tawk.to chat live on first deploy
- BDE can find services, understand value prop, and contact RSK in < 60 seconds
