# Debug Mode Rules (Non-Obvious Only)

## Common Dark Theme Debugging Gotchas

### Unexpected Bright Elements
If a UI element appears bright white/light in the dark theme, the root cause is almost always one of:
1. The Bootstrap utility class `.bg-white`, `.text-white`, `.border-white`, or `.bg-light` is being used — these render as dark Navy because `$white` and `$light` were deliberately remapped, BUT any hardcoded inline `style="background: #fff"` or `color: white` will NOT be caught
2. A hardcoded hex value (e.g., `#ffffff`, `#fff`) was used instead of a SCSS variable — grep for bare hex values in partials
3. A new Bootstrap component was imported but its variables weren't overridden in [`scss/_variables.scss`](scss/_variables.scss:1)

### Contrast Ratio Issues
If `color-contrast()` isn't picking light text on colored buttons (success green, danger red), check that `$min-contrast-ratio` is set to `4` (not Bootstrap's default `4.5`). The off-white `$white: #f5edf2` doesn't meet the 4.5 threshold against mid-tone backgrounds.

### CSS Specificity Conflicts
phpMyAdmin core CSS loads AFTER theme CSS. If theme styles aren't applying, the phpMyAdmin default stylesheet may be overriding them with higher specificity. Use browser DevTools to check which stylesheet wins — you may need `!important` or higher-specificity selectors.

### RTL Output
RTL styles compile from the exact same SCSS but with `/* rtl:begin:remove */` and `/* rtl:end:remove */` directive comments stripped by the RTL compiler pass. If RTL looks wrong, check for LTR-specific rules that should be wrapped in these comments (see [`scss/_common.scss`](scss/_common.scss:356-362) for examples).

### Compiled Output Verification
The compiled [`css/theme.css`](css/theme.css:1) is ~15,000 lines. Quick sanity checks:
- Line 15: `--bs-white: #f5edf2;` (NOT `#fff`)
- Line 16: `--bs-gray: #8a9aaa;` (NOT a real gray)
- Line 18: `--bs-gray-100: #2c3c4c;` (should be dark, not light)