# Division 7 — Design System

## Overview

**Division 7** is an indie rock band from Sweden. Their aesthetic is stark, physical, and confrontational — black-and-white photography of sweaty venues, crowd-surfing, stage-diving, and raw performance energy. The visual language is minimal but intense: no gradients, no decoration, just contrast and impact.

The band performs at mid-size Swedish venues (Pustervik, Fållan, etc.) and their photography captures that underground intimacy — grain, blown-out stage lights, silhouettes, crowds with hands raised.

**Sources provided:**
- Font file: `uploads/GellixExtraBoldItalic.otf` (Gellix Extra Bold Italic — primary heading font)
- Photography: 11 black-and-white live photos (see `assets/`)
- No codebase, Figma, or website URL was provided

---

## CONTENT FUNDAMENTALS

**Tone:** Direct, terse, unapologetic. The band doesn't explain themselves — they state. Copy is minimal and declarative, not descriptive. Think "Division 7. Gothenburg. Now." not "Division 7 is an exciting rock band from Gothenburg who play energetic shows."

**Voice:**
- Short sentences. Often sentence fragments.
- No fluff, no soft selling, no adjective-stacking.
- First person plural when needed ("we", "us") — rare. More often no personal pronoun at all.
- Direct address: "You were there." / "See you in the pit."
- Never precious or self-congratulatory.

**Casing:**
- Headings: ALL CAPS or Title Case — never sentence case for primary headlines.
- Band name always: **Division 7** (never "division 7" or "DIVISION 7" except in graphic treatments).
- Dates and venues: numeric and direct — "15 Nov — Pustervik, Gothenburg".

**Emoji:** Never. Zero. Not even sparingly.

**Language:** Swedish and English used interchangeably in context. Nothing is translated for comfort — if it's in Swedish, it stays in Swedish.

**Examples of copy in the spirit:**
- "On tour. No support needed."
- "Tickets. Merch. Nothing else."
- "Fållan. Sold out. Again."
- "New record. Out now."

---

## VISUAL FOUNDATIONS

### Colors
- **Black:** `#0a0a0a` — near-black, not pure. Used for backgrounds, heavy text.
- **White:** `#f5f5f0` — off-white, slightly warm. Used for text on dark, backgrounds on light.
- **Red (accent):** `#e8190e` — vivid, slightly warm red. Used sparingly: CTAs, highlights, active states, underlines.
- **Mid-grey:** `#888880` — used for secondary text, muted labels, borders.
- **Dark grey:** `#1a1a18` — used for card backgrounds, elevated surfaces on dark bg.
- **Light grey:** `#d4d4ce` — used for borders and dividers on light backgrounds.

### Typography
- **Display / Headings:** Gellix Extra Bold Italic — strong, urgent, slightly condensed feel. Used for all major headlines, track names, dates, hero text. All caps encouraged in large headings.
- **Body / UI:** Gellix Regular (weight 400) — used for all body text, navigation, labels, and UI elements. Clean grotesque with a slightly geometric character.
- **Mono / Technical:** `'Courier New', monospace` — used sparingly for track listings, timestamps, set lists.
- **Scale:** Large and aggressive. Headlines start at 48px and go up. Body text 15–17px. Never apologetically small.

### Backgrounds
- Primary: black (`#0a0a0a`) — the default canvas.
- Secondary: off-white (`#f5f5f0`) — for sections that need a breath.
- Photography: full-bleed, black-and-white, always. Photos are used as section backgrounds with a dark overlay (`rgba(0,0,0,0.45)`) so text reads on top.
- No gradients. No textures. No patterns.
- The stage-backlit image texture (blasted white light, dark crowd silhouettes) is a recurring visual motif — the contrast is the aesthetic.

### Imagery
- **Always black and white.** No color photography, ever.
- **High grain, high contrast.** The images feel like film — pushed ISO, blown highlights, crushed blacks.
- **Subject matter:** live performance, crowds, intimacy between band and audience, stage from behind, instruments close up.
- Images are used at full-bleed width, often cropped wide (landscape). Portrait crops used for individual band members.

### Spacing
- Generous whitespace on the page level, but tight spacing within components.
- Section padding: 80–120px vertical.
- Component inner padding: 16–24px.
- Typography tightly leaded: `line-height: 1.05–1.1` for headlines, `1.55` for body.

### Corner Radii
- **Zero.** No rounded corners anywhere. Everything is sharp/rectangular — consistent with the raw, industrial feel.

### Cards
- No rounding. Thin border: `1px solid #1a1a18` on dark; `1px solid #d4d4ce` on light.
- No shadow. Cards are defined by border or background contrast only.
- Dark card bg: `#1a1a18`. Light card bg: `#f5f5f0`.

### Borders & Dividers
- `1px solid` lines. Hairline. Never decorative — only structural.
- Red accent used as a single underline/border on active or highlighted items.

### Hover States
- Text links: color shifts to red (`#e8190e`) or opacity drops to 0.6.
- Buttons: background inverts (dark↔light) or fills red.
- Images: slight brightness increase (`filter: brightness(1.1)`).
- No scale transforms. No bounces.

### Press / Active States
- Button depresses with `opacity: 0.8` + no transform.
- Links go red.

### Animations
- Minimal. Fade only: `opacity 0.15s ease`. No slides, no bounces, no spring physics.
- The brand does not perform visually — the music performs.

### Shadows
- None. No drop shadows, no box shadows, no text shadows.

### Transparency & Blur
- Blur: never (no frosted glass).
- Transparency: only for photo overlays (`rgba(0,0,0,0.45)`). Never on UI elements.

### Layout
- Fixed header (navigation) always present.
- Content in a max-width container: `1200px`, centered.
- Full-bleed photo sections break out of the container.
- Asymmetric grid encouraged for editorial feel — not everything in equal columns.

---

## ICONOGRAPHY

No icon set was provided with the brand materials. Based on the aesthetic:
- **No decorative icons** used as UI chrome. Navigation is text-only.
- If icons are needed (social, playback), use a **minimal line-icon set** — recommended: [Phosphor Icons](https://phosphoricons.com/) (thin weight) via CDN.
- No emoji substitutes for icons.
- Social links: text labels ("Instagram", "Spotify") preferred over icon-only links.
- **No custom SVG illustrations.** The brand relies on photography, not illustration.
- Unicode characters are occasionally used for structural elements (em-dash `—`, bullet `·`).

CDN for icons (if needed):
```html
<script src="https://unpkg.com/@phosphor-icons/web"></script>
```

---

## FILE INDEX

```
/
├── README.md                          — This file
├── SKILL.md                           — Agent skill definition
├── colors_and_type.css                — CSS custom properties (colors, type, tokens)
├── fonts/
│   └── GellixExtraBoldItalic.otf     — Primary display font
├── assets/
│   ├── fallan-wide.jpg               — Wide stage shot, Fållan venue
│   ├── pustervik-surf-crop.jpg       — Crowd surf shot, Pustervik
│   ├── diffust.jpg                   — Stage shot from behind, diffuse light
│   ├── DSCF4337_svartvitt.jpg        — Portrait: keyboard/synth close-up
│   ├── DSCF4460_svartvitt.jpg        — Crowd, hands up, wide shot
│   ├── DSCF4544_svartvitt.jpg        — Stage end, saxophonist, band behind
│   ├── DSCF4557_svartvitt.jpg        — Saxophonist silhouette
│   ├── DSCF4576_svartvitt.jpg        — Band from behind, crowd in front
│   ├── DSCF4673_svartvitt.jpg        — Wide stage, band + crowd, blasted light
│   └── DSCF4686_svartvitt.jpg        — Guitarist crouching on stage edge
├── preview/
│   ├── colors-base.html              — Base color palette
│   ├── colors-semantic.html          — Semantic color tokens
│   ├── type-display.html             — Display / heading type specimens
│   ├── type-body.html                — Body & mono type specimens
│   ├── type-scale.html               — Full type scale
│   ├── spacing-tokens.html           — Spacing + radius + border tokens
│   ├── components-buttons.html       — Button states
│   ├── components-nav.html           — Navigation bar
│   ├── components-cards.html         — Event / release cards
│   ├── components-badges.html        — Badges & labels
│   ├── brand-photography.html        — Photography usage examples
│   └── brand-logo.html              — Wordmark / logotype treatment
└── ui_kits/
    └── website/
        ├── README.md                 — Website UI kit notes
        └── index.html               — Interactive band website prototype
```
