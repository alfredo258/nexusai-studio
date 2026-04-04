# CLAUDE.md — The Outbound Force

## Identidad
Agencia de outbound sales B2B. Llenamos la agenda de reuniones de nuestros clientes con prospectos calificados usando LinkedIn, Email, Meta Ads y Google Ads.

**URL:** https://theoutboundforce.com
**Stack:** Astro 5 + CSS puro (sin Tailwind) + Cloudflare Pages
**Contenido:** Español (mercado Argentina/LATAM)

## Reglas de Diseño

### Estética
- Diseño premium B2B inspirado en Clay, Linear, Stripe (VoltAgent design-md como referencia)
- Fondo warm cream (#faf9f7) como Clay
- Un solo color acento: violet (#6d28d9) — solo en CTAs e interacciones
- Tipografía: DM Sans (body) + Space Mono (labels)
- Zero JavaScript excepto: scroll reveals, counters, mobile menu, magnetic buttons
- Mobile-first, Lighthouse 100

### Reglas Estrictas
- NUNCA cambiar CSS sin ver el resultado en el browser primero (usar --chrome)
- NUNCA agregar decoración sin justificación (blobs, gradients, shimmer = NO)
- SIEMPRE planificar antes de ejecutar (usar /plan)
- SIEMPRE commitear antes de cambios grandes
- Imágenes en WebP con lazy-loading
- Animaciones máx 300ms, easing cubic-bezier(0.16, 1, 0.3, 1)

### Componentes Visuales
- Buscar referencia en Aceternity UI o Magic UI antes de crear componentes "wow"
- Cards con border oat (#dad4c8), radius 20px, sin sombras pesadas
- Botones con hover rotation Clay (-3deg + hard shadow)
- Shadow-as-border: box-shadow 0 0 0 1px en vez de CSS border

## Estructura del Proyecto
```
src/
├── layouts/Layout.astro      — Base con meta tags, JSON-LD, fonts
├── components/               — Un componente por sección
│   ├── Header.astro
│   ├── Hero.astro
│   ├── Stats.astro
│   ├── Services.astro
│   ├── Process.astro
│   ├── Testimonials.astro
│   ├── Clients.astro
│   ├── FAQ.astro
│   ├── Calendar.astro
│   └── Footer.astro
├── pages/index.astro         — Ensamblaje + scripts
├── styles/
│   ├── global.css            — Import del CSS activo
│   └── tof-v2.css            — Design system actual (Clay-based)
└── content/blog/             — Blog posts (pendiente actualizar)
```

## Comandos
```bash
npm run dev      # Dev server (localhost:4321)
npm run build    # Build producción
npm run preview  # Preview build
```

## Assets
- Avatares: public/assets/images/avatar-*.png
- Logos clientes: public/assets/images/gallery01/
- Referencia visual: design-md/ (54 design systems de VoltAgent)

## Datos Reales de TOF
- +500 reuniones agendadas
- +30 empresas confían
- x10 leads calificados
- +8 mercados alcanzados
- Google Calendar: https://calendar.app.google/Jxg7er6LkiL6tGEw6
- Email: alfredo@theoutboundforce.com
- LinkedIn: https://www.linkedin.com/company/the-outbound-force
- GA4: G-V0C9DB2TVB
