# TBPN Brand Standard

This is the short version of the TBPN system.

Use it when you need a fast orientation before reading the full implementation docs.

Primary references:

- [`BRAND_BIBLE.md`](/Users/blakeperry/Documents/New%20Project/docs/BRAND_BIBLE.md)
- [`DASHBOARD_ADDENDUM.md`](/Users/blakeperry/Documents/New%20Project/docs/DASHBOARD_ADDENDUM.md)
- [`TBPN_IMPLEMENTATION_RECIPES.md`](/Users/blakeperry/Documents/New%20Project/docs/TBPN_IMPLEMENTATION_RECIPES.md)
- [`brand-tokens.json`](/Users/blakeperry/Documents/New%20Project/docs/brand-tokens.json)
- [`week-over-week-dashboard-working.html`](/Users/blakeperry/Documents/New%20Project/week-over-week-dashboard-working.html)
- [`tbpn-component-library.html`](/Users/blakeperry/Documents/New%20Project/tbpn-component-library.html)

## Core Thesis

TBPN should feel like:

- black studio environment
- chrome typography
- green signal energy
- premium broadcast-tech dashboard

It should not feel like:

- a default BI tool
- a startup admin panel
- a colorful spreadsheet
- a generic dark dashboard theme

## Final Visual Equation

Use:

- near-black base
- low-opacity scanline texture
- green atmosphere wash
- chrome labels and titles
- sharp borders and separators
- one bright active state at a time

Treat this as `default + approved variants`, not one mandatory background recipe.

## Font Roles

- `Michroma`: chrome/system voice for rails, titles, tabs, and labels
- `Universal Sans`: regular non-bold support/body voice
- `Rajdhani`: stronger readable voice for bold values, denser UI, and text that must hit harder
- `Microgramma D Extended Bold` fallback stack: broadcast headline voice for giant promo/news/date moments only

Font installation rule:

- local applications and local design environments must have the approved fonts installed on the machine
- GitHub does not install fonts for the agent
- fallback stacks are acceptable for web-only work, not as the final answer for local app builds

Dense workflow type floors:

- `Michroma` is for short structural labels, not tiny dense control copy
- treat `10-11px` as the floor for short high-contrast `Michroma` labels
- use `Rajdhani 10-12px bold` for toggles, chips, status pills, compact buttons, and dense workflow controls
- use `Universal Sans 12-13px` for support copy and quieter metadata that still needs to be readable
- if muted steel text becomes hard to read, brighten it or enlarge it before adding more effect

## Header Standard

Default header:

- `PERFORMANCE OVERVIEW`

Rules:

- sticky rail
- integrated scanline background
- neutral chrome title
- no subtitle by default
- no right-side label by default

The component library itself now uses the `Lifted Signal` rail as the default top header shell.

The six component-library tabs are: `Core Library`, `Spec Imports`, `Fonts`, `Gradients & Textures`, `Logo`, `Animations`.

Those tabs keep the stronger broadcast treatment, but the bottom workspace-shell references in `Gradients & Textures` are optional variants, not the default shell.

## Surface Standard

Use `Gradients & Textures` as a chooser system.

Choose surfaces in this order:

1. product context
2. readability / density
3. then lift, glow, and texture intensity

Safe default:

- `Base Scanline`

Approved context variants:

- `Lifted Signal` for product UI that needs more brand lift
- `Adaptive Scanline`, `Heavy Horizontal`, `Dot Grid`, or `Chrome` for editorial, promo, and title-card moments
- `Soft Signal` or `Quiet Utility` for calmer, lighter, more supportive surfaces
- one of the five workspace-shell references at the bottom of `Gradients & Textures` for ClickUp-style headers or sidebars

Do not treat every family as equally valid everywhere.

## Workflow Archetype Standard

Choose one of these first for workflow-heavy screens:

- `Review Cockpit`: focused review, approval, and progression mode
- `Analysis Table`: denser analysis, filtering, and comparison mode

Review Cockpit rules:

- default this mode first for approval/review products
- show the smallest KPI set that still moves the operator forward
- keep progress visible
- hide month/tier/status/filter clutter unless it is essential to the review step
- keep the left-most main toggle on the focused mode and the denser mode to the right

Analysis Table rules:

- allow denser filters and segmented controls here
- keep the table headers, pills, and buttons readable before they are “stylized”
- do not let the denser mode inherit the visual weakness of spreadsheet-gray UI

## Control Standard

Top toggles:

- dark inactive state
- green active state
- dark text on active green
- active state must pop more than inactive state
- use `Rajdhani 10-12px bold` when the toggle copy is dense, repeated, or too small for clean `Michroma`

Account chips:

- one-color family only
- slightly larger and bolder than default UI chips
- green border
- green-tinted active fill
- use `Rajdhani` for chip text and dense filter controls before shrinking `Michroma` too far

Action buttons and status pills:

- keep them readable first, premium second
- prefer `Rajdhani` for compact workflow actions and small state pills
- do not ship tiny gray `Michroma` buttons that require squinting

## KPI Standard

KPI cards must include:

- muted small uppercase label
- dominant white number
- small top-right delta pill
- small baseline line at bottom

KPI cards should feel:

- tight
- scan-friendly
- aligned
- high-contrast

For review-heavy screens:

- use a smaller KPI set than a broad analysis surface
- keep the KPI row focused on progress, completion, reviewed dollars, or the few metrics that change operator behavior
- do not carry analytical clutter into the review cockpit just because it fits

## Account Card Standard

Account cards must include:

- chrome-glow company title
- `WK1 / WK2 / CHG` legend aligned at top
- brighter values than labels
- green and red change pills

## Chart Standard

Use:

- darker steel comparison bar
- green scanline current bar
- dark text inside both bars
- quiet `WK1 / WK2`
- more space between company groups than inside each pair

Do not:

- make every label equally loud
- over-enlarge helper labels
- let the gray comparison bar compete with green

## Table Standard

Tables must feel:

- dense
- grouped
- premium
- easy to scan

Use:

- grouped top headers
- clean subheaders
- subtle zebra rhythm
- brighter account names
- light vertical separators between metric groups
- enough text size and contrast that the table still reads fast at working distance

## Animation Standard

Animations are selective and physical — not decorative.

Use:

- `.tbpn-shadow-drop` for page load entrance (300ms)
- `.tbpn-scale-fade` for tab/panel switches (250ms)
- `.tbpn-flip-in` for major view changes only (350ms)
- `.tbpn-pulse-activate` for toggle activation (200ms)
- `.tbpn-hover-lift` for interactive card/button hover (200ms)
- `.tbpn-bar-grow-item` for chart bar fill with `--bar-i` stagger (350ms, 175ms gap)
- `.tbpn-chip-pop` for chip selection (200ms)
- `.tbpn-stagger` with `--i` for cascading entrances (50ms delay per item)
- `.tbpn-heartbeat` for critical KPI alerts only (600ms, never loop)
- `.tbpn-shadow-press` for button click feedback (200ms)

Do not:

- animate every element
- loop or repeat any animation
- use dramatic entrance within a single view
- use heartbeat on normal data display
- combine hover-lift and shadow-press on the same element

Default easing: `cubic-bezier(0.22, 0.68, 0.35, 1.0)`

## Asset And Example References

Use:

- [`assets`](/Users/blakeperry/Documents/New%20Project/assets)
- [`week-over-week-dashboard-working.html`](/Users/blakeperry/Documents/New%20Project/week-over-week-dashboard-working.html)

Treat the working dashboard file as the most faithful visual example of the final system.

Treat the component library file as the fastest reusable component reference.

The six top-level component-library tabs use the broadcast headline voice for stronger section switching, while still keeping the same dark-inactive / green-active control logic.

`Gradients & Textures` is the place where an agent should choose the correct surface family. The five ClickUp-style workspace shells at the bottom of that tab are intentionally stored there as surface references because they are shell/mood decisions, not ordinary component patterns.
