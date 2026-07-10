# Layout And Component Specs

This file contains concrete measurements for designing Stock Trading app screens and documenting the design system. Use it with `tokens.json` and `component-variables.css`.

## Page Grid

| Item | Value | Token / Note |
|---|---:|---|
| Mobile screen width | 375px | `size/screen/mobile-width` |
| Default horizontal page margin | 20px | Use on left and right |
| Default content width | 343px | 375px - 40px |
| Wide content width | 360px | Edge-aware modules only |
| Top safe area | 24px+ | Device dependent |
| Major section vertical gap | 16px | Use between stacked modules |
| Screen background | `#12121C` | `color/bg/app` |

## Card And Section Anatomy

| Item | Value | Token / Note |
|---|---:|---|
| Card fill | `rgba(37, 36, 50, 0.4)` | `color/bg/surface` |
| Solid fallback fill | `#252432` | Use in documentation/export when transparency is unclear |
| Card border | 1px | `stroke/hairline` |
| Card border color | `#3A3A47` | `color/border/default` |
| Accent border | `#7FDF9A` | `color/border/accent` |
| Card radius | 12px | `radius/xl` |
| Default card padding | 20px | Use for business modules |
| Compact card padding | 16px | Use for dense component demos |
| Card internal gap | 16px | Main vertical rhythm |
| Header title-to-caption gap | 6-8px | Keep section headers compact |
| Card-to-card vertical gap | 16px | Default screen rhythm |

## Controls

| Component | Value | Note |
|---|---:|---|
| Primary button large height | 48px | Main CTA |
| Primary button medium height | 40px | Compact action |
| Button horizontal padding | 16px | Default |
| Button icon/text gap | 8px | Default |
| Button radius | 6px | `radius/md` |
| Icon button size | 40px | 24px icon inside |
| Segment tab height | 28px | Filter tabs |
| Amount chip height | 40px | 2-column preset grid |
| Input field height | 44-56px | Depends on state and context |
| Payment method row height | 56px | Selectable row |
| Payment method radius | 6px | `radius/md` |
| Bottom navigation height | 68px | Fixed bottom area |
| Minimum touch target | 40px | Do not go below this in prototypes |

## Market Lists And Data Cards

| Component Part | Value | Note |
|---|---:|---|
| Stock row default height | 56px | `Stock List Item / Density=Default` |
| Stock row compact height | 44px | `Stock List Item / Density=Compact` |
| Stock logo size | 24px | Use local logo component |
| Logo-to-text gap | 12px | Default row gap |
| Ticker text | 16px / 19px | Body large, semi-bold |
| Company text | 12px / 14px | Body small |
| Price text | 16px / 19px | Right aligned |
| Change text | 12px / 14px | Positive or negative color |
| Market card width | 100px | Compact carousel card |
| Market card height | 98px | Compact carousel card |
| Market card radius | 6px | `radius/md` |

## Typography Roles

Use Material-style role names instead of H1/H2 labels. Choose type by product role.

| Role | Size / Line Height / Weight | Use |
|---|---|---|
| Display Medium | 36px / 42px / 600 | Portfolio balance and major numeric focus |
| Headline Small | 24px / 28px / 600 | Screen titles or major module headings |
| Title Large | 22px / 26px / 600 | App bar title and section title |
| Body Large | 16px / 19px / 400-600 | Ticker, key values, emphasized row content |
| Body Medium | 14px / 16px / 400 | Forms, buttons, regular row content |
| Body Small | 12px / 14px / 400 | Secondary information, company name |
| Label Medium | 11px / 12px / 500 | Compact labels |
| Label Small | 10px / 12px / 500 | Navigation labels and dense metadata |

Rules:

- Letter spacing is always `0`.
- Do not scale font size with viewport width.
- Use positive/negative colors only for market movement, active state, success, error, or decline data.
- Keep labels short enough for 375px mobile width.

## Screen Composition Rules

1. Start every mobile screen from 375px width and 20px side margins.
2. Use 343px content width for primary modules.
3. Use section cards with 20px padding and 12px radius for grouped content.
4. Use 16px vertical rhythm between major modules.
5. Use reusable component states instead of duplicating detached frames.
6. Use `Stock List Item` for quote rows and watchlists.
7. Use `Market Trend Card` for compact horizontal market cards.
8. Use `Payment Method Item` for selectable funding methods.
9. Use `Amount Chip` for preset amount selection.
10. Use one primary CTA per screen or task section.
11. Do not introduce marketing hero layouts inside app screens.
12. Do not add new button styles without design-system approval.
