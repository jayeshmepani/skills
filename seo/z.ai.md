Here is the consolidated, comprehensive reference document based on your file. No information has been removed; it has been formatted into a professional technical standard for readability and reference.

---

# Modern Web Development Reference: HTML, CSS, JS, SEO, & Accessibility

**Date:** March 02, 2026
**Scope:** Practical rules and examples for SEO, Accessibility, Semantics, and Performance.

---

## 1. High‑Level Mental Model

Modern front‑end development consists of three aligned stacks. Success requires keeping these three in sync.

```mermaid
mindmap
  root((Modern Web))
    SEO & Semantics
      "Semantic HTML (section, article, nav...)"
      "Meta tags & JSON-LD"
      "Core Web Vitals"
    Accessibility
      "WCAG contrast & color"
      "ARIA (only when needed)"
      "Keyboard & focus"
    Performance
      "Resource hints (preload/prefetch/preconnect)"
      "Lazy loading & responsive images"
      "Modern codecs (WebP/AVIF, AV1/VP9)"
      "Observer APIs"
```

---

## 2. Obsolete HTML Elements & Attributes

### 2.1 Obsolete Elements (Do Not Use)
These elements are non-conforming. They are either purely presentational or have been replaced by better alternatives.

*   **Presentational:**
    *   `<center>`, `<font>`, `<basefont>`, `<big>`, `<strike>`, `<u>` (Avoid `<u>` for styling; acceptable only for unarticulated annotations).
    *   `<blink>`, `<marquee>` → **Alternative:** Use CSS animations.
*   **Layout / Frames:**
    *   `<frame>`, `<frameset>`, `<noframes>` → **Alternative:** Use `<iframe>` and CSS Grid/Flexbox.
*   **Legacy Interactive / Media:**
    *   `<applet>` → **Alternative:** Use `<embed>` or `<object>`.
    *   `<bgsound>` → **Alternative:** Use `<audio>`.
*   **Miscellaneous:**
    *   `<acronym>` → **Alternative:** Use `<abbr>`.
    *   `<keygen>` → **Alternative:** Web Crypto API.

**Rule of thumb:** If an element exists only to change appearance or is tied to legacy plugins, it is obsolete.

### 2.2 Obsolete Presentational Attributes
HTML is for structure; CSS is for presentation. Do not use the following attributes:

*   `align`, `valign` → Use CSS `text-align`, `vertical-align`, `align-items`.
*   `bgcolor` → Use CSS `background-color`.
*   `border`, `cellpadding`, `cellspacing` (on tables) → Use CSS borders and padding.
*   `width`/`height` (on presentational elements like `<hr>`) → Use CSS.
*   `hspace`, `vspace` (on images/objects) → Use CSS margin.

### 2.3 Script & Link Obsolete Attributes
*   **`<script>`:**
    *   `language`: **Obsolete.** Omit it.
    *   `charset`: **Obsolete.** Set encoding via `<meta charset="utf-8">`.
*   **`<a>`:**
    *   `name`: **Obsolete** for fragment identifiers.
    *   **Bad:** `<a name="section5"></a>`
    *   **Good:** `<h2 id="section5">Section 5</h2>` (Link with `href="#section5"`).

### 2.4 Obsolete but "Conforming" (Discouraged)
*   `border="0"` on `<img>` → Use CSS `border: none`.
*   Legacy table attributes → Use CSS.

---

## 3. Semantic HTML, Landmarks, and ARIA

### 3.1 Landmark Elements & Implied Roles
HTML sectioning elements create "Landmarks" for assistive technology navigation.

| Element | Implied Landmark Role | Typical Usage |
| :--- | :--- | :--- |
| `<header>` | `banner` | Site header (logo, global tools). *Note: Does not map to banner if inside article/section.* |
| `<nav>` | `navigation` | Major navigation blocks. |
| `<main>` | `main` | Primary content. *Only one per page.* |
| `<footer>` | `contentinfo` | Footer info (copyright, links). *Note: Must be in body context.* |
| `<aside>` | `complementary` | Sidebars, tangentially related content. |
| `<section>` | `region` (if labeled) | Generic thematic grouping. |

**Rule:** Use native HTML elements first. Add ARIA roles only if HTML is insufficient.

### 3.2 Semantic Element Usage Guide
*   **`<header>`:** Site banner. Do not use as a generic "top of section" unless it is semantically a header.
*   **`<nav>`:** For major blocks (Main menu, TOC, Breadcrumbs). Use `<ul>`/`<ol>` inside.
*   **`<main>`:** The primary content. Exclude sidebars/footers.
*   **`<section>`:** Generic grouping with a heading. Use when `<article>` or `<aside>` doesn't fit.
*   **`<article>`:** Self-contained composition (Blog post, widget, news). Must be independently distributable (e.g., RSS).
*   **`<aside>`:** Content tangentially related (Sidebar, "Read also").
*   **`<footer>>`:** Copyright, contact info.
*   **`<a>` vs `<button>`:**
    *   `<a>`: Navigation (URL change, anchors).
    *   `<button>`: Actions (Submit, Modal, Toggle). **Do not** put `role="button"` on an `<a>`.

### 3.3 The First Rule of ARIA
> "If a native HTML element or attribute has the semantics and behavior you require, use it instead of re-purposing an element and adding an ARIA role, state or property."

**Common Patterns:**
*   Use `aria-label` / `aria-labelledby` to label landmarks (e.g., `<nav aria-label="Main">`).
*   Use `aria-current="page"` for the active link in a navigation list.
*   Use `aria-describedby` for form help text.

---

## 4. Accessibility (WCAG, Contrast, Keyboard)

### 4.1 Contrast Ratios
**Relative Luminance (L):** `0.2126 * R + 0.7152 * G + 0.0722 * B` (Linearized).
**Contrast Ratio (CR):** `(L1 + 0.05) / (L2 + 0.05)`.

**WCAG 2.1 Level AA Requirements:**
*   **Normal Text:** ≥ **4.5:1**
*   **Large Text:** ≥ **3:1** (≥18pt regular or ≥14pt bold).
*   **UI Components:** ≥ **3:1** (Buttons, inputs, icons).

**WCAG 2.2 Note:** Focus indicators must have ≥ 3:1 contrast against adjacent colors.

### 4.2 Keyboard & Focus
*   **Reachability:** All interactive elements must be keyboard accessible.
*   **Tabindex:**
    *   Use `tabindex="0"` to make non-interactive elements focusable (only if necessary).
    *   **Avoid** `tabindex > 0`. Manage focus via DOM order.
*   **Focus Indicator:** Must be visible (Outline/Color change). Satisfies WCAG 2.4.7.

### 4.3 Forms
*   Always link labels: `<label for="email">Email</label><input id="email">`.
*   Group related fields with `<fieldset>` and `<legend>`.

---

## 5. SEO & Meta Tags

### 5.1 Essential `<head>` Structure
```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8"> <!-- Required -->
  <title>Page Title | Brand</title>
  <meta name="viewport" content="width=device-width, initial-scale=1"> <!-- Critical for Mobile -->
  <meta name="description" content="Concise summary (approx 155-160 chars).">
  <meta name="theme-color" content="#ffffff">
  <link rel="canonical" href="https://example.com/this-page"> <!-- Prevent duplicate content -->
</head>
```

### 5.2 JSON-LD & Structured Data
Google recommends JSON-LD in the `<head>` or body.

**Organization Example:**
```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "Example Company",
  "url": "https://example.com/",
  "logo": "https://example.com/logo.png"
}
</script>
```

**Breadcrumb Example:**
```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "Books", "item": "https://example.com/books" },
    { "@type": "ListItem", "position": 2, "name": "Sci-Fi", "item": "https://example.com/books/scifi" }
  ]
}
</script>
```

---

## 6. Media Formats & Optimization

### 6.1 Image Formats
*   **JPEG:** Photos (legacy).
*   **PNG:** Transparency/Sharp edges.
*   **WebP:** Better compression than JPEG/PNG.
*   **AVIF:** Best compression efficiency.

**Strategy:** Use `<picture>` for fallback.
```html
<picture>
  <source srcset="photo.avif" type="image/avif">
  <source srcset="photo.webp" type="image/webp">
  <img src="photo.jpg" alt="Desc" width="800" height="600">
</picture>
```

### 6.2 Video Codecs
*   **H.264 (AVC):** Maximum compatibility.
*   **VP9:** Royalty-free, good efficiency.
*   **AV1:** Best compression, high CPU usage (good for archives/streaming).
*   **Strategy:** H.264 + VP9 (Compatibility), AV1 (Bandwidth savings).

### 6.3 Responsive & Lazy Loading
*   **Responsive:** Use `srcset` and `sizes` for resolution switching.
*   **Lazy:** Add `loading="lazy"` to `<img>` and `<iframe>` for below-fold content.

### 6.4 CLS Prevention
Always declare `width` and `height` attributes on `<img>`. The browser uses these to calculate aspect ratio and reserve layout space, preventing Cumulative Layout Shift.

---

## 7. Performance: Rendering & Metrics

### 7.1 Core Web Vitals
*   **LCP (Largest Contentful Paint):** Target **≤ 2.5s**.
*   **INP (Interaction to Next Paint):** Replaced FID (March 2024). Target **≤ 200ms**.
*   **CLS (Cumulative Layout Shift):** Target **≤ 0.1**.

### 7.2 Script Loading
*   **Modules:** `<script type="module" src="...">`. Deferred by default.
*   **Defer:** `<script defer src="...">`. Runs after HTML parse. Use for classic scripts.
*   **Async:** `<script async src="...">`. Runs when ready. Use for independent analytics/ads.
*   **Avoid:** Blocking scripts in `<head>` without attributes.

### 7.3 Resource Hints
Place in `<head>` or HTTP Headers:
*   `dns-prefetch`: Resolve DNS early.
*   `preconnect`: DNS + TCP + TLS handshake.
*   `preload`: Fetch critical resources for *current* page (LCP image, fonts).
*   `prefetch`: Fetch resources for *next* likely navigation.

### 7.4 Observer APIs
Replace heavy scroll/resize event listeners with:
*   **IntersectionObserver:** Visibility, lazy loading, infinite scroll.
*   **ResizeObserver:** Element size changes.
*   **MutationObserver:** DOM changes.

---

## 8. Obsolete CSS Patterns
*   **Float-based layouts:** Replaced by Flexbox and Grid.
*   **Vendor Prefixes:** (`-webkit-`, `-moz-`). Mostly obsolete for stable properties.
*   **Heavy Runtime CSS-in-JS:** Prefer zero-runtime or native CSS features.

---

## 9. Obsolete JavaScript Patterns
*   **Functions:** `escape()` / `unescape()` (Use `encodeURI`).
*   **Statements:** `with` (Deprecated).
*   **Properties:** `arguments.callee` (Strict mode violation).
*   **Async:** Prefer `async/await` over complex `.then()` chains.
*   **DOM:** Prefer `document.querySelector` over legacy collections like `document.all`.

---

## 10. Modern Reference Template

A minimal template combining semantic structure, SEO, accessibility, and performance strategies.

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Accessible, SEO‑friendly, performant page</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="description" content="A demo of modern SEO, accessibility, and performance best practices.">
  <meta name="theme-color" content="#ffffff">
  <link rel="canonical" href="https://example.com/">

  <!-- Preconnect to critical origins -->
  <link rel="preconnect" href="https://cdn.example.com">

  <!-- Optional: preload critical font or LCP image -->
  <link rel="preload" href="/fonts/inter.woff2" as="font" type="font/woff2" crossorigin>

  <!-- JSON‑LD structured data -->
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "WebPage",
    "name": "Modern Web Page Example",
    "publisher": {
      "@type": "Organization",
      "name": "Example Company"
    }
  }
  </script>
</head>
<body>
  <header>
    <a href="#content" class="skip-link">Skip to main content</a>
    <nav aria-label="Main">
      <ul>
        <li><a href="/" aria-current="page">Home</a></li>
        <li><a href="/about/">About</a></li>
      </ul>
    </nav>
  </header>

  <main id="content">
    <article>
      <h1>Modern web standards</h1>
      <p>Example article content.</p>

      <!-- Responsive image with AVIF/WebP fallback and lazy loading -->
      <picture>
        <source srcset="hero.avif" type="image/avif">
        <source srcset="hero.webp" type="image/webp">
        <img
          src="hero.jpg"
          alt="Hero image"
          width="800" height="450"
          loading="lazy"
        >
      </picture>
    </article>
  </main>

  <aside aria-label="Related links">
    <h2>Related</h2>
    <ul>
      <li><a href="/related-1/">Related article 1</a></li>
      <li><a href="/related-2/">Related article 2</a></li>
    </ul>
  </aside>

  <footer>
    <p>&copy; 2026 Example Company</p>
  </footer>

  <!-- Scripts at the end, with appropriate loading strategies -->
  <script type="module" src="app.js"></script>
</body>
</html>
```