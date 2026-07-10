---
name: stock-trading-design-system
description: Use this project skill when creating or reviewing stock trading app screens, mobile fintech prototypes, Figma updates, component specs, page specs, PM output, or implementation prompts that must follow the Stock Trading design system extracted from Figma file OHAU7JaTYZ1uNsITyPhvIF.
---

# Stock Trading Design System Skill

Use this skill whenever a designer, product manager, or coding agent works on the Stock Trading app and needs the output to stay aligned with the current design system.

This skill is for collaboration, not only for AI generation. It is the shared rulebook for:

- Figma page expansion
- new feature prototype output
- component and token governance
- screen review and QA
- PM-to-design handoff
- design-to-code prompts

## Source Of Truth

- Figma source file: `Stock Trading App - UI Concept (Community)` / file key `OHAU7JaTYZ1uNsITyPhvIF`
- Core app pages in the design file:
  - `Aktivitas`
  - `Trending`
  - `Detail Saham`
  - `Topup Buying Power 1`
  - `Topup Buying Power 2`
  - `Topup Buying Power 3`
- Design system pages in the file:
  - `Design System / Components`
  - `Design System / Examples`
  - `Design System / Sections`
  - `Design System / Handbook`
  - `Design System / Color Palette`

## Read Order

Use progressive loading. Do not read everything up front unless the task genuinely needs it.

### Layer 1: Entry

Always start here:

1. `SKILL.md`
2. `GLOSSARY.md`

### Layer 2: Working Specs

Pick by task type:

- component work: `components.md`
- page work: `page-list.md`
- layout sizing and measurements: `docs/layout-and-component-specs.md`
- code or prototype variables: `tokens.json`, `design-tokens.css`, `component-variables.css`

### Layer 3: Extended References

Read only when needed:

- reusable page shells: `page-shells/`
- business-domain guidance: `product-lines/`
- common mistakes and review patterns: `case-studies/`
- onboarding and distribution: `INSTALL.md`
- terminology and governance updates: `CHANGELOG.md`

## Hard Rules

### Always

1. Always keep the product mobile-first and based on `375px` screen width.
2. Always use the token system before inventing raw values.
3. Always reuse existing components before creating detached frames.
4. Always preserve the dark financial-product tone: dense, task-oriented, data-first.
5. Always use the current naming system for pages, components, tokens, and states.
6. Always keep stock movement semantics consistent:
   - positive = green
   - negative = red
   - neutral = muted text
7. Always keep button, tab, list row, payment control, and navigation elements componentized.
8. Always use local icon/logo components for business rows instead of pasted bitmap placeholders.
9. Always use role-based typography names such as `Display`, `Headline`, `Title`, `Body`, `Label`.
10. Always review new output against the Figma handbook pages before handoff.

### Never

1. Never introduce a new visual style only because a single screen looks empty.
2. Never use `H1 / H2 / body1 / body2` as the working naming system inside this project.
3. Never detach core controls such as button, bottom navigation, segment tab, stock row, payment method item.
4. Never replace stock logos with blank circles or random icons.
5. Never add light-theme surfaces, marketing hero patterns, or decorative gradients into app screens.
6. Never mix page-level spacing systems inside one screen.
7. Never create new colors, shadows, radii, or typography sizes unless the current token system cannot express the need and the change is explicitly approved.
8. Never describe a component with ad hoc property names when a Figma component API already exists in `tokens.json`.

## Task Routing

### If the task is page generation or page review

Read:

- `page-list.md`
- one file in `page-shells/`
- one file in `product-lines/`
- `docs/layout-and-component-specs.md`

### If the task is component generation or component review

Read:

- `components.md`
- `tokens.json`
- `docs/layout-and-component-specs.md`
- relevant case study in `case-studies/`

### If the task is prototype or implementation output

Read:

- `tokens.json`
- `design-tokens.css`
- `component-variables.css`
- `components.md`

### If the task is onboarding, team sync, or collaboration governance

Read:

- `INSTALL.md`
- `GLOSSARY.md`
- `CHANGELOG.md`

## Deliverable Standard

The output should satisfy all of the following:

- uses current component names and state names
- uses current spacing, radius, and color tokens
- matches the existing mobile-dark stock trading visual language
- can be understood by product managers, designers, and engineers without translation loss
- is reusable in future screens instead of solving only one local frame

## File Map

### Meta

- `SKILL.md`: entry, routing, hard rules
- `CHANGELOG.md`: version history for governance updates
- `GLOSSARY.md`: shared terminology
- `INSTALL.md`: onboarding and adoption guide

### Assets

- `tokens.json`: structured token source of truth
- `design-tokens.css`: CSS token export for prototypes and code-facing usage
- `component-variables.css`: legacy-compatible variable export including component variables
- `page-shells/`: reusable page composition skeletons
- `product-lines/`: business-domain overlays

### References

- `components.md`: component rules and APIs
- `page-list.md`: page rules and module composition
- `docs/layout-and-component-specs.md`: detailed measurement specs
- `case-studies/`: real failure patterns and review examples

## Self Check

Before final output, verify:

- Is the page still `375px` mobile-first?
- Did I reuse the correct component instead of drawing a detached copy?
- Are all colors and radii coming from the existing token system?
- Are positive and negative data colors semantically correct?
- Are button, tab, and navigation states complete?
- Are local icons and stock logos preserved?
- Does the page structure match one of the approved page shells?
- Can a PM and a designer both understand the output without extra explanation?
