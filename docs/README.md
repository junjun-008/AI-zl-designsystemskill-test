# Project Docs

This directory stores working product documents for this project.

Use this structure going forward.

## Structure

### `templates/`

Reusable document templates that are not tied to one page or one feature.

Current files:

- `feishu-prd-template.md`: generic Feishu-friendly PRD template

### `my-page/`

Working documents for the `我的 / Profile` page.

Current files:

- `prd-v1.md`: formal PRD for internal review
- `page-plan-v1.md`: page plan used before prototype or Figma generation

## Recommended Conventions

When adding a new page, create a dedicated folder:

```text
docs/
  <page-or-feature-name>/
    prd-v1.md
    page-plan-v1.md
    prototype-notes-v1.md
```

When adding a shared template, place it under:

```text
docs/templates/
```

## Document Roles

- `prd-*.md`: explains why the page or feature exists, what is in scope, and how it should be accepted
- `page-plan-*.md`: translates the PRD into page structure, module order, and component reuse strategy
- `prototype-notes-*.md`: records prototype behavior, transitions, and implementation notes if needed
- `templates/*.md`: reusable team templates

## Suggested Workflow

1. Create or update PRD
2. Create or update page plan
3. Generate prototype or Figma screen
4. If the page changes materially, sync back to PRD or page plan
