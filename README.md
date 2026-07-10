# Web Design & Development Reference Library (2025–2026)

A four-document reference library for modern web design theory, visual styles, technical standards, and native browser capabilities.

---

## Library overview

| File | Focus | Best for |
|------|-------|----------|
| [`01-design-theory-practice.md`](01-design-theory-practice.md) | Color, typography, spacing, layout, product/admin and marketing UI, accessibility, tokens, testing | Designers and developers building interfaces |
| [`02-design-styles-systems.md`](02-design-styles-systems.md) | Visual styles, design systems, methodologies, psychology, style selection | Style decisions and design-system architecture |
| [`03-standards-compliance.md`](03-standards-compliance.md) | WCAG, ARIA, SEO, structured data, performance, delivery, pre-launch checks | Compliance, accessibility, SEO, and performance work |
| [`04-modern-features-2026.md`](04-modern-features-2026.md) | Modern HTML/CSS/JS patterns plus a 147-feature platform catalogue (§16) | Native implementation and Baseline/support lookups |

**Edition:** July 2026 · **Catalogue snapshot:** 10 July 2026 (Web Features 3.32.0)

---

## Documents

### 01 — Design Theory & Practice

**Title:** Design Theory & Practice for Web Interfaces

| Section | Topics |
|---------|--------|
| 1 | Executive summary |
| 2 | Gestalt, hierarchy, balance, contrast, scanning patterns |
| 3 | Color theory, harmony, semantic palettes, light/dark |
| 4 | Typography systems, scales, fluid type, font performance |
| 5 | Spacing grids, CSS Grid/Flexbox, breakpoints, reflow |
| 6 | Product, admin, and dashboard design |
| 7 | Public-facing and marketing-site design |
| 8 | Accessibility and inclusive design |
| 9 | Design tokens and implementation contracts |
| 10–12 | Testing, workflow/governance, release checklist |
| 13–14 | Tools, research methods, further reading |

### 02 — Design Styles & Systems

**Title:** Web Design Styles, Systems, Psychology & Implementation

| Part | Topics |
|------|--------|
| I | Classification, evidence labels, selection framework, history |
| II | 30+ visual/interaction styles (skeuomorphism through anti-design) |
| III | Platform design systems (Material 3, HIG, Fluent 2, Carbon, Polaris, …) |
| IV | Atomic Design, CSS architecture, tokens, Storybook |
| V | Psychology, perception, trust |
| VI | Evaluating accessibility across styles |
| VII | Emerging directions (adaptive UI, agents, spatial, sustainability) |
| VIII | Decision frameworks and implementation playbook |

### 03 — Standards & Compliance

**Title:** Modern Web Standards — Master Reference (2026)

| Section | Topics |
|---------|--------|
| 1–2 | Philosophy; WCAG 2.2, EAA, legal context |
| 3–4 | Obsolete HTML; semantic HTML, forms, tables |
| 5–6 | ARIA roles/states/patterns; implementation patterns |
| 7–8 | SEO, crawl control, AI search features; JSON-LD |
| 9–10 | Modern CSS/JS practices and main-thread health |
| 11–12 | Media and codecs; critical rendering path, resource hints |
| 13–15 | Observer APIs and platform features; Core Web Vitals; delivery/CDN/offline |
| 16–18 | Testing/CI; full HTML template; pre-launch checklist |

### 04 — Modern Features (2025–2026)

**Title:** The Complete Modern HTML/CSS/JavaScript Master Guide

| Section | Topics |
|---------|--------|
| 1 | Native-first philosophy and adoption model |
| 2–4 | CSS architecture, units/layout/masonry, math/conditionals |
| 5–7 | Color/materials, typography, forms and native controls |
| 8–10 | Animation/scroll/view transitions; a11y/focus; dialog, popover, invokers |
| 11–13 | Modern JavaScript; Web Components, WebGPU, File System, platform APIs; performance |
| 14–15 | Experimental notes; Baseline matrices and adoption guidance |
| **16** | **Authoritative web platform catalogue** (1 Jan 2025 → 10 Jul 2026): **147** normalized features, C/F/S versions, Baseline dates, recent deltas, beta watchlist |

Prefer stable/Baseline features for hard dependencies. Feature-detect limited APIs and progressive-enhance.

---

## How the documents work together

```
Requirements
    │
    ▼
02  Choose visual style & design system
    │
    ▼
01  Apply color, type, spacing, layout, product patterns
    │
    ▼
03  Meet WCAG, SEO, performance, and delivery standards
    │
    ▼
04  Implement with modern native features; verify support in §16
```

Use them as a searchable reference, not as a cover-to-cover curriculum.

---

## Quick start

**Designers**

1. `01` — fundamentals  
2. `02` — style and system choices  
3. `03` — accessibility requirements  

**Developers**

1. `04` — modern patterns and support catalogue (§16)  
2. `03` — compliance and performance  
3. `01` — design collaboration details  

**Design-system architects**

1. `02` — systems, methodologies, decision frameworks  
2. `01` — tokens and implementation contracts  
3. `03` — compliance baseline  

---

## Common use cases

| Goal | Start here |
|------|------------|
| Admin dashboard | `01` §6 · `01` §3 · `03` §9 · `04` §2 (`@layer`, tokens) |
| Marketing site | `01` §7 · `01` §2.11 · `03` §7 · `04` §8 (scroll/view transitions) |
| Accessibility compliance | `03` §2 · `03` §5–6 · `01` §8 |
| “Is this API Baseline yet?” | `04` §16 (versions + Baseline dates) · earlier `04` sections for recipes |
| Native, dependency-light UI | `04` §§2–12 · verify limited APIs in `04` §16 · compliance in `03` |

---

## File details

Sizes measured on disk (bytes ÷ 1024, rounded).

| File | Size | Last updated |
|------|------|--------------|
| `01-design-theory-practice.md` | 125 KB (128,063 bytes) | July 2026 |
| `02-design-styles-systems.md` | 125 KB (127,876 bytes) | July 2026 |
| `03-standards-compliance.md` | 243 KB (248,362 bytes) | July 2026 |
| `04-modern-features-2026.md` | 214 KB (219,237 bytes) | 10 July 2026 |

---

## External resources

- [MDN Web Docs](https://developer.mozilla.org/)
- [WCAG 2.2](https://www.w3.org/TR/WCAG22/)
- [Web Platform Baseline](https://web.dev/baseline)
- [Web Features](https://github.com/web-platform-dx/web-features)
- [Can I Use](https://caniuse.com/)
- [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/)
- [Design Tokens Community Group](https://designtokens.org/)

---

## Tips

1. Jump to the section you need — use search (Ctrl/Cmd+F).  
2. Bookmark high-traffic sections: contrast, ARIA patterns, Core Web Vitals, `04` §16.  
3. Real projects usually need theory + styles + standards + implementation.  
4. Support tables are dated snapshots; re-check Baseline and target browsers before shipping.

---

**Last updated:** July 2026  
**Library size:** 707 KB (723,538 bytes) across the four documents  


Provided as educational and professional reference material compiled from public standards, documentation, and industry practice.
