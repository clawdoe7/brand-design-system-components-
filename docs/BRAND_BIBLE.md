# TBPN Brand Bible

This document is the master reference for building TBPN products exactly on-brand.

Use this when:

- creating a new dashboard or analytics product
- adapting the system to a new company or dataset
- prompting another coding agent
- reviewing whether a build matches the established direction

If there is a conflict between files:

1. this file wins
2. then [`DASHBOARD_ADDENDUM.md`](/Users/blakeperry/Documents/New%20Project/docs/DASHBOARD_ADDENDUM.md)
3. then [`TBPN_IMPLEMENTATION_RECIPES.md`](/Users/blakeperry/Documents/New%20Project/docs/TBPN_IMPLEMENTATION_RECIPES.md)
4. then [`brand-tokens.json`](/Users/blakeperry/Documents/New%20Project/docs/brand-tokens.json)
5. then [`BRAND_STANDARD.md`](/Users/blakeperry/Documents/New%20Project/docs/BRAND_STANDARD.md)

## 1. Canonical References

Live build reference:

- [`week-over-week-dashboard-working.html`](/Users/blakeperry/Documents/New%20Project/week-over-week-dashboard-working.html)
- [`tbpn-component-library.html`](/Users/blakeperry/Documents/New%20Project/tbpn-component-library.html)

Asset library:

- [`assets`](/Users/blakeperry/Documents/New%20Project/assets)

Key asset references:

- [`logo-lockup-hero.png`](/Users/blakeperry/Documents/New%20Project/assets/logo-lockup-hero.png)
- [`logo-world.png`](/Users/blakeperry/Documents/New%20Project/assets/logo-world.png)
- [`circlet.png`](/Users/blakeperry/Documents/New%20Project/assets/circlet.png)
- [`tbpn-logo-flat.png`](/Users/blakeperry/Documents/New%20Project/assets/tbpn-logo-flat.png)
- [`tbpn-logo-circle.png`](/Users/blakeperry/Documents/New%20Project/assets/tbpn-logo-circle.png)
- [`tbpn-showcase.png`](/Users/blakeperry/Documents/New%20Project/assets/tbpn-showcase.png)
- [`tbpn-hosts.png`](/Users/blakeperry/Documents/New%20Project/assets/tbpn-hosts.png)
- [`tbpn-starts-now.png`](/Users/blakeperry/Documents/New%20Project/assets/tbpn-starts-now.png)

### How To Use The HTML References

Use the working dashboard for:

- final dashboard page composition
- real product hierarchy
- state behavior inside a live dashboard

Use the component library for:

- clean reusable component patterns
- copyable HTML structures
- approved component states outside a page-specific dashboard layout
- top-level library navigation reference, where the six primary tabs use the stronger broadcast headline treatment while retaining the same green active state logic
- the default `Lifted Signal` top rail that now anchors the component-library shell
- the `Gradients & Textures` tab as a surface-chooser system rather than a loose inspiration board
- the bottom workspace-shell references in `Gradients & Textures`, which remain optional shell variants rather than the library default

## 2. Brand Definition

TBPN is a broadcast-tech visual system.

It should feel:

- sharp
- technical
- premium
- signal-rich
- fast
- credible

It should not feel:

- soft
- playful
- cozy
- rounded
- generic SaaS
- default dashboard software

## 3. Final Visual Thesis

TBPN is:

`black control room + scanline field + chrome typography + green signal light`

The dashboard system should feel like a polished command surface inside a larger media-tech environment.

## 4. The Four Big Rules

### Rule 1: Black First

Every screen starts from near-black or studio-black.

Do not design from white and theme it afterward.

### Rule 2: Green Means Signal

Green is used for:

- active state
- focus
- momentum
- current period
- positive motion
- key brand energy

Green is not for decorating every element.

### Rule 3: Chrome Means Structure

Chrome or chrome-adjacent text and borders are for:

- title rails
- company names
- chart titles
- important labels
- premium hierarchy

### Rule 4: Readability Beats Effect

When choosing between:

- more glow
- more blur
- more texture
- more readability

Always choose readability first.

## 5. Final Typography System

### Font Stack

- Display and engineered labels: `Michroma`
- Regular support and body text: `Universal Sans`
- Bold readable UI and value text: `Rajdhani`
- Broadcast headline voice: `Microgramma D Extended Bold`, fallback stack: `Microgramma`, `Eurostile Extended`, `Eurostile`, `Michroma`

### Role Map

- Header title: `Michroma`
- Toggle labels: `Michroma`
- Chip labels: `Rajdhani`
- KPI labels: `Michroma`
- KPI values: `Rajdhani`
- Support copy and explanatory text: `Universal Sans`
- Chart titles: `Michroma`
- Chart company names: `Rajdhani`
- Table headers: `Michroma`
- Table values: `Rajdhani`
- Giant promo slug: `Microgramma D Extended Bold`
- News-strip headline: `Microgramma D Extended Bold`
- Date/event masthead line: `Microgramma D Extended Bold`

### Typography Principles

- Use uppercase for structural labels and headings.
- Use Universal Sans for regular-weight explanatory copy, support text, and calmer body text.
- Use Rajdhani for anything that must read fast and carry more weight.
- Use Michroma for branding, titles, and system labels.
- Use the broadcast headline voice only when TBPN needs a giant editorial or promo moment that feels heavier than Michroma.
- Tighten letter spacing slightly before increasing glow.
- Never use glow as a substitute for contrast.
- Never use the broadcast headline voice for tabs, chips, KPI labels, dense dashboard UI, or paragraph text.
- If the exact licensed broadcast font is unavailable, preserve the role by using the documented fallback stack instead of inventing a new fourth voice.

### Dense Workflow Type Floor

For dense operational products, the small-type layer must stay readable before it stays “chrome.”

- Treat `Michroma` as the structural voice, not the default answer for every small control.
- `Michroma` below `10px` should be considered unsafe for dense workflow UI unless the label is extremely short and very high contrast.
- For toggles, chips, status pills, action buttons, and fast-read workflow controls, switch to `Rajdhani 10-12px bold` before shrinking `Michroma` too far.
- Use `Universal Sans 12-13px` as the minimum floor for support copy, helper notes, and quieter metadata that still needs to be read at working distance.
- If muted chrome text becomes hard to read, brighten the text or increase size before adding more glow, texture, or decorative weight.

### Workflow Typography Cutover

Use these cutovers:

- rail titles, short structural labels, and section headers: `Michroma`
- KPI values, counts, workflow buttons, compact pills, toggle text, and dense control copy: `Rajdhani`
- explanatory copy, help text, and support metadata: `Universal Sans`
- giant promo/editorial moments only: `Microgramma D Extended Bold`

### Font Availability Rule

- For local applications, local prototypes, native app shells, and any machine-rendered design workflow, the approved fonts must be installed on the machine.
- Do not assume GitHub or a local clone installs fonts automatically.
- Web-only implementations may use the documented fallback stacks when necessary, but local app work should not be approved until the actual installed fonts are available.

## 6. Final Color System

### Core Colors

- `TBPN Black`: `#020403`
- `Studio Black`: `#050808`
- `Panel Black`: `rgba(3,10,8,0.80)`
- `Neon Green`: `#18D39C`
- `Bright Glow Green`: `#6AFFD2`
- `Deep Green`: `#0D7859`
- `Chrome Light`: `#EAF0F7`
- `Chrome Mid`: `#98A9C8`
- `Chrome Dark`: `#485668`
- `Body White`: `#F3F6FB`
- `Muted Steel`: `#9FB1CA`
- `Negative Red`: `#C85A58`

### Final Dashboard Series Colors

- Current series: green scanline stack
- Previous series: darker steel scanline stack
- Positive delta: green pill
- Negative delta: restrained red pill
- Neutral: dark muted treatment

### Final Active Control Rule

For active green buttons:

- do not use white text
- use dark text
- use a denser green gradient
- use a bright edge so the active state reads instantly

## 7. Background And Atmosphere System

Treat `Gradients & Textures` as a chooser system.

Do not treat every texture family as equally valid everywhere.

### Default Surface Rule

`Base Scanline` is the universal safe default.

Start there unless the product context clearly asks for something else.

### Surface Choice Order

Choose surfaces in this order:

1. what kind of surface is this
2. how much readability and density does it need
3. only then how much lift, glow, or texture can it support

### Product Context Buckets

Use one of these buckets first:

- dashboard shell
- product panel
- modal / drawer
- quiet utility
- editorial / hero
- workspace shell

### Approved Family Logic

- `Base Scanline`: safest default for dense dashboards, product screens, docs shells, forms, and tables
- `Lifted Signal`: same family with more brand lift for product UI that still needs strong readability
- `Adaptive Scanline`: more art-directed hero/editorial surface where texture rhythm helps the composition
- `Heavy Horizontal`: stage-like broadcast surface for title cards, mastheads, and logo-forward moments
- `Soft Signal` / `Quiet Utility`: calmer, lighter, more open surfaces when scanlines would feel too technical
- `Dot Grid / Halftone`: secondary graphic field for spotlighted promo/editorial zones, not full dense data shells
- `Chrome / Grayscale`: material family for chrome title bars, giant title words, icon rails, and premium structural accents

### Readability / Density Filter

If the UI is dense, data-heavy, or operational:

- prefer `Base Scanline`
- use `Lifted Signal` only when you still need more brand atmosphere
- keep glow minimal or absent

If the UI is calm, open, or supportive:

- use `Soft Signal` or `Quiet Utility`
- keep the field smoother and less technical

If the UI is editorial, promo, or title-card driven:

- use `Adaptive Scanline`, `Heavy Horizontal`, `Dot Grid`, or `Chrome`
- choose the quietest family that still gives the right impact

### Glow Rule

Glow stays tiered and optional:

- no glow
- soft ambient glow
- focal glow

Use focal glow only for true hero or logo moments.

### Workspace Shell Rule

Headers, sidebars, and ClickUp-style shell references belong to the same surface system even when they look like navigation examples.

The five workspace-shell looks at the bottom of `Gradients & Textures` are approved reference variants.

The default component-library shell still uses the `Lifted Signal` top rail.

### Workflow Archetype Rule

For workflow-heavy products, choose the interface archetype before styling the details.

Approved archetypes:

- `Review Cockpit`: focused, progression-driven, low-clutter mode for vendor-by-vendor or item-by-item approval work
- `Analysis Table`: denser, filter-heavy, comparison-friendly mode for scanning, sorting, and cross-cutting review

Review Cockpit rules:

- make this the default entry mode for approval/review workflows unless the product explicitly says otherwise
- keep the KPI row tight and limited to the few metrics that move the operator forward
- keep progress visible
- hide dense analytical filters and dimensions unless they are truly needed in the moment
- keep the main toggle order focused-mode first and dense-mode second

Analysis Table rules:

- this is where dense filters, segmented controls, secondary dimensions, and full table analysis belong
- keep the typography cleaner and more readable than a spreadsheet, even when the information density increases
- do not let muted labels or tiny chrome text outrank scan-speed

## 8. Header Rail System

### Final Header Pattern

Default header:

- `PERFORMANCE OVERVIEW`

Default structure:

- title only

Optional structure:

- title + subtitle
- title + right-side label

Only add subtitle or right-side label if they add real orientation value.

### Final Header Behavior

- sticky
- integrated scanline background
- subtle green-black atmosphere
- neutral chrome title
- no heavy glow on the text itself

The component library now uses the `Lifted Signal` rail as its default top header shell.

The working dashboard baseline remains darker and more restrained by default. Use louder shell variants only when the product context calls for more lift than the week-over-week board needs.

## 9. Control System

### Top Mode Toggles

Final pattern:

- dark inactive button
- green active button
- dark text on active button
- slightly tighter letter spacing than the first draft
- stronger border and clearer active contrast

### Account Chips

Final pattern:

- one-color family only
- larger and bolder than default chips
- dark base
- green border
- green-tinted active state

Do not:

- assign each company its own color

## 10. KPI Card System

### Final KPI Behavior

KPI cards should feel:

- compact
- high-contrast
- aligned
- premium

Each card contains:

- label
- main number
- top-right delta pill
- bottom baseline line

### Final KPI Typography

- top label is chrome-muted, not dull gray
- big number is dominant and bright
- baseline line is small but legible
- delta badge is compact and readable

### Final KPI Layout

- less dead space than the early versions
- title area reserves enough room for wrapped labels
- baseline line is pinned toward the bottom

## 11. Account Card System

### Final Account Card Pattern

Each account card contains:

- company name
- top legend row: `WK1 / WK2 / CHG`
- metric label
- week one value
- week two value
- change pill

### Final Account Card Title Treatment

Use:

- soft chrome text
- tiny separation shadow
- faint green ambient glow in the card header area

Do not:

- turn the company name into neon glow text

### Final Account Card Layout Rule

- the company title is visually important, but not louder than the KPI values
- the legend belongs at the top, not the bottom

## 12. Chart Card System

### Chart Title Treatment

Chart card titles should use the same family as account-card titles:

- chrome-leaning
- slightly bright
- subtle shadow
- uppercase

### Chart Hierarchy Rules

For two-bar comparison charts:

- company names should sit close to the bar pair
- `WK1 / WK2` should be quieter than company names
- bar values must remain readable
- more spacing should exist between company groups than inside each company pair

For single-bar charts:

- chart can be more direct and simpler

### Final Comparison Bar Rule

Current period:

- green scanline fill
- dark text

Previous period:

- darker steel scanline fill
- dark text

Green must remain the hero.

Gray must support, not compete.

## 13. Table System

The full comparison table must feel like part of the same premium system.

Use:

- stronger metric-group header row
- cleaner second header row
- slightly roomier body rows
- brighter account names
- light vertical separators between metric groups
- subtle zebra rhythm

Do not:

- use a default spreadsheet look
- let all headers collapse into one visual layer

## 14. Glow Rules

Glow is allowed in:

- background atmosphere
- active green controls
- card header ambient areas
- select emphasis zones

Glow is not allowed as:

- a substitute for contrast
- a halo around every label
- a way to compensate for poor hierarchy

## 15. Animation System

### Animation Philosophy

Animations are selective, not decorative. They confirm state changes and add physical weight to key moments. The UI should feel still and fast by default, with animation reserved for boundaries: page load, tab switch, filter change, and direct interaction.

Do not animate everything. Do not loop anything. Do not use animation to compensate for poor hierarchy.

### Animation Timing

- Default speed: `200–350ms`
- Easing: `cubic-bezier(0.22, 0.68, 0.35, 1.0)` for all entrance and interaction animations
- No ambient or continuous animation — interaction-only
- Dramatic animations are reserved for major view changes only

### Animation Classes

| Class | Purpose | Speed | When To Use |
|---|---|---|---|
| `.tbpn-shadow-drop` | Page load entrance | 300ms | Cards and panels appearing on first load |
| `.tbpn-scale-fade` | Tab/panel switch | 250ms | Content swapping when switching tabs or filters |
| `.tbpn-flip-in` | Easter egg entrance | 350ms | Major view changes only — one per transition max |
| `.tbpn-pulse-activate` | Toggle active state | 200ms | Green flash when a toggle or tab activates |
| `.tbpn-hover-lift` | Hover feedback | 200ms | Interactive cards and buttons — 2px lift + shadow |
| `.tbpn-bar-grow-item` | Chart bar fill | 350ms | Bars growing from zero on appear or filter change |
| `.tbpn-chip-pop` | Chip selection | 200ms | Quick scale pop when a chip is selected |
| `.tbpn-stagger` | Cascading entrance | 250ms/item | Multiple items entering with 50ms stagger delay |
| `.tbpn-heartbeat` | Attention draw | 600ms | Critical KPI threshold or alert — never on loop |
| `.tbpn-shadow-press` | Click feedback | 200ms | Button press — inset shadow + 1px depress |

### Animation Rules

- Do not animate on every interaction — reserve for key moments
- Do not loop or repeat any animation continuously
- Do not combine `.tbpn-hover-lift` and `.tbpn-shadow-press` on the same element
- Do not use `.tbpn-flip-in` within a single dashboard view
- Do not use `.tbpn-heartbeat` on normal data display — only on threshold crossings
- Use `.tbpn-stagger` with `--i` CSS variable for cascading delays (50ms per item)
- Use `.tbpn-bar-grow-item` with `--bar-i` CSS variable for staggered bar fills (175ms per bar)
- Remove animation classes on `animationend` for classes that need to re-trigger (pulse, chip-pop, shadow-press)

### Animation Reference

For live demos, copyable code, and approved usage patterns, see the Animations tab in:

- [`tbpn-component-library.html`](/Users/blakeperry/Documents/New%20Project/tbpn-component-library.html)

## 16. What Changed From The Early Draft

(Section numbers shifted by one due to animation section insertion above.)

These are now final rules:

- the summary strip is removed by default
- the header is simplified
- active green buttons use dark text
- chips are slightly larger and bolder
- KPI labels are brighter and more legible
- KPI delta pills are more compact and intentional
- account-card titles use soft chrome plus ambient header glow
- chart comparison bars use the selected scanline stack
- table styling is upgraded beyond the earlier generic draft

## 16. What A New Agent Must Preserve

If a new coding agent builds another product in this system, it must preserve:

- the sticky integrated title rail
- the active green toggle treatment
- the unified chip system
- the KPI hierarchy
- the account-card title treatment
- the chart comparison bar treatment
- the premium grouped table treatment
- the black + chrome + green control-room atmosphere
- the animation system (selective, physical, shadow-driven, interaction-only)

It should also inspect:

- [`tbpn-component-library.html`](/Users/blakeperry/Documents/New%20Project/tbpn-component-library.html)

before inventing a new component shape or state treatment.

## 17. Build Rule

Do not invent a new TBPN style from scratch.

Start from:

- [`week-over-week-dashboard-working.html`](/Users/blakeperry/Documents/New%20Project/week-over-week-dashboard-working.html)
- [`tbpn-component-library.html`](/Users/blakeperry/Documents/New%20Project/tbpn-component-library.html)
- [`assets`](/Users/blakeperry/Documents/New%20Project/assets)
- [`brand-tokens.json`](/Users/blakeperry/Documents/New%20Project/docs/brand-tokens.json)

Then extend carefully.
