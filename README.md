# 🎨 phpMyAdmin Themes

> A collection of beautiful, handcrafted themes for **phpMyAdmin** — giving your database management interface a stunning modern look.

![Supported Versions](https://img.shields.io/badge/phpMyAdmin-5.0%20%7C%205.1%20%7C%205.2-blue?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)
![Author](https://img.shields.io/badge/author-Dumindu%20Damsara-orange?style=flat-square)

---

## ✨ Available Themes

### 🟢 Supabase Theme

Inspired by the iconic [Supabase](https://supabase.com/) design system — a sleek dark interface featuring deep charcoal backgrounds, vibrant green accents, and clean minimal typography powered by the **Outfit** font.

| Property | Details |
|---|---|
| 🎨 Color Palette | Dark charcoal + Supabase green |
| 🖋️ Font | Outfit, sans-serif |
| 🌙 Dark Mode | ✅ Fully supported |
| 🔲 Border Radius | 0.5rem (soft rounded corners) |
| 📦 phpMyAdmin Support | `5.0` · `5.1` · `5.2` |

**Preview:**

![Supabase Theme Preview](supabase/screen.png)

---

## ✅ Compatibility

All themes in this repository are fully compatible with:

| phpMyAdmin Version | Supported |
|---|---|
| 5.0.x | ✅ Yes |
| 5.1.x | ✅ Yes |
| 5.2.x | ✅ Yes |

> ⚠️ These themes are **not** compatible with phpMyAdmin 4.x or earlier.

---

## 🚀 Installation Guide

Follow the steps below to install a theme on your local PHP dev server.

### 📁 Step 1 — Download the Theme

Clone this repository or download the ZIP:

```bash
git clone https://github.com/dumindu2041329/phpmyadmin-themes.git
```

Or download directly as a ZIP from GitHub → **Code → Download ZIP**.

---

### 🖥️ XAMPP (Windows / macOS / Linux)

**Default phpMyAdmin path:**
```
C:\xampp\phpMyAdmin\            ← Windows
/Applications/XAMPP/phpMyAdmin/ ← macOS
/opt/lampp/phpmyadmin/          ← Linux
```

**Steps:**

1. Open your XAMPP phpMyAdmin directory.
2. Navigate to the `themes/` folder:
   ```
   C:\xampp\phpMyAdmin\themes\
   ```
3. Copy the theme folder (e.g. `supabase/`) into `themes/`:
   ```
   C:\xampp\phpMyAdmin\themes\supabase\
   ```
4. Start XAMPP and open phpMyAdmin in your browser: [http://localhost/phpmyadmin](http://localhost/phpmyadmin)
5. Go to **Appearance Settings** (bottom-left panel or top menu).
6. Select **supabase** from the **Theme** dropdown, then click **Go**. 🎉

---

### 🍎 MAMP (macOS / Windows)

**Default phpMyAdmin path:**
```
/Applications/MAMP/bin/php/phpMyAdmin/  ← macOS
C:\MAMP\bin\phpMyAdmin\                 ← Windows
```

**Steps:**

1. Open your MAMP phpMyAdmin directory.
2. Navigate to the `themes/` folder:
   ```
   /Applications/MAMP/bin/php/phpMyAdmin/themes/
   ```
3. Copy the theme folder (e.g. `supabase/`) into `themes/`.
4. Start MAMP and open phpMyAdmin via the MAMP start page.
5. Go to **Appearance Settings**.
6. Select **supabase** from the **Theme** dropdown, then click **Go**. 🎉

---

### 🟦 WAMP (Windows)

**Default phpMyAdmin path:**
```
C:\wamp64\apps\phpmyadmin5.x.x\
```

**Steps:**

1. Open your WAMP phpMyAdmin directory.
2. Navigate to the `themes/` folder:
   ```
   C:\wamp64\apps\phpmyadmin5.x.x\themes\
   ```
3. Copy the theme folder (e.g. `supabase/`) into `themes/`:
   ```
   C:\wamp64\apps\phpmyadmin5.x.x\themes\supabase\
   ```
4. Start WAMP (ensure the system tray icon is green 🟢).
5. Open phpMyAdmin: [http://localhost/phpmyadmin](http://localhost/phpmyadmin)
6. Go to **Appearance Settings**.
7. Select **supabase** from the **Theme** dropdown, then click **Go**. 🎉

---

## 🛠️ Changing the Theme in phpMyAdmin

Once the theme folder is placed in the `themes/` directory:

1. Open phpMyAdmin in your browser.
2. Look for the **Appearance settings** panel on the **left sidebar** or in the **top navigation**.
3. Under **Theme**, choose your desired theme from the dropdown list.
4. Click **Go** or **Apply** — the theme will be applied instantly! ✨

> 💡 **Tip:** If the theme doesn't appear, make sure the theme folder contains a valid `theme.json` file and a `css/` folder.

---

## 📂 Theme Structure

Each theme follows the standard phpMyAdmin theme structure:

```
theme-name/
├── css/            # Compiled CSS stylesheets
├── img/            # Theme images & icons
├── jquery/         # jQuery UI theme styles
├── scss/           # Source SCSS files
├── screen.png      # Theme preview screenshot
└── theme.json      # Theme metadata (name, version, author, supported versions)
```

---

## 👤 Author

**Dumindu Damsara**

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

> 💬 *If you find these themes useful, consider giving the repo a ⭐ on GitHub!*