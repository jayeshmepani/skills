# The Complete Modern HTML/CSS/JavaScript Master Guide — 2025–2026 Edition

> **Edition:** July 2026  
> **Scope:** Modern CSS, HTML UI primitives, JavaScript language features, DOM/Web APIs, performance, browser support, and a dated platform catalogue. Experimental features are separated from production guidance.

> [!CAUTION]
> This document intentionally covers both production-ready and emerging features. Read each feature's status label and the support catalogue before making it a hard dependency.

## Table of Contents

- [1. Scope, Native-First Philosophy, and Adoption Model](#1-scope-native-first-philosophy-and-adoption-model)
  - [1.1 Core Tenets of Modern Web Engineering:](#11-core-tenets-of-modern-web-engineering)
- [2. CSS Architecture: Nesting, Tokens, Layers, Scope, At-Rules, and Selectors](#2-css-architecture-nesting-tokens-layers-scope-at-rules-and-selectors)
  - [2.1 Mastering Native CSS Nesting](#21-mastering-native-css-nesting)
  - [2.2 Design Tokens & Architectural Patterns](#22-design-tokens-architectural-patterns)
  - [2.3 The Modern CSS Architecture](#23-the-modern-css-architecture)
  - [2.4 The Native CSS Nesting Ruleset (2025 Deep Dive)](#24-the-native-css-nesting-ruleset-2025-deep-dive)
  - [2.5 The Complete At-Rules (`@`) Matrix](#25-the-complete-at-rules-matrix)
  - [2.6 Logical Properties & Advanced Selectors](#26-logical-properties-advanced-selectors)
- [3. Units, Intrinsic Sizing, Layout, Masonry, and Container State](#3-units-intrinsic-sizing-layout-masonry-and-container-state)
  - [3.1 The Advanced Units Matrix: Viewports, Container Queries, Typography](#31-the-advanced-units-matrix-viewports-container-queries-typography)
  - [3.2 Intrinsic Sizing & Layout Control: Stretch, Fit-Content](#32-intrinsic-sizing-layout-control-stretch-fit-content)
  - [3.3 Masonry Layouts & Grid Lanes](#33-masonry-layouts-grid-lanes)
  - [3.4 Intrinsic Size Interpolation & `calc-size()`](#34-intrinsic-size-interpolation-calc-size)
  - [3.5 Scroll-State Queries & Sibling Functions (2025)](#35-scroll-state-queries-sibling-functions-2025)
- [4. CSS Mathematics, Randomness, Conditionals, Typed Attributes, and Custom Functions](#4-css-mathematics-randomness-conditionals-typed-attributes-and-custom-functions)
  - [4.1 The CSS Mathematics Engine: Trigonometry, Stepping & Algebra](#41-the-css-mathematics-engine-trigonometry-stepping-algebra)
  - [4.2 Conditional CSS and Typed `attr()`](#42-conditional-css-and-typed-attr)
  - [4.3 CSS Native Inline Conditionals](#43-css-native-inline-conditionals)
  - [4.4 Additional Cutting-Edge & Experimental Features](#44-additional-cutting-edge-experimental-features)
- [5. Color, Visual Materials, Masks, Blend Modes, HDR, and Shapes](#5-color-visual-materials-masks-blend-modes-hdr-and-shapes)
  - [5.1 Color Spaces, Mixing & Variables](#51-color-spaces-mixing-variables)
  - [5.2 Advanced UI Trends & Material Simulations](#52-advanced-ui-trends-material-simulations)
  - [5.3 Comprehensive Color Theory & Psychological Mapping](#53-comprehensive-color-theory-psychological-mapping)
  - [5.4 Control Mechanisms: Isolation, Z-Index, & Blend Modes](#54-control-mechanisms-isolation-z-index-blend-modes)
  - [5.5 The `light-dark()` Color Function](#55-the-light-dark-color-function)
  - [5.6 Advanced Gradient Masking (`mask-composite`)](#56-advanced-gradient-masking-mask-composite)
  - [5.7 Native Scrollbar Customization](#57-native-scrollbar-customization)
  - [5.8 Advanced Graphics & Display: HDR, P3, and Shapes](#58-advanced-graphics-display-hdr-p3-and-shapes)
- [6. Typography, Text Metrics, Wrapping, Whitespace, and Font Features](#6-typography-text-metrics-wrapping-whitespace-and-font-features)
  - [6.1 Next-Gen Formatting: `text-box-trim` & `corner-shape`](#61-next-gen-formatting-text-box-trim-corner-shape)
  - [6.2 Typographical Scales & Pairing Strategies](#62-typographical-scales-pairing-strategies)
  - [6.3 Whitespace Manipulation (`white-space-collapse`)](#63-whitespace-manipulation-white-space-collapse)
- [7. Forms and Customizable Native Controls](#7-forms-and-customizable-native-controls)
  - [7.1 Advanced Select & Option Styling (2025-2026)](#71-advanced-select-option-styling-2025-2026)
  - [7.2 Additional Forms & UI Styling Primitives](#72-additional-forms-ui-styling-primitives)
- [8. Animation, Intrinsic Transitions, Scroll Timelines, View Transitions, and Cursors](#8-animation-intrinsic-transitions-scroll-timelines-view-transitions-and-cursors)
  - [8.1 Next-Generation Animations & State Transitions: Discrete & Auto-Sizing](#81-next-generation-animations-state-transitions-discrete-auto-sizing)
  - [8.2 Advanced Animation & Scroll Architectures](#82-advanced-animation-scroll-architectures)
  - [8.3 Custom Cursor Architectures](#83-custom-cursor-architectures)
  - [8.4 Scroll-Driven Animations Deep Dive](#84-scroll-driven-animations-deep-dive)
  - [8.5 CSS Motion Path Animation](#85-css-motion-path-animation)
  - [8.6 Cutting-Edge Web Features (2024-2026 Expansion)](#86-cutting-edge-web-features-2024-2026-expansion)
- [9. Accessibility, Focus, Input Modality, Reading Order, and Motion Preferences](#9-accessibility-focus-input-modality-reading-order-and-motion-preferences)
  - [9.1 The Focus Hierarchy](#91-the-focus-hierarchy)
  - [9.2 Best Practice Implementation](#92-best-practice-implementation)
- [10. Declarative HTML Components: Dialog, Popover, Details, Datalist, Invokers, and Focus Groups](#10-declarative-html-components-dialog-popover-details-datalist-invokers-and-focus-groups)
  - [10.1 Advanced Native HTML APIs (No-JS Components)](#101-advanced-native-html-apis-no-js-components)
  - [10.2 Invoker Commands: Declarative Action Handling](#102-invoker-commands-declarative-action-handling)
- [11. Modern JavaScript Language and Built-Ins](#11-modern-javascript-language-and-built-ins)
  - [11.1 Modern Vanilla JavaScript Patterns](#111-modern-vanilla-javascript-patterns)
  - [11.2 Modern JavaScript Language Features](#112-modern-javascript-language-features)
  - [11.3 Modern JavaScript Data Structures & APIs (ES2024+)](#113-modern-javascript-data-structures-apis-es2024)
  - [11.4 Additional JavaScript Built-Ins](#114-additional-javascript-built-ins)
  - [11.5 ES2025/2026 JavaScript Features](#115-es20252026-javascript-features)
- [12. Web Components, DOM, Graphics, File-System, and Platform APIs](#12-web-components-dom-graphics-file-system-and-platform-apis)
  - [12.1 WebGPU & Graphics APIs](#121-webgpu-graphics-apis)
  - [12.2 File System Access API](#122-file-system-access-api)
  - [12.3 Shadow DOM & Web Components Architecture](#123-shadow-dom-web-components-architecture)
  - [12.4 Platform Web APIs (2025–mid-2026 Vanilla Renaissance)](#124-platform-web-apis-2025mid-2026-vanilla-renaissance)
- [13. Performance, Rendering Containment, Loading Priority, and Speculation](#13-performance-rendering-containment-loading-priority-and-speculation)
  - [13.1 `content-visibility`](#131-content-visibility)
  - [13.2 `fetchPriority`](#132-fetchpriority)
- [14. Advanced Specification Notes, Edge Cases, and Experimental Watchlist](#14-advanced-specification-notes-edge-cases-and-experimental-watchlist)
  - [14.1 The 2025/2026 Advanced Features: Edge Cases & Advanced APIs](#141-the-20252026-advanced-features-edge-cases-advanced-apis)
  - [14.2 Specification Edge-Case Reference](#142-specification-edge-case-reference)
- [15. Browser Support, Baseline, Stability, and Adoption Guidance](#15-browser-support-baseline-stability-and-adoption-guidance)
  - [15.1 Browser Support Matrix & Stability Indicators](#151-browser-support-matrix-stability-indicators)
  - [15.2 Baseline Digests Alignment (July 2026 Catalogue)](#152-baseline-digests-alignment-july-2026-catalogue)
- [16. Authoritative Web Platform Catalogue — 2025 to 10 July 2026](#16-authoritative-web-platform-catalogue-2025-to-10-july-2026)
  - [16.1 Executive summary](#161-executive-summary)
  - [16.2 How to read this report](#162-how-to-read-this-report)
  - [16.3 Practical adoption tiers](#163-practical-adoption-tiers)
  - [16.4 High-impact features and minimal examples](#164-high-impact-features-and-minimal-examples)
  - [16.5 Complete normalized catalogue (147 features)](#165-complete-normalized-catalogue-147-features)
  - [16.6 Very recent stable-release delta (19)](#166-very-recent-stable-release-delta-19)
  - [16.7 Beta / preview watchlist (not counted as shipped)](#167-beta-preview-watchlist-not-counted-as-shipped)
  - [16.8 Notable removals and behavior changes](#168-notable-removals-and-behavior-changes)
  - [16.9 Sources](#169-sources)
  - [16.10 Scope cautions](#1610-scope-cautions)

---

## 1. Scope, Native-First Philosophy, and Adoption Model

For over a decade, web developers relied heavily on abstractions (SCSS, Tailwind, JQuery) to patch missing features in browsers. As of 2024-2025, the W3C and browser vendors have reached a historic consensus, delivering mathematical capabilities, nesting, color spaces, and container awareness natively into CSS.

### 1.1 Core Tenets of Modern Web Engineering:

1. **Native-first styles:** Prefer standards-based CSS and keep the runtime output understandable. A build step is optional and remains useful for minification, compatibility transforms, linting, design-token generation, and bundling.
2. **Device-agnostic and context-aware:** Use container queries for component-local adaptation and media queries for viewport, user-preference, input-capability, print, and device-level conditions. They complement rather than replace one another.
3. **Accessibility First, Not as an Afterthought:** Focus states are mapped contextually (keyboard vs. mouse), ensuring compliance without sacrificing aesthetics.
4. **CSS before JavaScript for layout:** Let CSS handle layout, sizing, and responsive rules whenever it can express the requirement. JavaScript remains appropriate for state, measurement-dependent behavior, and APIs unavailable to CSS; avoid repeated synchronous layout reads and writes that cause main-thread work.

---

## 2. CSS Architecture: Nesting, Tokens, Layers, Scope, At-Rules, and Selectors

### 2.1 Mastering Native CSS Nesting
Native CSS nesting became interoperable across current engines during 2023 and removes one common reason for a preprocessor. Sass/SCSS can still provide modules, tooling conventions, and compatibility transformations that native nesting does not replace. However, Native Nesting has unique evaluation rules and specificity differences compared to SCSS.

#### 2.1.1 The Rules of the Ampersand (`&`)

The `&` acts as the explicit pointer to the parent selector.

##### Scenario A: Simple Descendant (Nesting without `&`)

When you nest a selector without an ampersand, it behaves exactly like a standard space-separated descendant selector.

```css
.card {
  background: white;
  padding: 1rem;

  /* Translates directly to: .card .card-title */
  .card-title {
    font-size: 2rem;
  }
}
```

##### Scenario B: Joined Selectors (Requires `&`)

If you need to attach a class pseudo-class directly to the parent object (no trailing space), you MUST use `&`.

```css
.button {
  background: blue;

  /* Translates to: .button.btn-large */
  &.btn-large {
    padding: 2rem;
  }

  /* Translates to: .button:hover */
  &:hover {
    background: darkblue;
  }
}
```

##### 🚨 Crucial Distinction: `&.xyz` vs `& .xyz`

You must understand the explicit spacing when using `&`:

- `.abc { &.xyz { ... } }` compiles to `.abc.xyz` (the element has both classes).
- `.abc { & .xyz { ... } }` compiles to `.abc .xyz` (the child element has `.xyz`).
- `.abc { .xyz { ... } }` compiles to `.abc .xyz` (exactly the same as above!).

##### Scenario C: Contextual / Prefix Selection (Requires `&`)

If you want to style an element differently based on a class applied to an ancestor (e.g., body or HTML tag), place the `&` second.

```css
.navigation {
  background: white;

  /* Translates to: .dark-mode .navigation */
  .dark-mode & {
    background: black;
  }
}
```

##### Scenario D: Sibling Selection Combinators

```css
.list-item {
  border-bottom: 1px solid #ccc;

  /* Translates to: .list-item + .list-item */
  /* Styles the item ONLY if it follows another list-item */
  & + & {
    border-top: 1px dashed red;
  }

  /* Translates to: .list-item ~ .featured */
  & ~ .featured {
    font-weight: bold;
  }
}
```

#### 2.1.2 Avoiding Extreme Specificity Escalation

Unlike SCSS, which simply strings text together, native CSS evaluates the `&` using `:is()`.
For example:

```css
.foo,
#bar {
  .baz {
    color: red;
  }
}
```

This is evaluated as `:is(.foo, #bar) .baz`. Because `#bar` is an ID, the entire block assumes the extremely high specificity weight of an ID. **Always stick to class selectors to avoid specificity wars.**

### 2.2 Design Tokens & Architectural Patterns
Follow a strict mapping system to prevent cascading failures.

#### 2.2.1 The 3-Tier Variable Paradigm

Define variables in three layers exactly like Enterprise Design Systems:

**1. Primitive Tokens (The Raw Data)**
Define the absolute core values. Never use these directly in components.

```css
:root {
  --blue-100: #e0f2fe;
  --blue-500: #0ea5e9;
  --blue-900: #0c4a6e;

  --spacing-1: 0.25rem;
  --spacing-4: 1rem;
}
```

**2. Semantic Tokens (The Meaning)**
Assign meaning to the primitives. These hold the application's rules.

```css
:root {
  --color-primary: var(--blue-500);
  --color-primary-hover: var(--blue-900);
  --color-bg-subtle: var(--blue-100);

  --space-component-padding: var(--spacing-4);
  --space-gap-small: var(--spacing-1);
}
```

**3. Component Specific Tokens (The Application)**
Locally scope variables inside the components themselves allowing instant overrides dynamically via HTML or JS!

```css
.card {
  --card-bg: white;
  --card-pad: var(--space-component-padding);

  background: var(--card-bg);
  padding: var(--card-pad);
  border-radius: 12px;
}

/* Dark mode just updates the semantic tokens or local tokens! */
.dark-theme .card {
  --card-bg: var(--color-bg-subtle);
}
```

---

### 2.3 The Modern CSS Architecture
Having mastered the individual native features, how do we stitch them together to build resilient, enterprise-scale web applications? BEM, CUBE CSS, utility classes, CSS Modules, and other naming methodologies remain valid choices. Native cascade layers, scoping, nesting, and low-specificity selectors add new architectural options; choose a convention deliberately rather than declaring one universal replacement.

Instead, we use native CSS `@layer`, Semantic Tokens, and Modern Selectors (`:is`, `:has`, `:where`).

#### 2.3.1 Natively Scoped Layers (`@layer`)

For decades, CSS specificity wars raged because a single ID (`#header`) would permanently overpower a utility class. `@layer` solves this by explicitly defining the priority of styles BEFORE the browser even parses them.

**The Golden Architecture:**

```css
/* Define the exact order of importance regardless of where the code lives */
@layer reset, tokens, base, layout, components, utilities, overrides;

/* 
  1. reset: Normalizing browser defaults
  2. tokens: CSS Custom Properties (Colors, Spacing, Typography)
  3. base: html, body, h1, a, p
  4. layout: .app-shell, .sidebar, .grid
  5. components: .card, .btn, .custom-table
  6. utilities: .d-flex, .mb-4, .text-center (these ALWAYS beat components now!)
  7. overrides: User theme injection, high contrast modes
*/
```

#### 2.3.2 Zero-Class Styling with `:where()`

Sometimes you want to style an element globally (like removing margins on lists) but you WANT developers to easily override it without fighting specificity. `:where()` applies styles with **zero specificity**.

```css
/* Applies to all UL/OL, but has a specificity of 0,0,0! Any class will beat it instantly. */
:where(ul, ol) {
  list-style: none;
  margin: 0;
  padding: 0;
}
```

#### 2.3.3 Grouping Specificity with `:is()`

`:is()` groups selectors together but adopts the specificity of the _most specific_ item inside it. It cleans up nesting drastically.

```css
/* Old Way - 4 separate blocks */
header h1,
header h2,
footer h1,
footer h2 {
  color: var(--color-primary);
}

/* Modern Way */
:is(header, footer) :is(h1, h2) {
  color: var(--color-primary);
}
```

#### 2.3.4 The Parent Selector (`:has`)

The most powerful selector introduced since CSS3. You can finally style a parent element based on what children it contains, or its state.

**Real-world Example: Advanced Data Tables**

```css
.custom-table tbody tr {
  transition: background var(--dur-fast);
  /* Default hover state */
  /* ONLY hover if the row DOES NOT have a checked checkbox! */
  &:not(:has(input[type="checkbox"]:checked)):hover {
    background: var(--color-bg-subtle);
  }

  /* Selected Row State */
  /* If the row HAS a checked checkbox anywhere inside it, highlight the whole row! */
  &:has(input[type="checkbox"]:checked) {
    background: var(--color-primary-subtle);

    & td {
      color: var(--color-primary-dark);
      font-weight: bold;
    }
  }
}
```

#### 2.3.5 Component Container Queries in Production

How do we make a data table responsive without writing massive media queries based on screen size? We query the _container_.

```css
/* 1. Define the container shell */
.data-table-wrapper {
  container-type: inline-size;
  container-name: data-table;
}

.table-toolbar {
  display: flex;
  justify-content: space-between;
}

/* 2. Style based on the wrapper, not the screen! */
/* If the table's container shrinks below 600px, stack the toolbar vertically! */
@container data-table (max-width: 600px) {
  .table-toolbar {
    flex-direction: column;
    align-items: stretch;
  }
}
```

#### 2.3.6 Type-Safe Custom Properties (`@property`)

Standard CSS variables (`--color-primary`) are treated as generic strings by the browser. You cannot animate them (e.g., you can't smoothly transition a linear gradient's colors). By registering them via Houdini `@property`, the browser engine understands their _type_ (e.g., `<color>`, `<length>`, `<percentage>`).

```css
@property --gradient-angle {
  syntax: "<angle>";
  inherits: false;
  initial-value: 0deg;
}

.magic-card {
  /* We can now animate this gradient because the browser knows --gradient-angle is an angle! */
  background: linear-gradient(
    var(--gradient-angle),
    var(--color-primary),
    var(--color-accent)
  );
  animation: spin 3s linear infinite;
}

@keyframes spin {
  from {
    --gradient-angle: 0deg;
  }
  to {
    --gradient-angle: 360deg;
  }
}
```

#### 2.3.7 Content Visibility for Extreme Performance

When dealing with massive DOM trees (like a table with 5000 rows), the browser struggles to calculate styling for items off-screen. `content-visibility` tells the browser to skip rendering things you can't see yet.

```css
.data-table-wrapper {
  /* The browser will NOT render or paint the table until it approaches the viewport */
  /* This yields massive FPS boosts on long, complex dashboard pages */
  content-visibility: auto;

  /* Optional: Provide an intrinsic size so the scrollbar doesn't jump randomly */
  contain-intrinsic-size: 800px;
}
```

---

### 2.4 The Native CSS Nesting Ruleset (2025 Deep Dive)
CSS nesting is inherently different from SCSS. While SCSS simply concatenates strings before compilation, Native CSS evaluates the DOM tree dynamically. Understanding the `&` (ampersand) is critical.

#### 2.4.1 The 6 Ironclad Nesting Rules

- **1. Implicit Descendant:**
  When you nest without `&`, it assumes a space character (descendant combinator).
  `ul { li {} }` translates to `ul li {}`
- **2. Compound Selectors (Same Element):**
  If the nested selector applies to the _same_ element as the parent, you MUST use `&` with no space.
  `.btn { &.active {} }` translates to `.btn.active {}`
- **3. Pseudo-classes & Pseudo-elements:**
  Because these apply to the current element, they require `&`.
  `.card { &:hover {}, &::before {} }` translates to `.card:hover {}, .card::before {}`
- **4. Context Reversal:**
  If you want the parent selector to act as the child in the compiled CSS, place `&` last.
  `.theme-dark { .card & {} }` translates to `.card .theme-dark {}`
- **5. Sibling Combinators:**
  While `.a { + .b {} }` works in modern parsers, explicitly writing `.a { & + .b {} }` is significantly better for readability.
- **6. NO String Concatenation (BEM Failure):**
  You **CANNOT** do `.button { &__icon {} }` to create `.button__icon`. Native CSS parses `&` as the actual DOM element reference (`:is(.button)`), not the string text ".button".

### 2.5 The Complete At-Rules (`@`) Matrix
Browser engines process instructions hierarchically. At-rules define the absolute logic of the CSS file.

#### 2.5.1 Core Structural At-Rules

- `@charset "UTF-8";` - Must be the very first line of the file.
- `@import url("theme.css") layer(theme);` - Imports a file and optimally assigns it directly to a cascade layer.
- `@layer reset, base, components;` - Defines the absolute priority weighting of the CSS file.
- `@supports (display: grid)` - A native feature query. Applies CSS only if the browser successfully understands the property.

#### 2.5.2 Viewport & Containment Logic

- `@media (min-width: 768px)` - The classic viewport constraint.
- `@container (min-width: 400px)` - Applies styles based on the parent _container's_ physical size, not the device screen.
- `@scope (.card) to (.card-content)` - A modern solution of Component isolation. It applies styles _only_ to the `.card`, but STOPS applying them as soon as it hits `.card-content` deeper in the DOM tree.

#### 2.5.3 Animation & Rendering

- `@keyframes spin { ... }` - Defines animation frames.
- `@starting-style` - Solves the "display: none" animation problem. Defines the style an element should have _before_ it physically enters the DOM viewport (e.g., `opacity: 0`).
- `@view-transition` - Triggers the View Ttransitions API for smooth morphing animations between page loads or DOM state swaps without JavaScript routing.

#### 2.5.4 Advanced Typographical & Variable At-Rules

- **`@font-face`**: Imports external woff2 typography.
- **`@property --my-color`**: Registers a custom CSS variable, locking its type (e.g., `syntax: "<color>"`) so the browser can parse and interpolate it as a typed value.
- **`@font-palette-values`**: Adjusts the internal color palette used by advanced multi-color fonts (like specific Emoji fonts).
- **`@color-profile`**: Defines a custom color space profile for use within `color()` and `color-mix()` functions.
- **`@function` (Experimental - Chrome 139+)**: Bringing DRY logic directly to CSS without SCSS mixins.
  ```css
  @function --calculate-fluid-space(--min, --max) {
    result: clamp(var(--min), 5vw, var(--max));
  }
  ```

### 2.6 Logical Properties & Advanced Selectors
#### 2.6.1 Logical Properties (RTL/LTR Agnostic)

Prefer logical properties for internationalized components; physical properties remain appropriate when the design is intentionally tied to physical directions. Physical directions break when websites are translated to Arabic or Hebrew (Right-to-Left alignment).
Instead, map coordinates to the _flow_ of text:

- `margin-inline-start`: Replaces `margin-left` in English, but automatically flips to `margin-right` in Arabic.
- `margin-inline-end`: Replaces `margin-right`.
- `padding-block-start`: Replaces `padding-top`.
- `padding-block-end`: Replaces `padding-bottom`.
- `inset`: Shorthand for top/right/bottom/left (`inset: 0;` replaces `top:0; bottom:0; left:0; right:0;`)
- **Logical Border Radius**:
  - `border-start-start-radius`
  - `border-start-end-radius`
  - `border-end-start-radius`
  - `border-end-end-radius`

#### 2.6.2 Advanced Structural Selectors

- **:has() (The Parent Selector):** Applies styles to a parent ONLY if it contains a specific child.
  - `form:has(input:invalid) { border: red; }` - The entire form goes red if ANY input inside fails validation.
- **:is() (Target Grouping):** Groups selectors effortlessly while maintaining the specificity of the highest item inside it.
  - `:is(h1, h2, h3) { color: blue; }`
- **:where() (Zero Specificity Grouping):** Groups selectors exactly like `:is()`, but forces their specificity to `0,0,0`. Perfect for defining base framework styles that users can override instantly without `!important`.
- **:not() (Exclusion):** Styles everything _except_ what is inside the parenthesis.
  - `.list-item:not(:last-child) { border-bottom: 1px solid gray; }`

#### 2.6.3 Sibling Counting & Flow Control

- **`sibling-index()` & `sibling-count()`**: Perform layout math based on how many elements live in the DOM without JS counting them!
- **`column-rule` / `row-rule`**: Styles the "gap" line between flex items or grid columns natively, without needing extra border wrappers or `:not(:last-child)` hacks.
  - `column-rule: 2px dashed blue;`

```css
.list-item {
  /* If there are 10 items, the first one gets an animation delay of 0.1s, the 5th gets 0.5s! */
  animation-delay: calc(sibling-index() * 0.1s);

  /* If a container has exactly 3 items, make them 33% wide. If it has 2, make them 50% wide! */
  width: calc(100% / sibling-count());
}
```

---

## 3. Units, Intrinsic Sizing, Layout, Masonry, and Container State

### 3.1 The Advanced Units Matrix: Viewports, Container Queries, Typography
We are no longer bound to `px`, `%`, `vw`, and `vh`. The modern web runs on dynamic, container-aware, and typographic sizing elements.

#### 3.1.1 Advanced Typographical Units

These units are relative to the font formatting of the element rendering them.

- **`ch` (Character):** Represents the width of the `0` (zero) glyph of the element's font.
  - _Usage:_ Setting line-length for optimal readability. (e.g., `p { max-width: 65ch; }`).
- **`ex`:** Represents the x-height of the element's font (the height of a lowercase 'x').
- **`cap`:** Represents the "cap height" of the font (height of a capital letter).
- **`ic` (Ideograph Character):** The width and height of the "水" (water) character, used heavily in CJK typography.
- **`rem` (Root EM):** Relative to the base HTML font-size (usually 16px). The gold standard for spacing and font sizes.
- **`em` (Element EM):** Relative to the element's _current_ font-size.
  - _Usage:_ Sizing SVG icons directly next to text: `svg { width: 1em; height: 1em; }` ensures the icon perfectly scales with the text.

#### 3.1.2 The Dynamic Viewport Revolution (`dvh`, `dvw`)

The classic `100vh` unit had a massive flaw: it didn't account for mobile browser UI (safari address bars) expanding and collapsing when scrolling, causing UI clipping. We now use dynamic viewport units.

- **`lvh` / `lvw` (Large Viewport):** The viewport size assuming all browser chrome/toolbars are MINIMIZED (hidden).
- **`svh` / `svw` (Small Viewport):** The viewport size assuming all browser chrome/toolbars are EXPANDED (visible).
- **`dvh` / `dvw` (Dynamic Viewport):** A modern solution. It reflects the dynamic viewport as browser UI expands or contracts. Because its value can change during interaction, test for visible resizing and prefer `svh` where a stable minimum is more appropriate.
  - _Usage:_ `min-height: 100dvh` is often useful for viewport-filling sections that should track the dynamic mobile viewport; use `100svh` when avoiding toolbar-driven resizing is more important.

#### 3.1.3 Container Query Units (`cqi`, `cqh`, `cqb`)

Why base a card's padding on the width of the _window_ (`vw`) when you can base it on the width of the _parent card container_ itself?

To unlock these, first declare a container on a parent element:

```css
.card-grid-item {
  container-type: inline-size;
  container-name: card;
}
```

Now, any child of `.card-grid-item` can use CQ units!

- **`cqi` (Container Query Inline):** 1% of the container's inline-size (typically width).
- **`cqb` (Container Query Block):** 1% of the container's block-size (typically height).
- **`cqmin` / `cqmax`:** Identifies the smaller/larger value between `cqi` and `cqb`.

_Example: Fluid typography exclusively driven by the box it lives in:_

```css
.card-title {
  /* Font starts at 1.5rem, but grows to represent 5% of the card's width, maxing out at 3rem */
  font-size: clamp(1.5rem, 5cqi, 3rem);
}
```

#### 3.1.4 Print & Absolute Units

Avoid these for ordinary responsive screen UI; they remain valid for print and specialized physical-size use cases:

- `pt` (Points), `pc` (Picas) - Derived from print typography.
- `cm`, `mm`, `in` - Centimeters, millimeters, inches.

#### 3.1.5 Relative Color Units from Elements

- **`currentcolor`**: References the element's computed `color` property.
  - _Usage:_ `border-color: currentcolor;` ensures borders match text color automatically.
- **`light-dark(light, dark)`**: Automatically switches between light and dark mode values.
  ```css
  :root {
    --bg: light-dark(white, black);
    --text: light-dark(black, white);
  }
  ```

### 3.2 Intrinsic Sizing & Layout Control: Stretch, Fit-Content
Avoid using `width: 100%` or proprietary fill keywords as a reflex; choose the sizing keyword that expresses the layout intent. Modern layout leverages properties that describe the _intent_ of the layout.

#### 3.2.1 The Intrinsic Sizing Triad

When assigning widths to elements, you can let the interior content dictate the box size natively:

- **`min-content`:** The absolute narrowest a box can become without overflowing its largest indestructible word (e.g., a long URL or a long word like "Pneumonoultramicroscopicsilicovolcanoconiosis"). It takes every possible line-break.
- **`max-content`:** The box ignores the parent boundary and extends physically as far as it takes to render the text on a single line with ZERO line wraps.
- **`fit-content`:** The perfect hybrid. The box behaviors like `max-content` (hugging the interior data closely) but the second it collides with the parent wrapper border, it behaves like `max-width: 100%` and begins wrapping naturally.

```css
.button,
.badge {
  /* Ensures buttons only take up as much space as their label */
  width: fit-content;
  margin-inline: auto; /* center it */
}
```

#### 3.2.2 The Ascension of `stretch`

Historically, `-webkit-fill-available` or `-moz-available` were used via hacks to force an element to take up remaining height/width space. The modern standardized property is `stretch`.

- _Usage:_ Use `width: stretch;` or `justify-self: stretch;` or `height: stretch;` inside Flexbox and Grid layouts to enforce absolute filling of the parent's available axis space without triggering scrollbars or math calculation errors associated with `100%`.

### 3.3 Masonry Layouts & Grid Lanes
A masonry layout fits elements together vertically without empty rows, resembling a brick wall (typically used for Pinterest-style image galleries). **2025–2026** work (sometimes branded **Grid Lanes**) lands native waterfall packing in CSS Grid without absolute-position hacks.

#### 3.3.1 Native masonry / Grid Lanes — evolving and limited availability

```css
.masonry-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  grid-template-rows: masonry; /* native packing — mixed-height items, no row stretch gaps */
  gap: 1.5rem;
}

/* Subgrid: child tracks align to parent tracks (Baseline-era refinement) */
.card-group {
  display: grid;
  grid-template-columns: subgrid;
  grid-column: span 2;
}
```

**Status:** Syntax and implementation have evolved across drafts and engines. Check the current CSSWG draft and browser data for your exact target versions. Keep a grid or multicolumn fallback and isolate any experimental syntax behind `@supports`.

```css
@supports (grid-template-rows: masonry) {
  .masonry-grid {
    display: grid;
    grid-template-rows: masonry;
  }
}
```

#### 3.3.2 The CSS Column Fallback (Production Ready)

Until masonry is 100% global Baseline, the most robust zero-JS fallback is multicolumn layout.

```css
.masonry-container {
  /* Creates a newspaper-style multi-column layout */
  column-count: 3;
  column-gap: 1.5rem;
}

/* Responsive breakdowns */
@container (max-width: 800px) {
  .masonry-container {
    column-count: 2;
  }
}
@container (max-width: 500px) {
  .masonry-container {
    column-count: 1;
  }
}

.masonry-item {
  /* CRITICAL: Prevents images or cards from breaking across two columns! */
  break-inside: avoid;
  margin-bottom: 1.5rem;
  width: 100%;
}

.masonry-item img {
  width: 100%;
  height: auto; /* MUST be auto so they scale proportionally without forced aspect ratios */
  display: block;
}
```

### 3.4 Intrinsic Size Interpolation & `calc-size()`
For 20 years, developers could not animate `height: 0` to `height: auto`. This was impossible because `0` is a number and `auto` is a string keyword based on content volume.

The W3C solved this via two mechanisms in 2024-2025:

#### 3.4.1 The Global Opt-in: `interpolate-size`

If you want your entire application to allow transitioning to intrinsic sizes (`min-content`, `fit-content`, `auto`), flip the global switch on the root:

```css
:root {
  interpolate-size: allow-keywords;
}

.dropdown-menu {
  height: 0;
  transition: height 0.3s ease;
  overflow: hidden;

  &.is-open {
    height: fit-content; /* It works perfectly without JS measuring! */
  }
}
```

#### 3.4.2 The Math Operator: `calc-size()`

If you need to perform math _while_ transitioning an intrinsic size, use `calc-size(basis, calculation)`.

```css
.card-drawer {
  /* Animate height up to the natural content size, PLUS 50px of extra padding */
  height: calc-size(max-content, size + 50px);
}
```

### 3.5 Scroll-State Queries & Sibling Functions (2025)
#### 3.5.1 `container-type: scroll-state`

Detect scroll position states natively in CSS.

```css
.scroll-wrapper {
  height: 200px;
  overflow-y: scroll;
  container-type: scroll-state;
  container-name: scroll-wrapper;
}

.sticky-header {
  position: sticky;
  top: 0;
  background: var(--surface-2);
  padding: 0.75rem 1rem;
  transition: all 0.3s;
}

@container scroll-wrapper scroll-state(stuck: top) {
  .sticky-header {
    background: color-mix(in oklch, var(--teal) 12%, var(--surface-strong));
    color: var(--teal);
    box-shadow: 0 4px 20px rgba(0,0,0,0.25);
  }
}
```

#### 3.5.2 `sibling-index()` & `sibling-count()`

Progressive styling based on element position.

```css
.sibling-list {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.sibling-item {
  padding: 0.75rem 1rem;
  background: var(--surface-2);
  border-radius: 6px;
  /* Progressive hue rotation */
  border-left: 4px solid oklch(
    from var(--accent) l c 
    calc(h + sibling-index() * 20)
  );
  /* Progressive opacity */
  opacity: calc(sibling-index() / sibling-count());
  /* Progressive scale */
  scale: calc(0.6 + sibling-index() / sibling-count() * 0.6);
  transition: all 0.3s;
}

.sibling-item:hover {
  transform: translateX(4px);
}
```

---

## 4. CSS Mathematics, Randomness, Conditionals, Typed Attributes, and Custom Functions

### 4.1 The CSS Mathematics Engine: Trigonometry, Stepping & Algebra
CSS now includes a much richer typed calculation language—trigonometric, exponential, sign, stepping, and conditional functions—but it is not generally described as a Turing-complete programming language. Rendering performance depends on the property, browser pipeline, device, and workload; do not assume every calculation is GPU-accelerated or runs at a fixed frame rate.

#### 4.1.1 The Core Modifiers: `calc()`, `min()`, `max()`, `clamp()`

- `calc(100% - 2rem)`: Perform basic math, mixing units freely.
- `min(50vw, 800px)`: Enforce a ceiling. Returns the _smallest_ value. "Take up half the screen, but NEVER exceed 800px."
- `max(20rem, 100%)`: Enforce a floor. Returns the _largest_ value. "Always be 100% wide, but if the container gets too small, stop shrinking at 20rem."
- `clamp(MIN, IDEAL, MAX)`: A useful fluid-sizing function. `clamp(1rem, 2vw, 2rem)`

#### 4.1.2 Trigonometry (`sin`, `cos`, `tan`, `asin`, `acos`, `atan`, `atan2`)

Place elements on circular paths, create interactive sun-dials, or calculate border offsets based on rotation angles.
Takes `deg`, `rad`, `grad`, or `turn`.

**Example: A Circular Clock UI Layout purely in CSS:**

```css
.dial {
  --radius: 15rem;
  --angle: 30deg; /* Updated by JS as time ticks */

  position: absolute;
  /* x = r * cos(θ), y = r * sin(θ) */
  translate: calc(cos(var(--angle)) * var(--radius))
    calc(sin(var(--angle)) * var(--radius));
}
```

#### 4.1.3 Exponents & Logarithms (`pow`, `sqrt`, `hypot`, `log`, `exp`)

- `pow(base, exponent)`: Calculate powers. E.g. `pow(2, 3)` = 8. Useful for creating modular font scales purely in CSS variables!
- `sqrt(x)`: Square root.
- `hypot(x, y)`: Calculate the hypotenuse (the diagonal distance). Useful for calculating the exact distance connecting two coordinates.

#### 4.1.4 Stepping & Gradients (`round`, `mod`, `rem`)

- **`round(strategy, value, step)`:** Snaps a fluid value to a hard grid.
  - _Strategies:_ `nearest`, `up`, `down`, `to-zero`
  - _Usage:_ `width: round(nearest, var(--calculated-width), 50px);` ensures a progress bar only visually moves in 50px chunks, creating a "retro game" stepping effect.
- **`mod()` and `rem()` (Modulo & Remainder):**
  - Useful for alternating patterns or infinite loops natively in CSS keyframes by evaluating the remainder of a division.

#### 4.1.5 Sign Metrics & Visual Curvature (`abs`, `sign`)

- **`abs(val)`:** Always returns the positive absolute value.
- **`sign(val)`:** Returns `1` if positive, `-1` if negative, `0` if zero. Vital for setting variable directions (Left/Right) in generic animations.

**The Golden Curvature Formula (Visual Consistency):**
When nesting boxes with borders, use this formula to ensure the inner curve matches the outer curve perfectly:
- `r_outer = r_inner + gap`
- `r_inner = r_outer - gap`

**Dynamic Scaling Formula:**
- `radius = k * min(height, width)` (where `k` is a factor like 0.2).

#### 4.1.6 5.5b CSS `random()` — Generative Values (CSS Snapshot 2025+)

In supporting engines, `random()` can produce controlled generative values without a JavaScript loop. It remains limited-availability and must have a deterministic fallback. Always pair with a fallback for engines without support.

```css
.chip {
  /* random(min, max, step?) — exact signature may evolve; feature-detect */
  --hue: random(0, 360, 10);
  --jitter: random(0.5rem, 1.5rem);
  background: oklch(70% 0.12 var(--hue));
  margin-inline-start: var(--jitter);
  border-radius: random(4px, 16px, 2px);
}

/* Prefer fixed seeds/caches when engines expose them so SSR + client match */
.sparkle {
  rotate: random(-8deg, 8deg);
  scale: random(0.9, 1.1);
}
```

```css
@supports not (margin: random(1px, 2px)) {
  .chip { margin-inline-start: 1rem; }
}
```

**Use sparingly in product UI** (reproducibility, a11y, and testing). Excellent for marketing textures, avatars, decorative grids.

#### 4.1.7 5.5c CSS Toggles — State Without Class-Toggling JS

CSS toggle/state proposals explore declarative binary and multi-state UI. Syntax and implementation status can change; prefer stable native state such as `details`, `popover`, `dialog[open]`, `:checked`, and invoker commands for production.

```css
/* Conceptual pattern — verify final syntax on MDN / caniuse before shipping */
.panel {
  /* Toggle named state driven by a control in the tree */
  display: none;
}
.panel:toggle(open) {
  display: block;
}

/* Progressive fallback: details/summary, checkbox hacks, or invoker+popover */
```

**Production guidance (July 2026):**
1. Prefer **native HTML state** first: `<details>`, `popover`, `dialog[open]`, checkbox/`:checked`, Invoker Commands.
2. Use CSS toggles only when the UA documents stable support for your targets.
3. Never rely on toggles alone for critical a11y state — keep keyboard and AT semantics on real controls.

#### 4.1.8 CSS Functions (`@function`) — Chrome 139+

Define reusable functions with typed parameters and return values.

```css
@function --tint(--base <color>, --amount <number>: 0.15) {
  result: color-mix(in oklch, var(--base) calc(var(--amount) * 100%), white);
}

@function --shade(--base <color>, --amount <number>: 0.2) {
  result: color-mix(in oklch, var(--base) calc((1 - var(--amount)) * 100%), black);
}

@function --fluid-space(--min <length>: 1rem, --max <length>: 3rem) {
  result: clamp(var(--min), 4vw, var(--max));
}

/* Usage */
.button {
  background: var(--tint(--brand, 0.3));
  padding: var(--fluid-space);
}
```

### 4.2 Conditional CSS and Typed `attr()`
#### 4.2.1 Inline Conditionals: `if()`

CSS can evaluate conditionals inline (media / style / feature queries), reducing duplicate rule blocks. **Chromium-led 2025–2026; progressive enhance with classic `@media` fallbacks.**

```css
.btn {
  /* Mobile full-width vs hug content */
  width: if(media(max-width: 600px): 100%; else: fit-content);

  /* Token-driven size */
  padding: if(style(--size: large): 2rem; else: 1rem);

  /* A11y: kill motion when the user asks */
  transition-duration: if(
    media(prefers-reduced-motion: reduce): 0ms;
    else: 180ms
  );
}

/* Always keep a classic fallback for browsers without if() */
@supports not (width: if(media(width >= 0): 1px; else: 0)) {
  @media (max-width: 600px) {
    .btn { width: 100%; }
  }
}
```

#### 4.2.2 Typed Attributes: `attr(type)`

The `attr()` function used to only extract string text for `::before { content: attr(data-label); }`. Now, it can extract numbers, colors, and percentages directly from HTML and cast them into CSS!

```html
<div class="progress" data-fill="75%" data-color="#ff0000"></div>
```

```css
.progress::after {
  /* Extracts the 75% string and casts it as a strict mathematical <length-percentage> */
  width: attr(data-fill type(<length-percentage>), 0%);

  /* Extracts the hex string and casts it as a strict <color>, defaulting to blue if missing */
  background: attr(data-color type(<color>), blue);
}
```

### 4.3 CSS Native Inline Conditionals
**(Experimental - e.g., Chrome 137+)**  
CSS now introduces the `if()` function combined with `style()` condition queries, allowing inline logic resolution based on custom properties. This replaces the need for many complex calc() toggles or CSS class injections.

```css
/* Example: Applying themes via inline if() conditions */
:root {
  --theme: neon;
  --size: large;
}

body {
  /* Using if() to choose background based on --theme */
  background: if(
    style(--theme: dark): linear-gradient(135deg, #1e1e2e, #2a2a3e);
    style(--theme: light): linear-gradient(135deg, #f8fafc, #e2e8f0);
    style(--theme: neon): linear-gradient(135deg, #0f0f23, #1a1a2e);
    else: #ffffff
  );

  /* Combining conditions for specific effects */
  animation: if(
    style(--animation: enabled) and style(--theme: neon): glow 2s ease infinite alternate;
    else: none
  );
}
```

### 4.4 Additional Cutting-Edge & Experimental Features
- **`shape()` function**: Animatable, responsive non-polygon clip-paths.
- **Native Carousels**: `::scroll-button()`, `::scroll-marker`, `::scroll-marker-group`.
- **`scrollbar-gutter`**: Reserves space for the scrollbar to prevent layout shifts.

---

## 5. Color, Visual Materials, Masks, Blend Modes, HDR, and Shapes

### 5.1 Color Spaces, Mixing & Variables
We no longer need SCSS functions like `darken()`, `lighten()`, or `transparentize()`.

#### 5.1.1 CSS Native `color-mix()`

Directly blend two colors together based on percentages in any targeted color space (`srgb`, `oklch`, `hsl`).

```css
.badge-warning {
  /* Background is 15% warning yellow, 85% transparent white background! */
  background: color-mix(in srgb, var(--color-warning) 15%, transparent);

  /* Text is 100% warning yellow! */
  color: var(--color-warning);

  /* Border is 30% warning yellow mixed with white */
  border: 1px solid color-mix(in srgb, var(--color-warning) 30%, white);
}
```

#### 5.1.2 Relative Color Syntax (RCS)

Unpack a CSS color variable on the fly to manipulate its individual channels (r, g, b, h, s, l).

```css
.card-hover {
  /* Take the primary color, keep red and green identical, but FORCE blue to 255 */
  background: rgb(from var(--color-primary) r g 255);

  /* Take primary color and apply 50% opacity/alpha without needing an RGB split! */
  box-shadow: 0 4px 20px rgb(from var(--color-primary) r g b / 50%);
}
```

#### 5.1.3 The OKLCH Color Model

Human eyes don't process "Lightness" equally across hues. HSL breaks down because "50% Lightness Yellow" looks vastly brighter than "50% Lightness Blue". `oklch` (Lightness, Chroma, Hue) ensures uniform perceptual brightness!

```css
:root {
  /* OKLCH makes lightness adjustments more perceptually predictable, but contrast must still be tested for every foreground/background pair. */
  --primary-color: oklch(60% 0.15 250); /* Blue */
  --secondary-color: oklch(
    60% 0.15 45
  ); /* Orange - EXACTLY matched brightness to the blue! */
}
```

#### 5.1.4 Font Palette Control

- **`font-palette`**: Select color variants in color fonts (emoji).
- **`@font-palette-values`**: Define custom emoji color schemes.

```css
@font-palette-values --custom {
  font-family: 'Noto Color Emoji';
  base-palette: 0;
  override-colors: 
    0 var(--accent),
    1 var(--accent-2);
}

.emoji {
  font-palette: --custom;
}
```

### 5.2 Advanced UI Trends & Material Simulations
Modern web design has moved beyond flat colors into highly tactile, immersive material simulations. You no longer need heavy images to achieve these effects.

#### 5.2.1 Glassmorphism (Frosted Glass)

The illusion of frosted glass sitting above a vibrant, moving background.

**Core Ingredients:**

1. A semi-transparent background (using `rgba` or `oklch` with alpha).
2. A background blur effect (`backdrop-filter`).
3. A subtle, bright interior border to simulate light reflection on the glass edge.
4. A soft shadow to float the glass Above the canvas.

```css
.card-glass {
  /* 1. Semi-transparent background */
  background: rgba(255, 255, 255, 0.05); /* Very faint white */

  /* 2. The blur effect (The most important part) */
  backdrop-filter: blur(16px);
  -webkit-backdrop-filter: blur(16px);

  /* 3. The glass edge reflection */
  border: 1px solid rgba(255, 255, 255, 0.2);
  border-top: 1px solid rgba(255, 255, 255, 0.4); /* Stronger light from above */

  /* 4. The drop shadow */
  box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.3);

  border-radius: 24px;
}

/* Dark Mode Glass */
.dark-theme .card-glass {
  background: rgba(0, 0, 0, 0.2);
  border: 1px solid rgba(255, 255, 255, 0.08);
}
```

#### 5.2.2 Neumorphism (Soft UI)

Simulating elements that are extruded from the background material itself, using double shadows (one light, one dark).

```css
.btn-neumorphic {
  background: #e0e5ec;
  border-radius: 50px;
  /* Top-left light shadow, Bottom-right dark shadow */
  box-shadow:
    9px 9px 16px rgb(163, 177, 198, 0.6),
    -9px -9px 16px rgba(255, 255, 255, 0.5);
  transition: box-shadow 0.2s ease;
}

.btn-neumorphic:active {
  /* Inset the shadows to simulate the button being pressed INTO the surface */
  box-shadow:
    inset 6px 6px 10px 0 rgba(163, 177, 198, 0.7),
    inset -6px -6px 10px 0 rgba(255, 255, 255, 0.8);
}
```

#### 5.2.3 Neobrutalism

A rejection of soft shadows and gradients in favor of high-contrast, bold geometry, and raw utilitarian aesthetics.

```css
.card-brutal {
  background: #ffffff;
  border: 4px solid #000000;
  border-radius: 0; /* Brutalism hates curves */

  /* The signature hard, unblurred shadow */
  box-shadow: 8px 8px 0px 0px #000000;
  transition:
    transform 0.1s,
    box-shadow 0.1s;
}

.card-brutal:hover {
  /* On hover, the card "presses" down */
  transform: translate(4px, 4px);
  box-shadow: 4px 4px 0px 0px #000000;
}
```

#### 5.2.4 Aurora UI (Mesh Gradients)

Simulating natural, moving northern lights or diffused plasma using radial gradients.

```css
.aurora-bg {
  background-color: #0b0f19;
  background-image:
    radial-gradient(at 0% 0%, hsla(253, 16%, 7%, 1) 0, transparent 50%),
    radial-gradient(at 50% 0%, hsla(225, 39%, 30%, 1) 0, transparent 50%),
    radial-gradient(at 100% 0%, hsla(339, 49%, 30%, 1) 0, transparent 50%);
  background-size: 200% 200%;
  animation: auroraFlow 15s ease infinite alternate;
}

@keyframes auroraFlow {
  0% {
    background-position: 0% 50%;
  }
  100% {
    background-position: 100% 50%;
  }
}
```

### 5.3 Comprehensive Color Theory & Psychological Mapping
Color is not just aesthetic; it is communicative, psychological, and critical to UX architecture.

#### 5.3.1 The 60-30-10 Rule

The golden ratio of UI color distribution ensures a balanced interface that doesn't overwhelm the user.

- **60% Dominant Color:** The background / negative space (Usually white, near-white, dark gray, or deep navy). Sets the overall mood.
- **30% Secondary Color:** Elements like cards, sidebars, or prominent structural sections. Formats the data.
- **10% Accent Color:** The Call-to-Action (CTA). Buttons, toggles, badges, active states. This guides the user's eye instantly to what matters.

#### 5.3.2 Color Psychology Mapping

- **Blue (commonly associated with trust, corporate identity, and calm):** Frequently used in technology, banking, and analytics. These associations are contextual and cultural—not mathematical accessibility guarantees. Accessibility depends on contrast, non-color cues, and the complete visual system.
- **Red / Rose (Urgency, Passion, Danger):** Highly stimulating. Triggers fight-or-flight in UI (Delete buttons, critical errors).
- **Green / Emerald (Growth, Success, Nature):** Signals safety, completion, and financial positive movement.
- **Purple / Violet (Luxury, Creativity, Mystery):** The rarest color in nature. Excellent for modern software, premium subscriptions, and imaginative tools.
- **Yellow / Amber (Warning, Sunshine, Anxiety):** The most visible color from a distance. Use extremely sparingly for warnings; large blocks of yellow induce fatigue rapidly.

### 5.4 Control Mechanisms: Isolation, Z-Index, & Blend Modes
#### 5.4.1 Isolation and Stacking Contexts

When applying filters, opacities, or transforms to parent elements, z-indexes inside often break or "leak" out, rendering above tooltips or navbars.

**The Fix:**

```css
.complex-card {
  /* Forces the browser to create an impenetrable ceiling. */
  /* No child's z-index (even z-index: 999999) can ever escape this container to overlap external navbars. */
  isolation: isolate;
}
```

#### 5.4.2 Blend Modes (`mix-blend-mode`)

Instead of exporting multiple tinted images from Photoshop, perform blending directly in the browser through the browser rendering pipeline.

```css
.overlay-text {
  /* Interacts mathematically with the pixels underneath it / behind it */
  mix-blend-mode: difference; /* Inverts color! White text over black background, becomes black text over white background seamlessly! */
  mix-blend-mode: multiply; /* Darkens the image below identically to photoshop */
  mix-blend-mode: screen; /* Lightens the image below */
}
```

### 5.5 The `light-dark()` Color Function
A powerful, native color function that dramatically simplifies dual-theme color assignments without an explicit `@media (prefers-color-scheme: dark)` block for every property.

```css
:root {
  /* Must opt-in via color-scheme for light-dark() to function naturally */
  color-scheme: light dark;
}

body {
  /* Automatically chooses #ffffff in light mode and #1a1a1a in dark mode */
  background-color: light-dark(#ffffff, #1a1a1a);
  color: light-dark(#000000, #E0D1FF);
}
```

### 5.6 Advanced Gradient Masking (`mask-composite`)
Enables complex gradient borders by combining multiple mask layers and defining how they overlap using `mask-composite`.

```css
.gradient-border-card {
  position: relative;
  /* Provides background padding clip to act as a border area */
  border: 4px solid transparent; 
  background-clip: padding-box;
}

.gradient-border-card::before {
  content: '';
  position: absolute;
  inset: -4px; /* Extends into the border area */
  background: conic-gradient(#381D6A, #E0D1FF, #381D6A);
  
  /* Apply masks and composite them */
  mask: linear-gradient(#fff 0 0) content-box, linear-gradient(#fff 0 0) border-box;
  mask-composite: exclude; /* or 'xor' depending on browser engine implementation */
  -webkit-mask-composite: xor;
}
```

### 5.7 Native Scrollbar Customization
A standardized, non-webkit way to customize scrollbars.

```css
.custom-scroll-area {
  /* Sets scrollbar track to dark-gray and thumb to a primary blue */
  scrollbar-color: #3b82f6 #1f2937;
  /* Thin variant */
  scrollbar-width: thin; 
}
```

### 5.8 Advanced Graphics & Display: HDR, P3, and Shapes
Modern browser engines leverage hardware acceleration for high-fidelity graphics.

#### 5.8.1 High Dynamic Range (HDR) & Color Gamut

-   **`dynamic-range-limit`**: Controls how HDR content is mapped (e.g., `high` or `standard`).
-   **`color(display-p3 r g b)`**: Accesses the wide-gamut P3 color space for colors that are physically impossible in standard sRGB.
-   **`contrast-color()`**: ✅ Baseline Newly available ~April 2026 — pass a background color; browser returns a high-contrast companion (typically black/white) for accessible text without JS contrast math.

#### 5.8.2 Complex Shape Mapping

-   **`shape()`**: An extension of `clip-path` and `offset-path` that allows animatable, responsive non-polygon paths.
-   **`mask-composite`**: Combine multiple mask layers (e.g., `exclude`, `intersect`, `xor`).

---

## 6. Typography, Text Metrics, Wrapping, Whitespace, and Font Features

### 6.1 Next-Gen Formatting: `text-box-trim` & `corner-shape`
#### 6.1.1 Eradicating Typographical Leading (`text-box-trim`)

Typography formatting has historically been broken because font files natively embed empty space (leading/baseline padding) above and below letters. This made centering text identically inside buttons impossible across different fonts.

- **`text-box-trim`:** Visually chops the bounding-box of the text node physically down to the characters themselves.
- **`text-box-edge`:** Define which parts to crop to.

```css
.perfectly-centered-btn {
  /* Crop top padding to height of capital letters */
  /* Crop bottom padding to the baseline of letters (ignoring dangling letters like g, y, j) */
  text-box-trim: trim-both;
  text-box-edge: cap alphabetic;
}
```

#### 6.1.2 Architectural Angles (`corner-shape`)

Forget `border-radius`. `corner-shape` introduces polygonal edge mapping native to CSS. Excellent for Sci-fi themes, hardware UI, and rugged interfaces.

```css
.mech-panel {
  border-radius: 20px;
  /* Instead of rounding the 20px corner, it slices it cleanly as an angled chamfer notch */
  corner-shape: bevel;

  /* Other options include: */
  /* corner-shape: round; */
  /* corner-shape: scoop; (Inward curves) */
  /* corner-shape: notch; (Rectangular cutouts) */
}
```

#### 6.1.3 Advanced Inline Formatting

- **`initial-letter`**: Native replacement for `::first-letter` float hacks.
  - `initial-letter: 3 2;` (Size 3 lines, sink 2 lines).
- **`box-decoration-break: clone`**: When a span wraps across two lines, `clone` ensures the padding and border are applied to BOTH ends of the break, rather than slicing the element open.
- **`zoom`**: While `transform: scale()` is standard, the legacy `zoom` property has been revived for non-destructive layout-aware scaling.

#### 6.1.4 Text Wrap Optimization

- **`text-wrap: balance`**: Balances line lengths in headings for better typography.
- **`text-wrap: pretty`**: Prevents widows (single words on last line).
- **`text-wrap: wrap`**: Default wrapping behavior.

```css
h1 { text-wrap: balance; }
p { text-wrap: pretty; }
```

#### 6.1.5 Initial Letter Styling

- **`initial-letter: 3 2`**: Creates drop caps (size 3 lines, sink 2 lines).
  ```css
  p::first-letter {
    initial-letter: 3 2;
    font-weight: bold;
    color: var(--accent);
  }
  ```

#### 6.1.6 Font Metric Stability & Find-in-Page Highlights

```css
/* Reduce FOUT metric shift when fallback → web font swaps */
body {
  font-family: "Inter", system-ui, sans-serif;
  font-size-adjust: 0.5; /* match x-height ratio of primary face */
}

/* Style browser find-in-page / scroll-to-text fragment targets */
::target-text {
  background: color-mix(in oklch, var(--color-warning) 55%, transparent);
  color: inherit;
}
```

- **`font-size-adjust`**: Keeps perceived size consistent across fallback fonts (CLS/FOUT hygiene).
- **`::target-text`**: Styles text matched by the UA’s find-in-page or text fragments (`#:~:text=`).

### 6.2 Typographical Scales & Pairing Strategies
Typography constitutes 90% of web design. If your layout looks "off," it is almost always an issue with typographical scaling and line-height.

#### 6.2.1 Mathematical Font Scales

Do not guess `font-size`. Pick a base (e.g., 16px) and multiply it by a consistent scale factor to generate all headers.

- **Minor Third (1.200):** Subtle hierarchy, great for dense dashboards and data apps.
  - _Scale:_ 16px, 19.2px, 23.0px, 27.6px...
- **Perfect Fourth (1.333):** The standard modern web scale. Bold, readable, distinct.
  - _Scale:_ 16px, 21.3px, 28.4px, 37.8px...
- **Golden Ratio (1.618):** Extremely dramatic hierarchy. Best for artistic portfolios and marketing hero sections.

**CSS Implementation (Modular Scale):**

```css
:root {
  --base-size: 1rem;
  --scale: 1.333;
  --text-base: var(--base-size);
  --text-md: calc(var(--text-base) * var(--scale));
  --text-lg: calc(var(--text-md) * var(--scale));
  --text-xl: calc(var(--text-lg) * var(--scale));
  --text-2xl: calc(var(--text-xl) * var(--scale));
}
```

#### 6.2.2 The Rules of Line-Height (Leading)

1. **Body Text:** Optimal readability requires line-heights between `1.5` and `1.7`.
2. **Headings:** Large text needs TIGHTER line-height. H1s should have line-heights between `1.1` and `1.2`. A line-height of 1.5 on an H1 looks broken.
3. **Labels and buttons:** Use a line height that preserves legibility and accommodates the chosen font. Flex/grid alignment usually handles vertical centering more reliably than forcing `line-height: 1`.

#### 6.2.3 Type Pairing

The most reliable method for pairing fonts without being a typography expert:

- **Super-Family Approach:** Choose one massive font family that has both Serif and Sans-Serif versions (e.g., _Roboto_ and _Roboto Slab_, or _Merriweather_ and _Merriweather Sans_). They will geometrically align perfectly.
- **Contrast Approach:** Pair an extremely geometric sans-serif (like _Inter_ or _Futura_) with a highly ornate serif (like _Playfair Display_). The high contrast creates premium tension.

### 6.3 Whitespace Manipulation (`white-space-collapse`)
Finer-grained control over how white spaces and new lines are handled within the DOM natively in CSS. Replaces/augments the traditional `white-space` property.

```css
.whitespace-collapse {
    white-space-collapse: collapse; /* Collpses spaces, normal behavior */
}

.whitespace-preserve {
    white-space-collapse: preserve; /* Preserves all spaces like <pre> */
}

.whitespace-preserve-breaks {
    white-space-collapse: preserve-breaks; /* Preserves line breaks only */
}
```

---

## 7. Forms and Customizable Native Controls

### 7.1 Advanced Select & Option Styling (2025-2026)
#### 7.1.1 `appearance: base-select` — Chrome 135+

Full customization of native `<select>` dropdowns while maintaining OS-level accessibility.

```css
select {
  appearance: base-select;
  border: 2px solid var(--border);
  border-radius: 8px;
  padding: 0.6rem 1rem;
  background: var(--surface);
}

select::picker(select) {
  appearance: base-select;
  background: var(--surface-strong);
  border: 1.5px solid var(--border);
  border-radius: 12px;
  box-shadow: 0 12px 40px rgba(0,0,0,0.3);
  padding: 0.4rem;
  animation: picker-in 0.2s ease;
}

select option {
  padding: 0.6rem 1rem;
  border-radius: 6px;
}

select option:hover {
  background: var(--surface-2);
}

select option:checked {
  background: var(--accent);
  color: white;
}

select option::checkmark {
  color: rgba(255,255,255,0.8);
}

@starting-style {
  select::picker(select) {
    opacity: 0;
    transform: translateY(-8px) scale(0.97);
  }
}
```

#### 7.1.2 `selectedcontent` Element

Custom display of selected option content.

```html
<select class="custom-select">
  <button type="button">
    <selectedcontent></selectedcontent>
  </button>
  <option value="color">🎨 Color</option>
  <option value="size">📐 Size</option>
</select>
```

#### 7.1.3 Rich Options with Icons

```css
select.rich option {
  display: flex;
  align-items: center;
  gap: 0.7rem;
  padding: 0.65rem 1rem;
}

select.rich option::checkmark {
  content: "✓";
  color: var(--accent);
  font-weight: 700;
  order: 1;
  margin-left: auto;
}
```

#### 7.1.4 Optgroup Styling

```css
select optgroup {
  border: 1.5px solid var(--border);
  border-radius: 8px;
  margin-bottom: 0.4rem;
  overflow: hidden;
  background: var(--surface);
}

select optgroup legend,
select optgroup[label]::before {
  font-size: 0.72rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: var(--text-dim);
  padding: 0.4rem 0.9rem 0.25rem;
  display: block;
  background: var(--surface-2);
}
```

### 7.2 Additional Forms & UI Styling Primitives
#### 7.2.1 Customizable `<select>` (The `base-select` Era)
Styling the "unstyleable" native dropdown is now possible without complex JS "custom select" libraries.

```css
select {
  appearance: base-select; /* Unlocks internal styling */
}

/* Style the popup container */
select::picker(select) {
  background: var(--card-bg);
  border-radius: 12px;
  box-shadow: 0 10px 40px rgba(0,0,0,0.2);
  padding: 8px;
  border: 1px solid var(--border-color);
}

/* Style individual options */
option {
  padding: 10px 15px;
  border-radius: 6px;
  transition: background 0.2s;
  
  &:hover {
    background: var(--color-primary-subtle);
  }
  
  &::checkmark {
    /* Style the native checkmark icon! */
    color: var(--color-primary);
  }
}

/* Customize the native dropdown arrow! */
select::picker-icon {
  background: url("arrow.svg");
  width: 1em;
  height: 1em;
}
```

**The `<selectedcontent>` Element:**
Allows you to customize exactly what is displayed in the select button when an option is chosen.

```html
<select appearance="base-select">
  <button>
    <selectedcontent></selectedcontent> <!-- Renders the active selection -->
    <span class="icon">▼</span>
  </button>
  <option value="1">Option 1</option>
</select>
```

#### 7.2.2 Auto-Growing Textareas (`field-sizing`)

```css
textarea {
  field-sizing: content; /* Auto-expands as user types */
  min-height: 2lh; /* Ensure at least 2 lines visible */
}
```

#### 7.2.3 Form Styling Selectors
- **`accent-color`**: One-line branding for radios/checkboxes/sliders.
- **`:user-valid` / `:user-invalid`**: Applies styles ONLY after user interaction (prevents premature error states).
- **`:open`**: Targets a `<select>` or `<details>` that is currently in the open state.

---

## 8. Animation, Intrinsic Transitions, Scroll Timelines, View Transitions, and Cursors

### 8.1 Next-Generation Animations & State Transitions: Discrete & Auto-Sizing
The two most requested CSS features in web history have been solved in the 2024-2025 specs: Transitioning to `height: auto` and transitioning out of `display: none`.

#### 8.1.1 `interpolate-size: allow-keywords` (Height 0 to Auto)

Historically, CSS transitions required explicit height mapping (e.g., `height: 0px` to `height: 500px`) leading to hard-coded max-height hacks for accordions and dropdowns. This is fixed.

```css
:root {
  /* Tells the browser engine: "Yes, you are allowed to calculate math between 0 and keywords like 'auto' or 'max-content'" */
  interpolate-size: allow-keywords;
}

.accordion-body {
  height: 0;
  overflow: hidden;
  transition: height 0.4s ease-out;
}

.accordion-body.is-open {
  height: auto; /* It will calculate the exact document flow height and animate it perfectly. */
}
```

#### 8.1.2 `transition-behavior: allow-discrete` (Display None to Block)

You cannot transition a boolean (none -> block). However, applying `allow-discrete` forces the browser to wait for OTHER animations (like opacity) to finish before flipping the discrete boolean property.

#### 8.1.3 `@starting-style`

If you insert a completely new DOM element into the page via JS, the browser instantly applies the CSS classes and the element appears instantly, missing its "fade-in" transition. `@starting-style` defines the "zero state" of an element BEFORE it hits the DOM.

**The Ultimate Dialog/Toast Pattern:**

```css
.toast {
  transition:
    opacity 0.5s,
    transform 0.5s,
    display 0.5s allow-discrete;

  /* Final state when visible */
  opacity: 1;
  transform: translateY(0);
  display: flex;

  /* Entry State: Run when element is injected into DOM or switches from display:none */
  @starting-style {
    opacity: 0;
    transform: translateY(20px);
  }
}

.toast.is-hidden {
  opacity: 0;
  transform: translateY(-20px);
  display: none; /* Because we use allow-discrete, it waits 0.5s before applying this! */
}
```

### 8.2 Advanced Animation & Scroll Architectures
When managing scroll animations, conflicts frequently arise between native CSS, smooth-scrolling libraries (like Lenis), and animation engines (like GSAP).

#### 8.2.1 Native CSS Scroll-Driven Animations

Scroll-driven CSS can replace many purely visual intersection animations. `IntersectionObserver` remains appropriate for behavior, analytics, loading, and compatibility fallbacks.

```css
.animate-on-scroll {
  /* Describe what to animate */
  animation: fade-in-up linear both;

  /* Link the animation strictly to the element intersecting the viewport scroll */
  animation-timeline: view();

  /* Start animation when element is 10% from bottom, end when 40% up the screen */
  animation-range: entry 10% cover 40%;
}

@keyframes fade-in-up {
  from {
    opacity: 0;
    transform: translateY(100px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
```

#### 8.2.2 Resolving GSAP vs CSS Conflicts

**CRITICAL RULE:** Avoid having CSS transitions and a JavaScript animation engine compete over the same property at the same time.

- _The Conflict:_ If you set `transition: all 0.3s` in CSS, and then ask GSAP to tween `y: 100`, GSAP updates the inline style on every frame. But CSS tries to _transition_ to each of those frames over 0.3 seconds. The result is massive jitter, lag, and breaking UI.
- _The Fix:_ Segregate your concerns.
  1. CSS handles `:hover` and `:focus-visible` (e.g., `transition: background-color 0.2s`).
  2. GSAP handles scroll position, parallax, and complex sequences (`transform`, `opacity`).
  3. Remove `all` from CSS transitions. Explicitly name the properties (e.g., `transition: color 0.3s;`).

#### 8.2.3 Smooth Scrolling (Lenis Integration)

Native CSS smooth scrolling (`html { scroll-behavior: smooth; }`) is great for anchor links, but rigid. Modern premium sites use virtual scroll (Lenis).

- _Rule:_ If using Lenis, disable `scroll-behavior: smooth` in your CSS, as they will fight each other and cause locking scrollbars.

### 8.3 Custom Cursor Architectures
A premium custom cursor replaces the default OS arrow with a dynamic, highly interactive element.

#### 8.3.1 The Native SVG Pointer Technique

The lightest, most performant way to change the cursor is natively in CSS using a custom SVG.

```css
/* Apply to the entire document */
body {
  /* Standard size, centered hotspot (16 16) */
  cursor:
    url("../assets/icons/custom-cursor.svg") 16 16,
    auto;
}

/* Ensure interactive elements use the pointer variation, or a different SVG! */
a,
button,
[role="button"] {
  cursor:
    url("../assets/icons/cursor-pointer.svg") 16 16,
    pointer;
}
```

#### 8.3.2 The JavaScript Follower (The "Aura" Cursor)

For advanced cursors that lag behind the mouse, invert colors, or expand when hovering elements, you need a fixed DOM element driven by JS.

**The CSS Setup:**

```css
.cursor-follower {
  position: fixed;
  top: 0;
  left: 0;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background-color: white;
  pointer-events: none; /* CRITICAL: Prevents the cursor from blocking clicks! */
  z-index: 9999;

  /* Blend mode inverses the color of whatever is behind it! */
  mix-blend-mode: difference;

  /* CSS transition for Smoothness - handled by JS GSAP preferably, but CSS works for simple setups */
  transition:
    width 0.3s,
    height 0.3s;
}

.cursor-follower.is-hovering {
  width: 80px;
  height: 80px;
  background-color: rgba(255, 255, 255, 0.2);
  backdrop-filter: blur(4px); /* The cursor becomes a magnifying glass! */
}
```

### 8.4 Scroll-Driven Animations Deep Dive
Scroll-linked visual effects were often implemented with JavaScript libraries or observers; poorly designed per-frame handlers could create main-thread work. CSS can bind animation progress to scroll and view timelines without per-frame JavaScript. Browsers may optimize these animations, but compositor/GPU execution depends on the animated properties and implementation.

#### 8.4.1 The `scroll()` Timeline

Links an animation directly to the physical distance a container has scrolled.

```css
.reading-progress-bar {
  /* No duration needed! It's bound to the scroll distance! */
  animation: fill-bar linear;
  animation-timeline: scroll(
    root block
  ); /* Binds to the main window vertical scrollbar */
}

@keyframes fill-bar {
  from {
    width: 0%;
  }
  to {
    width: 100%;
  }
}
```

#### 8.4.2 The `view()` Timeline

Links an animation to an element's _intersection_ with the viewport (When it enters and exits the screen).

```css
.staggered-card {
  animation: slide-in-up linear both;
  /* Triggers when the element intersects the nearest scroll container */
  animation-timeline: view();

### 22.3 Advanced Pseudo-Element Animations

- **`::scroll-marker` / `::scroll-marker-group`**: Natively creates pagination dots for scrollers without JS.
- **`::scroll-button()`**: Natively creates next/prev buttons for scrollers.
- **`::details-content`**: Allows you to finally style and animate the internal container of a `<details>` element (previously impossible).

```css

details::details-content {
  display: block;
  opacity: 0;
  transition: opacity 0.3s, content-visibility 0.3s allow-discrete;
}
details[open]::details-content {
  opacity: 1;
}

```
```

### 8.5 CSS Motion Path Animation
Allows elements to be animated along complex, arbitrary vector paths natively in CSS without relying on heavy JS libraries like GSAP or Three.js. Includes properties like `offset-path`, `offset-distance`, and `offset-position`.

```css
.animated-element {
  /* Define the path */
  offset-path: path("M20,20 C20,100 200,0 200,100");
  /* Animate the distance traveled along that path */
  animation: moveAlongPath 5s linear infinite alternate;
}

@keyframes moveAlongPath {
  from { offset-distance: 0%; }
  to   { offset-distance: 100%; }
}
```

### 8.6 Cutting-Edge Web Features (2024-2026 Expansion)
#### 8.6.1 Field Sizing & Animate-to-Auto (2025)

##### `field-sizing: content`

Auto-resize inputs and textareas based on content.

```css
textarea.auto-grow {
  field-sizing: content;
  min-height: 2.5rem;
  max-height: 20rem;
  resize: none;
}

input.auto-width {
  field-sizing: content;
  min-width: 3ch;
  width: auto;
}
```

##### `interpolate-size: allow-keywords`

Animate height/width from 0 to auto natively.

```css
:root {
  interpolate-size: allow-keywords;
}

.accordion-body {
  height: 0;
  overflow: hidden;
  transition: height 0.4s ease-out;
}

.accordion-body.is-open {
  height: auto;
}
```

##### `transition-behavior: allow-discrete`

Transition display: none with fade effects.

```css
.toast {
  transition:
    opacity 0.5s,
    transform 0.5s,
    display 0.5s allow-discrete;
  
  opacity: 1;
  transform: translateY(0);
  display: flex;
  
  @starting-style {
    opacity: 0;
    transform: translateY(20px);
  }
}

.toast.is-hidden {
  opacity: 0;
  transform: translateY(-20px);
  display: none;
}
```

##### `@view-transition` — Cross-Document Transitions

Enable smooth page-to-page transitions in MPAs.

```css
@view-transition {
  navigation: auto;
}

::view-transition-old(section-content) {
  animation: vt-out 0.3s ease forwards;
}

::view-transition-new(section-content) {
  animation: vt-in 0.3s ease forwards;
}

@keyframes vt-out {
  to { opacity: 0; transform: translateX(-20px); }
}

@keyframes vt-in {
  from { opacity: 0; transform: translateX(20px); }
}
```

##### Native CSS Carousel, Scroll Markers & Scroll-Spy

Native, accessible carousels and scroll-spy navigation without heavy JS libraries. Core primitives:

| Primitive | Role |
|-----------|------|
| `::scroll-button(left\|right\|…)` | Previous/next controls generated by the scroller |
| `::scroll-marker` / `::scroll-marker-group` | Pagination dots / tab-like markers per scroll item |
| `:target-current` | Styles the marker for the currently snapped/visible item |
| `scroll-target-group` | Groups in-page targets for scroll-spy / mutual exclusivity of `:target-current` |
| `scroll-marker-group` | Places the marker group (`before` / `after`) relative to the scroller |

```html
<nav class="toc" style="scroll-target-group: auto">
  <a href="#intro">Intro</a>
  <a href="#features">Features</a>
  <a href="#pricing">Pricing</a>
</nav>
<section id="intro">…</section>
<section id="features">…</section>
<section id="pricing">…</section>
```

```css
/* Carousel scroller */
.carousel {
  display: flex;
  overflow-x: auto;
  scroll-snap-type: x mandatory;
  scroll-behavior: smooth;
  scroll-marker-group: after;
  scrollbar-width: none;
}

.carousel-slide {
  flex: 0 0 100%;
  scroll-snap-align: start;
}

/* Generated prev/next — keyboard-friendly, no extra DOM */
.carousel::scroll-button(left),
.carousel::scroll-button(right) {
  content: '';
  width: 2.5rem;
  height: 2.5rem;
  border-radius: 999px;
  border: 1px solid var(--border);
  background: var(--surface);
  cursor: pointer;
}
.carousel::scroll-button(left) { content: '←'; }
.carousel::scroll-button(right) { content: '→'; }
.carousel::scroll-button(left):disabled,
.carousel::scroll-button(right):disabled {
  opacity: 0.35;
  cursor: not-allowed;
}

.carousel::scroll-marker-group {
  display: flex;
  gap: 0.4rem;
  justify-content: center;
  padding-top: 0.75rem;
}

.carousel-slide::scroll-marker {
  content: '';
  width: 6px;
  height: 6px;
  border-radius: 50%;
  background: var(--mid);
  cursor: pointer;
}

.carousel-slide::scroll-marker:target-current {
  background: var(--accent);
  width: 18px;
  border-radius: 3px;
}

/* Scroll-spy: highlight the nav link for the section currently in view */
.toc a:target-current {
  color: var(--accent);
  font-weight: 600;
  text-decoration: underline;
}
```

**A11y notes:** Prefer real content slides (not decorative-only). Respect `prefers-reduced-motion` by setting `scroll-behavior: auto` under reduced motion.

##### `::highlight()` API

Custom selection and search highlighting.

```css
::highlight(search) {
  background-color: oklch(85% 0.15 90);
  color: oklch(40% 0.2 50);
}

::highlight(keyword) {
  background-color: oklch(30% 0.15 280 / 0.4);
  color: oklch(75% 0.18 300);
}
```

##### `clip-path: shape()`

Draw custom shapes with path syntax.

```css
.arrow {
  clip-path: shape(
    from top left,
    hline to 70%,
    vline to 30%,
    hline to 100%,
    vline to 50%,
    hline to 100%,
    vline to 70%,
    hline to 70%,
    vline to 100%,
    hline to 0%,
    close
  );
}

.badge {
  clip-path: shape(
    from 50% 0%,
    curve to 100% 50% with 100% 15%,
    curve to 50% 100% with 100% 85%,
    curve to 0% 50% with 0% 85%,
    curve to 50% 0% with 0% 15%,
    close
  );
}
```

---

## 9. Accessibility, Focus, Input Modality, Reading Order, and Motion Preferences

Focus indicators are functional UI, not decoration. Keep a visible fallback for focused controls, then use `:focus-visible` to apply a stronger modality-aware treatment without assuming that keyboard input is the only case in which the browser may request an indicator.

### 9.1 The Focus Hierarchy

- **`:focus`:** Applies whenever an element has focus, regardless of input modality. It is not deprecated and should retain a safe fallback style.
- **`:focus-within` (The Parent Escalator):** Applies to a parent wrapper container if _any_ of its children receive focus.
- **`:focus-visible`:** Applies when the browser's modality heuristics determine that a visible focus indicator is appropriate—commonly for keyboard interaction, but not exclusively or identically in every browser.

### 9.2 Best Practice Implementation

**Rule 1: Keep a safe `:focus` fallback and enhance it with `:focus-visible`.**

```css
/* Keep a visible fallback focus indicator, then enhance keyboard modality. */
:focus {
  outline: 2px solid currentColor;
  outline-offset: 2px;
}

/* Establish the enhanced keyboard focus state. */
:focus-visible {
  outline: 3px solid var(--color-primary);
  outline-offset: 3px; /* Push outline OUTSIDE the element */
  transition: outline-offset 0.1s ease;
  border-radius: 4px; /* Curves the outline ring! */
}
```

**Rule 2: Leverage `:focus-within` for gorgeous forms.**
When building complex UI controls consisting of an wrapper `<div class="input-group">` housing an `<i class="icon">` and `<input>`, you want the entire wrapper to highlight when the user clicks the inner input.

```css
.input-wrapper {
  display: flex;
  align-items: center;
  border: 2px solid var(--border-color);
  background: var(--bg-surface);
  transition: all 0.2s cubic-bezier(0.4, 0, 0.2, 1);
}

.input-wrapper:focus-within {
  /* Highlights the exterior border of the div */
  border-color: var(--color-primary);
  /* Creates a heavy glow emanating inward on the div */
  box-shadow: 0 0 0 4px rgba(var(--color-primary-rgb), 0.1);
}

.input-wrapper i.icon {
  color: var(--text-muted);
}

/* Dynamically color the icon when the adjacent input gains focus */
.input-wrapper:focus-within i.icon {
  color: var(--color-primary);
}

### 7.3 Advanced Accessibility Control

- **`reading-flow`**: Controls the order in which screen readers and tab-navigation process elements, regardless of their visual CSS order (flex/grid).
  - `reading-flow: flex-visual;` (Follows visual order instead of DOM order).
- **`forced-color-adjust`**: Allows opting out of certain elements from the browser's High Contrast Mode to preserve branding where safe.
```

---

## 10. Declarative HTML Components: Dialog, Popover, Details, Datalist, Invokers, and Focus Groups

### 10.1 Advanced Native HTML APIs (No-JS Components)
#### 10.1.1 The Popover API
Allows for native, accessible popups/tooltips on top of everything automatically without z-index hunting.

```html
<!-- The Trigger -->
<button popovertarget="my-popover">Open Settings</button>

<!-- The Popover -->
<div id="my-popover" popover>
  <h2>Settings</h2>
  <p>Select your preferences...</p>
  <button popovertarget="my-popover" popovertargetaction="hide">Close</button>
</div>
```

#### 10.1.2 The Dialog API
A native modal layer with an innate `::backdrop`.

```html
<dialog id="modalDialog">
  <form method="dialog">
    <p>Are you sure you want to delete this?</p>
    <button>Close</button>
  </form>
</dialog>

<style>
/* Style the dimming backdrop layer natively */
dialog::backdrop {
  background: rgba(0, 0, 0, 0.7);
  backdrop-filter: blur(5px);
}
</style>

<script>
  // Recommended approach: .showModal() creates the strict backdrop/focus trap
  document.getElementById('modalDialog').showModal(); 
</script>
```

#### 10.1.3 Modern Autocomplete (`<datalist>`)
Natively providing a dropdown list of specific options to a standard text input element.

```html
<label for="browser">Choose a browser:</label>
<input list="browsers" name="browser" id="browser">
<datalist id="browsers">
  <option value="Edge">
  <option value="Firefox">
  <option value="Chrome">
  <option value="Opera">
  <option value="Safari">
</datalist>
```

### 10.2 Invoker Commands: Declarative Action Handling
Eliminate boilerplate JS event listeners for common UI actions (modals, popovers, custom commands). **Reached multi-engine Baseline track in early 2026 (Interop); still progressive-enhance older browsers.**

#### 10.2.1 Core Attributes

| Attribute | Role |
|-----------|------|
| `commandfor` | ID of the target element (like `popovertarget` / `form`) |
| `command` | Built-in or custom action string |

```html
<!-- Open modal — zero JS -->
<button type="button" commandfor="confirm" command="show-modal">Delete</button>

<dialog id="confirm" closedby="any">
  <p>Delete this item permanently?</p>
  <button type="button" commandfor="confirm" command="close">Cancel</button>
  <button type="button" commandfor="confirm" command="close" value="ok">Confirm</button>
</dialog>

<!-- Popover toggle without popovertarget -->
<button type="button" commandfor="menu" command="toggle-popover">Menu</button>
<div id="menu" popover>
  <button type="button" commandfor="menu" command="hide-popover">Close</button>
</div>
```

#### 10.2.2 Built-in Command Values

| `command` | Typical target | Effect |
|-----------|----------------|--------|
| `show-modal` | `<dialog>` | `showModal()` |
| `close` | `<dialog>` | `close()` |
| `request-close` | `<dialog>` | Soft close request (respects `closedby`) |
| `show-popover` | `[popover]` | `showPopover()` |
| `hide-popover` | `[popover]` | `hidePopover()` |
| `toggle-popover` | `[popover]` | `togglePopover()` |
| `--custom-name` | any | Fires `command` event for custom handlers |

#### 10.2.3 Custom Commands + Progressive Enhancement

```html
<button type="button" commandfor="player" command="--play-pause">Play</button>
<div id="player" data-state="paused"></div>

<script>
  document.getElementById('player').addEventListener('command', (e) => {
    if (e.command === '--play-pause') {
      // Custom invoker command — still declarative wiring from the button
      e.source; // the button that invoked
      togglePlayback(e.currentTarget);
    }
  });
</script>
```

**Accessibility:** Prefer real `<button type="button">` invokers. Native dialog/popover semantics still apply to the target; invokers only wire activation.

#### 10.2.4 Dialog Light Dismiss — `closedby`

Controls how a `<dialog>` can be dismissed without imperative JS. Complements Invoker Commands and brings popover-like light-dismiss options to modals.

| Value | Behavior |
|-------|----------|
| `none` | Only programmatic / form `method="dialog"` / explicit close — **no** ESC, **no** outside click |
| `closerequest` | Platform close request (typically ESC / OS back) — **no** light-dismiss outside click |
| `any` | ESC **and** outside-click light dismiss (popover-like) |

```html
<!-- Strict confirm: user must press a button -->
<dialog id="strict" closedby="none">…</dialog>

<!-- ESC allowed, not outside click -->
<dialog id="form-dlg" closedby="closerequest">…</dialog>

<!-- Full light dismiss -->
<dialog id="info" closedby="any">…</dialog>
```

```css
dialog {
  transition:
    opacity 0.25s,
    transform 0.25s,
    display 0.25s allow-discrete,
    overlay 0.25s allow-discrete;
}
dialog[open] {
  opacity: 1;
  transform: scale(1);
}
@starting-style {
  dialog[open] {
    opacity: 0;
    transform: scale(0.96);
  }
}
```

#### 10.2.5 `popover="hint"` + Interest Invokers (`interestfor`)

| API | Purpose |
|-----|---------|
| `popover="auto"` | Standard light-dismiss popover; one auto at a time |
| `popover="manual"` | Explicit show/hide only; multiple allowed |
| `popover="hint"` | Ephemeral tooltips/hints — does **not** force-dismiss other auto popovers |
| `interestfor` | Declarative “interest” (hover/focus/long-press style) targeting a hint/popover |

```html
<button type="button" interestfor="tip-save" aria-describedby="tip-save">
  Save
</button>
<div id="tip-save" popover="hint" role="tooltip">
  Saves the draft (Ctrl+S)
</div>

<button type="button" popovertarget="full-menu">Open menu</button>
<div id="full-menu" popover="auto" role="menu">…</div>
<!-- Opening the menu does not necessarily kill the hint popover -->
```

**Use cases:** Accessible tooltips, teaching hints beside dense admin UI, chart point labels. Pair with CSS Anchor Positioning for placement.

#### 10.2.6 Exclusive Accordions — `<details name>`

Native mutually exclusive disclosure groups (no JS radio accordion).

```html
<details name="settings" open>
  <summary>Account</summary>
  <p>Profile fields…</p>
</details>
<details name="settings">
  <summary>Billing</summary>
  <p>Payment methods…</p>
</details>
<details name="settings">
  <summary>Security</summary>
  <p>2FA options…</p>
</details>
```

```css
details::details-content {
  transition:
    content-visibility 0.3s allow-discrete,
    height 0.3s,
    opacity 0.3s;
}
```

---

## 11. Modern JavaScript Language and Built-Ins

### 11.1 Modern Vanilla JavaScript Patterns
1. **Prefer semantic state over scattered presentation writes:** Use classes, data attributes, native element state, or CSS custom properties for reusable UI states. Direct style writes are still appropriate for genuinely dynamic values, but avoid mixing behavior and presentation unnecessarily.
2. **CSS Variable Bridge:** When complex JS logic is required (e.g., tracking mouse X/Y coordinates), feed that data directly into a CSS Variable and let CSS do the styling.
   ```javascript
   document.addEventListener("mousemove", (e) => {
     document.body.style.setProperty("--mouse-x", `${e.clientX}px`);
     document.body.style.setProperty("--mouse-y", `${e.clientY}px`);
   });
   ```
   ```css
   /* CSS uses the variable dynamically! */
   .cursor-glow {
     transform: translate(var(--mouse-x), var(--mouse-y));
   }
   ```
3. **Data Attributes (`data-*`) for State:** Map complex state logic to data attributes.
   ```javascript
   button.dataset.status = "loading"; // Renders as <button data-status="loading">
   ```
   ```css
   button[data-status="loading"] {
     pointer-events: none;
     opacity: 0.7;
   }
   ```

4. **Iterator Helpers (2025):** Chainable operations on iterators without intermediate arrays.
   ```javascript
   const squares = [1, 2, 3, 4, 5]
     .values()
     .map(x => x * x)
     .filter(x => x > 10)
     .take(2)
     .toArray(); // [16, 25]
   ```

5. **Set Methods (2025):** Native set operations for better data structure handling.
   ```javascript
   const a = new Set([1, 2, 3]);
   const b = new Set([3, 4, 5]);

a.union(b);        // Set {1, 2, 3, 4, 5}
   a.intersection(b); // Set {3}
   a.difference(b);   // Set {1, 2}
   a.symmetricDifference(b); // Set {1, 2, 4, 5}
   a.isSubsetOf(b);   // false
   ```

6. **Promise.try() (2025):** Handle sync/async code uniformly.
   ```javascript
   Promise.try(() => {
     const data = loadData(); // May be sync or async
     return processData(data);
   }).catch(handleError);
   ```

7. **RegExp.escape() (2025):** Safely escape special regex characters.
   ```javascript
   const userInput = "How much $ for 1+1?";
   const safe = RegExp.escape(userInput);
   // "How much \\$ for 1\\+1\\?"
   const regex = new RegExp(safe, 'g');
   ```

8. **Array Grouping (2025):**
   ```javascript
   const grouped = Object.groupBy(items, item => item.category);
   const mapped = Map.groupBy(items, item => [item.key, item.value]);
   ```

### 11.2 Modern JavaScript Language Features
Vanilla JavaScript has rendered massive libraries like Moment.js, Lodash, and Redux completely obsolete via native memory-efficient implementations.

#### 11.2.1 The Temporal API (Replacing Date & Moment.js)

The legacy `Date` object is mutable and makes timezone-aware calendar logic difficult; it does represent instants and local/UTC views, but lacks Temporal's dedicated date/time types. `Temporal` is immutable, strictly typed, and timezone aware.

```javascript
// Native implementation without Day.js or Moment.js
const now = Temporal.Now.zonedDateTimeISO();
const tomorrow = now.add({ days: 1 });
const timeUntil = now.until(tomorrow); // Returns a strict Temporal.Duration
```

#### 11.2.2 Advanced Set Mathematics (Replacing Lodash)

Sets now have native V8-optimized C++ implementations for mathematical operations.

```javascript
const groupA = new Set([1, 2, 3]);
const groupB = new Set([3, 4, 5]);

const union = groupA.union(groupB); // [1, 2, 3, 4, 5]
const overlap = groupA.intersection(groupB); // [3]
const unique = groupA.difference(groupB); // [1, 2]
```

#### 11.2.3 Iterator Helpers (Zero Memory Overload)

Handling arrays with 1,000,000 items using `.filter().map()` historically crashed the browser because it created a new duplicate array in memory on each step. Iterator helpers process data _lazily_, one at a time.

```javascript
const massiveData = [
  /* 1 million records */
];
const iterator = massiveData.values();

// Evaluates instantly without duping memory. Only processes what is actually consumed.
const result = iterator
  .filter((x) => x.active)
  .take(5)
  .toArray();
```

#### 11.2.4 Reactive Signals (Replacing Framework State)

A TC39 proposal explores interoperable reactive primitives. It is not yet a universally available built-in and does not by itself replace framework state-management architectures.

```javascript
// A low-level primitive for building UIs that automatically update when variables change.
// Illustrative only: the TC39 Signals proposal is not a universal web standard.
// Use the syntax documented by the selected implementation or framework,
// and do not ship this pseudocode without a fallback or library.
const counter = createSignal(0);
const isEven = createComputed(() => counter.get() % 2 === 0);
```

#### 11.2.5 Resource Management (`using`)
Explicitly manage resource cleanup (like DB connections or file handles) natively.

```javascript
{
  await using connection = await db.connect();
  // connection is automatically closed when block scope ends!
}
```

#### 11.2.6 The Navigation API
A modern, unified replacement for `window.history` that actually understands single-page navigation.

```javascript
navigation.addEventListener('navigate', (event) => {
  if (shouldIntercept(event)) {
    event.intercept({
      async handler() {
        await updateThePageContent();
      }
    });
  }
});
```

#### 11.2.7 Esoteric Primitive Enhancements
- **`Promise.try()`**: Wraps synchronous code in a promise chain safely.
- **`RegExp.escape()`**: Natively escapes special characters for regex (e.g., `RegExp.escape("https://google.com")`).
- **`Float16Array`**: Memory-efficient 16-bit floating point numbers for heavy math/WebGL.
- **Import Attributes**: Native JSON/CSS imports: `import data from './meta.json' with { type: 'json' };`

#### 11.2.8 Non-Mutating Array Methods (ES2023)
Produce a new array instead of modifying the original.

```javascript
const sorted = arr.toSorted();
const reversed = arr.toReversed();
const spliced = arr.toSpliced(1, 1, 'new');
```

#### 11.2.9 New Static Creation Methods
- **`Array.fromAsync()`**: Creates an array from an async iterable or array-like source; verify support in your target engines.
- **`Iterator.from()`**: Wraps an iterable in an Iterator object with helper methods.
- **No standard `Set.from()` exists:** use `new Set(iterable)` unless a future proposal is standardized.

### 11.3 Modern JavaScript Data Structures & APIs (ES2024+)
#### 11.3.1 `Object.groupBy()` and `Map.groupBy()`
Natively grouping array or set elements by a given property without using complex string mapping or reduce loops.

```javascript
const inventory = [
  { name: 'asparagus', type: 'vegetables', quantity: 9 },
  { name: 'bananas', type: 'fruit', quantity: 5 },
  { name: 'goat', type: 'meat', quantity: 23 },
  { name: 'cherries', type: 'fruit', quantity: 12 },
  { name: 'fish', type: 'meat', quantity: 22 }
];

const result = Object.groupBy(inventory, ({ type }) => type);
// Use Map.groupBy(...) when keys should not be coerced to property keys.
/* Result:
{
  vegetables: [{ name: 'asparagus', type: 'vegetables', quantity: 9 }],
  fruit: [{ name: 'bananas', type: 'fruit', quantity: 5 }, { name: 'cherries', type: 'fruit', quantity: 12 }],
  meat: [{ name: 'goat', type: 'meat', quantity: 23 }, { name: 'fish', type: 'meat', quantity: 22 }]
}
*/
```

#### 11.3.2 `Promise.withResolvers()`
Bypasses the awkward Promise instantiation structure by immediately exposing the promise and its resolver/rejector functions into local scope.

```javascript
// Creates a promise mapping to a deferred action outside standard closures
const { promise, resolve, reject } = Promise.withResolvers();

// Usage outside the instantiation map
setTimeout(() => resolve("Task Completed"), 2000);

promise.then(console.log);
```

#### 11.3.3 RegExp 'v' Flag (Unicode sets mode)
Allows operations on character classes natively, including unions, intersections, and set subtractions.

```javascript
// Match letter characters
const regexV = /[\p{Letter}]/v;
console.log(regexV.test('Z')); // true
```

### 11.4 Additional JavaScript Built-Ins
#### 11.4.1 The Temporal API
Replacing `Date` and `Moment.js` with strictly immutable, timezone-aware objects.

```javascript
const now = Temporal.Now.zonedDateTimeISO();
const tomorrow = now.add({ days: 1 });
```

#### 11.4.2 Set Mathematics & Iterator Helpers
Natively perform Set operations and lazy data processing.
- `groupA.union(groupB)`, `groupA.intersection(groupB)`, `groupA.difference(groupB)`.
- `iterator.filter().take(5).toArray()`: Zero-memory duplicate processing.

#### 11.4.3 Non-Mutating Array Methods (ES2023)

### 11.5 ES2025/2026 JavaScript Features
#### 11.5.1 Pattern Matching (`match`/`case`)

**Status:** ES2026 — Rolling out in browsers 2026.

```javascript
const result = match(value) {
  when 0 => 'zero',
  when 1 => 'one',
  when { type: 'success', data } => `Success: ${data}`,
  when { type: 'error', code } => `Error ${code}`,
  when [first, ...rest] => `Array with ${rest.length + 1} elements`,
  when null || undefined => 'No value',
  else => `Default: ${value}`
};

// With guards
const httpStatus = match(statusCode) {
  when code if code >= 200 && code < 300 => 'Success',
  when code if code >= 400 && code < 500 => 'Client Error',
  when code if code >= 500 => 'Server Error',
  else => 'Unknown'
};
```

#### 11.5.2 Record & Tuple (Immutable Data Structures)

**Status:** ES2026 — Stage 3 proposal.

```javascript
// Record: Immutable object
const config = #{ theme: 'dark', language: 'en' };

// Tuple: Immutable array
const coordinates = #[10, 20, 30];

// Structural equality
const config2 = #{ theme: 'dark', language: 'en' };
console.log(config === config2); // true!
```

#### 11.5.3 Pipeline Operator (`|>`)

**Status:** ES2026 — Stage 3 proposal.

```javascript
const result = users
  |> filterActive
  |> toUpperCase
  |> trim;

const total = items
  |> filter(item => item.active)
  |> map(item => item.price)
  |> reduce((sum, price) => sum + price, 0);
```

#### 11.5.4 `Float16Array` (ES2025)

**Status:** Baseline 2025 — Chrome 123+, Firefox 124+, Safari 17.4+.

```javascript
// 50% smaller than Float32Array
const positions = new Float16Array([1.5, 2.7, 3.14, -0.5]);
const imageData = new Float16Array(width * height * 4); // RGBA pixels
```

#### 11.5.5 `using` Keyword (ES2026)

**Status:** limited availability in the July 2026 support snapshot; feature-detect or compile only when your runtime supports the syntax.

```javascript
// Automatic resource cleanup
{
  await using file = await openFile('data.txt');
  const content = await file.read();
  // file automatically closed when exiting scope
}

// Multiple resources
{
  await using db = await connectDatabase();
  await using transaction = await db.beginTransaction();
  await transaction.execute('INSERT...');
  // Both cleaned up automatically
}
```

#### 11.5.6 Import Attributes (ES2025)

**Status:** JSON import attributes are broadly available in the stated support snapshot; CSS module import attributes are not equivalently interoperable. Check the exact imported module type and target engines.

```javascript
// Import JSON securely
import config from './config.json' with { type: "json" };

// Import CSS as stylesheet
// CSS module scripts are not universally interoperable; feature-detect or use a build/tooling fallback.
// import styles from './styles.css' with { type: "css" };

// Dynamic imports
const data = await import('./data.json', { with: { type: "json" } });
```

#### 11.5.7 `Array.fromAsync()` (ES2026)

**Status:** ES2026 — shipping / rolling out mid-2026.

```javascript
async function* fetchPages(urls) {
  for (const url of urls) {
    yield fetch(url).then(r => r.json());
  }
}

const data = await Array.fromAsync(fetchPages(['/api/1', '/api/2']));
// Optional map callback (like Array.from)
const texts = await Array.fromAsync(stream, async (chunk) => chunk.toString());
```

#### 11.5.8 `Error.isError()` (ES2026)

Reliable cross-realm error detection — safer than `instanceof Error` (which fails across iframes/realms).

```javascript
function report(err) {
  if (Error.isError(err)) {
    console.error(err.name, err.message, err.stack);
  } else {
    console.error('Non-error throw:', err);
  }
}

try {
  throw 'oops'; // not an Error instance
} catch (e) {
  Error.isError(e); // false
}
```

#### 11.5.9 `Math.sumPrecise()` (ES2026)

Accurate summation that reduces floating-point accumulation error vs. naive `reduce((a,b)=>a+b, 0)`.

```javascript
// Classic float trap:
[0.1, 0.2, 0.3].reduce((a, b) => a + b, 0); // 0.6000000000000001

Math.sumPrecise([0.1, 0.2, 0.3]); // 0.6

// Finance / analytics totals, chart series, unit conversions
const total = Math.sumPrecise(lineItems.map((i) => i.amount));
```

#### 11.5.10 Map / WeakMap Upsert — `getOrInsert()` / `getOrInsertComputed()` (ES2026)

Simplified population of `Map` **and** `WeakMap` without the get-or-create boilerplate. Atomic “retrieve or initialize” in one step.

```javascript
const cache = new Map();
const perElement = new WeakMap();

// Insert only if missing; always return the stored value
const session = cache.getOrInsert('user:42', { hits: 0 });

// Compute only when missing (lazy expensive default)
const bucket = cache.getOrInsertComputed('group:admin', (key) => {
  return loadGroup(key); // runs once
});

// WeakMap: associate state with DOM nodes without leaking memory
function getWidgetState(el) {
  return perElement.getOrInsertComputed(el, () => ({
    open: false,
    retries: 0,
  }));
}

// Classic pattern replaced:
// if (!map.has(k)) map.set(k, defaultValue);
// return map.get(k);
```

#### 11.5.11 `Uint8Array` Base64 & Hex (ES2026)

Native binary ↔ text codecs without `btoa`/`atob` hacks or third-party libs.

```javascript
const bytes = new TextEncoder().encode('hello world');

const b64 = bytes.toBase64();           // "aGVsbG8gd29ybGQ="
const hex = bytes.toHex();              // "68656c6c6f20776f726c64"

const fromB64 = Uint8Array.fromBase64(b64);
const fromHex = Uint8Array.fromHex(hex);

// Options (alphabet / padding) per spec when available:
// bytes.toBase64({ alphabet: 'base64url', omitPadding: true });
```

**Use cases:** WebCrypto payloads, data URLs, checksum display, compact storage keys.

#### 11.5.12 `Iterator.concat()` (ES2026 Sequencing)

Combine multiple iterables lazily without allocating intermediate arrays.

```javascript
function* odds() { yield 1; yield 3; yield 5; }
function* evens() { yield 2; yield 4; }

const mixed = Iterator.concat(odds(), evens(), [6, 7]);
[...mixed]; // [1, 3, 5, 2, 4, 6, 7]

// Pipeline with iterator helpers (ES2025):
const firstThree = Iterator.concat(a, b)
  .filter((n) => n > 0)
  .take(3)
  .toArray();
```

#### 11.5.13 JSON Improvements (ES2026)

Source-text access in the reviver path and raw JSON fragments.

```javascript
// JSON.rawJSON — preserve a pre-serialized JSON value through stringify
const rawId = JSON.rawJSON('9007199254740993'); // big integer as raw digits
JSON.stringify({ id: rawId }); // {"id":9007199254740993} — no precision loss

// Reviver can inspect source text of the value being parsed (where supported)
JSON.parse(payload, (key, value, context) => {
  // context.source → original source text for this value (ES2026)
  if (key === 'id' && context?.source) {
    return BigInt(context.source);
  }
  return value;
});
```

#### 11.5.14 ES2025 Recap (Stable Set / Iterator / Promise)

Already documented earlier; keep as the Baseline core:

| Feature | Role |
|---------|------|
| Set: `union`, `intersection`, `difference`, `symmetricDifference`, `isSubsetOf`, `isSupersetOf`, `isDisjointFrom` | Set algebra |
| Iterator helpers: `map`, `filter`, `take`, `drop`, `flatMap`, `reduce`, `toArray`, `some`, `every`, `find` | Lazy pipelines |
| `Promise.try()` | Sync throw + async reject in one chain |
| `RegExp.escape()` | Safe dynamic regex from user input |
| Import attributes `with { type: "json" }` | Native JSON/CSS modules |
| `Float16Array` | Half-precision typed arrays |

#### 11.5.15 Temporal API — Modern date/time types

The legacy `Date` object is mutable, timezone-hostile, and month-index quirky. **Temporal** is the modern replacement: immutable, precise, and explicit about calendar/time-zone semantics.

**Status (10 July 2026):** Temporal reached **TC39 Stage 4 on 21 May 2026**. The support snapshot in this guide records Chrome 144 and Firefox 139, with Safari still missing complete support. Feature-detect `globalThis.Temporal`; use a maintained polyfill when required, and verify the exact Node.js/V8 release used in deployment.

| Type | Use for |
|------|---------|
| `Temporal.PlainDate` | Calendar date only (no time, no zone) |
| `Temporal.PlainTime` | Wall-clock time only |
| `Temporal.PlainDateTime` | Date + time, no zone |
| `Temporal.ZonedDateTime` | Instant in a specific IANA zone |
| `Temporal.Instant` | Exact UTC nanosecond instant |
| `Temporal.Duration` | Elapsed spans (add/until/since) |
| `Temporal.Now.*` | Current instant / plain / zoned values |

```javascript
const now = Temporal.Now.zonedDateTimeISO(); // system zone
const festival = Temporal.PlainDate.from('2026-10-20');
const inTwoWeeks = festival.add({ days: 14 });
const duration = festival.until(inTwoWeeks); // Temporal.Duration

const meeting = Temporal.ZonedDateTime.from(
  '2026-07-10T09:30:00[Asia/Kolkata]'
);
const inNy = meeting.withTimeZone('America/New_York');

// Never mutates the original — every op returns a new object
```

**Feature-detect:** `typeof Temporal !== 'undefined'`. Use a maintained polyfill or a runtime whose Temporal support you have verified when all deployment targets do not provide it.

---

## 12. Web Components, DOM, Graphics, File-System, and Platform APIs

### 12.1 WebGPU & Graphics APIs
**Support status:** WebGPU support is platform- and implementation-dependent and remains uneven across engines and operating systems in this dated snapshot. Feature-detect `navigator.gpu`, handle a missing adapter, test required limits/features, and provide a non-WebGPU fallback.

```javascript
// Initialize WebGPU
const adapter = await navigator.gpu.requestAdapter();
const device = await adapter.requestDevice();

// Create shader module
const shader = device.createShaderModule({
  code: `
    @vertex
    fn vs(@builtin(vertex_index) vi: u32) -> @builtin(position) vec4<f32> { }
    @fragment
    fn fs() -> @location(0) vec4<f32> { }
  `
});

// Create render pipeline
const pipeline = device.createRenderPipeline({
  layout: 'auto',
  vertex: { module: shader, entryPoint: 'vs' },
  fragment: { module: shader, entryPoint: 'fs', targets: [{ format: 'bgra8unorm' }] }
});
```

**Use Cases:**
- 3D Graphics: Games, data visualization, CAD
- Machine Learning: TensorFlow.js backend, on-device inference
- Image/Video Processing: Filters, encoding, computer vision
- Scientific Computing: Simulations, numerical analysis

### 12.2 File System Access API
**Browser Support:** Chrome 86+, Edge 86+ — Firefox/Safari under consideration.

#### 12.2.1 Reading Files

```javascript
async function readFile() {
  const [fileHandle] = await window.showOpenFilePicker({
    types: [{ description: 'Text Files', accept: { 'text/plain': ['.txt'] } }]
  });
  const file = await fileHandle.getFile();
  const contents = await file.text();
}
```

#### 12.2.2 Writing Files

```javascript
async function writeFile() {
  const fileHandle = await window.showSaveFilePicker({
    suggestedName: 'document.txt',
    types: [{ description: 'Text Files', accept: { 'text/plain': ['.txt'] } }]
  });
  const writable = await fileHandle.createWritable();
  await writable.write('Hello, File System!');
  await writable.close();
}
```

#### 12.2.3 Origin Private File System (OPFS)

```javascript
// Get root directory of OPFS
const root = await navigator.storage.getDirectory();

// Create a file
const fileHandle = await root.getFileHandle('data.db', { create: true });
const writable = await fileHandle.createWritable();
await writable.write('Binary data...');
await writable.close();
```

### 12.3 Shadow DOM & Web Components Architecture
Web Components allow you to create reusable, encapsulated UI elements that work in any framework (or no framework at all).

#### 12.3.1 The Shadow DOM Triple

1.  **Shadow Host:** The regular DOM element that contains the shadow DOM.
2.  **Shadow Root:** The root node of the shadow tree (`attachShadow({mode: 'open'})`).
3.  **Shadow Tree:** The encapsulated DOM tree inside the shadow root.

#### 12.3.2 CSS Selectors for Shadow DOM

-   **`:host`**: Selects the shadow host itself.
-   **`:host(selector)`**: Selects the host only if it matches a specific selector.
-   **`:host-context(selector)`**: Styles the host based on its ancestors (useful for theme-aware components).
-   **`::slotted(selector)`**: Styles elements that are passed into the component via a `<slot>`.

```css
:host {
  display: block;
  background: var(--component-bg, #eee);
}
:host-context(.dark-theme) {
  --component-bg: #333;
}
::slotted(span) {
  font-weight: bold;
}
```

#### 12.3.3 Lifecycle Callbacks

-   `connectedCallback()`: Component added to DOM.
-   `disconnectedCallback()`: Component removed from DOM.
-   `attributeChangedCallback(name, old, new)`: Observed attribute changed.
-   `static get observedAttributes()`: Returns an array of attributes to watch.

#### 12.3.4 Complete Shadow DOM JavaScript API

```javascript
class MyComponent extends HTMLElement {
  constructor() {
    super();
    this.shadow = this.attachShadow({
      mode: 'open',
      delegatesFocus: true
    });
  }

  connectedCallback() {
    this.render();
    this.setupEventListeners();
  }

  disconnectedCallback() {
    this.cleanup();
  }

  static get observedAttributes() {
    return ['data-value', 'disabled'];
  }

  attributeChangedCallback(name, oldValue, newValue) {
    if (name === 'data-value') {
      this.updateValue(newValue);
    }
  }

  render() {
    this.shadow.innerHTML = `
      <style>
        :host {
          display: block;
          --primary-color: blue;
        }
        :host(.active) {
          border: 2px solid red;
        }
        :host-context(.dark-theme) {
          background: black;
          color: white;
        }
        ::slotted(span) {
          font-weight: bold;
        }
      </style>
      <slot name="title">Default Title</slot>
      <slot>Default content</slot>
    `;
  }

  setupEventListeners() {
    this.shadow.addEventListener('click', this.handleClick.bind(this));
    
    this.dispatchEvent(new CustomEvent('componentReady', {
      detail: { component: this },
      bubbles: true,
      composed: true
    }));
  }
}
```

#### 12.3.5 CSS Custom Properties for Theming

```css
/* Inside Shadow DOM */
:host {
  --primary-color: blue;
  --text-size: 16px;
}

.content {
  color: var(--primary-color);
  font-size: var(--text-size);
  background: var(--bg-color, white); /* Fallback */
}

/* From outside */
my-component {
  --primary-color: red;
  --text-size: 20px;
  --bg-color: lightgray;
}
```

#### 12.3.6 Declarative Shadow DOM (SSR without hydration attach)

Shadow roots can be declared in HTML so **servers stream real encapsulated markup** — no client JS required just to call `attachShadow()`. Critical for true SSR of Web Components.

```html
<my-card>
  <template shadowrootmode="open">
    <style>
      :host { display: block; border: 1px solid #ccc; padding: 1rem; }
      ::slotted([slot="title"]) { font-weight: 700; }
    </style>
    <slot name="title"></slot>
    <div class="body"><slot></slot></div>
  </template>

  <h2 slot="title">Server-rendered card</h2>
  <p>This content is projected into the declarative shadow tree.</p>
</my-card>
```

| Attribute | Meaning |
|-----------|---------|
| `shadowrootmode="open"` | Declarative open shadow root (JS can reach `.shadowRoot`) |
| `shadowrootmode="closed"` | Closed root (no open access from outside) |
| `shadowrootdelegatesfocus` | Focus delegation into the shadow tree (boolean attribute form) |
| `shadowrootclonable` / `shadowrootserializable` | Cloning / serialization control (where supported) |

**Rules of thumb:**
- One declarative shadow root per host; subsequent attach attempts follow the HTML processing model.
- Progressive enhance: custom element class still upgrades behavior; markup is already present for SEO/FOUC-free paint.
- Prefer open mode unless you have a hard encapsulation requirement.

### 12.4 Platform Web APIs (2025–mid-2026 Vanilla Renaissance)
These APIs remove entire categories of libraries: navigation speculation, floating windows, close handling, and client-side compression.

#### 12.4.1 Speculation Rules API

Declarative JSON that tells the browser to **prefetch** or **prerender** likely next navigations. Cornerstone of MPA “instant navigation” (also integrated by CMS platforms such as WordPress 6.8+).

```html
<script type="speculationrules">
{
  "prerender": [{
    "source": "document",
    "where": { "href_matches": "/docs/*" },
    "eagerness": "moderate"
  }],
  "prefetch": [{
    "source": "document",
    "where": {
      "and": [
        { "href_matches": "/*" },
        { "not": { "href_matches": "/logout" } },
        { "not": { "href_matches": "/cart/checkout" } }
      ]
    },
    "eagerness": "conservative"
  }]
}
</script>
```

| Eagerness | Typical meaning |
|-----------|-----------------|
| `immediate` | Start ASAP (use sparingly — bandwidth/CPU) |
| `eager` | High confidence next step |
| `moderate` | On hover/pointer-down style signals (UA-dependent) |
| `conservative` | Cautious speculation |

**Rules:** Only same-origin (or carefully allowed) URLs; never prerender logout/mutation endpoints; respect `Save-Data` / user data limits; combine with View Transitions for SPA-like MPAs.

#### 12.4.2 Document Picture-in-Picture API

Unlike video-only PiP, **any HTML** can open in a floating, always-on-top window (custom player chrome, persistent chat, timers, monitoring widgets).

```javascript
async function openFloatingPanel() {
  if (!('documentPictureInPicture' in window)) {
    // Fallback: popover / dialog
    return;
  }
  const pip = await documentPictureInPicture.requestWindow({
    width: 360,
    height: 240,
  });
  // Move or clone UI into the PiP document
  pip.document.body.append(panel.cloneNode(true));
  pip.document.head.append(
    ...[...document.styleSheets].map((s) => s.ownerNode.cloneNode(true))
  );
}
```

**A11y / UX:** Provide an in-page alternative; don’t put critical-only controls exclusively in PiP; handle `pagehide` / window `close` to restore state.

#### 12.4.3 Close Watcher API

Platform-agnostic **close requests**: desktop `Esc`, Android back gesture, etc., unified for dismissing dialogs, drawers, and multi-step stacks.

```javascript
function attachCloseWatcher(onClose) {
  if (typeof CloseWatcher !== 'function') {
    document.addEventListener('keydown', (e) => {
      if (e.key === 'Escape') onClose();
    });
    return { destroy() {} };
  }
  const watcher = new CloseWatcher();
  watcher.addEventListener('close', () => {
    onClose();
    watcher.destroy();
  });
  return watcher;
}

// Nested UIs: create a new CloseWatcher per layer (topmost handles first)
```

Pairs with `<dialog>`, Popover, and Invoker Commands so back/Esc behavior matches native platform expectations.

#### 12.4.4 Compression Streams API

**Baseline Widely Available (late 2025 track):** compress/decompress with `gzip` or `deflate` via WHATWG Streams — ideal for large JSON, binary packs, or offline caches before network transfer.

```javascript
async function gzipString(text) {
  const input = new Blob([text]).stream();
  const compressed = input.pipeThrough(new CompressionStream('gzip'));
  return new Response(compressed).arrayBuffer();
}

async function gunzipToText(buffer) {
  const stream = new Blob([buffer]).stream()
    .pipeThrough(new DecompressionStream('gzip'));
  return new Response(stream).text();
}

// Feature-detect
const canCompress = typeof CompressionStream === 'function';
```

Formats: `'gzip'`, `'deflate'`, `'deflate-raw'` (where supported). Combine with `fetch` request/response streams for end-to-end pipeline processing.

#### 12.4.5 `<search>` Element (Semantic Landmark)

```html
<search>
  <form action="/search" method="get" role="search">
    <label for="q">Search</label>
    <input id="q" name="q" type="search" autocomplete="off">
    <button type="submit">Go</button>
  </form>
</search>
```

Implicit `search` landmark for AT and clearer SEO structure than a bare `<form>`.

---

## 13. Performance, Rendering Containment, Loading Priority, and Speculation

### 13.1 `content-visibility`
Optimizes rendering for off-screen content.

```css
.long-feed { content-visibility: auto; contain-intrinsic-size: 500px; }
```

### 13.2 `fetchPriority`
Hint the browser on resource importance.

```html
<img src="hero.jpg" fetchpriority="high">
```

---

## 14. Advanced Specification Notes, Edge Cases, and Experimental Watchlist

### 14.1 The 2025/2026 Advanced Features: Edge Cases & Advanced APIs
While the previous chapters cover the vast majority of modern CSS, this addendum serves to document the absolute bleeding-edge features and specific architectural synergies that reached maturity in late 2025 and 2026.

#### 14.1.1 ITCSS Architecture Synergy with `@layer`

For years, large-scale projects relied on **ITCSS** (Inverted Triangle CSS) to manage specificity. It structured files logically: Settings -> Tools -> Generic -> Elements -> Objects -> Components -> Trumps (Utilities).

The revolutionary synergy in 2025 is mapping ITCSS directly to CSS Cascade Layers.
Instead of relying on file-load order or hoping developers don't use high-specificity selectors in the "Elements" layer, we hardcode the ITCSS triangle into the engine:

```css
/* The ITCSS pattern codified natively */
@layer generic, elements, objects, components, utilities;

@layer utilities {
  /* Within the declared normal cascade layers, this utility layer outranks earlier component-layer rules regardless of selector specificity. Unlayered rules and !important layer ordering follow separate cascade rules. */
  .text-center {
    text-align: center;
  }
}
```

#### 14.1.2 The `@scope` Deep Dive & Scoping Proximity

While `@scope (.card)` keeps styles contained, the API goes much deeper than simple encapsulation.

**Scope Limits (The "Donut" Scope):**
You can define an upper boundary AND a lower boundary, effectively creating a "donut" of styling that stops at a specific inner element.

```css
/* Styles apply inside .card, but STOP applying the second they hit .card-content */
@scope (.card) to (.card-content) {
  p {
    color: red;
  } /* Will style paragraphs in the card header, but ignore the content body! */
}
```

**Scoping Proximity:**
`@scope` introduces a brand-new rule to the CSS Cascade: **Proximity**. If two scoped styles conflict on an element, the browser calculates the number of DOM hops up to the scope root. The style with the _smallest number of hops_ wins.

**The `:scope` Pseudo-Class:**
Selects the exact root element of the current scope, allowing you to style the container itself cleanly.

```css
@scope (.modal) {
  :scope {
    border: 1px solid gray;
  }
}
```

#### 14.1.3 Advanced Container Queries (Style & Scroll-State)

Beyond querying physics `inline-size`, container queries have evolved to query computed properties and scroll behaviors.

**Style Queries:**
Apply styles based on the computed value of a custom property on the parent:

```css
/* Parent container establishing the variable */
.theme-wrapper {
  --theme: dark;
}

@container style(--theme: dark) {
  .child-card {
    background: black;
    color: white;
  }
}
```

**Scroll-State Queries:**

```css
.scroll-container {
  container-type: scroll-state;
}

/* Apply styles to a child ONLY when its parent is currently being scrolled, or has snapped to a grid! */
@container scroll-state(snapped: block) {
  .snap-indicator {
    opacity: 1;
  }
}
```

#### 14.1.4 Anchor Positioning API

A monumental addition to CSS that eliminates complex JavaScript calculations for placing tooltips, popovers, and dropdown menus relative to trigger buttons.

1. **Define the Anchor Target (The Button):**

```css
.trigger-btn {
  anchor-name: --tooltip-anchor;
}
```

2. **Position the Tooltip:**

```css
.tooltip {
  position: absolute;
  /* Bind the tooltip to the button */
  position-anchor: --tooltip-anchor;
  /* Tell it to sit directly ABOVE the button in the 3x3 grid area! */
  position-area: top;
  /* Fallback: if there's no space on top, try the bottom! */
  position-try-fallbacks: flip-block;
}
```

#### 14.1.5 Next-Gen Text Wrapping Dynamics

Controlling typography line-breaks without manual `<br>` tags is now a native engine feature.

- **`text-wrap: balance`**: Instructs the browser to equalize the line lengths. Perfect for headlines and blockquotes (capped at ~6 lines for performance). It prevents a title from having 5 words on line 1, and 1 word isolated on line 2.
- **`text-wrap: pretty`**: Requests higher-quality line breaking for prose and may reduce short final lines or typographic widows. The exact algorithm is user-agent defined and does not guarantee that every orphan/widow is eliminated.

#### 14.1.6 The View Transitions API (Same-Doc & Cross-Doc)

Smoothly morphing elements between page changes historically required complex React/Vue routing frameworks (`framer-motion`).

- **Same-Document Transitions**: Used for DOM state swaps (e.g., filtering a list, opening a modal). You wrap the JS DOM update in `document.startViewTransition(() => updateDOM())`. The browser takes a screenshot of the old state, updates the DOM instantly, takes a screenshot of the new state, and smoothly cross-fades them through the browser rendering pipeline.
- **Cross-Document Transitions**: Added in 2024/2025, this opts standard Multi-Page Applications (MPA) into transitions when rendering completely new HTML pages from the server!

```css
/* Add this to both pages to enable native cross-fading page navigations! */
@view-transition {
  navigation: auto;
}
```

#### 14.1.7 Custom CSS Functions & Typed Attributes

**The `@function` Rule (limited availability):**
Bringing DRY logic directly to CSS without SCSS mixins.

```css
@function --calculate-fluid-space(--min, --max) {
  result: clamp(var(--min), 5vw, var(--max));
}

.card {
  padding: --calculate-fluid-space(10px, 40px);
}
```

**Enhanced `attr()` Casting:**
Typed `attr()` can parse values beyond strings in supporting engines. Treat it as progressive enhancement until your browser policy includes interoperable support.

```html
<div data-size="400" data-theme="#ff0000"></div>
```

```css
div {
  /* Parses "400" as a pure number, and multiplies it by px! Falls back to 200px if missing. */
  width: calc(attr(data-size type(<integer>), 200) * 1px);

  /* Parses the hex code strictly as an engine color, falling back to blue */
  background: attr(data-theme type(<color>), blue);
}
```

#### 14.1.8 Advanced Border & Outline Control

- **`border-image`**: Use images or gradients as borders with full slicing control.
  - `border-image: linear-gradient(to right, red, blue) 1;`
- **`outline-offset`**: Can take negative values to pull the outline *inside* the element for unique "inner border" effects.
- **`outline-color: Highlight`**: Uses the system's native selection color, ensuring perfect visibility in accessibility/forced-colors modes.
- **`box-shadow` vs `filter: drop-shadow()`**:
  - `box-shadow` follows the rectangular box model.
  - `filter: drop-shadow()` follows the actual alpha transparency of an image or irregular shape.

### 14.2 Specification Edge-Case Reference
This final section covers every esoteric parameter, obscure sub-rule, and bleeding-edge API specifically documented in the 2025/2026 specs, guaranteeing 100% coverage of modern browser engine capabilities.

#### 14.2.1 The Exotic `@` At-Rules

Beyond `@media` and `@container`, the CSS spec contains specialized configuration rules:

- `@color-profile`: Defines a custom color space profile for use within `color()` and `color-mix()` functions.
- `@counter-style`: Allows defining entirely custom bullet points and counter styles for ordered lists (e.g., custom emoji sequences instead of `1, 2, 3`).
- `@font-feature-values`: Provides human-readable names for deeply embedded font feature settings like swashes and historical ligatures.
- `@font-palette-values`: Adjusts the internal color palette used by advanced multi-color fonts (like specific Emoji fonts).
- `@namespace`: Declares an XML namespace, allowing you to target specific XML-based code dialects such as `SVG` or `MathML` seamlessly.
- `@page`: The master controller for Print Layouts (PDF generation).

##### Paged Media Sub-Rules (Print/PDF Engine)

Inside `@page`, a hyper-specific matrix of margin-box at-rules controls print headers, footers, and corners:
`@top-left-corner`, `@top-left`, `@top-center`, `@top-right`, `@top-right-corner`, `@left-top`, `@left-middle`, `@left-bottom`, `@right-top`, `@right-middle`, `@right-bottom`, `@bottom-left-corner`, `@bottom-left`, `@bottom-center`, `@bottom-right`, `@bottom-right-corner`, and `@document`.

#### 14.2.2 Stacking Context Triggers (Z-Index Exits)

Many developers assume only `position: relative|absolute` with `z-index` creates a stacking context. Modern CSS introduces numerous triggers that will trap z-indexes and form a new context shell. By 2025/2026, **any of the following** will create a new context:

1. `opacity` (any value less than 1)
2. `transform` (any value other than none)
3. `filter` (any value)
4. `perspective` (any value)
5. `clip-path` (any value)
6. `display: flex` or `display: grid` combined with a `z-index` other than `auto`
7. `contain: layout` or `contain: paint`
8. `will-change` (any value mapping to a property that creates a context, like transform)
9. `mix-blend-mode` (any value other than `normal`; incidentally, use `plus-lighter` for seamless cross-fading animations to prevent blinking!)
10. `isolation: isolate` (The explicit architectural fix)

#### 14.2.3 The `corner-shape` K-Values (The Superellipse Math)

The `corner-shape` property internally generates geometric bounds using the `superellipse(K)` mathematical function.

- `superellipse(1)` = `round` (The standard border-radius arc).
- `superellipse(2)` = `squircle` (The smooth iOS-style icon blend).
- `superellipse(0)` = `bevel` (A straight diagonal cut / chamfer).
- `superellipse(-1)` = `scoop` (Inward inverted curves).
- `superellipse(-infinity)` = `notch` (A 90-degree inward rectangular bite).
- `superellipse(infinity)` = `square` (Forces sharp 90-degree corners overriding border-radius).

#### 14.2.4 Advanced Scroll-State Tracking

The `@container scroll-state(...)` query tracks two specific dynamic variables:

- `scroll-state(stuck)`: Triggers when a `position: sticky` element finally hits its bounds and physically sticks to the viewport roof.
- `scroll-state(snapped)`: Triggers when CSS Scroll Snapping connects an element securely into its detent layout grid.

#### 14.2.5 Extended Timeline Controls

- `animation-range`: Accepts two points (e.g., `entry 10% cover 40%`) to control exactly when a scroll animation triggers relative to the scrollport.
- `timeline-scope`: If a scroll timeline is declared deep within a descendant, `timeline-scope` hoists it to the parent, allowing completely unrelated sibling DOM elements to animate based on that scroller's position!

#### 14.2.6 The Progressive `:not()` Selector

The negation pseudo-class no longer requires tedious chaining (`:not(.a):not(.b):not(.c)`). Browsers now natively parse selector lists inside the function:

- `:not(a, .b, [c])`: Excludes identical nodes in a single, perfectly optimized pass.

#### 14.2.7 The Typographical Historical Quirks

`text-box-trim` was heavily debated by the W3C and originally drafted under the name `leading-trim`. Similarly, `text-box-edge` was originally heavily drafted as `text-edge`. If old tooling (like ancient Figma exports) ejects `leading-trim`, recognize that it maps exactly to modern `text-box-trim`.

#### 14.2.8 The Complete ES2025/2026 JS Primitive Expansions

The JavaScript enhancements replacing legacy libraries (`lodash/moment`) include full strict-specification methods.
**The 7 Immutable Set Methods:**
`union()`, `intersection()`, `difference()`, `symmetricDifference()`, `isSubsetOf()`, `isSupersetOf()`, and `isDisjointFrom()`.

**The 10 Iterator Helpers:**
`map()`, `filter()`, `take()`, `drop()`, `flatMap()`, `reduce()`, `toArray()`, `some()`, `every()`, and `find()`.

---

#### 14.2.9 Netflix Polaris & `@layer` Architectures

Enterprise adoption of Cascade Layers is spearheaded by major architectures like **Netflix's Polaris Design System**, which completely abandoned monolithic stylesheets in favor of explicit `@layer` ordering to manage global resets and thematic hierarchies efficiently, demonstrating its real-world scalability.

#### 14.2.10 Future-Proofing: `@when`, `@else`, and Interop 2025

- **The `@when` & `@else` At-Rules**: While the inline `if()` function provides property-level conditionals, the W3C is actively drafting `@when` and `@else` at-rules. These will eventually provide block-level generalized conditional routing across the DOM without chaining `@media` queries.
- **Interop 2025 - Anchor Container Queries**: Container queries are evolving to combine with Anchor positioning, evaluating a container's size relative to a completely detached anchor node!

#### 14.2.11 The Underlying Timeline APIs & Chrome 145

The CSS `scroll()` and `view()` functions map directly to the newly exposed JavaScript **`ScrollTimeline`** and **`ViewTimeline`** objects. Furthermore, the 2026 pipeline (Chrome 145+) introduces **"Scroll-Triggered Animations"**—a declarative CSS alternative to `IntersectionObserver` that allows standard time-based animations to fire exactly once when a specific scroll offset is reached, rather than being scrubbed persistently by the scrollbar.

#### 14.2.12 Nesting Safety Limits & Feature Guards

While native nesting is incredibly powerful, strict organizational rules apply:

1. **Recommended nesting-depth limit:** Keep nesting shallow—often two or three levels—to reduce selector complexity and brittle coupling. This is an architecture convention, not a parser limit.
2. **Nesting Feature Detection:** To support browsers older than mid-2023 that lack native parser support, wrap your nested blocks using: `@supports (selector(&)) { ... }`.

#### 14.2.13 Complete Typographical Cropping Matrix

To finalize `text-box-trim` and `text-box-edge`, these are the precise layout engine keywords:

- `text-box-trim`: `trim-start` (Top bounding box only), `trim-end` (Bottom bounding box only), `trim-both` (Full crop), `none`.
- `text-box-edge`: `cap` (Top of uppercase letter), `alphabetic` (Bottom baseline), `ex` (Top of lowercase 'x'), `text` (The font's native bounding box).
  Note: Firefox does NOT support these as of early 2026, meaning they have not reached "Baseline" status yet.

#### 14.2.14 The 50% Discrete Transition Rule

When transitioning `display: none` to `block`, the visibility flips instantly at the **0%** mark natively. When transitioning from `block` to `none`, it waits and flips at the **100%** mark. However, for most other discrete animations (like animating `justify-content` or `box-sizing`), the internal engine flip typically happens at the **50% mark** of the transition duration.

#### 14.2.15 Advanced Native Highlighting (`::highlight()`)
Custom selection highlighting without modifying the underlying DOM structure.

```javascript
const userRange = new Range();
CSS.highlights.set("search-term", new Highlight(userRange));
```

```css
::highlight(search-term) {
  background-color: yellow;
  color: black;
  text-decoration: underline wavy red;
}
```

#### 14.2.16 Color Fonts & `font-palette`
Customize the layered colors inside modern color-aware font files (like COLRv1).
- `@font-palette-values`: Overrides internal font colors.
- `font-palette: --my-custom-palette;`

---

#### 14.2.17 Cutting-Edge Web Features (2024-2025/2026)
#### 14.2.18 =================================================

This section documents the latest bleeding-edge features in CSS, HTML, and JavaScript, extracted from state-of-the-art web demonstrations. These represent highly experimental or newly finalized APIs.

---

## 15. Browser Support, Baseline, Stability, and Adoption Guidance

### 15.1 Browser Support Matrix & Stability Indicators
#### 15.1.1 Stability Status Legend

| Status | Meaning | Production Ready |
|--------|---------|------------------|
| **Baseline** | Available in Chrome, Firefox, Safari, Edge | ✅ Yes |
| **Experimental** | Chrome-only or subject to spec changes | ⚠️ Use with caution |
| **Coming 2026** | ES2026 or browser implementation in progress | ❌ Not yet |

#### 15.1.2 CSS Features Matrix

| Feature | Chrome | Firefox | Safari | Edge | Status |
|---------|--------|---------|--------|------|--------|
| CSS Nesting | 112+ | 117+ | 17+ | 112+ | Baseline |
| `:has()` | 105+ | 121+ | 17.2+ | 105+ | Baseline |
| `@scope` | 118+ | 126+ | 17.5+ | 118+ | Baseline |
| `@layer` | 99+ | 107+ | 15.4+ | 99+ | Baseline |
| Container Queries | 105+ | 110+ | 16+ | 105+ | Baseline |
| Scroll-Driven Animations | 115+ | 123+ | 17.5+ | 115+ | Baseline |
| View Transitions | 111+ | 126+ | 17.5+ | 111+ | Baseline |
| Anchor Positioning | 125+ | 128+ | 18.2+ | 125+ | Baseline |
| `interpolate-size` | 123+ | 125+ | 17.5+ | 123+ | Baseline |
| `@starting-style` | 117+ | 125+ | 17.5+ | 117+ | Baseline |
| `color-mix()` | 111+ | 113+ | 16+ | 111+ | Baseline |
| `light-dark()` | 119+ | 121+ | 17.4+ | 119+ | Baseline |
| `text-box-trim` | 124+ | 126+ | 18+ | 124+ | Baseline |
| `field-sizing: content` | 123+ | 143+ | 18.4+ | 123+ | Baseline |
| `::details-content` | 131+ | 143+ | 18.4+ | 131+ | Baseline |
| `corner-shape` | 139+ | - | - | 139+ | Experimental |
| `if()` | 137+ | - | - | 137+ | Experimental |
| `reading-flow` | 141+ | 143+ | 18.5+ | 141+ | Baseline |
| `base-select` / `::picker(select)` | 135+ | - | - | 135+ | Experimental → Interop track |
| Invoker Commands (`command`/`commandfor`) | 135+ | 2026 | 2026 | 135+ | Baseline track early 2026 |
| `dialog[closedby]` | 134+ | 2026 | 2026 | 134+ | Expanding → Baseline track |
| `popover` API | 114+ | 125+ | 17+ | 114+ | Baseline (Jan 2025) |
| `popover="hint"` / `interestfor` | 133+ | Expanding | Expanding | 133+ | Expanding 2026 |
| `::scroll-button()` / `::scroll-marker` | 135+ | - | - | 135+ | Experimental |
| `scroll-target-group` / `:target-current` | 135+ | - | - | 135+ | Experimental |
| `grid-template-rows: masonry` (Grid Lanes) | Rolling | Partial | Partial | Rolling | Progressive enhance |
| CSS `random()` | Rolling | - | - | Rolling | CSS Snapshot 2025+ |
| CSS `:toggle()` track | Experimental | - | - | Experimental | Prefer HTML state first |
| Scroll-state container queries | 133+ | Expanding | Expanding | 133+ | Expanding 2026 |
| `sibling-index()` / `sibling-count()` | 138+ | - | - | 138+ | Experimental |
| Typed `attr()` | 133+ | Expanding | Expanding | 133+ | Expanding 2026 |
| `@scope` | 118+ | 128+ | 17.4+ | 118+ | Baseline (Dec 2025 track) |
| Cross-document View Transitions | 126+ | Expanding | 18+ | 126+ | Expanding Baseline |
| `font-size-adjust` | Baseline | Baseline | Baseline | Baseline | Baseline |
| `scrollbar-color` / `scrollbar-gutter` | Baseline | Baseline | Partial | Baseline | Mostly Baseline |

#### 15.1.3 JavaScript Features Matrix

| Feature | Chrome | Firefox | Safari | Edge | Status |
|---------|--------|---------|--------|------|--------|
| Top-Level Await | 89+ | 104+ | 15+ | 89+ | Baseline |
| `Object.hasOwn()` | 93+ | 92+ | 15.4+ | 93+ | Baseline |
| `Array.toSorted()` / `toReversed()` / `toSpliced()` | 110+ | 110+ | 16.4+ | 110+ | Baseline |
| Set Methods (7) | 122+ | 127+ | 17+ | 122+ | Baseline (ES2025) |
| Iterator Helpers | 122+ | 131+ | 18.4+ | 122+ | Baseline (ES2025) |
| `Promise.withResolvers()` | 119+ | 121+ | 17.5+ | 119+ | Baseline |
| `Promise.try()` | 128+ | 134+ | 18.2+ | 128+ | Baseline (ES2025) |
| `RegExp.escape()` | 136+ | 134+ | 18.2+ | 136+ | Baseline (ES2025) |
| `Float16Array` | 135+ | 129+ | 18.2+ | 135+ | Baseline (ES2025) |
| Import Attributes | 123+ | 138+ | 17.2+ | 123+ | Baseline (ES2025) |
| `Array.fromAsync()` | 117+ | 115+ | 18.4+ | 117+ | Baseline / ES2026 |
| `Error.isError()` | 134+ | 138+ | 18.4+ | 134+ | ES2026 |
| `Math.sumPrecise()` | 137+ | - | - | 137+ | ES2026 (expanding) |
| `Map`/`WeakMap` `getOrInsert*` | 138+ | Expanding | Expanding | 138+ | ES2026 (expanding) |
| `Uint8Array` Base64/Hex | 140+ | 133+ | 18.2+ | 140+ | ES2026 (expanding) |
| `Iterator.concat()` | 139+ | - | - | 139+ | ES2026 (expanding) |
| `JSON.rawJSON` / reviver source | 135+ | - | - | 135+ | ES2026 (expanding) |
| `using` / Explicit Resource Management | 134+ | Expanding | Expanding | 134+ | ES2026 / polyfill OK |
| Temporal API | Landing + polyfill | Shipped | Partial | Landing + polyfill | **Stage 4 on 21 May 2026** → ES2027; verify Node/runtime release support |
| Iterator Helpers | 122+ | 131+ | 18.4+ | 122+ | Baseline Newly Available ~Mar 2025 |
| `Object.groupBy` / `Map.groupBy` | Baseline | Baseline | Baseline | Baseline | ES2024/25 era — safe |
| `Promise.withResolvers()` | Baseline | Baseline | Baseline | Baseline | Safe evergreen |
| Decorators | Finalizing | Finalizing | Finalizing | Finalizing | Track with ES2026 — verify before ship |
| Pattern Matching | Proposal | - | - | - | Not Baseline — proposal only |
| Record & Tuple | Withdrawn / redesign | - | - | - | Do **not** ship as stable |

> **Note (July 2026):** Prefer features listed in the user-facing ES2025/ES2026 editions and Interop tracks. Speculative syntax (pattern matching, records/tuples) may appear in older drafts of this guide — treat as **non-production** until TC39 + Baseline confirm.

#### 15.1.4 Web APIs Matrix

| API | Chrome | Firefox | Safari | Edge | Status |
|-----|--------|---------|--------|------|--------|
| WebGPU | Platform-dependent | Platform-dependent | Platform-dependent | Platform-dependent | Limited/expanding; feature-detect and test the actual device |
| File System Access | 86+ | - | - | 86+ | Chromium-oriented |
| OPFS | 102+ | 111+ | 15.2+ | 102+ | Baseline |
| Popover API | 114+ | 125+ | 17+ | 114+ | Baseline (2025) |
| `<dialog>` | 37+ | 98+ | 15.4+ | 79+ | Baseline |
| Invoker Commands | 135+ | 2026 | 2026 | 135+ | Baseline track early 2026 |
| Declarative Shadow DOM | 90+ | 123+ | 16.4+ | 90+ | Baseline |
| Speculation Rules | 109+ | Expanding | Expanding | 109+ | Chromium-strong; PE elsewhere |
| Document Picture-in-Picture | 116+ | - | - | 116+ | Chromium-oriented |
| Close Watcher | 126+ | Expanding | Expanding | 126+ | Expanding 2025–26 |
| Compression Streams | 80+ | 113+ | 16.4+ | 80+ | Baseline Widely Available ~2025 |
| Shadow DOM / Custom Elements | 67+ | 63+ | 10.1+ | 79+ | Baseline |
| Navigation API | 102+ | - | - | 102+ | Chromium-oriented |
| View Transitions (same-doc) | 111+ | 144+ | 18+ | 111+ | Expanding Baseline |
| CSS Anchor Positioning | 125+ | 128+ | 18.2+ | 125+ | ✅ Baseline; Interop 2025 expansion |
| `Element.moveBefore()` | Shipping | Expanding | Expanding | Shipping | Baseline 2025–26 track |
| `scrollend` event | Baseline | Baseline | Baseline | Baseline | Prefer over scroll debounce |
| `navigator.userActivation` | Baseline | Baseline | Baseline | Baseline | Gesture-gated APIs |
| Trusted Types | Chromium-strong | Partial | Partial | Chromium-strong | Enforce via CSP |
| WebTransport | Expanding | Expanding | Expanding | Expanding | QUIC/HTTP3 alternative class |
| `hidden="until-found"` | Baseline | Baseline | Baseline | Baseline | Interop 2025 |
| `contrast-color()` | Newly ~2026 | Newly ~2026 | Newly ~2026 | Newly ~2026 | Baseline Newly available Apr 2026 |
| `field-sizing: content` | Newly ~Jun 2026 | Newly | Newly | Newly | Baseline Newly available |
| Container style queries | Baseline | 151+ (May 2026) | Baseline | Baseline | Cross-browser complete mid-2026 |

#### 15.1.5 Feature Detection Patterns

```javascript
// CSS Feature Detection
if (CSS.supports('selector(:has(*))')) { /* Use :has() */ }
if (CSS.supports('animation-timeline: scroll()')) { /* Use scroll-driven */ }

// JavaScript Feature Detection
if ('showOpenFilePicker' in window) { /* Use File System API */ }
if ('gpu' in navigator) { /* Use WebGPU */ }
if ('Temporal' in window) { /* Use Temporal API */ }

// Graceful Fallbacks
const sortArray = Array.prototype.toSorted 
  ? (arr, fn) => arr.toSorted(fn)
  : (arr, fn) => [...arr].sort(fn);
```

### 15.2 Baseline Digests Alignment (July 2026 Catalogue)
Features from web.dev Baseline digests, Chrome CSS Wrapped 2025, TC39/ES2026, and MDN that were thin or missing above. **Status legend:** ✅ Baseline / Widely · 🆕 Newly available 2025–26 · ⚠️ Experimental (progressive enhance).

#### 15.2.1 Layout, Anchors & Display

##### Container style queries (✅ Newly available mid-2026)

```css
.card {
  container-type: inline-size;
  --density: comfortable;
}
@container style(--density: compact) {
  .row { gap: 0.5rem; font-size: 0.875rem; }
}
/* Range comparisons (🆕 Chrome 142+ track) */
@container style(--progress > 45%) {
  .meter { accent-color: var(--success); }
}
```

##### Anchored container queries (🆕 Interop 2025)

Detect **which** `position-try` fallback actually won so children (e.g. tooltip arrows) restyle:

```css
.tooltip {
  anchor-name: --tip;
  position: absolute;
  position-anchor: --btn;
  position-area: top;
  position-try-fallbacks: flip-block, flip-inline;
  container-type: anchored;
}
@container anchored(fallback: flip-block) {
  .tooltip-arrow { rotate: 180deg; }
}
```

##### Multi-keyword `display` (✅ Widely available ~Jan 2026)

```css
.chip { display: inline flex; } /* outer: inline; inner: flex — not legacy inline-flex only */
.panel { display: block grid; }
```

##### `width` / `height: stretch` (🆕 2025)

Fills the **margin box** of the containing block (margins preserved, unlike naïve `100%`):

```css
.sidebar-fill { height: stretch; }
.full-row { width: stretch; }
```

#### 15.2.2 Color & Scrollbars

```css
/* ✅ contrast-color() — Baseline Newly available ~April 2026 */
.badge {
  --bg: oklch(65% 0.18 250);
  background: var(--bg);
  color: contrast-color(var(--bg)); /* browser picks black/white (or high-contrast pair) */
}

/* Scrollbars — width Baseline Dec 2024; color Newly available Dec 2025 (Safari last) */
.scroll-pane {
  scrollbar-width: thin;
  scrollbar-color: var(--accent) var(--surface-2);
}
```

#### 15.2.3 Typography Units & Text Controls

| Feature | Role | Status |
|---------|------|--------|
| `lh` | 1× current element’s used line-height | ✅ Widely (~May 2026) |
| `rlh` | 1× **root** line-height — site-wide vertical rhythm | ✅ Widely (~May 2026) |
| `rcap` / `rch` / `rex` / `ric` | Root-relative cap / ch / ex / ic | 🆕 Baseline 2026 |
| `text-box` / `text-box-trim` / `text-box-edge` | Visual vertical centering of glyphs | ✅ Baseline 2025 |
| `text-decoration-skip-ink: all` | Underlines skip descenders cleanly | 🆕 Baseline 2026 |
| `text-indent: each-line` / `hanging` | Per-line / hanging indents | 🆕 Baseline 2026 |
| `baseline-shift` | Vertical shift relative to baseline | 🆕 Baseline 2026 grab-bag |

```css
.icon-badge {
  width: 1lh;
  height: 1lh;
  border-radius: 999px;
}
.section-gap { margin-block: 1rlh; }
.lead {
  text-indent: hanging 2ch;
  text-decoration-skip-ink: all;
}
h1 {
  text-box: trim-both cap alphabetic;
}
```

#### 15.2.4 Selectors, Open State & View Transition Pseudos

```css
/* 🆕 :open — one selector for open dialog / details / popover / select picker */
:open { outline: 2px solid var(--accent); }

/* View transition in-flight */
:root:active-view-transition { cursor: wait; }
:root:active-view-transition-type(slide) {
  /* styles only while that VT type runs */
}

/* Nested view-transition groups (🆕 2025) — preserve clip/3D */
.card {
  view-transition-name: card;
  view-transition-group: nearest;
}
::view-transition-group-children(card) {
  overflow: clip;
}
```

```javascript
// Active View Transition types (🆕)
document.startViewTransition({
  update: () => swapDOM(),
  types: ['slide', 'fade'],
});
// CSS: :active-view-transition-type(slide) { … }
```

#### 15.2.5 Animation Composition & Math Language

```css
/* ✅ animation-composition — Widely available ~Jan 2026 */
.pulse {
  animation: bob 1s infinite alternate, drift 2s infinite;
  animation-composition: add; /* replace | add | accumulate */
}

/* ✅ Math constants in calc() — Widely Dec 2025 */
.orbit {
  --a: calc(pi * 1rad);
  rotate: calc(sin(var(--t) * pi) * 12deg);
  opacity: calc(e / 3); /* careful: design-token, not layout-critical */
}
```

#### 15.2.6 Forms, ToggleEvent.source & Custom Select Status

```javascript
// 🆕 ToggleEvent.source — which control flipped a popover/dialog/details
popover.addEventListener('toggle', (e) => {
  console.log(e.newState, e.source); // Element that triggered toggle
});
```

| Control | Status (Jul 2026 catalogue) |
|---------|------------------------------|
| Popover API | ✅ Baseline 2025 |
| `closedby` on `<dialog>` | ✅ Baseline (Chrome 134+) |
| `field-sizing: content` | ✅ Newly available ~June 16 2026 |
| Customizable `<select>` / `<selectedcontent>` | ⚠️ Experimental Chrome 139+ |
| Invoker Commands | ⚠️ Experimental Chrome 135+ (`invokers-polyfill`) |
| `interestfor` / `popover="hint"` | 🆕 2025 |

#### 15.2.7 HTML: `hidden="until-found"`, Details & Loading Hints

```html
<!-- ✅ Baseline Newly available 2025 (Interop) — find-in-page / fragment reveals content -->
<section hidden="until-found" id="advanced-filters">
  <h2>Advanced filters</h2>
  <p>Matched text here becomes visible when found.</p>
</section>

<details>
  <summary>FAQ answer</summary>
  <!-- ::details-content styles the content box; find-in-page can auto-open closed details -->
  <p>Browser may expand this when find-in-page hits text inside.</p>
</details>

<img src="hero.avif" alt="…" fetchpriority="high" width="1200" height="630">
<link rel="modulepreload" href="/js/app.js">
```

```css
details::details-content {
  transition: content-visibility 0.25s allow-discrete, opacity 0.25s;
}
summary::marker { color: var(--accent); }
```

#### 15.2.8 CSS-as-Language Gaps

```css
/* Range style queries + if() (🆕) */
width: if(style(--cols > 3): 25%; else: 50%);

/* @function already in §5.6 — default args + result: */
@function --fluid(--min <length>: 1rem, --max <length>: 3rem) {
  result: clamp(var(--min), 4vw, var(--max));
}

/* Typed attr() — any property */
.bar {
  width: attr(data-pct type(<percentage>), 0%);
  background: attr(data-color type(<color>), canvastext);
}
```

#### 15.2.9 JavaScript — ES2025 Recap + ES2026 Snapshot (Jul 2026)

**Safe to ship evergreen / Node 22+ (no polyfill):** Iterator helpers, Set algebra, `Array.fromAsync`, `Object.groupBy` / `Map.groupBy`, `Promise.withResolvers`, `Promise.try`, `RegExp.escape`, Uint8Array Base64/Hex (+ `setFromBase64` / `setFromHex` where available), import attributes.

**ES2026 shipping through 2026:**

| Feature | Notes |
|---------|--------|
| `using` / `await using` | Chrome/Node 22+; transpile for older |
| `Error.isError()` | Chrome 134+, Node 24+; Safari lag |
| `Map.getOrInsert*` | Chrome 144+ track, Node 24+ |
| `Math.sumPrecise()` | Chrome 137+, Node 24+ |
| `Iterator.concat()` | V8 14.6 / Chromium ~146 mid-2026 |
| `Float16Array` | Check the current ECMAScript/runtime compatibility data; do not infer support from WebGPU availability |
| **Decorators** | Finalizing with ES2026 — verify before production |
| **Temporal** | **TC39 Stage 4 on 21 May 2026** → slated **ES2027** edition. Firefox shipped; Chrome/V8 landing; Safari partial. **verify the exact Node.js/V8 release used in deployment**. Polyfills: `@js-temporal/polyfill`, `temporal-polyfill` |
| Duplicate named capture groups in RegExp | ES2025 — reuse names across alternation branches |
| `import defer` | Did **not** make ES2026; implementations exist — track separately |

```javascript
// Duplicate named groups (ES2025)
const re = /(?<id>\d+)-a|(?<id>[a-z]+)-b/u;

// Uint8Array extras
const u8 = Uint8Array.fromBase64(b64);
u8.setFromHex(hexString);
```

#### 15.2.10 Web Platform APIs (Baseline 2025–2026)

##### DOM move without state loss

```javascript
// Element.moveBefore() — keeps video playhead, iframe, focus, CSS animations
parent.moveBefore(node, referenceChild);
```

##### Scroll helpers

```javascript
el.scrollIntoView({ block: 'nearest', inline: 'nearest', container: 'nearest' });

scroller.addEventListener('scrollend', () => {
  // fires once when scroll settles — no setTimeout debounce
});
```

##### Caret, activation, navigation, workers

```javascript
const pos = document.caretPositionFromPoint(x, y);
// pos.offsetNode, pos.offset

if (navigator.userActivation?.isActive) {
  await navigator.clipboard.writeText(text);
}

navigation.addEventListener('navigate', (e) => {
  if (shouldIntercept(e)) {
    e.intercept({ async handler() { await render(e.destination.url); } });
  }
});

// Module workers + SharedWorker modules
const w = new Worker('/worker.js', { type: 'module' });
const sw = new SharedWorker('/shared.js', { type: 'module' });
```

##### Streams, transport, security, encoding

| API | Role |
|-----|------|
| Readable byte streams (`ReadableByteStreamController`) | Zero-copy-friendly binary reading |
| **WebTransport** | HTTP/3 / QUIC multiplexed transport (WebSocket alternative class) |
| **Event Timing API** | Powers **INP**; inspect interaction latency |
| **Reporting API** / `ReportingObserver` / CSP violation reports | Structured CSP, deprecation, intervention reports |
| **Trusted Types** | Require sanitizer types for `innerHTML` and other XSS sinks |
| **`zstd` content-encoding** | `Accept-Encoding: zstd` for faster compressed transfers |
| WebAssembly branch hinting | Perf hints for Wasm engines |

```javascript
// Trusted Types (when enforced by CSP)
if (window.trustedTypes) {
  const policy = trustedTypes.createPolicy('app', {
    createHTML: (s) => sanitize(s),
  });
  el.innerHTML = policy.createHTML(untrusted);
}

// ReportingObserver
const obs = new ReportingObserver((reports) => {
  for (const r of reports) console.warn(r.type, r.body);
}, { types: ['csp-violation', 'deprecation'], buffered: true });
obs.observe();
```

#### 15.2.11 Experimental Watch-list (do not require without fallback)

| Feature | Jul 2026 note |
|---------|----------------|
| `corner-shape`, `superellipse()` | Chrome 139+ |
| CSS `if()` | Chrome 137+ |
| Customizable `<select>` (`base-select`) | Chrome 139+ |
| Invoker Commands | ✅ Baseline newly available 2025-12-12 (C135·F144·S26.2) — PE older UAs |
| Temporal | Limited (C144·F139·S— in this snapshot); feature-detect and polyfill where required |
| Decorators | Proposal status and syntax must be checked against the current TC39 process and toolchain |
| `import defer` | Not in ES2026 proper |

#### 15.2.12 Sources (this catalogue pass)

- web.dev Baseline digests (Dec 2025, Jan/Apr/May 2026), web.dev/baseline/2025–2026  
- Chrome DevRel CSS Wrapped 2025  
- MDN (Temporal, individual features)  
- Node.js and V8 release notes for the exact deployed runtime  
- TC39 ES2026 trackers

Always re-check MDN / web.dev/baseline before hard-requiring a feature in production.

---

## 16. Authoritative Web Platform Catalogue — 2025 to 10 July 2026

> **Authoritative support catalogue** integrated from Web Features **3.32.0** + BCD cross-check (report date **10 July 2026**). Recipes and patterns are in earlier sections of this file and in `03-standards-compliance.md`. Use this section for version / Baseline truth.

A research catalogue of browser-native HTML, CSS, JavaScript language features, DOM APIs, and related Web APIs that either **first gained a complete stable implementation in a core browser** or **became interoperable across the core browsers** from 1 January 2025 through 10 July 2026. Frameworks, build tools, browser UI features, extensions APIs, DevTools-only features, and origin trials are excluded from the main count.

### 16.1 Executive summary
The normalized catalogue contains **147 distinct features**: **91** first entered stable support in the core browser set during this window, **67** became Baseline Newly available, and **11** did both. A further **19 very recent stable-release additions** are listed separately because the current Web Features dataset has not yet normalized them as standalone entries.

| Area | Tracked entries |
|---|---:|
| CSS and styling | 65 |
| DOM and Web APIs | 54 |
| HTML and declarative UI | 12 |
| JavaScript language and built-ins | 16 |

The biggest direction of travel is unmistakable: UI patterns that previously needed JavaScript libraries—anchored overlays, customizable selects, carousels, auto-growing form controls, view transitions, scroll-linked/triggered animation, focus management, and masonry-like layout—are moving into HTML and CSS. JavaScript itself gained safer string/regex handling, modern date/time support, precise summation, iterator composition, and binary encoding helpers.

**Stable-browser cutoff used:** Chrome 150 (30 June 2026), Firefox 152 (16 June 2026), and Safari 26.5 (11 May 2026). Firefox 153 and Safari 27 were beta-only on the report date and appear only in the preview appendix.

### 16.2 How to read this report
- **First complete core implementation** means the first stable Chrome, Firefox, or Safari release reported by the Web Features dataset for the complete tracked feature. Some older partial implementations may exist.
- **Baseline newly available** means the feature is supported across the Baseline core browser set. It does **not** mean every older browser in circulation supports it. Baseline calls a feature “widely available” only after 30 months.
- **Limited availability** means at least one core engine still lacks the complete feature. Use feature detection and progressive enhancement.
- Support cells use **C** = Chrome, **F** = Firefox, **S** = Safari. Version numbers are the first versions counted for the tracked feature by the dataset. “—” means no qualifying stable implementation is recorded.
- “Introduced” is implementation-based, not the date a proposal was first drafted. Specifications are living documents and can predate implementation by years.

### 16.3 Practical adoption tiers
1. **Use with ordinary compatibility policy:** entries marked Baseline Newly available, if your supported browser floor includes the listed versions.
2. **Progressively enhance:** limited CSS/HTML features that fail harmlessly when unsupported, such as corner shaping, CSS custom functions, scroll markers, or text fitting. Guard with `@supports` when possible.
3. **Feature-detect and provide a fallback:** JavaScript and Web APIs such as Temporal, Sanitizer, Navigation, CloseWatcher, WebGPU, Digital Credentials, and built-in AI APIs.
4. **Do not ship as a universal dependency:** beta-only items in the preview appendix.

### 16.4 High-impact features and minimal examples
#### 16.4.1 CSS and HTML UI

##### Typed CSS `attr()`

```css
.progress { width: attr(data-progress type(<percentage>), 0%); }
```

##### Scroll-state container queries

```css
.sticky { container-type: scroll-state; position: sticky; top: 0; }
@container scroll-state(stuck: top) { .sticky { box-shadow: 0 2px 8px #0003; } }
```

##### Declarative dialog control

```html
<button commandfor="profile" command="show-modal">Open profile</button>
<dialog id="profile" closedby="any">…</dialog>
```

##### Customizable select

```css
select, ::picker(select) { appearance: base-select; }
```

##### CSS conditionals and custom functions

```css
@function --space(--n) { result: calc(var(--n) * 0.25rem); }
.card { padding: if(style(--dense: true): --space(2); else: --space(6)); }
```

##### Auto-growing form controls

```css
textarea { field-sizing: content; min-block-size: 3lh; max-block-size: 12lh; }
```

##### Declarative keyboard navigation

```html
<div focusgroup="toolbar wrap" aria-label="Formatting">
  <button>Bold</button><button>Italic</button><button>Underline</button>
</div>
```

#### 16.4.2 JavaScript and DOM

##### Safe dynamic regular expressions

```js
const literal = RegExp.escape(userInput);
const matcher = new RegExp(`^${literal}$`, 'u');
```

##### Temporal

```js
const meeting = Temporal.ZonedDateTime.from('2026-07-10T09:30+05:30[Asia/Kolkata]');
console.log(meeting.add({ hours: 2 }).toString());
```

##### Uint8Array base64 helpers

```js
const bytes = Uint8Array.fromBase64(encoded);
const roundTrip = bytes.toBase64();
```

##### State-preserving DOM moves

```js
container.moveBefore(videoCard, container.firstElementChild);
// Playing media, focus, animations, open popovers, etc. remain intact.
```

##### Navigation API

```js
navigation.addEventListener('navigate', event => {
  if (event.canIntercept) event.intercept({ handler: () => render(new URL(event.destination.url)) });
});
```

##### HTML Sanitizer API

```js
const safe = new Sanitizer({ elements: ['p', 'strong', 'a'] });
container.setHTML(untrustedHTML, { sanitizer: safe });
```

### 16.5 Complete normalized catalogue (147 features)
#### 16.5.1 CSS and styling (65)

| Feature | 2025–today milestone | Core support | Status today | What it adds |
|---|---|---|---|---|
| [baseline-shift](https://drafts.csswg.org/css-inline-3/#baseline-shift-property) | Baseline newly available: 2026-03-24 | C 1 · F 149 · S 4 | Baseline newly available (2026-03-24) | The baseline-shift CSS property sets the position of an element relative to its dominant baseline. |
| [document.caretPositionFromPoint()](https://drafts.csswg.org/cssom-view-1/#dom-document-caretpositionfrompoint) | Baseline newly available: 2025-12-12 | C 128 · F 20 · S 26.2 | Baseline newly available (2025-12-12) | The document.caretPositionFromPoint() method finds an insertion point, represented by a DOM node and an offset within that node, for given coordinates in the viewport. |
| [crisp-edges](https://drafts.csswg.org/css-images-3/#the-image-rendering) | Baseline newly available: 2026-05-07 | C 148 · F 65 · S 7 | Baseline newly available (2026-05-07) | The image-rendering: crisp-edges CSS declaration scales images to preserve lines without blurring. |
| [scrollbar-color](https://drafts.csswg.org/css-scrollbars-1/#scrollbar-color) | Baseline newly available: 2025-12-12 | C 121 · F 64 · S 26.2 | Baseline newly available (2025-12-12) | The scrollbar-color CSS property sets the color of the scrollbar track and thumb. |
| [text-decoration-skip-ink: all](https://drafts.csswg.org/css-text-decor-4/#valdef-text-decoration-skip-ink-all) | Baseline newly available: 2026-05-07 | C 148 · F 75 · S 15.4 | Baseline newly available (2026-05-07) | The text-decoration-skip-ink: all CSS declaration forces interruptions in underlines and overlines where the line would cross a glyph. This contrasts with auto, which does not skip for CJK glyphs. |
| [text-indent: each-line](https://drafts.csswg.org/css-text-4/#text-indent-property) | Baseline newly available: 2026-03-13 | C 146 · F 121 · S 15 | Baseline newly available (2026-03-13) | The text-indent: each-line CSS declaration indents text after forced breaks as well as to the first line of a block. |
| [text-indent: hanging](https://drafts.csswg.org/css-text-4/#text-indent-property) | Baseline newly available: 2026-03-13 | C 146 · F 121 · S 15 | Baseline newly available (2026-03-13) | The text-indent: hanging CSS declaration indents all lines except the first. |
| [print-color-adjust](https://drafts.csswg.org/css-color-adjust-1/#propdef-print-color-adjust) | Baseline newly available: 2025-05-01 | C 136 · F 97 · S 15.4 | Baseline newly available (2025-05-01) | The print-color-adjust CSS property sets whether styles of printed pages should be adjusted to use less ink, in cases such as light text on a dark background. |
| [abs() and sign()](https://drafts.csswg.org/css-values-4/#sign-funcs) | Baseline newly available: 2025-06-26 | C 138 · F 118 · S 15.4 | Baseline newly available (2025-06-26) | The abs() and sign() CSS functions compute the absolute value or the sign of the input. |
| [Custom highlights](https://drafts.csswg.org/css-highlight-api-1/) | Baseline newly available: 2026-03-24 | C 105 · F 149 · S 17.2 | Baseline newly available (2026-03-24) | Custom highlights style arbitrary text ranges, without adding extra elements to the DOM. |
| [content-visibility](https://drafts.csswg.org/css-contain-2/#content-visibility) | Baseline newly available: 2025-09-15 | C 108 · F 130 · S 26 | Baseline newly available (2025-09-15) | The content-visibility CSS property delays rendering an element, including layout and painting, until it is needed. |
| [Math font family](https://drafts.csswg.org/css-fonts-4/#math-def) | Baseline newly available: 2026-03-24 | C 109 · F 149 · S 26.2 | Baseline newly available (2026-03-24) | The font-family: math CSS declaration uses the browser default font face for displaying mathematical expressions. |
| [scrollend](https://drafts.csswg.org/cssom-view-1/#eventdef-document-scrollend) | Baseline newly available: 2025-12-12 | C 114 · F 109 · S 26.2 | Baseline newly available (2025-12-12) | The scrollend event fires when an element or document has finished scrolling. |
| [Container style queries](https://drafts.csswg.org/css-conditional-5/#style-container) | Baseline newly available: 2026-05-19 | C 111 · F 151 · S 18 | Baseline newly available (2026-05-19) | Container style queries with the @container at-rule apply styles to an element based on the values of custom properties of its container. |
| [rch unit](https://drafts.csswg.org/css-values-4/#font-relative-lengths) | Baseline newly available: 2026-01-13 | C 111 · F 147 · S 17.2 | Baseline newly available (2026-01-13) | The rch CSS length unit is a font-relative length equal to the value of the ch unit on the root element. ch length is based on the width of the zero (0) character. |
| [rex unit](https://drafts.csswg.org/css-values-4/#font-relative-lengths) | Baseline newly available: 2026-01-13 | C 111 · F 147 · S 17.2 | Baseline newly available (2026-01-13) | The rex CSS length unit is a font-relative length that is equal to the x-height of the root element. |
| [ric unit](https://drafts.csswg.org/css-values-4/#font-relative-lengths) | Baseline newly available: 2026-01-13 | C 111 · F 147 · S 17.2 | Baseline newly available (2026-01-13) | The ric CSS length unit, or root international character, is a font-relative length equal to the width of CJK character relative to the root element. |
| [View transitions](https://drafts.csswg.org/css-view-transitions-1/) | Baseline newly available: 2025-10-14 | C 111 · F 144 · S 18 | Baseline newly available (2025-10-14) | View transitions allow you to create animated visual transitions between different states of a document. |
| [rcap unit](https://drafts.csswg.org/css-values-4/#font-relative-lengths) | Baseline newly available: 2026-01-13 | C 118 · F 147 · S 17.2 | Baseline newly available (2026-01-13) | The rcap CSS length unit is a font-relative length equal to the value of the cap unit on the root element. Cap-height is approximately equal to the height of a capital Latin letter. |
| [Spelling and grammar text decorations](https://drafts.csswg.org/css-text-decor-4/#valdef-text-decoration-line-spelling-error) | Baseline newly available: 2025-12-12 | C 121 · F 137 · S 26.2 | Baseline newly available (2025-12-12) | The text-decoration-line: spelling-error and text-decoration-line: grammar-error CSS declarations apply the browser's marking for spelling and grammatical mistakes. This is typically a wavy underline in red or green. |
| [field-sizing](https://drafts.csswg.org/css-forms-1/#field-sizing) | Baseline newly available: 2026-06-16 | C 123 · F 152 · S 26.2 | Baseline newly available (2026-06-16) | The field-sizing CSS property allows form controls such as <textarea> to be sized based on their content. |
| [Active view transition](https://drafts.csswg.org/css-view-transitions-2/#the-active-view-transition-pseudo) | Baseline newly available: 2026-01-13 | C 125 · F 147 · S 18.2 | Baseline newly available (2026-01-13) | The :active-view-transition CSS pseudo-class matches the root element when a view transition is active. The :active-view-transition-type() CSS pseudo-class matches only when the active view transition was started with the specified type. |
| [view-transition-class](https://drafts.csswg.org/css-view-transitions-2/#propdef-view-transition-class) | Baseline newly available: 2025-10-14 | C 125 · F 144 · S 18.2 | Baseline newly available (2025-10-14) | The view-transition-class CSS property sets a name that can be used to apply styles to multiple named view transition pseudo-elements. |
| [::details-content](https://drafts.csswg.org/css-pseudo-4/#details-content-pseudo) | Baseline newly available: 2025-09-16 | C 131 · F 143 · S 18.4 | Baseline newly available (2025-09-16) | The ::details-content pseudo-element selects the expandable content of a <details> element, excluding the <summary>. |
| [:open](https://drafts.csswg.org/selectors-4/#open-state) | First complete core implementation: 2025-02-04 (Chrome 133); Baseline newly available: 2026-05-11 | C 133 · F 136 · S 26.5 | Baseline newly available (2026-05-11) | The :open CSS pseudo-class matches elements that have open states, like <details>, <dialog>, or <select>, based on their state. |
| [Container scroll-state queries](https://drafts.csswg.org/css-conditional-5/#scroll-state-container) | First complete core implementation: 2025-02-04 (Chrome 133) | C 133 · F — · S — | Limited availability | Container scroll-state queries with the @container scroll-state(...) at-rule apply styles to an element based on the sticky positioning, snapped, and scrollable state of the container. |
| [scroll-initial-target](https://drafts.csswg.org/css-scroll-snap-2/#properties-on-the-scroll-container) | First complete core implementation: 2025-02-04 (Chrome 133) | C 133 · F — · S — | Limited availability | The scroll-initial-target: nearest CSS declaration sets the initial scroll position of its scroll container to the top of the element, much like scrolling to a URL fragment. |
| [:has-slotted](https://drafts.csswg.org/css-shadow-1/#the-has-slotted-pseudo) | First complete core implementation: 2025-03-04 (Firefox 136) | C — · F 136 · S — | Limited availability | The :has-slotted CSS pseudo-class matches <slot> elements where the fallback content is not shown. The pseudo-class matches any slotted content, including white space, text nodes, or elements. |
| [font-width](https://drafts.csswg.org/css-fonts-4/#font-width-prop) | First complete core implementation: 2025-03-31 (Safari 18.4) | C — · F — · S 18.4 | Limited availability | The font-width CSS property selects a font face from a font family based on width, either by a keyword such as condensed or a percentage. |
| [shape()](https://drafts.csswg.org/css-shapes-1/#shape-function) | First complete core implementation: 2025-03-31 (Safari 18.4); Baseline newly available: 2026-02-24 | C 135 · F 148 · S 18.4 | Baseline newly available (2026-02-24) | The shape() CSS function creates shapes with a series of commands like line, move, and curve. It can be used with clip-path and shape-outside. |
| [::column](https://drafts.csswg.org/css-multicol-2/#column-pseudo) | First complete core implementation: 2025-04-01 (Chrome 135) | C 135 · F — · S — | Limited availability | The ::column CSS pseudo-element represents the individual columns of a multi-column layout container. Columns can only be styled with scroll snap CSS properties and can also have a ::scroll-marker pseudo-element, which scrolls to the column when activated. |
| [interactivity](https://drafts.csswg.org/css-ui-4/#inertness) | First complete core implementation: 2025-04-01 (Chrome 135) | C 135 · F — · S — | Limited availability | The interactivity: inert CSS declaration makes an element and its descendants inert, like when using the inert HTML attribute. Inert elements can't be focused or clicked, their text can't be selected or found using the browser's find-in-page feature. |
| [dynamic-range-limit](https://drafts.csswg.org/css-color-hdr-1/#controlling-dynamic-range) | First complete core implementation: 2025-04-29 (Chrome 136) | C 136 · F — · S — | Limited availability | The dynamic-range-limit CSS property controls the peak luminance of high dynamic range content. You can use this to coordinate the apparent brightness of HDR and SDR content. |
| [if()](https://drafts.csswg.org/css-values-5/#if-notation) | First complete core implementation: 2025-05-27 (Chrome 137) | C 137 · F — · S — | Limited availability | The if() CSS function is an inline conditional value that returns a value based on a set of conditions. |
| [reading-flow](https://drafts.csswg.org/css-display-4/#reading-flow) | First complete core implementation: 2025-05-27 (Chrome 137) | C 137 · F — · S — | Limited availability | The reading-flow CSS property sets the order in which flex or grid elements are rendered to speech or reached via focus navigation. The reading-order property overrides this order. |
| [progress()](https://drafts.csswg.org/css-values-5/#progress) | First complete core implementation: 2025-06-24 (Chrome 138) | C 138 · F — · S 26 | Limited availability | The progress() CSS function returns a ratio for the relative position of one value between two other values, clamped between 0 and 1. You can use it to interpolate a value for other calculations. |
| [sibling-count() and sibling-index()](https://drafts.csswg.org/css-values-5/#tree-counting) | First complete core implementation: 2025-06-24 (Chrome 138) | C 138 · F — · S 26.2 | Limited availability | The sibling-count() and sibling-index() CSS functions return integers that are useful to style elements based on their positions among siblings or on the number of siblings, for example as part of a calc() expression. |
| [stretch](https://drafts.csswg.org/css-sizing-4/#stretch-fit-sizing) | First complete core implementation: 2025-06-24 (Chrome 138) | C 138 · F — · S — | Limited availability | The stretch CSS keyword expands a box as needed to fit its contents until the maximum size is reached, without preserving the content's preferred aspect ratio. |
| [Viewport segments](https://drafts.csswg.org/css-env-1/#viewport-segments) | First complete core implementation: 2025-06-24 (Chrome 138) | C 138 · F — · S — | Limited availability | The viewport segment CSS environment variables and media features, and the viewport.segments API, allow you to adapt your layout to devices where the display is split, such as on foldable devices. |
| [@function](https://drafts.csswg.org/css-mixins-1/#function-rule) | First complete core implementation: 2025-08-05 (Chrome 139) | C 139 · F — · S — | Limited availability | The @function CSS at-rule defines a custom function that takes CSS values or custom properties as arguments, and returns a CSS value. It can be based on conditional logic such as by using the @media at-rule. |
| [corner-shape](https://drafts.csswg.org/css-borders-4/#corner-shaping) | First complete core implementation: 2025-08-05 (Chrome 139) | C 139 · F — · S — | Limited availability | The corner-shape CSS property sets the shape of an element's corners when using border-radius, allowing for shapes other than rounded corners. For example, corner-shape: squircle is a shape in between a square and rounded corner. |
| [Custom highlights from point](https://drafts.csswg.org/css-highlight-api-1/#dom-highlightregistry-highlightsfrompoint) | First complete core implementation: 2025-09-02 (Chrome 140) | C 140 · F 150 · S — | Limited availability | The CSS.highlights.highlightsFromPoint() method returns an array of Highlight objects at a specified point. |
| [scroll-target-group](https://drafts.csswg.org/css-overflow-5/#scroll-target-group) | First complete core implementation: 2025-09-02 (Chrome 140) | C 140 · F — · S — | Limited availability | The scroll-target-group CSS property sets the container where anchor links act as scroll markers. Using selectors such as :target-current, you can style elements when a target has scrolled into view. It's an alternative to the ::scroll-marker-group pseudo-element, which generates scroll markers. |
| [scrollIntoView() container](https://drafts.csswg.org/cssom-view-1/#dom-scrollintoviewoptions-container) | First complete core implementation: 2025-09-02 (Chrome 140) | C 140 · F — · S — | Limited availability | The container option of the scrollIntoView() method sets which ancestor scroll container to scroll. The "nearest" value scrolls only the nearest ancestor, instead of the default "all". |
| [ToggleEvent source](https://html.spec.whatwg.org/multipage/interaction.html#dom-toggleevent-source) | First complete core implementation: 2025-09-02 (Chrome 140); Baseline newly available: 2026-05-11 | C 140 · F 145 · S 26.5 | Baseline newly available (2026-05-11) | The source property of a ToggleEvent object is the element which triggered the toggle event to fire for a popover, <dialog>, or <details> element, if applicable. |
| [contrast-color()](https://drafts.csswg.org/css-color-6/#funcdef-contrast-color) | First complete core implementation: 2025-09-15 (Safari 26); Baseline newly available: 2026-04-10 | C 147 · F 146 · S 26 | Baseline newly available (2026-04-10) | The `contrast-color()` function chooses black or white—whichever has greater contrast with the input color. Mid-tone colors can still produce insufficiently readable small text, so verify the resulting pair against the required contrast criterion. |
| [Scoped custom element registries](https://html.spec.whatwg.org/multipage/custom-elements.html#custom-elements-api) | First complete core implementation: 2025-09-15 (Safari 26) | C 146 · F — · S 26 | Limited availability | The CustomElementRegistry() constructor creates a new custom element registry that's separate from the global window.customElements registry. Creating more than one registry is useful for multiple custom elements that have the same tag name to coexist. |
| [Range syntax for style queries](https://drafts.csswg.org/css-conditional-5/#typedef-style-range) | First complete core implementation: 2025-10-28 (Chrome 142) | C 142 · F — · S — | Limited availability | The @container style() CSS at-rule and if(style()) CSS function queries accept a range syntax, such as >, <, >=, <=, to query for inexact values. |
| [Scroll marker target pseudo-classes](https://drafts.csswg.org/css-overflow-5/#active-before-after-scroll-markers) | First complete core implementation: 2025-10-28 (Chrome 142) | C 142 · F — · S — | Limited availability | The :target-current CSS pseudo-class selects the active scroll marker (as in ::scroll-marker), while the :target-after and :target-before pseudo-classes select the inactive markers preceding and following the active scroll marker. |
| [@scope](https://drafts.csswg.org/css-cascade-6/#scope-atrule) | First complete core implementation: 2025-12-02 (Chrome 143); Baseline newly available: 2025-12-12 | C 143 · F 146 · S 26.2 | Baseline newly available (2025-12-12) | The @scope CSS at-rule sets the scope for a group of rules. |
| [Anchor position container queries](https://drafts.csswg.org/css-anchor-position-2/#anchored-container-queries) | First complete core implementation: 2025-12-02 (Chrome 143) | C 143 · F — · S — | Limited availability | Anchor position container queries with the @container anchored(fallback: …) at-rule apply styles to an element based on the element's anchor position. |
| [cross-origin() for url()](https://drafts.csswg.org/css-values-5/#typedef-request-url-modifier-cross-origin-modifier) | First complete core implementation: 2025-12-12 (Safari 26.2) | C — · F — · S 26.2 | Limited availability | The url() CSS function accepts a cross-origin() modifier to control cross-origin resource sharing (CORS) when requesting the URL. For example, url("https://example.com" cross-origin(anonymous))) does not send credentials to the URL. |
| [random()](https://drafts.csswg.org/css-values-5/#random) | First complete core implementation: 2025-12-12 (Safari 26.2) | C — · F — · S 26.2 | Limited availability | The random() CSS function chooses a random numeric value within a specified range. This allows for dynamic, randomized styling using CSS. |
| [referrer-policy() for url()](https://drafts.csswg.org/css-values-5/#typedef-request-url-modifier-referrer-policy-modifier) | First complete core implementation: 2025-12-12 (Safari 26.2) | C — · F — · S 26.2 | Limited availability | The url() CSS function accepts a referrer-policy() modifier to choose which referrer to send when requesting the URL. For example, `url("https://example.com" referrer-policy(no-referrer)) does not send a referrer to the URL. |
| [Anchor positioning transforms](https://drafts.csswg.org/css-anchor-position-1/#anchoring) | First complete core implementation: 2026-01-13 (Chrome 144) | C 144 · F — · S — | Limited availability | Anchor positioned elements take CSS transforms on their anchor elements into account. |
| [caret-shape](https://drafts.csswg.org/css-ui-4/#propdef-caret-shape) | First complete core implementation: 2026-01-13 (Chrome 144) | C 144 · F — · S — | Limited availability | The caret-shape CSS property sets the shape of the insertion caret, the symbol that shows where the next character is to be inserted or deleted. |
| [overscroll-behavior](https://drafts.csswg.org/css-overscroll-1/) | First complete core implementation: 2026-01-13 (Chrome 144) | C 144 · F 150 · S — | Limited availability | The overscroll-behavior CSS property disables default scrolling behaviors when the edges of a scrolling area are reached. |
| [overflow-clip-margin](https://drafts.csswg.org/css-overflow-4/#overflow-clip-margin) | First complete core implementation: 2026-02-24 (Firefox 148) | C — · F 148 · S — | Limited availability | The overflow-clip-margin CSS property sets how far overflow content may appear outside the bounds of an element before it's clipped by effects such as overflow: clip. |
| [border-shape](https://drafts.csswg.org/css-borders-4/#border-shape) | First complete core implementation: 2026-04-07 (Chrome 147) | C 147 · F — · S — | Limited availability | The border-shape CSS property sets the geometry of the border box, changing the shape of any applicable border, border image, focus outline, or shadow. |
| [Element-scoped view transitions](https://drafts.csswg.org/css-view-transitions-2/#scoped-vt) | First complete core implementation: 2026-04-07 (Chrome 147) | C 147 · F — · S — | Limited availability | The startViewTransition() method of an Element object starts a view transition that affects only that element's DOM tree. You can use this to run separate elements' transitions concurrently. |
| [color-mix() with three or more colors](https://drafts.csswg.org/css-color-5/#color-mix) | First complete core implementation: 2026-04-21 (Firefox 150) | C — · F 150 · S — | Limited availability | The color-mix() CSS function accepts three or more colors. |
| [light-dark() image values](https://drafts.csswg.org/css-color-5/#typedef-light-dark-image) | First complete core implementation: 2026-04-21 (Firefox 150) | C — · F 150 · S — | Limited availability | The light-dark() CSS function accepts, in addition to colors, two <image> values, such as a gradient or URL, and uses one depending on the current color scheme. |
| [Hanging punctuation](https://drafts.csswg.org/css-text-4/#hanging-punctuation-property) | First complete core implementation: 2026-05-11 (Safari 26.5) | C — · F — · S 26.5 | Limited availability | The hanging-punctuation CSS property puts punctuation characters outside of the box to align the text with the rest of the document. |
| [Anchor positioning](https://drafts.csswg.org/css-anchor-position-1/#anchoring) | First complete core implementation: 2026-05-19 (Firefox 151) | C — · F 151 · S — | Limited availability | Anchor positioning places an element based on the position of another element. For example, you can place a tooltip next to the content it references. |
| [Gap decorations](https://drafts.csswg.org/css-gaps-1/) | First complete core implementation: 2026-06-02 (Chrome 149) | C 149 · F — · S — | Limited availability | The column-rule and row-rule CSS properties display decorative lines between columns and rows of a flex, grid, or multi-column layout. The rule-break, rule-outset, and rule-paint-order properties control the appearance of these lines. |

#### 16.5.2 DOM and Web APIs (54)

| Feature | 2025–today milestone | Core support | Status today | What it adds |
|---|---|---|---|---|
| [Shared worker](https://html.spec.whatwg.org/multipage/workers.html#shared-workers-introduction) | Baseline newly available: 2026-05-05 | C 5 · F 29 · S 16 | Baseline newly available (2026-05-05) | The SharedWorker() constructor runs a script in its own thread, which can send and receive messages with other scripts running at the same origin. |
| [<link rel="dns-prefetch">](https://html.spec.whatwg.org/multipage/links.html#link-type-dns-prefetch) | Baseline newly available: 2025-09-15 | C 46 · F 127 · S 5 | Baseline newly available (2025-09-15) | The rel="dns-prefetch" attribute for the <link> HTML element is a hint to the browser that the page or user is likely to request resources from another domain, so the browser should preemptively resolve DNS for the href value's domain. |
| [CSP violation reports](https://w3c.github.io/webappsec-csp/#reporting) | Baseline newly available: 2026-03-24 | C 74 · F 149 · S 18.4 | Baseline newly available (2026-03-24) | CSP violation reporting sends a report to a URL nominated by the Reporting-Endpoints header or the ReportingObserver API when a page violates its content security policy. |
| [Event timing](https://w3c.github.io/event-timing/) | Baseline newly available: 2025-12-12 | C 76 · F 89 · S 26.2 | Baseline newly available (2025-12-12) | The event and first-input performance entries and the PerformanceEventTiming API measures the latency of user input events, such as mouse clicks or keypresses. They're used to calculate Interaction to Next Paint (INP), a common metric for perceived responsiveness. |
| [Largest contentful paint (LCP)](https://w3c.github.io/largest-contentful-paint/) | Baseline newly available: 2025-12-12 | C 77 · F 122 · S 26.2 | Baseline newly available (2025-12-12) | The largest-contentful-paint performance entry and the LargestContentfulPaint API measures the time it takes for the largest image or text to appear. Largest contentful paint (LCP) is a common metric for perceived loading times. |
| [JavaScript modules in shared workers](https://html.spec.whatwg.org/multipage/workers.html#shared-workers-and-the-sharedworker-interface:dom-sharedworker-2) | Baseline newly available: 2026-05-05 | C 80 · F 114 · S 16 | Baseline newly available (2026-05-05) | The SharedWorker() constructor accepts { type: "module" } to load scripts that use import and export. Also known as ECMAScript modules or ESM in shared workers. |
| [Trusted types](https://w3c.github.io/trusted-types/dist/spec/) | Baseline newly available: 2026-02-24 | C 83 · F 148 · S 26 | Baseline newly available (2026-02-24) | Trusted types allow you to lock down insecure parts of the DOM API and prevent client-side cross-site scripting (XSS) attacks. |
| [Screen wake lock](https://w3c.github.io/screen-wake-lock/) | Baseline newly available: 2025-03-31 | C 84 · F 126 · S 16.4 | Baseline newly available (2025-03-31) | The navigator.wakeLock.request("screen") API prevents the device's screen from dimming or being turned off. |
| [Readable byte streams](https://streams.spec.whatwg.org/) | Baseline newly available: 2026-03-24 | C 89 · F 102 · S 26.4 | Baseline newly available (2026-03-24) | A ReadableStream constructed with { type: "bytes" } reads bytes from a stream without making extra copies, improving efficiency for streams of large chunks. Also known as BYOB or bring your own buffer. |
| [JavaScript modules in service workers](https://w3c.github.io/ServiceWorker/#dom-registrationoptions-type) | Baseline newly available: 2026-01-13 | C 91 · F 147 · S 15 | Baseline newly available (2026-01-13) | The navigator.serviceWorker.register() method accepts { type: "module" } to load scripts that use import and export. Also known as ECMAScript modules or ESM in service workers. |
| [URLPattern](https://urlpattern.spec.whatwg.org/) | Baseline newly available: 2025-09-15 | C 95 · F 142 · S 26 | Baseline newly available (2025-09-15) | The URLPattern API creates patterns that can be matched against URLs or URL components. |
| [Reporting API](https://w3c.github.io/reporting/) | Baseline newly available: 2026-03-24 | C 96 · F 149 · S 16.4 | Baseline newly available (2026-03-24) | The Reporting-Endpoints HTTP header and ReportingObserver() API send selected reports, such as Content Security Policy (CSP) violation reports or crash reports, to a nominated URL or callback function. |
| [WebTransport](https://w3c.github.io/webtransport/) | Baseline newly available: 2026-03-24 | C 97 · F 114 · S 26.4 | Baseline newly available (2026-03-24) | The WebTransport API transmits data between a client and a server, by using the HTTP/3 protocol. |
| [WebRTC encoded transform](https://w3c.github.io/webrtc-encoded-transform/) | Baseline newly available: 2025-10-03 | C 141 · F 117 · S 15.4 | Baseline newly available (2025-10-03) | The WebRTC encoded transform API allows you to modify audio and video streams in WebRTC connections. For example, it can be used for visual effects or custom codecs. |
| [Navigation API](https://html.spec.whatwg.org/multipage/nav-history-apis.html#navigation-api) | Baseline newly available: 2026-01-13 | C 102 · F 147 · S 26.2 | Baseline newly available (2026-01-13) | The navigation API initiates, intercepts, or modifies browser navigation actions. Not to be confused with the navigator API. |
| [Branch hinting (WebAssembly)](https://github.com/WebAssembly/branch-hinting/blob/main/proposals/branch-hinting/Overview.md) | Baseline newly available: 2026-02-24 | C 137 · F 148 · S 16 | Baseline newly available (2026-02-24) | Branch hints in WebAssembly allows a browser to optimize performance when a branch is a likely to take a specific path. |
| [Popover](https://html.spec.whatwg.org/multipage/popover.html) | Baseline newly available: 2025-01-27 | C 116 · F 125 · S 17 | Baseline newly available (2025-01-27) | The popover HTML attribute creates an overlay to display content on top of other page content. Popovers can be shown declaratively using HTML, or using the showPopover() method. |
| [Selection composed ranges](https://w3c.github.io/selection-api/#dom-selection-getcomposedranges) | Baseline newly available: 2025-08-19 | C 137 · F 142 · S 17 | Baseline newly available (2025-08-19) | The window.getSelection().getComposedRanges() method returns ranges that represent the current user selection, even if the selection spans across shadow tree boundaries. |
| [ClipboardItem.supports()](https://w3c.github.io/clipboard-apis/#dom-clipboarditem-supports) | Baseline newly available: 2025-03-31 | C 121 · F 127 · S 18.4 | Baseline newly available (2025-03-31) | The ClipboardItem.supports() static method checks if the browser supports writing data types such as "image/svg+xml" or other custom formats to the system clipboard. |
| [Zstandard compression](https://www.rfc-editor.org/info/rfc8878/) | Baseline newly available: 2026-02-11 | C 123 · F 126 · S 26.3 | Baseline newly available (2026-02-11) | Zstandard or zstd is a fast lossless compression algorithm. When used as a content encoding, it is often faster and offers better compression than brotli. |
| [Unsanitized HTML parsing methods](https://html.spec.whatwg.org/multipage/dynamic-markup-insertion.html#unsafe-html-parsing-methods) | Baseline newly available: 2025-09-15 | C 124 · F 128 · S 26 | Baseline newly available (2025-09-15) | The Document.parseHTMLUnsafe() static method parses HTML into a DOM tree, while the setHTMLUnsafe() method of Element and ShadowRoot parses and inserts HTML into an existing tree. No sanitization applies to these methods, so never call them with user-provided HTML strings. |
| [Memory64 (WebAssembly)](https://github.com/WebAssembly/memory64/blob/main/proposals/memory64/Overview.md) | First complete core implementation: 2025-01-07 (Firefox 134) | C 133 · F 134 · S — | Limited availability | Instructions accept 64-bit memory indexes. |
| [Device posture](https://w3c.github.io/device-posture/) | First complete core implementation: 2025-01-14 (Chrome 132) | C 132 · F — · S — | Limited availability | The device posture API and the device-posture CSS media feature reflect the physical posture of a device, such as whether a foldable device is folded or unfolded. |
| [Element capture](https://screen-share.github.io/element-capture/) | First complete core implementation: 2025-01-14 (Chrome 132) | C 132 · F — · S — | Limited availability | The restrictTo() method on screen capture media tracks limits capture to a specific element, excluding content which might occlude the element itself, such as video conferencing controls. |
| [Web authentication signal methods](https://w3c.github.io/webauthn/#sctn-signal-methods) | First complete core implementation: 2025-01-14 (Chrome 132) | C 132 · F — · S 26 | Limited availability | The signalUnknownCredential(), signalAllAcceptedCredentials(), and signalCurrentUserDetails() methods of PublicKeyCredential inform authenticators of the state of public key credentials, so that incorrect or revoked credentials may be updated, removed, or hidden. |
| [Attribution reporting](https://wicg.github.io/attribution-reporting-api/) | First complete core implementation: 2025-02-04 (Chrome 133) | C 133 · F — · S — | Limited availability | The attribution reporting API measures when an ad click or view leads to a conversion, such as a purchase on an advertiser site. |
| [moveBefore()](https://dom.spec.whatwg.org/#dom-parentnode-movebefore) | First complete core implementation: 2025-02-04 (Chrome 133) | C 133 · F 144 · S — | Limited availability | The moveBefore() DOM method relocates a node while preserving its state. For example, you can move the active element without losing focus, move an animated element without resetting the animation, or move an iframe without reloading its content. |
| [Protected audience](https://wicg.github.io/turtledove/) | First complete core implementation: 2025-03-04 (Chrome 134) | C 134 · F — · S — | Limited availability | The protected audience API facilitates advertisement sales by allowing sites to register users as part of an interest group or to choose which ads appear based on those interest groups, while minimizing the ability of advertisers to track specific members of the interest group. Also known as FLEDGE. |
| [Shared storage locks](https://wicg.github.io/shared-storage/#web-locks-integration) | First complete core implementation: 2025-03-04 (Chrome 134) | C 134 · F — · S — | Limited availability | The withLock option to set(), append(), delete(), clear(), and batchUpdate() methods of the sharedStorage API prevents duplicate reporting from cross-site race conditions. |
| [fetchLater](https://fetch.spec.whatwg.org/#dom-window-fetchlater) | First complete core implementation: 2025-04-01 (Chrome 135) | C 135 · F — · S — | Limited availability | The fetchLater() method requests a deferred fetch sent at an unknown time. The browser chooses a reliable time to send the request, ideally when the document is unloaded, and ignores the response. This API is useful for sending beacons to a server without expecting a particular response. |
| [Observable](https://wicg.github.io/observable/) | First complete core implementation: 2025-04-01 (Chrome 135) | C 135 · F — · S — | Limited availability | The when() method on a event target returns an Observable object, which provides a declarative API for subscribing to and operating on events. It's an alternative to addEventListener() callbacks. |
| [JavaScript promise integration (WebAssembly)](https://github.com/WebAssembly/js-promise-integration/blob/main/proposals/js-promise-integration/Overview.md) | First complete core implementation: 2025-05-27 (Chrome 137) | C 137 · F — · S — | Limited availability | The JavaScript promise integration (JSPI) suspends a WebAssembly module when it calls a JavaScript method that returns a promise. The module resumes when the promise is resolved. You can use this to call asynchronous Web APIs from synchronous WebAssembly. |
| [Language detector](https://webmachinelearning.github.io/translation-api/#language-detector-api) | First complete core implementation: 2025-06-24 (Chrome 138) | C 138 · F — · S — | Limited availability | The LanguageDetector API identifies the likely natural language that some text is written in. You can use this API to supplement machine translation when the source source language is not known. |
| [Summarizer](https://webmachinelearning.github.io/writing-assistance-apis/) | First complete core implementation: 2025-06-24 (Chrome 138) | C 138 · F — · S — | Limited availability | The Summarizer API uses an on-device language model to summarize text. |
| [Translator](https://webmachinelearning.github.io/translation-api/#translator-api) | First complete core implementation: 2025-06-24 (Chrome 138) | C 138 · F — · S — | Limited availability | The Translator API translates some text from one natural language to another, using machine translation. |
| [Secure payment confirmation](https://w3c.github.io/secure-payment-confirmation/) | First complete core implementation: 2025-08-05 (Chrome 139) | C 139 · F — · S — | Limited availability | The payment extension of a web authentication credential allows a relying party (such as a bank) to create a credential that can be queried by any merchant origin as part of an online checkout that uses the Payment Request API's secure-payment-confirmation payment method. Also known as SPC. |
| [Speech recognition](https://webaudio.github.io/web-speech-api/#speechreco-section) | First complete core implementation: 2025-08-05 (Chrome 139) | C 139 · F — · S — | Limited availability | The SpeechRecognition API converts audio into text using the device's speech recognition service. |
| [Digital credentials](https://w3c-fedid.github.io/digital-credentials/) | First complete core implementation: 2025-09-15 (Safari 26) | C 141 · F — · S 26 | Limited availability | The digital credentials API issues and requests digital credentials, such as driver's licenses or ID cards, with the browser or operating system. Digital credentials extend the navigator.credentials credential management API. |
| [WebGPU](https://gpuweb.github.io/gpuweb/) | First complete core implementation: 2025-09-15 (Safari 26) | C — · F — · S 26 | Limited availability | The navigator.gpu API performs operations such as rendering and computation on dedicated graphics hardware (also known as a Graphics Processing Unit). |
| [IndexedDB getAllRecords()](https://w3c.github.io/IndexedDB/#dom-idbindex-getallrecords) | First complete core implementation: 2025-09-30 (Chrome 141) | C 141 · F — · S — | Limited availability | The getAllRecords() method of IDBObjectStore and IDBIndex return records and their primary keys from an IndexedDB store or index. The records can be read in batches and in reverse order. The getAllRecords() methods speed up read operations on large datasets. |
| [Signature-based resource integrity](https://wicg.github.io/signature-based-sri/) | First complete core implementation: 2025-09-30 (Chrome 141) | C 141 · F — · S — | Limited availability | Signature-based resource integrity verifies a script's provenance by checking that the resource has been signed with a trusted key given by the <script> element's integrity attribute. |
| [Screen orientation lock](https://w3c.github.io/screen-orientation/#lock-method) | First complete core implementation: 2025-10-14 (Firefox 144) | C — · F 144 · S — | Limited availability | The screen.orientation.lock() method prevents changes to the screen orientation, typically in fullscreen applications such as games. For example, while locked, rotating a phone to the side won't change the screen orientation from landscape to portrait. |
| [Interest invokers](https://github.com/whatwg/html/pull/11006) | First complete core implementation: 2025-10-28 (Chrome 142) | C 142 · F — · S — | Limited availability | Interest invokers, registered by the interestfor HTML attribute, trigger events and actions on a target element when a user shows interest in the element, through behaviors such as hover, focus, or long-press. Pseudo-elements apply styles to sources and targets of interest. |
| [Local network access](https://wicg.github.io/local-network-access/) | First complete core implementation: 2025-10-28 (Chrome 142) | C 142 · F — · S — | Limited availability | The "local-network-access" user permission (and certain actions that imply this permission, such as a fetch() request with { targetAddressSpace: "local" }) allows a site to send requests to servers on a user's local network. |
| [clipboardchange](https://w3c.github.io/clipboard-apis/#clipboard-event-clipboardchange) | First complete core implementation: 2026-01-13 (Chrome 144) | C 144 · F — · S — | Limited availability | The clipboardchange event for navigator.clipboard fires when the user modifies the clipboard's contents. |
| [Crash report storage](https://wicg.github.io/crash-reporting/#crash-report-storage) | First complete core implementation: 2026-02-10 (Chrome 145) | C 145 · F — · S — | Limited availability | The window.crashReport object is a key-value store to record information about your application's state. If there's a crash, then the data in the key-value store is sent to your crash reporting endpoint, to help you pinpoint the cause of the crash. |
| [Navigation timing confidence](https://w3c.github.io/navigation-timing/#sec-performance-timing-confidence) | First complete core implementation: 2026-02-10 (Chrome 145) | C 145 · F — · S — | Limited availability | The confidence property of a navigation timing entry describes whether the navigation metric is likely to be representative the page's performance (high confidence) or affected by transient conditions, such as browser startup (low confidence). |
| [Origin](https://html.spec.whatwg.org/multipage/browsers.html#the-origin-interface) | First complete core implementation: 2026-02-10 (Chrome 145) | C 145 · F — · S 26.5 | Limited availability | An Origin object represents an origin, as in a scheme, hostname, and port. You can use it to make same-site and same-origin comparisons. |
| [Navigation precommit handlers](https://html.spec.whatwg.org/multipage/nav-history-apis.html#dom-navigationinterceptoptions-precommithandler) | First complete core implementation: 2026-02-24 (Firefox 148) | C 146 · F 148 · S — | Limited availability | The precommitHandler callback option to NavigateEvent's intercept() method returns a promise that defers navigation until the promise resolves. You can use this to change the navigation's URL, state, and history before navigation occurs. |
| [Sanitizer API](https://html.spec.whatwg.org/multipage/dynamic-markup-insertion.html#html-sanitization) | First complete core implementation: 2026-02-24 (Firefox 148) | C — · F 148 · S — | Limited availability | The Document.parseHTML() static method and the setHTML() method of Element and ShadowRoot objects parse and insert HTML into the DOM in a way that can prevent cross-site scripting attacks. The Sanitizer API can customize the sanitization process. |
| [Layers (WebXR)](https://immersive-web.github.io/layers/) | First complete core implementation: 2026-04-07 (Chrome 147) | C 147 · F — · S — | Limited availability | WebXR layer types, such as XRCylinderLayer, XRCylinderLayer, XREquirectLayer, XRProjectionLayer or XRQuadLayer, are managed by the system compositor, to reduce latency or resampling. |
| [ariaNotify()](https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/main/Accessibility/AriaNotify/explainer.md) | First complete core implementation: 2026-04-21 (Firefox 150) | C — · F 150 · S — | Limited availability | The ariaNotify() method of Element and Document requests assistive technology software, if activated, to announce a message to the user. This can help make dynamic content changes more accessible to users. |
| [LanguageModel](http://webmachinelearning.github.io/prompt-api/) | First complete core implementation: 2026-05-05 (Chrome 148) | C 148 · F — · S — | Limited availability | The LanguageModel API prompts an on-device language model. Also known as the Prompt API. |
| [Web app origin migration](https://wicg.github.io/manifest-incubations/#web-application-origin-migration) | First complete core implementation: 2026-06-02 (Chrome 149) | C 149 · F — · S — | Limited availability | The migrate_to and migrate_from web app manifest members move an installed app from one origin to another, within the same site. They preserve the user's installation settings on the device, like shortcuts. |

#### 16.5.3 HTML and declarative UI (12)

| Feature | 2025–today milestone | Core support | Status today | What it adds |
|---|---|---|---|---|
| [contenteditable="plaintext-only"](https://html.spec.whatwg.org/multipage/interaction.html#attr-contenteditable-plaintextonly-state) | Baseline newly available: 2025-03-04 | C 51 · F 136 · S 5.1 | Baseline newly available (2025-03-04) | The contenteditable="plaintext-only" global HTML attribute allows the user to edit the content of an element, but prevents rich-text formatting. |
| [<input type="file" webkitdirectory>](https://wicg.github.io/entries-api/#html-forms) | Baseline newly available: 2025-08-19 | C 13 · F 50 · S 11.1 | Baseline newly available (2025-08-19) | The <input type="file" webkitdirectory> HTML element shows a file picker from which users can choose a folder to upload with the form. |
| [popover="hint"](https://html.spec.whatwg.org/multipage/popover.html#attr-popover-hint) | First complete core implementation: 2025-02-04 (Chrome 133) | C 133 · F 149 · S — | Limited availability | The popover="hint" global HTML attribute creates a popover that is subordinate to popovers with a popover="auto" attribute. You can use this to create tooltips that don't dismiss auto popovers. |
| [<dialog closedby>](https://html.spec.whatwg.org/multipage/interactive-elements.html#attr-dialog-closedby) | First complete core implementation: 2025-03-04 (Chrome 134) | C 134 · F 141 · S — | Limited availability | The closedby HTML attribute for <dialog> sets which user actions close a dialog. For example, closedby="any" allows the dialog to be closed by clicking outside of it. |
| [<meta name="application-title">](https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/main/DocumentSubtitle/explainer.md) | First complete core implementation: 2025-03-04 (Chrome 134) | C 134 · F — · S — | Limited availability | The name="application-title" attribute for the <meta> HTML element sets an installed web application's title bar text. |
| [dialog.requestClose()](https://html.spec.whatwg.org/multipage/interactive-elements.html#dom-dialog-requestclose) | First complete core implementation: 2025-03-04 (Chrome 134); Baseline newly available: 2025-05-27 | C 134 · F 139 · S 18.4 | Baseline newly available (2025-05-27) | The requestClose() method of a <dialog> HTML element closes the dialog, firing a cancel event first, which listeners can use to prevent the dialog from closing. This differs from the close() method, which only fires the non-cancelable close event. |
| [alpha and colorspace attributes for <input type=color>](https://html.spec.whatwg.org/multipage/input.html#attr-input-alpha) | First complete core implementation: 2025-03-31 (Safari 18.4) | C — · F — · S 18.4 | Limited availability | The ability to control the opacity of a color picked using <input type="color"> and determine the colorspace of the selected color. |
| [Customizable <select>](https://open-ui.org/components/customizableselect/) | First complete core implementation: 2025-04-01 (Chrome 135) | C 135 · F — · S — | Limited availability | The <select> element's appearance, including the button, selected option, picker dropdown, and options, can be customized using CSS. |
| [Invoker commands](https://html.spec.whatwg.org/multipage/form-elements.html#attr-button-command) | First complete core implementation: 2025-04-01 (Chrome 135); Baseline newly available: 2025-12-12 | C 135 · F 144 · S 26.2 | Baseline newly available (2025-12-12) | The command and commandfor attributes for the <button> HTML element dispatch an action to an element when the button is invoked (by click or keystroke), as a declarative alternative to addEventListener() calls or onclick attribute handlers. |
| [Scroll markers](https://drafts.csswg.org/css-overflow-5/#scroll-markers) | First complete core implementation: 2025-04-01 (Chrome 135) | C 135 · F — · S — | Limited availability | A scroll marker scrolls a container to a scroll target. The ::scroll-marker CSS pseudo-element selects a scroll marker in a ::scroll-marker-group pseudo-element, generated before or after the scroll container. You can use them to navigate and style tables of contents, tab panels, and carousels. |
| [<geolocation>](https://wicg.github.io/PEPC/geolocation-element.html) | First complete core implementation: 2026-01-13 (Chrome 144) | C 144 · F — · S — | Limited availability | The <geolocation> HTML element represents a button that, upon activation, prompts the user to choose whether to grant the page access to geolocation data. |
| [<meta name="text-scale">](https://drafts.csswg.org/css-fonts-5/#text-scale-meta) | First complete core implementation: 2026-03-10 (Chrome 146) | C 146 · F — · S — | Limited availability | The <meta name="text-scale" content="scale" /> HTML element allows the browser's initial font size to be affected by the operating system text scale settings. The <meta name="text-scale" content="legacy" /> element is the default behavior that respects only browser font-size settings. |

#### 16.5.4 JavaScript language and built-ins (16)

| Feature | 2025–today milestone | Core support | Status today | What it adds |
|---|---|---|---|---|
| [Atomics.waitAsync()](https://tc39.es/ecma262/multipage/structured-data.html#sec-atomics.waitasync) | Baseline newly available: 2025-11-11 | C 90 · F 145 · S 16.4 | Baseline newly available (2025-11-11) | The Atomics.waitAsync() static method waits for a value in a shared memory location, providing a promise when the expected value is not yet in memory. The waitAsync() method is a non-blocking alternative to Atomics.wait(). |
| [Intl.DurationFormat](https://tc39.es/proposal-intl-duration-format/) | Baseline newly available: 2025-03-04 | C 129 · F 136 · S 16.4 | Baseline newly available (2025-03-04) | The Intl.DurationFormat API creates a locale-aware formatter that turns an object representing a duration (such as days, hours, and minutes) into a string. |
| [JSON source text access](https://tc39.es/proposal-json-parse-with-source/#sec-json-object) | Baseline newly available: 2025-03-31 | C 114 · F 135 · S 18.4 | Baseline newly available (2025-03-31) | To serialize and parse JSON in a lossless way, JSON.stringify() handles rawJSON values and JSON.parse()'s reviver callback takes a source context parameter. |
| [JSON import attributes](https://html.spec.whatwg.org/multipage/webappapis.html#json-module-script) | Baseline newly available: 2025-04-29 | C 123 · F 138 · S 17.2 | Baseline newly available (2025-04-29) | Module import … with { type: "json" } statements load JSON data. Also known as JSON module scripts. |
| [Iterator methods](https://tc39.es/ecma262/multipage/control-abstraction-objects.html#sec-iterator-helper-objects) | Baseline newly available: 2025-03-31 | C 122 · F 131 · S 18.4 | Baseline newly available (2025-03-31) | The Iterator object is an abstract base for objects that implement the iterator protocol. It provides methods common to built-in iterators, such as filter(), find(), map(), and reduce(). You can also use the static method Iterator.from() to convert an existing iterable into an Iterator. |
| [Float16Array](https://tc39.es/ecma262/multipage/global-object.html#sec-float16array) | Baseline newly available: 2025-04-04 | C 135 · F 129 · S 18.2 | Baseline newly available (2025-04-04) | Float16Array is a typed array of 16-bit floating point numbers. |
| [Promise.try()](https://tc39.es/ecma262/multipage/control-abstraction-objects.html#sec-promise.try) | Baseline newly available: 2025-01-07 | C 128 · F 134 · S 18.2 | Baseline newly available (2025-01-07) | The Promise.try() static method returns a promise that takes a callback of any kind (returns or throws, synchronously or asynchronously) and wraps its result in a Promise. |
| [Uint8Array base64 and hex conversion](https://tc39.es/ecma262/multipage/indexed-collections.html#sec-additional-properties-of-the-uint8array-constructor) | Baseline newly available: 2025-09-05 | C 140 · F 133 · S 18.2 | Baseline newly available (2025-09-05) | The Uint8Array object methods fromBase64(), toBase64(), and setFromBase64() convert to and from base64 strings. The fromHex(), toHex(), and setFromHex() methods convert to and from hex strings. |
| [RegExp.escape()](https://tc39.es/ecma262/multipage/text-processing.html#sec-regexp.escape) | Baseline newly available: 2025-05-01 | C 136 · F 134 · S 18.2 | Baseline newly available (2025-05-01) | The RegExp.escape() static method takes a string and replaces any characters that are potentially special characters of a regular expression with equivalent escape sequences. For example, RegExp.escape("[abc]") returns "\\[abc\\]". |
| [Atomics.pause()](https://tc39.es/proposal-atomics-microwait/) | First complete core implementation: 2025-02-04 (Chrome 133); Baseline newly available: 2025-04-01 | C 133 · F 137 · S 18.4 | Baseline newly available (2025-04-01) | The Atomics.pause() static method gives a hint to the CPU that the code calling the method is in a short-duration wait for shared memory, known as spinning or a spinlock. |
| [Error.isError()](https://tc39.es/ecma262/multipage/fundamental-objects.html#sec-error.iserror) | First complete core implementation: 2025-03-04 (Chrome 134) | C 134 · F 138 · S — | Limited availability | The Error.isError() static method checks whether a value is an Error object. |
| [Explicit resource management](https://tc39.es/proposal-async-explicit-resource-management/) | First complete core implementation: 2025-03-04 (Chrome 134) | C 134 · F 141 · S — | Limited availability | The using and await using declarations and the dispose and asyncDispose symbols manage the lifecycle of resources such as file handles and streams. The DisposableStack and AsyncDisposableStack objects can group, dispose, and coordinate dependencies between multiple disposable resources. |
| [Math.sumPrecise()](https://tc39.es/ecma262/multipage/numbers-and-dates.html#sec-math.sumprecise) | First complete core implementation: 2025-04-01 (Firefox 137); Baseline newly available: 2026-04-10 | C 147 · F 137 · S 26.2 | Baseline newly available (2026-04-10) | The Math.sumPrecise() static method returns the sum of an iterable of numbers. It avoids the precision loss of intermediate partial sums, as found using reduce() or a loop to add together an array of values. |
| [Temporal](https://tc39.es/proposal-temporal/) | First complete core implementation: 2025-05-27 (Firefox 139) | C 144 · F 139 · S — | Limited availability | The Temporal API allows you to work with dates, times, time zones, and durations. It is more powerful than the Date API. |
| [Map getOrInsert()](https://tc39.es/ecma262/multipage/keyed-collections.html#sec-map.prototype.getorinsert) | First complete core implementation: 2025-10-14 (Firefox 144); Baseline newly available: 2026-02-14 | C 145 · F 144 · S 26.2 | Baseline newly available (2026-02-14) | The getOrInsert() and getOrInsertComputed() methods of Map objects get a value, setting and getting a default value if needed. |
| [Iterator.concat()](https://tc39.es/ecma262/multipage/control-abstraction-objects.html#sec-iterator.concat) | First complete core implementation: 2026-01-13 (Firefox 147); Baseline newly available: 2026-03-24 | C 146 · F 147 · S 26.4 | Baseline newly available (2026-03-24) | The Iterator.concat() JavaScript method returns an iterator that yields values from a sequence of iterators, exhausting each iterator before moving on to the next. |

### 16.6 Very recent stable-release delta (19)
These features are present in official stable release notes but are not yet represented as separate, normalized entries in the Web Features dataset used above. They are intentionally kept outside the 147-feature count to avoid pretending the two data models are identical.

| Area | Feature | First stable release in scope | Purpose |
|---|---|---|---|
| CSS | [`at-rule()` in `@supports`](https://developer.chrome.com/release-notes/148) | Chrome 148 | Feature-detect support for CSS at-rules. |
| CSS | [`revert-rule`](https://developer.chrome.com/release-notes/148) | Chrome 148 | Roll back only the current style rule in the cascade. |
| HTML | [`loading="lazy"` on `<video>` and `<audio>`](https://developer.chrome.com/release-notes/148) | Chrome 148 | Native lazy loading for media elements. |
| CSS | [`path()`, `shape()`, `rect()`, `xywh()` in `shape-outside`](https://developer.chrome.com/release-notes/149) | Chrome 149 | Richer float-exclusion geometry; `rect()` and `xywh()` became Baseline. |
| CSS | [`AccentColor` and `AccentColorText`](https://developer.chrome.com/release-notes/150) | Chrome 150 | Expose the OS accent colors to installed web apps. |
| CSS | [Rounded `polygon()`](https://developer.chrome.com/release-notes/150) | Chrome 150 | Optional length parameter rounds polygon corners. |
| CSS | [Animatable `zoom`](https://developer.chrome.com/release-notes/150) | Chrome 150 | Animate layout-affecting CSS zoom as a number. |
| CSS | [`text-fit`](https://developer.chrome.com/release-notes/150) | Chrome 150 | Scale text to fill the width of its box. |
| CSS | [`background-clip: border-area`](https://developer.chrome.com/release-notes/150) | Chrome 150 | Clip backgrounds to the painted border area. |
| CSS | [`image(<color>)`](https://developer.chrome.com/release-notes/150) | Chrome 150 | Create a solid-color CSS image value. |
| CSS | [Comma-separated container queries](https://developer.chrome.com/release-notes/150) | Chrome 150 | OR multiple conditions inside one `@container` rule. |
| CSS | [`page-margin-safety`](https://developer.chrome.com/release-notes/150) | Chrome 150 | Avoid unprintable printer-edge areas. |
| CSS | [`flex-wrap: balance`](https://developer.chrome.com/release-notes/150) | Chrome 150 | Balance items across flex lines. |
| CSS | [`named-feature()` in `@supports`](https://developer.chrome.com/release-notes/150) | Chrome 150 | Test named capabilities that declaration syntax cannot detect. |
| CSS/SVG | [`path-length` property](https://developer.chrome.com/release-notes/150) | Chrome 150 | CSS equivalent of SVG geometry `pathLength`. |
| HTML | [`focusgroup`](https://developer.chrome.com/release-notes/150) | Chrome 150 | Declarative arrow-key navigation and roving focus for composite widgets. |
| HTML | [Out-of-order streaming](https://developer.chrome.com/release-notes/150) | Chrome 150 | Use `<template for>` and processing-instruction ranges to update document regions without JavaScript. |
| HTML/DOM | [HTML processing instructions](https://developer.chrome.com/release-notes/150) | Chrome 150 | Parse `<?target data?>` nodes and expose an attribute-like API. |
| DOM | [Programmatic scroll promises](https://developer.chrome.com/release-notes/150) | Chrome 150 | `scrollTo()`, `scrollBy()`, and `scrollIntoView()` return completion promises. |

### 16.7 Beta / preview watchlist (not counted as shipped)
These were available only in beta as of 10 July 2026 and must not be treated as generally shipped.

| Preview browser | Feature | Why it matters |
|---|---|---|
| Safari 27 beta | Transform-aware anchor positioning | Anchored UI follows transformed anchors. |
| Safari 27 beta | `:heading` | Matches all HTML heading levels, with level filtering. |
| Safari 27 beta | `revert-rule` | More precise cascade rollback. |
| Safari 27 beta | `stretch` sizing keyword | Fill available space while accounting for margins. |
| Safari 27 beta | `position-anchor: normal \| none` | Revised opt-in/default anchor behavior. |
| Safari 27 beta | `anchor-valid` and `anchor-visible` | Updated position-visibility keywords. |
| Safari 27 beta | `contain: style` for quotes | Scope quote-counter effects to a subtree. |
| Firefox 153 beta | `Intl.Locale` get-info methods | `getCalendars()`, `getWeekInfo()`, `getTimeZones()`, and related methods. |
| Firefox 153 beta | `IDBObjectStore.getAllRecords()` / `IDBIndex.getAllRecords()` | Faster bulk IndexedDB record retrieval. |
| Firefox 153 beta | `Error.stackTraceLimit` | Configure maximum captured stack depth. |
| Firefox 153 beta | `RTCDtlsTransport.getRemoteCertificates()` | Inspect remote WebRTC certificates. |

### 16.8 Notable removals and behavior changes
- Legacy DOM mutation events such as `DOMNodeInserted`, `DOMNodeRemoved`, and `DOMSubtreeModified` were removed from Firefox 140 after earlier Chrome removal. Use `MutationObserver`.
- Chrome 138 and Firefox 140 changed HTML serialization to escape `<` and `>` in attribute values, closing a mutation-XSS class of problems; Safari 26 followed.
- Chrome 149 changed editable/interactive `text-overflow: ellipsis` content to temporarily clip during interaction so hidden text can be reached.
- Chrome 150 gives workers created from `data:` URLs opaque origins instead of inheriting the creator's origin.
- Several entries are refinements to earlier platform features rather than brand-new top-level APIs. This report includes them when the refinement is independently tracked or materially changes author capabilities.

### 16.9 Sources

Dataset snapshot and report date: **10 July 2026** (Web Features **3.32.0**, MDN BCD cross-check).

- [Baseline definition and core-browser model](https://web.dev/baseline)
- [Web Features project](https://github.com/web-platform-dx/web-features)
- [Chrome stable release notes index](https://developer.chrome.com/release-notes)
- [Firefox developer release notes index](https://developer.mozilla.org/en-US/docs/Mozilla/Firefox/Releases)
- [WebKit news and Safari release notes](https://webkit.org/blog/category/news/)
- [Interop 2025 focus areas](https://web.dev/blog/interop-2025)
- [Interop 2026 focus areas](https://web.dev/blog/interop-2026)
- 2025 monthly platform reports: [January](https://web.dev/blog/web-platform-01-2025) · [February](https://web.dev/blog/web-platform-02-2025) · [March](https://web.dev/blog/web-platform-03-2025) · [April](https://web.dev/blog/web-platform-04-2025) · [May](https://web.dev/blog/web-platform-05-2025) · [June](https://web.dev/blog/web-platform-06-2025) · [July](https://web.dev/blog/web-platform-07-2025) · [August](https://web.dev/blog/web-platform-08-2025) · [September](https://web.dev/blog/web-platform-09-2025) · [October](https://web.dev/blog/web-platform-10-2025) · [November](https://web.dev/blog/web-platform-11-2025) · [December](https://web.dev/blog/web-platform-12-2025)
- 2026 monthly platform reports: [January](https://web.dev/blog/web-platform-01-2026) · [February](https://web.dev/blog/web-platform-02-2026) · [March](https://web.dev/blog/web-platform-03-2026) · [April](https://web.dev/blog/web-platform-04-2026) · [May](https://web.dev/blog/web-platform-05-2026) · [June](https://web.dev/blog/web-platform-06-2026)
- [Safari 26.4 detailed release](https://webkit.org/blog/17862/webkit-features-for-safari-26-4/)
- [Safari 27 beta preview](https://webkit.org/blog/17967/news-from-wwdc26-webkit-in-safari-27-beta/)
- [Firefox 153 beta notes](https://developer.mozilla.org/en-US/docs/Mozilla/Firefox/Releases/153)

### 16.10 Scope cautions

No finite report can enumerate every conformance fix, prefixed-alias cleanup, WebGL/WebGPU limit change, codec addition, DevTools feature, enterprise policy, extension API, origin trial, or platform-specific bug fix. “Comprehensive” here means every feature meeting the stated Web Features criteria plus the stable-release delta above—not every line item in every browser changelog. WebAssembly, WebXR, WebGPU, identity/payment/privacy APIs, and on-device AI APIs are included when exposed to ordinary site JavaScript, even though they sit beyond the narrowest interpretation of “HTML/CSS/JS.”
