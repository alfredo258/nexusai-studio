# CLAUDE.md

## Project Overview

**NexusAI Studio** — Agencia Web AI-Native de Elite. Landing page de servicios profesionales de IA construida con Astro + Tailwind CSS v4. Diseño minimalista premium inspirado en Apple/Vercel.

## Tech Stack

- **Framework**: Astro 5 (latest stable) con SSG
- **Styling**: Tailwind CSS v4 (CSS-first config)
- **Deploy**: Cloudflare Pages
- **Content**: Astro Content Collections para blog
- **Zero JS**: Componentes Astro puros, sin frameworks client-side

## Golden Rules

### 1. Vibe Coding & Velocidad Extrema
- Componentes pequeños, reutilizables, autodocumentados
- Nombres semánticos que hablen por sí mismos
- Iteración rápida: ship > perfect

### 2. Diseño Minimalista Premium
- Paleta: Negro, blanco, un acento (violet-500)
- Tipografía: Inter para body, system mono para code
- Espaciado generoso, jerarquía visual clara
- Animaciones sutiles con CSS (no JS)
- Mobile-first siempre

### 3. GSO/AEO Optimization (AI Search)
- JSON-LD en cada página (Organization, WebSite, Service, FAQPage, Article)
- Meta descriptions optimizadas para citación por IA
- Contenido estructurado con headers semánticos (h1 > h2 > h3)
- FAQ sections con schema markup
- Open Graph + Twitter Cards completos

### 4. Zero JavaScript = Lighthouse 100
- Solo Astro components (`.astro`), no React/Vue/Svelte
- CSS-only animations y interacciones
- Interactividad con `<details>`, `:target`, checkbox hacks
- Chatbot: CSS-only toggle + form action externo
- Imágenes optimizadas con `<picture>` y formatos modernos

### 5. Accesibilidad WCAG AA
- Contraste mínimo 4.5:1
- Focus visible en todos los interactivos
- Skip navigation link
- aria-labels en elementos no textuales
- Semántica HTML5 (nav, main, article, section, aside)

## Project Structure

```
src/
├── layouts/
│   └── Layout.astro          # Base layout con SEO
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
