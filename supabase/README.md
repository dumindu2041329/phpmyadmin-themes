# 🟢 Supabase — phpMyAdmin Theme

> **Sleek. Dark. Developer-first.** A phpMyAdmin theme inspired by the iconic Supabase design system — clean, modern, and built for developers who care about their tools.

---

## 🎨 About the Theme

**Supabase** is a custom phpMyAdmin theme that faithfully recreates the look and feel of the [Supabase](https://supabase.com/) platform UI. If you love working with Supabase, now your database manager can match that same polished, dark aesthetic.

The theme brings:

- 🌑 **Deep charcoal backgrounds** — Easy on the eyes during long dev sessions
- 🟢 **Vibrant Supabase green accents** — The signature `#3ECF8E` green used throughout
- 🔤 **Outfit font** — Clean, modern sans-serif typography for a polished feel
- 🔲 **Soft rounded corners** — `0.5rem` radius for a refined, contemporary look
- ✨ **Subtle depth** — Layered dark surfaces that create visual hierarchy without noise

---

## ✨ Features

| Feature | Description |
|---|---|
| 🌙 **Full Dark Mode** | Deep charcoal base with layered dark surfaces |
| 🟢 **Supabase Green Accents** | Signature `#3ECF8E` highlights on interactive elements |
| 🖋️ **Outfit Font** | Modern Google Font for clean, developer-friendly typography |
| 🗂️ **Styled Tables** | Alternating row shading with green hover highlights |
| 🔘 **Custom Buttons** | Rounded buttons with Supabase green fills and smooth transitions |
| 🧭 **Redesigned Navigation** | Dark sidebar and top-nav matching the Supabase dashboard feel |
| 📋 **Forms & Inputs** | Rounded inputs with green focus rings |
| 🏷️ **Badges & Tags** | Soft pill-style labels with muted backgrounds |
| ⚡ **Lightweight** | No external runtime dependencies — pure CSS |

---

## 🖼️ Preview

![Supabase Theme Preview](screen.png)

---

## 🛠️ Design Tokens

| Property | Value |
|---|---|
| 🎨 **Background** | `#1C1C1C` (deep charcoal) |
| 🟢 **Accent / Primary** | `#3ECF8E` (Supabase green) |
| 📝 **Text Primary** | `#EDEDED` |
| 📝 **Text Muted** | `#8C8C8C` |
| 🔲 **Border Radius** | `0.5rem` |
| 🖋️ **Font Family** | `Outfit, sans-serif` |
| 📦 **phpMyAdmin Support** | `5.0` · `5.1` · `5.2` |

---

## 🚀 Installation

### 📦 Prerequisites

- phpMyAdmin **5.0**, **5.1**, or **5.2**
- A local or hosted server environment (XAMPP, MAMP, WAMP, Laragon, etc.)

---

### 🪟 XAMPP (Windows / macOS / Linux)

1. Open your XAMPP installation directory:
   - **Windows:** `C:\xampp\phpMyAdmin\themes\`
   - **macOS/Linux:** `/opt/lampp/phpmyadmin/themes/`
2. Copy the `supabase` folder into the `themes` directory.
3. Open your browser and navigate to `http://localhost/phpmyadmin`.
4. Go to **Settings → Themes** and select **Supabase**. 🎉

---

### 🍎 MAMP (macOS / Windows)

1. Locate your MAMP phpMyAdmin themes folder:
   - **macOS:** `/Applications/MAMP/bin/phpMyAdmin/themes/`
   - **Windows:** `C:\MAMP\bin\phpMyAdmin\themes\`
2. Copy the `supabase` folder into the `themes` directory.
3. Open `http://localhost:8888/phpmyadmin` in your browser.
4. Go to **Settings → Themes** and select **Supabase**. 🎉

---

### 🟢 WAMP (Windows)

1. Navigate to your WAMP phpMyAdmin themes folder:
   - `C:\wamp64\apps\phpmyadmin<version>\themes\`
2. Copy the `supabase` folder into the `themes` directory.
3. Open `http://localhost/phpmyadmin` in your browser.
4. Go to **Settings → Themes** and select **Supabase**. 🎉

---

### 🐧 Linux (Manual Installation)

1. Find your phpMyAdmin themes directory:
   ```bash
   find / -name "themes" -path "*/phpmyadmin/*" 2>/dev/null
   ```
2. Copy the theme folder:
   ```bash
   sudo cp -r supabase /usr/share/phpmyadmin/themes/
   ```
3. Open phpMyAdmin and go to **Settings → Themes** → select **Supabase**. 🎉

---

## �️ Compatibility

| phpMyAdmin Version | Supported |
|---|---|
| 5.0.x | ✅ Yes |
| 5.1.x | ✅ Yes |
| 5.2.x | ✅ Yes |
| 4.x and below | ❌ No |

---

## 🎭 Design Philosophy

The Supabase design system is loved by developers for its balance of **clarity, elegance, and function**. This theme brings those same principles to phpMyAdmin:

- 🌑 **Dark-first** — Designed from the ground up for dark environments
- 🟢 **Green as a signal** — Accent color used purposefully to guide attention
- 🔤 **Typography matters** — The Outfit font keeps things modern and legible
- 🧘 **Calm UI** — Low-noise design so you can focus on your data, not the interface
- 🔲 **Consistently rounded** — Soft corners throughout for a cohesive feel

---

## 📁 File Structure

```
supabase/
├── css/
│   └── theme.css       # Compiled theme stylesheet
├── img/                # Theme images and icons
├── scss/               # Source SCSS files
│   ├── _variables.scss # Theme color tokens & variables
│   └── ...             # Component stylesheets
├── screen.png          # Theme preview screenshot
├── theme.json          # phpMyAdmin theme metadata
└── README.md           # You are here 📍
```

---

## 🤝 Contributing

Want to improve the theme or report a bug? Contributions are welcome!

1. 🍴 Fork the repository
2. 🌿 Create a feature branch
3. 💾 Commit your changes
4. 📬 Open a Pull Request

---

## 📜 License

This theme is open-source and available under the **MIT License**.

---

<div align="center">

Made with 🟢 and a love for green accents.

**[⬆ Back to Top](#-supabase--phpmyadmin-theme)**

</div>