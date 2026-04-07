# START HERE FOR AGENTS

This is the fastest onboarding file for any new coding agent working in this project.

Use this file first.

Its job is simple:

- tell you what the source of truth is
- tell you what the final UI system is
- tell you what not to break
- tell you how to start building new products in the same brand

## Mission

Build new products in the exact TBPN dashboard system already established in this project.

Do not redesign it from scratch.

Do not “make it look better” by drifting into generic SaaS, default dark dashboards, or vendor chart styling.

You are extending an existing visual system, not inventing a new one.

## Read In This Order

1. [`BRAND_BIBLE.md`](/Users/blakeperry/Documents/New%20Project/docs/BRAND_BIBLE.md)
2. [`DASHBOARD_ADDENDUM.md`](/Users/blakeperry/Documents/New%20Project/docs/DASHBOARD_ADDENDUM.md)
3. [`TBPN_IMPLEMENTATION_RECIPES.md`](/Users/blakeperry/Documents/New%20Project/docs/TBPN_IMPLEMENTATION_RECIPES.md)
4. [`brand-tokens.json`](/Users/blakeperry/Documents/New%20Project/docs/brand-tokens.json)
5. [`BRAND_STANDARD.md`](/Users/blakeperry/Documents/New%20Project/docs/BRAND_STANDARD.md)
6. [`AGENT_BRIEF.md`](/Users/blakeperry/Documents/New%20Project/docs/AGENT_BRIEF.md)

## Canonical Visual Reference

Treat this file as the implementation benchmark:

- [`week-over-week-dashboard-working.html`](/Users/blakeperry/Documents/New%20Project/week-over-week-dashboard-working.html)
- [`tbpn-component-library.html`](/Users/blakeperry/Documents/New%20Project/tbpn-component-library.html)

If a written doc and the final dashboard implementation disagree visually, first assume the implementation reflects the latest decision, then verify against the brand bible.

Use the working dashboard for:

- product-level layout
- real dashboard hierarchy
- final state behavior

Use the component library for:

- clean reusable component examples
- copyable HTML patterns
- approved component states without dashboard-specific clutter
- the canonical six-tab library shell: `Core Library`, `Spec Imports`, `Fonts`, `Gradients & Textures`, `Logo`, `Animations`
- the default `Lifted Signal` top header rail that now anchors the component library shell
- surface-family selection inside `Gradients & Textures`, where backgrounds are chosen by product context first and readability/density second
- the bottom `ClickUp Header / Side Menu Looks` section in `Gradients & Textures`, which is a reference-only workspace shell library rather than the default app shell

## Asset Library

Use these assets and this directory as the reference library:

- [`assets`](/Users/blakeperry/Documents/New%20Project/assets)
- [`tbpn-showcase.png`](/Users/blakeperry/Documents/New%20Project/assets/tbpn-showcase.png)
- [`tbpn-hosts.png`](/Users/blakeperry/Documents/New%20Project/assets/tbpn-hosts.png)
- [`tbpn-logo-flat.png`](/Users/blakeperry/Documents/New%20Project/assets/tbpn-logo-flat.png)
- [`tbpn-logo-circle.png`](/Users/blakeperry/Documents/New%20Project/assets/tbpn-logo-circle.png)
- [`logo-world.png`](/Users/blakeperry/Documents/New%20Project/assets/logo-world.png)

## Font Installation Requirement

For local applications, local prototypes, native apps, Figma-adjacent exports, or any build that depends on system-installed fonts, you must install the approved fonts on the machine first.

Do not assume GitHub or a cloned repo installs fonts for you.

Important:

- the repo documents the font system, but it does not install desktop fonts automatically
- local app work should verify that `Michroma`, `Universal Sans`, `Rajdhani`, and `Microgramma D Extended Bold` are actually available on the machine
- if the exact font is unavailable in a web-only context, preserve the role with the documented fallback stack
- if the task is a true local application or local design environment, install the fonts before judging the UI

## Final System In One Screen

The system is:

- black control-room base
- subtle scanline texture behind content
- green signal energy
- chrome hierarchy
- crisp typography
- hard-edged panels
- obvious active states
- premium analytics layout

The system is not:

- playful
- rounded and soft
- rainbow-coded
- generic BI software
- generic admin dashboard UI

## Non-Negotiables

- Start from near-black.
- Keep the background layered with atmosphere and scanline treatment.
- Start with `Base Scanline` when you need the safest default surface. Move to louder approved variants only when the product context truly calls for them.
- For workflow-heavy screens, choose the archetype first: `Review Cockpit` or `Analysis Table`.
- Use chrome or chrome-adjacent text for structural labels and titles.
- Keep the type system to four voices only: `Michroma`, `Universal Sans`, `Rajdhani`, and the broadcast headline stack headed by `Microgramma D Extended Bold`.
- Do not let dense workflow controls fall into tiny unreadable chrome text. If the control layer gets tight, move that layer to `Rajdhani` and brighten it before shrinking `Michroma` further.
- Use green as the primary active and current-period color.
- Keep active green controls using dark text, not white text.
- Keep company/account chips in one unified color family.
- Keep KPI cards compact and high-contrast.
- Keep account-card titles in the soft chrome treatment with ambient header glow.
- Keep chart current-series green and comparison-series darker steel.
- Keep dark text inside chart fills.
- Keep grouped comparison tables polished and deliberate.
- Default dashboard header is title-only unless extra context is truly needed.
- Keep animations selective and physical — use the approved animation classes from the Animations tab, never invent new motion patterns.
- Keep the component library on the `Lifted Signal` header rail by default. Treat the five workspace-shell looks at the bottom of `Gradients & Textures` as optional reference variants, not replacements for the main shell.

## Final Header Rule

Default header:

- `PERFORMANCE OVERVIEW`

Default behavior:

- sticky
- integrated with the page atmosphere
- no subtitle by default
- no right-side label by default

## Final Component Rules

### Top Toggles

- Inactive state is dark.
- Active state is a denser green gradient.
- Active text is dark.
- Active state must pop clearly without needing excessive glow.
- For workflow-heavy screens, keep the focused review mode on the left and the denser analysis mode on the right.
- If the toggle copy becomes compact, repeated, or fragile, move it to `Rajdhani` instead of forcing tiny `Michroma`.

### Workflow Modes

- `Review Cockpit` is the focused, progression-driven mode for approval work.
- `Analysis Table` is the denser mode for filters, grouped tables, and cross-cut scanning.
- Review Cockpit should be the default entry mode for review-heavy tools unless the product explicitly says otherwise.
- Review Cockpit hides dense analysis clutter by default.
- Analysis Table can keep more filter depth, but it still must preserve readability.

### Company Chips

- One color system only.
- Slightly larger and bolder than default chips.
- Green border.
- Active chip uses green-tinted fill.

### KPI Cards

- Muted chrome label
- Large white number
- Compact top-right delta pill
- Small `WK1` baseline line at bottom
- Tight spacing and minimal dead space

### Account Cards

- Soft chrome company title
- Faint ambient green glow behind the title area
- `WK1 / WK2 / CHG` at the top
- Labels quieter than values
- Change pill aligned to the right

### Chart Cards

- Chart title uses the same chrome family as account-card titles
- Company label sits close to the bar pair
- `WK1 / WK2` stays quieter than company names
- More spacing between company groups than within each pair

### Broadcast Headlines

- Use the broadcast headline stack only for giant promo/news/date moments
- Keep the sticky dashboard rail on `Michroma`
- Do not use the broadcast headline stack for tabs, chips, KPI labels, or dense dashboard copy

### Support Copy

- Use `Universal Sans` for regular-weight body text, support text, and explanatory copy
- Use `Rajdhani` when the text needs to feel bolder, faster, or more operational

### Comparison Bars

- Current series: green scanline stack
- Previous series: darker steel scanline stack
- Dark text inside both fills
- Green must clearly dominate

### Table

- Metric groups in the first header row
- `WK1 / WK2 / CHG` in the second row
- Brighter account names
- Slight zebra rhythm
- Light separators between groups

## Build Order

When building a new product in this system, use this order:

1. Build the background and atmosphere layers.
2. Choose the product archetype: `Review Cockpit` or `Analysis Table`.
3. Build the sticky header rail.
4. Build the top toggles.
5. Build the company chips.
6. Build KPI cards.
7. Build chart cards.
8. Build account/detail cards if needed.
9. Build the grouped comparison table.
10. Add selective animations to key moments using approved classes.
11. Tune readability before adding more visual effect.

When choosing a background or shell treatment, use this order:

1. decide what kind of surface this is
2. choose the safest approved family for that surface
3. only then decide how much lift, glow, or texture the context can support

When choosing a workflow pattern, use this order:

1. is this a focused review queue or cockpit
2. is this a denser analysis table
3. how much of the dense filter layer actually belongs in the default view
4. whether small controls should stay in `Michroma` or move to `Rajdhani` for readability

If you need to lift a reusable pattern quickly, copy from:

- [`tbpn-component-library.html`](/Users/blakeperry/Documents/New%20Project/tbpn-component-library.html)

## When Something Feels Off

Use this order of correction:

1. improve contrast
2. improve spacing hierarchy
3. improve font sizing
4. improve alignment
5. only then add more texture or glow

Do not solve readability problems with blur.

## Do Not Do

- Do not make active green buttons use white text.
- Do not rainbow-code companies.
- Do not use default chart library colors.
- Do not use soft generic shadows.
- Do not add glow halos to lots of text.
- Do not flatten the background into one solid color.
- Do not make helper text as loud as primary data.
- Do not add verbose subtitles unless the product truly needs them.
- Do not animate every element — reserve animation for page load, tab switch, filter change, and direct interaction.
- Do not loop or continuously repeat any animation.
- Do not invent new animation patterns — use the approved classes from the Animations tab.

## Default Prompt For A New Agent

```text
Build this product in the exact TBPN dashboard system defined in /docs/BRAND_BIBLE.md, /docs/DASHBOARD_ADDENDUM.md, /docs/TBPN_IMPLEMENTATION_RECIPES.md, and /docs/brand-tokens.json. Use /week-over-week-dashboard-working.html as the implementation benchmark, /tbpn-component-library.html as the reusable component reference, and /assets as the visual resource library. If the screen is workflow-heavy, decide first whether it is a focused Review Cockpit or a denser Analysis Table. Preserve the established header rail, active toggle treatment, chip system, KPI hierarchy, account-card title treatment, comparison bar treatment, grouped table styling, and surface-family logic. Use Rajdhani for dense compact controls when Michroma would become too small or fragile. Use only the approved animation classes from the Animations tab in /tbpn-component-library.html. After building, run the self-check in /docs/VALIDATION_CHECKLIST.md. Do not reinterpret the brand from scratch and do not drift into generic SaaS or vendor-default dashboard styling.
```

For copyable approved component markup, also inspect:

- [`tbpn-component-library.html`](/Users/blakeperry/Documents/New%20Project/tbpn-component-library.html)

## Final Rule

If you are unsure what to do, do not invent.

Copy the logic, spacing, hierarchy, and component behavior already established in:

- [`week-over-week-dashboard-working.html`](/Users/blakeperry/Documents/New%20Project/week-over-week-dashboard-working.html)
- [`tbpn-component-library.html`](/Users/blakeperry/Documents/New%20Project/tbpn-component-library.html)

Then extend carefully.
