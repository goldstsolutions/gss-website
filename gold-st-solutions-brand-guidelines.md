# Gold St Solutions — Brand Guidelines

> Sourced directly from goldstsolutions.com CSS (May 2026)

---

## 1. Color Palette

### Gold (Primary Brand Color)

| Token | Hex / Value | Usage |
|---|---|---|
| `--gold` | `#D4B96A` | Primary accent, headings highlights, icons, CTAs |
| `--gold-bright` | `#E2CB85` | Gradient end points, hover highlights |
| `--gold-muted` | `#A8904E` | Eyebrow labels, secondary text accents |
| `--gold-dim` | `rgba(212,185,106, 0.10)` | Icon backgrounds, subtle fills |
| `--gold-border` | `rgba(212,185,106, 0.18)` | Default card/section borders |
| `--gold-border-mid` | `rgba(212,185,106, 0.32)` | Hover states on borders |

### Background / Dark Scale

| Token | Hex | Usage |
|---|---|---|
| `--void` | `#07090D` | Base page background |
| `--navy` | `#0B1220` | Hero background, alternate sections |
| `--navy-mid` | `#0F1A2E` | Mid-tier section backgrounds |
| `--navy-light` | `#162338` | Card backgrounds |
| `--steel` | `#1C2D44` | Card hover state backgrounds |

### Text

| Token | Value | Usage |
|---|---|---|
| `--text-primary` | `rgba(255,255,255, 0.92)` | Headings, primary body copy |
| `--text-body` | `rgba(255,255,255, 0.62)` | Descriptive / supporting copy |
| `--text-muted` | `rgba(255,255,255, 0.28)` | Labels, stat sub-text, de-emphasized text |

---

## 2. Typography

Four font families are loaded via Google Fonts. Each has a specific role — do not swap them.

### Font Stack

| Font | Weights | Role |
|---|---|---|
| **Plus Jakarta Sans** | 300, 400, 500, 600, 700, 800 | Display headings, section titles, CTAs, logo, stat values |
| **Syne** | 400, 600, 700, 800 | Eyebrow labels, nav links, stat labels — all-caps only |
| **Space Grotesk** | 300, 400, 500, 600 | Body copy (default `font-family` on `body`) |
| **DM Mono** | 300, 400, 500 | Code, technical strings, monospaced elements |

### Type Scale & Styles

| Element | Font | Size | Weight | Transform | Tracking |
|---|---|---|---|---|---|
| Hero title | Plus Jakarta Sans | clamp(30px, 6vw, 76px) | 800 | Uppercase | -0.03em |
| Section title | Plus Jakarta Sans | clamp(28px, 3.8vw, 46px) | 800 | Uppercase | -0.025em |
| Card heading | Plus Jakarta Sans | 13px | 700 | Uppercase | 0.02em |
| Eyebrow label | Syne | 9px | 700 | Uppercase | 0.46em |
| Nav links | Syne | 9px | 700 | Uppercase | 0.24em |
| Stat value | Plus Jakarta Sans | 24px | 800 | — | -0.03em |
| Stat label | Syne | 8px | 700 | Uppercase | 0.20em |
| Body / section desc | Space Grotesk | 15px | 400 | — | — |
| Body (hero sub) | Space Grotesk | 17px | 400 | — | — |
| Small body (cards) | Space Grotesk | 14px | 400 | — | — |

**Line heights:** Headings use `0.92–0.95`. Body copy uses `1.6–1.75`.

---

## 3. Buttons

### Primary — Gold Button (`.btn-gold`)

- Background: linear gradient `135deg`, `#D4B96A` → `#E2CB85`
- Text color: `#07090D` (void — dark text on gold)
- Font: Plus Jakarta Sans, 11px, weight 700, uppercase, letter-spacing 0.08em
- Border radius: 3px
- Padding: 14px 28px
- Hover: lifts `translateY(-2px)`

### Secondary — Ghost Button (`.btn-ghost`)

- Background: transparent
- Text color: `#D4B96A` (gold)
- Border: 1px solid `rgba(212,185,106, 0.32)`
- Same font, size, and radius as primary
- Padding: 13px 28px
- Hover: background fills to `rgba(212,185,106, 0.10)`, border upgrades to `#D4B96A`

---

## 4. Cards & Surfaces

- **Default card background:** `--navy-light` (`#162338`)
- **Default card border:** 1px solid `rgba(212,185,106, 0.18)`
- **Border radius:** 6px (pain/feature cards), 8px (service cards)
- **Left accent bar on cards:** 3px vertical bar, gradient `#D4B96A` → `#A8904E`
- **Card hover:** border upgrades to `rgba(212,185,106, 0.32)`, background becomes `#1C2D44`
- **Icon containers:** 36x36px, rounded 6px, background `rgba(212,185,106, 0.10)`, border `rgba(212,185,106, 0.18)`, stroke `#D4B96A`

---

## 5. Navigation

- Height: 70px, fixed
- Background: `rgba(7,9,13, 0.85)` with `backdrop-filter: blur(20px)`
- Bottom border: 1px solid `rgba(212,185,106, 0.18)`
- Logo: Plus Jakarta Sans, 14px, weight 800, uppercase — accent word in `#D4B96A`

---

## 6. Section Layout

- Section padding: `100px 64px` desktop, `72px 24px` mobile (breakpoint: 768px)
- Section separator: 1px bottom border using `rgba(212,185,106, 0.18)`
- Eyebrow labels always have a `22px` horizontal rule line before the text (via `::before` pseudo-element)
- Decorative rule below section eyebrow: 44px wide, 2px tall, gradient `#D4B96A` → `#E2CB85`

---

## 7. Hero Section

- Background: `--navy` (`#0B1220`)
- Padding: `220px 64px 128px` desktop, `120px 24px 80px` mobile
- Background grid: 64x64px grid lines in `rgba(212,185,106, 0.10)`, masked radially
- Ambient glow: two radial gradients using `rgba(212,185,106, 0.07)` and `rgba(212,185,106, 0.05)`

---

## 8. Animation

- All entrance animations use `fadeUp`: `opacity 0 → 1`, `translateY 22px → 0`
- Duration: 0.7s, easing: `cubic-bezier(.22, 1, .36, 1)` (spring-like deceleration)
- Staggered delays: `.15s`, `.30s`, `.45s`, `.60s`, `.75s`
- Hover transitions: `0.18s–0.25s`, same easing

---

## 9. Dos and Don'ts

### DO

- Use `#D4B96A` (gold) exclusively as the accent color — never swap it for yellow, amber, or orange
- Use Plus Jakarta Sans weight 800 for all display headings, always uppercase
- Apply the 3px gold left-border treatment on all card components
- Use `rgba` opacity variants of gold for borders and fills — never flat gold fills on dark backgrounds except for buttons
- Keep body copy in Space Grotesk on the dark scale backgrounds
- Use Syne only in small, uppercase, high-letter-spacing contexts (eyebrows, nav, labels)
- Keep border radius tight: 3px for buttons, 6–8px for cards
- Use `text-transform: uppercase` and wide letter-spacing for all Syne instances

### DON'T

- Don't use white as a background color — the brand is dark-first
- Don't use the gold color at full opacity on large background areas
- Don't mix heading fonts — Plus Jakarta Sans is the only display face
- Don't use DM Mono for body copy — it is for code/technical strings only
- Don't use rounded or pill-shaped buttons — border radius stays at 3px
- Don't use color fills on section backgrounds outside the defined dark scale (`--void`, `--navy`, `--navy-mid`)
- Don't use drop shadows as a depth mechanism — use border opacity and background step-ups instead
- Don't display the logo without the gold accent on the brand name word

---

## 10. Logo & Wordmark

- Asset path: `/branding_assets/logo-wordmark.png`
- OG image uses the wordmark on dark background
- Logo text treatment: white base, gold accent on a specific word — mirrors the `.nav-logo span { color: var(--gold) }` pattern

---

*Last updated: May 2026 — based on live CSS at goldstsolutions.com*
