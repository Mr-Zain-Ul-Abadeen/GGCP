# AI Coding Agent Rules & Behavioral Boundaries
## Project: Govt. Graduate College Pattoki

---

### 1. Mandatory Tech Stack & Constraints
1. **Forbidden Frameworks & Libraries:**
   - STRICTLY PROHIBITED: React, Vue, Angular, Svelte, Next.js, Nuxt, Astro.
   - STRICTLY PROHIBITED: jQuery, Lodash, Axios, Bootstrap, Material UI.
   - STRICTLY PROHIBITED: Node.js server runtimes, Express, PHP, Python backends.
2. **Permitted Technologies:**
   - Semantic HTML5, CSS3 with modern CSS variables, Tailwind CSS, modern Vanilla JavaScript (ES6+).
3. **Zero Installation Overhead:**
   - The code must be viewable directly by opening `index.html` in any modern web browser.

---

### 2. Execution Boundaries & Anti-Hallucination Protocol
1. **Strict Phase Adherence:**
   - NEVER generate code for future phases prematurely.
   - NEVER generate multiple HTML pages in a single turn. Work file-by-file with full production quality.
2. **No Placeholder Laziness:**
   - DO NOT output incomplete blocks like `<!-- Add other programs here... -->` or `/* Add more CSS */`.
   - Always output complete, ready-to-run code.
   - Use contextual, realistic college data for Govt. Graduate College Pattoki (e.g., real faculties, regional context, appropriate academic credentials) rather than generic "Lorem Ipsum".
3. **Strict Verification Checkpoint:**
   - After writing any file or section, verify that all open HTML tags are closed, all Tailwind classes exist, and all JS selectors match the corresponding DOM attributes.

---

### 3. Code Style & Formatting Standards

#### 3.1 HTML5 Standards
- All code must pass W3C validation rules.
- Explicit semantic elements (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`) are mandatory. No generic `<div>` soup.
- Every `<img>` tag must include `alt`, `loading="lazy"` (except hero images which use `loading="eager"`), and explicit aspect ratio or dimension classes.
- Form controls must have associated `<label>` elements or descriptive `aria-label` attributes.

#### 3.2 Tailwind CSS Utility Class Ordering
To ensure consistency and ease of maintenance, Tailwind classes must follow a strict outside-in concentric order:
1. **Display & Positioning:** `block`, `flex`, `grid`, `absolute`, `relative`, `fixed`, `inset-0`, `z-10`
2. **Box Model & Sizing:** `w-full`, `max-w-7xl`, `h-auto`, `min-h-screen`, `m-auto`, `p-6`, `space-y-4`, `gap-6`
3. **Typography:** `font-serif`, `font-sans`, `text-3xl`, `font-bold`, `tracking-tight`, `text-slate-900`
4. **Visuals, Backgrounds & Borders:** `bg-slate-900`, `bg-emerald-950/40`, `border`, `border-slate-800`, `rounded-2xl`
5. **Effects & Shadows:** `shadow-xl`, `backdrop-blur-md`, `opacity-90`
6. **Transitions & Interactivity:** `transition-all`, `duration-300`, `ease-out`, `hover:scale-105`, `focus:ring-2`

#### 3.3 Vanilla JavaScript Standards
- Modern ES6+ syntax (`const`, `let`, arrow functions, destructuring, template literals).
- **Defensive DOM Querying:** Always check if an element exists before attaching event listeners:
  ```javascript
  const mobileToggle = document.querySelector('#mobile-menu-toggle');
  if (mobileToggle) {
    mobileToggle.addEventListener('click', handleMenuToggle);
  }
  ```
- No inline JavaScript handlers in HTML (e.g., `onclick="..."` is forbidden). All behavior must reside in dedicated script files or controlled script blocks.
- Wrap scripts in `DOMContentLoaded` or use the `defer` attribute on script tags.

---

### 4. Error Handling & Defensive Frontend Strategy
1. **Asset Fallbacks:**
   - Provide graceful CSS background color fallbacks (`bg-slate-900`) behind all external images so layouts remain visually intact while assets load.
2. **Form Feedback UI:**
   - Provide client-side visual validation states (red ring for invalid fields, green ring for valid fields, animated status message box upon submit) without page reloads.
3. **Responsive Stress Testing:**
   - All navigation bars, grids, and tables must be built mobile-first. Tables must be wrapped in `overflow-x-auto` containers with custom scrollbars.
