# 🎨 LinkedIn Post — phpMyAdmin Themes

---

🚀 **Just shipped something fun — open-source custom themes for phpMyAdmin!**

If you've ever stared at the default phpMyAdmin interface and thought *"this could really use a glow-up"* — this one's for you. 😄

I built and published a collection of handcrafted themes for phpMyAdmin that transform the look of your database management interface into something you'll actually enjoy using. 💾✨

---

🖌️ **Themes available:**

⚡ **NeoBrutalism** — Bold. Raw. Unapologetic. Thick borders, flat colors, and hard shadows inspired by the Neo-Brutalism design trend.

🟢 **Supabase** — A sleek dark theme inspired by the Supabase UI. Clean greens, deep backgrounds, and a modern developer aesthetic.

---

🛠️ **Tech stack:**
- Pure **SCSS** with CSS custom properties for theming
- Follows the official **phpMyAdmin theme structure**
- Compatible with **phpMyAdmin 5.0, 5.1 & 5.2**
- Works on **XAMPP**, **MAMP**, and **WAMP**

---

🎨 **SCSS → CSS compilation:**

The themes are written in **SCSS** and compiled down to plain CSS. Here's the workflow I used:

**Option A — Dart Sass (recommended):**

```bash
# Install globally
npm install -g sass

# Compile once
sass scss/theme.scss css/theme.css

# Watch mode (auto-recompile on save 🔥)
sass --watch scss/theme.scss:css/theme.css
```

**Option B — VS Code (zero terminal):**
- Install extension: **Live Sass Compiler**
- Set output to `css/theme.css`, source to `scss/theme.scss`
- Hit Save → it auto-compiles ✅

---

📦 **Installation is super easy:**

1. Clone the repo or download the ZIP
2. Drop your chosen theme folder into phpMyAdmin's `themes/` directory
3. Select it from **Appearance Settings** in phpMyAdmin → done! 🎉

---

🌟 If you work with PHP on a local dev server and use phpMyAdmin daily, give your workflow a fresh coat of paint!

🔗 GitHub → github.com/dumindu2041329/phpmyadmin-themes

⭐ A star on the repo would mean the world — and feel free to open issues or PRs if you'd like to contribute a theme!

---

#OpenSource #PHP #phpMyAdmin #WebDevelopment #SCSS #CSS #DeveloperTools #NeoBrutalism #Supabase #SideProject #Programming #Frontend
