---
name: kma-design
description: Apply the Kiss My Apps brand (kissmyapps.com) to web pages, landings, and web apps. Cyberpunk-webpunk, Stolzl type, Emerald/Blueberry, LED-matrix hero, bento layouts. Use for any KMA web surface.
license: Complete terms in LICENSE.txt
---

# Kiss My Apps — Web Design System

A working brief for building new web products in the Kiss My Apps style: campaign sites, sub-domain landing pages, marketing micro-sites, web tools. Loads the full design system: spirit, voice, color, typography, motion, components, page archetypes, and paste-ready CSS / Tailwind / JSON token blocks.

## When to use

Invoke when the task involves any of:

- "design / build / mock / sketch a landing page (or site, or hero, or section) for [a KMA product or campaign]"
- "make it look like kissmyapps.com" / "apply the KMA brand"
- "build a web app in the Kiss My Apps style"
- "create a marketing surface for [KISS & TELL · KISS MY ADS · READY2KISS · PAY2KISS] or any other KMA product"
- "critique / audit / polish a page against the KMA design system"
- referencing tokens, fonts, or motion in the KMA brand

If the user's project is a partner-facing deck, Instagram post, or print artifact (not web), this skill still applies but defer to the brand reference for SMM rules; the web defaults below diverge from print.

## Spirit (read this first)

KMA is a builder collective, not a startup. It scaled to nine figures of ARR on its own money by shipping consumer apps that hit millions of users. The energy is **adult**, direct, confident without ceremony.

**Core beliefs that drive every visual choice:**

- **Build, scale, repeat.** Physical verbs. You build the thing, make it bigger, do it again.
- **Co-founding beats employment.** The marketing CTAs say *co-found*; *employee* does not appear.
- **Execution beats theory.** Models and decks are scaffolding; ship is the verb.
- **Bootstrap pride.** No VC, no board steering the ship. We own outcomes.
- **Consumer-scale obsession.** Apps that hit millions of users, fast, repeatedly.
- **No-bullshit support.** Mentorship and ownership, not perks.
- **Mature freedom.** Autonomy because you're a grown-up.
- **Made in Kyiv, shipped globally.** Quiet defiance under everything.

**KMA refuses:** earnest startup-fun, buzzword filler, hype without delivery, generic stock visuals, single-fold compression, apology in copy.

## Theme: ask the user, default to shipping both

The skill supports **dark** and **light** themes. The brandbook (and the live site `kissmyapps.com`) is more optimized for **dark** — that's where the LED-matrix hero, the cyberpunk-precise voice, and the Emerald-on-black CTA pattern live. Light theme is fully supported (Color Combinating rule #2 explicitly endorses it) and reads as cleaner and more document-like, but it's the secondary mode.

### Always ask before scaffolding a page

When the user invokes this skill, **ask one short question before generating code**. Do not guess silently. The default question:

> *"This skill ships dark and light themes. Three options for this build:
> **(a) Both** — page renders both, with an explicit `<html data-theme>` toggle the user can flip + respect for `prefers-color-scheme`. **Default.**
> **(b) Dark only** — single-theme implementation. The KMA brandbook is more optimized for dark; the LED-matrix hero / Emerald-on-black CTA / cyberpunk-precise voice all live here.
> **(c) Light only** — single-theme implementation. Cleaner and document-like; good for careers detail, terms, partner decks, long-form articles.
> Which do you want?"*

If the user says **"doesn't matter"** or **"you pick"**, default to **(a) Both** — ship the full token set with the `[data-theme]` toggle wired up. Don't lock the page to one theme without a reason.

### Surface guidance (use to recommend a default)

If the user says "build a landing for X" without specifying theme, gently nudge:

| Surface | Recommend |
|---|---|
| Landing / hero / campaign / product detail | **Dark** (or both, dark default) — brand voice is built around dark |
| Newsroom article body, blog post body | **Both** (article hero stays dark; body switches to light when the user toggles) |
| Careers job *detail* page | **Both** with **light default** — long-form reading |
| Terms / Privacy / Legal | **Light only** — document |
| Pricing / inquiry / contact form | **Both** with **light default** |
| Partner-facing deck rendered as a page | **Both** with **light default** |
| Print stylesheet | **Light only** |

Frame the recommendation, then still let the user choose. The brandbook's dark optimization means dark-default + light-available is the safe baseline.

### What changes between themes

- Surface background and body text colors swap.
- Inline-accent text on body switches: pure Emerald on dark bodies → Emerald-Dark `#245726` on light bodies. Same for Blueberry → Blueberry-Dark.
- CTA stays Emerald-plate-with-dark-text on **both** themes — it's the brand handshake.
- Brand accent fills (Emerald and Blueberry) do not change. Dark twins are *not* a "light variant" of the accents; they are paired text colors for Color Combinating rule #3.

See [`reference/design-system.md`](reference/design-system.md) §3 for the full decision matrix and scene sentences.

## Quick reference (the answer most of the time)

When in doubt: **chosen-theme canvas, Stolzl Heavy huge, Emerald accent, one focal moment, grain on top.**

The skill ships **three tones**: dark (default canvas), light (long-form body), paper (warm cream — for alternating metric/marquee panels inside a mostly-dark marketing page). A real KMA landing page alternates **6 – 8 dark sections with 1 – 2 paper interludes**. See §3.2 in `design-system.md`.

| Token | Dark theme | Light theme | Paper panel |
|---|---|---|---|
| Surface (`--kma-surface` / `--kma-surface-paper`) | `#1E1E20` | `#F5F5F5` | `#EFEEE7` warm cream |
| Body text | `#F5F5F5` | `#1E1E20` | `#1E1E20` |
| Inline accent on body | Emerald `#58D65E` | Emerald-Dark `#245726` | Emerald-Dark `#245726` |
| Primary CTA plate | Emerald `#58D65E` | Emerald `#58D65E` | Emerald `#58D65E` |
| Primary CTA text | `#1E1E20` | `#1E1E20` | `#1E1E20` |
| Border | `oklch(0.32 0.006 286)` | `#BBBCC4` Gray-40 | `#BBBCC4` Gray-40 |

| Token | Constant across themes |
|---|---|
| Display type | Stolzl Heavy (CSS alias `heavy`) |
| Body type | Stolzl Book (CSS alias `book`) |
| Hero size | `clamp(4rem, 7vw + 1rem, 7rem)` — 64–112 px |
| Line-height (display) | `0.92` (tight) |
| UI radius | `1px` (sharp) |
| Pill radius | `9999px` — accent words and product tags only |
| Motion easing | `cubic-bezier(0.85, 0, 0.15, 1)` (decisive ease-in-out) |
| Motion durations | `300ms / 600ms / 1200ms / 2000ms` |

CTA pattern: filled Emerald `kma-btn--primary` (uppercase Stolzl Heavy, dark text `#1E1E20`) + outlined `kma-btn--secondary` (transparent, white border on dark / dark border on light).

Hero canvas: **LED-dot-matrix** animation in Emerald, **wireframe / line-art 3D** (mesh sphere, blueprint asset), or organic Blueberry⇄Emerald gradient blob. Mix one per page only. **Never** a static stock photo as hero.

### Signature treatments to reach for

**Visual / composition:**

| Treatment | Where it lives | Section in design-system.md |
|---|---|---|
| **Pill-word inside headline** (`LET'S LAUNCH YOUR [CO-FOUNDING] FUTURE TOGETHER`) | Co-founding hero | §6.4.A |
| **Striped-letter fill marquee** on paper background (`BUILD / SCALE / REPEAT`) | Paper marquee section | §9.5.B |
| **Metric panel pair** (paper + drenched, with thin dark label bar) | About / metrics block | §11.11 |
| **Product browser** (vertical menu + card with drenched sub-plate) | Products that succeeded | §11.12 / §12.7 |
| **Hero callout** (Q&A in bottom-right of hero, glass-backed) | Hero / about block | §11.14 |
| **Active-nav green underline** (2 px Emerald bar above active item) | Top nav | §11.13 |
| **Credit byline** on 3D assets (`Create: 'feedforward.', AsishCoOp'`) | Wireframe / Blob 3D | §9.3.C |
| **Wireframe 3D + heavy grain** as analog-blueprint hero | About / narrative block | §9.3.B |
| **LED-dot-matrix hero** — three implementation tiers (static / SVG / canvas) | Hero with dot texture | §9.2 |

**Interactive:**

| Treatment | Where it lives | Section in design-system.md |
|---|---|---|
| **Stroked link** with underline scaling from left | Nav, footer links, inline | §11.15 |
| **Multi-layer card hover reveal** (bg + image + logo darken + dot pattern) | Feature cards | §11.5 |
| **Row invert hover** (`.row` + `.row--inverted`) | Job listings, careers strip | §11.16 |
| **Button hover** — text → `--section-color`, `::after` opacity 0.5 | Primary CTAs | §11.2 |
| **Marquee pause on hover / click** (`--pauseOnHover`, `--pauseOnClick`) | Scrolling text-repeater | §11.6 |
| **Icon double-image shake** on hover (translate + rotate apart) | White-column feature icons | §11.17.A |
| **Lottie reveal** on subsection hover (`opacity 0 → 1`) | Subsections with accent animation | §11.17.B |
| **SlideUpCard** on scroll-snap engage (`scale(0.5) → 1`, translate `150vh → 0`) | Snap-triggered cards | §11.17.C |
| **Hamburger → cross morph** (0.6s cubic-bezier) | Mobile menu icon | §11.17.D |

**Motion granularity** — 8 production-verified durations: `0.05 / 0.1 / 0.2 / 0.3 / 0.4 / 0.6 / 0.8 / 1.2s`. Property-specific mapping in §10.2 (e.g. `background-color → 0.2s`, `color → 0.3s`, `clip-path → 0.8s`). Prefer property-specific transitions over generic `transition: all`.

## Reference files

Load these conditionally based on the task. Read tool against the relative path inside this skill.

| File | When to read |
|---|---|
| [`reference/design-system.md`](reference/design-system.md) | Full spec: spirit, voice, color, typography, logo, layout, visual elements, motion, components, page archetypes, copy voice, imagery, accessibility, slop test. The authoritative reference. |
| [`reference/tokens.css`](reference/tokens.css) | Paste-ready CSS custom properties. Imports `assets/fonts/fonts.css`. Drop into a `:root` layer or a global stylesheet. |
| [`reference/tokens.tailwind.css`](reference/tokens.tailwind.css) | Tailwind v4 `@theme` block. Import alongside `tailwindcss`. |
| [`reference/tokens.json`](reference/tokens.json) | W3C / Style Dictionary design tokens. For build pipelines that generate cross-platform token outputs. |
| [`assets/fonts/`](assets/fonts/) | Five Stolzl woff2 files plus `fonts.css` (`@font-face` for the `book` and `heavy` family aliases). Weights: `Stolzl-Book.woff2` (book/350), `Stolzl-Regular.woff2` (book/400), `Stolzl-Medium.woff2` (book/500), `Stolzl-Bold.woff2` (book/700), `heavy.woff2` (heavy/400, display). KMA-licensed — use only on KMA brand surfaces. |

**Default workflow when building a new KMA web app:**

1. Read `reference/design-system.md` §1 (Spirit) and §2 (Voice & lane) to align on energy.
2. Read §3 (Theme) to confirm dark canvas + scene-sentence reasoning.
3. Copy `reference/tokens.css` (or the Tailwind variant) into the project's global stylesheet.
4. Compose page from the archetype in §12 that matches your surface (landing / product / careers / newsroom).
5. Use components from §11 as primitives.
6. Run the §17 slop test before shipping.

## Hard rules (the AI-slop test, short version)

If any of these slip through, the output is not on-brand. Rework.

- ❌ Pure black/white with no grain — flat and template-looking.
- ❌ Stolzl substituted with Inter / Manrope / DM Sans / Plus Jakarta / Geist. Those are SaaS-cream reflex.
- ❌ Editorial-magazine reflex: display serif italic, drop caps, ruled separators above every section.
- ❌ Hero metric template: big number + tiny caption + gradient sparkle.
- ❌ Identical card grids (icon + heading + two-line body × six).
- ❌ Gradient text via `background-clip: text`.
- ❌ Side-stripe colored accents (`border-left: 4px solid`).
- ❌ Glass card with no purpose.
- ❌ Modal as the first thought for any interaction.
- ❌ Three+ brand colors at equal weight on one page.
- ❌ Em dashes in body copy. Allowed only in Q&A constructions (`— How?` `— Result?`).
- ❌ Static stock-photo hero. KMA hero is generative (LED-matrix / 3D blob / animated canvas).

## Brand permissions (take them — don't hedge)

- Ambitious first-load motion (orchestrated reveals, glitch-in entrances).
- Single-purpose viewports. Long scroll, scroll-snap, 13-viewport pages.
- Typographic risk: Stolzl Heavy at 110 px; one word as the hero; stacked overlapping text; stroke-only headlines.
- Unexpected color strategies: drenched Emerald section; Blueberry-on-Black hi-fi; per-page accent rotation via `--section-color`.
- Art direction per section: different sections, different visual worlds.
- Imagery as canvas: real photos treated heavily, or LED-matrix, or fake-3D blobs.

## Voice samples

For copy inspiration. Don't copy verbatim; sample the rhythm.

- "AI PLATFORM THAT FUELS PRODUCTS FOR MILLIONS"
- "Let's launch the future together"
- "— In 3 years, we became a 9-figure company purely on a bootstrap. — How? — Building a launchpad with Product Engine and M&A."
- "Got a strong idea and proven expertise, but missing a partner-in-scale?"
- "IT'S A PEOPLE THING"
- "BUILD / SCALE / REPEAT"
- "Mature Freedom — Yes, we really give freedom to create. But freedom here is not about chaos — it's about your ownership and execution."

CTA labels are short, all-caps, Stolzl Heavy: **WORK WITH US** · **CO-FOUND WITH US** · **EXPLORE ENGINE** · **SEE OPEN ROLES** · **EXPLORE MORE CONTENT**.

## Output expectations

When generating code or design output for KMA:

- **Ask the theme question first** (see the Theme section above). Default suggestion is "both with toggle". Do not scaffold a page until you've offered the dark / light / both choice.
- If shipping **both**: include the full `tokens.css` (it has the swappable semantic tokens + `prefers-color-scheme` fallback baked in), add a visible toggle UI in the page header that swaps `<html data-theme="dark"|"light">`, and persist the choice in `localStorage` so the user's pick survives reloads.
- If shipping **single-theme**: set `<html data-theme="dark">` (or `light`) explicitly so other CSS won't trip on `prefers-color-scheme`. Skip the toggle UI.
- Use the semantic tokens (`--kma-surface`, `--kma-text`, `--kma-accent`, etc.) in components — they swap automatically between themes when both are shipped. Use raw palette names (`--kma-blueberry`, `--kma-emerald`) only when the color must NOT theme-switch.
- Use the `kma-` prefix on all custom properties to avoid collisions.
- Ship real working code (HTML / CSS / React / Vue). No placeholder `<div>` blocks where a real component should be.
- Respect `prefers-reduced-motion`. Disable the LED canvas, glitch, distortion, parallax, and large entrance choreography when the OS flag is set.
- Cap body line length at 65–75 ch (especially in light theme — long-form bodies live there).
- Use `clamp()` for fluid heading sizes; never hard-code px on display type.
- Match implementation complexity to the aesthetic vision. On dark hero pages, the LED-matrix is voice, not decoration — skipping it makes the page read as a downgrade. On light long-form pages, restraint is voice — over-decorating breaks the document mood.
