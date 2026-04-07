# TBPN Brand Kit

TBPN brand kit — design system, component library, and agent onboarding for building on-brand products.

Start here:

- [`/docs/START_HERE_FOR_AGENTS.md`](/Users/blakeperry/Documents/New%20project/docs/START_HERE_FOR_AGENTS.md)

Core references:

- [`/tbpn-component-library.html`](/Users/blakeperry/Documents/New%20project/tbpn-component-library.html)
- [`/docs/BRAND_BIBLE.md`](/Users/blakeperry/Documents/New%20project/docs/BRAND_BIBLE.md)
- [`/docs/DASHBOARD_ADDENDUM.md`](/Users/blakeperry/Documents/New%20project/docs/DASHBOARD_ADDENDUM.md)
- [`/docs/TBPN_IMPLEMENTATION_RECIPES.md`](/Users/blakeperry/Documents/New%20project/docs/TBPN_IMPLEMENTATION_RECIPES.md)
- [`/docs/brand-tokens.json`](/Users/blakeperry/Documents/New%20project/docs/brand-tokens.json)

## Font Requirement

If you are building a local application, local prototype, native app, or any environment that depends on system-installed fonts, install the approved fonts on the machine first.

GitHub does not install fonts for you.

Approved font roles:

- `Michroma`
- `Universal Sans`
- `Rajdhani`
- `Microgramma D Extended Bold`

For web-only work, use the documented fallback stacks when the exact local font is unavailable. For local app work, do not treat fallback rendering as final if the fonts are not installed.

## Workflow UI Rule

For workflow-heavy products, choose the product archetype before styling the details:

- `Review Cockpit`: focused review and progression mode
- `Analysis Table`: denser filtering and comparison mode

For compact workflow controls, use `Rajdhani` when `Michroma` would become too small or too weak to read cleanly.
