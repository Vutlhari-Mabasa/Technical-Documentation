
# 📘 Project Documentation: Technical Documentation Page

## 📄 Project Overview

This project is a **responsive technical documentation webpage** built using HTML and CSS. This project was created on FreeCodeCamp, this was the project I submitted to get 
certification on the website for Responsive Web Design. It includes:

* A **fixed vertical navigation bar** on larger screens.
* A **main content area** divided into five informative sections: *Introduction*, *Getting Started*, *Syntax*, *Examples*, and *Best Practices*.
* Responsive design that adapts to mobile and smaller screens.

---

## 🌐 HTML Structure (`index.html`)

### 1. `<!DOCTYPE html>` and `<html lang="en">`

Defines the document type and the primary language of the page.

---

### 2. `<head>`

Contains metadata and links to external resources:

* `<meta charset="UTF-8">`: Sets the character encoding.
* `<meta name="viewport" content="width=device-width, initial-scale=1.0">`: Enables responsive scaling on different screen sizes.
* `<title>`: Sets the browser tab title.
* `<link rel="stylesheet" href="styles.css" />`: Links the external stylesheet.

---

### 3. `<body>`

Contains the visible content, divided into:

#### A. **Navigation Bar** (`<nav id="navbar">`)

* `<header>`: The title of the navbar.
* Five `<a class="nav-link">`: Navigation links pointing to each section via their `id` attributes.

#### B. **Main Content Area** (`<main id="main-doc">`)

Includes five `<section class="main-section">`, each with:

* A `<header>`: Section title.
* Paragraphs `<p>`: Explanatory text.
* Code blocks `<code>`: Highlight example code.
* Unordered lists `<ul><li>`: Key takeaways or bullet points.

Each section is uniquely identified by its `id` (e.g., `#Introduction`, `#Syntax`).

---

## 🎨 CSS Styling (`styles.css`)

### 1. **Global Styles**

```css
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
```

* Applies consistent box sizing and resets margins/paddings for all elements.

---

### 2. **Body**

```css
body {
  font-family: Arial, sans-serif;
  display: flex;
  background: #f0f0f0;
  line-height: 1.6;
}
```

* Uses a clean, readable font.
* Applies a light gray background.
* Makes the body a flex container for horizontal layout (nav + main-doc).
* Sets line height for better readability.

---

### 3. **Navbar (`#navbar`)**

```css
#navbar {
  position: fixed;
  top: 0;
  left: 0;
  width: 250px;
  height: 100%;
  background-color: #1e293b;
  color: white;
  padding: 1rem;
  overflow-y: auto;
}
```

* Fixed to the left of the screen.
* Full vertical height.
* Dark blue background with white text.
* Scrollable if the content exceeds viewport height.

#### Navbar Header

```css
#navbar header {
  font-size: 1.5rem;
  margin-bottom: 1rem;
}
```

* Increases font size and adds spacing below the title.

#### Navigation Links

```css
.nav-link {
  display: block;
  color: white;
  text-decoration: none;
  margin: 0.5rem 0;
  padding: 0.5rem;
  transition: background 0.3s;
}

.nav-link:hover {
  background-color: #334155;
}
```

* Displayed as block elements for full clickable area.
* Hover effect changes background to a darker blue.

---

### 4. **Main Content (`#main-doc`)**

```css
#main-doc {
  margin-left: 270px;
  padding: 2rem;
  flex-grow: 1;
}
```

* Leaves space for the fixed navbar.
* Adds internal padding.
* Grows to fill remaining horizontal space in the `flex` layout.

---

### 5. **Sections (`.main-section`)**

```css
.main-section {
  margin-bottom: 3rem;
}
```

* Adds spacing between sections for visual separation.

#### Section Headers

```css
.main-section header {
  font-size: 1.8rem;
  margin-bottom: 1rem;
  color: #1e293b;
}
```

* Dark blue headings to stand out.
* Spacing for clear readability.

---

### 6. **Code Blocks**

```css
code {
  background-color: #e2e8f0;
  padding: 0.3rem 0.6rem;
  display: block;
  margin: 0.5rem 0;
  border-left: 3px solid #0ea5e9;
}
```

* Light gray background with left blue border for visual emphasis.
* Makes code block-like with internal spacing and separation from text.

---

### 7. **Lists**

```css
ul {
  margin-left: 1.5rem;
  list-style-type: disc;
}

li {
  margin-bottom: 0.5rem;
}
```

* Uses bullet points.
* Adds spacing between list items for readability.

---

### 8. **Responsive Design (Media Query)**

```css
@media (max-width: 768px) {
  #navbar {
    position: relative;
    width: 100%;
    height: auto;
  }

  #main-doc {
    margin-left: 0;
  }

  .nav-link {
    padding: 1rem 0;
  }
}
```

* On smaller screens (≤768px):

  * Navbar becomes horizontal and non-fixed.
  * Main content adjusts margin.
  * Navigation links become vertically spaced for tap-friendliness.

---

## ✅ Features Summary

| Feature                    | Description                                                 |
| -------------------------- | ----------------------------------------------------------- |
| **Fixed Navbar**           | Remains visible on desktop for quick access.                |
| **Smooth Code Formatting** | Syntax is shown using styled `<code>` blocks.               |
| **Responsive Design**      | Works on both desktop and mobile views.                     |
| **Semantic HTML**          | Uses semantic tags for accessibility and SEO.               |
| **Clear Structure**        | Each section is clearly separated with headers and styling. |


