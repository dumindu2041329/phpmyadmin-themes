# Code Mode Rules (Non-Obvious Only)

## SCSS Variable Lying Pattern
When adding new component styles, NEVER use actual light/bright color values. The entire Bootstrap variable system has been subverted in [`scss/_variables.scss`](scss/_variables.scss:1):
- `$white`, `$gray-*`, and `$light` are all mapped to dark navy tones
- Any hardcoded hex value like `#fff` or `#ffffff` will produce bright white and break the dark theme
- Always reference existing SCSS variables (`$body-color`, `$bg-one`, `$navi-background`, etc.) rather than hardcoding colors

## Bootstrap Import Chain
The theme imports Bootstrap 5 SCSS directly from `../../bootstrap/scss/bootstrap` (phpMyAdmin's bundled copy). This means [`scss/_variables.scss`](scss/_variables.scss:1) must define ALL Bootstrap variables BEFORE the `@import "../../bootstrap/scss/bootstrap"` line in [`scss/theme.scss`](scss/theme.scss:2). Variable order matters — Bootstrap's `!default` flag means our overrides only work if declared first.

## Compiled Files
- Never edit [`css/theme.css`](css/theme.css:1) or [`css/theme.rtl.css`](css/theme.rtl.css) directly — they are compiled output
- The RTL file uses identical SCSS source compiled with an RTL flag by the Sass compiler

## Dart Sass Only
Uses `@use "sass:string"` syntax — do NOT use Node Sass (`node-sass`) which doesn't support this module system. The `string.quote()` function in [`scss/_variables.scss`](scss/_variables.scss:187) for `$breadcrumb-divider` requires Dart Sass.

## No Build System
There is no package.json, no npm scripts, no webpack/vite config. SCSS compilation is done externally via the Live Sass Compiler VSCode extension or manual `sass` CLI. Do not add build tooling — this is by design for phpMyAdmin theme distribution.