# Technical Architecture & File System Strategy
## Govt. Graduate College Pattoki — Static Web Architecture

---

### 1. Architectural Principles
The project uses a pure **Modern Static Architecture**. There is no backend runtime, no Node.js server dependencies, and no client-heavy JS frameworks (e.g., React, Next.js, Vue). 

The goal is absolute simplicity, ultra-fast load times, robust SEO, and frictionless deployment to any static host (GitHub Pages, Cloudflare Pages, Netlify, Vercel, or traditional Apache/Nginx web hosting).

---

### 2. File & Directory Structure

```plaintext
project-college/
│
├── index.html                   # Flagship Home Page
├── about.html                   # About the College & Leadership
├── admissions.html              # Admissions, Programs & Merit Lists
├── academics.html               # Faculties, Departments & Curriculum
├── contact.html                 # Contact Directory & Inquiry Form
│
├── assets/
│   ├── css/
│   │   ├── styles.css           # Custom styles, animations & design token overrides
│   │   └── tailwind.css         # Compiled Tailwind or direct configuration bridge
│   │
│   ├── js/
│   │   ├── main.js              # Core UI orchestration (Mobile drawer, header scroll)
│   │   ├── counters.js          # IntersectionObserver stats counter
│   │   ├── accordion.js         # FAQ and curriculum accordion controllers
│   │   └── forms.js             # Client-side validation & UI feedback for forms
│   │
│   ├── images/
│   │   ├── brand/
│   │   │   ├── college-logo.svg # Official vector emblem/insignia
│   │   │   ├── college-logo.png # High-res fallback
│   │   │   └── favicon.ico      # Multi-resolution favicon
│   │   ├── hero/
│   │   │   ├── campus-hero-1.webp
│   │   │   └── campus-hero-2.webp
│   │   ├── leadership/
│   │   │   ├── principal.webp
│   │   │   └── vice-principal.webp
│   │   ├── campus/
│   │   │   ├── science-lab.webp
│   │   │   ├── it-center.webp
│   │   │   ├── central-library.webp
│   │   │   └── sports-complex.webp
│   │   └── icons/
│   │       └── [SVG Icon Sprites or inline SVGs]
│   │
│   └── docs/
│       ├── prospectus-2025.pdf
│       └── sample-merit-list.pdf
│
└── config/
    └── documentation/           # System instructions, design tokens, and PRD
```

---

### 3. Asset Management Strategy

#### 3.1 Styling Engine (Tailwind CSS)
- **Engine:** Tailwind CSS loaded via modern CDN or pre-compiled CLI output.
- **Custom Design Tokens:** Defined cleanly via Tailwind configuration or CSS root variables in `styles.css`.
- **CSS Strategy:** 95% utility-first markup; 5% dedicated CSS for micro-animations (`@keyframes`), custom gradients, and custom scrollbars.

#### 3.2 Typography & Web Fonts
- **Font Delivery:** Preconnected Google Fonts CDN for zero render-blocking delay:
  ```html
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&family=Playfair+Display:ital,wght@0,600;0,700;0,800;1,600&display=swap" rel="stylesheet">
  ```
- **Primary Body Font:** `Plus Jakarta Sans` (ultra-clean geometric modern sans).
- **Institutional Display Font:** `Playfair Display` (editorial serif evoking academic prestige).

#### 3.3 Imagery & Aspect Ratios
- **Format:** Modern `.webp` format with high visual density and small file footprints.
- **Layout Containers:** Explicit aspect-ratio containers (`aspect-[16/9]`, `aspect-[4/3]`, `aspect-[1/1]`) to prevent Cumulative Layout Shift (CLS).
- **Visual Overlays:** Deep emerald and slate semi-transparent gradient overlays (`bg-gradient-to-t from-slate-950/90 via-slate-900/40 to-transparent`) to ensure text contrast over imagery.

#### 3.4 Vector Icons
- High-efficiency inline SVGs from **Lucide** or **Heroicons**.
- Standardized dimensions (`w-5 h-5`, `w-6 h-6`) with `stroke-width="1.75"` for crisp, high-DPI rendering.

---

### 4. Client-Side UI State Management (Vanilla JavaScript)

Because there is no framework-driven virtual DOM, UI state is managed through clean, modular, and accessible Vanilla JavaScript:

```
[User Action] ---> [DOM Event Listener] ---> [State Function] ---> [CSS Class Toggle / ARIA Update]
```

#### 4.1 State Patterns
1. **Header Elevation on Scroll:**
   - Monitored via `window.addEventListener('scroll', ...)` with `requestAnimationFrame` debouncing.
   - Dynamic class toggle: Switches from transparent to frosted glass (`bg-slate-950/90 backdrop-blur-md border-b border-white/10 shadow-lg`).
2. **Mobile Navigation Drawer:**
   - Controlled via `aria-expanded` and a state toggle class on the navigation drawer (`translate-x-0` vs `translate-x-full`).
   - Disables document body scrolling (`overflow-hidden`) when open.
   - Listens for `Escape` key events and backdrop clicks to close.
3. **Animated Number Counters:**
   - Triggered using the `IntersectionObserver` API when the stats section enters the viewport.
   - Smooth numerical tick interpolation over 2000ms.
4. **Accessible Accordions:**
   - Independent component encapsulation using `data-accordion-target` attributes.
   - Updates `aria-expanded="true|false"` and dynamically controls max-height for fluid CSS transitions.
5. **Interactive Tabs (Admissions / Programs):**
   - Click handlers toggle active state on trigger buttons (`bg-emerald-800 text-white` vs `bg-slate-100 text-slate-600`) and unhide corresponding panel containers (`hidden` vs `block`).
