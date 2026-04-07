# TBPN Agent Brief

Use this file when a coding agent needs the shortest possible path to building a new product in the exact TBPN dashboard system established in this project.

## Source Of Truth

Read these in this order:

1. [`BRAND_BIBLE.md`](/Users/blakeperry/Documents/New%20Project/docs/BRAND_BIBLE.md)
2. [`DASHBOARD_ADDENDUM.md`](/Users/blakeperry/Documents/New%20Project/docs/DASHBOARD_ADDENDUM.md)
3. [`TBPN_IMPLEMENTATION_RECIPES.md`](/Users/blakeperry/Documents/New%20Project/docs/TBPN_IMPLEMENTATION_RECIPES.md)
4. [`brand-tokens.json`](/Users/blakeperry/Documents/New%20Project/docs/brand-tokens.json)
5. [`BRAND_STANDARD.md`](/Users/blakeperry/Documents/New%20Project/docs/BRAND_STANDARD.md)

Reference implementation:

- [`week-over-week-dashboard-working.html`](/Users/blakeperry/Documents/New%20Project/week-over-week-dashboard-working.html)
- [`tbpn-component-library.html`](/Users/blakeperry/Documents/New%20Project/tbpn-component-library.html)

Reference assets:

- [`assets`](/Users/blakeperry/Documents/New%20Project/assets)

## Font Install Rule

For any local application, local prototype, native wrapper, or local design/export environment, install the approved fonts on the machine before evaluating the UI.

GitHub and a cloned repo do not install fonts automatically.

Use the documented fallback stacks only when the context is genuinely web-only. If the task is local app work, verify that `Michroma`, `Universal Sans`, `Rajdhani`, and `Microgramma D Extended Bold` are installed first.

## What To Build

Build TBPN interfaces so they feel like:

- a premium control room
- a broadcast-tech operating surface
- a high-contrast analytics product
- an on-brand dashboard template, not a one-off page

When you need reusable approved component markup, copy from:

- [`tbpn-component-library.html`](/Users/blakeperry/Documents/New%20Project/tbpn-component-library.html)

Inside that file, preserve the stronger top-level tab rail for:

- `Core Library`
- `Spec Imports`
- `Fonts`
- `Gradients & Textures`
- `Logo`
- `Animations`

Treat the component library header itself as the default `Lifted Signal` shell.

Inside `Gradients & Textures`, use the section as a surface chooser:

- start from `Base Scanline` when you need the safest product shell
- step up to other approved families only when product context requires more lift
- use readability and density as the second filter after context
- treat the bottom `ClickUp Header / Side Menu Looks` section as reusable workspace-shell references, not as the default library shell

## Non-Negotiables

- Start from near-black, never white.
- Choose the workflow archetype first when the screen is operational: `Review Cockpit` or `Analysis Table`.
- Use green as the primary signal color.
- Use chrome or chrome-adjacent text treatment for major labels and titles.
- Use four font roles only: `Michroma`, `Universal Sans`, `Rajdhani`, and the broadcast headline stack headed by `Microgramma D Extended Bold`.
- If a compact control becomes too small or weak in `Michroma`, switch that layer to `Rajdhani` instead of leaving it fragile.
- Use scanline and atmosphere layers behind the UI, not pasted on top of it.
- Keep panels hard-edged, aligned, and grid-driven.
- Keep active states unmistakable.
- Keep account chips one-color, never rainbow-coded.
- Keep chart current-series brighter than comparison-series.
- Keep the comparison table polished, grouped, and deliberate.
- Default header is a single title only: no subtitle and no right label unless required.
- The component library top rail now defaults to the `Lifted Signal` shell, while actual dashboard product rails should remain more restrained unless the product context calls for more brand lift.

## Default Header Pattern

Use:

- `PERFORMANCE OVERVIEW`

Do not add subtitle or right-side label unless the product truly needs them.

## Final Dashboard Decisions To Preserve

- Sticky integrated-scanline top rail
- Keep `Michroma` as the normal dashboard chrome voice; do not replace the main rail title with the broadcast headline font
- Keep regular non-bold support copy on `Universal Sans`
- Keep bold readable values and stronger UI text on `Rajdhani`
- Dark active toggle text on green gradient buttons
- Unified account chips with slightly larger, bolder text
- KPI cards with compact title/value rhythm and top-right delta pills
- Account cards with chrome-glow company names and top-aligned `WK1 / WK2 / CHG`
- Comparison charts with:
  - slightly darker steel previous bars
  - green scanline current bars
  - dark text inside both fills
  - quieter `WK1 / WK2`
  - more space between company groups than inside each pair
- Full-width comparison table with grouped headers and subtle separators
- Reserve the broadcast headline font for giant promo/news/date slugs, masthead callouts, and editorial cards only

## Animation Rules

- Use `.tbpn-shadow-drop` on page load entrance (300ms)
- Use `.tbpn-scale-fade` on tab/panel switches (250ms)
- Use `.tbpn-pulse-activate` on toggle activation (200ms)
- Use `.tbpn-hover-lift` on interactive cards and buttons (200ms)
- Use `.tbpn-bar-grow-item` with `--bar-i` for chart bar fill (350ms, 175ms stagger)
- Use `.tbpn-chip-pop` on chip selection (200ms)
- Use `.tbpn-shadow-press` on button click feedback (200ms)
- Use `.tbpn-heartbeat` only for critical KPI alerts (600ms, never loop)
- Use `.tbpn-flip-in` only for major view changes (350ms, one per transition max)
- Use `.tbpn-stagger` with `--i` for cascading entrances (50ms delay per item)
- Do not animate every element — selective and physical, not decorative
- Do not loop or repeat any animation
- Default easing: `cubic-bezier(0.22, 0.68, 0.35, 1.0)`

See the Animations tab in the component library for live demos and copyable code.

## Default Build Order

1. Add background layers.
2. Choose the workflow archetype: `Review Cockpit` or `Analysis Table`.
3. Build sticky title rail.
4. Build top toggles.
5. Build account chips.
6. Build KPI cards.
7. Build charts.
8. Build account detail cards.
9. Build table.
10. Add selective animations to key moments.
11. Tune readability before adding more effects.

When choosing a surface family:

1. dense dashboard or product screen: `Base Scanline`
2. product UI that needs more lift: `Lifted Signal`
3. hero/editorial/title-card moment: `Adaptive Scanline`, `Heavy Horizontal`, `Dot Grid`, or `Chrome`
4. calm/open/supportive moment: `Soft Signal` or `Quiet Utility`
5. workspace header/sidebar shell: one of the five workspace-shell variants at the bottom of `Gradients & Textures`

When choosing a workflow pattern:

1. focused review queue or cockpit
2. denser analysis table
3. how much filter clutter belongs in the default mode
4. whether compact controls should cut over from `Michroma` to `Rajdhani`

If you are building from reusable parts rather than from full-page dashboard composition, use the component library before inventing new component structure.

## Do Not Do

- no generic SaaS card grids
- no soft rounded pastel UI
- no rainbow categories
- no white text on bright green active buttons
- no blurred/glowing text halos
- no giant verbose headers
- no default vendor chart styling

## Prompt Snippet

```text
Build this product in the exact TBPN dashboard system defined in /docs/BRAND_BIBLE.md, /docs/DASHBOARD_ADDENDUM.md, /docs/TBPN_IMPLEMENTATION_RECIPES.md, and /docs/brand-tokens.json. Use /week-over-week-dashboard-working.html as the implementation benchmark, /tbpn-component-library.html as the reusable component reference, and /assets as the visual resource library. If the screen is workflow-heavy, decide first whether it is a focused Review Cockpit or a denser Analysis Table. Preserve the established header rail, active toggle treatment, chip system, KPI hierarchy, account-card title treatment, comparison bar treatment, grouped table styling, and surface-family logic. Use Rajdhani for dense compact controls when Michroma would become too small or fragile. Use only the approved animation classes from the Animations tab in /tbpn-component-library.html. After building, run the self-check in /docs/VALIDATION_CHECKLIST.md. Do not reinterpret the brand from scratch and do not drift into generic SaaS or vendor-default dashboard styling.
```

For clean reusable component markup and approved examples, also inspect:

- [`tbpn-component-library.html`](/Users/blakeperry/Documents/New%20Project/tbpn-component-library.html)
