# TBPN Implementation Recipes

This file contains the exact implementation patterns another coding agent should use to reproduce the final TBPN dashboard style.

Reference build:

- [`week-over-week-dashboard-working.html`](/Users/blakeperry/Documents/New%20Project/week-over-week-dashboard-working.html)
- [`tbpn-component-library.html`](/Users/blakeperry/Documents/New%20Project/tbpn-component-library.html)

Use the working dashboard when you need real page composition.

Use the component library when you need the cleanest copyable component pattern.

Use the `Gradients & Textures` tab as a surface chooser:

- start from one safe default
- choose approved variants by product context first
- use readability and density as the second filter
- treat the five ClickUp-style shell looks at the bottom of that tab as reference workspace shells, not the default library header

## 1. Root Tokens

```css
:root {
  --tbpn-black: #020403;
  --tbpn-studio: #050808;
  --tbpn-panel: rgba(3, 10, 8, 0.8);
  --tbpn-green: #18d39c;
  --tbpn-green-bright: #6affd2;
  --tbpn-green-deep: #0d7859;
  --tbpn-chrome-light: #eaf0f7;
  --tbpn-chrome-mid: #98a9c8;
  --tbpn-chrome-dark: #485668;
  --tbpn-text: #f3f6fb;
  --tbpn-muted: #9fb1ca;
  --tbpn-line: rgba(131, 255, 210, 0.17);
  --tbpn-line-chrome: rgba(170, 186, 223, 0.22);

  --tbpn-chrome-gradient: linear-gradient(180deg, #f7fbff 0%, #b7c5dd 48%, #4b5c73 100%);
  --tbpn-green-gradient: linear-gradient(180deg, #2de7a9 0%, #0f8c63 100%);
  --tbpn-panel-gradient: linear-gradient(180deg, rgba(6, 12, 10, 0.92), rgba(3, 7, 6, 0.96));

  --current: #52e0ae;
  --previous: #6d7891;
  --negative: #c85a58;
  --g: #52e0ae;
  --gbg: rgba(82, 224, 174, 0.12);
  --r: #c85a58;
  --rbg: rgba(200, 90, 88, 0.12);

  --page-pad: 20px;
  --section-gap: 20px;
  --sub-gap: 12px;
  --card-gap: 8px;
  --card-pad: 12px;
  --card-min: 82px;
  --chip-h: 28px;
  --chip-px: 12px;
  --chip-text: 11px;
  --tab-h: 34px;
  --tab-px: 14px;
  --tbpn-font-display: "Michroma", sans-serif;
  --tbpn-font-support: "Universal Sans", "Rajdhani", sans-serif;
  --tbpn-font-ui: "Rajdhani", sans-serif;
  --tbpn-font-broadcast: "Microgramma D Extended Bold", "Microgramma Extd D", "Microgramma", "Eurostile Extended", "Eurostile", "Michroma", sans-serif;
}
```

## 2. Background Recipe

```css
body {
  margin: 0;
  min-height: 100vh;
  background:
    radial-gradient(circle at 50% -12%, rgba(96, 255, 208, 0.14), transparent 28%),
    radial-gradient(circle at 50% 18%, rgba(24, 211, 156, 0.12), transparent 32%),
    linear-gradient(180deg, #030706 0%, #020403 36%, #010202 100%);
  color: var(--tbpn-text);
  font-family: var(--tbpn-font-support);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  overflow-x: hidden;
}

.tbpn-bg-lines,
.tbpn-bg-atmosphere {
  position: fixed;
  inset: 0;
  pointer-events: none;
}

.tbpn-bg-lines {
  z-index: 0;
  background-image: linear-gradient(
    to bottom,
    #005947 0px,
    #00ad73 1px,
    #59e6bf 2px,
    #00ad73 3px,
    #005947 4px
  );
  background-size: 100% 4px;
  background-repeat: repeat;
  opacity: 0.12;
  mask-image: linear-gradient(180deg, transparent 0%, rgba(0, 0, 0, 0.9) 24%, #000 48%, rgba(0, 0, 0, 0.92) 100%);
}

.tbpn-bg-atmosphere {
  z-index: 0;
  background:
    radial-gradient(circle at 50% 16%, rgba(106, 255, 210, 0.28), transparent 20%),
    radial-gradient(circle at 50% 42%, rgba(24, 211, 156, 0.14), transparent 34%),
    linear-gradient(to top, #ffffff 0%, #59e6bf 4%, #00ad99 15%, #00241c 34%, #000000 68%);
  mix-blend-mode: multiply;
  opacity: 0.88;
}
```

## 3. Header Rail Recipe

```css
.hdr {
  position: sticky;
  top: 0;
  z-index: 30;
  padding: 22px var(--page-pad) 18px;
  border-bottom: 1px solid var(--tbpn-line);
  background:
    radial-gradient(120% 140% at 50% 100%, rgba(81, 255, 208, 0.20), rgba(81, 255, 208, 0) 42%),
    radial-gradient(84% 90% at 50% 0%, rgba(70, 255, 196, 0.14), rgba(70, 255, 196, 0) 44%),
    linear-gradient(180deg, rgba(18, 50, 40, 0.98), rgba(11, 27, 22, 0.985) 52%, rgba(4, 9, 7, 0.99));
  box-shadow:
    inset 0 1px 0 rgba(255, 255, 255, 0.05),
    inset 0 -1px 0 rgba(24, 211, 156, 0.12),
    0 8px 24px rgba(0, 0, 0, 0.24);
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(10px);
}

.hdr h1 {
  font-family: var(--tbpn-font-display);
  font-size: 16px;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: transparent;
  background: linear-gradient(180deg, #eef3fa 0%, #cbd5e2 46%, #9aa7bb 100%);
  -webkit-background-clip: text;
  background-clip: text;
}
```

Rendered example:

- `Layout Rails And Section Headers` in [`tbpn-component-library.html`](/Users/blakeperry/Documents/New%20Project/tbpn-component-library.html)

This is now the default library top rail treatment: `Lifted Signal`.

Keep the actual dashboard rail darker and more restrained by default unless the product context truly needs more lift.

## 3A. Broadcast Headline Recipe

```css
.broadcast-slug,
.broadcast-headline,
.broadcast-date {
  font-family: var(--tbpn-font-broadcast);
  text-transform: uppercase;
  color: #050808;
  letter-spacing: 0.01em;
}

.broadcast-slug {
  font-size: clamp(2rem, 4.4vw, 3.4rem);
  line-height: 0.92;
}

.broadcast-headline {
  font-size: clamp(1.7rem, 3.4vw, 2.8rem);
  line-height: 0.96;
}

.broadcast-date {
  font-size: clamp(1.45rem, 3vw, 2.4rem);
  line-height: 0.96;
}
```

Use this only for giant promo/news/date bars, masthead slugs, and editorial callouts where Michroma is not heavy enough.

Do not use it for dashboard rails, tabs, chips, KPI labels, chart titles, table headers, or dense product UI.

## 3B. Support Copy Recipe

```css
.support-copy,
.field-help,
.card-note,
.empty-copy {
  font-family: var(--tbpn-font-support);
  font-size: 13px;
  line-height: 1.5;
  font-weight: 400;
  letter-spacing: 0.01em;
  color: #a3b4c8;
}

.support-copy-strong,
.utility-copy-strong {
  font-family: var(--tbpn-font-ui);
  font-size: 13px;
  line-height: 1.42;
  font-weight: 600;
  letter-spacing: 0.01em;
  color: #dce5f0;
}
```

Use Universal Sans for calmer regular-weight explanatory copy.

Switch to Rajdhani when the copy needs more punch, denser readability, or a stronger operational tone.

## 3C. How To Choose A Surface

Choose the surface family in this order:

1. Is this a dense dashboard or product screen?
   - Use `Base Scanline`
   - Avoid using for: title-card, promo, or hero moments that need more lift or stronger brand atmosphere
2. Is it still product UI, but it needs more brand lift?
   - Use `Lifted Signal`
   - Avoid using for: the default everywhere background or the densest data-heavy screens when the extra lift is unnecessary
3. Is it a hero, editorial, promo, or title-card moment?
   - Use `Adaptive Scanline`, `Heavy Horizontal`, `Dot Grid`, or `Chrome` depending on role
   - `Adaptive Scanline`: premium hero/editorial background with texture rhythm
   - `Heavy Horizontal`: title-card, masthead, or broadcast-stage surface
   - `Dot Grid`: spotlighted promo/editorial or hero/profile surface
   - `Chrome`: giant titles, logo/title lockups, icon bars, and premium shell accents
   - Avoid using for: dense dashboards, tables, or operational product shells
4. Is it calm, light, open, or supportive?
   - Use `Soft Signal` or `Quiet Utility`
   - Avoid using for: the main shell of dense operational UI that needs the stronger control-room floor
5. Is it a workspace shell, header, or sidebar pattern?
   - Use one of the five ClickUp-style shell variants at the bottom of `Gradients & Textures`
   - Treat those as reference workspace shells, not as the default library shell

When in doubt:

- start with `Base Scanline`
- move to louder variants only if the product context and readability budget can support them

## 4. Toggle Recipe

```css
.wk-tog,
.view-tog {
  display: flex;
  gap: 0;
  background: linear-gradient(180deg, rgba(10, 14, 17, 0.95), rgba(4, 6, 7, 0.98));
  border-radius: 6px;
  padding: 3px;
  border: 1px solid rgba(139, 157, 182, 0.18);
}

.wk-btn,
.view-btn {
  padding: 0 var(--tab-px);
  height: var(--tab-h);
  display: flex;
  align-items: center;
  font-family: "Michroma", sans-serif;
  font-size: 10px;
  letter-spacing: 0.055em;
  text-transform: uppercase;
  font-weight: 500;
  color: #94a7c0;
}

#libraryModes .view-btn {
  font-family: var(--tbpn-font-broadcast);
  font-size: 12px;
  letter-spacing: 0.01em;
  line-height: 0.96;
  min-width: 118px;
  justify-content: center;
  padding: 0 16px;
  color: #b2bfd1;
  text-shadow: 0 1px 0 rgba(0, 0, 0, 0.92);
}

.wk-btn.ac,
.view-btn.ac {
  background:
    linear-gradient(180deg, rgba(255, 255, 255, 0.14), rgba(255, 255, 255, 0) 28%),
    linear-gradient(180deg, #41e4af 0%, #24c793 56%, #139d6e 100%);
  color: #07110d;
  font-weight: 700;
  border: 1px solid rgba(152, 255, 222, 0.65);
}

#libraryModes .view-btn.ac {
  text-shadow: none;
}
```

Rendered example:

- `Toggles And Segmented Controls` in [`tbpn-component-library.html`](/Users/blakeperry/Documents/New%20Project/tbpn-component-library.html)

Use this exact override only for the six top-level component-library tabs:

- `Core Library`
- `Spec Imports`
- `Fonts`
- `Gradients & Textures`
- `Logo`
- `Animations`

## 5. Company Chip Recipe

```css
.tb {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  height: 28px;
  padding: 0 12px;
  border-radius: 4px;
  border: 1px solid rgba(24, 211, 156, 0.28);
  background: rgba(5, 8, 8, 0.92);
  color: #c8d3e4;
  font-family: "Rajdhani", sans-serif;
  font-size: 11px;
  font-weight: 700;
  letter-spacing: 0.035em;
  text-transform: uppercase;
}

.tb.ac {
  background: linear-gradient(180deg, rgba(45, 231, 169, 0.28), rgba(15, 140, 99, 0.28));
  border-color: #43e7b1;
  color: #f3f6fb;
}
```

Rendered example:

- `Chips And Filters` in [`tbpn-component-library.html`](/Users/blakeperry/Documents/New%20Project/tbpn-component-library.html)

## 6. KPI Card Recipe

```css
.kpi {
  min-height: 82px;
  padding: 12px 12px 11px;
  border: 1px solid rgba(24, 211, 156, 0.18);
  border-radius: 6px;
  background: var(--tbpn-panel-gradient);
  display: flex;
  flex-direction: column;
  position: relative;
}

.kpi:nth-child(-n + 4) {
  min-height: 96px;
}

.kpi .l {
  font-family: "Michroma", sans-serif;
  font-size: 12px;
  letter-spacing: 0.035em;
  text-transform: uppercase;
  color: #c1ccda;
  margin-bottom: 6px;
  min-height: 24px;
  padding-right: 64px;
}

.kpi .v {
  font-size: clamp(2.15rem, 3.15vw, 2.8rem);
  font-weight: 700;
  line-height: 0.94;
  color: var(--tbpn-text);
}

.kpi .prev {
  margin-top: auto;
  font-size: 11px;
  color: #a7b4c6;
}

.kpi .delta {
  position: absolute;
  top: 10px;
  right: 10px;
  min-width: 44px;
  height: 28px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  font-size: 12px;
  font-weight: 800;
  border-radius: 4px;
}
```

Rendered example:

- `KPI Cards` in [`tbpn-component-library.html`](/Users/blakeperry/Documents/New%20Project/tbpn-component-library.html)

## 7. Account Card Recipe

```css
.acard {
  position: relative;
  overflow: hidden;
  padding: 14px 14px 12px;
  border: 1px solid rgba(24, 211, 156, 0.16);
  border-radius: 6px;
  background:
    linear-gradient(180deg, rgba(7, 12, 11, 0.975), rgba(2, 5, 5, 0.985)),
    radial-gradient(circle at 50% -8%, rgba(106, 255, 210, 0.04), transparent 40%),
    linear-gradient(180deg, rgba(106, 255, 210, 0.028), transparent 16%);
}

.acard::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 58px;
  background:
    radial-gradient(circle at 18% 20%, rgba(106, 255, 210, 0.08), transparent 34%),
    linear-gradient(180deg, rgba(106, 255, 210, 0.028), transparent 80%);
}

.acard h3 {
  position: relative;
  z-index: 1;
  font-family: "Michroma", sans-serif;
  font-size: 14px;
  letter-spacing: 0.028em;
  text-transform: uppercase;
  color: #f2f6fb;
  text-shadow: 0 1px 0 rgba(0, 0, 0, 0.9), 0 0 10px rgba(255, 255, 255, 0.04);
}
```

## 8. Chart Card Recipe

```css
.cc h3 {
  font-family: "Michroma", sans-serif;
  font-size: 14px;
  letter-spacing: 0.04em;
  text-transform: uppercase;
  color: #f2f6fb;
  text-shadow: 0 1px 0 rgba(0, 0, 0, 0.9), 0 0 10px rgba(255, 255, 255, 0.04);
}

.cmp-chart {
  display: flex;
  flex-direction: column;
  gap: 16px;
}

.cmp-row {
  display: flex;
  flex-direction: column;
  gap: 1px;
}

.cmp-label {
  font-size: 13px;
  color: #e2e9f2;
  font-weight: 700;
  letter-spacing: 0.025em;
  text-transform: uppercase;
}

.cmp-bars {
  display: flex;
  flex-direction: column;
  gap: 1px;
}

.cmp-wk {
  font-family: "Michroma", sans-serif;
  font-size: 8px;
  color: #8898ae;
}
```

## 9. Final Comparison Bar Recipe

```css
.cmp-fill {
  font-size: 11px;
  font-weight: 700;
  color: #07110d;
}

.cmp-fill.previous {
  background:
    repeating-linear-gradient(180deg, rgba(255, 255, 255, 0.1) 0 1px, rgba(255, 255, 255, 0) 1px 3px),
    linear-gradient(180deg, #b1bbcf 0%, #7a859b 56%, #515c70 100%);
}

.cmp-fill.current {
  background:
    repeating-linear-gradient(180deg, rgba(255, 255, 255, 0.1) 0 1px, rgba(255, 255, 255, 0) 1px 3px),
    linear-gradient(180deg, #a8f4d9 0%, #59e0ae 54%, #21b57f 100%);
}
```

## 10. Table Recipe

```css
.wow-table {
  width: 100%;
  border-collapse: collapse;
  font-size: 13px;
}

.wow-table thead tr:first-child th {
  font-size: 10px;
  color: #d8e2ee;
  background:
    linear-gradient(180deg, rgba(12, 18, 18, 0.98), rgba(6, 9, 9, 0.98)),
    linear-gradient(90deg, rgba(106, 255, 210, 0.03), transparent 40%);
}

.wow-table thead tr:nth-child(2) th {
  font-size: 9px;
  color: #aab8ca;
  background: rgba(7, 11, 11, 0.96);
}

.wow-table td {
  padding: 11px 12px;
  color: #d5deea;
}

.wow-table td:first-child {
  color: #f0f5fb;
  text-shadow: 0 1px 0 rgba(0, 0, 0, 0.85);
}
```

## 11. Animation Recipes

### Entrance: Shadow Drop

```css
@keyframes tbpn-shadow-drop {
  0%   { opacity: 0; transform: translateY(-20px) scale(0.95);
         box-shadow: 0 0 0 rgba(0,0,0,0); }
  50%  { opacity: 1; transform: translateY(5px) scale(1.01);
         box-shadow: 0 12px 28px rgba(0,0,0,0.45),
                     0 0 32px rgba(24,211,156,0.12); }
  75%  { transform: translateY(-2px) scale(1);
         box-shadow: 0 5px 14px rgba(0,0,0,0.28),
                     0 0 18px rgba(24,211,156,0.07); }
  100% { transform: translateY(0) scale(1);
         box-shadow: 0 2px 8px rgba(0,0,0,0.18),
                     0 0 12px rgba(24,211,156,0.04); }
}
.tbpn-shadow-drop {
  animation: tbpn-shadow-drop 300ms cubic-bezier(0.22, 0.68, 0.35, 1.0) both;
}
```

### Entrance: Scale Fade

```css
@keyframes tbpn-scale-fade {
  0%   { opacity: 0; transform: scale(0.98); }
  100% { opacity: 1; transform: scale(1); }
}
.tbpn-scale-fade {
  animation: tbpn-scale-fade 250ms cubic-bezier(0.22, 0.68, 0.35, 1.0) both;
}
```

### Entrance: Dramatic Flip

```css
@keyframes tbpn-flip-in {
  0%   { opacity: 0; transform: perspective(600px) rotateX(-85deg); }
  60%  { opacity: 1; transform: perspective(600px) rotateX(10deg); }
  80%  { transform: perspective(600px) rotateX(-3deg); }
  100% { transform: perspective(600px) rotateX(0deg); }
}
.tbpn-flip-in {
  animation: tbpn-flip-in 350ms cubic-bezier(0.22, 0.68, 0.35, 1.0) both;
}
```

### Toggle Pulse

```css
@keyframes tbpn-pulse-activate {
  0%   { box-shadow: 0 0 0 0 rgba(65,228,175,0.55); }
  50%  { box-shadow: 0 0 16px 4px rgba(65,228,175,0.35); }
  100% { box-shadow: 0 0 0 0 rgba(65,228,175,0); }
}
.tbpn-pulse-activate { animation: tbpn-pulse-activate 200ms ease-out; }
```

### Hover Lift

```css
.tbpn-hover-lift {
  transition: transform 200ms cubic-bezier(0.22, 0.68, 0.35, 1.0),
              box-shadow 200ms cubic-bezier(0.22, 0.68, 0.35, 1.0);
}
.tbpn-hover-lift:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 24px rgba(0,0,0,0.28), 0 0 16px rgba(24,211,156,0.06);
}
```

### Chart Bar Grow

```css
@keyframes tbpn-bar-grow {
  0%   { width: 0%; opacity: 0.6; }
  100% { opacity: 1; }
}
.tbpn-bar-grow-item {
  animation: tbpn-bar-grow 350ms cubic-bezier(0.22, 0.68, 0.35, 1.0) both;
  animation-delay: calc(var(--bar-i, 0) * 175ms);
}
```

### Chip Pop

```css
@keyframes tbpn-chip-pop {
  0%   { transform: scale(1); }
  50%  { transform: scale(1.06); }
  100% { transform: scale(1); }
}
.tbpn-chip-pop { animation: tbpn-chip-pop 200ms cubic-bezier(0.22, 0.68, 0.35, 1.0); }
```

### Stagger Entrance

```css
.tbpn-stagger {
  animation: tbpn-shadow-drop 250ms cubic-bezier(0.22, 0.68, 0.35, 1.0) both;
  animation-delay: calc(var(--i, 0) * 50ms);
}
```

### Heartbeat

```css
@keyframes tbpn-heartbeat {
  0%   { transform: scale(1); }
  14%  { transform: scale(1.06); }
  28%  { transform: scale(1); }
  42%  { transform: scale(1.04); }
  56%  { transform: scale(1); }
  100% { transform: scale(1); }
}
.tbpn-heartbeat { animation: tbpn-heartbeat 600ms cubic-bezier(0.22, 0.68, 0.35, 1.0) both; }
```

### Shadow Press

```css
@keyframes tbpn-shadow-press {
  0%   { box-shadow: 0 2px 8px rgba(0,0,0,0.18), 0 0 12px rgba(24,211,156,0.04);
         transform: translateY(0); }
  50%  { box-shadow: inset 0 2px 8px rgba(0,0,0,0.45), inset 0 1px 3px rgba(0,0,0,0.3),
                     0 0 8px rgba(24,211,156,0.06);
         transform: translateY(1px); }
  100% { box-shadow: 0 2px 8px rgba(0,0,0,0.18), 0 0 12px rgba(24,211,156,0.04);
         transform: translateY(0); }
}
.tbpn-shadow-press { animation: tbpn-shadow-press 200ms cubic-bezier(0.22, 0.68, 0.35, 1.0); }
```

### Animation Build Rules

- animations are selective, not decorative
- use at boundaries only: page load, tab switch, filter change, direct interaction
- do not loop or repeat any animation
- do not animate every element — reserve for key moments
- do not combine hover-lift and shadow-press on the same element
- remove animation classes on `animationend` for re-triggerable animations
- use `--i` for stagger delays and `--bar-i` for bar stagger delays

Rendered examples:

- `Animations` tab in [`tbpn-component-library.html`](/Users/blakeperry/Documents/New%20Project/tbpn-component-library.html)

## 12. Build Rules

Use these recipes directly.

Do not:

- replace the fonts
- brighten helper text until it competes with the main numbers
- make the previous series lighter than the current series
- revert to white text on active green controls
- remove the background scanline and atmosphere system
