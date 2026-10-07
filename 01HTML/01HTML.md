# 01HTML - HTML5 Complete Guide & Reference

Welcome to the **01HTML** directory! This module serves as a comprehensive reference guide, cheat sheet, and learning repository for **HTML5 (HyperText Markup Language)**—the backbone of web development.

---

## 📌 Table of Contents
1. [Introduction to HTML5](#1-introduction-to-html5)
2. [Boilerplate & Basic Structure](#2-boilerplate--basic-structure)
3. [Text Formatting & Headings](#3-text-formatting--headings)
4. [Links, Images & Media](#4-links-images--media)
5. [Lists & Tables](#5-lists--tables)
6. [HTML5 Semantic Elements](#6-html5-semantic-elements)
7. [Forms & Input Validation](#7-forms--input-validation)
8. [Meta Tags & SEO Essentials](#8-meta-tags--seo-essentials)
9. [Best Practices](#9-best-practices)

---

## 1. Introduction to HTML5
HTML controls the structural layout and content representation of web applications.

* **Elements & Tags**: HTML uses tags enclosed in angle brackets (`<tagname>`). Most elements have an opening tag `<tag>` and a closing tag `</tag>`.
* **Void Elements**: Tags that do not have closing tags or inner text (e.g., `<img />`, `<br />`, `<hr />`, `<input />`).
* **Attributes**: Provide additional metadata or properties to elements (e.g., `id`, `class`, `src`, `href`, `alt`).

---

## 2. Boilerplate & Basic Structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML5 Reference Guide</title>
</head>
<body>
    <h1>Hello, World!</h1>
</body>
</html>
```

### Key Components:
* <!DOCTYPE html>!DOCTYPE html: Declares the document type and HTML version (HTML5).
* <html lang="en">html lang="en": Root element specifying language for accessibility and search engines.

* <head>head: Contains metadata, title, character encoding, and resource links.

* <body>body : Contains all renderable page content visible to the user.

## 3. Text Formatting & Headings
Headings
Headings organize the structure of your page (<h1> is highest priority, <h6> is lowest).
```
<h1>Main Title (Use once per page)</h1>
<h2>Section Header</h2>
<h3>Sub-section Header</h3>
```
### Text Formatting Tags
### HTML  
```
<p>This is a standard paragraph.</p>
<strong>Bold text (Strong importance)</strong>
<em>Italicized text (Emphasis)</em>
<mark>Highlighted text</mark>
<small>Small print text</small>
<del>Strikethrough / deleted text</del>
<ins>Inserted / underlined text</ins>
<sub>Subscript</sub> and <sup>Superscript</sup>
<blockquote>Block quotation for cited content</blockquote>
<code>inline code snippet</code>
<pre>Preformatted text that preserves spaces and line breaks</pre>
```
## 4. Links, Images & Media
### A. Hyperlinks (<a>)
```
<!-- External Link opening in a new tab -->
<a href="[https://github.com](https://github.com)" target="_blank" rel="noopener noreferrer">GitHub</a>

<!-- Relative Internal Link -->
<a href="./pages/about.html">About Us</a>

<!-- Anchor Link (Scroll to Section) -->
<a href="#section-1">Jump to Section 1</a>

<!-- Email / Telephone Links -->
<a href="mailto:example@email.com">Send Email</a>
<a href="tel:+1234567890">Call Support</a>
```
### B. Images (<img>)
Always include descriptive alt attributes for screen readers and fallback rendering.

```
<img src="assets/logo.png" alt="Company Logo" width="200" height="100" loading="lazy" />
```
### C. Audio & Video
```
<!-- Video Player -->
<video controls width="600" poster="thumbnail.jpg">
    <source src="video.mp4" type="video/mp4">
    <source src="video.webm" type="video/webm">
    Your browser does not support the video tag.
</video>
```
```
<!-- Audio Player -->

<audio controls autoplay muted>
    <source src="audio.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
</audio>
```
## 5. Lists & Tables
### Lists
```
<!-- Unordered List (Bullet Points) -->
<ul>
    <li>Item A</li>
    <li>Item B</li>
</ul>

<!-- Ordered List (Numbered) -->
<ol type="1">
    <li>First Step</li>
    <li>Second Step</li>
</ol>

<!-- Description / Definition List -->
<dl>
    <dt>HTML</dt>
    <dd>HyperText Markup Language</dd>
</dl>
```
### Tables
```
<table>
    <caption>User Data Table</caption>
    <thead>
        <tr>
            <th>ID</th>
            <th>Name</th>
            <th>Role</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>Abhishek</td>
            <td>Developer</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td colspan="3">Total Users: 1</td>
        </tr>
    </tfoot>
</table>
```
## 6. HTML5 Semantic Elements
Semantic HTML improves SEO, readability, and web accessibility (a11y) by giving structural meaning to web elements.
```
                                             +---------------------------------------------------+
                                             |                     <header>                      |
                                             +---------------------------------------------------+
                                             |                      <nav>                        |
                                             +---------------------------------------------------+
                                             |         <main>        |        <aside>            |
                                             |  +-----------------+  | (Sidebar, Info, Ads)      |
                                             |  |    <article>    |  |                           |
                                             |  |  +-----------+  |  |                           |
                                             |  |  | <section> |  |  |                           |
                                             |  |  +-----------+  |  |                           |
                                             |  +-----------------+  |                           |
                                             +---------------------------------------------------+
                                             |                     <footer>                      |
                                             +---------------------------------------------------+
```
### Core Semantic Tags:
. <header>: Page or section introductory header.

. <nav>: Navigation links container.

. <main>: Central, non-repeating content of the document.

. <section>: Standalone thematic grouping of content.

. <article>: Self-contained composition (blog post, news article, comment).

. <aside>: Tangentially related content (sidebar, callouts).

. <footer>: Footer containing copyright, contact info, or legal links.

. <figure> & <figcaption>: Encapsulates media alongside its caption.

## 7. Forms & Input Validation
Forms capture user input and communicate with backend scripts.
```
<form action="/api/submit" method="POST">
    <!-- Text Input -->
    <label for="username">Username:</label>
    <input type="text" id="username" name="username" placeholder="Enter username" required minlength="3">

    <!-- Email Input -->
    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>

    <!-- Password Input -->
    <label for="password">Password:</label>
    <input type="password" id="password" name="password" required minlength="8">

    <!-- Number Input -->
    <label for="age">Age:</label>
    <input type="number" id="age" name="age" min="18" max="99">

    <!-- Dropdown Select -->
    <label for="role">Role:</label>
    <select id="role" name="role">
        <option value="developer">Developer</option>
        <option value="designer">Designer</option>
    </select>

    <!-- Checkbox & Radio -->
    <input type="checkbox" id="terms" name="terms" required>
    <label for="terms">I accept the terms</label>

    <input type="radio" id="gender_m" name="gender" value="male">
    <label for="gender_m">Male</label>
    <input type="radio" id="gender_f" name="gender" value="female">
    <label for="gender_f">Female</label>

    <!-- Textarea -->
    <label for="bio">Bio:</label>
    <textarea id="bio" name="bio" rows="4" cols="50"></textarea>

    <!-- Submit Button -->
    <button type="submit">Submit Form</button>
</form>
```
## 8. Meta Tags & SEO Essentials
Place these inside the <head> section to optimize search engine ranking and social sharing cards.

```
<!-- Primary Meta Tags -->
<meta name="title" content="HTML5 Notes & Reference Guide">
<meta name="description" content="Complete HTML5 cheat sheet covering elements, forms, semantics, and best practices.">
<meta name="keywords" content="HTML, HTML5, Web Development, Frontend, Cheat Sheet">
<meta name="author" content="Abhishek Jaiswar">

<!-- Open Graph / Facebook / LinkedIn -->
<meta property="og:type" content="website">
<meta property="og:title" content="HTML5 Notes & Reference Guide">
<meta property="og:description" content="Complete HTML5 cheat sheet and reference guide.">
<meta property="og:image" content="[https://example.com/og-image.jpg](https://example.com/og-image.jpg)">

<!-- Twitter -->
<meta property="twitter:card" content="summary_large_image">
<meta property="twitter:title" content="HTML5 Notes & Reference Guide">
<meta property="twitter:description" content="Complete HTML5 cheat sheet and reference guide.">
```
## 9. Best Practices
### 1. Always use semantic elements over generic <div> and <span> tags whenever possible.

### 2. Ensure proper nesting: Close inner tags before closing outer tags.

### 3. Always supply the alt attribute for <img> tags.

### 4. Use lowercase for element names and attributes.

### 5. Keep standard file naming conventions: Use index.html for main entry points and hyphenated lower-case filenames (about-us.html).

### 6. Include viewport meta tag to guarantee proper responsive rendering across mobile and desktop devices.


#  NOTE:
## 01 HTML REVISION DONE ✅
