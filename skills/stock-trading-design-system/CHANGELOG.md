# Changelog

## 2026.07.13

### Added

- added `assets/icons/common-icons/icon-sprite.svg` with 24 reusable app icons
- added `assets/icons/icon-map.json` as the machine-readable icon registry
- wired the current HTML prototype to use inline Sprite references instead of page-specific common SVG paths

### Clarified

- CSS controls icon size, color, and state; SVG stores icon geometry; JSON maps IDs to assets
- special page icons may be temporary, but approved common icons must be reused

## 2026.07.10

### Added

- added `assets/icon-index.json` as the first semantic icon/logo usage index
- covered navigation, actions, watchlist, portfolio, monitoring, trigger, market, payment, and stock logo scenarios
- added Chinese names and meanings for icon review

### Changed

- updated `SKILL.md` routing so icon/logo-related work loads `assets/icon-index.json`
- strengthened rules against generic or visually similar but semantically wrong icons

## 2026.05.18

### Added

- expanded the skill from a lightweight token pack into a collaboration-grade design-system skill
- rewrote `SKILL.md` with routing, hard rules, and self-check logic
- added `GLOSSARY.md`, `INSTALL.md`, `components.md`, and `page-list.md`
- added `design-tokens.css` as a code-facing token entry file
- added `page-shells/` for reusable page composition patterns
- added `product-lines/` for business-domain guidance
- added `case-studies/` to capture common breakages and recovery rules

### Clarified

- formalized the canonical page list from the Figma source file
- formalized the role-based typography naming system
- clarified that this skill serves PM, design, and engineering collaboration together

### Notes

- `tokens.json` remains the structured token source of truth
- `component-variables.css` remains valid and is retained for backwards compatibility
