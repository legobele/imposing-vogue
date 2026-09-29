# Imposing Vogue

A unified editorial design system — one set of tokens and components, reusable across future projects. Imposing like a Vogue cover, disciplined like a brand book.

## The fusion

Three inspirations, one system:

| # | Source | What it contributed |
|---|--------|---------------------|
| 1 | **Church announcement slide** ("ELIGIÉNDONOS" graphic) | Photo-forward hero · handwritten script layered *over* massive condensed serif caps · chartreuse/lime-yellow on imagery · small-cap sans details · circular badge mark · slide number "01" |
| 2 | **Vogue high fashion** | Imposing condensed display type (Oswald 600, uppercase) · monochrome discipline · generous whitespace · editorial section numbering |
| 3 | **Oakley sport-luxe** (oakley.com) | Dark cinematic surfaces · energy accents used with restraint · pill CTAs (100px radius, uppercase, tracked) · glassmorphism · heavy multi-layer text-shadows keeping over-image type cinematic · global letter-spacing as a luxury signal |

## Files

```
tokens.css      — every design decision as a CSS custom property
components.css  — buttons, hero, cards, tags, section heads, footer, utilities
index.html      — live demo showcasing every token and component
```

## Usage

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Oswald:wght@200..700&family=Pinyon+Script&family=EB+Garamond:ital,wght@1,400;1,500&family=Inter:wght@400;500;600;700&family=JetBrains+Mono:wght@400;700&display=swap" rel="stylesheet">

<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/legobele/imposing-vogue@main/tokens.css">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/legobele/imposing-vogue@main/components.css">
```

Or vendor the two CSS files into your project (recommended for offline-first sites).

## Tokens

### Color

| Token | Value | Role |
|-------|-------|------|
| `--ink` | `#111214` | Primary text / darkest surface |
| `--ink-2` | `#222222` | Secondary dark (Oakley) |
| `--paper` | `#ffffff` | Primary light surface |
| `--bone` | `#f6f6f6` | Light surface alt |
| `--smoke` | `#eeeeee` | Hairlines on light |
| `--muted` | `#3d3d3d` | Muted dark |
| `--faint` | `#999999` | Quiet meta text |
| `--chartreuse` | `#d7e14b` | **Primary energy accent.** Kickers, hero type on imagery, the one key CTA. Never body text. |
| `--signal` | `#c83430` | **Secondary accent.** Sparing use only — max one detail per viewport. |
| `--cobalt` | `#0e70ee` | Links on dark, informational |

### Type (Google Fonts only)

| Token | Font | Used for |
|-------|------|----------|
| `--font-display` | Oswald 600 | Imposing headlines, always uppercase |
| `--font-script` | Pinyon Script | Script accent layered over display |
| `--font-serif` | EB Garamond italic | Serif italic accents in body copy |
| `--font-sans` | Inter | Kickers, labels, body |
| `--font-mono` | JetBrains Mono | Tags, meta, stats |

Luxury signals: `--ls-luxe: 0.22em` on kickers/labels, `--ls-tight: -0.02em` on display.

### Shape & depth

- `--radius-pill: 100px` (CTAs), `--radius-card: 4px` (editorial sharpness), `--radius-chip: 999px`
- `--shadow-cinematic`: heavy multi-layer text-shadow for type over imagery
- `--shadow-lift` / `--shadow-card` for surfaces

## Components

| Class | What |
|-------|------|
| `.iv-kicker` | Tracked-out uppercase kicker, chartreuse |
| `.iv-display-1/2/3` | Imposing Oswald headlines (hero / section / card) |
| `.iv-script` | Script accent, pulled up to overlap the display line |
| `.iv-serif-accent` | Italic serif accent inside copy |
| `.iv-lede` | Section lede paragraph |
| `.iv-btn` + `.iv-btn-solid` / `.iv-btn-energy` / `.iv-btn-ghost` / `.iv-btn-ghost-light` | Pill CTAs |
| `.iv-hero`, `.iv-hero-media`, `.iv-hero-content`, `.iv-hero-actions`, `.iv-hero-index` | Full-bleed photo hero |
| `.iv-emblem` | Circular glass badge mark |
| `.iv-card-grid`, `.iv-card`, `.iv-card-index`, `.iv-card-title`, `.iv-card-desc`, `.iv-card-meta`, `.iv-card-links` | Numbered editorial cards |
| `.iv-tag` (+ `--energy`, `--signal`) | Mono pill tags |
| `.iv-sections`, `.iv-section`, `.iv-section-head` | Auto-numbered section heads (kicker → headline) |
| `.iv-footer`, `.iv-footer-brand`, `.iv-footer-meta` | Dark disciplined footer |
| `.iv-glass`, `.iv-cinematic`, `.iv-rule`, `.iv-pad`, `.iv-signal` | Utilities |

## Rules

1. **Chartreuse is energy, not decoration.** One hero moment, kickers, one CTA. If everything glows, nothing does.
2. **Signal red is rationed.** One detail per viewport, maximum.
3. **Display type is always uppercase Oswald 600.** Script is always Pinyon, always overlapping.
4. **Type over imagery is always cinematic** — never flat white on a photo.
5. **Light mode exists** (`data-iv-theme="light"`) but dark is the home turf.

---

Built for [benj legobele](https://github.com/legobele) — first consumer: her portfolio.
