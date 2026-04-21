# Discord Landing Page Clone

**A pixel-faithful recreation of the Discord homepage built entirely with Tailwind CSS and Vite.**

---

## Table of Contents

- [Overview](#overview)
- [Tools and Technologies](#tools-and-technologies)
- [Project Structure](#project-structure)
- [Methods](#methods)
- [Key Features](#key-features)
- [How to Run](#how-to-run)
- [Results and Conclusion](#results-and-conclusion)
- [Future Work](#future-work)
- [Author and Contact](#author-and-contact)

---

## Overview

This project is a front-end clone of the Discord marketing landing page. The goal was to practice utility-first CSS methodology by rebuilding a real-world, production-grade webpage from scratch using Tailwind CSS, without writing a single line of custom CSS beyond the Tailwind directives.

The page replicates Discord's hero section, feature highlights, footer, and responsive layout breakpoints across mobile, tablet, and desktop viewports.

---

## Tools and Technologies

| Tool | Version | Purpose |
|---|---|---|
| HTML5 | — | Page markup and structure |
| Tailwind CSS | v3.2.4 | Utility-first styling |
| PostCSS | v8.4.21 | CSS transformation pipeline |
| Autoprefixer | v10.4.13 | Cross-browser vendor prefixes |
| Vite | v7.0.6 | Dev server and build tooling |
| Node.js | ≥16 | Runtime for build tools |

**Custom fonts used:**
- `gg sans` : Discord's primary UI typeface
- `Ginto` / `Ginto Nord` : display headings
- `Whitney` : body copy fallback

---

## Project Structure

```
discord-tailwind-clone/
│
├── assets/
│   ├── fonts/                  # Custom webfonts (gg-sans, Ginto, Ginto-Nord, Whitney)
│   └── images/                 # SVG illustrations and favicon
│
├── index.html                  # Main page (single-page layout)
├── main.css                    # Tailwind entry point (@tailwind directives)
├── tailwind.config.js          # Tailwind configuration
├── postcss.config.js           # PostCSS plugin configuration
├── package.json                # Project metadata and dependencies
├── .gitignore                  # Git exclusions (node_modules, dist, etc.)
└── README.md                   # This file
```

> **Note:** `node_modules/` is excluded from this repository. Run `npm install` to restore dependencies locally.

---

## Methods

**Utility-First Approach**

Rather than writing component-level CSS classes, every visual property : spacing, color, typography, responsiveness, is expressed directly in HTML using Tailwind's utility classes. This keeps styles co-located with markup and eliminates dead CSS.

**Responsive Design**

Tailwind's responsive prefixes (`sm:`, `md:`, `lg:`, `xl:`) handle all breakpoint transitions. The layout shifts between a stacked single-column view on mobile and a side-by-side two-column grid on desktop.

**PostCSS Pipeline**

`main.css` contains only three lines, the Tailwind directives. At build time, PostCSS scans the HTML for class usage and generates a purged, production-ready stylesheet. Autoprefixer adds vendor prefixes automatically.

**Vite Dev Server**

Vite provides instant hot-module replacement during development and an optimised static bundle for production.

---

## Key Features

- Full responsive layout : tested across mobile (320px) through widescreen (1440px+)
- Five distinct content sections mirroring Discord's actual landing structure
- Custom font stack loaded via `@font-face`, matching Discord's brand typography
- SVG-based hero illustrations layered with CSS `z-index` and absolute positioning
- Sticky-free, scroll-friendly navigation with a transparent-to-solid header effect
- Dark footer with a four-column link grid that collapses to two columns on mobile

---

## How to Run

**Prerequisites:** Node.js v16 or higher

```bash
# 1. Clone the repository
git clone https://github.com/<your-username>/discord-tailwind-clone.git
cd discord-tailwind-clone

# 2. Install dependencies
npm install

# 3. Start the development server
npm run start
```

Then open [http://localhost:5173](http://localhost:5173) in your browser.

To build for production:

```bash
npx vite build
```

Output will be in the `dist/` folder.

---

## Results and Conclusion

The final page closely matches the visual design of the Discord landing page at a component level. Working through this project reinforced several practical skills:

- Internalising Tailwind's spacing and colour scale rather than reaching for arbitrary values
- Understanding how PostCSS and a JIT compiler work together under the hood
- Managing layered SVG assets with Tailwind's positioning and opacity utilities
- Structuring a responsive layout with flex and grid without writing media queries manually

The single-file HTML approach kept the project simple, but it also highlighted where a component-based framework would begin to pay dividends as page complexity grows.

---

## Future Work

- Migrate from a single `index.html` to a component-based architecture (React or Vue) to make sections reusable
- Add a working hamburger menu for the mobile navigation
- Implement smooth scroll and scroll-triggered animations using Framer Motion or vanilla Intersection Observer
- Replace placeholder lorem ipsum copy with the actual Discord marketing text
- Add dark/light mode toggle using Tailwind's `dark:` variant
- Deploy to Vercel or Netlify with a CI/CD pipeline

---

## Author and Contact

Built as part of a front-end skills portfolio, feel free to reach out with questions or feedback.

**Manas Gulati**

- **GitHub:** [github.com/ManasGulati](https://github.com/ManasGulati)
- **LinkedIn:** [linkedin.com/in/manasgulatiryu](https://linkedin.com/in/manasgulatiryu)
- **Email:** manasgulati222@gmail.com

---

> *This is a clone built for educational and portfolio purposes. All Discord branding, design, and assets belong to Discord Inc.*
