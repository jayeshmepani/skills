# Modern Web Standards: Obsolescence, Accessibility, SEO, and Performance

Modern front-end engineering is the ongoing practice of (a) using **native semantics first**, (b) layering CSS for presentation, (c) using JavaScript for progressive enhancement, and (d) staying aligned with evolving specs and browser behavior. The goal is not “newer is always better,” but rather: **avoid features that standards bodies and platform docs mark as obsolete/deprecated**, because they increase maintenance risk and can produce broken accessibility semantics or inconsistent behavior. citeturn11search13turn5view0turn18search1

This report focuses on **(1) obsolete/deprecated HTML/CSS/JS**, **(2) accessibility-driven best practices (especially semantic HTML + ARIA)**, **(3) SEO & metadata (including JSON-LD)**, and **(4) performance techniques that connect directly to real-user metrics (Core Web Vitals)**. It is intentionally grounded in normative standards and widely-used platform documentation: entity["organization","WHATWG","html living standard group"], entity["organization","World Wide Web Consortium","web standards body"], and entity["organization","MDN Web Docs","mozilla docs site"]. citeturn2search5turn5view0turn11search13

## How standards define obsolete and deprecated in practice

In modern web standards, “obsolete” and “deprecated” are not just vibes—they have specific meanings and consequences:

HTML distinguishes between **“obsolete but conforming”** features (still allowed for compatibility but expected to trigger warnings in conformance checkers) and **non-conforming features** (entirely obsolete; must not be used). citeturn5view0

Platform documentation similarly labels features as **experimental**, **deprecated**, or **obsolete** to indicate stability and future risk, and recommends avoiding deprecated APIs even if they still work today. citeturn11search13turn0search6turn0search14

A practical interpretation used by many engineering teams:

- **Removed / non-conforming (must not use):** features explicitly listed as entirely obsolete (e.g., `<frameset>`, `<marquee>`, `<keygen>`). citeturn5view0  
- **Obsolete but conforming (use only if maintaining legacy):** features that still parse and render, but are discouraged and usually flag in validators and linters (e.g., `language` on `<script>`, presentational table attributes). citeturn5view0turn21view0  
- **Deprecated (in docs/specs):** expected to be replaced; may be dropped later, or maintained only for compatibility (e.g., CSS `clip`, many legacy DOM events). citeturn11search2turn30search0turn30search2  

This matters for accessibility and SEO because a core WCAG principle is that **information and relationships implied visually must be programmatically determinable** (e.g., using headings, lists, form labels, landmarks)—and older presentational hacks often obscure that structure. citeturn6search3turn6search17

## Obsolete and deprecated patterns in HTML, CSS, and JavaScript

### HTML features that are obsolete today

The most authoritative single “inventory” is the HTML Standard’s **Obsolete features** section: it includes removed elements, and also many once-common attributes that modern HTML expects you to replace with CSS or different markup. citeturn5view0turn21view0

A few high-impact examples (selected because they commonly still appear in legacy codebases):

**Script and style attributes that are now obsolete or redundant**

- `type="text/javascript"` on classic scripts is unnecessary; authors are encouraged to omit `type` for JavaScript, because omitting it has the same effect as specifying a JavaScript MIME type. citeturn4view0turn5view0  
- `language="JavaScript"` on `<script>` is obsolete and should be omitted. citeturn5view0  
- `type="text/css"` on `<style>` is obsolete and should be omitted. citeturn5view0  

**Linking and fragment targets**

- `name` on `<a>` is obsolete for defining fragment targets; use `id` instead. (If a legacy `name` exists, the spec notes constraints and the preference for `id`.) citeturn5view0  

**Presentational attributes replaced by CSS**

Many historically popular layout/styling attributes are explicitly marked obsolete (common examples include `bgcolor`, `align`, `cellpadding`, `cellspacing`, `width` on tables, and various old body/table attributes). citeturn21view0turn21view1  

This doesn’t mean “browsers won’t render them”—it means: modern authoring should not rely on them, because CSS is the correct layer for presentation. citeturn5view0turn18search0

**Entirely obsolete HTML elements**

The HTML Standard lists elements that are “entirely obsolete, and must not be used,” alongside recommended replacements. Representative examples include:

- `<frame>`, `<frameset>`, `<noframes>` → use `<iframe>` + CSS, or generate complete pages server-side. citeturn5view0  
- `<marquee>`, `<blink>`, `<center>`, `<font>`, `<big>`, `<tt>` → “use appropriate elements or CSS instead.” citeturn5view0turn0search14  
- `<acronym>` → use `<abbr>` instead. citeturn5view0  
- `<bgsound>` → use `<audio>`. citeturn5view0  
- `<keygen>` → use modern platform capabilities; for certificate enrollment, the spec points to the Web Cryptography API. citeturn5view0turn27search1  

### CSS features that are deprecated or risky in modern practice

CSS rarely “removes” features because the web prioritizes backwards compatibility, but several patterns are broadly considered legacy because better primitives exist or because the old ones are deprecated in documentation.

A concrete example that appears in real code (including some older “sr-only” utilities):

- The CSS `clip` property is deprecated in practice; authors are encouraged to use `clip-path` instead. citeturn11search2turn11search6  

Also important is the difference between **standardized** and **non-standard** CSS:

- Some selectors like `::-webkit-scrollbar` are explicitly labeled **non-standard** and not recommended for production unless there’s no standard alternative. citeturn31search5  
- Standard scrollbar styling exists via the CSS Scrollbars Styling module (e.g., `scrollbar-width` / `scrollbar-color`) and is now supported broadly enough to be a preferred baseline compared with WebKit-only pseudo-elements. citeturn31search8turn31search16turn31search12  

For layout, floats are not “deprecated,” but they are historically overloaded:

- MDN notes floats were introduced to allow text to wrap around images (newspaper-like layouts), and then developers started using them for general layout. citeturn26search4turn26search0  
- Modern layout systems exist specifically for layout: **Flexbox** (one-dimensional layout) and **Grid** (two-dimensional page regions). citeturn26search6turn26search2turn26search9  

When you modernize a float/table layout into Grid/Flexbox, remember accessibility: MDN’s Grid accessibility guidance warns that if you visually move items around, you should keep (or restore) a logical DOM order, because keyboard/screen reader navigation follows the source order. citeturn26search22  

Vendor prefix management is also very different now than in the early web:

- Vendor prefixes (e.g., `-moz-`, `-webkit-`) indicate browser-specific extensions; production code should not rely on prefixed-only behavior unless intentionally targeting those browsers, and the modern approach is usually “use the standardized feature, and let tools handle prefixes if needed.” citeturn31search7turn31search23  

### JavaScript and DOM APIs that are deprecated or discouraged

A useful, curated entry point is MDN’s list of deprecated/obsolete JavaScript features. citeturn11search20

High-impact examples:

- `escape()` / `unescape()` are deprecated; use `encodeURI`, `encodeURIComponent`, `decodeURI`, or `decodeURIComponent` instead. citeturn11search20turn11search8turn11search4  
- `document.write()` is strongly discouraged in modern development (MDN includes explicit warnings about avoiding it). citeturn11search1  
- Mutation Events are deprecated; MutationObserver is the intended replacement. citeturn30search2turn30search14turn20search3  
- The `keypress` event is deprecated; MDN recommends `beforeinput` or `keydown` instead. citeturn30search0turn30search16turn30search4  
- `KeyboardEvent.keyCode` is deprecated; use `KeyboardEvent.key` / `KeyboardEvent.code` where appropriate (with awareness of compatibility for `code`). citeturn30search1turn30search9turn30search19  
- Synchronous XHR on the main thread is deprecated and should be avoided in favor of async requests, because it can cause hangs/freezes. citeturn30search3  

Finally, some “modern replacements” are still in-flight:

- The Temporal API is designed to address long-standing issues with the Date object, but it remains a Stage 3 proposal as of February 2026. citeturn11search3turn11search7  
- By contrast, `Promise.withResolvers()` is already part of ECMAScript 2024 and documented as a standard convenience API. citeturn12search6turn12search0turn12search12  

## Semantic HTML and ARIA usage guide

Semantic HTML and ARIA are tightly coupled: HTML provides **native roles, states, and keyboard behavior**, and ARIA is for the cases where HTML alone cannot express the semantics of custom UI. The entity["organization","World Wide Web Consortium","web standards body"] ARIA Authoring Practices summarize this bluntly: **“No ARIA is better than Bad ARIA.”** citeturn0search12turn0search4

The ARIA in HTML spec adds a related constraint: it is **not recommended** to redundantly restate an element’s implicit role, and in many cases authors **must not overwrite** native semantics. citeturn6search0

image_group{"layout":"carousel","aspect_ratio":"16:9","query":["semantic HTML layout diagram header nav main footer aside","ARIA landmarks banner navigation main contentinfo complementary diagram"],"num_per_query":1}

### Choosing semantic structure elements

For the core layout elements you listed, the modern guidance is: use them to reflect the *meaning* of regions, not their appearance.

- `<main>` represents the dominant content of the document. A document must not have more than one `<main>` that isn’t hidden, and `<main>` provides an implicit landmark; prefer it over adding `role="main"` unless dealing with legacy browser concerns. citeturn25view0  
- `<header>` represents introductory content, often including navigational aids. citeturn6search10  
- `<nav>` represents a section whose purpose is to provide navigation links (menus, tables of contents, indexes). Not every set of links belongs in `<nav>`—reserve it for primary navigation blocks. citeturn23search0turn23search23  
- `<aside>` represents content only indirectly related to the main content—often a sidebar or callout. citeturn23search3  
- `<article>` represents a self-contained composition intended to be independently distributable/reusable (posts, product cards, comments, widgets). citeturn23search1turn23search8  
- `<section>` is for a generic standalone section that doesn’t have a more specific semantic element. MDN’s practical rule: sections should generally have a heading (with few exceptions). citeturn23search2  

These choices support both accessibility navigation (screen readers use landmarks/headings as signposts) and maintainable structure. citeturn6search13turn15search2

### Buttons, links, and “don’t fight the platform”

A common accessibility failure is using the wrong element and trying to patch it with ARIA.

- Use `<a href="…">` for navigation (it becomes a real hyperlink and is activated with Enter by default). citeturn8search1  
- Use `<button>` for actions that trigger behavior in the current page/app state. If the button is inside a form and is not intended to submit, explicitly set `type="button"` to prevent accidental form submission. citeturn8search4turn8search16  
- If you add `role="button"` to a non-button element, you must re-implement button behavior (keyboard handling, activation, focus). MDN’s ARIA button role documentation therefore recommends using native `<button>`/`<input type="button">` instead in most cases. citeturn6search4turn8search13  
- Redundant ARIA can be harmful or ignored. ARIA in HTML explicitly warns against overwriting implicit semantics, and the APG’s “No ARIA is better than bad ARIA” principle is the practical consequence. citeturn6search0turn0search12  

### When to use ARIA attributes and how `id` linkage fits in

ARIA attributes often require **ID references**. The key is to use them to create relationships that HTML can’t express or to expose state changes in custom UI.

**Accessible naming rules of thumb**

- If there is a visible label, prefer `aria-labelledby` (it reuses real text and can reference multiple elements). For classic form controls, prefer a native `<label for="…">` when possible because label-click focusing is built in. citeturn6search1turn6search5  
- Use `aria-label` when there is no appropriate visible label to reference. The APG guidance for naming landmarks and widgets follows this pattern explicitly: use `aria-labelledby` if a visible label is present; otherwise use `aria-label`. citeturn22search14  

**Descriptions (help text, requirements, errors)**

- `aria-describedby="id1 id2"` points to one or more element IDs that provide descriptive information. WCAG techniques explicitly describe it as an ID reference list of unique element IDs. citeturn22search0turn22search1  
- Prefer visible helper text + `aria-describedby` over purely hidden descriptions when feasible; WCAG techniques treat this as a robust way to attach long descriptions (especially for complex controls). citeturn22search20turn22search5  

**Common failure to avoid:** broken ID references (e.g., `aria-describedby="help"` but no element with `id="help"`). That produces “broken ARIA reference” findings in accessibility tooling. citeturn22search1turn22search15  

### Skip links and landmark navigation

Skip links are a modern best practice for accessibility and are directly connected to WCAG “Bypass Blocks”:

- WCAG SC 2.4.1 requires a way to bypass repeated content (like global navigation). One sufficient technique is adding a “skip to main content” link. citeturn15search0turn15search7  
- MDN highlights skip links as especially useful for assistive tech users because repeatedly traversing navigation can be laborious. citeturn15search1  
- MDN also notes that adding an `id` to `<main>` makes it a target for a skip link. citeturn25view0  

Example pattern:

```html
<a class="skip-link" href="#main">Skip to main content</a>

<header>
  <!-- site chrome -->
</header>

<nav aria-label="Primary">
  <!-- primary nav links -->
</nav>

<main id="main">
  <h1>Page title</h1>
  <!-- main content -->
</main>
```

The core idea—skip link + meaningful landmarks—is directly aligned with WCAG’s stated intent for bypassing repeated blocks. citeturn15search7turn25view0turn23search0  

## Accessibility requirements that strongly influence “best practices”

Accessibility best practices are not arbitrary—they map to WCAG success criteria and to the way assistive technologies interpret structure and interaction.

### Programmatic structure and relationships

WCAG SC 1.3.1 requires that information/relationships conveyed by presentation are available to assistive tech (“when the presentation format changes,” e.g., a screen reader). Semantic HTML is the primary mechanism for that. citeturn6search3turn6search17

This is a major reason why “presentational HTML” is not just stylistically outdated—it can make content relationships harder to determine programmatically. citeturn6search11turn5view0

### Keyboard, focus, and pointer target size

A modern accessibility baseline typically includes:

- **Keyboard operability** (SC 2.1.1): content should be operable via keyboard, benefiting users with no vision and those using alternative input devices. citeturn14search0  
- **Visible focus** (SC 2.4.7): users must be able to see which element has keyboard focus. citeturn14search1turn14search12  
- **Focus not obscured** is new in WCAG 2.2 (SC 2.4.11 AA). WCAG explicitly lists it among new 2.2 criteria, and the intent is that the focused component remains at least partially visible. citeturn14search4turn14search2  
- **Target size** is also new in WCAG 2.2 (SC 2.5.8 AA): targets must be at least **24×24 CSS pixels** unless an exception applies (spacing, inline, essential, etc.). citeturn29view0turn14search4  

These requirements influence design decisions (spacing, sticky headers that can cover focus, custom controls that must be keyboard accessible, etc.), and they interact strongly with performance and layout choices (for example, ensuring focus remains visible with overlays). citeturn14search2turn29view0

### Contrast rules and formulas

WCAG contrast is one of the most cited—and most misunderstood—areas. The key points are:

- The contrast ratio formula is defined as **(L1 + 0.05) / (L2 + 0.05)**, where L1 is the relative luminance of the lighter color and L2 is the relative luminance of the darker color. citeturn0search7turn28view0  
- For normal text, Level AA uses a minimum contrast ratio of **4.5:1** (chosen to compensate for typical contrast sensitivity loss). Level AAA uses **7:1**. citeturn28view0  
- For non-text UI components and graphical objects needed to understand content, WCAG 2.2 SC 1.4.11 expects a relative luminance contrast of **3:1 or greater** for the visual indicators that identify controls and states. citeturn28view1turn0search3  

Because modern sites often use subtle borders, low-contrast placeholders, and thin focus rings, contrast rules apply not just to body text but to **inputs, buttons, toggles, charts, and focus indicators**. citeturn28view1turn14search1

### Motion preferences and reducing vestibular risk

A “modern best practice” is to respect user preferences for reduced motion:

- The `prefers-reduced-motion` media feature detects whether a user has enabled reduced motion at the OS/browser level. citeturn16search2turn16search6  

In accessibility terms, the intended response is typically “reduce or remove non-essential motion,” not “disable every animation,” which can itself be harmful to usability (e.g., removing essential affordances). citeturn16search6  

### Live regions and dynamic updates

Modern web apps often change content after page load; assistive tech users need to be informed about important updates.

- `aria-live` lets authors specify how updates should be announced (depending on urgency). citeturn16search1turn16search12  
- WCAG technique ARIA19 describes using live regions / role=alert to notify assistive technologies when input errors occur. citeturn16search8  
- Implementation detail matters: MDN notes that mixing `role="alert"` with redundant `aria-live="assertive"` can cause double speaking in some assistive tech (e.g., VoiceOver on iOS). citeturn16search4  

## SEO, metadata, and structured data

### Core SEO metadata in the `<head>`

For mainstream SEO, the most stable guidance is provided by entity["company","Google","search company"] documentation (as a major search engine) and cross-platform metadata standards (Open Graph, etc.). citeturn1search0turn7search0turn7search2

Key elements and what current documentation emphasizes:

- **Meta description:** there is no fixed character limit; snippets are truncated as needed (often based on device width). citeturn1search0  
- **Robots directives:** page-level robots directives can be provided via `<meta name="robots" content="…">`, crawler-specific variants, or via the `X-Robots-Tag` HTTP header; these control indexing and snippet behavior. citeturn1search1turn1search5  
- **Canonicalization:** canonical URLs are a search engine mechanism for choosing a representative URL among duplicates; you can influence canonicalization with `rel="canonical"` and other signals. citeturn7search4turn7search0  
- **Hreflang (internationalization):** `hreflang` helps search engines understand localized variations of content. (Google explicitly notes it uses algorithms to detect language rather than relying only on `lang` or `hreflang`, but `hreflang` still provides important relationship cues across localized pages.) citeturn7search1  

For social previews, Open Graph is the dominant cross-platform metadata pattern:

- The Open Graph protocol defines fields like `og:title`, `og:image`, etc., and recommends including `og:image:alt` when you specify `og:image`. citeturn7search2  

For responsive UX (which strongly affects both SEO outcomes and accessibility), the viewport meta tag matters:

- MDN documents that the viewport meta tag influences the “actual viewport” after processing the meta tag, and that certain rigid values can cause problems on larger screens. citeturn7search3turn7search10  
- web.dev explains that using `initial-scale=1` helps ensure a 1:1 relationship between CSS pixels and device-independent pixels, especially across orientation changes. citeturn7search17  

### Structured data and JSON-LD

Structured data is a “bridge” between semantic HTML and machine-readable meaning. For search features (rich results), Google’s guidance is:

- Supported structured data formats include JSON-LD, Microdata, and RDFa; JSON-LD is widely recommended because it is often easiest to implement and maintain (provided the markup is valid and follows the feature’s documentation). citeturn1search2turn1search6  
- You should validate structured data using appropriate testing tools (e.g., Rich Results Test) and fix critical errors. citeturn1search18turn1search6  

A standard JSON-LD placement pattern is:

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "Example Inc"
}
</script>
```

This aligns with the idea that JSON-LD is “separate from user-facing code,” making it maintainable without changing visual elements. citeturn1search10turn1search6  

### “SRO” vs “SEO” in 2026

You explicitly asked for “Sro” research. The term **SRO is not a single standardized discipline**; it is used in multiple (sometimes competing) ways. In organic marketing contexts, it is used by some authors to describe evolutions of SEO toward “relevance” or AI-mediated discovery—e.g., “Search Relevance Optimization” or similar. citeturn13search1turn13search0

There is also visible pushback against constantly renaming SEO into new acronyms, arguing that the fundamentals remain the same even as surfaces evolve. citeturn13search13

From a front-end engineering perspective, the stable, technical throughline is:

- Use **semantic HTML** and **accessible structure** (so machines and assistive technologies can parse meaning). citeturn6search3turn6search13  
- Provide **high-quality metadata** (canonical, robots, hreflang where relevant) and **structured data** that matches visible content. citeturn7search0turn1search6  
- Improve **real-user experience signals**, including Core Web Vitals. citeturn2search3turn17search2  

## Media formats, responsive delivery, and bandwidth efficiency

### Modern image formats and when to use them

MDN’s image format guide provides concrete format recommendations and tradeoffs:

- AVIF (AV1 Image File Format) is described as a high-performance, royalty-free format with strong compression, transparency, animation, and high color depth support; MDN advises providing fallbacks using `<picture>` because historical support depth is lower than older formats. citeturn10view1turn9search1  
- WebP is described as an excellent choice for still and animated images with better compression than JPEG/PNG; in many cases AVIF offers slightly better compression but may have other tradeoffs (e.g., progressive rendering support differences). citeturn10view1turn9search4  
- MDN explicitly recommends formats like WebP and AVIF as performing better than PNG/JPEG/GIF for many scenarios, while still noting SVG as best for crisp resolution-independent graphics. citeturn9search16turn10view1  

### Responsive images: `srcset`, `sizes`, and `<picture>`

Responsive images are a performance feature (smaller bytes for smaller screens and DPR-aware images) and a quality feature (better sharpness where needed):

- MDN explains that `srcset` defines the set of images the browser can choose from, and `sizes` helps the browser pick the correct candidate based on layout. citeturn8search2turn8search14  
- `<picture>` chooses a compatible image by evaluating each `<source>`’s `srcset`, `media`, and `type`, and the fallback `<img>` both describes the image and provides fallback if no `<source>` matches. citeturn9search1turn8search6  

A common modern pattern for AVIF/WebP fallback:

```html
<picture>
  <source type="image/avif" srcset="hero.avif">
  <source type="image/webp" srcset="hero.webp">
  <img src="hero.jpg" alt="Descriptive alt text" width="1200" height="675" loading="lazy" decoding="async">
</picture>
```

This uses modern formats with a safe fallback chain, and includes dimensions and loading/decoding hints. citeturn9search1turn24search0turn24search8turn3search12  

### Video codecs: AV1, VP9, H.264, HEVC and practical fallback

MDN’s video codec guide is one of the clearest public references for web video choices:

- AV1 is described as an open, royalty-free codec designed for internet video, with higher compression than VP9 and H.265/HEVC and up to ~50% higher than AVC (H.264). citeturn10view0  
- MDN also notes patent/licensing realities: formats like MP4/H.264 are encumbered by patents (with H.264 patents noted as extending through at least 2027 in that MDN learning material). citeturn8search15turn10view0  

For delivery, a typical web pattern is to provide multiple sources (e.g., MP4 with H.264 for broad compatibility, plus WebM with VP9 or AV1 where supported). MDN’s media format documentation covers container/codec combinations and emphasizes using appropriate `type` (and codecs parameters) to help the browser make correct decisions. citeturn8search7turn8search11  

## Performance optimization that connects to Core Web Vitals

Performance “best practices” are most useful when tied to measured outcomes. Modern guidance usually centers on **Core Web Vitals** and the critical rendering path.

### Core Web Vitals: what to optimize for

Core Web Vitals are a set of real-user experience metrics for loading, responsiveness, and visual stability. citeturn2search3turn17search2  

Current thresholds (as documented by web.dev) are:

- LCP: good ≤ 2.5s  
- INP: good ≤ 200ms  
- CLS: good ≤ 0.1 citeturn17search2  

Google’s PageSpeed Insights documentation explains that passing an assessment for a page or origin depends on the **75th percentile** of field data being “good” for all three metrics. citeturn17search3  

### Critical rendering path and render-blocking resources

The “critical rendering path” is the sequence by which the browser turns HTML/CSS/JS into pixels—DOM, CSSOM, render tree, layout, paint. Optimizing it improves render performance. citeturn18search1  

Key implications:

- CSS is render-blocking by default: browsers wait for CSSOM construction before rendering to avoid flash of unstyled content. citeturn18search18turn18search0  
- Deferring non-critical CSS is a recognized optimization technique to improve early paint metrics like FCP. citeturn18search0  
- Lighthouse explicitly frames the goal as reducing render-blocking impact by inlining critical resources, deferring non-critical resources, and removing unused code. citeturn18search11  

### Script loading: `async`, `defer`, and modules

The HTML Standard precisely defines how async/defer affect classic and module scripts:

- For external classic scripts:  
  - `async` fetches in parallel and executes as soon as available (possibly before parsing completes).  
  - `defer` fetches in parallel and executes after parsing completes. citeturn18search3  
- For module scripts: they defer by default unless `async` is present; `defer` has no effect on module scripts. citeturn18search3turn18search2  

This is one of the simplest performance wins in legacy pages that still rely on parser-blocking scripts in the head. citeturn18search4turn18search3  

### Resource hints: preconnect, dns-prefetch, preload, prefetch

Resource hints let you inform the browser about what to connect to or fetch early.

- The W3C Resource Hints specification defines `dns-prefetch`, `preconnect`, `prefetch`, and `prerender` relationships. citeturn2search12  
- web.dev explains resource hints as a way to improve load time by informing the browser how to prioritize resources, and notes that preload and fetch priority capabilities followed earlier hints like preconnect/dns-prefetch. citeturn2search0  
- MDN gives practical constraints: `preconnect` provides benefit to future cross-origin requests, but preconnecting too many third-party domains can be counterproductive; use it for the most critical connections, and consider `dns-prefetch` for others. citeturn24search3turn24search7  
- MDN describes `preload` as declaring fetch requests for resources needed “very soon,” so they load early and are less likely to block render. citeturn24search6  
- MDN describes `prefetch` as fetching/caching resources likely needed for future navigations (often “next page” resources). citeturn24search10  

### Priority hints: `fetchpriority`

Sometimes the browser cannot infer what *you* consider most important (e.g., a hero image that is the LCP element).

- MDN documents `fetchpriority` as a developer signal to increase/decrease fetch priority for resources like images and scripts. citeturn3search2turn3search10  
- web.dev provides direct guidance for using the `fetchpriority` HTML attribute for CSS/fonts/scripts/images fetched via `link/img/script`. citeturn3search18turn24search9  

### Lazy loading and decoding hints

Lazy loading is a strategy to shorten the critical rendering path by deferring non-critical resource loads until needed. citeturn3search0turn20search13  

Native lazy loading exists:

- For images, `loading="lazy"` lazy-loads images without custom JS in many browsers. citeturn3search4turn3search12  
- For iframes, `loading="lazy"` also exists and affects how resources contribute to the page load event. citeturn3search8turn3search16  

Decoding hints:

- The `decoding` attribute/property provides a hint about whether the browser should decode the image asynchronously and whether it should block other content updates to decode first. citeturn24search8turn3search1  

### Preventing layout shifts: `width` and `height` and aspect ratio

CLS is deeply affected by images/videos without reserved space.

- web.dev explains that modern best practice is setting `width` and `height` so the browser can derive aspect ratio and reserve space, reducing or preventing layout shifts. citeturn24search11  
- MDN strongly recommends explicit width and height for all images to avoid layout shift, and highlights that it’s especially important for lazy-loaded images. citeturn24search0  
- MDN performance guidance reiterates that without width/height attributes, no placeholder space is created and reflow/repaint issues occur. citeturn24search14  

### Observers and modern APIs for efficient UI

Modern best practice is to avoid polling and heavy scroll handlers in favor of observer APIs:

- Intersection Observer enables detection of element visibility and is explicitly listed by MDN as suitable for lazy loading and infinite scrolling patterns. citeturn20search0  
- ResizeObserver reports element size changes (a performant alternative to many resize hacks). citeturn20search1turn20search4  
- PerformanceObserver allows observing performance entries as they’re recorded, supporting modern performance measurement strategies. citeturn20search2turn20search5  

### Rendering optimization with CSS: `content-visibility`

For long pages with lots of off-screen content:

- `content-visibility: auto` allows the user agent to skip rendering work (layout/paint) for off-screen content, improving initial load and interactions; web.dev notes an accessibility benefit: off-screen content remains in the DOM and accessibility tree (unlike `visibility: hidden`). citeturn16search3turn16search15  

## Tooling, auditing, and maintaining compliance over time

A “comprehensive” standard-compliant workflow usually includes all of the following, because each catches different classes of issues:

Conformance checking for obsolescence and validity matters because HTML defines obsolete features as those that should trigger warnings in conformance checkers and lists non-conforming features that authors must not use. citeturn5view0  

Lighthouse provides targeted audits that map directly to SEO and performance guidance, such as:

- canonical link validity and hreflang correctness. citeturn7search18turn7search5  
- render-blocking resources diagnostics and remediation goals. citeturn18search11  

Core Web Vitals measurement should prioritize field data:

- PageSpeed Insights documentation emphasizes that CWV assessment is based on the 75th percentile of field metrics (LCP/INP/CLS). citeturn17search3  

Accessibility validation requires both automated checks and manual testing:

- Automated checks can catch structural errors like broken ARIA references and invalid role usage (which ARIA in HTML explicitly constrains). citeturn22search15turn6search0  
- Manual validation is essential for keyboard/focus behavior, because WCAG success criteria like keyboard operability and focus visibility are fundamentally interaction-based. citeturn14search0turn14search1  

The sustainable strategy is to attach these checks to CI (linting + unit/e2e + accessibility audits) and treat “deprecated/obsolete warnings” as technical debt you actively burn down, rather than letting them accumulate until a rewrite is forced by breakage. This aligns with both standards labeling expectations and the practical “avoid deprecated/obsolete features” guidance in platform documentation. citeturn11search13turn0search6turn5view0