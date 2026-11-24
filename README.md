# ☕ Brew Bliss Café - Modern & Responsive Café Website

A premium, modern, and fully responsive coffee shop website crafted exclusively using **HTML5 and CSS3** (no JavaScript, no external CSS frameworks like Bootstrap or Tailwind). Designed with professional UI/UX standards, warm coffee aesthetics, and tailored for B.Tech Web Development practical examinations, lab assignments, and project submissions.

---

## 📁 1. Project Folder Structure

```text
HTML -Cafe/
│
├── index.html        # Complete semantic HTML5 structure for all 9 sections
├── style.css         # Modern pure CSS3 stylesheet with CSS Grid, Flexbox, & Media Queries
└── README.md         # Comprehensive documentation, setup instructions, & code explanation
```

---

## 🚀 2. Instructions to Run the Website in VS Code

You can run and test this project in Visual Studio Code using any of the following methods:

### Method 1: Using Live Server Extension (Recommended)
1. Open **Visual Studio Code**.
2. Go to the **Extensions view** (`Ctrl + Shift + X`).
3. Search for **Live Server** (by Ritwick Dey) and click **Install**.
4. Open the project folder in VS Code: `File -> Open Folder... -> select HTML -Cafe`.
5. Open `index.html`.
6. Right-click anywhere in the editor and select **"Open with Live Server"** (or click **"Go Live"** in the bottom status bar).
7. The website will automatically launch in your default web browser at `http://127.0.0.1:5500/index.html`.

### Method 2: Direct Browser Execution (No Extension Needed)
1. Navigate to the project folder `c:\Users\DELL\Documents\HTML -Cafe` in your file explorer.
2. Double-click on `index.html`.
3. It will immediately open in Google Chrome, Microsoft Edge, Brave, or Mozilla Firefox.

---

## 🎨 3. Key Website Sections & Features

| # | Section | Details & Implementation |
|---|---|---|
| **1** | **Navigation Bar** | Sticky header with `backdrop-filter: blur()`, brand logo with coffee mug icon, smooth scroll links (`#home`, `#about`, `#menu`, `#specials`, `#reviews`, `#hours`, `#contact`), table reservation CTA, and a **pure CSS mobile hamburger menu toggle** (using the checkbox hack). |
| **2** | **Hero Section** | Fullscreen moody coffee shop backdrop with dual-color linear overlay, "100% Ethically Sourced" pill badge, large heading *"Welcome to Brew Bliss Café"*, subtitle *"Where Every Sip Tells a Story"*, call-to-action buttons, and an interactive 4-card feature ribbon (Freshly Roasted, Artisan Bakery, Cozy Ambiance, Work & Chill). |
| **3** | **About Our Café** | Two-column responsive layout. Left: High-resolution barista coffee photo with an overlapping floating badge (*8+ Years of Craftsmanship*). Right: Café story, atmosphere details, and 3 value cards (*Supreme Quality*, *Inviting Ambiance*, *Fresh Daily Bakes*). |
| **4** | **Our Menu** | Responsive CSS Grid featuring the 6 required items: **Espresso**, **Cappuccino**, **Café Latte**, **Cold Coffee**, **Chocolate Brownie**, and **Croissant**. Each card includes high-definition images, category tags (Hot Brew, Chilled, Bakery), 5-star ratings, pricing, descriptions, serving details, and order buttons. |
| **5** | **Chef's Specials** | 4 signature gourmet creations (*Hazelnut Praline Mocha*, *Spanish Vanilla Iced Latte*, *Belgian Truffle Brownie Royale*, *Almond Frangipane Croissant*). Enhanced with a golden **"Chef's Recommendation"** badge, calories/meta tags, and high-impact dark roast glassmorphism styling. |
| **6** | **Customer Reviews** | 3 authentic testimonial cards featuring guest avatars, names, professional designations, 5-star rating stars, authentic quotes praising the coffee and ambiance, and decorative quotation mark watermarks. |
| **7** | **Opening Hours** | Premium schedule container showing Weekdays (*Mon–Fri: 8:00 AM – 10:00 PM*) and Weekends (*Sat–Sun: 9:00 AM – 11:00 PM*), a pulsing green "Open Today & Brewing Fresh" status pill, and a Happy Hour banner with 20% discount details. |
| **8** | **Location & Contact** | Left: Full physical address, phone numbers, email, and a stylized map placeholder with a pulsing pin indicator and directions link. Right: Complete Table Reservation & Contact form with floating labels, guest selector, date & time slots, and message textarea. |
| **9** | **Footer & Back to Top** | 4-column comprehensive footer: Brand summary, Social media icons (Instagram, Facebook, X, Pinterest), Quick links, Favorites menu, and Newsletter subscription bar. Includes a floating circular "Back to Top" button linked to `#home`. |

---

## 💡 4. Important HTML5 & CSS3 Concepts Explained

### A. Semantic HTML5 Elements
- `<header>`: Represents the site header containing branding and top-level navigation.
- `<nav>`: Wraps navigation links for search engine crawlers and screen readers.
- `<section>`: Divides the page into distinct thematic areas (Hero, About, Menu, Specials, Reviews, Hours, Contact).
- `<article>`: Self-contained cards for menu items, specials, and reviews.
- `<footer>`: Structural container for copyright, secondary navigation, social links, and legal notice.

### B. Pure CSS Responsive Hamburger Menu (No JavaScript!)
```html
<input type="checkbox" id="nav-toggle" class="nav-toggle">
<label for="nav-toggle" class="nav-toggle-label">
  <span class="hamburger-bar"></span>
  <span class="hamburger-bar"></span>
  <span class="hamburger-bar"></span>
</label>
```
```css
/* Controlled entirely via the CSS :checked pseudo-class and sibling combinators */
.nav-toggle:checked ~ .nav-menu {
  left: 0;
}
```

### C. Modern CSS Layouts (Flexbox & CSS Grid)
- **CSS Grid** (`display: grid`): Used for menu cards, specials, reviews, and footer columns:
  ```css
  grid-template-columns: repeat(3, 1fr);
  gap: 32px;
  ```
- **Flexbox** (`display: flex`): Used for navigation alignment, card rows, icon-text pairings, and buttons:
  ```css
  display: flex;
  align-items: center;
  justify-content: space-between;
  ```

### D. CSS Custom Properties (Variables)
All theme colors, fonts, shadows, and transitions are managed through `:root` variables:
```css
:root {
  --color-espresso-dark: #1F110B;
  --color-chocolate: #2C1810;
  --color-coffee-medium: #6F4E37;
  --color-caramel: #C58940;
  --color-cream: #FAF7F2;
  --color-beige: #F3EDE2;
}
```

### E. Smooth Scrolling & Sticky Navbar Offset
```css
html {
  scroll-behavior: smooth;
  scroll-padding-top: var(--header-height); /* Prevents sticky header from obscuring section headings */
}
```

### F. Responsive Media Queries
Breakpoints configured at **1024px** (laptops/tablets), **768px** (mobile tablets), and **480px** (smartphones) ensure fluid responsiveness across all screen sizes.

---

## 🎓 5. B.Tech Practical / Viva Q&A Tips
1. **Why use semantic HTML5 elements?**
   - *Answer:* They improve website accessibility (for assistive screen readers), provide cleaner document outlines, and enhance SEO ranking.
2. **How does the mobile menu work without JavaScript?**
   - *Answer:* It uses a hidden HTML checkbox (`<input type="checkbox">`) and `<label>`. When the user clicks the label, the checkbox is toggled. In CSS, the `:checked` pseudo-class with the general sibling selector (`~`) shows the navigation drawer.
3. **What is the advantage of CSS variables (`:root`)?**
   - *Answer:* It centralizes styling rules, eliminates duplicate color codes, enables effortless theme switching (like dark/light mode), and improves code maintainability.
