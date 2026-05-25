# AGENTS.md

This file provides guidance to agents when working with code in this repository.

## Project Context
This is a **phpMyAdmin theme** ("Bubblegum Dark"), not a standalone application. There are **no build scripts, package.json, tests, or linter configs**. SCSS is compiled externally via the Live Sass Compiler VSCode extension (or any Dart Sass compiler).

## Compilation
- Entry point: [`scss/theme.scss`](scss/theme.scss:1) — compiles to [`css/theme.css`](css/theme.css:1) and [`css/theme.rtl.css`](css/theme.rtl.css)
- Uses **Dart Sass** (`@use "sass:string"` syntax) — not Node Sass
- Imports Bootstrap 5 SCSS from `../../bootstrap/scss/` (phpMyAdmin's bundled Bootstrap)
- RTL output is generated as a separate compilation pass

## Critical Variable Overrides (Non-Obvious)
The theme achieves a dark look by **deliberately lying to Bootstrap** about light color values in [`scss/_variables.scss`](scss/_variables.scss:1):

- **`$white: #f5edf2`** and **`$gray-100` through `$gray-900`** are mapped to dark navy/charcoal tones, NOT actual whites/grays. This neutralizes Bootstrap utility classes like `.bg-white`, `.text-white`, `.bg-light` so they render dark instead of bright.
- **`$min-contrast-ratio: 4`** is lowered from Bootstrap's default (4.5) because the "white" text color is actually an off-white (`#f5edf2`), and `color-contrast()` would otherwise fail to pick light text on colored buttons (success green, danger red).
- **`$enable-transitions: false`** — transitions are disabled globally for performance in the phpMyAdmin admin interface.
- **`$light: #283848`** — the `.bg-light` class renders as a dark navy, not a light gray.

## Theme Metadata
- [`theme.json`](theme.json:1) defines supported phpMyAdmin versions (5.0–5.2), name, and author
- [`theme.md`](theme.md:1) is a **Tailwind CSS design token file** — it is NOT compiled into the theme and exists as a separate design system reference (contains `@theme inline` blocks and oklch() color values)

## File Organization
- `scss/_*.scss` — SCSS partials (one per component: buttons, nav, tables, etc.)
- `css/` — compiled output; never edit directly
- `img/` — theme icons (mostly PNGs used by phpMyAdmin's icon system)
- `jquery/` — jQuery UI theme overrides