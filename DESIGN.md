# Florida Funders — Design System (DESIGN.md)

<img src="assets/flf-logo-horizontal.png" alt="Florida Funders" width="360">

> Source: *FL Funders Brand Identity — 2025*. This document translates the brand guidelines into a developer-ready design reference (design tokens, typography scale, logo rules, voice).

> **Audit status (2026-07-06):** reconciled against the live Figma file `ZDc3GIQgFJ1sJULel8UUo3` (page 🧤 Guidelines). All ~40 cited node IDs resolve. Seven material corrections are folded in inline (search "audit 2026-07-06"): Button `ghost`/size-naming, Tabs active-label color, Platform Apple/iCloud, LogoWall height cap, OfferingCard overlay alpha, Input `auto` size, and Input focus provenance. Confirmed-correct tokens and Figma-side hygiene items (layer-name typos, generic frame names) are tracked outside this file.

---

## 1. Brand Overview

Florida Funders is the Southeast's most active early-stage VC — a hybrid venture capital fund and active investor network (2,000+ investors, 100+ portfolio companies across four funds). Focus vertical: **B2B SaaS**, from late pre-seed through early Series A.

Brand personality: stable, reliable, innovative, direct, partnership-focused. "Founders helping founders."

---

## 2. Color

### Primary Palette
Used across interactive elements: CTAs, links, inputs, active states.

| Token | Name | HEX | RGB | CMYK |
|-------|------|-----|-----|------|
| `--color-cyan` | Bluish Cyan | `#00AFE2` | 0, 175, 226 | 72, 11, 2, 0 |
| `--color-lime` | Lemon Green | `#A8F200` | 168, 242, 0 | 38, 0, 100, 0 |
| `--color-aquamarine` | Aquamarine | `#61D9AF` | 97, 217, 175 | 55, 0, 43, 0 |
| `--color-atlantis` | Medium Atlantis | `#95CB23` | 149, 203, 35 | 47, 0, 100, 0 |
| `--color-ink` | Black Gradient | `#222222` | 34, 34, 34 | 71, 66, 64, 72 |

**Brand gradient:** transition from Bluish Cyan `#00AFE2` → Lemon Green `#A8F200` (represents financial transformation, growth, and trust).

### Secondary — Neutrals

| Token | Name | HEX | RGB |
|-------|------|-----|-----|
| `--color-black` | Black | `#000000` | 0, 0, 0 |
| `--color-white` | White | `#FFFFFF` | 255, 255, 255 |

### Status Colors

| Purpose | Token | HEX | RGB |
|---------|-------|-----|-----|
| Danger | `--color-danger` | `#FF4747` | 255, 71, 71 |
| Danger (light) | `--color-danger-light` | `#FFDADA` | 255, 218, 218 |
| Warning | `--color-warning` | `#FF8E3C` | 255, 142, 60 |
| Warning (light) | `--color-warning-light` | `#FFE8D8` | 255, 232, 216 |
| Success | `--color-success` | `#13BA74` | 19, 186, 116 |
| Success (light) | `--color-success-light` | `#E7F8F1` | 241, 248, 241 |

### CSS Custom Properties

```css
:root {
  /* Primary */
  --color-cyan:        #00AFE2;
  --color-lime:        #A8F200;
  --color-aquamarine:  #61D9AF;
  --color-atlantis:    #95CB23;
  --color-ink:         #222222;

  /* Neutrals */
  --color-black:       #000000;
  --color-white:       #FFFFFF;

  /* Status */
  --color-danger:        #FF4747;
  --color-danger-light:  #FFDADA;
  --color-warning:       #FF8E3C;
  --color-warning-light: #FFE8D8;
  --color-success:       #13BA74;
  --color-success-light: #E7F8F1;

  /* Brand gradient */
  --gradient-brand: linear-gradient(90deg, #00AFE2 0%, #A8F200 100%);
}
```

---

## 3. Typography

**Primary typeface: Clash Display.** Set headlines in Bluish Cyan and Lemon Green where appropriate.

Weights used: Light, Regular, Medium, SemiBold, Bold, Extrabold.
- **Bold** — headlines, subheadlines, captions, CTAs
- **Regular** — body copy

### Heading Scale
Format: `size / line-height` in px.

| Level | Size / Line-height | Weight |
|-------|--------------------|--------|
| H1 | 72 / 120 | Bold |
| H2-L | 60 / 120 | Bold |
| H2 | 48 / 120 | Bold |
| H2-S | 40 / 120 | SemiBold |
| H3 | 32 / 120 | SemiBold |
| H4 | 24 / 130 | Bold |
| H5 | 20 / 130 | SemiBold |

### Body Scale

| Token | Size / Line-height | Weight |
|-------|--------------------|--------|
| L-Medium | 18 / 160 | Medium |
| L-Bold | 18 / 160 | Bold |
| L-Extrabold | 18 / 160 | Extrabold |
| Medium | 16 / 160 | Medium |
| Bold | 16 / 160 | Bold |
| Extrabold | 16 / 160 | Extrabold |
| S-Regular | 14 / 160 | Regular |
| S-Bold | 14 / 160 | Bold |
| Button | 16 / 100 | SemiBold |

### CSS Tokens

```css
:root {
  --font-family-primary: "Clash Display", sans-serif;

  --h1: 700 72px/120% var(--font-family-primary);
  --h2-l: 700 60px/120% var(--font-family-primary);
  --h2: 700 48px/120% var(--font-family-primary);
  --h2-s: 600 40px/120% var(--font-family-primary);
  --h3: 600 32px/120% var(--font-family-primary);
  --h4: 700 24px/130% var(--font-family-primary);
  --h5: 600 20px/130% var(--font-family-primary);

  --body-l: 500 18px/160% var(--font-family-primary);
  --body-m: 500 16px/160% var(--font-family-primary);
  --body-s: 400 14px/160% var(--font-family-primary);
  --button: 600 16px/100% var(--font-family-primary);
}
```

---

## 4. Logo

<img src="assets/flf-logo-horizontal.png" alt="Florida Funders — primary horizontal logo" width="440">

_Primary horizontal lockup. Assets live in [`assets/`](assets/): [`flf-logo-horizontal.png`](assets/flf-logo-horizontal.png) (1200 px web) and [`flf-logo-horizontal@master.png`](assets/flf-logo-horizontal@master.png) (4019 px master, transparent). Exported from Figma node `4026-2`._

The FLF mark is geometric and modern — bold, blocky, interconnected "F / L / F" letters conveying stability, reliability, and precision. Uses the green→blue brand gradient.

**Variations:** Master logo, primary horizontal logos (a, b, c), a vertical logo (d — use sparingly, only when horizontal space is limited), and secondary variations.

### Clear space (exclusion zone)
Always keep clear space around the logo — no graphics or text inside it. Minimum padding is derived from the logo's `x` unit (guideline reference values: 2x / 5x / 15x / 20x depending on side). Keep generous margins.

### Minimum sizes
- **Screen:** 100 px wide minimum
- **Print:** 35 mm wide minimum

### Positioning
Digital or print, portrait or landscape: place the logo in one of the four corners or centered on the vertical axis. Make it as large as the layout allows. Avoid using it smaller than **one-third of the canvas width**. "Be bold, be proud, make it big."

### App Icon / Favicon
Derived from the FLF symbol. Site: https://floridafunders.com

### Do NOT
- Rotate the logo
- Stretch or squeeze it in any direction
- Recolor it with off-brand colors
- Outline the logo

---

## 5. Voice & Tone

- We are founders ourselves — speak from authentic, hands-on experience while maintaining professional investment expertise.
- Direct, transparent, partnership-focused. Reflects active engagement and long-term relationships.
- Balance sophisticated investment knowledge with approachable, tactical insights from operational experience.
- Optimistic yet pragmatic, emphasizing real-world results — whether addressing investors or founders.

### Core Messages
- **Founders helping founders** — battle-tested experience in every relationship.
- The Southeast's most active early-stage VC — institutional strength + entrepreneurial DNA.
- More than capital — a hybrid model uniting traditional VC with a network of 2,000+ operators.
- Deep involvement from day one — true partners who help navigate challenges and accelerate growth.
- Right time, right place — rooted in the Southeast, investing wherever innovation leads.

---

## 6. Components

### Button
Implemented from Figma (node `4002-68`). Reusable component in `Button.jsx`.

**Base spec (all sizes):** border-radius `6px`, icon–label gap `8px`, Clash Display `600` (SemiBold), icon `16px`, `1px` border.

> **Figma alignment (audit 2026-07-06):** the Figma component set has four axes — **Variant** (`Cyan`/`Atlantis`/`Gradient`/`Black`), **Size** (`xs`/`S`/`M`/`L`), **State** (`Default`/`Hover`/`Disable`), and **Outline** (`Inactive`/`Active`/`Disable`) — with a single `6px` corner radius. There is **no `ghost` value in Figma**: our `ghost` appearance is a deliberate code-only extension. Code size names `sm`/`md`/`lg` map to Figma `S`/`M`/`L`.

**Props**
- `variant`: `cyan` · `atlantis` · `gradient` · `black`
- `appearance`: `solid` (Figma "Inactive"/filled) · `outline` (Figma "Active") · `ghost` (**code-only**, text-only — not in Figma)
- `size`: `xs` · `sm` · `md` · `lg` (Figma labels these `xs`/`S`/`M`/`L`)
- `leftIcon` / `rightIcon`: node, or `true` for the default user / chevron icons
- `fullWidth`, `disabled`

**Sizes**

| Size | Font | Line-height | Padding | Icon |
|------|------|-------------|---------|------|
| xs | 14px | 18px | 6px 14px | 14px |
| sm | 16px | 18px | 8px 20px | 16px |
| md | 16px | 18px | 11px 28px | 16px |
| lg | 16px | 18px | 14px 32px | 16px |

**Variant colors**

| Variant | Fill | Hover | Text | Soft (disabled/outline hover) |
|---------|------|-------|------|------|
| Cyan | `#00AFE2` | `#0092BE` | `#FFFFFF` | `#00AFE2` @ 20% |
| Atlantis | `#95CB23` | `#7BA91C` | `#FFFFFF` | `#95CB23` @ 20% |
| Gradient | `135deg #00AFE2→#A8F200` | darkened | `#FFFFFF` | gradient @ 20% |
| Black | `#222222` | `#000000` | `#A8F200` (Lemon Green) | `#333333` @ 20% |

**States**
- **Solid** — filled variant color, white text (Lemon Green on Black). Hover darkens the fill.
- **Outline** — transparent fill, `1px` variant-colored border and text; hover fills with the soft (20%) tint.
- **Ghost** — transparent fill, hairline `#E0E0E0` border, muted `#4F4F4F` text.
- **Disabled** — solid: 20% fill tint + `#D1D1D1` text; outline: `#E0E0E0` border + `#D1D1D1` text; `not-allowed` cursor.

### Radio
Implemented from Figma (node `4080-1804`). Reusable `Radio` + `RadioGroup` in `Radio.jsx`.

**Spec:** circle drawn with `1.5px` border, fully rounded. Inner dot = 60% of the circle diameter. Label: Clash Display Medium `16px` / `24px` line-height, letter-spacing `0.3px`, color `#333333`, `8px` gap from the control. Standalone state chips render at `24px`; labelled radios at ~`16–20px`.

**Props (`Radio`)**: `checked`, `disabled`, `label`, `name`, `value`, `onChange`, `size`.
**Props (`RadioGroup`)**: `name`, `value`, `onChange`, `options: [{value, label, disabled?}]`, `direction`, `gap`, `size`.

**States**

| State | Border | Fill / dot | Extra |
|-------|--------|-----------|-------|
| Default | `rgba(51,51,51,0.8)` | white, no dot | — |
| Hover | `#95CB23` (Atlantis) | white, no dot | — |
| Focus | `#95CB23` | white | `0 0 0 3px rgba(168,242,0,0.2)` halo (Lemon Green 20%) |
| Selected | `#95CB23` | dot `rgba(149,203,35,0.8)` (Atlantis 80%) | — |
| Disabled | `rgba(38,38,38,0.2)` | white, no dot | `not-allowed` cursor, muted label |

Uses a real `<input type="radio">` for accessibility with the visual circle drawn over it; hover/focus states are CSS-driven.

### Checkbox
Implemented from Figma (node `4259-2242`). Reusable `Checkbox` in `Checkbox.jsx`.

**Spec:** box `20px`, border-radius `3px`, `1.5px` border. Checked fills Atlantis 90% with a white checkmark (~75% of box). Label: Clash Display Regular `14px` / `18px` line-height, letter-spacing `0.3px`, color `#131927` (`#9EA2AE` when disabled). Label sits right (gap `8px`) or left (gap `16px`) of the box.

**Props**: `checked`, `disabled`, `label`, `textSide` (`left` \| `right`), `name`, `value`, `onChange`, `size`.

**States**

| State | Border | Background | Extra |
|-------|--------|-----------|-------|
| Default | `rgba(51,51,51,0.8)` | white | — |
| Hover | `#95CB23` (Atlantis) | `rgba(231,231,231,0.6)` | — |
| Focus | `#95CB23` | white | `0 0 0 3px rgba(149,203,35,0.2)` halo |
| Selected | `#95CB23` | `rgba(149,203,35,0.9)` | white check |
| Disabled | `#E5E7EA` (Grey/200) | white | muted label, `not-allowed` |

Built on a real `<input type="checkbox">` for accessibility with the styled box layered over it; hover/focus states are CSS-driven.

### Pagination
Implemented from Figma (node `4090-228`). Reusable `Pagination` + `PaginationItem` in `Pagination.jsx`.

**Spec:** each item is a `48px` circle (radius `24px`, `12px` padding) holding a page number or a `24px` nav chevron. Item gap `8px`. Number text `16px` / `24px` line-height. Includes automatic ellipsis truncation for large page counts.

**Props (`Pagination`)**: `currentPage`, `totalPages`, `onPageChange`, `siblingCount`, `showArrows`.

**Item states**

| State | Background | Text/icon | Extra |
|-------|-----------|-----------|-------|
| Default | transparent | `#000000` | — |
| Hover | `rgba(0,175,226,0.1)` (Cyan 10%) | `#000000` | — |
| Focus | white | `#000000` | `1.5px` `#00AFE2` ring |
| Selected | `rgba(0,175,226,0.5)` (Cyan 50%); arrows `Cyan 30%` | `#000000` | `aria-current="page"` |
| Disabled | transparent | `#9EA2AE` | `not-allowed` (used for arrows at bounds) |

Rendered as a `<nav>` of real `<button>`s with `aria-label` / `aria-current` for accessibility.

> Note: the Figma frame set page numbers in Inter; this implementation uses Clash Display to stay consistent with the rest of the FF component set. Swap the item `fontFamily` if Inter is intended.

### Dropdown / Select
Implemented from Figma (node `4093-310`). Reusable `Dropdown` in `Dropdown.jsx`. Supports single and multiple selection.

**Trigger spec:** radius `12px`, `1.5px` border, `12px` padding, `12px` gap; optional `24px` left icon, label (Clash Display Regular `14px` / `18px`), and a chevron that flips when open.

**Menu spec:** white, radius `8px`, `8px` vertical padding, item gap `8px`, shadow `0 6px 14px -6px rgba(19,25,39,0.12), 0 10px 32px -4px rgba(19,25,39,0.1)`. Rows: padding `12px 16px 12px 12px`, `24px` icon + `14/18` label.

**Props**: `options: [{value, label, disabled?}]`, `value`, `onChange`, `placeholder`, `multiple`, `disabled`, `showIcon`, `width`.

**Trigger states**

| State | Border | Extra |
|-------|--------|-------|
| Default | `#E5E7EA` (Grey/200) | chevron down |
| Hover | `#95CB23` (Atlantis) | — |
| Expanded | `#95CB23` | `0 0 0 3px rgba(149,203,35,0.3)` halo, chevron up |
| Disabled | `#E5E7EA` | text `#9EA2AE`, icons `#D2D5DB`, `not-allowed` |

**Menu-item states**

| State | Background | Text | Extra |
|-------|-----------|------|-------|
| Default | transparent | `#131927` | — |
| Hover | `#95CB23` (Atlantis) | `#131927` | — |
| Selected | transparent | `#131927` | cyan check `#00AFE2` (right) |
| Disabled | transparent | `#9EA2AE` | `not-allowed` |

Closes on outside-click; trigger carries `aria-haspopup` / `aria-expanded`, menu uses `role="listbox"` / `role="option"`. Star icon and chevrons are inline SVG (Figma used hosted assets); the multi-select trigger summarizes as "Selected: N options".

### Progress Bar
Implemented from Figma (node `4115-298`). Reusable `ProgressBar` in `ProgressBar.jsx`.

**Spec:** track `8px` tall, radius `8px`. Fill uses the brand gradient `linear-gradient(90deg, #A8F200 0%, #00AFE2 100%)` (Lemon Green → Bluish Cyan), width = `value%`. Optional percentage label (Clash Display Regular `14px` / `18px`, tracking `0.3px`) sits left or right with a `16px` gap.

**Props**: `value` (0–100), `showLabel`, `labelPosition` (`left` \| `right`), `disabled`, `height`, `width`.

**States**

| State | Track | Fill | Label |
|-------|-------|------|-------|
| Active | `#EDEFFE` (Primary/50) | green→cyan gradient | `#131927` |
| Disabled | `#F3F4F6` (Grey/100) | none | `#9EA2AE` |

Rendered with `role="progressbar"` and `aria-valuenow/min/max`; the fill width animates on change.

### Input / Textarea
Implemented from Figma (node `4093-1112`, "Define Input Component Variants"). Reusable `Input` + `Textarea` in `Input.jsx`.

**Base spec:** radius `8px`, default border `#D1D5DC`, label Clash Display `14px` / `18px` (`#364153`), placeholder `#99A1AF`, value `#111827`.

**Interaction states** (node `4813-2843`): hover on a resting field fills light grey `#E7E7E7`; focus/selected shows a `1.5px` Atlantis-green (`#95CB23`, ~`80%`) border + soft green halo; a `required` empty field can surface a `1.5px` danger (`#C54949`) border via `status="error"`. Status inputs halo in their own color. (Focus was aligned to Atlantis green to match Radio/Checkbox/Dropdown — note: the Figma interaction frame `4813-2843` defines `Default/hover/selected/error/data/required/disabled` but **no explicit `focus` state**, so the input focus styling is a deliberate decision carried over from Radio/Checkbox, not sourced from this frame.)

**Sizes**

| Size | Height | Padding-X | Font |
|------|--------|-----------|------|
| small | 32px | 12px | 12px |
| medium (default) | 40px | 16px | 16px |
| large | 48px | 16px | 16px |
| auto | content | 16px | 16px |

> **Figma note (audit 2026-07-06):** Figma also defines a fourth **`auto`** (content-height) size — added above. Consider surfacing it on the `inputSize` prop, or intentionally exclude it.

**Status states**

| Status | Border | Background | Helper / icon |
|--------|--------|-----------|---------------|
| default | `#D1D5DC` | white | — |
| error | `#C54949` | `#FFDADA` | helper `#E7000B`, alert-circle icon |
| success | `#13BA74` | `#E7F6F1` | helper `#13BA74`, check-circle icon |
| warning | `#FF8E3C` | `#FFECB6` | helper `#E17100`, alert-triangle icon |
| disabled | `rgba(51,51,51,0.2)` | `rgba(176,176,176,0.1)` | `not-allowed`, muted text |
| readonly | same as disabled visual | — | non-editable |

**Props (`Input`)**: `label`, `value`, `onChange`, `placeholder`, `type` (`text`/`email`/`password`/`number`/`tel`/`date`/`search`), `inputSize`, `status`, `disabled`, `readOnly`, `required`, `optional`, `helperText`, `leftIcon`, `rightIcon`, `id`, `name`, `width`.

Icons sit at `12px` from the edge (`20px`); left/right padding grows to `40px` when present. `type="password"` adds an eye reveal toggle; status inputs auto-show their status icon on the right. `required` renders a red asterisk, `optional` a grey "(optional)" tag. Bundled inline icons: search, mail, lock, phone, calendar, user, eye/eye-off, alert-circle, check-circle, alert-triangle.

`Textarea` shares the same tokens/status system with a multiline field (`rows`, vertical resize).

### Message (modal dialog)
Implemented from Figma (node `4281-675`). Reusable `Message` in `Message.jsx`.

**Spec:** centered card, width `382px`, radius `16px`, shadow `0 25px 50px -12px rgba(0,0,0,0.25)`, padding `40px 31px`, over a `rgba(17,24,39,0.55)` backdrop. Stacked content (`15px` gap): brand logo, title (Clash Display SemiBold `20px`, `#111827`, centered, supports line breaks), a `64×4px` rounded gradient divider (`#4ADE80 → #60A5FA`), body text (Clash Display Regular `14px` / `18px`, `#4B5563`), and a full-width `48px` gradient button (`#A8F200 → #00AFE2`, radius `6px`, black `16px` label). Close (X) button top-right.

**Props**: `open`, `onClose`, `onAction`, `title`, `description`, `actionLabel`, `logo`, `showClose`, `width`. _(Figma defaults: FF wordmark logo, title "Registration completed successfully", body "Your account has been created", action label "Submit".)_

Backdrop click and `Escape` close the dialog; `role="dialog"` + `aria-modal`, close button `aria-label`. The FF logo is recreated inline (mark + wordmark) so there's no hosted-asset dependency; pass a `logo` node to override.

### Platform buttons (social login)
Implemented from Figma (node `4239-274`, "Platforms"). Reusable `PlatformButton` + `PlatformButtons` in `Platforms.jsx`.

**Spec:** each tile is `68 × 48px`, white, radius `6px`, hairline border `rgba(0,0,0,0.1)`, centered `~21px` brand icon; group gap `12px`. Hover lightens the fill to `#F9FAFB` and darkens the border to `rgba(0,0,0,0.2)`.

**Props (`PlatformButton`)**: `platform` (`google` \| `apple` \| `outlook` \| `linkedin` \| `facebook`), `onClick`, `width`, `height`, `ariaLabel`. **Note (audit 2026-07-06):** the 2nd Figma tile is labelled **iCloud**, not Apple — confirm whether the real provider is "Sign in with Apple" (`apple`) or iCloud before shipping, and align the prop value + icon accordingly.
**Props (`PlatformButtons`)**: `platforms` (array), `onSelect`, `gap`.

Brand logos are recreated as inline SVG (no hosted-asset dependency); each button gets a "Continue with …" `aria-label`.

### LogoWall ("Investments Logo")
Implemented from Figma (node `4116-2656`, "logos"). Reusable `LogoWall` in `LogoWall.jsx`.

**Spec:** section title Clash Display SemiBold `32px` / `40px` (`#434343`) + hairline divider (`#E5E7EB`), followed by a logo grid — default 2 columns (or `auto-fit` responsive), column gap `48px`, row gap `40px`, logos vertically centered and capped at `48px` tall.

> **Figma note (audit 2026-07-06):** the source frame is not consistent with the `48px` cap — 2ULaundry renders at `52px` and valicyber at `54px`. The component's `maxLogoHeight` (default `48`) enforces the documented cap; leave it on unless the intent is to raise the cap to ~`54px`. (The Figma title also reads "Investmens Logo" — a typo to fix in the file.)

**Props**: `title`, `logos: [{src, alt, height}]`, `columns` (set falsy for responsive `auto-fit`), `grayscale`, `maxLogoHeight`, `minColumnWidth`.

Portfolio-company logos are third-party brand assets, so they're passed as data rather than hardcoded. When a logo has no `src`, a muted name placeholder renders (useful in dev). `DEFAULT_INVESTMENT_LOGOS` ships the nine companies from the frame as alt-text entries — supply real logo files (`src`) to display them.

> Note: the Figma frame embeds the actual company logos via short-lived hosted URLs; those aren't baked in. Drop the real logo image files into the `logos` prop.

### Calendar / Date pickers
Implemented from Figma (nodes `4357-1111` "Calendars" and `4524-350` "Calendars Input"). Reusable `Calendar`, `DateInput`, and `DateRangePicker` in `Calendar.jsx`.

**Popover spec:** white card, radius `16px`, shadow `0 8px 40px -8px rgba(43,48,59,0.12)`, padding `24px`. Month title Clash Display SemiBold `18px` / `28px` (`#2B303B`), centered above the grid; weekday headers Clash Display Medium `12px` (`#818898`). Prev/next chevrons (`#818898`) flank the title — in the dual-month view they sit at the far left/right of the whole popover, one navigation control moving both months together.

**Grid:** 7 columns, **Sunday-first**. Weekday headers are **Spanish** — `Do Lu Ma Mi Ju Vi Sa` — while **month names render in English** (e.g. `January 2026`, `February 2026`), matching the frames. Day cells are `40px` tall with a `36px` round hit target; day text `14px` (`#2B303B`).

**Day-cell states**

| State | Fill | Text | Notes |
|-------|------|------|-------|
| Default | transparent | `#2B303B` | — |
| Hover | Atlantis tint `rgba(149,203,35,0.12)` | `#2B303B` | round `36px` target |
| Selected | Atlantis `#95CB23` (solid round) | `#FFFFFF` | single date or range endpoints |
| In-range | light Atlantis tint | `#2B303B` | days between range endpoints (range mode) |
| Out-of-month | transparent | muted `#C7CBD3` | leading/trailing days shown from adjacent months |
| Disabled | transparent | `#C7CBD3` | `not-allowed`, non-selectable |

**Triggers**
- `DateInput` — `MM/DD/YYYY` field (`1px #E5E7EB` border, radius `10px`, placeholder `#818898`, right calendar icon) opening a **single-month** popover.
- `DateRangePicker` — "Select date range" pill (`224×40`, `1px #D1D1D1` border, radius `12px`, calendar icon + chevron) opening a **dual-month** popover with range selection.

**Props (`Calendar`)**: `months` (1 or 2), `value`, `range`, `rangeValue {start,end}`, `onChange`, `initialMonth`, `minDate`, `maxDate`. Real date math (Sunday-first grid, month navigation, range logic including in-range highlighting); closes on outside-click.
**Props (`DateInput`)**: `value`, `onChange`, `placeholder` (default `MM/DD/YYYY`), `disabled`, `minDate`, `maxDate`, `id`, `name`.
**Props (`DateRangePicker`)**: `value {start,end}`, `onChange`, `placeholder` (default `Select date range`), `disabled`.

Days carry `aria-current="date"` when selected and the grid is keyboard-navigable (arrow keys move by day/week, Enter selects); the popover traps focus and restores it to the trigger on close. Calendar/chevron icons are inline SVG (Figma used hosted assets).

### Filters (panel)
Implemented from Figma (node `4252-877`, "Filters = Offerings"). Reusable `FilterButton`, `FilterPanel`, and `Filters` (wired) in `FilterPanel.jsx`.

**Trigger:** outline button (`1px #D1D1D1`, radius `6px`, `48px` tall) with a sliders icon + "Filters" (`16px`, `#4F4F4F`).

**Panel:** `320px`, white, `1px #E5E7EB` border, radius `12px`, shadow `0 10px 15px -3px rgba(0,0,0,.1), 0 4px 6px -4px rgba(0,0,0,.1)`, padding `16px`. Header "Filters" (plain `#262626` text — no highlight) + close X; a **filled light-grey search field** (`#E7E7E7`, radius `8px`, magnifier icon + "Search investments…" placeholder); collapsible sections titled **"Filter by {name}"** (e.g. Filter by Status / Filter by Profile Type) each with a collapse chevron; footer (top border) with **View All** (outline, `#D1D1D1` border) + **Save View** (Atlantis `#95CB23`, black label) buttons.

**Tag chips:** radius `12px`, default fill `rgba(241,242,244,0.5)`, text `#222`. Selected = `rgba(130,203,21,0.1)` fill + `1px #82CB15` (green) border. List sections stack full-width chips (`36px`); grid sections use a 2-column layout (`38px` chips).

**Props (`FilterPanel`)**: `open`, `onClose`, `searchPlaceholder`, `sections: [{id, title, layout: "list"|"grid", options: [{value,label}]}]`, `value`, `onChange`, `onSave`, `onViewAll`, `width`. Selection is multi-select per section (controlled or internal); search filters options live; sections collapse; `Filters` wraps button + panel with outside-click close. `DEFAULT_SECTIONS` provides Status + Profile Type examples; `INVESTMENT_SECTIONS` (node `4257-154`, "Filters = Investments") provides a single Status section (Live / Successful / Closed).

### Tag
Implemented from Figma (node `4253-224`, "Tags"). Reusable `Tag` in `Tag.jsx` — the selectable chip used inside `FilterPanel`.

**Spec:** radius `12px`. Large `286×36`, small `139×38`. States: default (white, `1px rgba(51,51,51,0.1)` border), hover (`rgba(241,242,244,0.5)` fill), selected (`rgba(130,203,21,0.1)` fill + `1px #82CB15` green border). Text Clash Display `13.3px` / `20px`, `#222`.
**Props**: `size` (`large`\|`small`), `selected`, `disabled`, `onClick`, `fullWidth`.

### Footer
Implemented from Figma (node `4082-110`, "Footer"). Reusable `Footer` in `Footer.jsx`.

**Spec:** slim bar, top hairline `#F3F4F6`, `~53px` tall, `0 30px` padding. Left: copyright `12px` `#6C757D`. Right: "Please review our" (`#6C757D`) + underlined **important disclosure** link (`#222`, `13.3px`, medium). The two Figma variants (with-navbar / pre-login) differ only by width — renders full-width with an optional `maxWidth`.
**Props**: `copyright`, `reviewText`, `linkText`, `onDisclosureClick`, `maxWidth`.

### Disclosure (modal)
Implemented from Figma (node `4283-646`, "Important Disclosure" popup). Reusable `Disclosure` in `Disclosure.jsx`.

**Spec:** centered modal (`439px`, radius `16px`) over a dimmed backdrop. Title Clash Display SemiBold `32px` / `40px` (`#29303D`, centered); a bordered (`#E5E7EB`, radius `8px`) scrollable box (`max-height 382px`) of legal paragraphs (`14px` / `22px`, `#6C757D`); a centered "Go back" link with a left arrow. **No close (X) button** — Go back (plus backdrop-click / Escape) is the only dismiss control.
**Props**: `open`, `onGoBack`/`onClose`, `title`, `paragraphs`, `width`. Backdrop-click + `Escape` close; `role="dialog"` + `aria-modal`. `DEFAULT_DISCLOSURE` ships the four FF legal paragraphs.

### Tabs
Implemented from Figma (nodes `4354-355` "Tabs" and `4550-2475` "Tabs Investments"). Reusable `Tabs` in `Tabs.jsx` — one component covers both.

**Spec:** horizontal `role="tablist"`. Active tab: dark label (Figma binds `Basic-Text/900/70` = `rgba(51,51,51,0.7)`; our code uses `#111827` — reconcile to the Figma token if matching 1:1) + a `4px` green underline (`#13BA74`). Inactive: muted `#6B7280`. Labels Clash Display Medium (`16px` default, `size` prop). Optional per-tab `count` renders a `24px` pill badge — Atlantis `#95CB23` when the tab is active, `#E5E7EB` otherwise (badge text `#374151`, `12px`).
**Props**: `items: [{value, label, count?}]`, `value`, `onChange`, `size`.

### SidebarNav
Vertical icon-rail main navigation with hover tooltips (Figma node `4112-2506`). In `SidebarNav.jsx`. 79px rail with a **square brand logo + hairline divider at the top**, then **8** `56×56` rounded (r12) tiles, 22px inline-SVG icons. Default order (audit 2026-07-07): **Dashboard · Browse Offerings · My Investments · Documents · My Inbox · Profiles · Account Info · Accreditation**. States: default (icon `#98A6AD`), hover (tile fill `rgba(152,166,173,0.1)`), selected (**lime→teal gradient `#A8F200 → #61D9AF`**, white icon). The **My Investments** tile carries a green glow (`drop-shadow` ~`rgba(74,222,128,.25)`). Hover reveals a dark `#222` pill label (**Inter 12px**) with a left-pointing arrow. Rail border `#F3F4F6`.
**Props (`SidebarNav`)**: `items [{key,icon,label}]`, `activeKey`, `onSelect(key)`, `logo`. **`NavItem`**: `icon`, `label`, `selected`, `onClick`, `showLabelOnHover`.

### Graphics (charts)
Inline-SVG data-viz primitives (Figma node `4112-2431`). In `Graphics.jsx`. **`AreaLineChart`** (audit 2026-07-07): a **multi-series** line chart with an explicit **$ y-axis** (`$0 / $10,000 / $30,000 / $40,000 / $50,000` — the frame skips `$20,000`) and a **year x-axis** (`2021–2025`), Inter `#9CA3AF` labels, faint `#E5E7EB` gridlines; each series is a 2px line with a **white + colored-ring marker at every point**; the primary series is lemon `#A8F200` with a faint area fill; a **4-item legend** below (Kyle Eddins / Profile 1 - Updated / Cody Eddins / Profile 3 → lemon/cyan/`#13BA74`/`#6C757D`). **`DonutChart`**: **5 segments** (lemon `#A8F200`, aquamarine `#61D9AF`, cyan `#00AFE2`, Atlantis `#95CB23`, **gray `#98A6AD`**) rendered **on white — no lavender track**; center is empty by default — the `#E7F6F1` chip with `#95CB23` amount is a **hover tooltip** (e.g. "Bambino Offline / $15,343"), not a static label.
**Props (`AreaLineChart`)**: `variant`, `data`, `width`, `height`, `showLegend`. **`DonutChart`**: `size`, `thickness`, `segments [{value,color}]`, `centerLabel {title,amount}`.

### OfferingCard
Browse/offering card with logo, location, live status, progress bar and dual CTAs (Figma node `4116-175`). In `OfferingCard.jsx`. 318×256, r8, `rgba(0,0,0,0.1)` border. Rows: logo / map-pin location / clock status (cyan) / progress bar (gradient on `#EDEFFE`) / two black r6 buttons with gradient-clipped text. Locked state overlays `rgba(51,51,51,.86)` with a lock badge and an Atlantis "Complete Self Accreditation" CTA (on hover). _(Audit 2026-07-06: the nearest bound Figma token reads `~rgba(51,51,51,0.8)` — base color matches, alpha differs; confirm on `card=inactive` node `4291:367` and settle on one value.)_ Composes the library `ProgressBar` via a `bar` prop (inline fallback for standalone).
**Props**: `logo`, `companyName`, `location`, `status`, `progress`, `bar`, `locked`, `onViewDetails`, `onInvest`, `onAccredit`.

### CardPreLogin
Pre-login offering card: brand logo, location, status, teaser copy, gradient progress bar and a gradient "Login" CTA, with optional locked/accreditation overlay (Figma node `4195-4748`). In `CardPreLogin.jsx`. 318px, white, `rgba(0,0,0,0.1)` border, r8. Progress 272×8 on `#EDEFFE`; Login button black r6 with gradient bg-clip text; locked overlay uses Atlantis `#95CB23` button.
**Props**: `logoSrc`, `logoAlt`, `location`, `status`, `teaser`, `progress`, `progressLabel`, `locked`, `loginLabel`, `accreditationLabel`, `onLogin`, `onAccredit`.

### VideoHero / VideoMedium
Video surfaces over an image with a dark gradient overlay and a gradient circular play button (Figma nodes `4130-3959`, `4738-112`). In `VideoHero.jsx` and `VideoMedium.jsx`. Hero: large `1360×452` (r0) / small `978×575` (r12), optional title (58px) + subtitle (20px) + play. Medium: `723×456` (r12), centered play, hides button when playing. Play button gradient circle (`#A8F200→#00AFE2`).
**Props (`VideoHero`)**: `imageSrc`, `size` (`large`\|`small`), `showText`, `showPlay`, `title`, `subtitle`, `onPlay`. **`VideoMedium`**: `imageSrc`, `play`, `width`, `height`, `onPlay`.

### ProfileMenu
Avatar trigger that opens a dropdown with two views — an account **menu** and a **profile list** (Figma nodes `4283-972`, `4308-512`). In `ProfileMenu.jsx`. Trigger: 36px cyan→lime gradient avatar (`linear-gradient(248deg, rgba(0,175,226,.64), rgba(168,242,0,.64))`) + name + role + chevron. Dropdown: 222px, white, r12, shadow. **Menu view** (audit 2026-07-07): an account **header** (name + email; chevron opens the profiles view), separator, **Manage Profiles**, **Account Settings**, separator, **Sign Out** (danger red `#C54949`). **Profiles view**: header (name + email + back chevron) then profile rows, the selected one with a **right-aligned cyan `#00AFE2` check**. Rows 40px, hover fill lemon `#A8F200`. Click-outside close; menu/menuitem roles.
**Props (`ProfileMenu`)**: `user {name,email,role,initials}`, `profiles`, `activeProfile`, `defaultOpen`, `onManageProfiles`, `onAccountSettings`, `onSignOut`, `onSelectProfile`. **`ProfileMenuItem`** (covers node 4308-512): `name`, `selected`, `onSelect`.

### Stepper
Horizontal multi-step progress indicator with status badges and connector dividers (Figma node `4455-756`). In `Stepper.jsx`. `StepStatus`: 35px circle — active/done lemon `#A8F200` with `rgba(163,230,53,.3)` ring, inactive `rgba(231,231,231,.6)`; done shows a check. Dividers `40×2`. Labels below (12/16): active `#000`, others `#5D5D5D`. `current` index drives states; `aria-current="step"`.
**Props (`Stepper`)**: `steps [{label}]`, `current`. **`StepStatus`**: `number`, `step` (`active`\|`inactive`\|`done`), `size`.

### InvestmentList / InvestmentCard
Full investment-management screen — search + profile filter + entries selector, status tabs with counts, and a stacked list of investment cards (Figma nodes `4558-1855` Incomplete, `4591-4542` Pending, `4558-2576` card states). In `InvestmentList.jsx`. Status tabs get a `#13BA74` underline + count pills (active `#95CB23`, else `#E5E7EB`); client-side search.

**`InvestmentCard` layout** (audit 2026-07-07): a wide card (white, `1px` border, radius `16px`, padding ~`24px 28px`) laid out as a left **avatar** + a right **main column**. The avatar is an `~88px` circle filled light lemon-green `#C4E76A` with dark initials (`#262626`, `~25px` Bold). The main column has two rows split by a hairline divider (`#E5E7EB`):
- **Top row** — left: a `Profile:` line (label Bold `#222`, value regular), the offering **title** (Clash Display Bold `24px`, `#111`), an `Account:` line, and a muted underlined **View agreements** link with a document icon (`#6B7280`). Right (right-aligned): the **amount** (Bold `~28px`, `#111`, tabular figures) with **Funded Balance:** beneath it (`14px`, muted).
- **Footer row** — left: `Date:` and `Status:` labels (Bold label + value), the status rendered as a rounded **pill** (Incomplete = amber `#FCEFC7` bg / `#9A6B12` text; Pending = cyan tint; etc.). Right: contextual **action buttons** — `Complete` (solid green `#A4C851`, dark label, check icon) / `Fund Now` (green, plus icon) and `Cancel` (outline **danger** — red border + red text + × icon); other states surface Review Requested / Pending Self Accreditation. Status badge and action set vary per `variant`.
**Props (`InvestmentList`)**: `initialTab`, `tabs [{key,label,count,disabled}]`, `items`, `profileLabel`. **`InvestmentCard`**: `name`, `account`, `profile`, `initials`, `date`, `status`, `amount`, `fundedBalance`, `variant`, `documentRequested`, `reviewRequested`, `selfAccreditation`, `onComplete`/`onCancel`/`onFundNow`/`onEdit`/`onReview`.

### PageHeader
Page-level header — H3 title, muted subtitle, optional "Go Back" link (Figma node `4653-613`). In `PageHeader.jsx`. Title 32/40 SemiBold `#000`; subtitle 14/18 `rgba(38,38,38,0.7)`. The **"Go Back" link sits BELOW the title/subtitle block** (audit 2026-07-07), `#222` 14px with a left-arrow — not above it.
**Props**: `title`, `subtitle`, `showGoBack`, `goBackLabel`, `onGoBack`.

### AccountCard
Selectable bank/account card — circular tinted icon, name + masked account line, default vs selected states (Figma node `4593-5243`). In `AccountCard.jsx`. `446×76`, r8, `2px` border; default `rgba(38,38,38,0.7)` on white; selected `#13BA74` on `#E7F6F1` with a trailing check-circle. 40px icon circle (`rgba(52,178,119,0.1)` bg, `#13BA74` **bank/columns glyph**). Name Clash Display SemiBold ~`13.7px` `#2b303b`; detail Regular `12px` `#6e7d91`, formatted `"<Type> •••• 4821"` (e.g. "Checking •••• 4821"). `aria-pressed`, keyboard-focusable.
**Props**: `name`, `detail`, `selected`, `disabled`, `onClick`, `fullWidth`.

### Switch
Toggle switch (Figma nodes `4594-6814` on, `4594-6812` off). In `Switch.jsx`. `44×24` pill track, `20px` knob; on track `#A4C851`, off `#E5E7EB`; `#FAFAFA` knob slides 0↔20. `role="switch"`, `aria-checked`.
**Props**: `checked`, `defaultChecked`, `onChange(bool)`, `disabled`, `label`, `id`.

### SegmentedChoice
Horizontal pill-segment single-select group; powers Yes/No and Score selectors (Figma nodes `4594-6468/6473`, `4594-6479/6512/6523/6490/6501`). In `SegmentedChoice.jsx`. `42px` segments, radius `20`, `8px` gap; selected `#95CB23` fill + `#A4C851` border, unselected white + `#E5E7EB`; text `#212529` `14/500`. `role="radiogroup"`.
**Props**: `options`, `value`, `defaultValue`, `onChange`, `name`, `gap`, `fill`, `ariaLabel`. Helpers: `YesNoChoice`, `ScoreChoice`.

### ActivityScale
0–10 scale slider with a large value readout (Figma nodes `4594-6715`…`4594-6625`). In `ActivityScale.jsx`. `8px` track (`rgba(115,115,115,0.3)`), **fill `#A4C851`** (muted olive-green, NOT Atlantis — audit 2026-07-07), **`20px` knob** (`#FAFAFA` with a 2px `#A4C851` ring); centered `24/700` value readout in Atlantis `#95CB23`; end labels + 0–10 ticks (`#737b8c`); pointer-drag + arrow/Home/End keys. `role="slider"`.
**Props**: `value`, `defaultValue`, `onChange(n)`, `min`, `max`, `lowLabel`, `highLabel`, `showTicks`, `ariaLabel`.

### SettingsMenuItem
Icon + label settings row with hover/active state (Figma nodes Account `4594-6783/6788`, Profile `4594-6794/6798`, Security `4594-6803/6807`). In `SettingsMenuItem.jsx`. `184px`, padding `12/16`, radius `16`, `12px` gap; default text `rgba(51,51,51,0.7)`; hover/active fill `rgba(130,203,21,0.9)` + text `#262626`; inline SVG icons. `role="menuitem"`.
**Props**: `label`, `icon` (`account`\|`profile`\|`security`\|node), `active`, `onClick`, `as`, `width`.

### SelectableCard
Collapsible multi-select option card — header + search + Select-All + chip row (Figma nodes `4597-8132/8133`, `4619-3031/3033`, `4622-3684/3686`, `4622-4182/4184`, `4623-5641/5643`, `4634-6399/6401`, `4665-861`/`4668-919`; all the same component). In `SelectableCard.jsx`. White card, `1px #E5E7EB`, radius `24`, soft shadow. **Header** (audit 2026-07-07): tinted-square icon + title (`16/600`) + a prompt subtitle (e.g. "Which business models are you interested in?") + `n/total` count pill + rotating chevron. **Body:** a row holding a `40px` search field (magnifier + "Search…") on the left and a **Select All / Deselect All** outline button on the right; below it a **wrapping row of pill chips** (`38px`, radius `12`, `1px #E5E7EB` border) — selected = `rgba(130,203,21,0.1)` fill + `#82CB15` border. Count reads `0/N` until options are chosen. Chips `role="checkbox"`.
**Props**: `title`, `subtitle`, `icon`, `options`, `selected`, `defaultSelected`, `onChange(arr)`, `defaultOpen`, `searchable`, `showSelectAll`, `showCount`, `minChipWidth`.

---

## 7. Audiences

**High Net Worth Individuals** — curated high-growth opportunities; institutionally vetted deals led by experienced founders; a community of impactful investors.

**Family Offices & VC Partners** — an outsourced VC arm; proven deal-flow pipeline with rigorous due diligence; access to the Southeast's fastest-growing tech market at attractive valuations; strategic co-investment.

**Startup Founders** — an experienced, dedicated long-term partner; access to network, expertise, and comprehensive due diligence.

---

## 8. Brand in Documents & Presentations

Guidelines for applying the Florida Funders brand to presentations (PowerPoint/Keynote/Slides), letterheads, and reports. All of these draw on the same tokens defined above — colors (§2), typography (§3), and logo rules (§4).

### Shared foundations
- **Typeface:** Clash Display throughout. Bold for titles and headings, SemiBold for subheads and callouts, Regular for body copy. Fall back to Inter or a system sans only when Clash Display is unavailable on the recipient's machine.
- **Color discipline:** white or very light backgrounds as the default canvas. Use Bluish Cyan `#00AFE2`, Lemon Green `#A8F200`, and Atlantis `#95CB23` as accents — not large fill areas. Reserve the green→cyan gradient (`#A8F200 → #00AFE2`) for a single hero moment per document (cover accent, divider, or one key stat), never as a page-wide background behind text. Body text is `#131927`; secondary text `#6D717F`.
- **Logo:** follow §4 — clear space, `100px` / `35mm` minimums, one of the four corners or centered on the vertical axis, never rotated, stretched, recolored, or outlined. On dark or photographic backgrounds use the reversed/white logo.
- **Accent shapes:** the gradient bar (rounded, e.g. `64×4px` scaled to context) is the signature divider — reuse it under titles to tie documents to the product UI.
- **Status colors** (`#13BA74` success, `#FF8E3C` warning, `#C54949` danger) are for data/labels only, never decorative.

### Presentations (PowerPoint / Keynote / Google Slides)
- **Format:** 16:9 widescreen. Keep a consistent master with left/top margins ≈ 5–7% of slide width.
- **Cover slide:** large Clash Display Bold title (~40–54pt), the FF logo, and a single gradient accent bar or corner mark. "Be bold, be proud, make it big" — the title and logo should dominate.
- **Section dividers:** short Clash Display SemiBold heading over white, with the gradient bar beneath it.
- **Content slides:** one idea per slide. Headings in Atlantis or ink; body in `#131927`. Use the component palette for any embedded UI (buttons, tags, progress bars) so decks match the product.
- **Charts:** use the data-viz palette — area/line charts in the brand gradient or single accent (cyan/green), donuts using the primary + neutral ramp. Gridlines `#E5E7EB`, axis/labels `#818898`. Avoid rainbow series; group by category with 2–3 colors max.
- **Footer:** slide number + "Florida Funders" wordmark or small mark, muted `#6D717F`, on every content slide.
- **Restraint:** no drop shadows, bevels, or clip-art. Flat, generous whitespace, high contrast.

### Letterheads
- **Header:** FF logo top-left (or centered) with full clear space; optional thin gradient rule or `1px #E5E7EB` divider beneath the header band.
- **Type:** recipient/date/body in Clash Display Regular `11–12pt`, `1.4–1.5` line spacing, `#131927`. Sender name/title in SemiBold.
- **Margins:** ~1" (25mm) all sides; keep the body within the logo's clear-space envelope.
- **Footer:** company legal name, address, website (`floridafunders.com`), and contact in `9–10pt` muted `#6D717F`, optionally separated by a hairline rule. Keep it single-line or two-line and unobtrusive.
- **Color:** monochrome body; a single Atlantis or gradient accent (header rule or a small corner mark) only. No colored text in the body.

### Reports
- **Cover:** report title in Clash Display Bold, subtitle/date in SemiBold, FF logo, and one gradient accent element. Optional full-bleed brand photo with the reversed logo.
- **Headings:** H1 Bold, H2 SemiBold, H3 SemiBold — mirror the type scale in §3 (H1 72 / H2 48 / H3 32, scaled down for print, e.g. 24 / 18 / 14pt). Accent headings in Atlantis where emphasis helps; keep most in ink.
- **Body:** Clash Display Regular `10–11pt`, `1.5` line spacing, `#131927`, ragged-right, generous margins. Prose in paragraphs — reserve bullet lists for genuine enumerations.
- **Tables:** header row `#F9FAFA` fill with `#333333` text; body rows white; hairline borders `rgba(209,209,209,0.4)`; numeric columns right-aligned. Highlight key figures in Atlantis or with a status color, sparingly.
- **Data & callouts:** stat callouts can use one gradient or Atlantis accent; charts follow the presentation chart rules above.
- **Page furniture:** running header (report title, muted) and footer (page number + "Florida Funders", muted `#6D717F`) with a `1px #E5E7EB` divider. Consistent page margins throughout.
- **Legal / disclosures:** set important-disclosure text in `#6C757D` at `9–10pt` (see the Disclosure component copy in §6 for the canonical language).
