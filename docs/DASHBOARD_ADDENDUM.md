# TBPN Dashboard Addendum

This file converts the TBPN brand into an exact dashboard specification.

It is written from the final dashboard implementation in:

- [`week-over-week-dashboard-working.html`](/Users/blakeperry/Documents/New%20Project/week-over-week-dashboard-working.html)
- [`tbpn-component-library.html`](/Users/blakeperry/Documents/New%20Project/tbpn-component-library.html)

Use these references differently:

- the working dashboard controls dashboard-level composition
- the component library controls reusable approved component markup

Use this when another coding agent needs to build:

- a new analytics page
- a scorecard
- a reporting dashboard
- an operations surface
- a week-over-week board

Important context:

- the week-over-week dashboard still defaults to the darker core shell logic
- the component library's other texture families are approved extensions, not replacements for that baseline
- the component library now uses the `Lifted Signal` rail as its default top header shell, but dashboard product rails should remain structurally conservative unless the product truly needs more lift

## Workflow-heavy products

If the product is not a general analytics dashboard, do not force it into the exact same composition.

For review-heavy tools such as closes, approvals, reconciliations, or transaction classification:

- choose the workflow archetype first:
  - `Review Cockpit`
  - `Analysis Table`
- use the component library's `Workflow Modes` section as the reusable pattern reference
- keep the review cockpit lighter, more decisive, and more progression-driven than a normal dashboard
- let the denser table mode hold the extra filters, breakout dimensions, and audit density
- switch compact controls, pills, and dense table chrome to `Rajdhani` before shrinking `Michroma` below readability

## 1. Final Dashboard Order

Use this default order:

1. sticky title rail
2. top mode toggles
3. company / account chips
4. KPI cards
5. account comparison cards
6. chart cards
7. comparison table

Do not add a narrative summary strip by default.

## 2. Page Frame

### Spacing

- page outer padding desktop: `20px`
- tablet: `16px`
- mobile: `12px`
- major section gap: `20px`
- subsection gap: `12px`
- card gap: `8px`

### Page Width

- content frame max width: `1320px`

## 3. Header Rail Spec

### Content

Default title:

- `PERFORMANCE OVERVIEW`

Default structure:

- title only

### Behavior

- sticky at top
- integrated scanline texture
- subtle green atmosphere
- neutral chrome title
- no subtitle by default
- no right label by default

### Final Header Typography

- font: `Michroma`
- size: `16px`
- letter spacing: `0.1em`
- chrome-neutral gradient, not green accent text
- do not use the broadcast headline font in the sticky rail; the header should stay structural, not editorial

## 4. Top Toggle Spec

### Container

- dark metallic panel
- `34px` tab height
- `14px` horizontal tab padding

### Inactive State

- dark background
- chrome-muted text
- engineered uppercase

### Active State

- denser green gradient
- dark text
- brighter edge
- stronger weight

### Rule

The selected state must be obvious without relying on glow alone.

## 5. Company Chip Spec

### Final Chip Settings

- height: `28px`
- horizontal padding: `12px`
- font: `Rajdhani`
- size: `11px`
- weight: `700`
- letter spacing: `0.035em`

### Visual Style

- dark base
- green border
- active: green-tinted fill with brighter edge

### Rule

All companies use the same chip system.

No per-company color coding.

## 6. KPI Card Spec

### Final Layout

- top row cards are slightly larger
- title area reserves room for wrapped labels
- big number dominates
- baseline line sits lower and reads clearly
- delta badge sits in the title corner but feels anchored

### Final KPI Metrics

- card padding: `12px 12px 11px`
- base min height: `82px`
- first row min height: `96px`
- label size: `12px`
- label color: lighter chrome-muted, not muddy gray
- label letter spacing: `0.035em`
- main value size: `clamp(2.15rem, 3.15vw, 2.8rem)`
- baseline size: `11px`
- delta badge size: `12px`

### Delta Badge Rules

- compact pill
- red and green states are restrained, not loud
- badge should feel integrated into the title area, not floating

## 7. Account Card Spec

### Final Layout

- company title
- top legend row
- metric rows

### Final Typography

- company title font: `Michroma`
- size: `14px`
- soft chrome text with subtle shadow
- ambient green glow belongs to the header strip behind the title, not the letters
- the broadcast headline font is reserved for promo/editorial modules, not account cards

### Legend

- top-aligned
- size: `9px`
- chrome-muted

### Row Typography

- row labels: `13px`
- values: `13px`
- `WK1` values: chrome-muted
- `WK2` values: bright
- change pills: `11px`

## 8. Chart Card Spec

### Chart Card Title

- font: `Michroma`
- size: `14px`
- chrome-glow treatment matching card titles
- if a future dashboard introduces a major editorial promo block, switch that block to the broadcast headline stack instead of oversizing these chart titles

### Chart Company Labels

- size: `13px`
- bright chrome-white
- slightly tighter tracking than early drafts

### `WK1 / WK2`

- size: `8px`
- quieter than company labels
- slightly muted chrome

### Bar Value Labels

- size: `11px`
- dark text inside both gray and green bars

## 9. Two-Bar Comparison Chart Rule

For each company block:

- company name sits close to the bar pair
- internal spacing between `WK1` and `WK2` rows is tight
- spacing between one company block and the next is larger

This rule is critical.

It is the reason the two-bar charts read cleanly instead of looking like repeated helper text.

## 10. Final Series Treatment

### Previous Series

- darker steel scanline bar
- darker than early versions
- readable, but clearly secondary

### Current Series

- green scanline bar
- brighter than previous
- clearly dominant

### Rule

The gray bar should never visually compete with the green bar.

## 11. Table Spec

### Final Hierarchy

- chart-card title treatment above the table
- first header row for metric groups
- second header row for `WK1 / WK2 / CHG`
- body rows with enough room to scan

### Final Table Typography

- base table font size: `13px`
- top metric-group row: `10px`
- second header row: `9px`
- account names: brighter and more premium than the data cells

### Final Table Behavior

- subtle zebra rhythm
- subtle hover
- light separators between grouped metrics

## 12. Animation Spec

### When To Animate

- page load: all cards enter together with `.tbpn-shadow-drop` (300ms)
- tab/panel switch: new panel content uses `.tbpn-scale-fade` (250ms)
- toggle activation: active button gets `.tbpn-pulse-activate` (200ms)
- chart bars: fill from zero with `.tbpn-bar-grow-item` (350ms, staggered 175ms per bar via `--bar-i`)
- chip selection: `.tbpn-chip-pop` (200ms)
- hover on interactive cards/buttons: `.tbpn-hover-lift` (200ms, 2px lift + shadow)
- button click feedback: `.tbpn-shadow-press` (200ms, inset shadow)
- critical KPI alert: `.tbpn-heartbeat` (600ms, use once, never loop)
- major view change: `.tbpn-flip-in` (350ms, one per transition maximum)
- cascading entrance: `.tbpn-stagger` with `--i` variable (250ms/item, 50ms stagger)

### When NOT To Animate

- do not animate every element on every page
- do not loop or repeat any animation
- do not use animation to fix poor contrast or hierarchy
- do not use dramatic entrance within a single view
- do not use heartbeat on normal data — only threshold crossings
- do not combine hover-lift and shadow-press on the same element

### Default Easing

`cubic-bezier(0.22, 0.68, 0.35, 1.0)` for all animations.

### Reference

See the Animations tab in [`tbpn-component-library.html`](/Users/blakeperry/Documents/New%20Project/tbpn-component-library.html) for live demos and copyable code.

## 13. Readability Rules

When something feels off, use this order:

1. improve contrast
2. improve spacing hierarchy
3. improve font size
4. only then add texture or glow

Do not:

- solve readability with blur
- overuse glow on text
- increase every font at once

## 13. What Another Agent Should Copy Exactly

Another coding agent should copy exactly:

- sticky integrated header rail
- dark-text active toggles
- larger unified account chips
- compact KPI cards with anchored delta pills
- account-card title treatment
- chart-card title treatment
- current vs previous bar hierarchy
- grouped comparison table styling
- selective animation system with approved utility classes

## 15. Final Reminder

If the new product is another dashboard, the starting point should not be a blank design.

The starting point should be:

- the structure
- hierarchy
- typography
- state behavior
- and component treatments

already established in the current reference dashboard.

If you need the cleanest reusable component examples, use:

- [`tbpn-component-library.html`](/Users/blakeperry/Documents/New%20Project/tbpn-component-library.html)
