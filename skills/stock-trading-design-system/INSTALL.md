# Install And Adoption Guide

## Purpose

This skill is meant to be shared across product managers, designers, and engineers so that new requirements, prototypes, and implementation prompts stay aligned with the current Stock Trading design system.

## Recommended Folder

Put the full folder at:

```text
.codex/skills/stock-trading-design-system/
```

Keep the full structure intact. Do not copy only `SKILL.md`.

## Minimum Files To Keep In Sync

These files should always move together:

- `SKILL.md`
- `tokens.json`
- `design-tokens.css`
- `component-variables.css`
- `components.md`
- `page-list.md`

If only part of the pack is copied, routing and usage quality will drop.

## Team Usage

### Product Managers

Use this skill when:

- writing prototype requests
- describing new screens
- reviewing whether a proposal matches the current app language

Recommended reading:

1. `SKILL.md`
2. `page-list.md`
3. one file in `page-shells/`
4. one file in `product-lines/`

### Designers

Use this skill when:

- extending existing Figma pages
- creating new component states
- reviewing consistency across pages

Recommended reading:

1. `SKILL.md`
2. `components.md`
3. `docs/layout-and-component-specs.md`
4. `case-studies/common-breakages.md`

### Engineers

Use this skill when:

- building HTML/CSS prototypes
- implementing screens from design
- mapping component APIs to code props

Recommended reading:

1. `SKILL.md`
2. `tokens.json`
3. `design-tokens.css`
4. `component-variables.css`
5. `components.md`

## Update Protocol

When the Figma library changes:

1. update tokens first
2. update component API descriptions second
3. update page rules third
4. record the change in `CHANGELOG.md`

If a change affects naming, also update `GLOSSARY.md`.

## Review Protocol

Before shipping a new skill version:

- confirm the page list still matches the Figma file
- confirm core components still exist and keep the same names
- confirm token names still match the exported CSS variables
- confirm PM and designer readers can understand the docs without internal context

## Distribution Notes

If the team shares this skill through zip packages or internal knowledge bases, package the whole directory rather than individual files. The skill depends on cross-file routing.
