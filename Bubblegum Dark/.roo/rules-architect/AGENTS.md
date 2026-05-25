# Architect Mode Rules (Non-Obvious Only)

## Architectural Constraint: Bootstrap Variable Subversion

The fundamental architecture of this theme is a **deliberate deception of Bootstrap's SCSS variable system**. All "light" variables are mapped to dark values so that Bootstrap's generated utility classes and components render dark without requiring markup changes in phpMyAdmin core.

This means:
- **You cannot add a new Bootstrap component** without first overriding its relevant color/background variables in [`scss/_variables.scss`](scss/_variables.scss:1). Import order is critical — variable overrides must come before `@import "../../bootstrap/scss/bootstrap"` in [`scss/theme.scss`](scss/theme.scss:2).
- **Any Bootstrap utility class** (`.bg-*`, `.text-*`, `.border-*`) in phpMyAdmin core HTML will render with the theme's dark variable values, NOT Bootstrap's defaults. This is intentional and must be preserved.
- **Hardcoded colors in core phpMyAdmin CSS** that load after this theme WILL break the dark appearance. The theme cannot fix these — they must be reported upstream.

## Component Coupling
- [`scss/_variables.scss`](scss/_variables.scss:1) is the single source of truth for ALL colors. Every other partial (`_buttons.scss`, `_tables.scss`, `_navigation.scss`, etc.) depends on it.
- Variables from `_variables.scss` use both Bootstrap variables (`$primary`, `$body-bg`) and phpMyAdmin-specific variables (`$navi-background`, `$bg-one`, `$th-background`). Both groups must be maintained.
- [`scss/_common.scss`](scss/_common.scss:1) is the largest partial (~2900 lines) and handles most of phpMyAdmin's non-Bootstrap UI elements. It hardcodes some colors directly (e.g., `#5a9aaa` for links) rather than using variables — these are intentionally NOT variable-driven to ensure they work regardless of Bootstrap variable changes.

## Constraints
- **No build pipeline** — SCSS is compiled externally. Do not add package.json, webpack, or any build tooling. This is a phpMyAdmin theme that must work as a drop-in folder.
- **No JavaScript** — themes cannot include JS. All interactivity comes from phpMyAdmin core scripts.
- **Bootstrap version is locked** — the theme imports Bootstrap from `../../bootstrap/scss/` which is phpMyAdmin's bundled Bootstrap 5.x. Do not upgrade Bootstrap independently.
- **phpMyAdmin version support** — declared in [`theme.json`](theme.json:7) as ["5.0", "5.1", "5.2"]. New features must remain compatible with these versions.