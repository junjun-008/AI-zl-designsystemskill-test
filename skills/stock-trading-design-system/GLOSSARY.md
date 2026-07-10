# Glossary

## Core Terms

### Design System

The complete rule set for tokens, components, page structures, and documentation that keeps new output aligned with the existing Stock Trading app.

### Token

A named design value such as color, spacing, radius, stroke, size, typography, or effect. In this skill, `tokens.json` is the structured source.

### Semantic Token

A product-facing token name that explains usage, not raw value. Example: `color/text/positive`.

### Primitive Token

A raw value bucket used to build semantics. Example: `primitive.color.neutral.900`.

### Component

A reusable UI element with a stable API, such as `Primary Button` or `Stock List Item`.

### Pattern Component

A larger reusable business block built from smaller components, such as `Watchlist` or `Payment Method List`.

### Page Shell

A reusable page composition skeleton that defines module order, spacing rhythm, and navigation structure.

### Product Line Overlay

A business-domain-specific layer that adjusts copy, modules, and emphasis without inventing a new visual language.

## Naming Terms

### Role-Based Typography

The approved naming system for text styles:

- `Display`
- `Headline`
- `Title`
- `Body`
- `Label`

Do not use `H1 / H2 / body1 / body2` as the working naming language in this project.

### Density

The compactness mode of a component. Example: `Stock List Item` supports `Default` and `Compact`.

### State

The interaction or semantic mode of a component, such as:

- `Default`
- `Pressed`
- `Focus`
- `Disabled`
- `Selected`
- `Positive`
- `Negative`

### Instance Swap

A Figma component property that allows a nested component such as an icon or stock logo to be swapped without detaching the parent component.

## Page Terms

### Aktivitas

Portfolio and recent activity screen. Focuses on balance summary, quick actions, watchlist, and bottom navigation.

### Trending

Market discovery screen. Focuses on tabs, trend cards, market filters, and dense stock lists.

### Detail Saham

Stock detail screen. Focuses on price context, key stats, market movement, and action entry points.

### Top Up Flow

The three-step funding flow:

1. amount entry
2. payment selection
3. completion or confirmation

## Visual Language Terms

### App Background

The main dark canvas color, usually `color/bg/app`.

### Elevated Surface

A denser or more separated surface layer, usually `color/bg/elevated`.

### Glass Surface

A translucent card-like layer used in the current app language, usually `color/bg/surface`.

### Section Card

A grouped module with:

- `12px` radius
- `20px` padding
- `1px` border
- dark translucent or solid surface fill

### Positive Movement

Price or data increase. Uses green semantic tokens.

### Negative Movement

Price or data decline. Uses red semantic tokens.

## Governance Terms

### Source Of Truth

The file that should be trusted first for a specific category:

- structured values: `tokens.json`
- CSS variables: `design-tokens.css`
- component APIs: `tokens.json` plus `components.md`
- page composition: `page-list.md` plus `page-shells/`

### Detached Frame Debt

The design debt created when a screen copies a component visually instead of reusing the actual component instance.

### Logo Integrity

The rule that stock list rows and market cards must preserve the correct local logo component instead of falling back to generic placeholders.
