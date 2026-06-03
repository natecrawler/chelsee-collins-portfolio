# Chelsee Collins — Portfolio Website

A fast, accessible, fully-responsive portfolio for graphic designer **Chelsee Collins**,
built with plain HTML, CSS, and a little JavaScript. No build tools, no dependencies —
open it and it works.

## 📁 What's here

```
index.html               Home — hero, featured work, about teaser, CTA
work.html                Full project gallery (5 projects)
about.html               Bio, capabilities, toolkit, experience, education
contact.html             Contact form + email / phone / LinkedIn
project-converse.html    Case study — Converse "Rethink, Reuse, Renew" catalog
project-moma.html        Case study — MoMA April Film Calendar brochure
project-austen.html      Case study — Jane Austen book cover series
project-loops.html       Case study — Loops packaging
project-firefly.html     Case study — Firefly 2020 festival poster
css/style.css            All styling + the design system (colors, type, spacing)
js/main.js               Mobile menu, scroll reveal, form handler
assets/img/              Portrait + favicon
assets/work/             Optimized project images (covers, heroes, galleries)
assets/Chelsee-Collins-Resume.pdf   The real résumé (downloadable site-wide)
```

All real project images and the résumé are already wired in. Total image weight is
~3.8 MB across the whole site (optimized from ~50 MB of source mockups).

## ✏️ Things you may still want to do

1. **(Optional) Add a real portrait photo.** The About page and home About section
   use a designed **brand card** (`<div class="brand-card">…`) instead of a headshot —
   so no photo is required and nothing looks unfinished. If Chelsee ever wants her
   photo there, replace that `<div class="brand-card reveal">…</div>` block in
   `index.html` / `about.html` with:
   ```html
   <div class="media reveal"><img src="assets/img/portrait.jpg" alt="Chelsee Collins" /></div>
   ```
   and drop a ~800×1000 (4:5) photo at `assets/img/portrait.jpg`.
2. **Tweak the case-study copy.** Each `project-*.html` follows a
   **Brief → Approach → Outcome** structure (what hiring managers look for). The text
   is written to fit the work, but feel free to make it more personal or add real
   project details / clients where you have them.
3. **Buy the domain.** The résumé lists `chelseecollins.com` — see hosting below.

## 🖼️ Swapping or adding images

Replace files in `assets/work/`. Naming convention:
- `*-cover.jpg` → 1200×900 (4:3) card thumbnail on Work/Home
- `*-hero.jpg`  → 1600×900 (16:9) case-study banner
- `*-1.jpg, *-2.jpg …` → gallery images inside the case study

JPG, PNG, or WebP all work. Keep file sizes reasonable (under ~300 KB each) for speed.

### Add a brand-new project
1. Copy any `project-*.html` to a new file (e.g. `project-newthing.html`).
2. Edit the heading, eyebrow, facts, copy, and image filenames.
3. Add a card for it in `work.html` (and optionally `index.html`), pointing to the new file.

## 🎨 Rebrand in one place

Open `css/style.css` and edit the variables at the top (`:root`):

```css
--accent: #e0573e;   /* brand accent — recolors the whole site */
--paper:  #faf8f4;   /* page background */
--ink:    #1a1a1a;   /* text */
```

Fonts are **Fraunces** (headings) + **Inter** (body) from Google Fonts — swap them in
the `<head>` `<link>` and the `--font-*` variables.

## ✅ Wire up the contact form (optional, ~2 min)

The form shows a friendly message instead of sending. To make it real, use
**[Formspree](https://formspree.io)** (free):

1. Create a form and copy your endpoint, e.g. `https://formspree.io/f/abcdwxyz`.
2. In `contact.html`, change the `<form …>` tag to:
   ```html
   <form action="https://formspree.io/f/abcdwxyz" method="POST">
   ```
3. Remove the `data-contact-form` attribute so the JS demo handler steps aside.

(The email and phone links already work without any setup.)

## 🚀 Put it online for free

- **Netlify Drop** (easiest): go to <https://app.netlify.com/drop> and drag this whole
  folder onto the page. Live in seconds, with a URL you can rename.
- **GitHub Pages**: create a repo, upload these files, enable Pages
  (Settings → Pages → deploy from `main`).
- **Cloudflare Pages / Vercel**: connect the repo or drag-and-drop.

Then point a custom domain (e.g. `chelseecollins.com`) at the host.

## ♿ Best practices already baked in

- Responsive from 320px to widescreen
- Keyboard accessible — skip-link, focus states, semantic landmarks, ARIA on the menu
- Respects `prefers-reduced-motion`
- SEO + social-share meta tags on every page (with a preview image)
- Lazy-loaded, web-optimized images; system-font fallbacks; no heavy frameworks
- Work-first layout and Brief → Approach → Outcome case studies — structured for hiring

---

Made with care for Chelsee. Everything is plain files — edit away.
