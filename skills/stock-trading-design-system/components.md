# Components

This file defines which components are approved, how they should be used, and what their stable APIs mean.

## Usage Rules

1. Reuse the existing component before drawing a new frame.
2. Preserve component property names from `tokens.json`.
3. Use local icon or logo instances for instance-swap slots.
4. Check `assets/icon-index.json` before selecting an icon for navigation, action, monitoring, trigger, stock logo, or payment slots.
5. Add states before adding new visual styles.
6. Treat section components as reusable patterns, not one-off layouts.

## Foundations For All Components

- screen width baseline: `375px`
- card radius baseline: `12px`
- compact control radius baseline: `6px`
- primary vertical rhythm: `16px`
- page horizontal margin: `20px`
- primary action heights: `48px` and `40px`

## Navigation

### Top App Bar

- purpose: screen title and top-level navigation
- component name: `Stock Trading / Navigation / Top App Bar`
- required properties:
  - `Title`
  - `Leading Icon`
  - `Trailing Icon`
  - `Leading`
  - `Trailing`
- use for:
  - `Aktivitas`
  - `Trending`
  - `Detail Saham`
  - top up flow steps

### Bottom Navigation

- purpose: primary app-level navigation
- component name: `Stock Trading / Navigation / Bottom Navigation`
- required properties:
  - `Activity Label`
  - `Trending Label`
  - `Top Up Label`
  - `Market Label`
  - `Profile Label`
  - `Selected`
- rule: never detach; selection must reflect the active page

## Action Components

### Primary Button

- purpose: main call to action
- sizes: `Large`, `Medium`
- states: `Default`, `Pressed`, `Focus`, `Disabled`, `Loading`
- icon mode: `None`, `Leading`
- use for:
  - payment confirmation
  - top up progression
  - critical single-step actions

### Icon Button

- purpose: compact utility action
- states: `Default`, `Pressed`, `Focus`, `Disabled`
- rule: use for icon-only actions, not for primary page CTA
- icon rule: icon meaning must come from `assets/icon-index.json`; do not choose an icon only because the shape looks similar

### Text Button

- purpose: secondary action and low-emphasis navigation
- sizes: `Medium`, `Small`
- states: `Default`, `Pressed`, `Disabled`
- common copy:
  - `Lihat Semua`
  - `Ganti`

### Quick Action Button

- purpose: fast portfolio actions
- actions: `Deposit`, `Withdraw`
- states: `Default`, `Pressed`, `Focus`, `Disabled`

## Data Discovery Components

### Segment Tab

- purpose: short category switching
- states: `Selected`, `Default`, `Pressed`, `Disabled`
- rule: use for market groupings, not for long filters

### Filter Select

- purpose: compact time or filter selector
- states: `Default`, `Pressed`, `Focus`, `Disabled`

### Market Trend Card

- purpose: compact market highlight card
- states: `Default`, `Pressed`, `Focus`
- semantic change modes: `Positive`, `Negative`
- required properties:
  - `Ticker`
  - `Price`
  - `Change Label`
  - `Logo`

### Stock List Item

- purpose: dense quote row
- densities: `Default`, `Compact`
- semantic change modes: `Positive`, `Negative`, `Neutral`
- required properties:
  - `Ticker`
  - `Company Name`
  - `Price`
  - `Change Label`
  - `Logo`
- rule: logo must be a local stock logo component, not a placeholder

### Key Stat Row

- purpose: compact metric row in detail pages
- required properties:
  - `Metric Label`
  - `Metric Value`
  - `Divider`

## Funding And Payment Components

### Payment Stepper

- purpose: multi-step funding progress
- required properties:
  - `Step One Label`
  - `Step Two Label`
  - `Current Step`

### Payment Method Item

- purpose: selectable funding method row
- states: `Selected`, `Default`, `Pressed`, `Disabled`
- required properties:
  - `Method Label`
  - `Method Icon`

### Amount Chip

- purpose: preset amount selection
- states: `Default`, `Selected`, `Pressed`, `Disabled`
- required property:
  - `Amount`

### Amount Input

- purpose: freeform value entry
- states: `Default`, `Focused`, `Filled`, `Error`, `Disabled`
- required property:
  - `Value`

## Section Components

These are reusable business blocks. They are larger than atomic components and should be reused for page assembly.

### Approved Section-Level Patterns

- `Balance Summary`
- `Trending Carousel`
- `Watchlist`
- `Market Filter Header`
- `Payment Method List`
- `Amount Presets`
- `Top Up Destination`
- `Key Stats`

Rule:

- reuse these when building pages that match the same business structure
- do not invent a new section wrapper if one of these already fits

## Naming Rules

- component names stay in title case
- property names stay human-readable and stable
- state names stay short and explicit
- do not rename a property only to match one local frame's copy

## Review Checklist

- Did I use the real component instance?
- Did I preserve the correct state model?
- Did I preserve the correct local icon or logo?
- Did I keep semantic color usage consistent?
- Did I keep the component API readable for PM, design, and engineering?
