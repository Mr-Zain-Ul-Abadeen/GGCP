# UI/UX Design System & Visual Specification
## Govt. Graduate College Pattoki

---

### 1. Design Concept & Philosophy
**"Academic Heritage Meets Modern Contemporary Minimalism"**

The visual language balances the dignity, history, and civic gravity of a Pakistani public sector graduate institution with the crisp typography, refined negative space, and sleek micro-interactions of a world-class international university portal.

Key visual pillars:
- **Depth & Atmosphere:** Deep institutional greens and midnight slates accented with warm champagne gold.
- **Editorial Typography:** High-contrast pairing of a regal serif for display titles and a geometric sans for body copy.
- **Subtle Modernism:** Frosted-glass containers, hairline borders (`border-white/10`), and smooth 300ms transitions.

---

### 2. Comprehensive Color Palette

```
 Institutional Green        Midnight Slate           Champagne Gold           Pure Alabaster
    #064E3B                   #0F172A                   #C59B27                   #F8FAFC
┌─────────────────────┐   ┌─────────────────────┐   ┌─────────────────────┐   ┌─────────────────────┐
│                     │   │                     │   │                     │   │                     │
│    Primary Brand    │   │   Secondary Dark    │   │   Prestige Accent   │   │   Surface Light     │
│                     │   │                     │   │                     │   │                     │
└─────────────────────┘   └─────────────────────┘   └─────────────────────┘   └─────────────────────┘
```

#### 2.1 Color Tokens

| Token Name | Hex Code | Tailwind Equivalent | Role & Application |
| :--- | :--- | :--- | :--- |
| **Institutional Emerald** | `#064E3B` | `emerald-900` | Primary brand anchor, header accents, primary buttons. |
| **Deep Forest Green** | `#022C22` | `emerald-950` | Hero dark sections, visual contrast backdrops. |
| **Midnight Slate** | `#0F172A` | `slate-900` | High-contrast text, secondary cards, dark mode foundations. |
| **Abyssal Black** | `#020617` | `slate-950` | Primary dark background, main footer background. |
| **Academic Gold** | `#C59B27` | `amber-600/700` | Accent badges, borders, merit indicators, CTA highlights. |
| **Light Gold Tint** | `#FEF3C7` | `amber-100` | Badge backgrounds, highlighted notice containers. |
| **Pure Alabaster** | `#F8FAFC` | `slate-50` | Primary light section backgrounds. |
| **Subtle Border Gray**| `#E2E8F0` | `slate-200` | Light-mode card dividers, table borders. |
| **Glass White** | `rgba(255,255,255,0.08)` | `white/10` | Hairline borders on dark backdrops. |

---

### 3. Typography System

#### 3.1 Font Families
- **Display & Headings:** `Playfair Display`, serif
  - *Usage:* Hero titles, section headers, Principal quote blocks, award titles.
  - *Characteristics:* High contrast, elegant brackets, authoritative collegiate feel.
- **Body & UI Elements:** `Plus Jakarta Sans`, -apple-system, sans-serif
  - *Usage:* Navigation links, body copy, stats numbers, buttons, form inputs, tables.
  - *Characteristics:* Wide aperture, crisp legibility at small sizes, modern geometry.

#### 3.2 Type Scale & Hierarchy

| Element | Size | Weight | Line Height | Tracking | Font Family |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Hero Title (Display 1)** | `3.5rem` – `4.5rem` (56–72px) | Bold (700) | `1.1` | `-0.02em` | Playfair Display |
| **Section Title (H2)** | `2.25rem` – `3.0rem` (36–48px) | Bold (700) | `1.2` | `-0.01em` | Playfair Display |
| **Card Header (H3)** | `1.25rem` – `1.5rem` (20–24px) | SemiBold (600) | `1.3` | `normal` | Plus Jakarta Sans |
| **Subtitle / Overline** | `0.875rem` (14px) | Bold (700) | `1.5` | `0.1em` (UPPERCASE) | Plus Jakarta Sans |
| **Body Regular** | `1.0rem` (16px) | Regular (400) | `1.65`| `normal` | Plus Jakarta Sans |
| **Body Small / Captions** | `0.875rem` (14px) | Medium (500) | `1.5` | `normal` | Plus Jakarta Sans |

---

### 4. UI Components & Visual Stylings

#### 4.1 Buttons & Interactive Elements
- **Primary CTA (Gold Accent):**
  - Classes: `inline-flex items-center justify-center px-6 py-3.5 rounded-xl bg-amber-600 hover:bg-amber-500 text-white font-semibold shadow-lg shadow-amber-600/25 transition-all duration-300 hover:-translate-y-0.5 active:translate-y-0`
- **Secondary CTA (Emerald Prestige):**
  - Classes: `inline-flex items-center justify-center px-6 py-3.5 rounded-xl bg-emerald-900 hover:bg-emerald-800 text-emerald-50 font-semibold shadow-lg shadow-emerald-950/20 transition-all duration-300 hover:-translate-y-0.5`
- **Ghost Button (Glassmorphic):**
  - Classes: `inline-flex items-center justify-center px-6 py-3.5 rounded-xl bg-white/10 hover:bg-white/20 text-white font-medium backdrop-blur-sm border border-white/15 transition-all duration-300`

#### 4.2 Content Cards
- **Light Theme Cards:**
  - `bg-white rounded-2xl p-8 border border-slate-200/80 shadow-sm hover:shadow-xl hover:border-emerald-700/30 transition-all duration-300 hover:-translate-y-1`
- **Dark / Glassmorphic Cards:**
  - `bg-slate-900/60 backdrop-blur-md rounded-2xl p-8 border border-white/10 shadow-2xl hover:border-amber-500/40 transition-all duration-300 hover:-translate-y-1`

#### 4.3 Image Treatments & Overlays
- **Rounded Geometry:** All featured imagery must use `rounded-2xl` or `rounded-3xl` with `overflow-hidden`.
- **Prestige Dual Gradients:** Images must be overlaid with subtle gradient masks to ensure text legibility:
  `bg-gradient-to-t from-slate-950 via-slate-950/40 to-transparent`
- **Decorative Badges:** Floating badges on image corners (`absolute top-4 left-4 bg-emerald-900/90 backdrop-blur-md text-emerald-100 text-xs font-bold px-3 py-1.5 rounded-full border border-emerald-500/30`).

---

### 5. Motion & Micro-Interactions

| Interaction | Target | Transition Property | Easing & Duration |
| :--- | :--- | :--- | :--- |
| **Card Hover Lift** | Program & News Cards | `transform: translateY(-4px)`, `box-shadow` | `cubic-bezier(0.16, 1, 0.3, 1)`, 300ms |
| **Button Scale** | Primary/Secondary CTAs | `transform: translateY(-2px)` | `ease-out`, 200ms |
| **Navbar Blur In** | Header Navigation | `background-color`, `backdrop-filter`, `border` | `ease-in-out`, 300ms |
| **Accordion Expansion**| FAQ & Curriculum Panels | `max-height`, `opacity` | `ease-in-out`, 350ms |
| **Mobile Drawer Slide**| Navigation Overlay | `transform: translateX(0)` | `cubic-bezier(0.16, 1, 0.3, 1)`, 300ms |
