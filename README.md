# GemCommerce — Technical Task Submission  
Author: Krishna V V     
 Live Link : [https://krishnavisweswaran.github.io/gemcommerce/](https://krishnavisweswaran.github.io/gemcommerce/)  
 Repository : [https://github.com/krishnavisweswaran/gemcommerce](https://github.com/krishnavisweswaran/gemcommerce)

---

## 🧠 Overview
This project is a **static responsive section** built as part of the **GemCommerce Technical Test**.  
It showcases a clean, modern layout using **HTML and CSS only**, focused on structure, alignment, and visual hierarchy.

The section is lightweight, fast-loading, and compatible across all major browsers.

---

## 🛠️ Built With
- **HTML5** – for semantic structure and accessibility  
- **CSS3** – for styling, layout, and responsiveness  
- **GitHub Pages** – for hosting and live deployment

No JavaScript or frameworks were required for this task.


## 📁 Folder Structure
```plaintext
gemcommerce/
├─ images/          # Contains all the image assets used in the page
├─ index.html       # Main HTML file
├─ style.css        # Styling file for the layout and responsiveness
└─ README.md        # Project documentation

```
## 📂 Key Files and Their Roles

### 1. `index.html`
- Acts as the **main entry point** of the website.  
- Structured using semantic elements like `<header>`, `<section>`, `<div>`, and `<footer>`.  
- Divided into logical parts such as:
  - Hero / Introduction
  - Feature or Product highlight section
  - Footer with social or contact info
- Each content block uses class names linked to `style.css` for styling.

### 2. `style.css`
- Handles **typography**, **colors**, **grid layout**, and **spacing**.  
- Mobile-first design: ensures the layout adapts gracefully to different screen sizes.  
- Uses **Flexbox and CSS Grid** for clean alignment and responsiveness.  
- Includes hover effects and spacing utilities for better visual balance.

### 3. `images/`
- Stores all the static assets (icons, product visuals, banners).  
- Images are optimized for faster page loading.

---

## ⚙️ How to Run Locally
To view or modify the project on your computer:

1. Clone this repository:
   ```bash
   git clone https://github.com/krishnavisweswaran/gemcommerce.git
   cd gemcommerce
    ```
   ## ♿ Accessibility & SEO Considerations
- Used semantic HTML for better accessibility.
- Optimized heading hierarchy (H1 → H2 → H3).
- Included responsive meta viewport for mobile scaling.
- Lightweight structure ensures fast loading.

  ---

## 💬 Code Explanation (detailed)

### Structure (HTML)
- The document is a single-page static layout (no JavaScript). It uses semantic HTML with multiple `<section>` elements to separate page areas:
  - `.hero-section` — top marketing/hero area with feature items, product image and CTA.
  - `.nutrition-section` — stats and supporting text with an image.
  - `.benefits-section` (and `.benefits-section.alt`) — two benefit blocks with alternating image/text layouts.

- Key container elements and classes used:
  - `.features-container` — 3-column layout grouping `.features-left`, `.center-image-container`, `.features-right`.
  - `.feature-item` — repeated pattern for each feature: `.feature-icon` + `.feature-content`.
  - `.center-image-container` + `.product-bowl` + `.bowl-image` — central hero image with a vertical timeline overlay (implemented via a `::before` pseudo-element).
  - CTA area: `.cta-container` with `.cta-button` and `.cta-footer` (guarantee + `.payment-methods` icons).

- Example HTML snippet (hero feature pattern):
  ```html
  <div class="feature-item">
    <div class="feature-icon bg-green">
      <img src="images/realfood.png" alt="Real Food icon">
    </div>
    <div class="feature-content">
      <h3 class="feature-title">Real Food</h3>
      <p class="feature-description">Wholesome recipes for dogs with real meat and veggies.</p>
    </div>
  </div>

  Layout & styling (CSS)

### Mobile-first approach

- Base CSS defines typography, spacing, and stacked/mobile behaviors.  
- Breakpoints (`@media`) at **768px**, **1024px**, and **1200px** adapt the layout from mobile → tablet → desktop, switching to multi-column or flex/grid styles.

### Key techniques used
- **Flexbox** — for horizontal alignment in `.features-container`, `.feature-item`, `.cta-footer`, `.payment-methods`, `.row`.  
- **Grid-like responsiveness** — achieved with flex rules and `max-width` constraints to mimic a 3-column layout (`.features-left`, `.center-image-container`, `.features-right`).  
- **Pseudo-element overlay** — `.center-image-container::before` draws a vertical timeline line centered over the bowl image.  
- **Responsive images** — global rule `img { max-width: 100%; height: auto; }` ensures safe scaling on all screens.  
- **Animations** — a single `@keyframes fadeIn` gives smooth entry to `.feature-item` and `.stat-item`.

### Example CSS snippets
```css
.features-container {
  display: flex;
  gap: 30px;
  align-items: center;
  justify-content: center;
  width: 100%;
  max-width: 1170px;
}

.center-image-container::before {
  content: '';
  position: absolute;
  left: 50%;
  top: 0;
  bottom: 0;
  width: 2px;
  background: linear-gradient(180deg, #EE6F4B 0%, #EE6F4B 100%);
  transform: translateX(-50%);
}
```
### 📱 Responsiveness & Breakpoints

- **Desktop (≥1024px):** Three-column hero layout with fixed-width sides and a centered image (`.features-left`, `.center-image-container`, `.features-right`).  
- **Tablet and below (≤1200px, ≤768px):** `.features-container` wraps into single-column blocks, while `.nutrition-content` and `.benefit-row` stack vertically.  
- **Small screens (≤480px):** Font sizes and icon sizes are reduced for better mobile readability.

---

### ♿ Accessibility & Semantics

- Images include `alt` attributes.  
- Headings follow a clear visual hierarchy (`<h1>`, `<h2>`, `<h3>`).  
- A `<main>` wrapper can be used around primary content for better structure.  
- The CTA button uses `type="button"` to prevent accidental form submission.  
- Interactive elements can include visible focus styles for keyboard users.  
- `aria-label` can be used for icon-only buttons to ensure accessibility.

---

### 💾 Data & Behavior

- The page is static — no APIs or dynamic content are used.  
- All images and icons are local and stored in the `images/` folder.  






