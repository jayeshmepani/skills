# Design Theory & Practice for Web Interfaces

> **Edition:** July 2026  
> **Scope:** Evidence-aware visual design, color, typography, spacing, responsive layout, product/admin interfaces, marketing sites, accessibility, tokens, testing, and governance.  
> **Companion:** `02-design-styles-systems.md` contains the non-duplicated catalogue of named styles, historical movements, major design systems, and implementation methodologies.

This is a living reference. It distinguishes standards from research findings, heuristics, and trends; avoids unsupported universal claims; and requires context-specific validation.

## Table of Contents

- [1. Executive Summary](#1-executive-summary)
- [2. Foundational Design Theory, Gestalt & Attention](#2-foundational-design-theory-gestalt-attention)
  - [2.1 Visual Hierarchy & Attention Management](#21-visual-hierarchy-attention-management)
  - [2.2 Balance & Layout Stability](#22-balance-layout-stability)
  - [2.3 Contrast as a Design Tool](#23-contrast-as-a-design-tool)
  - [2.4 Alignment & Grid-Based Structure](#24-alignment-grid-based-structure)
  - [2.5 Gestalt Grouping: Proximity, Similarity, Continuity and More](#25-gestalt-grouping-proximity-similarity-continuity-and-more)
  - [2.6 Repetition, Rhythm & Consistency](#26-repetition-rhythm-consistency)
  - [2.7 Whitespace (Negative Space)](#27-whitespace-negative-space)
  - [2.8 Emphasis & Focal Points](#28-emphasis-focal-points)
  - [2.9 Proportion Heuristics: Golden Ratio & Rule of Thirds](#29-proportion-heuristics-golden-ratio-rule-of-thirds)
  - [2.10 Decision and Interaction Heuristics](#210-decision-and-interaction-heuristics)
  - [2.11 Scanning and Reading Patterns](#211-scanning-and-reading-patterns)
- [3. Color Theory & Semantic Color Systems](#3-color-theory-semantic-color-systems)
  - [3.1 Color Fundamentals: Hue, Chroma/Saturation, Lightness and Value](#31-color-fundamentals-hue-chromasaturation-lightness-and-value)
  - [3.2 Color Models for the Web: RGB, HSL, HSB, LAB/LCH, OKLCH](#32-color-models-for-the-web-rgb-hsl-hsb-lablch-oklch)
  - [3.3 Color Harmony Systems](#33-color-harmony-systems)
  - [3.4 Color Psychology & Emotional Associations](#34-color-psychology-emotional-associations)
  - [3.5 Cultural Context & Color Meaning](#35-cultural-context-color-meaning)
  - [3.6 The 60-30-10 Rule](#36-the-60-30-10-rule)
  - [3.7 Building a Semantic UI Color System](#37-building-a-semantic-ui-color-system)
  - [3.8 Complete Light & Dark Palette with Measured Contrast Ratios](#38-complete-light-dark-palette-with-measured-contrast-ratios)
  - [3.9 Generating Palettes: A Repeatable Token-Based Method](#39-generating-palettes-a-repeatable-token-based-method)
  - [3.10 Dark Mode Design Best Practices](#310-dark-mode-design-best-practices)
  - [3.10.1 Gamut, Forced Colors and Real-World Validation](#3101-gamut-forced-colors-and-real-world-validation)
  - [3.11 Current Directional Trends (Non-Normative)](#311-current-directional-trends-non-normative)
- [4. Typography Systems, Readability & Font Performance](#4-typography-systems-readability-font-performance)
  - [4.1 Typography as a Primary Interface Material](#41-typography-as-a-primary-interface-material)
  - [4.2 Typeface Classification & Selection](#42-typeface-classification-selection)
  - [4.3 Modular Type Scales](#43-modular-type-scales)
  - [4.4 Line Height (Leading)](#44-line-height-leading)
  - [4.5 Letter Spacing (Tracking) & Kerning](#45-letter-spacing-tracking-kerning)
  - [4.6 Line Length (Measure)](#46-line-length-measure)
  - [4.7 Font Weight Strategy](#47-font-weight-strategy)
  - [4.8 Font Pairing Principles](#48-font-pairing-principles)
  - [4.9 Tabular/Monospaced Numerals for Data](#49-tabularmonospaced-numerals-for-data)
  - [4.10 Font Loading & Performance](#410-font-loading-performance)
  - [4.11 Fluid Typography with clamp()](#411-fluid-typography-with-clamp)
  - [4.12 Contextual Typography Decisions](#412-contextual-typography-decisions)
  - [4.13 Font Metrics, Internationalization and Resilience](#413-font-metrics-internationalization-and-resilience)
- [5. Spacing, Grids, Responsive Layout & Reflow](#5-spacing-grids-responsive-layout-reflow)
  - [5.1 Spacing Grids: 4-Unit and 8-Unit Systems](#51-spacing-grids-4-unit-and-8-unit-systems)
  - [5.2 Spacing Scale & Token System](#52-spacing-scale-token-system)
  - [5.3 Macro vs. Micro Whitespace](#53-macro-vs-micro-whitespace)
  - [5.4 The Internal ≤ External Rule](#54-the-internal-external-rule)
  - [5.5 Grid Systems: 12-Column & CSS Grid](#55-grid-systems-12-column-css-grid)
  - [5.6 Breakpoints & Container Widths](#56-breakpoints-container-widths)
  - [5.7 Content Width & Reading Measure](#57-content-width-reading-measure)
  - [5.8 CSS Grid vs. Flexbox vs. Container Queries](#58-css-grid-vs-flexbox-vs-container-queries)
  - [5.9 Responsive Design: Constraint-First and Mobile-First](#59-responsive-design-constraint-first-and-mobile-first)
  - [5.10 Density Modes and Semantic Spacing](#510-density-modes-and-semantic-spacing)
  - [5.11 Container-Driven Components](#511-container-driven-components)
  - [5.12 Reflow, Zoom, Safe Areas and Dynamic Viewports](#512-reflow-zoom-safe-areas-and-dynamic-viewports)
- [6. Product, Admin & Dashboard Design](#6-product-admin-dashboard-design)
  - [6.1 Product and Admin Design Philosophy](#61-product-and-admin-design-philosophy)
  - [6.2 Admin Layout Structure (App Shell Pattern)](#62-admin-layout-structure-app-shell-pattern)
  - [6.3 Sidebar Navigation Design](#63-sidebar-navigation-design)
  - [6.4 Data Tables: The Core Admin Surface](#64-data-tables-the-core-admin-surface)
  - [6.5 KPI Cards & Dashboard Widgets](#65-kpi-cards-dashboard-widgets)
  - [6.6 Form Design in Admin](#66-form-design-in-admin)
  - [6.7 Data Visualization & Chart Design](#67-data-visualization-chart-design)
  - [6.8 Color Use in Admin Templates](#68-color-use-in-admin-templates)
  - [6.9 Admin-Specific Typography Details](#69-admin-specific-typography-details)
  - [6.10 Admin Density Controls](#610-admin-density-controls)
  - [6.11 Progressive Disclosure](#611-progressive-disclosure)
  - [6.12 Responsive and Accessible Data Tables](#612-responsive-and-accessible-data-tables)
  - [6.13 Command, Undo and Destructive-Action Design](#613-command-undo-and-destructive-action-design)
- [7. Public-Facing & Marketing-Site Design](#7-public-facing-marketing-site-design)
  - [7.1 Hero Section Design](#71-hero-section-design)
  - [7.2 Landing Page Flow & Narrative Arc](#72-landing-page-flow-narrative-arc)
  - [7.3 CTA Design](#73-cta-design)
  - [7.4 Social Proof Patterns](#74-social-proof-patterns)
  - [7.5 Cards & Content Grouping](#75-cards-content-grouping)
  - [7.6 Navigation Design](#76-navigation-design)
  - [7.7 Motion & Microinteractions](#77-motion-microinteractions)
  - [7.8 Component-First Design Thinking](#78-component-first-design-thinking)
  - [7.9 Content Design and Evidence Hierarchy](#79-content-design-and-evidence-hierarchy)
  - [7.10 Ethical Conversion Design](#710-ethical-conversion-design)
- [8. Accessibility & Inclusive Design](#8-accessibility-inclusive-design)
  - [8.1 WCAG 2.2 Visual Requirements](#81-wcag-22-visual-requirements)
  - [8.2 Contrast and State Design](#82-contrast-and-state-design)
  - [8.3 Do Not Encode Meaning with Color Alone](#83-do-not-encode-meaning-with-color-alone)
  - [8.4 Focus, Keyboard and Source Order](#84-focus-keyboard-and-source-order)
  - [8.5 Text Spacing, Zoom and Reflow](#85-text-spacing-zoom-and-reflow)
  - [8.6 Motion, Transparency and Sensory Preferences](#86-motion-transparency-and-sensory-preferences)
  - [8.7 Semantic HTML, Names and Instructions](#87-semantic-html-names-and-instructions)
  - [8.8 ARIA and Complex Widgets](#88-aria-and-complex-widgets)
  - [8.9 Neuro-Inclusive and Cognitive Design](#89-neuro-inclusive-and-cognitive-design)
  - [8.10 Legal and Organizational Scope](#810-legal-and-organizational-scope)
- [9. Design Tokens & Implementation Contracts](#9-design-tokens-implementation-contracts)
  - [9.1 Token Architecture](#91-token-architecture)
  - [9.2 Naming Principles](#92-naming-principles)
  - [9.3 DTCG 2025.10 Format](#93-dtcg-202510-format)
  - [9.4 CSS Custom Properties](#94-css-custom-properties)
  - [9.5 Theme and Mode Strategy](#95-theme-and-mode-strategy)
  - [9.6 Tailwind CSS Integration](#96-tailwind-css-integration)
  - [9.7 Bootstrap Integration](#97-bootstrap-integration)
  - [9.8 Sass/SCSS and Build-Time Adapters](#98-sassscss-and-build-time-adapters)
  - [9.9 Component Contracts](#99-component-contracts)
  - [9.10 Governance and Versioning](#910-governance-and-versioning)
- [10. Testing, Validation & Quality Assurance](#10-testing-validation-quality-assurance)
  - [10.1 Quality Model](#101-quality-model)
  - [10.2 Automated Accessibility Testing](#102-automated-accessibility-testing)
  - [10.3 Component-State Coverage](#103-component-state-coverage)
  - [10.4 Interaction and Keyboard Tests](#104-interaction-and-keyboard-tests)
  - [10.5 Visual Regression](#105-visual-regression)
  - [10.6 Manual Accessibility Protocol](#106-manual-accessibility-protocol)
  - [10.7 Usability and Content Validation](#107-usability-and-content-validation)
  - [10.8 Performance and Field Quality](#108-performance-and-field-quality)
  - [10.9 Cross-Browser and Device Matrix](#109-cross-browser-and-device-matrix)
  - [10.10 Release Gates](#1010-release-gates)
- [11. Complete Design Workflow & Governance](#11-complete-design-workflow-governance)
  - [11.1 Evidence and Decision Records](#111-evidence-and-decision-records)
  - [11.2 Design-System Governance](#112-design-system-governance)
- [12. Release Evidence Checklist](#12-release-evidence-checklist)
  - [12.1 Foundation and Content](#121-foundation-and-content)
  - [12.2 Visual System](#122-visual-system)
  - [12.3 Responsive and Internationalized Layout](#123-responsive-and-internationalized-layout)
  - [12.4 Accessibility](#124-accessibility)
  - [12.5 Performance and Resilience](#125-performance-and-resilience)
  - [12.6 Quality, Governance, and Release](#126-quality-governance-and-release)
- [13. Tools & Research Methods](#13-tools-research-methods)
  - [13.1 Design and System Authoring](#131-design-and-system-authoring)
  - [13.2 Color, Typography, and Layout](#132-color-typography-and-layout)
  - [13.3 Accessibility and Interaction Testing](#133-accessibility-and-interaction-testing)
  - [13.4 Performance and Visual Quality](#134-performance-and-visual-quality)
  - [13.5 Research and Validation](#135-research-and-validation)
- [14. Research Basis & Further Reading](#14-research-basis-further-reading)
  - [14.1 Normative Standards and Specifications](#141-normative-standards-and-specifications)
  - [14.2 Browser and Performance References](#142-browser-and-performance-references)
  - [14.3 Usability and Perception Research](#143-usability-and-perception-research)
  - [14.4 Current Implementation Documentation](#144-current-implementation-documentation)
  - [14.5 Companion Reference](#145-companion-reference)

---

## 1. Executive Summary

Modern web-interface quality does not come from a single aesthetic. It comes from a **repeatable, testable decision system** that coordinates hierarchy, content, typography, color, layout, interaction, accessibility, performance, and validation.

This guide treats design rules according to their evidence level:

- **Normative requirement** — defined by a standard, law, contract, or platform rule.
- **Evidence-informed practice** — supported by research, established usability findings, or repeated product evidence.
- **Heuristic** — a useful starting point that must be validated in context.
- **Aesthetic convention** — a stylistic choice, not a usability law.

That distinction matters. A 4.5:1 text-contrast requirement is not the same kind of rule as an 8-unit spacing scale. The former is a WCAG conformance threshold; the latter is a practical convention that may be adapted when typography, platform density, localization, or component geometry requires it.

For task-heavy product and admin interfaces, the dominant risks are crowding, hidden complexity, weak state communication, inaccessible data structures, and inefficient repeated workflows. For public-facing and marketing interfaces, the dominant risks are aesthetic-first breakage, unclear value hierarchy, unsupported persuasion claims, unstable responsive composition, and visual effects that reduce readability or performance.

This document therefore provides one integrated practice reference for:

1. foundational visual and interaction principles;
2. color, typography, spacing, and responsive layout systems;
3. product/admin and marketing-site design;
4. accessibility and inclusive-design requirements;
5. design tokens and implementation contracts;
6. testing, governance, and delivery workflow.

Named visual styles, historical movements, platform design languages, and major design systems are intentionally catalogued in the companion file **`02-design-styles-systems.md`** so they are not duplicated here.

## 2. Foundational Design Theory, Gestalt & Attention

Design theory is the systematic framework that transforms aesthetic instinct into deliberate, purposeful decisions. Every pixel, every pause, every contrast ratio tells the user what to think, feel, and do next. These principles form the bedrock of every design decision — whether for a dense admin dashboard or a high-conversion landing page.

---

### 2.1 Visual Hierarchy & Attention Management

Visual hierarchy is the arrangement of interface elements to communicate relative importance and guide attention through content and actions. It helps people decide what to inspect first, what belongs together, and what can be deferred.

Visual hierarchy works through perceptual attention cues such as size, contrast, position, grouping, and motion. These cues influence what people notice first, but their effect depends on content, culture, reading direction, device, and task; they are not universal biological laws.

**How to create effective hierarchy:**

- **Size/Scale:** Larger elements often attract attention sooner. Use a defined scale and validate that the hierarchy remains clear at different viewport sizes and zoom levels.
- **Color & Contrast:** Higher contrast can increase salience. Reserve the strongest contrast for content or controls that genuinely deserve priority.
- **Weight:** Heavier weight can establish emphasis; italic is better reserved for linguistic or editorial emphasis than used as a generic hierarchy device.
- **Position:** Starting-edge and upper-page areas often receive early attention in left-to-right layouts, but reading direction, task, and established conventions matter.
- **Spacing:** More space around an element increases its perceived prominence and importance
- **Movement:** Motion is highly salient and can distract from tasks; use it only to explain change, provide feedback, or support narrative.

**Optional hierarchy heuristic:** A 60–30–10 distribution can be adapted to visual emphasis—most content at a base level, a smaller portion emphasized, and a small focal layer—but this is a composition heuristic, not a measured standard.

**Practical rule for both admin and frontend:** Each view should have:
1. A single primary focal point (headline, key metric, hero CTA)
2. A clear "next" action or section
3. Supporting content that is visually quieter

| Hierarchical Element | Perceptual Effect | Implementation Starting Point |
|:---|:---|:---|
| **Size and Scale** | Larger objects signal dominance and priority | Use a consistent typographic scale (e.g., Major Third 1.25) |
| **Color and Contrast** | High contrast isolates elements from background noise | Maintain 4.5:1 ratio for standard text (WCAG AA) |
| **Position and Flow** | Placement affects discovery and reading order | Keep priority content near likely task paths and verify with usability testing |
| **Weight** | Bold text and heavier fonts establish importance | Use 2–3 weights maximum in a systematic way |
| **Spacing** | Space establishes grouping and emphasis | Use a documented 4/8-unit token scale or another consistent scale |
| **Movement** | Motion can explain change but also interrupt attention | Reserve for meaningful feedback; respect reduced-motion preferences |

**Hierarchy levels for implementation:**

```
LEVEL 1 — Most Important
├── Primary CTAs and actions
├── Key metrics / KPIs
├── Critical alerts and notifications
└── Main navigation / current page title

LEVEL 2 — Important
├── Secondary actions
├── Section headings
├── Data visualizations
└── Cards and widgets

LEVEL 3 — Supporting
├── Body content and descriptions
├── Labels and metadata
├── Secondary information
└── Tertiary navigation

LEVEL 4 — Background
├── Timestamps and dates
├── Helper text and hints
├── Legal disclaimers
└── Decorative elements
```

> **Validation principle:** hierarchy must be evaluated in context. Use task-based usability testing, first-click testing, and—in high-traffic products—controlled experiments to verify that users notice and understand the intended priority.

---

---

### 2.2 Balance & Layout Stability

Balance is not symmetry — it is the sense that the page "settles." It provides visual equilibrium that makes a design feel stable and intentional rather than chaotic.

**Two types of balance:**

- **Symmetrical balance:** More formal, stable, corporate. Often used for admin dashboards, data-heavy layouts, and enterprise tools where predictability and consistency are paramount. Stable columns and consistent density — tables/forms don't randomly compress or expand
- **Asymmetrical balance:** More dynamic, modern, editorial. Used for marketing landing pages and creative frontends to create visual tension and guide focus toward specific elements. Achieved via larger whitespace regions and deliberate content proportions (hero vs. supporting sections)

When balance is missing, users perceive the UI as "noisy" even if individual components look polished.

---

---

### 2.3 Contrast as a Design Tool

Contrast is the visual difference between elements — in size, color, weight, shape, or texture. It operates at three levels in web design:

1. **Luminance contrast** — For readability and accessibility. Measurable via WCAG contrast ratios
2. **Size/weight contrast** — For establishing hierarchy. Larger and bolder elements dominate
3. **Shape/boundary contrast** — For interaction affordances. Distinguishing clickable from static elements

**Practical contrast applications:**
- High contrast between CTA buttons and their background
- Strong contrast for primary interactive elements vs. static content
- Selected navigation items vs. unselected
- Active states vs. default states
- Text against its background surface

> **Warning:** Same weight/color on interactive and static elements destroys affordance — users can't tell what's clickable.

---

---

### 2.4 Alignment & Grid-Based Structure

Every element should have a visual connection to something else on the page. Alignment creates order, reduces visual noise, and communicates professionalism. Consistent alignment creates rhythm and reduces cognitive load — especially critical for admin UIs where users must compare rows and columns quickly.

**Best practices:**
- Align to an invisible 8px or 12px grid
- All text, inputs, and icons should share alignment edges
- Use CSS Grid and Flexbox to enforce structural alignment
- Avoid "random pixel nudges" — misalignment of even 1–2px is perceptible to users and creates a feeling of unprofessionalism

---

---

### 2.5 Gestalt Grouping: Proximity, Similarity, Continuity and More

Gestalt principles describe recurring ways people organize visual information into groups and figures. They are useful design lenses, not deterministic laws: context, learned conventions, culture, reading direction, and assistive technology can change how a layout is understood.

| Principle | Design implication | Practical application |
|:---|:---|:---|
| **Proximity** | Nearby items are likely to be interpreted as related | Keep labels close to their fields; separate unrelated form groups with a larger gap |
| **Similarity** | Shared appearance suggests shared role | Give primary actions one consistent treatment; do not style static text like a link |
| **Common region** | A visible boundary can create a group | Use cards, fieldsets, panels, or table sections when spacing alone is insufficient |
| **Connectedness** | Explicit connections imply stronger relationships | Use lines or connectors in timelines, process diagrams, and node graphs |
| **Continuity** | The eye tends to follow aligned paths | Align headings, values, controls, and columns to stable edges |
| **Closure** | People can perceive a complete form from incomplete cues | Use carefully in icons and logos; never rely on ambiguity for critical controls |
| **Figure/ground** | Foreground must remain distinguishable from its background | Ensure overlays, dialogs, menus, and text remain legible against every underlying state |
| **Common fate** | Elements changing together are perceived as related | Coordinate motion only when it explains a shared state change |
| **Prägnanz** | People often prefer the simplest coherent interpretation | Reduce unnecessary competing shapes and styles, while preserving required cues |

**Spacing hierarchy:** a small gap communicates a strong relationship, a medium gap separates items within one section, and a large gap separates sections. Define these relationships with tokens rather than one-off values.

**Forms and data tools:**
- Place a label closer to its own control than to the previous control.
- Keep table search, filters, bulk actions, and result counts within the table's visual region.
- Use `<fieldset>` and `<legend>` for semantic grouping when a border or heading alone would not communicate the relationship to assistive technology.

---

### 2.6 Repetition, Rhythm & Consistency

Repeating visual elements throughout a design — fonts, colors, shapes, spacing values — builds unity and brand cohesion. Inconsistency breaks trust; repetition builds it.

**What to repeat consistently:**
- Button styles (same padding, border-radius, font)
- Card padding and internal spacing
- Spacing values drawn from the documented scale, with intentional exceptions
- Semantic color roles that keep the same meaning across components and modes
- A coherent icon system; intentional filled/outline state variants are documented
- Border radius values

This is especially important in admin templates where many similar screens (lists, forms, dashboards) must feel coherent. Users who spend hours daily in your admin interface build muscle memory — inconsistency taxes that muscle memory and reduces efficiency.

---

---

### 2.7 Whitespace (Negative Space)

Whitespace is not "empty" — it is "active space" that reduces cognitive load, improves comprehension, and communicates quality. Whitespace can improve grouping, scanability, and perceived quality when it supports the content hierarchy; the appropriate amount is task- and context-dependent.

**Two categories of whitespace:**

| Type | Definition | Examples |
|:---|:---|:---|
| **Macro whitespace** | Large areas of space between major elements | Page margins, section gaps, hero padding, space between card groups |
| **Micro whitespace** | Small spaces within and between individual elements | Line height, paragraph spacing, button padding, space between icon and label |

**Application by context:**
- **Admin templates:** Compressed whitespace but still consistent. Use more micro whitespace inside tables/cells than macro whitespace between major sections. A thoughtful admin sidebar might use 4px–8px increments to maximize visible navigation items without compromising scannability
- **Marketing/Frontend sites:** Generous macro whitespace (big margins, large section gaps, spacious hero padding). A marketing page might use 80px of margin to create a sense of luxury and breathing room
- **Contextual rule:** Use a consistent token scale and make the gap between unrelated groups visibly larger than the gap between related items. Dense admin screens may use smaller values than marketing pages; there is no universal card or section spacing minimum.

---

---

### 2.8 Emphasis & Focal Points

Emphasis is about creating a single clear focal point on each view. Without a focal point, users experience "decision paralysis" — everything competes equally and nothing wins.

**Where to place emphasis:**
- **Admin dashboards:** A main KPI or chart at the top, or a highlighted "Needs attention" metric
- **Landing pages:** Hero headline + primary CTA
- **Forms:** The submit/save button should be the most prominent element
- **Tables:** The most important column (e.g., status, name) should have the strongest visual treatment

---

---

### 2.9 Proportion Heuristics: Golden Ratio & Rule of Thirds

**The Golden Ratio (approximately 1:1.618)** is an optional proportioning heuristic used in art and design. It can help generate coherent ratios, but it is not inherently or universally more pleasing than other well-structured proportions. In web design, it may guide:
- Layout proportions (e.g., a 960px page width split into 593px content + 367px sidebar)
- Font size scales (each step roughly 1.618× the previous, though most practical scales use smaller ratios)
- Spatial relationships between elements

**The Rule of Thirds** divides your canvas into a 3×3 grid. Placing focal elements along these grid lines — especially at the four intersections — creates visually engaging, naturally balanced compositions. This is particularly powerful for hero sections and featured image placement.

---

---

### 2.10 Decision and Interaction Heuristics

These cognitive principles from UX studies directly shape design decisions:

| Law | Principle | Application |
|:---|:---|:---|
| **Hick's Law** | Decision time increases with the number and complexity of choices | Reduce choices: filter options on product-heavy sites, limit navigation items, use progressive disclosure in admin UI |
| **Fitts's Law** | Time to reach a target is a function of distance and size; closer/larger targets are faster | Make frequent targets larger and closer to likely cursor positions. Enlarge CTAs, put primary actions in easily reachable zones |
| **Occam's Razor** | Prefer the least complex solution that fully satisfies the requirements | Remove nonessential controls and decoration, but do not remove information or affordances users need |

---

---

### 2.11 Scanning and Reading Patterns

Eye-tracking research does not support one universal path for every page. Nielsen Norman Group describes several recurring text-scanning behaviors, including the **F-pattern**, **layer-cake pattern**, **spotted pattern**, and **commitment pattern**. The pattern that appears depends on the user's goal, page structure, content quality, familiarity, and motivation.

| Pattern | Typical behavior | Design response |
|:---|:---|:---|
| **F-pattern** | Broad scan near the top, shorter scans lower down, then a vertical scan along the starting edge | Front-load headings and key words; improve subheadings and paragraph openings rather than deliberately designing an F-shaped page |
| **Layer-cake** | Users scan headings and subheadings, then selectively read sections | Use descriptive headings, clear hierarchy, and meaningful section labels |
| **Spotted** | Users search for visually distinctive words, numbers, links, or shapes | Make key facts easy to locate without turning every phrase into a visual accent |
| **Commitment** | Users read most or all content carefully | Support sustained reading with clear language, comfortable measure, and stable typography |

The often-cited **Z-pattern** is better understood as a composition heuristic for simple, sparse layouts—not as a universal eye-tracking law. It can help distribute a logo, navigation, focal content, and action across a simple frame, but the actual path must be validated with task testing.

**Reading-direction rule:** do not assume “top-left first” for every language. Source order, alignment, and emphasis must adapt to the writing system and localization.

## 3. Color Theory & Semantic Color Systems

Color in web design is a high-bandwidth communication channel that conveys brand personality, emotional tone, and functional status long before the user reads a single word. It has two overlapping jobs: (1) **aesthetics and brand meaning**, and (2) **functional signaling** (states, emphasis, affordances) that must remain visible and accessible across multiple modes and under different forms of color perception.

### 3.1 Color Fundamentals: Hue, Chroma/Saturation, Lightness and Value

Newton’s prism experiments helped establish the visible spectrum and inspired later circular color arrangements. Modern UI color work, however, must distinguish between artistic color wheels, additive screen color, perceptual color spaces, and accessibility contrast.

The color wheel organizes colors into three categories:
- **RYB:** A traditional artist-oriented mixing model; useful historically but not a precise model of display color.
- **RGB:** The additive model used by displays. Equal channel values create neutrals; full red, green, and blue combine toward white.
- **Color-space note:** “Primary,” “secondary,” and “tertiary” relationships vary by model, so name the model when teaching or generating palettes.

**Core color properties:**

| Property | Definition | Design Impact |
|:---|:---|:---|
| **Hue** | The pure color — position on the color wheel (0°–360°). Red=0°, Yellow=60°, Green=120°, Cyan=180°, Blue=240°, Magenta=300° | Determines the fundamental character of the color |
| **Saturation** | Color intensity/purity (0–100%). 100% = vivid, pure. 0% = gray | Lower saturation for backgrounds and supporting elements; higher for CTAs and accents |
| **Brightness/Value** | Lightness of the color (0–100%). 0% = black, 100% = full color | Use brightness shifts to create shade/tint scales for design system tokens |
| **Tint** | Hue + white (lighter versions) | Backgrounds, subtle highlights, hover states |
| **Shade** | Hue + black (darker versions) | Active states, pressed states, dark mode accents |
| **Tone** | Hue + gray (muted versions) | Sophisticated, less aggressive color choices for professional UIs |

### 3.2 Color Models for the Web: RGB, HSL, HSB, LAB/LCH, OKLCH

Understanding different color models helps you choose the right one for different tasks:

| Model | Description | Best For |
|:---|:---|:---|
| **RGB** | Additive model (Red, Green, Blue). Native to screens. Hex (#2563EB), rgb(37,99,235) | Technical color definitions, CSS values, exact specification |
| **HSL** | Hue, Saturation, Lightness — intuitive for manual adjustment but not perceptually uniform | Simple authoring and legacy workflows; equal HSL lightness values can appear very different across hues |
| **HSB/HSV** | Hue, Saturation, Brightness — used in design tools (Figma, Sketch) | Design-tool color picking, adjusting colors visually |
| **LAB / LCH** | Perceptually uniform models | Accessible color generation, smooth gradients, programmatic palette creation |
| **OKLCH** | Updated perceptually uniform model, increasingly available in CSS | Modern CSS color manipulation, creating consistent contrast steps and smooth neutral ramps |

**Practical recommendation:** HSL remains convenient for manual authoring, but it does not preserve perceived lightness across hues. For programmatic palette generation, interpolation, and theme systems, OKLCH is usually a better starting space; always gamut-map and verify final sRGB/P3 output and contrast.

### 3.3 Color Harmony Systems

Color harmony is achieved by selecting colors whose relationships follow predictable, perceptually pleasing patterns on the color wheel. In web UI (especially admin), harmony rules are best treated as "seed ideas," then reshaped into a **semantic palette** mapped to functional roles.

| Harmony Type | Description | Color Count | Web UI Application |
|:---|:---|:---:|:---|
| **Monochromatic** | Single hue in varying shades, tints, and tones | 1 hue | Sophisticated unity, strong brand recall. Easiest to get right; hardest to make interesting. Great for minimalist portfolios and SaaS |
| **Analogous** | 3–5 colors adjacent on the wheel | 3–5 | Naturally harmonious, serene, cohesive feel. Choose one dominant, one supporting, one accent. Great for nature/wellness brands |
| **Complementary** | Two colors directly opposite on the wheel | 2 | Maximum contrast and vibrant energy. Use 70% dominant / 30% accent to avoid visual chaos. High-conversion CTAs |
| **Split-Complementary** | Base color + two colors on either side of its complement | 3 | High contrast but less tension than pure complementary. More flexible and forgiving for web UI |
| **Triadic** | Three colors evenly spaced (120° apart) | 3 | Vibrant and balanced. Let one color dominate heavily. Extremely difficult to balance — use sparingly |
| **Tetradic / Square** | Four colors forming a rectangle on the wheel | 4 | Very rich but complex to manage. Keep saturation/value consistent. Better for illustration than minimal UI |

> **Practical guidance:** Start with a small functional palette, then expand only when additional semantic or brand roles require it. Harmony models are starting points, not usability guarantees.

### 3.4 Color Psychology & Emotional Associations

Colors can influence attention and learned associations, but their meaning is contextual rather than universal. However, it is important to note that **context and culture matter greatly** — there is little robust, universal evidence that any single color has the same effect on everyone.

| Color | Emotional Associations | Strategic Web Applications |
|:---|:---|:---|
| **Red** | Urgency, passion, danger, energy, power | CTAs, sales badges, error states, alerts, food brands, "Delete" buttons |
| **Orange** | Enthusiasm, creativity, warmth, affordability | Startups, retail, entertainment, secondary CTAs, notifications |
| **Yellow** | Optimism, clarity, attention, caution | Warnings, children's sites, hospitality, pending states, low-priority alerts |
| **Green** | Growth, health, nature, safety, money, success | Success states, "Save" buttons, finance, health apps, active/positive states |
| **Blue** | Trust, calm, professionalism, reliability, stability | Tech companies, banking, healthcare, B2B, navigation, links, primary branding |
| **Purple** | Luxury, wisdom, creativity, mystery | Beauty brands, premium products, spirituality, creative industries |
| **Pink** | Playfulness, romance, femininity, care | Fashion, beauty, lifestyle, youth brands |
| **Black** | Sophistication, luxury, authority, mystery | Luxury brands, high fashion, SaaS dark mode, photography |
| **White** | Purity, cleanliness, simplicity, space | Backgrounds, breathing room, minimalist design, medical |
| **Gray** | Sophistication, order, balance, neutrality | Backgrounds, secondary text, layout borders, disabled states |

### 3.5 Cultural Context & Color Meaning

> ⚠️ **Critical consideration:** Color meanings vary dramatically across cultures. White signifies purity in Western cultures but mourning in parts of Asia. Red means luck and prosperity in China but danger in Western UX. Green can represent nature globally but also represents Islam in Middle Eastern contexts. **Always validate color choices against your primary user's cultural background before finalizing a palette.**

### 3.6 The 60-30-10 Rule

A widely used composition heuristic for distributing color is:

- **60% — Dominant/Neutral color:** Backgrounds, large surfaces, body areas. Creates the overall tone and feel
- **30% — Secondary color:** Sidebars, cards, secondary text, supporting surfaces. Provides visual interest
- **10% — Accent color:** CTAs, highlights, interactive elements, links, critical alerts. Creates focal points and drives action

In admin templates and frontend UIs, this ratio prevents visual fatigue while maintaining brand presence and functional clarity.

### 3.7 Building a Semantic UI Color System

A modern UI color system separates raw colors from their functional meaning. all authoritative sources converge on a layered token architecture:

**Layer 1 — Primitives (Raw Values)**
```
PRIMARY COLOR (Brand)
├── Primary-50   (lightest tint, backgrounds)
├── Primary-100  (light tint, hover backgrounds)
├── Primary-200  (light, borders)
├── Primary-300  (medium-light)
├── Primary-400  (medium)
├── Primary-500  (base, the "primary color")
├── Primary-600  (hover state)
├── Primary-700  (active/pressed state)
├── Primary-800  (dark)
└── Primary-900  (darkest shade, text on light)

NEUTRAL COLORS (Grays)
├── White / Off-White (#FFFFFF, #F8F9FA)
├── Light Gray (#E9ECEF, #DEE2E6)
├── Medium Gray (#ADB5BD, #6C757D)
├── Dark Gray (#495057, #343A40)
└── Black / Near Black (#212529, #000000)
```

**Layer 2 — Semantic Tokens (Meaning)**
```
SEMANTIC COLORS (Functional Meaning)
├── color-primary      → Brand identity, primary actions
├── color-secondary    → Supporting brand, secondary actions
├── color-success      → Positive states, confirmations (#28A745 / #15803D)
├── color-warning      → Caution states, pending (#FFC107 / #FBBF24)
├── color-danger/error → Error states, destructive actions (#DC3545 / #DC2626)
├── color-info         → Informational states, neutral alerts (#17A2B8 / #0E7490)
└── color-link         → Hyperlinks, navigation (#007BFF / #2563EB)
```

**Layer 3 — Component Tokens (Specific Use)**
```
COMPONENT-LEVEL TOKENS
├── button.primary.bg        → var(--color-primary)
├── button.primary.text      → var(--color-on-primary)
├── table.row.height         → 44px (touch) / 36px (dense)
├── card.padding             → var(--space-6)
├── input.border             → var(--color-border)
└── input.border-focus       → var(--color-primary)
```

### 3.8 Complete Light & Dark Palette with Measured Contrast Ratios

The following palettes are worked examples for typical UI roles. They are not universal brand palettes. Contrast ratios were recalculated using the WCAG 2 relative-luminance formula; every real component must still be tested in its actual state and background.

#### Light Palette

| Token | Hex | Purpose |
|:---|:---|:---|
| `bg` | `#FFFFFF` | Page background |
| `surface` | `#F8FAFC` | Card/panel background |
| `text` | `#0F172A` | Primary body text |
| `textMuted` | `#334155` | Secondary/muted text |
| `borderStrong` | `#64748B` | Visible borders, input outlines |
| `borderLight` | `#E0E4EA` | Subtle dividers, card borders |
| `primary` / `onPrimary` | `#2563EB` / `#FFFFFF` | Primary actions, links |
| `success` / `onSuccess` | `#15803D` / `#FFFFFF` | Positive states |
| `warning` / `onWarning` | `#FBBF24` / `#0F172A` | Warning states (dark text on yellow!) |
| `danger` / `onDanger` | `#DC2626` / `#FFFFFF` | Error/destructive states |
| `info` / `onInfo` | `#0E7490` / `#FFFFFF` | Informational states |
| `focusRing` | `#6366F1` | Keyboard focus indicator |

#### Dark Palette

| Token | Hex | Purpose |
|:---|:---|:---|
| `bg` | `#0B1220` | Page background |
| `surface` | `#111827` | Card/panel background |
| `text` | `#F9FAFB` | Primary body text |
| `textMuted` | `#CBD5E1` | Secondary/muted text |
| `borderStrong` | `#64748B` | Visible borders |
| `borderLight` | `#1F2937` | Subtle dividers |
| `primary` / `onPrimary` | `#60A5FA` / `#0B1220` | Primary actions (desaturated for dark bg) |
| `success` / `onSuccess` | `#4ADE80` / `#0B1220` | Positive states |
| `warning` / `onWarning` | `#FBBF24` / `#0B1220` | Warning states |
| `danger` / `onDanger` | `#F87171` / `#0B1220` | Error/destructive states |
| `info` / `onInfo` | `#22D3EE` / `#0B1220` | Informational states |
| `focusRing` | `#A5B4FC` | Keyboard focus indicator |

#### Contrast Ratio Verification

WCAG-informed targets: **≥ 4.5:1 for normal text (AA)**; **≥ 3:1 for large text and non-text UI boundaries**.

| Pairing | Light Ratio | Dark Ratio | Passes AA? |
|:---|---:|---:|:---:|
| Primary text on background | 17.85:1 | 17.92:1 | ✅ |
| Muted text on background | 10.35:1 | 12.61:1 | ✅ |
| Link/primary on background | 5.17:1 | 7.36:1 | ✅ |
| Primary button text on primary | 5.17:1 | 7.36:1 | ✅ |
| Success button text on success | 5.02:1 | 10.74:1 | ✅ |
| Warning badge text on warning | 10.69:1 | 11.22:1 | ✅ |
| Danger button text on danger | 4.83:1 | 6.77:1 | ✅ |
| Info button text on info | 5.36:1 | 10.36:1 | ✅ |
| Focus ring vs background (non-text) | 4.47:1 | 9.39:1 | ✅ |
| Input border vs surface (non-text) | 4.55:1 | 3.73:1 | ✅ |

### 3.9 Generating Palettes: A Repeatable Token-Based Method

A repeatable palette method that scales across products:

1. **Define primitives** — Create a neutral gray ramp (10 steps from near-white to near-black) and a small set of brand hue ramps (primary, plus 1–2 secondary hues, each with 10 steps)
2. **Define semantic roles** — Map primary/success/warning/danger/info to specific steps in your primitive ramps. Each role gets a base shade, a text-on shade, a light background shade, and a dark variant
3. **Define theme modes** — Light and dark themes change which primitive steps are used for each role, not the roles themselves. This means adding new themes (high-contrast, brand variant) is a configuration change, not a redesign

### 3.10 Dark Mode Design Best Practices

Dark mode is common and may be valuable when the product, platform, or audience expects it, but it is not mandatory for every interface. It must be designed as a separate appearance rather than produced by simple inversion.

**Critical dark mode rules (established through industry best practices):**
- **Dark ≠ Black:** Use dark grays (#0B1220, #111827, #1A1D24) instead of pure black (#000000) to maintain a sense of depth and avoid "OLED halo" effects
- **Re-tune accent colors:** Evaluate chroma and lightness on dark surfaces. Some accents need reduced chroma; others need higher lightness. Do not apply a fixed percentage mechanically.
- **Shadows lose impact:** In dark mode, shadows are less visible. Use subtle borders and background-color elevation instead of shadow elevation
- **Text colors:** Prefer explicit, tested text tokens rather than arbitrary white opacity. Very high contrast can feel harsh for some users, but lowering contrast must never compromise readability.
- **Layer with backgrounds:** Create depth through progressively lighter dark backgrounds (e.g., bg → surface → elevated surface: #0B1220 → #111827 → #1F2937)
- **Test independently:** Dark mode is a separate design that must be tested independently for contrast, readability, and visual hierarchy


### 3.10.1 Gamut, Forced Colors and Real-World Validation

A color token is not complete until its rendering context is known.

- **sRGB remains the safest baseline.** Display-P3 can provide richer colors on capable displays, but include an sRGB fallback and avoid relying on out-of-gamut differences to communicate meaning.
- **Perceptual uniformity is approximate.** OKLCH improves palette authoring, but equal lightness does not automatically guarantee WCAG contrast or identical perceived prominence.
- **Forced-colors mode can replace authored colors.** Test semantic states with `forced-colors: active`; do not disable system adaptation unless a specific component truly requires it.
- **Transparency changes the effective color.** Test text, icons, focus indicators, and borders against every background they can overlap.
- **Charts need redundant encoding.** Combine color with labels, direct annotation, symbols, line styles, or patterns.


### 3.11 Current Directional Trends (Non-Normative)

These are observed directions rather than standards or guaranteed forecasts:
- **Natural, muted tones** and soft pastels replacing bright neons
- **Smooth, subtle gradients** for modern depth perception
- **Dark and alternative appearance modes** where user context and platform expectations justify them
- **Warm vs. cool colors** strategically deployed for emotional engagement
- **OKLCH and LCH** color spaces gaining adoption in CSS for perceptually uniform palette generation
- **Reduced color** — fewer colors used more intentionally, with meaning attached to each

---

## 4. Typography Systems, Readability & Font Performance

### 4.1 Typography as a Primary Interface Material

Typography is one of the primary materials of interface design because labels, instructions, navigation, data, and long-form content are largely textual. The goal of good typography is **invisibility** — type should guide without being noticed, communicate without demanding attention. Every typographic choice from scale to kerning shapes reading experience, brand perception, and cognitive load.

A robust typographic system must produce hierarchy, remain readable under user overrides (WCAG SC 1.4.12), and behave well under font loading and performance constraints.

### 4.2 Typeface Classification & Selection

| Category | Characteristics | Best For | Example Fonts |
|:---|:---|:---|:---|
| **Serif** | Small strokes (serifs) at letterform endings. Tradition, authority, credibility, editorial gravitas | Newspapers, luxury brands, editorial, long-form reading, headings | Playfair Display, Georgia, Merriweather, Garamond, Lora |
| **Sans-Serif** | Clean, strokeless letterforms. Modernity, clarity, approachability | Tech, UI, body copy on screens, admin dashboards, any digital interface | Inter, Roboto, DM Sans, Open Sans, Nunito, Plus Jakarta Sans, Outfit |
| **Monospace** | Each character occupies identical horizontal space. Precision, technical depth | Code blocks, data tables (numeric alignment), terminal UIs, badges, IDs | DM Mono, JetBrains Mono, Fira Code, Source Code Pro |
| **Display / Expressive** | Highly stylized, designed for large sizes only. Personality, brand distinctiveness | Headlines, hero text, logos. NEVER use for body text | Fraunces, Syne, Unbounded, Clash Display |
| **System Fonts** | Pre-installed on user's OS. Zero loading cost, native feel | Performance-critical applications, admin UIs where brand fonts aren't needed | system-ui, -apple-system, Segoe UI, Roboto (Android) |

**Selection criteria for UI typefaces:**
- **x-height:** Larger x-height = more legible at small sizes (critical for admin UIs)
- **Open apertures:** Letters like 'a', 'e', 'c' should have open counters for screen legibility
- **Distinguishable characters:** The letters 'i', 'l', '1' and 'O', '0' must be clearly distinct
- **Character set support:** Ensure the font covers all languages and character sets you need
- **Variable font availability:** Variable fonts can reduce request count and support continuous axes, but they are not automatically smaller than a carefully subset static-font set

### 4.3 Modular Type Scales

A **type scale** is a documented progression of text sizes. A mathematical ratio can provide a starting point, but optical adjustment is often necessary because display size, x-height, language, density, and component constraints do not scale uniformly.

**Common scale ratios and their character:**

| Scale Ratio | Value | Character | Possible Context |
|:---|:---:|:---|:---|
| **Minor Second** | 1.067 | Extremely subtle hierarchy | Dense data-heavy admin UIs |
| **Major Second** | 1.125 | Subtle, gentle progression | Admin tools, tight interfaces |
| **Minor Third** | 1.200 | Balanced, restrained | Dense admin tools, technical documentation |
| **Major Third** | 1.250 | Standard, versatile | General web content, most applications |
| **Perfect Fourth** | 1.333 | Clear distinction between levels | Marketing sites, editorial |
| **Augmented Fourth** | 1.414 | Dynamic, high-impact | Marketing, landing pages, hero-first design |
| **Golden Ratio** | 1.618 | Dramatic, but can skip too much | Display-heavy designs, very few heading levels |

**Worked type-scale example (root 16px, approximately Major Third):**

| Role | rem | px | Typical Use | Line Height |
|:---|---:|---:|:---|:---:|
| `text-xs` / Caption | 0.75 | 12 | Overlines, tags, labels, badges (use sparingly). Use UPPERCASE + letter-spacing | 1.4 |
| `text-sm` / Small | 0.875 | 14 | Dense UI text, captions, table data, metadata, helper text | 1.4–1.5 |
| `text-base` / Body | 1.0 | 16 | Default UI text, form inputs, body copy | 1.5–1.6 |
| `text-lg` / Body Large | 1.125 | 18 | Lead paragraphs, section introductions, emphasized body | 1.5–1.7 |
| `text-xl` / H4 | 1.25 | 20 | Sub-section headings, page titles in compact layouts | 1.3–1.4 |
| `text-2xl` / H3 | 1.5–1.563 | 24–25 | Section headings, card group titles | 1.3–1.4 |
| `text-3xl` / H2 | 1.875–1.953 | 30–31 | Major section headings | 1.2–1.3 |
| `text-4xl` / H1 | 2.25–2.441 | 36–39 | Page titles | 1.1–1.2 |
| `text-5xl` / Display | 3.0–3.815 | 48–61 | Hero headlines, marketing display | 1.0–1.1 |

**CSS implementation:**

```css
/* Modern Type Scale (Major Third 1.25 ratio) */
:root {
  --text-xs: 0.75rem;     /* 12px */
  --text-sm: 0.875rem;    /* 14px */
  --text-base: 1rem;      /* 16px */
  --text-lg: 1.25rem;     /* 20px */
  --text-xl: 1.563rem;    /* 25px */
  --text-2xl: 1.953rem;   /* 31px */
  --text-3xl: 2.441rem;   /* 39px */
  --text-4xl: 3.052rem;   /* 49px */
  --text-5xl: 3.815rem;   /* 61px */
}
```

### 4.4 Line Height (Leading)

Line height is the vertical distance between baselines. Larger display text often works with tighter leading, while long-form text usually needs more. These ranges are starting points, not WCAG requirements.

| Text Type | Line Height | Rationale |
|:---|:---:|:---|
| **Body text** | Commonly 1.45–1.7 | Tune for typeface, measure, language, and density; WCAG does not prescribe a default line-height value |
| **Large body / Lead text** | 1.4–1.6 | Slightly tighter as size increases |
| **Headings (H3–H1)** | 1.1–1.3 | Larger glyphs require less vertical separation. Tight line height keeps multi-line headings cohesive |
| **Display text (Hero)** | 1.0–1.1 | Very tight for dramatic visual impact |
| **UI labels / Buttons** | 1.0–1.2 | Single-line elements need minimal leading |
| **Small text / Captions** | 1.4–1.5 | Maintain readability at reduced sizes |

**CSS line height tokens:**
```css
:root {
  --leading-tight: 1.1;     /* Headings, display */
  --leading-snug: 1.375;    /* Sub-headings */
  --leading-normal: 1.5;    /* Body text minimum */
  --leading-relaxed: 1.7;   /* Comfortable body reading */
  --leading-loose: 2;       /* Spacious, editorial */
}
```

### 4.5 Letter Spacing (Tracking) & Kerning

**Letter spacing (tracking):** Uniform spacing between ALL characters in a text block.
- **Tighten slightly for large headings:** −0.02em to −0.04em (large text has natural optical spacing that reads as too loose)
- **Expand for uppercase and small text:** +0.05em to +0.2em (uppercase lacks ascenders/descenders, so needs extra spacing for legibility)
- **Body text:** Leave at normal (0) or near-normal

**Kerning:** Spacing between two SPECIFIC characters. Most modern fonts handle this automatically via OpenType kerning pairs. Watch for awkward gaps in display type — especially in AV, Ty, WA, and To combinations at large sizes.

### 4.6 Line Length (Measure)

A useful starting range for sustained body reading is roughly **45–75 characters per line**. Around **60–70 characters** often works well, but typeface, language, font size, and reading context should determine the final measure. This is one of the most impactful and easiest readability improvements you can make.

- **Too long (>75ch):** Reader loses their place when returning to the next line ("regression"). Common on wide-screen layouts without max-width constraints
- **Too short (<45ch):** Fatiguing eye jumps and disrupted reading rhythm. Breaks flow
- **Implementation:** Use `max-width: 65ch` on content containers and center them. Allow background sections (heroes, full-width imagery) to remain fluid

### 4.7 Font Weight Strategy

Use as few weights as the hierarchy needs. Two or three are often enough, but complex editorial or data products may need more when roles remain consistent:

| Weight | Value | Role |
|:---|:---:|:---|
| **Light** | 300 | Captions, subtle text, decorative use |
| **Regular** | 400 | Body text, default UI text |
| **Medium** | 500 | Labels, emphasis within body |
| **Semibold** | 600 | Sub-headings, table headers, important labels |
| **Bold** | 700 | Headings, strong emphasis, primary actions |

Variable fonts can expose continuous weight and other axes in one font resource, but file size depends on the font and subset; compare the real transfer size with static alternatives.

### 4.8 Font Pairing Principles

Combine a distinctive display/heading font with a neutral, readable body font. Create contrast in **category** (serif + sans-serif) but harmony in **mood**.

**Common pairing patterns:**
- **Sans-serif body + sans-serif heading** (same family or different weights) — Clean, modern, utilitarian. Best for admin UIs
- **Sans-serif body + serif heading** — Editorial, sophisticated, distinctive. Best for marketing/content sites
- **Sans-serif body + display heading** — Bold personality. Best for brand-forward landing pages

**Rules:**
- Limit to **2 typefaces maximum** (some reports allow 3, but 2 is safer)
- Use different weights and sizes to differentiate, not just different fonts
- Avoid pairing fonts with similar personalities — the contrast IS the point
- Ensure both fonts have matching x-heights for visual harmony in mixed content

### 4.9 Tabular/Monospaced Numerals for Data

For administrative interfaces and data-heavy tables, **tabular numerals** are a functional necessity. In proportional fonts, the digit "1" is narrower than "9", causing columns of numbers to misalign and making visual comparison difficult.

Tabular numerals ensure every digit occupies the same horizontal space, allowing users to scan columns of currency, counts, or IDs and immediately perceive magnitudes based on decimal alignment.

```css
/* Enable tabular numerals for data tables */
.data-table td.numeric {
  font-variant-numeric: tabular-nums;
  text-align: right;
}
```

### 4.10 Font Loading & Performance

**System UI fonts** reduce loading cost and provide excellent platform-native legibility:
```css
:root {
  --font-sans: system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
}
```

**When brand requires custom fonts, manage:**
- **Discovery/loading:** Use `@font-face` with self-hosted `woff2` files for best performance
- **Render behavior:** Use `font-display: swap` to avoid invisible text (FOIT). Accept a brief flash of unstyled text (FOUT) as the better tradeoff
- **Layout stability:** Use `size-adjust` or font metric matching to reduce Cumulative Layout Shift (CLS) when the web font loads and swaps
- **Subsetting:** Remove unused character ranges to reduce file size dramatically
- **Preloading:** Preload only fonts that are genuinely critical to the initial render; excessive font preloads compete with images, CSS, and other high-priority resources

```css
/* Resilient font stack with safe loading */
@font-face {
  font-family: "BrandSans";
  src: url("/fonts/brand-sans.woff2") format("woff2");
  font-weight: 100 900; /* variable font axis */
  font-style: normal;
  font-display: swap;
}

html {
  font-family: "BrandSans", var(--font-sans);
  line-height: 1.5;
}
```

### 4.11 Fluid Typography with clamp()

Modern CSS `clamp()` creates typography that scales smoothly between viewport sizes without media query breakpoints:

```css
:root {
  /* clamp(minimum, preferred, maximum) */
  --text-h1: clamp(1.8rem, 4vw + 1rem, 4rem);
  --text-h2: clamp(1.4rem, 3vw + 0.8rem, 2.5rem);
  --text-body: clamp(0.875rem, 0.5vw + 0.75rem, 1rem);
}

h1 {
  font-size: var(--text-h1);
  font-family: var(--font-display);
  line-height: var(--leading-tight);
  letter-spacing: -0.03em;
}
```

### 4.12 Contextual Typography Decisions

Administrative and marketing typography require different density and hierarchy ranges; the context-specific guidance is kept in their respective chapters.

---

### 4.13 Font Metrics, Internationalization and Resilience

A typography system must survive more than the default English mockup.

- Test long translations, right-to-left scripts, CJK text, Devanagari and any scripts in the product scope.
- Avoid fixed-height text containers; allow wrapping and vertical growth.
- Use `size-adjust`, `ascent-override`, `descent-override`, and `line-gap-override` only after measuring fallback and web-font metrics.
- Preserve user zoom and text resizing; do not use viewport units alone for body text.
- Use `font-synthesis: none` only when the required real styles are loaded, otherwise users may lose meaningful bold or italic distinctions.
- Check numerals, currency symbols, diacritics, punctuation, and mixed-script fallback before approving a font family.
- For data, use `font-variant-numeric` features intentionally: `tabular-nums` for aligned columns, `slashed-zero` where identifiers need disambiguation, and proportional figures for prose.

## 5. Spacing, Grids, Responsive Layout & Reflow

A robust layout system solves a recurring problem: **how to scale complexity without losing clarity**. Spacing is the grammar of design — it tells the eye which elements belong together, establishes rhythm, creates breathing room, and communicates hierarchy before any content is read.

### 5.1 Spacing Grids: 4-Unit and 8-Unit Systems

A 4- or 8-unit spacing grid is a common design-system convention because it limits arbitrary values and creates repeatable rhythm. The purpose is consistency—not literal adherence to every multiple for every property. Typography, one-pixel borders, optical alignment, and platform-native control sizes may require exceptions.

**Why 8 specifically?**
- Provides a manageable vocabulary of spacing decisions
- Maps cleanly to many component and layout systems
- Supports density variants by shifting semantic tokens to smaller or larger primitive steps

**Two implementation approaches:**
- **Hard Grid:** Snap all content to a document-wide 8px grid (more rigid, more precise)
- **Soft Grid (recommended for web):** Focus on 8px increments between individual elements. More accurately reflects CSS box model behavior with Flexbox and Grid

**For tighter admin UIs:** A 4-unit base can provide half-steps while preserving a coherent scale. Do not reduce interactive target size merely to satisfy density.

### 5.2 Spacing Scale & Token System

A worked, code-friendly spacing scale that supports comfortable marketing layouts and denser application interfaces:

| Token | px | rem | Typical Use |
|:---|---:|---:|:---|
| `space-0` | 0 | 0 | Reset, flush alignment |
| `space-1` | 4 | 0.25 | Micro — icon gaps, badge padding, compact table cell padding, border-radius adjustments |
| `space-2` | 8 | 0.5 | XSmall — inline element gaps, chip padding, tight lists, label-to-input gap |
| `space-3` | 12 | 0.75 | Small — dense card padding, label-to-input in compact forms |
| `space-4` | 16 | 1.0 | Base — default padding unit, list item gaps, form row gaps, gutter width |
| `space-5` | 20 | 1.25 | Between — KPI card padding, small section gaps |
| `space-6` | 24 | 1.5 | Medium — card padding, between form groups, sidebar section spacing, dashboard card gaps |
| `space-8` | 32 | 2.0 | Large — between sections within a card, between card rows |
| `space-10` | 40 | 2.5 | XLarge — major content group spacing |
| `space-12` | 48 | 3.0 | 2XL — between content sections, hero internal padding |
| `space-16` | 64 | 4.0 | 3XL — major section separation, page-level vertical padding |
| `space-20` | 80 | 5.0 | 4XL — large layout separation (frontend) |
| `space-24` | 96 | 6.0 | 5XL — between page sections, scroll-reveal breathing room |
| `space-32` | 128 | 8.0 | 6XL — hero height, full-page section blocks, landing page blocks |

**CSS implementation:**
```css
:root {
  --space-1: 4px;    --space-2: 8px;
  --space-3: 12px;   --space-4: 16px;
  --space-6: 24px;   --space-8: 32px;
  --space-10: 40px;  --space-12: 48px;
  --space-16: 64px;  --space-20: 80px;
  --space-24: 96px;  --space-32: 128px;
}

/* Component spacing examples */
.card { padding: var(--space-6); }                 /* 24px */
.card + .card { margin-top: var(--space-4); }      /* 16px */
.section { padding-block: var(--space-24); }       /* 96px top/bottom */
.form-group + .form-group { margin-top: var(--space-6); }
.label { margin-bottom: var(--space-2); }          /* 8px */
```

### 5.3 Macro vs. Micro Whitespace

| Type | Scale | Examples |
|:---|:---|:---|
| **Micro whitespace** | 4–16px | Line height, paragraph spacing, button padding, icon-to-label gap, input internal padding |
| **Macro whitespace** | 24–128px | Page margins, section gaps, hero padding, space between card groups, column gutters |

**Admin templates:** Use more micro whitespace inside tables/cells while keeping macro whitespace moderate. Favor 4px base for dense tables and forms, 8px for overall layout.

**Marketing/Frontend:** Generous macro whitespace. Use 8px base with larger steps (32, 48, 64, 96px) to create "breathing room."

### 5.4 The Internal ≤ External Rule

A useful proximity heuristic is: **space between unrelated groups should usually be greater than space inside a related group**. This is not an absolute mathematical rule; card padding can legitimately exceed a compact grid gap. This is a direct application of Gestalt proximity — it ensures related items stay grouped together while distinct sections are clearly separated.

**Example:**
- Related controls might use an 8px gap while separate groups use 24px.
- A card may use 24px internal padding and a 16px grid gap when density requires it; grouping must remain perceptually clear.
- Validate the relationship with real content rather than enforcing a universal padding-to-gap equation.

### 5.5 Grid Systems: 12-Column & CSS Grid

**12-Column Grid (Template-Driven):**
The classic approach for responsive layouts. 12 columns allow easy division into halves (6+6), thirds (4+4+4), quarters (3+3+3+3), and asymmetric splits (8+4, 9+3).

Key parameters:
- **Columns:** 12 (standard), with gutters between them
- **Gutters:** 16–24px between columns (fixed within breakpoint ranges)
- **Margins:** Page-edge spacing that prevents content from touching viewport edges
- **Container:** Max-width wrapper that centers content

**CSS Grid (Content-Driven):**
For card layouts, dashboard panels, and responsive compositions:
```css
/* Auto-responsive grid without breakpoints */
.card-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: var(--space-6); /* 24px */
}

/* Fixed admin dashboard layout */
.dashboard {
  display: grid;
  grid-template-columns: 250px 1fr;
  grid-template-rows: 56px 1fr;
  min-height: 100vh;
}
```

### 5.6 Breakpoints & Container Widths

The following values are example starting points, not device categories or universal standards. Choose breakpoints where content, navigation, or component behavior actually needs to change:

| Tier | Min Width | Container Max | Columns | Typical Devices |
|:---|---:|---:|:---:|:---|
| `xs` | 0 | Fluid (100%) | 1 | Small phones, stacked layout |
| `sm` | 576px | 540px | 1–2 | Large phones |
| `md` | 768px | 720px | 2–3 | Tablets portrait |
| `lg` | 1024px | 960px | 3 | Tablets landscape, small laptops |
| `xl` | 1200px | 1140px | 3–4 | Standard laptops/desktops |
| `xxl` | 1440px | 1320px | 4+ | Large desktops, ultrawide |

**Responsive behavior for admin templates:**
```
┌─ Mobile (<768px): Sidebar collapses to drawer/overlay; single column; stacked KPI cards
├─ Tablet (768–1024px): Sidebar icon-only rail (64px); 2-column card grid
├─ Desktop (1024–1440px): Full sidebar (220–280px); 3-4 column card grid
└─ Wide (>1440px): Max-width container; spacious layout with persistent sidebar
```

### 5.7 Content Width & Reading Measure

For content-heavy frontend pages, controlling line length is a critical usability win. A frequently useful range for sustained body reading is **about 45–75 characters per line**, but language, typeface, font size, and task can move the appropriate measure.

```css
/* Cap article content at comfortable reading width */
.article-content {
  max-width: 65ch;
  margin-inline: auto;
}

/* Allow background sections to remain fluid */
.hero, .full-width-section {
  width: 100%;
  /* Content inside still constrained */
}
.hero .inner {
  max-width: 65ch;
  margin-inline: auto;
}
```

### 5.8 CSS Grid vs. Flexbox vs. Container Queries

| Technology | Axes | Best For | Key Pattern |
|:---|:---:|:---|:---|
| **CSS Grid** | 2D (rows + columns) | Page structure, card grids, dashboard layouts, any layout needing alignment in both axes | `grid-template-columns: repeat(auto-fit, minmax(280px, 1fr))` |
| **Flexbox** | 1D (row OR column) | Navigation bars, button groups, card headers, form rows, single-axis alignment | `display: flex; align-items: center; gap: 16px` |
| **Container Queries** | Component-driven | Components that respond to their container size, not viewport. Admin templates with resizable sidebars | `@container card (min-width: 400px) { ... }` |

### 5.9 Responsive Design: Constraint-First and Mobile-First

Mobile-first is a strong default for many products: start with the tightest constraints and progressively enhance. It is not the only valid workflow; complex desktop applications may require a shared constraint model designed from both narrow and wide states.

```css
/* Base: mobile (no query needed) */
.page-container {
  padding-inline: 16px;
  max-width: 100%;
}

/* Tablet */
@media (min-width: 640px) {
  .page-container { padding-inline: 32px; }
  .grid { grid-template-columns: repeat(2, 1fr); }
}

/* Laptop */
@media (min-width: 1024px) {
  .page-container { padding-inline: 48px; }
  .grid { grid-template-columns: repeat(3, 1fr); }
  .sidebar { display: block; }
}

/* Desktop */
@media (min-width: 1440px) {
  .page-container { max-width: 1280px; margin-inline: auto; }
  .grid { grid-template-columns: repeat(4, 1fr); }
}
```

### 5.10 Density Modes and Semantic Spacing

Do not create separate arbitrary spacing scales for every screen. Keep one primitive scale and map semantic tokens such as `--space-control-gap`, `--space-card-padding`, and `--space-section` to different steps for comfortable, compact, and dense modes.

---

### 5.11 Container-Driven Components

Viewport media queries remain useful for page-level composition, but reusable components should often respond to their own available space.

```css
.card-region {
  container: card / inline-size;
}

.card {
  display: grid;
  gap: var(--space-4);
}

@container card (min-width: 32rem) {
  .card {
    grid-template-columns: minmax(0, 1fr) auto;
    align-items: start;
  }
}
```

Use container queries when the same component can appear in a sidebar, modal, dashboard grid, or full-width page. Keep a non-container fallback for older targets when required by the support policy.

### 5.12 Reflow, Zoom, Safe Areas and Dynamic Viewports

Responsive design is not only breakpoint selection.

- At 320 CSS pixels or 400% zoom, content should reflow without two-dimensional scrolling except where the content genuinely requires it, such as a large data table or map.
- Prefer `min-block-size: 100dvh` for viewport-filling regions, with appropriate fallbacks; avoid assuming classic `100vh` equals the visible mobile viewport.
- Use `env(safe-area-inset-*)` when full-bleed interfaces can overlap display cutouts or system UI.
- Let text and controls grow. Fixed heights commonly fail when users zoom, increase text size, or load longer translations.
- For wide data tables, preserve semantics and provide scrolling, column prioritization, or alternate summaries rather than hiding important columns without explanation.

## 6. Product, Admin & Dashboard Design

Admin interfaces are dense, data-rich environments where **efficiency, clarity, and learnability** take precedence over visual flair. Every design decision must reduce cognitive load and accelerate the path from question to insight. Users of admin templates are typically repeat users who spend hours daily in the interface — optimizing for expert use patterns (shortcuts, density, quick scanning) is at least as important as first-use learnability.

### 6.1 Product and Admin Design Philosophy

Product and admin interfaces usually prioritize repeatable task completion, information retrieval, and state management.

The core distinction: admin UIs serve **expert, repeat users** performing **task-oriented workflows** (CRUD, filtering, monitoring). Every design decision prioritizes **efficiency and data clarity** over emotional expression. The layout follows an **app shell pattern** (sidebar + topbar + content area) rather than scrolling page sections.

### 6.2 Admin Layout Structure (App Shell Pattern)

The standard admin layout follows the "app shell" pattern:

```
┌──────────────────────────────────────────────────────┐
│  TOPBAR (56–64px height)                             │
│  Logo · Search (⌘K) · Notifications · User Avatar   │
├─────────┬────────────────────────────────────────────┤
│         │  BREADCRUMB: Home / Dashboard              │
│ SIDEBAR │                                            │
│ 220–    │  KPI CARDS (3–4 columns)                   │
│ 280px   │  ┌─────┐ ┌─────┐ ┌─────┐ ┌─────┐         │
│         │  │Rev  │ │Ord  │ │Users│ │Churn│          │
│ ○ Dash  │  └─────┘ └─────┘ └─────┘ └─────┘         │
│ ○ Analy │                                            │
│ ○ Users │  CHARTS (2 columns)                        │
│ ○ Prods │  ┌───────────┐ ┌───────────┐              │
│ ○ Ordrs │  │ Bar Chart │ │Donut/Pie  │              │
│ ─────── │  └───────────┘ └───────────┘              │
│ ○ Setng │                                            │
│ ○ Logs  │  DATA TABLE (full width)                   │
│         │  ┌────────────────────────────┐            │
│         │  │ Search │ Filters │ Export  │            │
│         │  │ Row 1                      │            │
│         │  │ Row 2                      │            │
│         │  │ Row 3                      │            │
│         │  │ Pagination                 │            │
│         │  └────────────────────────────┘            │
└─────────┴────────────────────────────────────────────┘
```

### 6.3 Sidebar Navigation Design

**Specifications:**
- **Width:** 220–280px expanded, 64px collapsed (icon-only rail)
- **Content:** Icons + text labels (not icons alone — icons without labels are ambiguous)
- **Grouping:** Organize items into labeled sections (e.g., "Overview", "Management", "System")
- **Active state:** Left border accent (3–4px) + background fill + text color change
- **Nesting:** Prefer shallow information architecture. When deeper hierarchy is necessary, use clear group labels, disclosure, breadcrumbs, search, or alternate views and test findability.
- **Responsive behavior:** Choose collapse points from available content width. A full sidebar may become a labeled compact rail, drawer, or alternate navigation; icon-only navigation requires especially strong testing and accessible names.
- **Section labels:** 10–12px, uppercase, expanded letter-spacing (0.1–0.2em), muted color

### 6.4 Data Tables: The Core Admin Surface

Data tables are the most critical component in admin UIs. Getting them right determines overall usability.

**Essential specifications:**
- **Row height:** Size rows for legibility and interaction. WCAG 2.2 Target Size (Minimum) uses a 24×24 CSS-pixel floor with exceptions; 44×44 remains a strong touch-oriented target. Dense desktop rows may be shorter only when controls still meet the applicable target/spacing rules.
- **Text alignment:** Left-align text; right-align numbers. Center icons/status badges
- **Number formatting:** Use monospace/tabular numerals for numeric columns
- **Striping:** Zebra striping and hover highlighting can coexist when the difference remains clear and does not create visual noise; choose based on table length, density, and user testing.
- **Fixed header:** On scroll, the table header should remain visible
- **Sorting:** Sort arrows on all sortable columns, clear visual indicator of current sort column and direction
- **Pagination vs. incremental loading:** Use pagination when users need stable position, sharing, comparison, or bulk operations. Infinite or virtualized scrolling can suit discovery, but must preserve keyboard access, focus, history, and a reachable footer.
- **Search and filters:** Place directly above the table, visually connected via proximity
- **Bulk actions:** Checkbox column + action bar that appears when rows are selected
- **Empty states:** When table has no data, show a helpful message with guidance — never show a blank table

### 6.5 KPI Cards & Dashboard Widgets

KPI cards follow a consistent internal structure:

```
┌─────────────────────────────┐
│  REVENUE            ↗ 12%  │  ← Label (small, uppercase, muted)
│  $84.2K                    │  ← Value (large, bold, prominent)
│  ▲ 12.4% vs last month    │  ← Delta (colored, directional arrow)
│  ═══════════════════       │  ← Color strip (categorize card types)
└─────────────────────────────┘
```

**Rules:**
- Label → Value → Delta vertical hierarchy
- Colored bottom borders or left strips to categorize card types
- Consistent padding (20–24px)
- Keep KPI card composition consistent within a comparison group; deliberate variation may be used when it communicates different information rather than decoration.
- Delta values: communicate meaning with text or symbols as well as color; direction alone is not equivalent to good or bad.
- Use sparklines or micro-charts inside cards for trend context

### 6.6 Form Design in Admin

**Best practices established through industry best practices:**
- **Label placement:** Stacked labels are a robust default, especially for narrow screens and variable-length translations. Inline labels can work in compact expert tools when alignment, zoom, errors, and localization remain usable.
- **Label-to-input gap:** 8px (consistent)
- **Field grouping:** Group related fields in fieldsets with 24px inter-group spacing
- **Error handling:** Error messages appear immediately below the relevant field, in red/danger color, with an icon. Required fields marked clearly with asterisk
- **Buttons:** Primary action (Save/Submit) on the right or left based on convention, visually dominant. Secondary (Cancel) visually subordinate
- **Validation timing:** Validate at a moment that helps the user without interrupting entry. Blur can work for many fields; immediate validation is appropriate only when the feedback is stable and non-disruptive. Always validate again on submission.
- **Unavailable actions:** Prefer explaining why an action is unavailable. Native disabled controls are exempt from some WCAG contrast criteria, but low opacity can still harm comprehension; do not use a fixed opacity as the only pattern.

### 6.7 Data Visualization & Chart Design

**Guidelines for admin charts:**
- **Choose the chart by task:** Bar charts support comparison, line charts support change over ordered intervals, and part-to-whole charts require very few clearly differentiated categories. A table or direct label may be better than a chart.
- **Color usage:** Use a constrained, contrast-tested palette and redundant encoding. “Positive” and “negative” depend on context—a decrease in churn is positive, for example—so pair color with direction, labels, or symbols.
- **Legends:** Place directly above or beside the chart, use color dots + text labels
- **Axes and labels:** Always label axes. Use readable, abbreviated formats for large numbers (e.g., $84K, 1.2M)
- **Interactivity:** Hover tooltips for exact values. Click-to-filter for drill-down flows
- **Simple is better:** Keep charts simple. A clear bar chart communicates better than a complex 3D visualization

### 6.8 Color Use in Admin Templates

**Admin-specific color system:**
- **Sidebar/topbar:** Dark, desaturated primary (navy #1a2744, slate #1d3557, charcoal #2d3748)
- **Content area:** White (#FFFFFF) or near-white (#F0F2F5, #F8FAFC) background
- **Single brand accent:** One primary color for main actions and active states
- **Semantic status colors:** Common conventions use green for success, red for error/danger, amber for warning, and blue/cyan for information. Do not depend on hue alone, and introduce only the roles the product genuinely needs.
- **Text hierarchy:** Primary text (#1a2030), secondary (#5a6478), muted (#8898aa)
- **Borders:** Light (#E0E4EA) for subtle dividers, slightly darker for input borders

```css
/* Admin Template Color Tokens */
:root {
  /* Surface */
  --bg-app: #f0f2f5;
  --bg-card: #ffffff;
  --bg-sidebar: #1a2744;
  --bg-topbar: #1d3557;

  /* Text */
  --text-primary: #1a2030;
  --text-secondary: #5a6478;
  --text-muted: #8898aa;
  --text-on-dark: rgba(255,255,255,0.85);

  /* Semantic status */
  --color-success: #27ae60;
  --color-warning: #f39c12;
  --color-danger: #c84b31;
  --color-info: #3498db;

  /* Brand accent */
  --color-primary: #2563EB;
  --color-primary-light: rgba(37,99,235,0.12);
}
```

### 6.9 Admin-Specific Typography Details

Beyond the general admin typography guidelines covered in Sections 4 and 8, these admin-specific specifications apply:

- **Table data cells:** 13px, monospace for numbers, tabular figures enabled via `font-variant-numeric: tabular-nums`
- **Sidebar navigation labels:** 12px, 400 weight, muted color
- **Section group labels:** 10–11px, uppercase, 0.1–0.2em letter-spacing, muted color
- **Breadcrumbs and metadata:** 12–13px, regular weight, secondary color

### 6.10 Admin Density Controls

Beyond the general admin spacing guidelines covered in Sections 5 and 8, admin templates benefit from **user-configurable density modes**:

- **Comfortable:** Default spacing (card padding 20px, table rows 44px, form gaps 16px)
- **Compact:** One step tighter (card padding 16px, table rows 36px, form gaps 12px)
- **Dense:** Maximum density (card padding 12px, table rows 32px, form gaps 8px)

Implement by shifting token values down one step in the spacing scale per mode. Sidebar item height should remain at 36–40px across all modes to maintain clickability.

### 6.11 Progressive Disclosure

In complex admin UIs, show only what's needed and reveal additional detail on demand:
- **Expandable table rows:** Click to reveal detail panels
- **Accordion sections:** Collapse infrequently-used settings
- **Filters on demand:** "Show filters" toggle rather than always-visible filter bar
- **Contextual actions:** Reduce persistent clutter where appropriate, but never make essential actions hover-only. Ensure keyboard, touch, and screen-reader users can discover and operate the same actions.
- **Modal/drawer detail views:** Click a row to open a side panel or modal with full record detail

---

### 6.12 Responsive and Accessible Data Tables

A table should remain a table when relationships between rows and columns matter.

- Keep real `<table>`, `<th>`, and `<td>` semantics for tabular data.
- Provide a caption or nearby programmatic name that explains the table's purpose.
- Use `scope` for straightforward headers; use explicit `headers`/`id` relationships only for genuinely complex header structures.
- Make sortable headers buttons inside header cells, and expose the current direction with `aria-sort`.
- When horizontal scrolling is necessary, keep the scroll region keyboard accessible and visually indicate that more columns exist.
- Do not transform every row into unrelated cards without preserving header context.
- Virtualization must preserve accessible names, row/column context, focus, and announcement of updated result counts.

### 6.13 Command, Undo and Destructive-Action Design

Frequent expert workflows benefit from shortcuts and reversible actions.

- Advertise keyboard shortcuts without making them the only way to act.
- Prefer undo or soft deletion when the domain permits it.
- Use confirmation dialogs for high-impact, hard-to-reverse actions—not for every minor operation.
- State exactly what will happen: identify the record, scope, side effects, and whether recovery is possible.
- Keep primary and destructive actions visually distinct; do not rely on red alone.

## 7. Public-Facing & Marketing-Site Design

Marketing and public-facing design often prioritizes explanation, persuasion, brand expression, and conversion while still requiring clarity, efficiency, accessibility, and performance. Expressiveness is useful only when it supports the content and user goal.

### 7.1 Hero Section Design

A hero or opening region should quickly establish the page purpose, value proposition, and next useful path. Not every page needs a large hero; task pages and returning-user experiences often benefit from a compact introduction.

**Rules:**
- **Headline:** Make it specific, comprehensible, and consistent with the page content. Word count is a constraint to test, not a universal limit.
- **Supporting copy:** Add only the context needed to understand the offer, audience, or next step.
- **Primary action:** Establish one visually dominant next action. Secondary links are valid when users genuinely need alternate paths.
- **Visual focal point:** Use a product image, demonstration, illustration, or other evidence when it improves understanding; decoration is optional.
- **Whitespace:** Your most powerful tool here — resist the urge to fill it
- **Height:** Let content and context determine height. Avoid forcing every hero to 100vh; test small screens, dynamic browser chrome, zoom, and translated copy.

### 7.2 Landing Page Flow & Narrative Arc

A common landing-page narrative follows the user’s questions, but the order should be adapted to awareness level, traffic source, risk, and purchase complexity:

```
1. HERO          → "What is this?" (headline, CTA, hero image)
2. PROBLEM/PAIN  → "I have this problem" (empathy, pain points)
3. SOLUTION      → "This solves it" (product/service overview)
4. SOCIAL PROOF  → "Others trust it" (testimonials, logos, stats)
5. FEATURES      → "How it works" (key features, benefits)
6. FAQ           → "What about..." (objections addressed)
7. FINAL CTA     → "I'm convinced" (repeat CTA, urgency)
```

Each section should answer a real user question. Alternating backgrounds is one possible rhythm device, not a requirement; hierarchy and continuity matter more than visual alternation.

### 7.3 CTA Design

**Primary CTA:**
- High-contrast filled button
- Prominent size (minimum 44px height, 48px preferred)
- Action-oriented verb ("Start Free Trial", "Download Now", "Get Access")
- One visually dominant primary action per decision point; additional actions should have clearly lower emphasis
- Visual dominance — largest, boldest button on the page

**Secondary CTA:**
- Ghost/outline style or text link
- Visually subordinate to primary
- Avoid presenting competing primary actions with equal prominence unless the choice is genuinely equal and clearly explained.

### 7.4 Social Proof Patterns

- **Testimonials:** Identify the source and context, obtain permission, and avoid fabricated or misleading endorsements. Length should preserve the evidence rather than satisfy an arbitrary line limit.
- **Ratings:** Show only when they are genuine, attributable, representative, and relevant to the decision.
- **Customer logos:** Use only with authorization and enough context to avoid implying a relationship or endorsement that does not exist.
- **Specific metrics:** "$2.4M revenue in 90 days" beats "significant revenue growth." Specificity = credibility
- **Case study numbers:** Concrete, specific results with named companies

### 7.5 Cards & Content Grouping

Cards are the universal content container for both admin and frontend:

**Frontend card design:**
- Subtle shadow (box-shadow: 0 4px 12px rgba(0,0,0,0.08)) or light border
- Consistent padding (24–32px)
- Internal hierarchy: image/icon → heading → description → action
- Hover state: slight elevation increase, shadow deepening
- Border radius: 8–12px for modern, rounded feel

### 7.6 Navigation Design

**Desktop:** A horizontal top navigation is common, but layout and item count should follow the information architecture. Dropdowns and mega-menus are both valid when their structure, keyboard behavior, and content volume justify them.

**Mobile:** A menu button may open a drawer, disclosure, or full-screen panel. Label the control clearly, manage focus, and keep essential tasks reachable without obscuring content.

### 7.7 Motion & Microinteractions

Motion is a powerful tool when used with restraint. It signals state changes, guides attention, and creates delight.

**Timing guidelines:**
- **Hover states:** 150–250ms ease transitions
- **Button press:** scale(0.97) on active for tactile feedback
- **Scroll animation:** Use only when it explains progression or supports narrative. Avoid hiding essential content until animation runs.
- **Loading states:** Use skeletons for predictable content layouts and progress indicators or status text for indeterminate operations; avoid decorative loading animation that hides real delay
- **Entrance animations:** Under 300ms
- **Exit animations:** Under 200ms
- **Animation budget:** Evaluate cumulative motion, interruption, CPU/GPU cost, and task delay rather than applying one universal duration budget.

**Animation tokens:**
```css
:root {
  --ease-in: cubic-bezier(0.4, 0, 1, 1);
  --ease-out: cubic-bezier(0, 0, 0.2, 1);
  --ease-inout: cubic-bezier(0.4, 0, 0.2, 1);
  --duration-fast: 150ms;
  --duration-base: 250ms;
  --duration-slow: 400ms;
}
```

**Critical:** Respect `prefers-reduced-motion` and provide a low-motion treatment for non-essential movement:
```css
@media (prefers-reduced-motion: reduce) {
  [data-motion="decorative"],
  .scroll-reveal,
  .parallax {
    animation: none !important;
    transition: none !important;
    transform: none !important;
  }
}
```

### 7.8 Component-First Design Thinking

Modern frontend work benefits from reusable, variant-aware components, but page and content needs should inform the component model. Avoid designing an abstract component library without representative page scenarios.

**Define your button in 5 states** (default, hover, active, disabled, loading) **and 3 sizes** (sm, md, lg) before building a single page. This atomic approach ensures consistency at scale and eliminates "design drift" that happens when components are invented per-page.

**Design token cascade for components:**
```css
/* Button component with design tokens */
.btn {
  padding: var(--space-3) var(--space-6);
  font-size: var(--text-sm);
  font-weight: 600;
  border-radius: var(--radius-md);
  transition:
    background-color var(--duration-fast) var(--ease-out),
    color var(--duration-fast) var(--ease-out),
    border-color var(--duration-fast) var(--ease-out),
    box-shadow var(--duration-fast) var(--ease-out),
    transform var(--duration-fast) var(--ease-out);
  cursor: pointer;
  border: none;
}

.btn-primary {
  background: var(--color-primary);
  color: var(--color-on-primary);
}

.btn-primary:hover {
  background: var(--color-primary-hover);
  box-shadow: var(--shadow-md);
}

.btn-primary:active {
  transform: scale(0.97);
}

.btn-primary:disabled {
  opacity: 0.5;
  cursor: not-allowed;
}
```

**Front-end design token system:**
```css
:root {
  /* Shadows */
  --shadow-sm: 0 1px 2px rgba(0,0,0,0.05);
  --shadow-md: 0 4px 12px rgba(0,0,0,0.08);
  --shadow-lg: 0 12px 40px rgba(0,0,0,0.12);
  --shadow-xl: 0 24px 64px rgba(0,0,0,0.16);

  /* Border radius */
  --radius-sm: 4px;   --radius-md: 8px;
  --radius-lg: 12px;  --radius-xl: 20px;
  --radius-full: 9999px;
}
```

---

### 7.9 Content Design and Evidence Hierarchy

A polished layout cannot compensate for vague or unsupported content.

- Put the claim, supporting evidence, and action in a logical order.
- Use concrete language and disclose important limitations, prices, commitments, and eligibility conditions before the user acts.
- Match the page message to the acquisition source; an ad, search result, email, and direct visit may create different expectations.
- Treat testimonials, ratings, customer counts, and performance claims as evidence that requires provenance and maintenance.
- Give privacy, cancellation, returns, and contact information appropriate visibility instead of hiding trust-critical details in decorative footers.

### 7.10 Ethical Conversion Design

Conversion optimization must not depend on deception.

- Do not preselect optional purchases or consent.
- Do not create false scarcity, fake countdowns, hidden recurring charges, or confusing cancellation paths.
- Keep accept and decline choices understandable and proportionate.
- Confirm high-impact commitments with a clear summary.
- Measure downstream outcomes—returns, support contacts, cancellation, and trust—not only immediate clicks.

## 8. Accessibility & Inclusive Design

Accessible design is a product-quality requirement, not a visual afterthought. The normative baseline in this guide is **WCAG 2.2**. Legal obligations vary by jurisdiction, organization, sector, contract, and product scope; WCAG conformance is not automatically identical to legal compliance.

### 8.1 WCAG 2.2 Visual Requirements

| Topic | WCAG 2.2 requirement | Level | Design consequence |
|:---|:---|:---:|:---|
| Normal text contrast | At least 4.5:1 | AA | Test text in every state and on every actual background |
| Large text contrast | At least 3:1 | AA | “Large” means at least 18pt regular or 14pt bold under WCAG's definition |
| Non-text contrast | At least 3:1 for required visual information in controls and graphics | AA | Boundaries, icons, chart marks, and states may need contrast; exceptions apply |
| Focus visible | A visible focus indicator is required for keyboard-operable UI | AA | Do not remove focus without an effective replacement |
| Focus appearance | Minimum area and 3:1 change-of-contrast requirements | AAA | A strong design target, but not an AA criterion |
| Focus not obscured | Focused components must not be entirely hidden by author-created content | AA | Sticky headers, cookie banners, and overlays must not cover the focused item |
| Target size (minimum) | At least 24×24 CSS px, subject to listed exceptions | AA | Use larger targets where practical; spacing can satisfy some small-target cases |
| Target size (enhanced) | At least 44×44 CSS px | AAA | Strong touch-oriented target, not the WCAG 2.2 AA minimum |
| Reflow | Content reflows at 320 CSS px equivalent, with exceptions | AA | Avoid fixed layouts and unnecessary two-dimensional scrolling |
| Text spacing | No loss when users apply specified line, paragraph, letter, and word spacing | AA | Avoid fixed heights and clipped text |
| Use of color | Color is not the only visual means of conveying information | A | Add text, symbols, patterns, shape, or position |
| Animation from interaction | Motion animation triggered by interaction can be disabled unless essential | AAA | Reduced-motion support is a strong inclusive-design practice |
| Pause, stop, hide | Moving, blinking, scrolling, or auto-updating content has controls under defined conditions | A | Do not treat all autoplay as harmless decoration |

**Important distinction:** WCAG techniques are informative examples, not the only valid implementations. Conformance is evaluated against the success criteria.

### 8.2 Contrast and State Design

Contrast must be checked at the component-state level, not only in the palette.

Test at least:
- default, hover, focus, active, selected, visited, invalid, disabled, and loading states;
- text over images, gradients, video, glass/translucent surfaces, and elevated layers;
- light, dark, high-contrast, and forced-colors modes;
- icons, chart marks, input boundaries, focus indicators, and status badges.

Placeholder text is still text and normally needs text contrast, but it must not replace a persistent label. Disabled controls are exempt from some contrast requirements; nevertheless, users still need to understand that the control exists and why it is unavailable.

### 8.3 Do Not Encode Meaning with Color Alone

Use redundant encoding:

- Error: icon or prefix + clear message + field association.
- Success: text confirmation + optional symbol, not green alone.
- Charts: direct labels, patterns, line styles, point shapes, or a data table.
- Required fields: explicit text or a programmatically explained marker.
- Navigation state: `aria-current`, text/shape/weight changes, and color where useful.
- Positive/negative trends: describe the meaning; “up” is not always positive.

A grayscale preview is a useful diagnostic, but it does not replace testing for specific forms of color-vision deficiency or real assistive technology.

### 8.4 Focus, Keyboard and Source Order

```css
:focus-visible {
  outline: 3px solid var(--color-focus);
  outline-offset: 3px;
}

@media (forced-colors: active) {
  :focus-visible {
    outline-color: Highlight;
  }
}
```

- Keep DOM/source order consistent with the logical reading and interaction order.
- Avoid positive `tabindex` values.
- Ensure every function is operable from a keyboard where the task can be performed with a keyboard.
- Keep focus visible when content scrolls beneath sticky or fixed regions.
- When opening a modal dialog, move focus appropriately, constrain interaction to the modal, support Escape where appropriate, and restore focus to a logical place when it closes.
- Prefer native `<dialog>`, `<button>`, `<details>`, `<select>`, and form controls before recreating their behavior.
- A focus ring must remain distinguishable from an existing border; a color change alone can be too subtle.

### 8.5 Text Spacing, Zoom and Reflow

WCAG 2.2 SC 1.4.12 requires no loss of content or functionality when users apply:

- line height of at least 1.5 times the font size;
- paragraph spacing of at least 2 times the font size;
- letter spacing of at least 0.12 times the font size;
- word spacing of at least 0.16 times the font size.

These values describe a **resilience test**, not mandatory default typography. Test 200% browser zoom, 400% zoom/reflow where applicable, text-only zoom on supporting platforms, and operating-system text scaling.

Common failures:
- fixed-height buttons or inputs that clip text;
- cards whose text overflows hidden;
- icon-only layouts that lose labels;
- sticky regions that leave too little viewport space;
- horizontal navigation that cannot wrap or scroll;
- absolute positioning that disconnects visual and source order.

### 8.6 Motion, Transparency and Sensory Preferences

```css
@media (prefers-reduced-motion: reduce) {
  [data-motion="decorative"],
  .parallax,
  .scroll-reveal {
    animation: none !important;
    transition: none !important;
    transform: none !important;
  }
}

@media (prefers-reduced-transparency: reduce) {
  .glass-surface {
    backdrop-filter: none;
    background: var(--color-surface);
  }
}
```

`prefers-reduced-motion` is broadly useful. As of July 2026, `prefers-reduced-transparency` still has limited browser availability, so provide a solid fallback without depending on the query.

Reduce or remove:
- large parallax movement;
- zooming and spatial transitions;
- looping ambient animation;
- autoplay carousels;
- rapid flashing;
- motion that tracks the pointer continuously.

Preserve essential feedback in a less motion-intensive form—for example, an immediate state change or short opacity transition.

### 8.7 Semantic HTML, Names and Instructions

- Use headings to represent document structure, not visual size.
- Use landmarks (`header`, `nav`, `main`, `aside`, `footer`) according to their semantics.
- Give every form control a persistent accessible name, usually with `<label>`.
- Use `fieldset` and `legend` for related options.
- Give informative images meaningful alternative text; use `alt=""` for decorative images.
- Give icon-only controls an accessible name.
- Use real buttons for actions and real links for navigation.
- Associate errors and help text with their controls.
- Use table headers, captions, and scopes for tabular data.
- Keep instructions available to users who cannot perceive color, position, shape, sound, or motion.

### 8.8 ARIA and Complex Widgets

ARIA supplements native HTML; it does not add behavior.

- **Tabs:** implement tab/tabpanel relationships, selected state, focus management, and the documented keyboard model.
- **Disclosure/accordion:** a button controls a region and exposes `aria-expanded`; native `<details>` may be sufficient.
- **Dialog:** accessible name, modal semantics when modal, focus management, and a clear close path.
- **Combobox/listbox:** use the WAI-ARIA Authoring Practices pattern only when a native control cannot meet the requirement.
- **Live updates:** use `role="status"` or a suitable live region for important asynchronous updates; avoid announcing every minor DOM change.
- **Custom grids:** require advanced keyboard and screen-reader behavior; do not apply `role="grid"` to a static table merely for styling.

“No ARIA is better than bad ARIA” remains a practical rule: broken names, states, or keyboard behavior can make an otherwise usable control inaccessible.

### 8.9 Neuro-Inclusive and Cognitive Design

Support varied attention, memory, language, and sensory-processing needs through:

- predictable navigation and consistent control placement;
- plain language and concise instructions;
- visible progress and save state;
- error prevention, recovery, and undo;
- reduced distraction or focus modes;
- user control over motion, sound, density, and notifications;
- avoiding unnecessary time limits;
- authentication flows that do not depend solely on memory puzzles or transcription.

Do not claim that one layout “works for ADHD,” autism, dyslexia, or another condition as a universal rule. Test with diverse participants and provide adjustable options.

### 8.10 Legal and Organizational Scope

WCAG is a technical standard; laws and procurement rules determine where and how it is required. The European Accessibility Act applies to specified products and consumer services from 28 June 2025, with scope, exemptions, national implementation, and transitional provisions that require legal review. Public-sector rules, the ADA, Section 508, EN 301 549, and other regimes have different scopes.

For high-risk or regulated products:
1. identify applicable laws and contracts;
2. define the conformance target;
3. document exceptions and known limitations;
4. include disabled users in research;
5. maintain an accessibility statement and issue process;
6. retest after component, content, and platform changes.

## 9. Design Tokens & Implementation Contracts

Design tokens turn design decisions into named, reusable data. They are most effective when they separate raw values from meaning and component use, and when governance prevents components from bypassing the token system.

### 9.1 Token Architecture

```text
Primitive tokens
├── color.blue.600
├── space.6
├── radius.medium
└── duration.fast

Semantic tokens
├── color.action.primary
├── color.text.muted
├── space.container.padding
└── duration.feedback

Component tokens
├── button.primary.background
├── input.border.focus
├── table.row.block-size
└── card.padding
```

**Responsibilities:**
- **Primitive:** raw scales with no usage promise.
- **Semantic:** stable intent that can map to different primitives by theme, mode, brand, or platform.
- **Component:** local decisions used when a component needs a controlled exception or a public customization contract.

Do not expose every internal component value as a public token. Too many tokens make the system harder to change, not easier.

### 9.2 Naming Principles

A useful name describes intent rather than appearance.

```text
Prefer: color.text.danger
Avoid:  color.red.600 in component code

Prefer: space.control.inline
Avoid:  margin-left-12

Prefer: motion.duration.feedback
Avoid:  animation-200
```

Names should remain meaningful when:
- light mode becomes dark mode;
- a brand changes its primary hue;
- a component moves from web to native;
- density changes;
- localization changes text length.

### 9.3 DTCG 2025.10 Format

The Design Tokens Community Group published its first stable Community Group Report, **2025.10**, on 28 October 2025. It is stable for production exchange workflows but is not a W3C Standards Track Recommendation.

```json
{
  "color": {
    "blue": {
      "600": {
        "$type": "color",
        "$value": {
          "colorSpace": "srgb",
          "components": [0.145, 0.388, 0.922],
          "alpha": 1
        }
      }
    },
    "action": {
      "primary": {
        "$type": "color",
        "$value": "{color.blue.600}"
      }
    }
  },
  "space": {
    "6": {
      "$type": "dimension",
      "$value": { "value": 1.5, "unit": "rem" }
    }
  }
}
```

Use the resolver/module features only when the toolchain supports them. Validate token files in CI and pin tool versions because ecosystem implementations may support different parts of the report.

### 9.4 CSS Custom Properties

```css
@layer tokens {
  :root {
    --color-bg: #fff;
    --color-surface: #f8fafc;
    --color-text: #0f172a;
    --color-text-muted: #334155;
    --color-action: #2563eb;
    --color-on-action: #fff;

    --space-1: 0.25rem;
    --space-2: 0.5rem;
    --space-4: 1rem;
    --space-6: 1.5rem;

    --radius-sm: 0.25rem;
    --radius-md: 0.5rem;
  }

  [data-theme="dark"] {
    --color-bg: #0b1220;
    --color-surface: #111827;
    --color-text: #f9fafb;
    --color-text-muted: #cbd5e1;
    --color-action: #60a5fa;
    --color-on-action: #0b1220;
  }
}
```

Prefer semantic variables in components:

```css
.card {
  background: var(--color-surface);
  color: var(--color-text);
  padding: var(--space-card-padding, var(--space-6));
  border-radius: var(--radius-card, var(--radius-md));
}
```

### 9.5 Theme and Mode Strategy

A mode changes context; a theme changes identity. Keep those dimensions separate where the product needs both.

```html
<html data-color-scheme="dark" data-brand="acme" data-density="compact">
```

```css
[data-density="compact"] {
  --space-card-padding: var(--space-4);
  --table-row-size: 2.25rem;
}

[data-density="comfortable"] {
  --space-card-padding: var(--space-6);
  --table-row-size: 2.75rem;
}
```

Support a three-way color choice when useful:
- light;
- dark;
- system preference.

Store an explicit user choice and avoid overwriting it when the operating-system preference changes.

### 9.6 Tailwind CSS Integration

Current Tailwind uses CSS-first theme variables through `@theme`. Use them when a token should generate utilities; use ordinary custom properties for tokens that should not.

```css
@import "tailwindcss";

@theme {
  --color-brand-600: oklch(55% 0.19 255);
  --font-display: "Brand Sans", system-ui, sans-serif;
  --breakpoint-3xl: 120rem;
}

:root {
  --color-text-danger: #b91c1c;
}
```

This creates utilities such as `bg-brand-600` and `font-display`, while `--color-text-danger` remains a normal runtime variable. Keep the DTCG source independent from Tailwind and generate the adapter so framework naming does not become the source of truth.

### 9.7 Bootstrap Integration

Bootstrap 5.3 exposes many `--bs-*` CSS variables and supports color modes through `data-bs-theme`.

```css
[data-bs-theme="brand-dark"] {
  --bs-body-bg: var(--color-bg);
  --bs-body-color: var(--color-text);
  --bs-primary: var(--color-action);
  --bs-border-color: var(--color-border);
  --bs-focus-ring-color: color-mix(
    in srgb,
    var(--color-focus) 35%,
    transparent
  );
}
```

Some Bootstrap decisions still originate in Sass variables or maps. Create a documented adapter layer instead of scattering Bootstrap overrides through component files.

### 9.8 Sass/SCSS and Build-Time Adapters

Sass remains useful for generating repetitive static output, but semantic CSS custom properties are better for runtime theme switching.

```scss
$space: (
  1: 0.25rem,
  2: 0.5rem,
  4: 1rem,
  6: 1.5rem
);

@each $step, $value in $space {
  .gap-#{$step} {
    gap: $value;
  }
}
```

Do not maintain unrelated values independently in JSON, Sass, CSS, Figma, and native code. Generate platform outputs from one reviewed token source wherever the toolchain permits.

### 9.9 Component Contracts

A component contract should document:
- semantic purpose;
- supported variants and states;
- public tokens or slots;
- accessible name and keyboard behavior;
- responsive behavior;
- localization constraints;
- motion behavior and reduced-motion alternative;
- color-mode and forced-colors behavior;
- deprecation and migration policy.

Example:

```css
.button {
  --button-bg: var(--color-action);
  --button-fg: var(--color-on-action);
  --button-radius: var(--radius-md);

  min-block-size: 2.75rem;
  padding-inline: var(--space-4);
  border-radius: var(--button-radius);
  background: var(--button-bg);
  color: var(--button-fg);
}
```

### 9.10 Governance and Versioning

- Assign token owners and reviewers.
- Record why a token exists and where it may be used.
- Detect unused and hard-coded values.
- Treat renaming or semantic changes as migrations.
- Publish changelogs and codemods where practical.
- Test visual output and accessibility before release.
- Keep aliases shallow enough to debug.
- Do not use tokens to hide inconsistent product decisions; resolve the decision first.

## 10. Testing, Validation & Quality Assurance

Testing must verify both implementation and design intent. Automated checks are valuable, but they cannot determine whether content is understandable, focus moves logically, an interaction model is appropriate, or a visual hierarchy matches the task.

### 10.1 Quality Model

Use multiple layers:

1. **Static validation:** HTML, CSS, linting, type checks, token validation.
2. **Component tests:** states, interactions, keyboard behavior, themes, localization.
3. **Automated accessibility checks:** axe-based rules and other machine-testable failures.
4. **Visual regression:** unexpected rendering changes across components and pages.
5. **End-to-end tests:** complete user workflows in representative browsers.
6. **Manual accessibility testing:** keyboard, screen readers, zoom, reflow, forced colors.
7. **Usability testing:** whether real users understand and complete tasks.
8. **Field monitoring:** Core Web Vitals, errors, abandonment, support signals.

### 10.2 Automated Accessibility Testing

Useful tools include:
- **axe-core** directly or through Playwright/Cypress integrations;
- **Storybook accessibility testing** for rendered component stories;
- **Lighthouse** for a broad automated audit and performance diagnostics;
- **Pa11y** or equivalent CI runners;
- HTML validators and framework-specific lint rules.

Playwright’s current guidance uses axe integrations for accessibility rules. Its old `page.accessibility` API was removed; do not build new test infrastructure around it.

```ts
import AxeBuilder from '@axe-core/playwright';
import { expect, test } from '@playwright/test';

test('account form has no detectable WCAG A/AA violations', async ({ page }) => {
  await page.goto('/account');

  const results = await new AxeBuilder({ page })
    .withTags(['wcag2a', 'wcag2aa', 'wcag21aa', 'wcag22aa'])
    .analyze();

  expect(results.violations).toEqual([]);
});
```

An automated pass does not prove conformance. It only shows that the selected rules did not detect a failure in that rendered state.

### 10.3 Component-State Coverage

Every reusable component should be exercised in the states it actually supports:

- default;
- hover where a hover-capable pointer exists;
- focus visible;
- active/pressed;
- selected/current/expanded;
- disabled or unavailable;
- loading/busy;
- invalid/error;
- empty;
- long content and localization;
- light, dark, forced-colors, and high-contrast variants;
- reduced motion;
- narrow and wide containers.

Storybook or another component workbench is useful when stories represent real contracts rather than decorative examples.

### 10.4 Interaction and Keyboard Tests

Automate important behavior:

- Tab reaches controls in logical order.
- Enter and Space work according to the native or ARIA pattern.
- Escape closes dismissible overlays where appropriate.
- Focus moves into and out of dialogs correctly.
- Arrow-key models work for tabs, menus, listboxes, and grids only when those roles are used.
- Validation errors receive an understandable announcement.
- Dynamic updates expose status without excessive live-region noise.
- Hidden or inert content is not reachable.

ARIA snapshots can help detect changes in accessible roles, names, and states, but they do not replace screen-reader testing.

### 10.5 Visual Regression

Capture representative states, not only the default component.

Test:
- responsive widths and container sizes;
- multiple browsers where rendering differs materially;
- font-loading completion;
- light/dark/high-contrast themes;
- long translations and bidirectional text;
- focus, validation, loading, and empty states;
- reduced-motion snapshots at a stable animation state.

Treat expected rendering updates as reviewed design changes. Avoid approving large snapshot batches without inspecting why they changed.

### 10.6 Manual Accessibility Protocol

At minimum:

**Keyboard**
- Complete core workflows without a pointer.
- Verify visible focus, logical order, no trap, and reachable dismiss controls.

**Screen reader**
- Test with at least one desktop and one mobile combination appropriate to the audience.
- Verify headings, landmarks, names, descriptions, errors, state changes, and table context.

**Zoom and reflow**
- Test 200% zoom and WCAG reflow conditions.
- Apply text-spacing overrides.
- Check small viewport height as well as width.

**Visual modes**
- Forced colors or a platform high-contrast mode.
- Light and dark appearance.
- Color-vision simulation as a diagnostic.
- Grayscale as a color-dependence check.

**Motion**
- Reduced-motion preference.
- Pause/stop controls for persistent motion.
- Keyboard and touch behavior when animation is removed.

### 10.7 Usability and Content Validation

Use representative tasks and participants. Measure:
- task completion;
- time and error recovery;
- first-click success where relevant;
- comprehension of labels and instructions;
- findability of actions and information;
- confidence before destructive or financial actions;
- perceived workload;
- qualitative reasons for failure.

A/B testing can measure behavior at scale, but it cannot explain every cause and must not be used to justify deceptive patterns.

### 10.8 Performance and Field Quality

Use field data where possible. Current Core Web Vitals “good” thresholds are:
- **LCP:** ≤ 2.5 seconds;
- **INP:** ≤ 200 milliseconds;
- **CLS:** ≤ 0.1;

evaluated at the 75th percentile, separately for mobile and desktop datasets where available.

Also monitor:
- JavaScript errors;
- failed requests;
- long tasks;
- route and interaction latency;
- font and image failures;
- memory growth in long-lived applications;
- accessibility defects reported by users;
- regressions by release.

Lab tools help diagnose; field data reveals what real users experienced.

### 10.9 Cross-Browser and Device Matrix

Derive the matrix from analytics, contracts, and risk.

Include:
- evergreen Chromium, Firefox, and Safari where supported;
- iOS Safari and Android Chrome on real devices for touch-critical products;
- Windows forced-colors behavior;
- keyboard-only desktop use;
- low-power or memory-constrained devices if the audience includes them;
- slow and unreliable network profiles;
- installed/PWA mode where offered.

Do not claim universal browser support based on one engine.

### 10.10 Release Gates

A release is blocked when:
- a core task cannot be completed with the required input methods;
- a new WCAG A/AA failure is confirmed within the conformance scope;
- text or controls become unreadable in a supported theme;
- focus is lost or obscured;
- critical content clips at supported zoom/localization settings;
- visual regression is unexplained;
- performance budgets or field thresholds materially regress without an approved exception;
- analytics, consent, or conversion changes introduce deceptive behavior.

Record exceptions with owner, impact, mitigation, and expiry date.

## 11. Complete Design Workflow & Governance

A practical end-to-end workflow. Adapt the sequence to project risk, team size, and delivery model:

```
PHASE 1: RESEARCH & DEFINE
├── 1.1 Define user personas and use cases
├── 1.2 Analyze competitive landscape
├── 1.3 Establish brand attributes (if applicable)
├── 1.4 Define content hierarchy and information architecture
└── 1.5 Identify applicable accessibility standards, laws, contracts, target conformance, and user needs

PHASE 2: DESIGN SYSTEM FOUNDATION
├── 2.1 Define a documented 4/8-unit spacing scale and exceptions policy
├── 2.2 Define typography scale (modular ratio, font selection)
├── 2.3 Define color palette (primitives → semantic → component)
├── 2.4 Define elevation/shadow scale
├── 2.5 Define border radius and border tokens
├── 2.6 Define motion/animation tokens
└── 2.7 Set up design tokens in code (CSS custom properties)

PHASE 3: COMPONENT DESIGN
├── 3.1 Design atomic components (buttons, inputs, badges, icons)
├── 3.2 Define all component states (default, hover, active, disabled, error, loading)
├── 3.3 Design composite components (cards, forms, navigation, tables)
├── 3.4 Document component usage guidelines
└── 3.5 Build component library (Storybook or equivalent)

PHASE 4: LAYOUT & PAGES
├── 4.1 Design content-driven layout constraints, containers, and responsive transitions
├── 4.2 Create page layouts using components
├── 4.3 Design key page templates (admin: dashboard, list, form, detail; frontend: home, product, landing)
├── 4.4 Validate hierarchy and actual scan/task behavior through testing
└── 4.5 Design responsive behavior for each breakpoint

PHASE 5: VALIDATION & TESTING
├── 5.1 Accessibility audit (contrast, keyboard, screen reader)
├── 5.2 Cross-browser and cross-device testing
├── 5.3 Performance testing and field-monitoring plan (LCP, INP, CLS, errors)
├── 5.4 Visual regression baseline
├── 5.5 Usability testing with real users
└── 5.6 Iterate based on feedback

PHASE 6: DOCUMENTATION & HANDOFF
├── 6.1 Document design decisions and rationale
├── 6.2 Create developer handoff materials
├── 6.3 Maintain living style guide
├── 6.4 Establish ownership, contribution, release, and deprecation processes
└── 6.5 Record decisions, evidence, exceptions, and review dates
```

---

### 11.1 Evidence and Decision Records

For important design decisions, record:

| Field | Purpose |
|:---|:---|
| Problem and users | Prevents a solution from becoming detached from its original need |
| Constraints | Documents platform, legal, accessibility, content, and performance limits |
| Options considered | Shows that the chosen pattern was not arbitrary |
| Evidence | Research, analytics, usability findings, standards, or domain expertise |
| Decision | The selected approach and its intended outcome |
| Risks and exceptions | Known limitations and mitigations |
| Owner and review date | Ensures the decision can be revisited when conditions change |

### 11.2 Design-System Governance

A mature system needs:
- contribution criteria;
- component and token ownership;
- accessibility review;
- design and code review;
- semantic versioning or an equivalent release policy;
- migration guidance and deprecation windows;
- usage analytics or inventory scans;
- a process for product exceptions;
- regular review with real product teams and users.

Governance should enable justified variation, not force every interface into one visual template.

## 12. Release Evidence Checklist

Use this as a **release evidence record**, not as a substitute for the detailed guidance in earlier chapters. A checked item should point to an artifact, test result, issue, decision record, or responsible owner.

### 12.1 Foundation and Content

- [ ] Primary users, critical tasks, content owners, and failure consequences are documented.
- [ ] Information architecture and page hierarchy have been tested with representative content.
- [ ] Empty, loading, partial, error, permission-denied, offline, and destructive-action states exist where relevant.
- [ ] Long labels, translated text, large numbers, missing images, and untrusted user content have been stress-tested.
- [ ] Persuasive claims, testimonials, metrics, and comparison statements have evidence and approval.

### 12.2 Visual System

- [ ] Primitive, semantic, and component tokens have named owners and source-of-truth locations.
- [ ] Typography, spacing, color, radius, border, elevation, and motion decisions are tokenized where reuse is expected.
- [ ] Every interactive component has documented default, hover, focus, active, selected, disabled, loading, error, and read-only behavior as applicable.
- [ ] Light, dark, forced-color, high-contrast, print, and reduced-motion/transparency behavior has been evaluated where supported.
- [ ] Charts and status indicators remain understandable without hue alone.

### 12.3 Responsive and Internationalized Layout

- [ ] Layouts work at 320 CSS px width or the product's documented minimum supported viewport.
- [ ] Content reflows at 400% zoom without loss of information or two-dimensional scrolling except where an exception is legitimate.
- [ ] Components respond to their available container, not only to named device widths.
- [ ] Touch, mouse, keyboard, pen, and coarse-pointer behavior is appropriate to the supported platforms.
- [ ] Bidirectional text, longer translations, locale-sensitive dates/numbers, and font fallback have been tested when the product is internationalized.

### 12.4 Accessibility

- [ ] Target WCAG version and conformance level are recorded; legal or contractual obligations are separately identified.
- [ ] Automated checks run in CI and their limitations are understood.
- [ ] Complete keyboard operation, logical focus order, visible focus, skip/bypass mechanisms, and modal focus behavior have been manually verified.
- [ ] Screen-reader testing covers representative flows and dynamic announcements.
- [ ] Text alternatives, labels, names, roles, states, errors, instructions, and table relationships are programmatically available.
- [ ] Contrast, non-text contrast, text-spacing overrides, resize/reflow, target size, and motion requirements have been tested.
- [ ] No critical workflow depends on drag, hover, color, gesture, memory, or a cognitive-function test without an accessible alternative where required.

### 12.5 Performance and Resilience

- [ ] LCP, INP, and CLS are measured in representative lab tests and monitored with field data when traffic permits.
- [ ] Critical fonts and images have explicit loading, sizing, fallback, and failure strategies.
- [ ] Decorative blur, transparency, animation, video, and 3D effects degrade gracefully on constrained devices.
- [ ] The interface exposes meaningful loading, stale-data, retry, offline, and synchronization states.
- [ ] Third-party scripts and embeds have owners, budgets, consent behavior, and removal criteria.

### 12.6 Quality, Governance, and Release

- [ ] Component stories or equivalent fixtures cover supported variants, content extremes, and themes.
- [ ] Interaction, accessibility, visual-regression, and browser tests cover critical paths.
- [ ] Remaining defects and exceptions are documented with severity, owner, mitigation, and review date.
- [ ] Design and code documentation match the released implementation.
- [ ] Analytics and user-feedback plans measure the intended outcome without dark patterns or unnecessary data collection.
- [ ] Deprecation, migration, rollback, and post-release monitoring plans exist for material system changes.

## 13. Tools & Research Methods

Choose tools according to the question being tested; no single tool proves usability, accessibility, visual quality, or performance.

### 13.1 Design and System Authoring

| Tool or category | Appropriate use |
|:---|:---|
| **Figma and comparable design tools** | Interface composition, variables/tokens, prototypes, libraries, and collaboration |
| **Tokens Studio / Style Dictionary or equivalent pipelines** | Token transformation and delivery across code platforms; validate output against the DTCG format you actually support |
| **Storybook** | Component documentation, isolated states, interaction tests, accessibility checks, and visual-review workflows |
| **Penpot or other open tools** | Open-source or self-hosted collaborative design workflows |

### 13.2 Color, Typography, and Layout

| Tool | Appropriate use |
|:---|:---|
| **WebAIM Contrast Checker / browser DevTools** | WCAG 2.x contrast calculation; still test real states and backgrounds |
| **Stark and comparable plugins** | Early accessibility review inside design tooling |
| **OKLCH tools** | Perceptual palette exploration; gamut mapping and contrast still require validation |
| **Utopia** | Generating fluid type and spacing scales as starting points |
| **Wakamai Fondue** | Inspecting font axes, OpenType features, metadata, and character coverage |
| **Every Layout** | Studying resilient intrinsic-layout patterns rather than copying device-specific compositions |

### 13.3 Accessibility and Interaction Testing

| Tool | Appropriate use |
|:---|:---|
| **axe-core / axe DevTools** | Automated detection of a subset of accessibility failures |
| **Accessibility Insights** | Guided automated and manual assessment workflows |
| **NVDA, JAWS, VoiceOver, TalkBack** | Testing screen-reader behavior on supported platform combinations |
| **Chrome/Edge/Firefox/Safari DevTools** | Accessibility tree, contrast, rendering, network, performance, and device emulation |
| **Playwright** | Browser automation, keyboard flows, screenshots, accessibility-tree snapshots, and axe integration |
| **WAVE / HTML_CodeSniffer / Pa11y** | Supplementary page-level checks; results still require human interpretation |

### 13.4 Performance and Visual Quality

| Tool | Appropriate use |
|:---|:---|
| **Lighthouse** | Repeatable lab diagnostics, not a substitute for field data |
| **PageSpeed Insights / Chrome UX Report** | Origin or URL-level field data when sufficient traffic exists |
| **WebPageTest** | Detailed loading waterfalls, filmstrips, device/network profiles, and repeat-view tests |
| **Chromatic, Percy, BackstopJS, Playwright screenshots** | Visual-regression review with an explicit approval process |
| **Real-device testing** | Input, viewport, font, color, browser-chrome, and performance behavior that emulation can miss |

### 13.5 Research and Validation

Use interviews, contextual inquiry, usability testing, card sorting, tree testing, first-click testing, analytics, support data, controlled experiments, and accessibility testing with disabled participants as appropriate. Select methods from the uncertainty and risk—not from tool popularity.

## 14. Research Basis & Further Reading

The guide was reconciled against primary standards, official platform documentation, established research, and current design-system documentation. Publication dates matter: historical studies remain useful when their scope is stated, but should not be presented as timeless universal laws.

### 14.1 Normative Standards and Specifications

- [W3C — Web Content Accessibility Guidelines (WCAG) 2.2](https://www.w3.org/TR/WCAG22/)
- [W3C WAI — Understanding WCAG 2.2](https://www.w3.org/WAI/WCAG22/Understanding/)
- [WAI-ARIA Authoring Practices Guide](https://www.w3.org/WAI/ARIA/apg/)
- [European Union — Directive (EU) 2019/882, European Accessibility Act](https://eur-lex.europa.eu/eli/dir/2019/882/oj)
- [Design Tokens Community Group — Format Module 2025.10](https://www.designtokens.org/tr/2025.10/format/)
- [WHATWG HTML Living Standard](https://html.spec.whatwg.org/)
- [CSS specifications and drafts](https://www.w3.org/Style/CSS/specs.en.html)

### 14.2 Browser and Performance References

- [MDN Web Docs](https://developer.mozilla.org/)
- [web.dev — Core Web Vitals](https://web.dev/articles/vitals)
- [Chrome UX Report](https://developer.chrome.com/docs/crux)
- [Can I Use](https://caniuse.com/) for browser-support exploration, followed by target-browser testing

### 14.3 Usability and Perception Research

- Nielsen Norman Group research on [F-shaped scanning](https://www.nngroup.com/articles/f-shaped-pattern-reading-web-content/) and [text-scanning patterns](https://www.nngroup.com/articles/text-scanning-patterns-eyetracking/)
- Stanford Web Credibility Research, including the 2002 report *How Do People Evaluate a Web Site's Credibility?*
- Lindgaard et al. (2006), *Attention web designers: You have 50 milliseconds to make a good first impression!*—evidence about rapid visual-appeal judgments, not proof that all trust or usability judgments are settled in 50 ms
- Don Norman, *The Design of Everyday Things* and *Emotional Design*
- Robert Bringhurst, *The Elements of Typographic Style*
- Ellen Lupton, *Thinking with Type*
- Josef Albers, *Interaction of Color*

### 14.4 Current Implementation Documentation

- [Tailwind CSS — Theme variables](https://tailwindcss.com/docs/theme)
- [Bootstrap 5.3 — Color modes](https://getbootstrap.com/docs/5.3/customize/color-modes/)
- [Storybook — Accessibility testing](https://storybook.js.org/docs/writing-tests/accessibility-testing)
- [Playwright — Accessibility testing guidance](https://playwright.dev/docs/accessibility-testing)

### 14.5 Companion Reference

For the histories, classifications, strengths, risks, and application guidance of named styles and design systems, see **`02-design-styles-systems.md`**. Keeping that catalogue separate prevents this practice guide from repeating the same movements and product systems.

---

> **Revision:** 2026.2 — reorganized, deduplicated, and research-corrected.
