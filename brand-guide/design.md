# Design System

The visual language for Kerala Ayurveda product pages. Every rule here is extracted from the live Neelibhringadi Keram PDP (V2, main branch). Follow these when building new pages, components, or marketing assets.

---

## 1. Color System

### Core Palette

| Token | Hex | Role |
|---|---|---|
| `--primary` | `#1E4B3C` | Brand anchor. CTAs, headings, trust elements, dark sections |
| `--primary-dark` | `#013426` | Deep accent. Bundle add-ons, high-contrast cards |
| `--secondary` | `#7a5900` | Warm brown. Section labels, heritage/trust text |
| `--on-surface` | `#191d18` | Near-black. Primary body text, strong emphasis |

### Surface Hierarchy

Backgrounds layer from warm to cool. Never use pure white (`#fff`) as a page background — reserve it for cards and content sections that sit on top of a surface.

| Token | Hex | Usage |
|---|---|---|
| `--surface` | `#FDFCF8` | Page base (body background) |
| `--beige` | `#F9F8F3` | Alternating sections, gallery background, pricing zone |
| `--surface-container` | `#F7FAF2` | Light sage. Subtle container differentiation |
| `--surface-container-low` | `#F2F5ED` | Paler sage. Secondary containers |
| `--cream` | `#FEF9E7` | Luxury accent. Ritual guides, safety badges, text on dark green |
| `white` | `#FFFFFF` | Cards, content sections, accordion panels, review areas |

### Accent Colors

| Token | Hex | Usage |
|---|---|---|
| `--amber-500` | `#f59e0b` | Rating stars, testimonial borders, micro-testimonial accents |
| `--amber-700` | `#b45309` | Ritual guide labels, safety icon tint |
| `--amber-900` | `#78350f` | Dark gold text. Ritual guide body, safety badge text |

### Semantic Colors (Non-Token)

These appear inline, not as CSS variables.

| Hex / Value | Usage |
|---|---|
| `#16a34a` | In-stock dot, "what's in" positive icon |
| `#dc2626` | "What's not in" negative icon |
| `rgba(34,197,94,0.08)` | Reaction callout background (green tint) |
| `#7c3aed` | Greying testimonial badge |
| `rgba(168,85,247,0.08)` | Greying badge background (purple tint) |
| `#C49B55` | Testimonial stars on dark green backgrounds |
| `#fbbf24` / `#60a5fa` / `#4ade80` | Timeline circle borders (amber / blue / green) |

### Ingredient Role Pills

| Role | Background | Text |
|---|---|---|
| Growth | `rgba(34,197,94,0.2)` | `#16a34a` |
| Recovery | `rgba(59,130,246,0.2)` | `#2563eb` |
| Strength | `rgba(245,158,11,0.2)` | `#d97706` |
| Nourish | `rgba(232,193,122,0.25)` | `#b8860b` |

### Text Opacity Scale

Body text uses rgba on `--on-surface` (`25,29,24`) to create hierarchy without introducing new colors.

| Opacity | Usage |
|---|---|
| `1.0` | Strong emphasis, names, titles |
| `0.8` | Primary body text, ingredient descriptions, review text |
| `0.7` | Secondary body text, technical descriptions |
| `0.6` | Tertiary text. Section descriptions, persona tile body, milk item descriptions |
| `0.55` | Delivery badge text, comparison "them" cells |
| `0.45` | Heritage line, muted sub-text |
| `0.4` | Label text, timeline periods, per-use pricing, review metadata |
| `0.35` | Disclaimer text, pricing labels, comparison row labels |
| `0.3` | Pricing per-use text, ingredient origin labels |
| `0.2` | Accordion chevron default state |

On dark green (`--primary`) backgrounds, text uses rgba on `--cream` (`254,249,231` or `248,245,236`):

| Opacity | Usage |
|---|---|
| `0.9` | Testimonial quotes |
| `0.8` | Section body text on dark |
| `0.6` | Section labels, closing CTA body, comparison row labels on highlight |
| `0.4` | Footer labels, meta text on dark |

### Border & Divider System

Borders are nearly invisible — structural, not decorative. All use rgba.

| Value | Usage |
|---|---|
| `rgba(192,200,195, 0.1)` | Default section dividers, card borders, step separators |
| `rgba(192,200,195, 0.12)` | Comparison row borders |
| `rgba(192,200,195, 0.15)` | Header border, mobile menu links, credential bar, comparison table rows |
| `rgba(192,200,195, 0.2)` | Heavier dividers: credential bar, section tops |
| `rgba(192,200,195, 0.3)` | Product info meta border-top |
| `rgba(255,255,255, 0.1)` | Borders on dark green backgrounds |
| `rgba(255,255,255, 0.2)` | Buy bar divider |
| `rgba(217,178,78, 0.3)` | Cream/amber accent borders (ritual guide, safety badges) |

---

## 2. Typography

### Font Pairing

| Role | Family | Load |
|---|---|---|
| Heading / Editorial | `'Noto Serif', serif` | 400, 400i, 700, 700i |
| Body / Functional | `'Work Sans', sans-serif` | 300, 400, 500, 600, 700 |

CSS also references `var(--font-heading)` and `var(--font-body)` in V2 components (heritage line, closing CTA, bundle addon). Both resolve to the same families above.

**Rule:** Noto Serif is for headings, prices, editorial statements, and testimonial quotes. Work Sans is for everything else — body text, labels, buttons, badges, navigation.

### Type Scale

Sizes are mobile-first. Desktop overrides noted where applicable.

**Display / Hero**

| Element | Size (Mobile) | Size (Desktop) | Weight | Family | Style |
|---|---|---|---|---|---|
| Product name (H1) | 1.875rem | 2.25rem / 2.5rem (1024px) | 700 | Serif | Normal |
| Price | 2.5rem | 3rem | 700 | Serif | Normal |
| Rating score | 1.5rem | — | 700 | Serif | Normal |
| Stats bar value | 1.125rem | — | 700 | Serif | Normal |
| Summary stats value | 1.25rem | — | 700 | Serif | Normal |

**Section Headings**

| Element | Size (Mobile) | Size (Desktop) | Weight | Family | Style |
|---|---|---|---|---|---|
| Section H2 (standard) | 1.5rem | 2rem / 2.25rem | 700 | Serif | Italic |
| Reviews H2 | 1.875rem | — | 700 | Serif | Italic |
| Closing CTA text | 1.375rem | 1.75rem | — | Serif | Normal (strong tags bold) |
| Testimonial quote | 1.25rem | — | — | Serif | Italic |

**Body Text**

| Element | Size | Weight | Family | Line Height |
|---|---|---|---|---|
| Section body (large) | 0.9375rem | 400 | Sans | 1.6–1.7 |
| Standard body | 0.875rem | 400–500 | Sans | 1.6 |
| Card body / descriptions | 0.75rem | 500 | Sans | 1.5–1.6 |
| Product info tagline | 1.25rem (mob) / 1.375rem (desk) | — | Serif | Italic |
| Heritage line | 0.875rem | — | Serif var | Italic |
| Accordion trigger | 0.875rem | — | Serif | Italic |
| Accordion content | 0.8125rem | — | Sans | 1.7 |

**Labels / Micro-Text**

| Element | Size | Weight | Transform | Spacing |
|---|---|---|---|---|
| Section label | 9px | 700 | Uppercase | 0.2em |
| Badge text | 9px | 700 | Uppercase | 0.15em |
| CTA button text | 0.75rem–0.8125rem | 700 | Uppercase | 0.12em–0.15em |
| Delivery badge | 0.6875rem | 500 | Normal | — |
| Timeline period | 8px | 700 | Uppercase | 0.12em |
| Step label | 8px | 700 | Uppercase | 0.12em |
| Ingredient origin | 8px | 700 | Uppercase | 0.12em |
| Stats bar label | 7px | — | Uppercase | 0.15em |
| Credential label | 7px | — | Uppercase | — |
| Ingredient role (on image) | 6px | 700 | Uppercase | 0.12em |

### Uppercase System

Uppercase is reserved for **functional labels, badges, CTAs, and metadata** — never for body text or editorial headings.

When text is uppercase, it always has letter-spacing:
- `0.05em–0.08em` — tighter (safety headings, comparison labels, milk item names)
- `0.12em` — standard (CTAs, badges, step labels, origins, reorder button)
- `0.15em` — wider (badge text, stats bar labels, buy bar CTA)
- `0.2em` — widest (section labels)
- `0.3em` — extreme (expectation section labels on dark background)

### Italic Usage

Italic serif (`Noto Serif italic`) is used for:
- Section headings (H2) — editorial/emotional framing
- Product tagline — brand voice
- Heritage line — sub-tagline
- Testimonial quotes — personal voice
- Accordion triggers — conversational invitations
- Review text — customer voice
- Disclaimer text — legal softening

**Never** use italic on: body text, labels, badges, CTAs, prices, or navigation.

---

## 3. Spacing & Layout

### Breakpoints

| Name | Width | Key Changes |
|---|---|---|
| Base (mobile) | < 768px | Single column, stacked sections |
| Tablet/Desktop | >= 768px | Side-by-side PDP, multi-column grids |
| Large Desktop | >= 1024px | 55/45 gallery split, 4-col ingredients, 3-col comparison |

### Grid System

**Above the fold (PDP zone):**
- Mobile: Single column, stacked (gallery then product info)
- Desktop (768px): `grid-template-columns: 1fr 1fr` (50/50)
- Large Desktop (1024px): `grid-template-columns: 55% 45%`

Gallery is sticky on desktop: `position: sticky; top: 4.5rem; height: calc(100vh - 4.5rem - 4rem)`
Right column scrolls independently: `overflow-y: auto`

**Below the fold (content sections):**
Full-width sections with content constrained by max-width.

### Max-Width Constraints

| Width | Usage |
|---|---|
| `56rem` | Standard content max-width (technical, ingredients grid, testimonials, comparison, reviews, application, persona tiles, sensory testimonial) |
| `40rem` | Narrow content (accordion, triple-milk grid mobile, what's-in card, safety content) |
| `32rem` | Text-only blocks (closing CTA text on desktop, buy bar inner) |
| `28rem` | Centered paragraphs (reaction callout body, triple milk description) |
| `24rem` | Closing CTA text on mobile |
| `20rem` | Mobile menu panel max-width, centered body text on dark sections |

### Padding Scale

**Section padding (mobile → desktop):**

| Pattern | Mobile | Desktop |
|---|---|---|
| Standard section | `4rem 1.5rem` | `4rem 2.5rem` |
| Compact section | `2rem–3rem 1.5rem` | `2.5rem–3rem 2.5rem` |
| Product info | `2rem 1.5rem` | `3rem 2.5rem` |
| Header | `0 1.5rem` (h: 4rem) | `0 2.5rem` (h: 4.5rem) → `0 4rem` (1024px) |

**Component internal padding:**
- Card padding: `1rem–1.5rem`
- Accordion trigger: `1.25rem 1.5rem`
- Accordion content: `0 1.5rem 1.25rem`
- Persona tile: `1.25rem`
- Milk item: `1rem 1.25rem`
- Comparison cell: `0.625rem 0.75rem`
- Badge: `0.25rem 0.625rem`
- Buy bar: `0.75rem 1.5rem` (mobile), `1rem 2.5rem` (desktop)

### Section Rhythm

Sections alternate backgrounds to create visual rhythm without heavy borders:
```
white → beige → white → green tint → white → beige → dark green → white → beige → white → beige → white → dark green
```

The pattern loosely follows: **light → neutral → light → accent → repeat → dark anchor**.

---

## 4. Component Patterns

### Cards

**Ingredient Card**
- Horizontal layout (mobile), vertical (desktop 4-col grid)
- Image panel: 33% width, `--primary` background, image at `opacity: 0.55` with `mix-blend-mode: luminosity`, `transform: scale(2.2)`
- Body panel: 67% width
- Border: `1px solid rgba(192,200,195,0.1)`
- Shadow: `0 1px 3px rgba(0,0,0,0.04)`
- Hover: `translateY(-1px)`, shadow intensifies to `0 4px 16px rgba(30,75,60,0.06)`
- Corner radius: `0.5rem`

**Persona Tile**
- Background: `--beige`
- Corner radius: `0.75rem`
- Icon circle: `2.5rem` white circle with subtle shadow
- Grid: 2-col (mobile), 4-col (desktop)

**Milk Item**
- Background: `--beige`
- Corner radius: `0.75rem`
- Icon: `3rem` white circle with border
- Flex row (mobile), flex column centered (desktop)

**Comparison Column (Desktop)**
- Background: `--beige` (default), `--primary` (highlight)
- Corner radius: `0.75rem`
- Rows separated by `border-top`

**Comparison Rows (Mobile)**
- 2-column grid: "Us" cell (`rgba(30,75,60,0.06)` bg, primary text, 600 weight) vs "Them" cell (`rgba(25,29,24,0.03)` bg, muted text)
- Header labels: primary green pill vs gray pill
- Corner radius on cells: `0.5rem`

### Badges & Pills

| Type | Background | Border | Text | Radius |
|---|---|---|---|---|
| In-stock badge | `rgba(30,75,60,0.05)` | `1px solid rgba(30,75,60,0.2)` | `--primary`, 9px, 700, uppercase | `9999px` (pill) |
| Ingredient role pill | Color-coded (see palette) | None | Color-coded, 0.6875rem, 700 | `2rem` |
| Testimonial badge | Varies by type | `1px solid` (varies) | 8px, 700, uppercase | `4px` |
| Compare "Us" label | `--primary` | None | `--cream`, 0.6875rem, 700 | `0.5rem` |
| Compare "Them" label | `rgba(25,29,24,0.06)` | None | `rgba(25,29,24,0.5)` | `0.5rem` |
| Safety badge | `--cream` | `1px solid rgba(217,178,78,0.3)` | `--amber-900`, 10px, 700 | `9999px` |

### Buttons

**Primary CTA (Inline)**
- Background: `--primary`, color: white
- Font: Work Sans, 0.8125rem, 700, uppercase, `letter-spacing: 0.12em`
- Padding: `1rem` full width
- Radius: `0.5rem`
- Shadow: `0 2px 8px rgba(30,75,60,0.2)`
- Hover: `background: #164032`
- Active: `transform: scale(0.98)`

**Secondary / Outline CTA**
- Border: `2px solid --primary`, no background
- Color: `--primary`
- Font: Work Sans, 10px, 700, uppercase, `letter-spacing: 0.12em`
- Hover: `background: rgba(30,75,60,0.05)`

**Small Action Button (Reorder, Protocol Add)**
- Background: `#000` (black), color: white
- Font: 8–9px, 700, uppercase, `letter-spacing: 0.12em`
- Padding: `0.375rem 0.75rem` / `0.625rem 1rem`
- Radius: `4px`
- Active: `transform: scale(0.95–0.97)`

**Bundle Addon Button**
- Background: `--amber-500`
- Color: `--primary-dark`
- Font: 0.75rem, 700, uppercase
- Hover: `background: #d4a849`, `transform: scale(1.03)`

**Closing CTA Button**
- Background: `--cream`, color: `--primary`
- Font: 0.875rem, 700, `letter-spacing: 0.05em`
- Radius: `0.625rem`
- Hover: `background: white`, `transform: scale(1.02)`, shadow `0 4px 16px rgba(0,0,0,0.15)`

**Buy Bar CTA**
- No background (transparent on primary bar)
- Color: white, 0.75rem, 700, uppercase, `letter-spacing: 0.15em`
- Hover: `background: rgba(255,255,255,0.08)`
- Active: `background: rgba(255,255,255,0.15)`

**Variant Selector Button**
- Active: `--primary` bg, white text, shadow
- Inactive: white bg with outline-variant border
- Hover (inactive): border changes to `--primary`

### Testimonials

**On dark green backgrounds:**
- Left border: `1px solid rgba(254,249,231,0.2)`
- Quote: Noto Serif italic, 1.25rem, `rgba(254,249,231,0.9)`
- Name: 0.875rem, 700, cream
- Meta: 9px, uppercase, `rgba(254,249,231,0.4)`
- Stars: `#C49B55` (muted gold)

**Micro-testimonial (on light backgrounds):**
- Left border: `2px solid --amber-500`
- Background: `rgba(196,155,85,0.06)`
- Radius: `0 0.5rem 0.5rem 0` (right side only)
- Quote: 0.8125rem, italic
- Attribution: 0.75rem, 600 weight, 0.5 opacity

**Sensory testimonial:**
- Same pattern as micro but `3px` left border
- Max-width constrained: `40rem` (mobile), `56rem` (desktop)

### Accordion

- Container: white, `0.75rem` radius, subtle border and shadow
- Trigger: Noto Serif italic, 0.875rem, full-width button
- Trigger hover: `background: rgba(249,248,243,0.5)`
- Chevron: `rgba(25,29,24,0.2)` default → `--primary` when open
- Chevron animation: `rotate(90deg)`, `0.3s ease`
- Content: `max-height: 0` → animated open, `0.35s ease`

### Sticky Elements

**Header:**
- `position: fixed; top: 0; z-index: 50`
- Background: `rgba(253,252,248,0.92)` with `backdrop-filter: blur(12px)`
- Border-bottom: `rgba(192,200,195,0.15)`
- Scroll state: adds `box-shadow: 0 2px 20px rgba(30,75,60,0.06)`
- Height: `4rem` (mobile), `4.5rem` (desktop)

**Buy Bar:**
- `position: fixed; bottom: 0; z-index: 50`
- Background: `rgba(255,255,255,0.95)` with `backdrop-filter: blur(16px)`
- Inner bar: `--primary` background, `0.75rem` radius
- Shadow: `0 4px 20px rgba(30,75,60,0.3)`
- Safe-area padding: `padding-bottom: max(0.75rem, env(safe-area-inset-bottom))`
- Max-width: `32rem` (mobile), `28rem` (desktop)
- Two states: Add-to-cart (CTA + price) and In-cart (qty controls + total + view cart)

**Toast:**
- `position: fixed; top: 4.5rem; z-index: 100`
- `--primary` background, white text, `0.75rem` radius
- Shadow: `0 8px 30px rgba(0,0,0,0.2)`
- Entry animation: translateY(-20px) → 0, opacity 0 → 1, `0.3s ease`

---

## 5. Motion & Interaction

### Hover States

| Element | Effect |
|---|---|
| Ingredient card | `translateY(-1px)`, shadow intensifies |
| Primary CTA | Background darkens (`#164032`) |
| Outline CTA | Subtle background tint |
| Gallery arrow | Opacity 0 → 1 (desktop), 0.5 → 0.85 (always-visible mode) |
| Nav links | Opacity `0.6 → 1` |
| Accordion trigger | Light background tint |
| Bundle addon button | `scale(1.03)`, color shift |
| Closing CTA button | `scale(1.02)`, shadow appears, bg → white |
| Buy bar view-cart | Shadow appears |

### Active / Press States

| Element | Effect |
|---|---|
| Primary CTA | `scale(0.98)` |
| Reorder button | `scale(0.97)` |
| Protocol add button | `scale(0.95)` |
| Quantity button | `scale(0.93)` |
| Buy bar view-cart | `scale(0.96)` |
| Accordion trigger | Deeper background tint |

**Rule:** Scale decreases as element size decreases. Large buttons: 0.98. Medium: 0.96–0.97. Small: 0.93–0.95.

### Transition Durations

| Duration | Usage |
|---|---|
| `0.1s` | Button press (transform only) |
| `0.15s` | Micro-interactions: button backgrounds, hover states, quantity controls |
| `0.2s` | Nav link opacity, variant buttons, thumbnail states, badge hover |
| `0.25s` | Gallery arrow opacity reveal |
| `0.3s` | Header shadow on scroll, accordion chevron rotation, toast entry, mobile menu |
| `0.35s` | Accordion content expand/collapse |
| `0.5s` | Gallery image crossfade |

**Easing:** `ease` universally. No custom cubic-bezier curves in this system.

### Backdrop Blur

| Blur | Usage |
|---|---|
| `4px` | Gallery arrows |
| `8px` | Stats bar overlay |
| `10px` | Gallery thumbnails tray |
| `12px` | Header |
| `16px` | Buy bar |

---

## 6. Iconography

### System

All icons are inline SVGs referenced via a `<use href="#id">` sprite pattern. Icons use `fill: currentColor` so they inherit text color from their parent.

### Size Scale

| Class | Size | Usage |
|---|---|---|
| `icon--xs` | 0.625rem (10px) | Tiny indicators |
| `icon--sm` | 0.75rem (12px) | Delivery badges, inline icons |
| `icon--md` | 1.125rem (18px) | Standard inline icons |
| `icon--lg` | 1.25rem (20px) | Card icons, action icons |
| `icon--xl` | 1.5rem (24px) | Featured icons (ritual guide) |
| (base `.icon`) | 1em | Inherits parent font-size |

### Icon Set

The sprite includes: `star`, `star-half`, `check`, `check-circle`, `close`, `x-circle`, `cart`, `arrow-right`, `menu`, `truck`, `cash`, `return`, `sun`, `chevron`, `minus`, `plus`, `leaf`, `shield`, `droplet`, `package`.

---

## 7. Shadows

| Shadow | Usage |
|---|---|
| `0 1px 3px rgba(0,0,0,0.04)` | Cards at rest, whats-in card, safety badges |
| `0 1px 4px rgba(0,0,0,0.05)` | Persona tile icons |
| `0 1px 4px rgba(0,0,0,0.06)` | Timeline circles |
| `0 1px 6px rgba(0,0,0,0.1)` | Gallery arrows |
| `0 1px 6px rgba(30,75,60,0.2)` | Active thumbnail |
| `0 2px 8px rgba(0,0,0,0.04)` | Milk item icons |
| `0 2px 8px rgba(0,0,0,0.15)` | View cart button hover |
| `0 2px 8px rgba(30,75,60,0.2)` | Primary CTA, active variant button |
| `0 2px 12px rgba(0,0,0,0.12)` | Gallery thumbnails tray |
| `0 2px 20px rgba(30,75,60,0.06)` | Header on scroll |
| `0 4px 16px rgba(30,75,60,0.06)` | Ingredient card hover |
| `0 4px 16px rgba(0,0,0,0.15)` | Closing CTA button hover |
| `0 4px 20px rgba(30,75,60,0.3)` | Buy bar inner |
| `0 8px 30px rgba(0,0,0,0.15)` | Protocol card |
| `0 8px 30px rgba(0,0,0,0.2)` | Toast notification |
| `4px 0 20px rgba(0,0,0,0.1)` | Mobile menu panel |

**Pattern:** Brand shadows use `rgba(30,75,60,...)` (green-tinted). Neutral shadows use `rgba(0,0,0,...)`. Green-tinted shadows go on brand elements (CTAs, buy bar, header). Neutral shadows go on generic UI (cards, panels, overlays).

---

## 8. Responsive Patterns

### Mobile-First Defaults

- Single column layout
- Full-width sections
- Horizontal padding: `1.5rem`
- Gallery aspect ratio: `3:4`
- Comparison: 2-column "Us vs Them" rows
- Persona tiles: 2x2 grid
- Timeline: vertical steps with left icon rail
- Testimonials: stacked, left-border
- Ingredients: stacked horizontal cards

### Desktop (768px+) Transformations

- PDP splits into side-by-side grid
- Gallery becomes sticky
- Stats bar hidden
- Padding increases to `2.5rem`
- Comparison: switches to 3-column card layout (via `display: none` / `display: grid !important` swap)
- Persona tiles: 4-column
- Timeline: 2-column grid (changed from 3-col in V1)
- Testimonials: 3-column grid (changed from 2-col in V1)
- Ingredients: 4-column grid, cards flip to vertical
- Triple milk: row layout, centered cards
- Application steps: 3-column grid, vertical orientation
- Reviews: 2-column grid
- Accordion: centered at `40rem` max-width

### Large Desktop (1024px+)

- PDP grid: `55% / 45%` (gallery gets more space)
- Header padding: `4rem`
- Product name: `2.5rem`
- Comparison desktop cards: 3-column (enabled at this breakpoint)

### Touch Device Handling

```css
@media (hover: none) {
  .gallery-arrow { opacity: 0.5; }  /* Always subtly visible */
}
```

Gallery arrows are hidden by default on pointer devices and revealed on hover. On touch devices, they stay at 50% opacity permanently.
