# Design System: The Outbound Force

## 1. Visual Theme & Atmosphere

The Outbound Force's website is a light-mode, violet-infused B2B sales platform — a design that bridges approachability and authority. The page opens on a soft lavender-tinted canvas (`#fafafc` blending through `#f5f1ff` into `#f5f3ff`) with a body gradient that creates an almost atmospheric, cloud-like backdrop. White cards (`#ffffff`) float on this tinted surface with violet-tinted borders (`rgba(109, 40, 217, 0.08)`) and shadows (`rgba(109, 40, 217, 0.06–0.12)`), creating a cohesive brand-colored depth system where even elevation feels on-brand.

The typography is built on a dual-font system: **Outfit** for display and headings — a geometric sans-serif with aggressive negative letter-spacing (-2px at hero sizes, -1.2px at section sizes) that creates dense, authoritative headlines — and **DM Sans** for body copy, providing excellent readability at text sizes. Both are Google Fonts, loaded asynchronously with a print-media swap technique for performance.

The hero section features "The Pipeline" — a premium animation system with morphing gradient blobs, glassmorphism notification cards that float with clip-path reveals and staggered cubic-bezier timing, and pulse connection lines. The Process section has a dark background (`#0b0a10`) with dual animated panels simulating Gmail and LinkedIn interfaces — a direct visual metaphor for the outbound workflow. A hand-drawn SVG cat mascot with glasses sits at a desk near the calendar section, toggling between sleeping and working states via CSS checkbox hack.

**Key Characteristics:**
- Outfit (display) + DM Sans (body) dual-font system with negative letter-spacing at display sizes
- Light-mode violet-tinted canvas with body gradient from `#fafafc` through `#f5f1ff` to `#f5f3ff`
- White cards with violet-tinted shadows: `rgba(109, 40, 217, 0.06–0.12)` — elevation is brand-colored
- Single brand color: Violet 700 (`#6d28d9`) as the dominant accent across all interactive elements
- Morphing blob backgrounds with `filter: blur(60px)` and organic border-radius keyframes
- Glassmorphism cards: `rgba(255,255,255,0.85)` + `backdrop-filter: blur(16px) saturate(180%)`
- Dark section (`#0b0a10`) for Process with animated Gmail/LinkedIn panels as background
- Custom SVG mascot (cat with glasses) with CSS-only sleep/wake state toggle
- Scroll-triggered `.reveal` animations with `cubic-bezier(0.16, 1, 0.3, 1)` easing
- Infinite marquee testimonials and client logos with CSS `translateX(-50%)` loops
- Google Calendar integration with time-slot pills linking to real booking

## 2. Color Palette & Roles

### Primary
- **Background** (`#fafafc`): Page base. Not white — a barely-perceptible blue-cool tint that prevents sterility.
- **Background Violet** (`#f5f1ff`): Gradient midpoint. Soft lavender wash that ties the background to the brand.
- **Background Violet 2** (`#ede5ff`): Deeper violet tint for surface variation.
- **Background Dark** (`#0b0a10`): Process section background. Near-black with a blue-purple undertone — the darkest canvas in the system.
- **Card White** (`#ffffff`): Card and elevated surface backgrounds. Pure white for maximum contrast against the tinted canvas.

### Brand Violet Scale
- **Violet 900** (`#3b0764`): Deepest violet. Reserved for extreme emphasis or very dark text on light violet surfaces.
- **Violet 700** (`#6d28d9`): **Primary brand color**. CTA backgrounds, stat numbers, nav CTA, key interactive elements. The anchor of the entire system.
- **Violet 600** (`#7c3aed`): Secondary interactive. Section labels, icon accents, calendar top-bar gradient, service tags, focus states.
- **Violet 500** (`#8b5cf6`): Tertiary accent. Stars, hero badge dot pulse, gradient endpoints, SVG mascot glow.
- **Violet 400** (`#a78bfa`): Soft accent. Process section label color, timeline glow, dark-section text accents.
- **Violet 300** (`#c4b5fd`): Decorative. Cat mascot body fill, pulse line gradients.
- **Violet 200** (`#ddd6fe`): Light border. Hero badge border, ghost button border, floating element borders.
- **Violet 100** (`#ede9fe`): Surface tint. Icon wrap borders, service tag borders, time-slot borders, calendar icon background borders.
- **Violet 50** (`#f5f3ff`): Lightest tint. Icon backgrounds, badge backgrounds, time-slot backgrounds, service tag backgrounds.

### Text
- **Primary** (`#1a1625`): Headings and strong text. A warm near-black with a subtle purple undertone — not pure black.
- **Secondary** (`#4a4458`): Body text, descriptions. Medium-weight purple-tinted dark gray.
- **Muted** (`#7c7591`): Tertiary text, nav links, footer text, captions. Distinctly violet-gray.

### Borders & Shadows
- **Card Border** (`rgba(109, 40, 217, 0.08)`): Default card and container border. Violet-tinted transparency.
- **Card Hover** (`rgba(109, 40, 217, 0.18)`): Intensified border on hover states.
- **Section Border** (Violet 100 `#ede9fe`): Stats bar top/bottom borders, premium dividers.
- **Shadow Light** (`0 8px 30px rgba(109, 40, 217, 0.06)`): Default card shadow — soft violet ambient.
- **Shadow Medium** (`0 12px 40px rgba(109, 40, 217, 0.12)`): Card hover shadow — intensified violet.
- **Shadow Heavy** (`0 20px 60px rgba(109, 40, 217, 0.08)`): Calendar visual card — deep violet elevation.
- **Shadow CTA** (`0 4px 20px rgba(109, 40, 217, 0.25)` → hover: `0 8px 35px rgba(109, 40, 217, 0.4)`): Button shadow system.
- **Shadow Nav** (`0 4px 30px rgba(0, 0, 0, 0.06)`): Scrolled nav shadow — neutral, not brand-tinted.

### Dark Section (Process)
- **Background** (`#0b0a10`): Section fill. Cool near-black.
- **Surface** (`rgba(255, 255, 255, 0.04)`): Process step card backgrounds.
- **Border** (`rgba(139, 92, 246, 0.12)` → hover: `rgba(139, 92, 246, 0.3)`): Semi-transparent violet borders on dark.
- **Text Primary** (`#ffffff`): Headings on dark.
- **Text Secondary** (`rgba(255, 255, 255, 0.5)`): Body text on dark.
- **Glow** (`0 0 30px rgba(139, 92, 246, 0.2)` → hover: `0 0 50px rgba(139, 92, 246, 0.4)`): Step number glow.

### Status & Accent (Pipeline Cards)
- **Green** (`#dcfce7` bg / `#16a34a` icon): Meeting confirmed, success states.
- **Blue** (`#dbeafe` bg / `#2563eb` icon): LinkedIn, new lead.
- **Violet** (`#ede9fe` bg / `#7c3aed` icon): Email, proposals.
- **Amber** (`#fef3c7` bg / `#d97706` icon): Metrics, achievements.

## 3. Typography Rules

### Font Family
- **Display**: `Outfit`, with fallback: `sans-serif`
- **Body**: `DM Sans`, with fallback: `sans-serif`
- **Loading**: Google Fonts async via `media="print" onload="this.media='all'"` technique
- **Weights loaded**: Outfit 500, 700, 800 | DM Sans 400, 500, 700

### Hierarchy

| Role | Font | Size | Weight | Line Height | Letter Spacing | Notes |
|------|------|------|--------|-------------|----------------|-------|
| Hero Headline | Outfit | clamp(2.6rem, 5.5vw, 4.2rem) | 900 | 1.05 (ultra-tight) | -2px | Maximum impact, gradient text for emphasis |
| Section Title | Outfit | clamp(2rem, 3.8vw, 2.8rem) | 800 | 1.10 (tight) | -1.2px | Feature section headings |
| Calendar Title | Outfit | clamp(1.8rem, 3vw, 2.4rem) | 800 | 1.10 (tight) | -1px | CTA section heading |
| Card Heading | Outfit | 1.25rem | 700 | inherit | -0.3px | Service cards, process steps |
| Service Label | Outfit | 0.85rem | 700 | inherit | 3px | `text-transform: uppercase`, section labels |
| Nav Logo | Outfit | 1.3rem | 800 | inherit | -0.5px | Brand name in navigation |
| Nav Link | Outfit | 0.82rem | 500 | inherit | 0.3px | Navigation links |
| Stat Number | Outfit | 3rem | 900 | inherit | -1px | Counter stats, maximum visual weight |
| Stat Label | Outfit | 0.85rem | 600 | inherit | 1.5px | `text-transform: uppercase`, stat descriptions |
| Process Tag | Outfit | 0.68rem | 600 | inherit | 2px | `text-transform: uppercase`, step labels |
| Service Tag | Outfit | 0.68rem | 600 | inherit | normal | Pill tags on service cards |
| Button | Outfit | 0.95rem | 600 | inherit | normal | CTA buttons |
| Body Large | DM Sans | 1.1rem | 400 | 1.75 | normal | Hero subtitle, section descriptions |
| Body | DM Sans | 0.95–1.05rem | 400 | 1.70 | normal | Standard reading text, card descriptions |
| Body Small | DM Sans | 0.92rem | 400 | 1.70 | normal | Testimonial text, process step descriptions |
| Caption | DM Sans | 0.82rem | 400 | inherit | normal | Footer text, nav CTA |
| Testimonial Name | Outfit | 0.92rem | 700 | inherit | normal | Author names |
| Testimonial Role | DM Sans | 0.78rem | 400 | inherit | normal | Author title/company |
| Pipe Card Title | DM Sans | 12px | 700 | 1.30 | normal | Floating notification card headings |
| Pipe Card Sub | DM Sans | 10px | 400 | inherit | normal | Notification card secondary text |

### Principles
- **Dual-font role clarity**: Outfit handles all structural/navigational/display text; DM Sans handles all reading/body text. There is no crossover — the boundary is strict.
- **Weight 900 as hero signature**: Unlike most systems that cap at 700-800, TOF uses 900 (black) for the hero headline and stat numbers, creating a uniquely heavy, attention-demanding top of the hierarchy.
- **Progressive tracking**: Letter-spacing is tightly negative at display (-2px), moderate at section (-1.2px), slightly negative at card (-0.3px), and positive at labels (+1.5px to +3px). This creates a rhythmic tension between compressed headlines and airy labels.
- **Uppercase for taxonomy**: Section labels, stat labels, process tags, and service tags all use `text-transform: uppercase` with expanded letter-spacing. This creates a clear visual "category" voice distinct from content text.
- **Fluid hero sizing**: `clamp()` functions create smooth responsive scaling without breakpoint jumps for the three key heading sizes.

## 4. Component Stylings

### Buttons

**Primary (Gradient)**
- Background: `linear-gradient(135deg, #6d28d9, #8b5cf6)`
- Text: `#ffffff`
- Padding: 0.95rem 2rem
- Radius: 12px
- Shadow: `0 4px 20px rgba(109, 40, 217, 0.25), inset 0 1px 0 rgba(255, 255, 255, 0.15)`
- Hover: translateY(-2px) + shadow `0 8px 35px rgba(109, 40, 217, 0.4)`
- Font: Outfit 0.95rem weight 600
- Use: Primary CTA ("Agendar reunión", "Elegir horario")

**Ghost**
- Background: `#ffffff`
- Text: Violet 700 (`#6d28d9`)
- Border: 1px solid Violet 200 (`#ddd6fe`)
- Padding: 0.95rem 2rem
- Radius: 12px
- Shadow: `0 2px 8px rgba(0, 0, 0, 0.04)`
- Hover: border-color Violet 400 + shadow `0 4px 16px rgba(109, 40, 217, 0.1)`
- Use: Secondary CTA ("Ver cómo funciona")

**Nav CTA**
- Background: Violet 700 (`#6d28d9`)
- Text: White
- Padding: 0.55rem 1.4rem
- Radius: 10px
- Font: Outfit weight 600
- Shadow: `0 2px 12px rgba(109, 40, 217, 0.2)`
- Hover: bg Violet 600 + shadow `0 4px 20px rgba(109, 40, 217, 0.35)` + translateY(-1px)

### Cards

**Service Row**
- Background: `#ffffff`
- Border: 1px solid `rgba(109, 40, 217, 0.08)`
- Radius: 20px
- Shadow: `0 8px 30px rgba(109, 40, 217, 0.06)`
- Padding: 2rem 2.5rem
- Layout: grid `56px 1fr` (icon + content)
- Hover: shadow `0 12px 40px rgba(109, 40, 217, 0.12)` + border Violet 200 + translateY(-2px)

**Testimonial Card**
- Background: `#ffffff`
- Border: 1px solid `rgba(109, 40, 217, 0.08)`
- Radius: 18px
- Padding: 2.2rem 2rem
- Width: 380px (fixed for marquee)
- Hover: border `rgba(109, 40, 217, 0.18)` + translateY(-4px) + shadow `0 16px 40px rgba(109, 40, 217, 0.08)`

**Process Step Card (Dark)**
- Background: `rgba(255, 255, 255, 0.04)`
- Border: 1px solid `rgba(139, 92, 246, 0.12)`
- Radius: 18px
- Padding: 2.2rem
- Backdrop-filter: blur(10px)
- Hover: border `rgba(139, 92, 246, 0.3)` + bg `rgba(255, 255, 255, 0.07)` + translateY(-3px)

**Pipeline Notification Card (Glassmorphism)**
- Background: `rgba(255, 255, 255, 0.85)`
- Backdrop-filter: `blur(16px) saturate(180%)`
- Border: 1px solid `rgba(255, 255, 255, 0.5)`
- Radius: 14px
- Padding: 12px 16px
- Shadow: `0 8px 32px rgba(109, 40, 217, 0.08), 0 1px 3px rgba(0, 0, 0, 0.04)`
- After pseudo-element: gradient border overlay `linear-gradient(135deg, rgba(139, 92, 246, 0.15), transparent, rgba(139, 92, 246, 0.08))`
- Animation: clip-path reveal + float-drift

### Calendar Visual
- Background: `#ffffff`
- Border: 1px solid `rgba(109, 40, 217, 0.08)`
- Radius: 20px
- Padding: 2.5rem
- Shadow: `0 20px 60px rgba(109, 40, 217, 0.08)`
- Top accent: 4px gradient bar `linear-gradient(90deg, #7c3aed, #a78bfa)`
- Overflow: visible (for mascot positioning)

### Service Tags (Pill)
- Background: Violet 50 (`#f5f3ff`)
- Border: 1px solid Violet 100 (`#ede9fe`)
- Radius: 6px
- Padding: 0.25rem 0.65rem
- Font: Outfit 0.68rem weight 600
- Color: Violet 600 (`#7c3aed`)

### Time Slot Pills
- Background: Violet 50 (`#f5f3ff`)
- Border: 1px solid Violet 100 (`#ede9fe`)
- Radius: 10px
- Padding: 0.45rem 1rem
- Font: Outfit 0.82rem weight 500
- Color: Violet 700 (`#6d28d9`)
- Hover: bg Violet 100 + border Violet 200 + scale(1.05)

### Navigation
- Fixed top, full-width
- Background: `rgba(250, 250, 252, 0.8)` + `backdrop-filter: blur(24px)`
- Scrolled: bg `rgba(250, 250, 252, 0.95)` + shadow `0 4px 30px rgba(0, 0, 0, 0.06)`
- Border-bottom: 1px solid `rgba(109, 40, 217, 0.08)`
- Logo: Outfit 1.3rem weight 800, "Outbound" in brand violet
- Inner max-width: 1200px

### Icon Wraps
- Size: 56×56px
- Background: Violet 50 (`#f5f3ff`)
- Border: 1px solid Violet 100 (`#ede9fe`)
- Radius: 14px
- Icon size: 28×28px
- Hover: bg Violet 100, border Violet 200, scale(1.06)

## 5. Layout Principles

### Spacing System
- Container max-width: 1200px (`--mw`)
- Container padding: 0 2rem
- Section padding: 7rem 0 (vertical)
- Stats bar padding: 4.5rem 0
- Card margin-bottom: 1.2rem (service rows)
- Service icon-to-content gap: 2rem
- Process step gap: 3rem (horizontal), 2rem (vertical padding)
- Testimonial card gap: 1.5rem
- Client logo gap: 3rem
- Calendar grid gap: 4rem

### Grid & Container
- Max content width: 1200px centered
- Hero: single column, left-aligned content (max 720px), animation fills right space
- Stats: 4-column equal grid
- Services: single column stacked rows
- Process: 3-column timeline grid (content | number | spacer), alternating sides
- Testimonials: infinite horizontal marquee
- Calendar: 2-column grid (text + visual)
- Footer: centered flex with space-between

### Whitespace Philosophy
- **Violet atmosphere**: The body gradient creates a sense of depth and atmosphere without requiring section background variation. The tinted canvas IS the background system.
- **Generous section spacing**: 7rem (112px) vertical padding per section creates confident breathing room between content blocks.
- **Hero dominance**: The hero section is min-height 100vh with animation elements filling the entire viewport, establishing visual scale and brand immersion from the first scroll.
- **Divider accent system**: Premium dividers between sections use a gradient line (`#ddd6fe` to `#a78bfa` to `#ddd6fe`) with a center accent dot, adding premium punctuation between content blocks.

### Border Radius Scale
- Small (6px): Service tags, pill badges
- Standard (10px): Nav CTA, time-slot pills, hamburger menu items
- Comfortable (12px): Primary buttons, ghost buttons
- Card (14px): Icon wraps, glassmorphism notification cards
- Large (18px): Testimonial cards, process step cards
- XL (20px): Service rows, calendar visual, nav main border-radius
- Full Pill (100px): Hero badge

## 6. Depth & Elevation

| Level | Treatment | Use |
|-------|-----------|-----|
| Atmospheric (Level 0) | Body gradient `#fafafc` → `#f5f1ff` → `#f5f3ff` | Page background atmosphere |
| Flat (Level 1) | 1px solid `rgba(109, 40, 217, 0.08)` | Default card border, nav border |
| Ambient (Level 2) | `0 8px 30px rgba(109, 40, 217, 0.06)` | Service rows, default cards |
| Elevated (Level 3) | `0 12px 40px rgba(109, 40, 217, 0.12)` | Card hover states |
| Featured (Level 4) | `0 20px 60px rgba(109, 40, 217, 0.08)` | Calendar visual, hero animation zone |
| CTA (Level 5) | `0 4px 20px rgba(109, 40, 217, 0.25)` → `0 8px 35px rgba(109, 40, 217, 0.4)` | Button shadow + hover |
| Glassmorphism | `0 8px 32px rgba(109, 40, 217, 0.08), 0 1px 3px rgba(0, 0, 0, 0.04)` + backdrop-filter | Pipeline notification cards |
| Dark Glow | `0 0 30px rgba(139, 92, 246, 0.2)` → `0 0 50px rgba(139, 92, 246, 0.4)` | Process step numbers |
| Focus | Not explicitly defined | Needs accessibility review |

**Shadow Philosophy**: TOF uses a brand-colored shadow system — every shadow in the light sections uses `rgba(109, 40, 217, ...)` (the brand violet) rather than neutral black/gray. This creates a cohesive "purple atmosphere" where elevation feels like emerging from a violet haze rather than floating above a surface. The shadow intensity increases proportionally with elevation: 0.06 (resting) → 0.08 (featured) → 0.12 (hover) → 0.25–0.4 (CTA). This progressive system creates a clear depth hierarchy using a single color channel.

## 7. Animation System

### Easing Functions
- **Default**: `cubic-bezier(0.16, 1, 0.3, 1)` — fast start, smooth deceleration. Used for most transitions.
- **Spring**: `cubic-bezier(0.34, 1.56, 0.64, 1)` — overshoot bounce. Used for card reveals.
- **Smooth**: `cubic-bezier(0.25, 0.46, 0.45, 0.94)` — gentle, organic. Used for blob morphing.
- **Dramatic**: `cubic-bezier(0.77, 0, 0.175, 1)` — defined but available for future use.

### Hero: "The Pipeline"
- **Morphing blobs**: 3 gradient blobs with organic `border-radius` keyframes (12s, 15s, 18s cycles), `filter: blur(60px)`, opacity 0.12
- **Notification cards**: 6 cards with `clip-path: inset()` reveal animation (1–1.2s) + float-drift infinite loops (6–9s cycles)
- **Pulse lines**: Gradient lines that fade-grow-fade (3s infinite) connecting card positions
- **Staggered delays**: Cards reveal at 0.3s intervals (0.3, 0.8, 1.3, 1.8, 2.3, 2.8)

### Scroll Reveals
- **`.reveal`**: opacity 0 → 1, translateY(40px → 0), transition 0.7s
- **`.reveal-left`**: translateX(-50px → 0)
- **`.reveal-right`**: translateX(50px → 0)
- **`.reveal-scale`**: scale(0.92 → 1)
- **Stagger classes**: `.st1` through `.st5` with 0.05s delay increments
- **Trigger**: IntersectionObserver at threshold 0.15

### Process Section: Dual Panels
- **Gmail panel** (left, 480px): Dark material theme, animated email rows with clip-path reveals, auto-scroll loop (35s), compose button, sidebar
- **LinkedIn panel** (right, 280px): Dark LinkedIn theme, conversation list with slide-in animations, auto-scroll (40s), avatar-based messages
- **Interaction**: Default opacity 0.09, hover → 0.55 with pause on all animations
- **Fade overlays**: Top/bottom gradient fades from `#0b0a10` to transparent

### Marquees
- **Testimonials**: `translateX(0) → translateX(-50%)` at 38s linear infinite, pause on hover
- **Client logos**: Same technique at 40s, with mask-image fade edges (5%–95% and 8%–92%)

### Mascot Cat
- **Default state**: Sleeping (closed eyes, zzz text floating up with stagger)
- **Active state**: CSS checkbox toggle → eyes open with sparkle, typing paws animation, speech bubble appears, zzz hides
- **Steam animation**: Coffee cup steam floats upward infinitely

### Counter Animation
- **Slot counter**: JavaScript-driven number counting from 0 to target on scroll intersection
- **Duration**: ~1.5s with easing

## 8. Do's and Don'ts

### Do
- Use Outfit for ALL display/heading/navigation/label text — never DM Sans for structural elements
- Use DM Sans for ALL body/reading/description text — never Outfit for paragraphs
- Use `rgba(109, 40, 217, ...)` for shadows — every shadow should feel violet, not neutral gray
- Apply negative letter-spacing at display sizes (-2px hero, -1.2px section, -0.3px card)
- Use positive letter-spacing (1.5–3px) on uppercase labels to create the "category voice"
- Apply the progressive shadow intensity scale (0.06 → 0.08 → 0.12 → 0.25)
- Use `cubic-bezier(0.16, 1, 0.3, 1)` as the default transition easing
- Keep cards at 18–20px border-radius — this is the signature softness
- Use the violet scale from `--v50` to `--v900` — never introduce off-brand purples
- Animate with `translateY(-2px to -4px)` on hover — subtle lift, never dramatic

### Don't
- Don't use neutral gray shadows (`rgba(0,0,0,...)`) on light section cards — always violet-tinted
- Don't use border-radius below 6px or above 20px for cards (100px only for pills/badges)
- Don't use weight 900 anywhere except the hero headline and stat counters — it's the top of the hierarchy
- Don't apply `backdrop-filter` on mobile — it's disabled for performance
- Don't use solid background colors for sections — the body gradient provides all atmospheric variation
- Don't mix English and Spanish in a single viewport — maintain language consistency
- Don't place interactive elements inside the floating animation cards — they're decorative only
- Don't use pure black (`#000000`) for text — always `#1a1625` (purple-tinted near-black)
- Don't apply transitions longer than 0.7s for scroll reveals — they feel sluggish beyond that
- Don't skip the `inset 0 1px 0 rgba(255,255,255,0.15)` on primary buttons — it's the subtle top-edge highlight

## 9. Responsive Behavior

### Breakpoints
| Name | Width | Key Changes |
|------|-------|-------------|
| Mobile | ≤768px | Single column, no blobs/glows/float-els, simplified hero (2 cards only), no dual panels, stacked calendar, centered everything |
| Tablet | 769–1024px | No dual panels, 2-column stats, stacked calendar, simplified process timeline (linear left-aligned), smaller icons |
| Desktop | >1024px | Full layout, all animations, dual panels visible, timeline alternating, mascot positioned absolutely |

### Touch Targets
- Buttons: min-height 48px on mobile with full-width
- Time slots: adequate padding (0.45rem 1rem) for tapping
- Nav hamburger: min 44×44px touch target
- Hero CTAs: full-width stacked on mobile

### Collapsing Strategy
- Hero: min-height auto on mobile (from 100vh), font scales down to 2.2rem
- Pipeline cards: only 2 visible on mobile (pc-3 through pc-6 hidden)
- Stats: 4-col → 2-col on tablet/mobile
- Services: icon shrinks 56→48→42px, padding reduces
- Process: 3-column alternating timeline → single-column left-aligned linear flow
- Testimonials: card width 380→280px
- Calendar: 2-col → stacked, mascot repositioned inline below calendar
- Dual panels (Gmail/LinkedIn): completely hidden below 1024px
- Blobs, glows, floating elements: all hidden on mobile for performance
- Footer: flex row → stacked column centered

## 10. Agent Prompt Guide

### Quick Color Reference
- Primary CTA: Gradient `linear-gradient(135deg, #6d28d9, #8b5cf6)`
- Background: Body gradient `#fafafc` → `#f5f1ff` → `#f5f3ff`
- Heading text: `#1a1625` (purple-tinted near-black)
- Body text: `#4a4458` (purple-tinted dark gray)
- Muted text: `#7c7591` (violet-gray)
- Card border: `rgba(109, 40, 217, 0.08)`
- Card shadow: `0 8px 30px rgba(109, 40, 217, 0.06)`
- Brand accent: Violet 700 `#6d28d9`
- Dark section: `#0b0a10`

### Example Component Prompts
- "Create a hero section on violet-tinted background (#fafafc). Headline at clamp(2.6rem, 5.5vw, 4.2rem) Outfit weight 900, line-height 1.05, letter-spacing -2px, color #1a1625. Emphasis span with gradient text (linear-gradient 135deg #6d28d9 to #8b5cf6). Subtitle at 1.1rem DM Sans weight 400, line-height 1.75, color #7c7591. Primary CTA with gradient background, 12px radius, 0.95rem 2rem padding, violet shadow."
- "Design a service card: white background, 1px solid rgba(109,40,217,0.08) border, 20px radius, shadow 0 8px 30px rgba(109,40,217,0.06). 56px icon wrap with #f5f3ff bg and #ede9fe border, 14px radius. Title at 1.25rem Outfit weight 700. Body at 0.95rem DM Sans weight 400, color #7c7591. Hover: shadow intensifies to 0.12, translateY(-2px)."
- "Build a section label: Outfit 0.85rem weight 700, text-transform uppercase, letter-spacing 3px, color #7c3aed. Below it: section title at clamp(2rem, 3.8vw, 2.8rem) Outfit weight 800, letter-spacing -1.2px, color #1a1625."
- "Create a testimonial card for marquee: white bg, violet border rgba(109,40,217,0.08), 18px radius, 380px fixed width. Star rating in #8b5cf6. Body at 0.92rem DM Sans. Author section with 52px avatar, Outfit 0.92rem weight 700 name, DM Sans 0.78rem role."
- "Design the process section: bg #0b0a10, text white. Timeline with vertical line (2px, linear-gradient violet 0.2 opacity). Step cards: rgba(255,255,255,0.04) bg, rgba(139,92,246,0.12) border, 18px radius, backdrop-filter blur(10px). Number circles: 60px, 2px solid #8b5cf6, glow shadow."

### Iteration Guide
1. Always use violet-tinted shadows on light sections — `rgba(109, 40, 217, opacity)` is the foundation
2. Letter-spacing follows size: -2px (hero) → -1.2px (section) → -0.3px (card) → +1.5–3px (labels)
3. Two fonts, strict roles: Outfit (structure/display), DM Sans (reading/body)
4. Weight hierarchy: 900 (hero only) → 800 (sections) → 700 (cards/names) → 600 (buttons/labels) → 500 (nav) → 400 (body)
5. The body gradient replaces section backgrounds — no section should override the atmospheric canvas
6. Card radius is 18–20px throughout — this is the signature softness
7. Hover effects are always: shadow intensification + subtle translateY + optional border color shift
