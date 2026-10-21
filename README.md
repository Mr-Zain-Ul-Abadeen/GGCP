# Govt. Graduate College Pattoki (GGCP) — Official Web Portal

A modern, highly visual, multi-page static web application built for **Govt. Graduate College Pattoki** (Kasur District, Punjab, Pakistan). 

Designed with an **"Academic Prestige / Light Academia"** aesthetic, featuring a unified sans-serif typographic system, high-contrast dark hero banners, a slim frosted-glass navbar, and responsive collegiate modules.

---

## 🏛️ Project Overview

- **Institution:** Govt. Graduate College Pattoki (Established 1970)
- **Governance:** Higher Education Department (HED), Government of the Punjab
- **Affiliations:** University of the Punjab (PU), Board of Intermediate & Secondary Education (BISE) Lahore
- **Tech Stack:** Semantic HTML5, Tailwind CSS (via CDN), Vanilla JavaScript (ES6+)
- **Design Philosophy:** Pure static zero-build architecture, zero framework bloat, instant browser execution.

---

## 📄 Site Structure & Pages

The application is structured as a multi-page static website with 6 internal pages:

| Page | File | Description |
| :--- | :--- | :--- |
| **Home** | [`index.html`](index.html) | Institutional flagship layout with hero video/image, key pillars, academic pathways, campus life gallery, and admissions CTA. |
| **About** | [`about.html`](about.html) | Heritage narrative since 1970, Principal's executive address, core values, and a 4-box campus facilities Bento grid. |
| **Academics** | [`academics.html`](academics.html) | Intermediate (BISE Lahore) vs. BS 4-Year Honors curricula, faculty cards, and semester examination guidelines. |
| **Admissions** | [`admissions.html`](admissions.html) | Fall cycle announcement, 3-tab eligibility breakdown, 5-step application roadmap, official PDF downloads, and fee structure table. |
| **Sports** | [`sports.html`](sports.html) | Cricket Oval, Football Stadium, Indoor Complex, Annual Sports Gala masonry showcase, and Collegiate Trophy Cabinet. |
| **Contact** | [`contact.html`](contact.html) | Campus address, departmental PBX extensions, interactive validated inquiry form, visitor protocols, and responsive Google Map. |

---

## 🎨 Design & Typographic Tokens

- **Global Typography:** Single global font family: **`Plus Jakarta Sans`** strictly across all headings, body text, and interfaces (zero serif fonts).
- **Global Theme:** Light Academia:
  - Backgrounds: `#FDFBF7` (Academic Cream), `bg-white`, `bg-stone-50`, `#F5F2EB` (Warm Beige)
  - Text & Accents: `text-stone-800`, `text-emerald-950`, `bg-emerald-900`, `border-stone-200`
  - Hero Banners: High-contrast dark overlays (`bg-slate-900/70`) paired with stark white headings (`text-white`) for legibility.
- **Master Header:** Slim full-width edge-to-edge navbar (`bg-white/95 backdrop-blur-md border-b border-stone-200`) with centered logo and balanced 3-left / 3-right navigation distribution.

---

## 🚀 Getting Started & Local Preview

This project requires **zero build steps, zero node_modules, and zero local servers**.

### Direct Browser Execution
Simply double-click or open `index.html` in any modern web browser (Google Chrome, Mozilla Firefox, Microsoft Edge, Safari).

### Quick Local Server (Optional)
If you prefer running via a local development server:

```bash
# Using Python 3
python -m http.server 8000

# Using Node.js npx serve
npx serve .
```
Then visit `http://localhost:8000` in your browser.

---

## 📁 Repository Directory Structure

```text
GGCP/
├── index.html          # Flagship Home Page
├── about.html          # About & Institutional Heritage
├── academics.html      # Academic Programs & Faculty Directory
├── admissions.html     # Admissions, Merit Lists & Fee Structure
├── sports.html         # Sports Facilities, Gala & Trophy Cabinet
├── contact.html        # Contact Info, Inquiry Form & Campus Map
├── logo.png            # Official College Crest (High-Res Transparent PNG)
├── README.md           # Project Documentation
├── PRD.md              # Product Requirements Document
├── architecture.md     # Technical Architecture & File Hierarchy
├── design.md           # Color Palettes, Typography & Spacing Rules
├── phases.md           # Implementation Roadmap & Milestone Tracker
└── memory.md           # Context Memory & Component Parity Log
```

---

## 📜 License & Accreditation

Developed for **Govt. Graduate College Pattoki**, Higher Education Department, Government of the Punjab. All rights reserved.
