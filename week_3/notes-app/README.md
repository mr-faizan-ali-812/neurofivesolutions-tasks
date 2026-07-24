# Zenote — Slate & Emerald Minimalist Notes App

A premium, lightweight, local-first notes application built using vanilla web technologies. It combines high-end modern minimalist styling with rich user interactions, enabling users to capture thoughts instantly.

---

## 🎨 Theme & Visual Design

The application features a tailored **Slate & Emerald Minimalist Theme**:
* **Background:** Deep rich space-slate (`#090D16`) with an immersive radial gradient glow (`#151F32`).
* **Accent Accents:** Vivid emerald green (`#10B981`) for primaries, inputs, and successful actions; electric cyan (`#06B6D4`) for supporting highlights.
* **Typography:** Premium modern font pairings:
  * **Headings & Logo:** [Plus Jakarta Sans](https://fonts.google.com/specimen/Plus+Jakarta+Sans) (bold, geometric, clean).
  * **Body Copy:** [Inter](https://fonts.google.com/specimen/Inter) (highly readable).
  * **Metadata & Code:** [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) (clean monospace formatting).
* **Interactions:** Elegant elevational transitions (`translateY(-4px)` with custom cubic-bezier timing), thin high-contrast borders, and glowing focus rings instead of traditional retro tape/pins.

---

## ✨ Features

1. **Local-First Data Persistence:** Automatically reads and writes notes to the browser's `localStorage` namespace. Includes fallback session indicators if storage access is restricted.
2. **Instant Search Filtering:** Filters the grid collection in real time on every keystroke by scanning titles and body text.
3. **Responsive Grid Layout:** Standard grid with `minmax` layout adapters that seamlessly morph from mobile lists to multi-column desktop grids.
4. **Inline Edit Mode:** Form overlays swap inline to allow quick title/content editing without opening distracting modal popups.
5. **Delete Confirmation Safety:** Built-in two-step confirm delete indicator ("sure?") to prevent accidental note loss.
6. **Input Field Validation:** Checks for empty states and highlights erroneous fields with neon coral indicators and error messages.

---

## 🛠️ Technical Implementation

### File Structure
* [notes-app.html](file:///d:/neurofive/neurofivesolutions-tasks/week_3/notes-app/notes-app.html): Single-page app containing structures, design patterns, and application state controllers.

### Core Technologies
* **Structure:** HTML5 Semantic Elements (`<header>`, `<form>`, `<textarea>`, `<article>`).
* **Styling:** CSS3 variables, CSS Grid, custom transitions, viewport styling.
* **Logic:** Vanilla Javascript (ES6) handling state binding, state updates, relative timestamp intervals, and localStorage parsing.

---

## 🚀 Running Locally

No installation, build steps, or local servers are required:
1. Double-click [notes-app.html](file:///d:/neurofive/neurofivesolutions-tasks/week_3/notes-app/notes-app.html) or open it using any modern web browser (Chrome, Safari, Edge, Firefox).
2. Start adding, searching, and managing your personal notes board immediately.
