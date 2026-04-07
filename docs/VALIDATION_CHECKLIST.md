# TBPN Validation Checklist

## Background & Atmosphere

- [ ] Is the base near-black, not white or gray?
- [ ] Are scanline and atmosphere layers present behind content?
- [ ] Is there a green atmosphere wash?

## Typography

- [ ] Are you using only the four approved font roles (`Michroma`, `Universal Sans`, `Rajdhani`, `Microgramma D Extended Bold`)?
- [ ] Is the broadcast headline font reserved for giant promo/editorial moments only?
- [ ] Are structural labels and titles uppercase in `Michroma`?
- [ ] Is support copy in `Universal Sans`?
- [ ] Are bold values and UI text in `Rajdhani`?
- [ ] If a dense control became too small or weak for `Michroma`, did you switch it to `Rajdhani` instead of leaving it fragile?
- [ ] Are compact buttons, toggles, chips, and status pills staying above the readable floor?
- [ ] Is muted/support text still readable at normal working distance, not just technically on-brand?

## Color

- [ ] Is green used only for active state, signal, and current period?
- [ ] Is chrome used for structural labels and titles?
- [ ] Are active green buttons using dark text, not white?
- [ ] Are company chips all one color family, not rainbow-coded?

## Controls

- [ ] Do active toggles use a green gradient with dark text?
- [ ] Do chips use green border with green-tinted active fill?
- [ ] Is the header sticky with integrated scanline background?
- [ ] Are dense workflow controls readable before they are “chrome”?
- [ ] Are compact action buttons and pills big enough to scan quickly?

## KPI Cards

- [ ] Is the label chrome-muted, not gray?
- [ ] Is the big number white and dominant?
- [ ] Is the delta pill compact and anchored top-right?
- [ ] Is the baseline line small but legible at the bottom?
- [ ] In review-heavy screens, is the KPI row limited to the few metrics that actually move the operator forward?

## Charts

- [ ] Is the current series green scanline and clearly dominant?
- [ ] Is the previous series darker steel and secondary?
- [ ] Is text dark inside both bar fills?
- [ ] Is there more space between company groups than within each pair?

## Tables

- [ ] Are there grouped metric headers?
- [ ] Is there a clean `WK1/WK2/CHG` subheader row?
- [ ] Are account names brighter than data cells?
- [ ] Is there subtle zebra rhythm and light vertical separators?
- [ ] Are table headers and compact cells still readable at working distance?
- [ ] Is the dense table mode cleaner than spreadsheet-default gray UI?

## Workflow Modes

- [ ] Did you decide whether the screen is a focused `Review Cockpit` or a denser `Analysis Table` before styling it?
- [ ] If it is a review workflow, is the focused review mode the default entry mode?
- [ ] Is the focused review mode visually lighter and less cluttered than the dense analysis mode?
- [ ] Are dense analytical filters hidden from the review cockpit unless they are truly needed?
- [ ] Is the left-most main toggle the focused mode and the denser mode to the right?

## Animations

- [ ] Are you using only approved animation classes (`.tbpn-shadow-drop`, `.tbpn-scale-fade`, `.tbpn-flip-in`, `.tbpn-pulse-activate`, `.tbpn-hover-lift`, `.tbpn-bar-grow-item`, `.tbpn-chip-pop`, `.tbpn-stagger`, `.tbpn-heartbeat`, `.tbpn-shadow-press`)?
- [ ] Are animations selective — only at page load, tab switch, filter change, and direct interaction?
- [ ] Is nothing looping or repeating continuously?
- [ ] Is `.tbpn-flip-in` used only for major view changes, not within a single dashboard?
- [ ] Is `.tbpn-heartbeat` used only for threshold crossings, not normal data?
- [ ] Are `.tbpn-hover-lift` and `.tbpn-shadow-press` never combined on the same element?

## General

- [ ] Does readability come before effects?
- [ ] Is contrast, spacing, and font size correct before adding glow or texture?
