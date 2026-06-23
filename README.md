# Anvil & Oak 🪡

**Live Site →** https://buvan-buddu.github.io/Anvil-Oak/

A fully responsive multi-page business website for a fictional handcrafted leather & woodcraft shop based in Dharmapuri, Tamil Nadu — built with pure **HTML, CSS & Bootstrap 5**. No JavaScript frameworks. No build tools. No backend. Just two files.

---

## Live Pages

| Page | Hash Route | Description |
|------|-----------|-------------|
| 🏠 Home | `#home` | Hero banner, 4-step process strip, featured products, newsletter signup |
| 🛍️ Shop | `#shop` | 9-product grid with filter sidebar (category, material, price) and sort dropdown |
| 📖 About | `#about` | Founder story, 3 brand values, 4 team member cards, visit info |
| 🔐 Login | `#login` | Sign-in form with dark split-panel image side |
| 📝 Register | `#register` | Full account creation form — first/last name, email, password confirm |
| 🔑 Forgot Password | `#forgot` | Email reset form |

---

## What Makes This Project Unique

### 1. Zero-JavaScript Page Routing
All 6 pages live inside **one `index.html`** and switch instantly using nothing but CSS — no JavaScript, no React, no frameworks. Built with the CSS `:target` pseudo-selector:

```css
.page          { display: none; }    /* all pages hidden by default  */
.page:target   { display: block; }   /* show whichever page is #targeted */
#home          { display: block; }   /* home is visible by default   */
:target ~ #home { display: none; }  /* hide home when any other page is active */
```

Clicking `href="#shop"` → URL hash changes → CSS detects it → Shop section appears → Home hides. **Zero page reload.**

### 2. CSS Design System with Custom Properties
Every colour and font is stored once in `:root` and reused across the full stylesheet — change the brand colour in one line and the entire site updates:

```css
:root {
  --bg:         #FBF7F1;  /* warm parchment background */
  --ink:        #2B1B12;  /* dark walnut text           */
  --brand:      #8C4A2F;  /* saddle leather brown       */
  --accent:     #C98A2B;  /* brass gold highlights      */
  --line:       #D9C9AE;  /* subtle hairline borders    */

  --font-display: 'Fraunces', serif;
  --font-body:    'Inter', sans-serif;
  --font-mono:    'JetBrains Mono', monospace;
}
```

### 3. Stitch & Rivet Motif — Signature CSS Detail
The decorative dashed border with four brass corner dots on the auth cards is built entirely in CSS — no images, no SVG:

```css
.stitch-frame { border: 1px dashed var(--brand); }  /* the stitch */
.rivet-tl { top: -4px;    left: -4px;  }            /* brass rivets */
.rivet-tr { top: -4px;    right: -4px; }
.rivet-bl { bottom: -4px; left: -4px;  }
.rivet-br { bottom: -4px; right: -4px; }
```

### 4. Three-Role Typography System
Each of the three Google Fonts has a specific design job — not picked randomly:

| Font | Role | Used on |
|------|------|---------|
| **Fraunces** (serif) | Display / editorial | All headings, quotes |
| **Inter** (sans-serif) | Body / readable | Paragraphs, nav, buttons |
| **JetBrains Mono** (monospace) | Labels / technical | Prices, category tags, eyebrows |

### 5. Fully Responsive — Bootstrap 5 Grid
Product cards go from 3 columns → 2 columns → 1 column across screen sizes. Nav collapses to a hamburger on mobile. Auth side-panel hides on small screens. All using Bootstrap's grid classes — `col-md-4`, `col-sm-6`, `navbar-expand-lg`.

---

## Tech Stack

| Technology | Version | Purpose |
|------------|---------|---------|
| HTML5 | — | Page structure |
| CSS3 | — | Design, layout, `:target` routing |
| Bootstrap | 5.3.3 | Grid system, responsive navbar |
| Google Fonts | — | Fraunces, Inter, JetBrains Mono |

---

## File Structure

```
Anvil-Oak/
├── index.html   ← all 6 pages in one file
└── style.css    ← complete design system
```

---

## Run Locally

No install. No terminal. No commands needed.

```
1. Download or clone this repo
2. Open index.html in any browser
3. Done ✅
```

---

## Screenshots

> Home · Shop · About · Login · Register · Forgot Password
> All navigated via URL hash — try clicking the nav links on the live site.

---

## Author

**Buvanraj** — HTML & CSS Internship Project
Ladybird Web Solution Pvt Ltd, Dharmapuri Branch · 2024

---

> *"Built by hand. Built to last."*
