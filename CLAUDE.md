# CLAUDE.md

## Project Overview

**The Outbound Force (TOF)** — AI-Powered Outbound Sales Automation. We build the pipeline, you close the deals. Landing page built with Astro + Tailwind CSS v4. Premium minimalist design inspired by Apple/Vercel/Linear.

## Tech Stack

- **Framework**: Astro 5 (latest stable) with SSG
- **Styling**: Tailwind CSS v4 (CSS-first config)
- **Deploy**: Cloudflare Pages
- **Content**: Astro Content Collections for blog
- **Zero JS**: Pure Astro components, no client-side frameworks

## Golden Rules

### 1. Vibe Coding & Extreme Speed
- Small, reusable, self-documenting components
- Semantic names that speak for themselves
- Fast iteration: ship > perfect

### 2. Premium Minimalist Design
- Palette: Black, white, violet-500 accent
- Typography: Inter for body, system mono for code
- Generous spacing, clear visual hierarchy
- Subtle CSS animations (no JS)
- Mobile-first always

### 3. GSO/AEO Optimization (AI Search)
- JSON-LD on every page (Organization, WebSite, Service, FAQPage, Article)
- Meta descriptions optimized for AI citation
- Structured content with semantic headers (h1 > h2 > h3)
- FAQ sections with schema markup
- Complete Open Graph + Twitter Cards

### 4. Zero JavaScript = Lighthouse 100
- Only Astro components (`.astro`), no React/Vue/Svelte
- CSS-only animations and interactions
- Interactivity with `<details>`, `:target`, checkbox hacks
- Chatbot: CSS-only toggle + external form action
- Optimized images with `<picture>` and modern formats

### 5. Accessibility WCAG AA
- Minimum contrast 4.5:1
- Visible focus on all interactive elements
- Skip navigation link
- aria-labels on non-text elements
- HTML5 semantics (nav, main, article, section, aside)

## Project Structure

```
src/
├── layouts/
│   └── Layout.astro          # Base layout with SEO
├── components/
│   ├── Header.astro
│   ├── Hero.astro
│   ├── Services.astro
│   ├── Chatbot.astro
│   ├── BlogPreview.astro
│   ├── Footer.astro
│   └── JsonLd.astro
├── pages/
│   ├── index.astro
│   └── blog/
│       └── [...slug].astro
├── content/
│   └── blog/
│       └── *.md
└── styles/
    └── global.css            # Tailwind v4 imports
```

## Commands

```bash
npm run dev      # Dev server
npm run build    # Production build
npm run preview  # Preview production build
```
