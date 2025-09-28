# 📜 History of CSS

## 1. Before CSS (Early 1990s)

- HTML was used only for structure (headings, paragraphs, tables).
- No separation of content and design.
- Developers used HTML attributes like `bgcolor`, `font`, `align`, and even **tables** for layout.
- Websites became heavy and hard to maintain.

---

## 2. The Birth of CSS (1994–1996)

- **1994** → Håkon Wium Lie (working with Tim Berners-Lee at CERN) proposed **Cascading Style Sheets**.
- **1996** → The first official **CSS1** specification was released by **W3C**.
- CSS1 introduced:
  - Fonts, colors, text alignment, margins, borders.
  - The “cascading” concept: styles could come from multiple sources (browser, user, author).

---

## 3. CSS2 (1998)

- Added more advanced features:
  - Positioning (absolute, relative, fixed).
  - `z-index` for layering.
  - Media types (screen, print).
- Browser support was inconsistent (Internet Explorer vs. Netscape issues).

---

## 4. The Long Gap & CSS2.1 (2004–2011)

- Many CSS2 features lacked full support.
- **CSS2.1** was introduced as a stable version:
  - Fixed bugs.
  - Removed poorly supported features.
- Developers used hacks and **CSS reset stylesheets** for cross-browser consistency.

---

## 5. CSS3 (2005–2012)

- CSS3 became **modularized** (split into modules: Flexbox, Grid, Transforms, etc.).
- Key innovations:
  - `border-radius` (rounded corners).
  - `box-shadow`, `text-shadow` (shadows).
  - Gradients.
  - Transitions & Animations.
  - Media Queries → **responsive design**.
  - Flexbox & Grid → modern layouts.

---

## 6. Modern CSS (2015–Today)

- **CSS Grid (2017)** → true 2D layout system.
- **CSS Variables (custom properties)** → reusable styling.
- New tools: `subgrid`, `clamp()`, `minmax()`, `aspect-ratio`.
- **CSS Houdini (experimental)** → extend CSS capabilities.
- Evergreen browsers (Chrome, Firefox, Safari, Edge) now update frequently → consistent support.

---

## ✅ Why CSS Changed the Web

- Separated **content (HTML)** from **presentation (CSS)**.
- Made websites easier to **design, maintain, and scale**.
- Enabled **responsive, mobile-friendly, visually rich** designs.
- Allowed developers to shape the **modern web**.

---

# CSS – The 5W Explanation

## ❓ What is CSS?

- **CSS (Cascading Style Sheets)** is a stylesheet language used to describe how HTML elements should look.
- It controls the **layout, colors, fonts, spacing, and overall presentation** of a webpage.

---

## ❓ Why CSS?

- To separate **content (HTML)** from **presentation (design)**.
- Makes websites **easier to design, update, and maintain**.
- Provides **consistency** across multiple pages.
- Enables **responsive design** (works on mobile, tablet, desktop).
- Eliminates the need for inline styles and table-based layouts.

---

## ❓ When was CSS created?

- **1994** → Proposed by **Håkon Wium Lie**.
- **1996** → First official specification **CSS1** released by **W3C**.
- **1998** → CSS2 introduced (advanced layouts, positioning).
- **2005–2012** → CSS3 modularized (Flexbox, Grid, Animations).
- **2017 onwards** → Modern CSS with Grid, variables, and new functions.

---

## ❓ Where is CSS used?

- **Websites** → styling HTML pages.
- **Web applications** → making UIs interactive and user-friendly.
- **Mobile apps (with frameworks)** → React Native, Ionic use CSS-like styling.
- **Printed documents** → CSS has print stylesheets (`@media print`).

---

## ❓ How does CSS work?

1. A **browser** loads HTML.
2. The **CSS rules** (inline, internal, external) are applied.
3. If multiple rules apply, the **cascade** decides priority:
   - Inline CSS > Internal CSS > External CSS > Browser defaults.
4. The final **rendered design** is displayed to the user.

---

# CSS Basics Notes

## 1. What is CSS?

**CSS (Cascading Style Sheets)** is the language we use to style and
design web pages. If HTML is the skeleton (structure) of a webpage, CSS
is the skin, clothes, and decorations that make it look nice.

- **Cascading** → Means that rules are applied in a certain order. If
  two styles conflict, the browser decides which one has higher
  priority.
- **Style Sheets** → A sheet (or file) full of style rules that can be
  applied to many HTML pages.

👉 **Real-Life Example:** Think of an online resume: HTML gives the
basic text like "Education, Skills, Projects." CSS decides the font,
colors, spacing, and how attractive it looks.

---

## 2. Why Do We Use CSS?

- **To make websites beautiful:** Add colors, fonts, backgrounds.
- **To control layout:** Arrange text, images, and sections.
- **To save time:** One CSS file can style multiple HTML pages.
- **For responsive design:** Adjusts look for mobile, tablet, and
  desktop.
- **For better user experience:** Helps people enjoy using the
  website.

Without CSS, every website would look like plain black-and-white text.

---

## 3. Types of CSS

### 3.1 Inline CSS

Written directly inside an HTML tag using the `style` attribute.

```html
<p style="color: red; font-size: 20px;">This is inline styled text.</p>
```

✅ Quick and easy for one element. ❌ Becomes messy in big projects.

---

### 3.2 Internal CSS

Written inside `<style>` tags in the `<head>` of an HTML file.

```html
<head>
  <style>
    h1 {
      color: blue;
      text-align: center;
    }
  </style>
</head>
```

✅ Useful for single-page projects. ❌ Cannot be reused across multiple
pages.

---

### 3.3 External CSS

Written in a separate `.css` file and linked to HTML.

```html
<!-- In HTML -->
<link rel="stylesheet" href="styles.css" />
```

```css
/* In styles.css */
p {
  color: green;
  font-size: 18px;
}
```

✅ Best method for large projects. ✅ Reusable and clean.

👉 **Real-Life Example:** Think of a school dress code. One rulebook
(external CSS) applies to all students (HTML pages).

---

## 4. How to Link External CSS

Use `<link>` tag inside `<head>`:

```html
<head>
  <link rel="stylesheet" href="style.css" />
</head>
```

- `rel="stylesheet"` → Tells browser it's a stylesheet.
- `href` → Path of CSS file.

---

## 5. How CSS Works: Selector and Rules

### Syntax:

```css
selector {
  property: value;
}
```

👉 Example:

```css
p {
  color: red;
  font-size: 20px;
}
```

- `p` → selector (chooses `<p>` elements).
- `color`, `font-size` → properties.
- `red`, `20px` → values.

---

## 6. Selecting Elements in CSS

### 6.1 Universal Selector

Applies to everything.

```css
* {
  margin: 0;
  padding: 0;
}
```

### 6.2 Tag Selector

Applies to specific HTML tags.

```css
h1 {
  color: blue;
}
```

### 6.3 Class Selector

Applies to elements with a `class` attribute.

```css
.highlight {
  color: green;
  font-weight: bold;
}
```

```html
<p class="highlight">This is highlighted text.</p>
```

### 6.4 ID Selector

Applies to element with unique `id`.

```css
#special {
  color: red;
}
```

```html
<p id="special">This is special text.</p>
```

👉 **Rule of Thumb:**

- Use **class** when you want to reuse styles.
- Use **id** only for unique elements.

---

## 7. CSS Text and Color Properties

### 7.1 `color`

Sets text color.

```css
p {
  color: purple;
}
```

### 7.2 `background-color`

Sets background.

```css
div {
  background-color: yellow;
}
```

### 7.3 `font-size`

Controls text size.

```css
h1 {
  font-size: 40px;
}
```

### 7.4 `font-family`

Defines the font.

```css
p {
  font-family: Arial, sans-serif;
}
```

👉 Always use a **fallback font** like `sans-serif` in case the first
font isn't available.

### 7.5 `font-weight`

Controls boldness.

```css
h2 {
  font-weight: bold;
}
```

### 7.6 `font-style`

Italic or normal text.

```css
p {
  font-style: italic;
}
```

### 7.7 `text-align`

Aligns text.

```css
h1 {
  text-align: center;
}
```

### 7.8 `text-transform`

Controls text case.

```css
p {
  text-transform: uppercase;
}
```

👉 "hello world" → "HELLO WORLD"

---

## 8. Working with Fonts

### 8.1 Google Fonts

- Go to [Google Fonts](https://fonts.google.com).
- Choose a font and copy the link tag.

```html
<link
  href="https://fonts.googleapis.com/css2?family=Poppins&display=swap"
  rel="stylesheet"
/>
```

- Apply in CSS:

```css
body {
  font-family: "Poppins", sans-serif;
}
```

### 8.2 Download Fonts from a Website

- Right-click → Inspect → Computed Styles → check font-family.
- Download from sites like **dafont.com** or **fontsquirrel.com**.

### 8.3 Using `@font-face`

If you have a font file in your project:

```css
@font-face {
  font-family: "MyFont";
  src: url("MyFont.woff2") format("woff2");
}

p {
  font-family: "MyFont", sans-serif;
}
```

---

## 9. ID vs Class in CSS

```html
<p id="unique">This uses ID</p>
<p class="note">This uses Class</p>
<p class="note">Another element with same Class</p>
```

```css
#unique {
  color: red;
}

.note {
  color: green;
}
```

- **ID** → used for one unique element.
- **Class** → can be reused many times.

---

## 10. Div in CSS

The `<div>` tag is a **container**. By default, it does nothing
visually, but with CSS, we can make sections, boxes, or layouts.

Example: A colored rectangle

```html
<div class="box"></div>
```

```css
.box {
  width: 200px;
  height: 100px;
  background-color: lightblue;
  border: 2px solid blue;
}
```

👉 **Real-Life Example:** Think of `<div>` as a cardboard box. On its
own, it's just empty. With CSS, you can paint it, resize it, and place
it wherever you want.

---

## Summary

- CSS styles HTML and makes web pages attractive.
- Three ways to use CSS: inline, internal, and external (best).
- CSS selects elements with tags, classes, or IDs.
- Text properties control color, fonts, size, and alignment.
- We can import and apply custom fonts.
- Divs are containers that can be shaped with CSS.

---
