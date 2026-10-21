# AI Context Memory & Quick Reference
## Project: Govt. Graduate College Pattoki Web Portal

---

### Core Architecture & Design Identity
- **Institution:** Govt. Graduate College Pattoki (Kasur District, Punjab, Pakistan).
- **Aesthetic:** "Light Academia" — Classic, slim, full-width multi-page static portal.
- **Global Typography Mandate:** Single global sans-serif font across all pages: **`Plus Jakarta Sans`**. Zero serif fonts anywhere.
- **Routing:** Real multi-page static routing across `index.html`, `about.html`, `academics.html`, `admissions.html`, `sports.html`, and `contact.html`.

---

### Pages Completed
1. `index.html` (Home Page): Slim navbar with 'Home' active, balanced hero, heritage pillars, academic pathways, campus visual gallery, and warm beige footer.
2. `about.html` (About Page): Slim navbar with 'About' active, wide campus hero banner, 2-column history & heritage with asymmetric image grid, Principal's message with portrait placeholder, and 4-box facilities Bento grid.
3. `academics.html` (Academics Page): Slim navbar with 'Academics' active, academic hero banner, split degree programs (Intermediate vs. BS 4-Year), 4 major faculty cards with field imagery, and academic calendar/examination regulations.
4. `admissions.html` (Admissions Page): Slim navbar with 'Admissions' active, admissions banner, live cycle banner, 4 key deadline cards, 3-tab eligibility breakdown (Intermediate, BS 4-Year, Quotas), 5-step visual application roadmap, 4 downloadable PDF archives, transparent institutional fee structure table, accessible Vanilla JS FAQ accordion, and campus helpdesk callout.
5. `contact.html` (Contact Page): Slim navbar with 'Contact' active, collegiate administration banner, 4 contact info cards (address, phones, emails, visiting hours), client-side validated online inquiry form with instant feedback state, 6-department PBX extension directory, visitor protocols, Google Maps campus embed, and warm beige footer.
6. `sports.html` (Sports & Athletics Page): Slim navbar with 'Sports' active, high-contrast dark overlay hero with stark white typography, 4 athletic metrics pills, 3-column facility cards (Cricket Oval, Football Field, Indoor Complex), asymmetric Annual Sports Gala masonry grid, 4-trophy achievement cabinet, and sports quota trials callout.

---

### Mandatory Components & Layout Rules
1. **Slim Full-Width Navbar:**
   - Attached to top: `w-full fixed top-0 bg-white/95 backdrop-blur-md border-b border-stone-200 z-50 px-6 py-3`.
   - Logo strictly centered: `src="./logo.png"` with `h-10 w-auto object-contain`. Zero text next to it.
   - Left Links: Home (`index.html`), About (`about.html`), Academics (`academics.html`).
   - Right Links: Admissions (`admissions.html`), Sports (`sports.html`), Contact (`contact.html`).
2. **Hero Sections:**
   - Dark high-contrast overlays (`bg-slate-900/70 backdrop-blur-[1px]`) and stark white headings (`text-white`) standardized across all internal pages (`about.html`, `academics.html`, `admissions.html`, `sports.html`, `contact.html`).
3. **Footer:**
   - Refined warm beige (`bg-[#F5F2EB]`) with stone borders and dark text linking to all internal pages.
