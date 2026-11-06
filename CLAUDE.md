# CLAUDE.md – Shoot (customer app design)

## Before any design work
1. **Always read `brief.md` first, then `references/notes.md`.** Do this at the start of every design task, even small ones.
2. Follow their rules and priorities. They are the source of truth.
3. Also read `design-brief-final.md` (approved 2026-11-06) – it records decisions made after the brief.
4. `PRODUCT.md` holds the durable product record (users, positioning, constraints, platform: adaptive) used by the Impeccable skill.

## Priority when sources disagree
1. Wireframes (`wireframes/`) – structure, content, flow
2. `brief.md` – rules, personas, colors, fonts
3. `references/apps/` – feel: simplicity, spacing, button placement
4. `references/inspirations/` – visual style, illustrations only

## Working rules (summary – the brief is authoritative)
- Don't invent features or content. Ask instead.
- Ask one question at a time and wait for the answer.
- Build one screen at a time, in the order from brief section 8, and wait for feedback after each.
- Open the matching wireframe before designing a screen and follow its structure.
- Colors come only from `color_palettes/color_palette_1.png` (unless the user asks to compare).
- Fonts: Shrikhand (logo + short large headlines only), Inter 400/500/600/700 for all UI.
- No generic AI design: no purple gradients, template cards, emoji icons or default fonts.
- Save mockups as HTML in `screens/`.

## Design tokens (hard rule)
- `design-system/tokens.css` is the single source of every design value: colours, fonts, font sizes/weights/line-heights, spacing, sizes, radius, borders, shadows, motion.
- Every screen in `screens/` loads, in this order: the Google Fonts link, `../design-system/tokens.css`, `../design-system/components.css`, `../design-system/icons.js`. Its own CSS uses **only** `var(--…)` from tokens.css.
- Components (buttons, cards, inputs, chips, banners, sheets, nav, tab bar, illustration placeholders) come from `components.css`. Screens add layout only and never restyle a component locally; a new component or variant goes into `components.css` first and onto the design-system page (`design-system/index.html`).
- Icons come only from `icons.js` (`<svg class="i"><use href="#i-name"/></svg>`). New icons are added there, from the same Lucide set.
- Never hardcode hex/rgb colours, px/em sizes, font names, radii, shadows or durations in screens: not in CSS, not in inline `style=""`.
- Allowed without a token: `0`, percentages, `1fr`/`auto`, aspect ratios, SVG drawing coordinates, and the `@media (min-width: 720px)` breakpoint (CSS can't use variables in media queries; the value is documented as `--bp-wide`).
- Need a value that doesn't exist? Add it to `tokens.css` first (semantic name, comment), then use it. Don't invent one-off values.
- Prefer semantic tokens (`--primary`, `--ink`, `--surface`) over raw palette tokens (`--rust`, `--brown`).

## Communication
- Talk to the user in Slovak.
- Write all files (docs, code, mockup copy) in English.

## Actual folder names (differ from the brief)
- Palettes: `color_palettes/` (brief says `colorpallets/`)
- Inspiration: `references/inspirations/` (brief says `references/inspiration/`)
- Wireframe files use names like `1.6-Caf-list-Home.png`, `E4-QR-can-t-be-read.png` (the "é" and apostrophes were dropped on export)
- `assets/fonts/` does not exist yet
