# Page List

This file defines the approved page set and what each page is expected to contain.

## Core Product Pages

### Aktivitas

- role: home portfolio and recent activity entry
- required modules:
  - `Top App Bar`
  - `Balance Summary`
  - `Quick Action Button`
  - `Watchlist`
  - `Bottom Navigation`
- optional modules:
  - secondary summary chips
  - recent transaction preview
- composition rule: one clear balance focal point, then action row, then market or activity modules

### Trending

- role: market discovery and scanning
- required modules:
  - `Top App Bar`
  - `Segment Tab`
  - `Trending Carousel`
  - `Market Filter Header`
  - `Stock List Item`
  - `Bottom Navigation`
- optional modules:
  - time filter with `Filter Select`
  - secondary category tabs
- composition rule: compact and scan-friendly; avoid oversized hero content

### Detail Saham

- role: stock detail and decision support
- required modules:
  - `Top App Bar`
  - price headline area
  - `Key Stats`
  - chart or change area
  - main action area
- optional modules:
  - related market entries
  - market news teaser
- composition rule: price context first, supporting metrics second, action third

### Topup Buying Power 1

- role: amount entry
- required modules:
  - `Top App Bar`
  - `Payment Stepper`
  - `Amount Input`
  - `Amount Presets`
  - primary CTA
- composition rule: amount decision first, payment selection later

### Topup Buying Power 2

- role: funding method selection
- required modules:
  - `Top App Bar`
  - `Payment Stepper`
  - `Payment Method List`
  - `Top Up Destination`
  - primary CTA
- composition rule: keep selection rows readable and clearly selected

### Topup Buying Power 3

- role: confirmation or payment completion
- required modules:
  - `Top App Bar`
  - `Payment Stepper`
  - confirmation summary
  - payment method recap
  - primary CTA or completion state
- composition rule: summarize before commit, do not reintroduce exploratory content

## Design System Pages

These pages are documentation pages, not product pages.

### Design System / Components

- role: atomic and reusable component library
- should contain:
  - production components
  - variant sets
  - icon and logo inventory
- should not contain:
  - random section demos mixed into the same layout area

### Design System / Examples

- role: usage examples and page assembly demonstrations
- rule: examples may extend the original screen structure, but must still use the real component system

### Design System / Sections

- role: reusable business-module patterns
- rule: section components here should match actual page use cases

### Design System / Handbook

- role: visual manual for foundations and usage
- rule: handbook sections must stay readable even for readers with weak English

### Design System / Color Palette

- role: color ramp and palette reference for future expansion
- rule: treat as reference, not as a place to invent new semantic colors casually

## Common Cross-Page Rules

1. Keep all primary app screens at `375px` width.
2. Keep the main content width at `343px` unless edge-aware sections explicitly need `360px`.
3. Use one primary CTA per task section.
4. Keep bottom navigation fixed to app-level pages, not to transient modals or documentation pages.
5. Reuse the same market row and funding patterns across screens.

## Expansion Rule

If a new request does not fit an existing page exactly, map it to the closest shell first:

- portfolio or activity = `Aktivitas`
- market scanning = `Trending`
- asset deep dive = `Detail Saham`
- multi-step money movement = `Topup Buying Power`
