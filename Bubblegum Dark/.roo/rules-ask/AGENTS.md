# Ask Mode Rules (Non-Obvious Only)

## Counterintuitive File Purposes

### [`theme.md`](theme.md:1) is NOT Documentation
Despite the `.md` extension, this file is a **Tailwind CSS design token file** — not markdown documentation. It contains `@import "tailwindcss"`, `@theme inline` blocks, and `oklch()` color values. It exists as a design system reference for the Tailwind ecosystem and is **not compiled into the theme**. The actual theme uses Bootstrap SCSS, not Tailwind.

### Navigation Frame Variables
The theme uses phpMyAdmin's specific SCSS variables for the navigation sidebar:
- `$navi-width` — fixed nav sidebar width (240px)
- `$navi-color` / `$navi-background` — nav text/background
- `$navi-pointer-color` / `$navi-pointer-background` — selected item highlight

These are NOT Bootstrap variables — they're phpMyAdmin-specific and used throughout [`scss/_navigation.scss`](scss/_navigation.scss:1).

### Table Styling Variables
phpMyAdmin has its own table variable system separate from Bootstrap's:
- `$th-background` / `$th-color` — table header styles
- `$bg-one` / `$bg-two` — alternating row backgrounds
- `$browse-pointer-color` / `$browse-pointer-background` — hover state
- `$browse-marker-color` / `$browse-marker-background` — row selection marker

### Two Separate Icon Systems
- `img/` contains PNG icons used by phpMyAdmin's built-in icon system (e.g., `b_edit.png`, `s_cog.png`)
- [`scss/_icons.scss`](scss/_icons.scss:1) provides icon-specific CSS overrides
- `jquery/` contains jQuery UI theme assets — a completely separate icon/image set for jQuery UI widgets (datepicker, dialogs, etc.)