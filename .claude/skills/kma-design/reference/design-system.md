# DESIGN.md — Kiss My Apps

A design system for building new web products in the Kiss My Apps style.
Authored from the KMA brandbook and a style audit of kissmyapps.com.

---

## 0. How to read this

This file is the working brief for any new KMA web product (campaign sites, sub-domain landing pages, marketing micro-sites, web tools). Read §1–§4 before opening a code editor; the rest is reference.

- **§1.** Spirit — who KMA is, what it stands for, why the visual rules below exist. Read this first.
- **§2–§4.** Strategy: voice, lane, theme, source-of-truth resolutions.
- **§5–§7.** Identity tokens: color, type, logo. Non-negotiable.
- **§8–§11.** Construction: layout, visuals, motion, components.
- **§12.** Page archetypes — how to compose a new page from primitives.
- **§13.** Copy voice with real samples.
- **§14–§15.** Imagery, accessibility.
- **§16.** Paste-ready tokens (CSS / Tailwind / JSON).
- **§17.** The slop test — last gate before shipping.

When in doubt: dark canvas, Stolzl Heavy huge, Emerald accent, one focal moment, grain on top. That is most of the answer most of the time.

---

## 1. Spirit

KMA is a **builder collective**, not a startup, not an agency, not a fund. It scaled, on its own money, to nine figures of ARR by shipping consumer apps that hit millions of users. Now it co-founds with other people's ideas too.

The energy is **adult**. Direct. Confident without ceremony. The site doesn't try to charm you with a team-photo carousel; it states the numbers, makes a joke about the company name, and walks away. If you're serious, you'll come back. That's the contract.

### 1.1 Core beliefs

**Build, scale, repeat.** Three words on the wall, in Stolzl Heavy at A1 scale. Not *ideate, validate, pivot.* Not *growth-hack, optimize, scale.* The verbs are physical. You build the thing. You make it bigger. You do it again with the next thing.

**Co-founding beats employment.** Everyone is a co-founder of something. People bringing ideas co-found a product. People bringing skills co-found a team. The verb on the marketing CTAs is *co-found*; the word *employee* does not appear on the public site.

**Execution beats theory.** "Bold ideas transform into millions of customers, bold technologies and groundbreaking results only through dedication and delivery." Models, decks, and frameworks are scaffolding; ship is the verb that matters.

**Bootstrap pride.** "In 3 years, we became a 9-figure company purely on a bootstrap." No VC, no board steering the ship. The implicit boast: we'd rather own the outcome.

**Consumer-scale obsession.** The audience is people who want millions of users. Not indie hackers with side projects. Not enterprise sales cycles. Apps that hit consumer-scale numbers, fast, repeatedly.

**No-bullshit support.** "We're here to make cool things together, so you'll receive support and mentorship from day one." The promise is mentorship and ownership, not perks. Free lunches don't show up on the careers page.

**Mature freedom.** "Freedom is not about chaos — it's about your ownership and execution." Translation: you get autonomy because you're a grown-up. If you can't ship, the freedom evaporates.

**Made in Kyiv, shipped globally.** Headquarters Kyiv. Office Warsaw. C-suite scattered across Europe. The work happens during a war, from a country at war. There's a quiet defiance under everything, and the visual language — cyberpunk, glitch, dot-matrix — is the echo of it. None of it is decorative.

### 1.2 What KMA respects

- **A shipped product over a perfect pitch.** Show the app.
- **Numbers stated plainly.** "80% success rate" lands harder than "industry-leading success metrics."
- **Punk technical taste.** ZX Spectrum, demoscene, arcade LED, hacker terminals. Not Helvetica Neue and `#f9fafb` backgrounds.
- **Bilingual humans.** Ukrainian, Russian, English, Polish — all show up in copy without apology.
- **Operators, not hopefuls.** "Got a strong idea and proven expertise" is who the pitch is aimed at.
- **Long-scroll attention.** The site expects readers to scroll 13 viewports of content. It gives that attention the same respect.

### 1.3 What KMA refuses

- **Earnest startup-fun.** No "we're a fun bunch of folks" energy. No founder-in-hoodie photos. No mascots.
- **Buzzword filler.** "Empowering businesses to leverage synergies" is the opposite of the voice.
- **Hype without delivery.** Ambition is fine; ambition without numbers behind it isn't.
- **Generic-stock visuals.** Diverse-team-high-fives, finance-charts-with-rising-arrows, strawberry-stock-photos. Banned on sight.
- **Single-fold compression.** Cramming the whole pitch into a half-screen hero. Long scroll is the voice.
- **Apology in copy.** No "we hope this is helpful," no "would love to hear from you." Direct address, declarative sentences.

### 1.4 Visual implications

This spirit drives every choice below. Without it, the file collapses into "tasteful dark dashboard with a green accent."

- **Dark canvas** because punk-technical taste reads as adult and confident; light SaaS-cream reads as earnest.
- **Stolzl Heavy at 110 px** because confidence speaks in big committed type; modest type reads as apologetic.
- **LED-dot-matrix hero** because the visual DNA is arcade / demoscene / hacker, not Webflow templates.
- **Emerald on black** as the canonical CTA because it punches like a green LED on a switched-on machine.
- **Sharp 1 px corners on UI** because precision beats softness for cyberpunk-precise voice.
- **One brand color carries the page**, not three at equal weight, because confident voices commit.
- **Q&A em dashes** because the dialogue pattern is a conversation with an adult, not a marketing funnel.
- **Long scroll, scroll-snap, 13-viewport pages** because the audience reads, and the brand respects reading.

If the spirit gets lost, the design defaults to *SaaS-clean tasteful editorial* and KMA stops being recognizable. The rules in §2–§17 are downstream of this section.

---

## 2. Voice & lane

Kiss My Apps is **an AI platform company that scales B2C digital products globally**. Public-facing positioning: *AI platform that fuels products for millions.*

Three load-bearing voice words drive every visual choice:

- **Bold & rebellious.** Strong contrasts. Vivid hits of color. Daring, provocative composition.
- **Cyberpunk & webpunk.** Classic clean product design fused with digital noise: dither, pixel, distortion, holographic edges, LED-matrix.
- **Professional with passion.** Unexpected layouts, asymmetric compositions, ironic and playful elements that break SaaS-template defaults.

### 2.1 Aesthetic lane

The lane is **cyberpunk-webpunk + bento + LED-matrix typography**, with references in *Pentagram's Spotify Wrapped 2022*, *Daily Type / Type Hike* poster work, *Sucklord-style* distorted-glyph display type, and the acid-display-on-bento-grid current.

**Lanes KMA is NOT in:**

- Editorial-typographic (Klim / Stripe / Notion: display-serif italic, tracked uppercase metadata, ruled separators).
- Tasteful corporate SaaS (clean white, navy + lime, rounded card grids).
- Liquid-Death acid-maximalism (close cousin but louder and dumber — KMA keeps the minimalist scaffolding under the chaos).
- Brutalist-Swiss (visible grid as voice). Bento is not a Swiss grid.

If a draft could fit any of those four lanes, restart.

### 2.2 Use / avoid at a glance

| Use | Avoid |
|---|---|
| Editorial-scale typography (Stolzl 72 – 200 px). | Hero-metric template (big number + tiny caption + gradient sparkle). |
| Bento composition with deliberate corner-radius hierarchy. | Same-sized card grids repeated endlessly. |
| Photo with bitmap / posterize / distort treatment. | Stock-photo SaaS-cream. |
| Brand-color organic gradients **or** LED-dot-matrix animations as background canvas. | Gradient text (`background-clip: text`). |
| Grain (PNG noise, Soft Light) on imagery + plates. | Grain overlaying typography. |
| Dither / pixel / ASCII / glass-morph as deliberate vibe markers. | Decorative glass / blur with no purpose. |
| Fake-3D objects as focal accent (one per composition). | A grid of 3D objects as decoration. |
| Bilingual cuts (`in the тоР-5`). | Sanitized monolingual corp-speak. |
| Layered/stacked text experiments (BUILD over SCALE over REPEAT). | Single centered hero with subtitle stack. |

---

## 3. Theme

KMA uses **three theme tones**: dark, light, and paper. They are not a stack-rank — they are **panels you alternate inside a single page** to control rhythm. A landing page that's 100% dark reads as monotone; a landing page that alternates dark-paper-dark-paper-Blueberry-dark reads as a real KMA marketing page.

The brandbook is **more optimized for dark** (LED-matrix hero, cyberpunk-precise voice, Emerald-on-black CTA all live there). But light and paper sections are first-class supporting tones that show up across the live site in metric panels, marquee blocks, and document surfaces.

### 3.1 The three tones

| Tone | Token | Hex (approx) | Where it lives |
|---|---|---|---|
| **Dark** | `--kma-black` | `#1E1E20` | Default canvas. Heroes, navigation, product detail, narrative body. |
| **Light** | `--kma-white` | `#F5F5F5` | Long-form bodies (careers detail, terms, articles), partner decks, light-mode toggle. |
| **Paper** | `--kma-paper` | warm cream, `oklch(0.945 0.005 80)` ≈ `#EFEEE7` | **Alternating panels** inside a dark page: metric callouts, marquee/text-repeater blocks, occasional drenched-light sections. Reads as printed paper. |

Paper is **warm** — not cool-grey white. It tints toward yellow/cream, not toward blueberry. Mixing paper and white on the same page reads as a mistake; pick one as your "light side" and stay with it.

### 3.2 Two operating modes

**Mode A — Single tone (the whole page)**

The page is dark **or** light **or** paper end-to-end. Use for:
- Dark: marketing landings with LED-matrix hero, product detail pages.
- Light: terms, privacy, legal, long-form careers detail.
- Paper: rare — partner-facing one-pagers when the document mood is the point.

**Mode B — Alternating sections (most landing pages)**

The page is **predominantly dark** with **paper or drenched-color panels** punched in between. The live `kissmyapps.com` does this. Example flow:

1. Dark hero (LED-matrix + headline)
2. Dark about (wireframe 3D + Q&A callout)
3. **Paper metric panel pair** (`130M+ Users` + `X3 YoY` — see §11.11)
4. Dark product engine title
5. Dark product feature cards
6. **Paper marquee** (`BUILD / SCALE / REPEAT` — see §9.5)
7. Dark products-that-succeeded section
8. Dark co-founding hero (pill-word treatment — see §6.4.A)
9. Dark people / values
10. Dark careers index
11. Dark newsroom strip
12. Dark footer

Pattern: **6–8 dark sections separated by 1–2 paper interludes**. The paper sections *earn* their place — they slow the eye, anchor a fact, give the dark sections breathing room.

### 3.3 Mental scenes (run these before picking a mode)

**Dark scene:** an app-studio founder is scrolling on a phone at full brightness in a mid-day office. The KMA page appears: jet-black canvas with an Emerald LED-dot-matrix glowing through, one huge Stolzl headline, the wordmark in the corner. It **punches** because the surrounding UI chrome is light.

**Light scene:** a partner is reading a careers detail page in afternoon sunlight on a 14" laptop. Three columns of responsibilities, calm pacing, controlled accent moments. The page behaves like a serious document.

**Paper scene:** the same partner has scrolled past the dark hero and arrives at a metric panel: cream background, gigantic `130M+`, a thin dark label bar at the bottom reading "Users". It reads like a print poster torn out of a magazine and pasted into the page. The cream texture (subtle grain) is what makes it feel physical, not just "light theme".

### 3.4 Decision matrix

| Surface or section | Tone | Notes |
|---|---|---|
| Marketing landing — overall page | **Dark** | Use alternating mode (§3.2 Mode B). |
| Hero block | **Dark** | LED-matrix / wireframe 3D lives here. |
| About / company narrative block | **Dark** | Q&A callout in bottom-right (§11.14). |
| Metric panel pair | **Paper + drenched** | Always alternating — paper on left, brand-color drench on right (§11.11). |
| Marquee / text-repeater (`BUILD / SCALE / REPEAT`) | **Paper** | The marquee belongs to paper — striped letterforms read well on cream (§9.5). |
| Product engine / features | **Dark** | With drenched colored sub-plates inside cards. |
| Product showcase (vertical browser + card) | **Dark** | Card may contain a drenched colored sub-plate (§11.12). |
| Co-founding pill-word hero | **Dark** | Pill word is Blueberry-filled (§6.4.A). |
| People / values block | **Dark** | With Emerald drenched right rail. |
| Careers index | **Dark** | Marketing-flavored. |
| Careers job detail | **Light** | Long-form reading. |
| Newsroom article — hero | **Dark** | Hero rule wins. |
| Newsroom article — body | **Light** | Document mood. |
| Terms / Privacy / Legal | **Light** | Document. |
| Pricing / inquiry / contact form | **Light** | Partner-facing reading + form. |
| Print stylesheet | **Light** | Always. |
| User toggle preference | **System** | Light-eligible surfaces respect `prefers-color-scheme`. |

### 3.5 System preferences

Light-eligible surfaces (careers detail, terms, articles) respect `prefers-color-scheme: light` and ship light by default. The user toggle overrides. Dark-locked surfaces (landings, heroes, campaigns) set `[data-theme="dark"]` on `<html>` regardless of system preference — the alternating dark + paper mode does not flip to light + dark when the user prefers light. The brand voice doesn't invert.

### 3.6 What does NOT change between tones

Brand accent colors are constant. **Emerald is Emerald on dark, light, and paper.** Blueberry is Blueberry on all three. Dark twins exist for Color Combinating rule #3 (light brand-color plate + dark-twin text), not as a "light-mode version" of the accents.

What changes:
- **Surface background** swaps (dark → light → paper).
- **Body text color** swaps to maintain AA contrast.
- **Inline-accent text on body**: pure Emerald reads great on dark; on light or paper bodies, use **Emerald-Dark `#245726`** for inline emphasis (pure Emerald is too light on cream).
- **Border/divider** ramp stays neutral (Gray-40 works on all three tones).
- **CTA pattern** stays Emerald-plate-with-dark-text on all tones. The CTA is the brand handshake; it doesn't switch.
- **Grain** is mandatory on **all** colored panels (drenched, paper, even dark plates). See §9.4.

---

## 4. Sources of truth

When the brandbook and the marketing site agreed, that's the rule. When they disagreed, this file already resolved it:

- **Neutrals:** web = `#1E1E20` + `#F5F5F5` (cleaner on screens). Print/SMM keeps `#111111`/`#202020`/`#FFFFFF`.
- **UI radius:** web defaults to sharp plates (1 – 2 px); bento radii (24 – 64 px) reserved for hero/feature panels and SMM. Pills for accent words and product tags.
- **Em dashes:** banned in body copy, legal in **Q&A constructions only** (`— How?` `— Result?`).
- **Quokka:** print/SMM only. Web ships Stolzl Book + Heavy.

You do not need to re-litigate these.

---

## 5. Color

### 5.1 Strategy

Pick one before placing any color.

| Strategy | When | Spread |
|---|---|---|
| **Restrained** | Long-form partner decks, B2B contractual surfaces, careers job-detail pages. | Neutrals + 1 brand color, ≤ 10%. |
| **Committed** — **default for web** | Most landing pages, hero slides, product pages. | One saturated brand color (Blueberry or Emerald) carries 30 – 60% of the surface. |
| **Drenched** | Campaign moments, IG stories, full-bleed sections (e.g. "IT'S A PEOPLE THING" Emerald right rail). | The surface **is** the color. |
| ~~Full palette~~ | Avoid. Mixing 3+ brand colors at equal weight reads as data-viz, not voice. | — |

If your reflex answer is "Restrained because that's safe," reach for Committed.

### 5.2 Neutrals

| Token | HEX | OKLCH | Use |
|---|---|---|---|
| `--kma-black` | `#1E1E20` | `oklch(0.230 0.004 286)` | Default web background. Dark plates. Body text on light plates. |
| `--kma-white` | `#F5F5F5` | `oklch(0.962 0.000 0)`   | Body text on dark. Light plates. |
| `--kma-gray-25` | `#DFDFE0` | `oklch(0.892 0.002 286)` | High-emphasis dividers on dark, secondary text on light chips. |
| `--kma-gray-40` | `#BBBCC4` | `oklch(0.770 0.012 280)` | Placeholder text, inactive labels, hairlines. |
| `--kma-gray-60` | `#C8CAD0` | `oklch(0.819 0.010 270)` | Hover plate fill, soft borders. |

For **print and SMM only**, use the brandbook neutrals `#111111` / `#202020` / `#FFFFFF`. Don't mix the two scales inside a single artifact.

### 5.3 Primary brand colors

Two saturated colors plus their dark twins. These are equal in tier — alternate, don't stack.

| Token | HEX | OKLCH | Pantone | Use |
|---|---|---|---|---|
| `--kma-blueberry` | `#657FFF` | `oklch(0.642 0.191 271.4)` | 2727 U | Hero accent #1. Logo. Stroke-only headline emphasis (e.g. "CO-FOUNDING" wordmark moment). Inline noun emphasis on white body. |
| `--kma-emerald`   | `#58D65E` | `oklch(0.779 0.196 144.2)` | — | Hero accent #2. CTAs. Inline-question emphasis on dark body. Drenched right-rail panels. |
| `--kma-blueberry-dark` | `#293366` | `oklch(0.341 0.090 272.5)` | — | Dark text on Blueberry plate. Dark UI on light bg. |
| `--kma-emerald-dark`   | `#245726` | `oklch(0.409 0.096 144.3)` | — | Dark text on Emerald plate. |

**Rule of one accent.** A given page elevates one of Blueberry / Emerald as its hero color. The other appears at most once per page as a chord change. The `--section-color` variable (see §11) holds the page's chosen accent.

### 5.4 Secondary palette

Use only situationally. Main colors take priority. **Don't introduce a secondary color to a web page without a reason** — the brandbook describes these for SMM, posters, and print.

| Token | HEX | OKLCH | Dark twin | Dark twin HEX |
|---|---|---|---|---|
| `--kma-light-blue` | `#66CCFF` | `oklch(0.804 0.119 232.7)` | `--kma-light-blue-dark` | `#336680` |
| `--kma-purple`     | `#AA80FF` | `oklch(0.696 0.182 296.6)` | `--kma-purple-dark`     | `#554080` |
| `--kma-pink`       | `#FF80BF` | `oklch(0.762 0.168 350.8)` | `--kma-pink-dark`       | `#804060` |
| `--kma-red`        | `#FF6767` | `oklch(0.706 0.186 23.1)`  | `--kma-red-dark`        | `#803333` |
| `--kma-orange`     | `#FFB74D` | `oklch(0.829 0.145 73.5)`  | `--kma-orange-dark`     | `#805C26` |
| `--kma-yellow`     | `#FFEA30` | `oklch(0.926 0.184 102.4)` | `--kma-yellow-dark`     | `#807518` |
| `--kma-violet-app` | `#927DFF` | `oklch(0.621 0.183 286.6)` | — | Reserved for charity / fundraiser moments and newsroom tags. |

### 5.5 Color combinating (the four legal pairings)

Every text-on-color decision must match one of these four. Anything else is undefined behavior and probably ugly.

1. **Black background + color text.** Emerald, Blueberry, or White text on `--kma-black`. Default for dark layouts.
2. **White background + color text.** Emerald, Dark Blueberry, Blueberry, or near-black text on `--kma-white`. Default for "clean partner deck" mode.
3. **Light brand color + dark twin text.** Emerald plate → Dark-Emerald text. Light-Blue plate → Dark-Blueberry text. Pair a color with its own twin.
4. **Dark brand color + light text.** Dark-Emerald plate → Emerald text. Dark-Blueberry plate → Light-Blue text. Same twin-pairing rule.

**Explicitly undefined:** black-on-Blueberry, white-on-Yellow, Purple-on-Pink, any neutral-on-neutral pair where contrast < WCAG AA. Don't.

**Hero CTA exception:** `--kma-black` text (`#1E1E20`) on a `--kma-emerald` plate is the canonical primary-button pairing, even though strictly it's not the dark-twin form. Contrast clears AA by a comfortable margin (≈ 9 : 1). Use it; it is the brand.

### 5.6 Inline color emphasis

Inline color > inline bold for accents.

- **On dark body text:** inline-Emerald a question word (`How?`, `Result?`) or a noun phrase you want to land. Q&A patterns use it heavily.
- **On light body text:** inline-Blueberry the noun phrase you want to land.
- **Hero stroke-only word:** for occasional dramatic emphasis, set a single word in Stolzl Heavy with `color: transparent` and `-webkit-text-stroke: 2px var(--kma-blueberry)` — the "CO-FOUNDING" treatment.

### 5.7 Gradients

Brand-color organic gradients are the canonical alternative-background canvas to the LED-matrix.

- Spline-shaped, asymmetric blobs. No hard banding.
- Typical stops: Blueberry → Emerald → White, or Dark-Blueberry → Blueberry → Emerald.
- Run grain on top at Soft Light blend (§8.4).
- Ship as PNG when the surface is large enough that 8-bit banding would show.
- **Never** gradient text. One solid color, emphasis via weight and scale.

---

## 6. Typography

### 6.1 Faces

| Face | Role | Weights available | Permission |
|---|---|---|---|
| **Stolzl Book** | Body, nav, links, light headlines | 400, 500 (CSS alias `book`) | Open. |
| **Stolzl Heavy** | All hero / display / CTA type | ~900 (CSS alias `heavy`) | Open. |
| **Quokka** | Print/SMM accent only | 1 display | Not used on web. |
| **Emojis** | Voice marker | Native | Open. 🇺🇦 ❤️ 👉 land as on-brand voice. |

CSS aliases: `font-family: "book", Arial, Helvetica, sans-serif;` and `font-family: "heavy", Arial, Helvetica, sans-serif;`. Don't substitute Stolzl with Inter / Manrope / DM Sans / Plus Jakarta / Geist — those are SaaS-cream reflex. Either ship Stolzl as `@font-face`, or fall back visibly to the system stack.

### 6.2 Scale

Steep, ≥ 1.5× between adjacent steps. Web body sits at 18 – 24 px; the rest builds up from there.

| Role | Face | Size (target px @ 1440 vp) | Line-height | Letter-spacing | Used for |
|---|---|---|---|---|---|
| **A1** Accent | Heavy | 96 – 120 | 0.92 | `-0.02em` | One hero word or metric per page. Sporadic, not regular. `+30`, `AI PLATFORM`. |
| **H1** Title | Heavy | 64 – 80 | 0.98 – 1.00 | normal | Main section title. Max 3 lines, then demote to H3. |
| **H3** Subtitle | Heavy or Book Medium | 32 – 40 | 1.20 | normal | Supplement to H1, secondary lines on a hero. |
| **B1** Body | Book | 18 – 24 | 1.20 – 1.40 | normal | Paragraph copy. |
| **Tag** | Heavy, uppercase | 14 – 16 | normal | `+0.04em` | Section labels, product chips. |

Ratios at the typical web bottom of each range: 96 → 64 → 32 → 18 = **1.5× / 2.0× / 1.78×**. Steep and committed.

### 6.3 Web sizes (fluid)

```css
--kma-fs-a1:  clamp(4rem, 7vw + 1rem, 7rem);          /* 64 – 112 px */
--kma-fs-h1:  clamp(2.5rem, 3vw + 1rem, 4.5rem);      /* 40 – 72 px  */
--kma-fs-h3:  clamp(1.75rem, 1vw + 1rem, 2.5rem);     /* 28 – 40 px  */
--kma-fs-b1:  clamp(1.125rem, 0.25vw + 1rem, 1.5rem); /* 18 – 24 px  */
--kma-fs-tag: 1rem;                                   /* 16 px       */
```

### 6.4 Tactics

- **Steep hierarchy is the voice.** Hero is huge, body sits small. Never pad to "feel balanced."
- **Inline color > inline bold** for accents. See §5.6.
- **All-caps** on tags, on hero A1, on H1 when it carries a slogan. Never on B1 body. Never on H3 subtitles longer than a half-line.
- **Body line length** capped at 65 – 75 ch. Sidebars run 30 – 40 ch.
- **Light text on dark** gets +0.05 – 0.10 line-height vs the same text on light. Light type reads lighter and needs breathing room.
- **Layered/stacked typography** is on-brand: three giant words rendered overlapped, one filled and two stroke-only, riffing on a single concept (`BUILD / SCALE / REPEAT`). One per page maximum. See §9.5 for the striped-fill variant.
- **Negative letter-spacing** on display type (`-0.02em`) tightens the geometry; do not exceed.
- **Stroke-only headlines** legal as occasional emphasis (see §5.6).

#### 6.4.A Inline-pill word emphasis

A signature KMA treatment: drop a **single word inside a flowing headline as a tight filled pill**, sized to wrap the word and sitting on the same baseline as the rest of the line. Production reference: the co-founding hero — *"LET'S LAUNCH YOUR `[CO-FOUNDING]` FUTURE TOGETHER"* — where `CO-FOUNDING` is a Blueberry pill with black text, breaking the all-white Stolzl Heavy line with one chord change.

**Rules:**
- One pill word per headline. Never two.
- The pill word is the **concept the headline pivots around** (`CO-FOUNDING`, `MILLIONS`, `LAUNCH`). Not a stylistic decoration on a random word.
- Pill background = Blueberry (default) or Emerald (alternate). Text inside the pill = `--kma-black`. Always the legal CTA pairing (Color Combinating #3).
- Pill is **inline-block**, not floated. Headline wraps around it naturally on narrow viewports.
- Padding sized to the headline's font-size: roughly `0.05em` top, `0.1em` bottom, `0.4em` left/right. Border-radius matches the host text size — about `0.6em`.
- Pill word matches host `line-height: 1` so it doesn't push surrounding lines apart.

**Code:**

```html
<h1 class="kma-hero">
  LET'S LAUNCH YOUR
  <span class="kma-pill-word">CO-FOUNDING</span>
  FUTURE TOGETHER
</h1>
```

```css
.kma-hero {
  font-family: var(--kma-font-display);
  font-size: var(--kma-fs-a1);
  line-height: var(--kma-lh-tight);
  letter-spacing: var(--kma-ls-display);
  color: var(--kma-text);
  text-transform: uppercase;
}

.kma-pill-word {
  display: inline-block;
  padding: 0.05em 0.4em 0.1em;
  background: var(--kma-blueberry);
  color: var(--kma-black);
  border-radius: 0.6em;
  line-height: 1;
  vertical-align: baseline;
  /* Keep within the headline's rhythm: */
  margin: 0 0.05em;
}

/* Emerald variant for variety across pages: */
.kma-pill-word--emerald { background: var(--kma-emerald); }
```

This is distinct from the stroke-only headline word (§5.6) — pill word is filled, stroke-only word is outlined. Use one or the other on a given page, never both in the same headline.

### 6.5 No-go

- No em dashes in body copy. Allowed only in Q&A constructions (`— How?` `— Result?`).
- No drop caps. KMA is not editorial-magazine.
- No tracked-uppercase metadata above every section. A single kicker = voice; repeating it as grammar = AI scaffolding.
- No script or handwritten fonts. Stolzl is the system.
- No Stolzl weights other than Book (400) and Heavy (~900) on web without updating the font-files set first.

---

## 7. Logo

### 7.1 Variants

- **Long logo** — horizontal wordmark with the M/Y superscript glyph cluster. **Primary for everything.** Use in nav, footer, social, decks.
- **Square logo** — stacked two-line version of the wordmark. Use for avatars, app-icon contexts, square ratios. Not for accent placements inside compositions.
- **No-outline (textile)** — same wordmark without the stroke. **Physical merch only.** Not for digital.

### 7.2 Approved logo color combinations

Long and Square ship in two construction modes: **filled with offset stroke** (default) and **stroke-only** (alternative). Six approved combinations:

| Mode | Fill | Stroke | Background |
|---|---|---|---|
| Filled | Blueberry | White | Black / Gray |
| Filled | Emerald | White | Black / Gray |
| Filled | Black | Black | White |
| Stroke-only | — | Blueberry | Black / Gray |
| Stroke-only | — | Emerald | Black / Gray |
| Stroke-only | — | White | Black / Gray |

The **stroke-only White on dark** combination is the canonical web-nav choice.

### 7.3 Rules

- Clearspace: one × cap-height of the `K` glyph on every side. Nothing crosses it.
- Don't put the wordmark on a busy photo without a plate beneath.
- Don't invent new fill/stroke colors.
- Don't rotate, skew, or apply effects to the wordmark itself. Grain on the plate behind is fine.

### 7.4 Minimum sizes

- Long, digital: ≥ 100 px wide (any smaller and the M/Y superscripts close up).
- Square, digital: ≥ 48 × 48 px (favicon territory).
- Print: ≥ 20 mm wide for Long; ≥ 10 × 10 mm for Square.

---

## 8. Layout

### 8.1 Grid

Web grid uses fluid margins, not fixed columns.

```css
--kma-grid-margin: 2.22rem;  /* ~36 px outer side padding */
--kma-grid-gutter: 0.56rem;  /*  ~9 px inner gutter      */
--kma-nav-h:       3.89rem;  /* ~62 px sticky nav        */
```

For content blocks below 1024 px viewport, drop margin to `1rem` and gutter to `0.5rem`. Don't add columns; let content stack.

### 8.2 Spacing rhythm

Use a base-8 modular scale:

```css
--kma-space-1: 0.25rem;  /*  4 */
--kma-space-2: 0.5rem;   /*  8 */
--kma-space-3: 0.75rem;  /* 12 */
--kma-space-4: 1rem;     /* 16 */
--kma-space-6: 1.5rem;   /* 24 */
--kma-space-8: 2rem;     /* 32 */
--kma-space-12: 3rem;    /* 48 */
--kma-space-16: 4rem;    /* 64 */
--kma-space-24: 6rem;    /* 96 */
```

**Vary spacing for rhythm.** Identical 24 px padding on every plate reads as a Bootstrap dump. Tight clusters + generous breathing room.

### 8.3 Corner radius

Three families. Match the family to the role.

```css
--kma-radius-sharp: 1px;     /* default web UI: buttons, plates, image frames */
--kma-radius-pill:  9999px;  /* accent words and product chips (KISS & TELL) */
--kma-radius-xs:    0.5rem;  /*  8 px — secondary shapes */
--kma-radius-sm:    1rem;    /* 16 px — small feature cards */
--kma-radius-md:    1.5rem;  /* 24 px — Instagram-scale plate, also legal on hero panels */
--kma-radius-lg:    2rem;    /* 32 px — feature panel */
--kma-radius-xl:    3rem;    /* 48 px — hero plate, large panel */
--kma-radius-2xl:   4rem;    /* 64 px — full-bleed hero, drenched feature */
```

Roles:

- **Sharp (1 px):** default for live UI on web — buttons, image frames, content plates. The brand voice is precise.
- **Pill (9999px):** reserved for **accent words and product tags only** (`Увага`, `500 000 ₴`, `KISS & TELL`). Never for body text containers. Never for image frames.
- **Bento (24 – 64 px):** for **framed feature content** — a hero panel, a callout card, a drenched-color section that needs to feel softer. The brandbook rule of thumb: `cornerRadius = max(width, height) / 11`. Same depth → same radius; don't mix 32 and 48 at the same level of nesting.

### 8.4 Compositional rules

- One focal element per section. A hero is one of: photo, fake-3D blob, headline-as-art, animated canvas. Not two.
- Asymmetric layouts beat centered stacks. Left rail + right content + right margin is the canonical asymmetry.
- Don't wrap every section in a container. Sections breathe to the edge of `--kma-grid-margin`.
- Nesting cap: bento-in-bento ok; bento-in-bento-in-bento not.
- **Scroll-snap** is canonical for vertical landing pages. Use `scroll-snap-type: y mandatory` on the page container, `scroll-snap-align: start` on each block.

---

## 9. Visual elements

### 9.1 Effect vocabulary

Six markers. Use one or two per composition deliberately. **Not all six.**

| Marker | What | Where |
|---|---|---|
| **Dither** | Bayer / Floyd-Steinberg 1-bit pattern. | Photo plates, background pattern fills, hero canvases. |
| **Bitmap** | 1-bit black/white halftone. | Photo treatment. Never on type. |
| **Glass morph** | Frosted glass over a brand-color gradient. | Rare and purposeful. Decorative glass is banned. |
| **Pixel** | Explicit chunky-pixel render. | Icons, text-as-art (not body type), retro-game moments. |
| **ASCII** | Monospaced text-art panels. | Low-key cyberpunk plates, code-adjacent content. |
| **Distortion** | Mesh / wave / displace warps. | Hero word, photo treatment. Noise displaces only — never on type body. |

### 9.2 LED-dot-matrix hero (build options)

A grid of green dots that morph between shapes — letters, faces, glyphs. The signature dot-matrix look. **The production homepage doesn't use a live `<canvas>` for this — verified by DOM probe.** The hero on `kissmyapps.com` is a wireframe-3D asset (§9.3.B) plus grain, not animated dots. The LED-matrix look below is **the canonical implementation for new builds** when you want the dots-morph effect, ranging from cheapest static through full animated:

#### 9.2.A Tier 1 — static dot-grain (cheapest)

A single PNG of evenly-spaced Emerald dots at ~5–10% opacity, overlaid on `--kma-black`. No JS. Good for sub-pages where the hero needs the texture but not the motion.

```css
.kma-hero--static-dots {
  background-color: var(--kma-black);
  background-image: url("../assets/textures/dots-emerald.png");
  background-size: 12px 12px;
  background-repeat: repeat;
}
```

#### 9.2.B Tier 2 — SVG dot grid with CSS-driven animation

A repeating SVG `<pattern>` of circles, animated via CSS `transform` on a wrapping group. Adds gentle motion (drift / pulse) without a JS loop.

```html
<svg viewBox="0 0 1440 900" preserveAspectRatio="xMidYMid slice"
     class="kma-hero-dots" aria-hidden="true">
  <defs>
    <pattern id="dot" width="12" height="12" patternUnits="userSpaceOnUse">
      <circle cx="6" cy="6" r="1.5" fill="var(--kma-emerald)" opacity="0.5"/>
    </pattern>
  </defs>
  <rect width="100%" height="100%" fill="url(#dot)"/>
</svg>
```

```css
.kma-hero-dots {
  position: absolute; inset: 0;
  animation: kma-dots-drift 12s linear infinite;
  will-change: transform;
}
@keyframes kma-dots-drift {
  from { transform: translate(0, 0); }
  to   { transform: translate(-12px, -12px); }
}
@media (prefers-reduced-motion: reduce) {
  .kma-hero-dots { animation: none; }
}
```

#### 9.2.C Tier 3 — full `<canvas>` morph (richest)

For pages where the hero must be a generative interactive moment: a `<canvas>` with a 2D context running a brightness field that morphs between glyphs, lightly responsive to cursor position. This is the implementation in earlier KMA experimental hero builds, kept here as the reference shape:

- `<canvas>` element behind the hero content, sized via `devicePixelRatio` for crisp dots.
- Fixed grid of small circles (7 × 4 to 12 × 8 px spacing on a 1440 viewport).
- Each cell holds a brightness value in `[0, 1]`; render the circle in Emerald at that opacity (`oklch(0.779 0.196 144.2 / a)`).
- Animate the brightness field via Perlin / simplex noise plus optional patterns (letter shapes scrolling through the grid).
- Light cursor reaction: `mouse → grid coord → boost brightness within radius`.
- **Always pause on `prefers-reduced-motion`** and on `document.hidden`.

Tier 3 is overkill for most new pages. Default to Tier 2 unless you have a specific need for cursor interaction or a glyph-morph narrative.

### 9.3 Fake 3D

Treat 3D as a focal accent — **one per composition**. Two sub-styles, pick one per page.

#### 9.3.A Blob 3D — saturated, glossy, color-overridable

- **Asset source: Endless Tool** (`https://endless.tools/`). Pull, re-color in a brand color, export to PNG.
- **Re-coloring:** brand colors are interchangeable on the same blob. Try Emerald first, then Blueberry, then a secondary.
- **Common shapes:** crystal hand, 3D heart, 3D plus, 3D flower, 3D propeller, abstract twisted blob, chromatic-edge X.
- **Best for:** product detail pages, feature cards, secondary accents inside drenched panels.

#### 9.3.B Wireframe / line-art 3D — mesh, schematic, blueprint-like

- **Asset source:** custom-rendered or stock blueprint-style assets (mesh wireframe spheres, UFO-shaped saucer schematics, isometric line-drawings). Production reference: the wireframe sphere/saucer on the about block.
- **Treatment:** Emerald or white lines on `--kma-black`, with **heavy grain overlay** so the wireframe reads as analog film still rather than a clean CAD render.
- **Best for:** hero / about / narrative blocks where the 3D is the visual canvas, not a chip-sized accent.
- **Render path:** Blender / Spline / Cinema 4D → export wireframe-only render at high resolution → apply film grain and dark vignette in post → PNG/WebP overlay.
- **Don't** mix Blob 3D and Wireframe 3D in the same composition. Different families, breaks consistency (§9.6).

#### 9.3.C Universal rules

- **Render path:** external 3D tool → PNG cutout → drop into a sharp-corner plate. **Never inline CSS 3D transforms** as a substitute. They look bad and they're not the voice.
- **One per composition.** A grid of 3D objects is decoration, not voice.
- **Credit byline** allowed (and encouraged for collaborator/Endless Tool attribution): a tiny `Create: 'feedforward.', AsishCoOp'` style overlay text on or near the 3D asset, 10–12 px Stolzl Book, low-contrast Gray-40. Keeps the line-of-credit visible without competing for attention. Position: corner of the asset's bounding box.

### 9.4 Grain

- Source: PNG noise texture (not CSS `filter`).
- Blend mode: **Soft Light**.
- Overlay on backgrounds and plates. **Never on typography** (kills legibility).
- On a flat black/white page, grain rescues it from looking like default LinkedIn carousel.

**Mandatory on all colored panels.** Drenched Blueberry, drenched Emerald, paper-cream metric panels — **all carry grain**. A flat colored rectangle without grain reads as web-template; the same rectangle with grain reads as printed material. The production site applies grain at ~5 – 12% opacity on every drenched panel, including the Blueberry metric tile in the about block.

```css
.kma-drenched-panel,
.kma-paper-panel {
  position: relative;
  isolation: isolate;
}

.kma-drenched-panel::after,
.kma-paper-panel::after {
  content: "";
  position: absolute;
  inset: 0;
  background-image: url("../assets/textures/grain.png");
  background-size: 256px;
  mix-blend-mode: soft-light;
  opacity: 0.6;
  pointer-events: none;
  z-index: 1;
}
```

### 9.5 Layered typography experiment

Once per page, take three related words and stack them with overlapping y-axis offsets, mixing different letter-fill treatments. Use Stolzl Heavy at A1 size or larger. This is the typographic-risk permission.

#### 9.5.A Plain stacked variant

Three words, one filled, two stroke-only, on a dark canvas. Best for hero/title sections that need a typographic moment without slowing the eye.

#### 9.5.B Striped letter fill — paper marquee

Signature paper-tone treatment. Three concept words (`BUILD / SCALE / REPEAT`) rendered on a cream/paper background, where the **letterforms are filled with horizontal stripes** rather than solid color. One word stays solid (the punchline word — `REPEAT` in the live site), the other two render in striped fill.

The striped fill reads as the letter forms cross-sectioned through a venetian blind, or printed through a Risograph with horizontal misregister. Density: roughly 4 – 6 px stripes alternating black/transparent (`repeating-linear-gradient(to bottom, var(--kma-black) 0 4px, transparent 4px 8px)`), clipped to the glyph shape via SVG mask or `background-clip: text` + paint-the-text-with-stripes.

**Implementation — SVG mask approach (recommended):**

```html
<div class="kma-marquee-paper">
  <span class="kma-marquee-word kma-marquee-word--striped">BUILD</span>
  <span class="kma-marquee-word kma-marquee-word--striped">SCALE</span>
  <span class="kma-marquee-word kma-marquee-word--solid">REPEAT</span>
</div>
```

```css
.kma-marquee-paper {
  background: var(--kma-paper);
  padding: var(--kma-space-12) var(--kma-grid-margin);
  font-family: var(--kma-font-display);
  font-size: clamp(6rem, 18vw, 18rem);
  line-height: 0.9;
  letter-spacing: var(--kma-ls-display);
  text-transform: uppercase;
  position: relative;
}

.kma-marquee-word--solid {
  color: var(--kma-black);
}

.kma-marquee-word--striped {
  color: transparent;
  /* Paint stripes inside the glyph: */
  background-image: repeating-linear-gradient(
    to bottom,
    var(--kma-black) 0 4px,
    transparent 4px 8px
  );
  background-clip: text;
  -webkit-background-clip: text;
}
```

This is the **one place** the gradient-text ban in §16.1 is relaxed — the striped fill is a brand-specific paint, not the SaaS gradient-text reflex. Use only inside the marquee/text-repeater context, not on regular headlines.

#### 9.5.C Rules

- **Once per page maximum.** Two marquee blocks in one page reads as a typography demo, not a brand.
- The marquee almost always sits on **paper background**, not dark. (Confirmed by the live site.)
- **No grain on the typography itself** (§9.4) — grain stays on the paper background underneath, never overlaid on the striped letters.

### 9.6 Consistency

"Don't use non-consistent graphics." Mixing flat cartoon-vector illustration with bitmap photo with custom 3D blob in one composition is the most common failure mode. **Pick one graphic family per piece.** Vector + photo together is allowed only if the photo is treated heavily (bitmap / posterize) and the vector is brand-3D.

---

## 10. Motion

### 10.1 Easing

```css
--kma-ease:           cubic-bezier(0.85, 0, 0.15, 1);  /* decisive ease-in-out — default */
--kma-ease-out-quart: cubic-bezier(0.16, 1, 0.30, 1);  /* organic ease-out for hero reveals */
```

Use `--kma-ease` for anything that has to feel mechanical and decisive: button states, link underlines, scroll-snap settle, marquee acceleration, accordion open/close. Use `--kma-ease-out-quart` for anything that should feel like it settles into place: first-load reveals, page-enter choreography, photo crossfades.

**No bounce, no elastic.** They clash with cyberpunk-precise.

### 10.2 Durations

Production uses **eight granular durations**, not three. Property-specific durations are the rule, not generic `transition: all`. Pick the duration by property type (table below), not by component.

```css
--kma-dur-tap:   0.05s;  /* position-only (.left, scroll-driven sticky) */
--kma-dur-snap:  0.1s;   /* border-radius flick, opacity flick */
--kma-dur-quick: 0.2s;   /* background-color, height, transform on small UI */
--kma-dur-fast:  0.3s;   /* color, border-color, opacity — the canonical "fast" */
--kma-dur-ease:  0.4s;   /* transform on cards, opacity-fades */
--kma-dur-mid:   0.6s;   /* hamburger animation, checkmark reveal, accordion */
--kma-dur-slow:  0.8s;   /* clip-path reveals, slideUpCard, transform on large elements */
--kma-dur-page:  1.2s;   /* scroll-snap settle, marquee tick, page-load reveal */
--kma-dur-hero:  2.0s;   /* orchestrated entrance sequences (used sparingly) */
```

**Property → duration mapping** (matches production):

| Property | Default duration | Notes |
|---|---|---|
| `color`, `border-color` | `0.3s` (`--kma-dur-fast`) | Hover state, link underline color. |
| `opacity` | `0.3s` or `0.4s` | `0.1s` for instant flickers, `0.4s` for fade-ins. |
| `background-color` | `0.2s` (`--kma-dur-quick`) | Row hover, plate hover. |
| `transform` (small UI) | `0.2s` – `0.4s` | Button press, icon shift, focus state. |
| `transform` (large elements) | `0.6s` – `0.8s` (`--kma-dur-mid` / `--kma-dur-slow`) | Card slideUp, hero translate. |
| `clip-path` | `0.8s` (`--kma-dur-slow`) | Headline reveal, image mask reveal. |
| `border-radius` | `0.1s` – `0.2s` | Plate shape morph. |
| `filter` | `0.3s` – `0.4s` | Logo brightness invert, image desaturate. |

**Prefer property-specific transitions over `transition: all`** in new code. `transition: all` is convenient but defeats the granular durations above. Production cheats on this in places (lots of `transition: all 0.3s`), but the granular spec is the right thing to copy.

### 10.3 Properties

- Animate `transform`, `opacity`, `clip-path`, `filter` (sparingly), `background-color`, `border-color`, `color`, `border-radius`.
- For collapsing/expanding regions, animate `grid-template-rows` (`0fr → 1fr`), not `height`.
- Parallax is legal on hero scroll; cap at 0.4× scroll speed.
- Scroll-snap on the page container, not on individual scroll-y containers nested inside.
- Glitch / distortion motion (`translate3d` small jitter + `clip-path` shifts) is on-voice for hero moments.
- **Never** animate width, height, margin, padding, top, or left.

### 10.4 First-load choreography

KMA can afford ambitious entrance motion. A canonical first-load sequence:

1. `0 ms`: dark canvas paints in.
2. `120 ms`: nav fades in (`opacity 0 → 1`, `--kma-dur-fast`, `--kma-ease-out-quart`).
3. `200 ms`: hero subtitle slides up 12 px and fades in.
4. `400 ms`: hero A1 reveals via `clip-path: inset(0 100% 0 0) → inset(0 0 0 0)`, `--kma-dur-slow`, `--kma-ease`.
5. `1000 ms`: LED-matrix animation begins its first morph.
6. `1400 ms`: CTAs fade in.

Total under 2 s. `prefers-reduced-motion` skips to a static final state in `<300 ms`.

### 10.5 Forbidden motion

- Endless idle wobble loops on UI elements. The hero canvas can loop; UI cannot.
- Reverse-animation on hover.
- CSS keyframe rotations on icons unless the icon represents loading.
- Auto-playing carousels with timed advance.

---

## 11. Components

Build new pages from these primitives. Each ships with the canonical tokens; deviation must be justified.

### 11.1 Nav

- Sticky, ~62 px tall, transparent background that becomes `--kma-black` with a 1 px `--kma-gray-40 / 30%` bottom border on scroll.
- Layout: left link group (Co-founding, Product Hub) · center logo (stroke-only White) · right link group (About, Career, Jobs, Newsroom) · language toggle (Eng / Українська).
- Type: Stolzl Book 16 px, color `--kma-white`, hover color `--kma-emerald`, transition `--kma-dur-fast --kma-ease`.
- Mobile breakpoint (≤768 px): collapse right group into a hamburger that opens a full-height dark drawer.

### 11.2 Buttons

Two variants: **primary** and **secondary**. Both uppercase, Stolzl Heavy.

Hover spec on the live site: text color goes to `--section-color` (per-section accent rotation, defaults to `--kma-emerald`), and a faint `::after` decorative overlay opacity fades to 0.5. Use this when the button lives inside a section that already paints `--section-color`; otherwise fall back to the Emerald-dark hover below.

```css
.kma-btn {
  position: relative;
  display: inline-flex; align-items: center; justify-content: center;
  height: 3.5rem; padding: 0 var(--kma-space-12);
  font-family: var(--kma-font-display); font-size: 1rem;
  text-transform: uppercase; letter-spacing: 0.02em;
  border-radius: var(--kma-radius-sharp);
  isolation: isolate;
  transition: background-color var(--kma-dur-quick) var(--kma-ease),
              color var(--kma-dur-fast) var(--kma-ease),
              border-color var(--kma-dur-fast) var(--kma-ease);
}
.kma-btn::after {
  /* Subtle hover-only overlay — appears on hover at 0.5 opacity */
  content: "";
  position: absolute; inset: 0;
  background: currentColor;
  opacity: 0;
  pointer-events: none;
  transition: opacity var(--kma-dur-fast) var(--kma-ease);
  z-index: -1;
}
.kma-btn:hover::after { opacity: 0.5; }

.kma-btn--primary {
  background: var(--kma-emerald); color: var(--kma-black); border: 0;
}
.kma-btn--primary:hover {
  /* Live site: text → --section-color (defaults to Emerald, so fall back to dark twin) */
  color: var(--section-color, var(--kma-emerald-dark));
  background: var(--kma-emerald-dark);
}

.kma-btn--secondary {
  background: transparent; color: var(--kma-white);
  border: 1px solid var(--kma-white);
}
.kma-btn--secondary:hover { background: var(--kma-white); color: var(--kma-black); }

.kma-btn:focus-visible {
  outline: 2px solid var(--kma-emerald);
  outline-offset: 2px;
}
```

Light-theme override (`<html data-theme="light">`): secondary button uses dark border instead of white. Primary unchanged.

### 11.3 Product / accent chip

Pill-radius, uppercase Stolzl Heavy.

```css
.kma-chip {
  display: inline-flex; padding: 0.5rem 1rem; gap: 0.25rem;
  background: var(--kma-emerald); color: var(--kma-black);
  font-family: var(--kma-font-display); font-size: 0.875rem;
  text-transform: uppercase; letter-spacing: 0.04em;
  border-radius: var(--kma-radius-pill);
}
```

### 11.4 Section block (snap target)

Each top-level page section is a snap target.

```css
.kma-section {
  min-height: 100vh; scroll-snap-align: start;
  padding: var(--kma-space-12) var(--kma-grid-margin);
  display: grid; gap: var(--kma-space-8);
  /* asymmetric default: 30% left rail, 70% content */
  grid-template-columns: minmax(0, 30%) minmax(0, 70%);
}
```

Per-section accent color: `.kma-section { --section-color: var(--kma-emerald); }` (or `--kma-blueberry`, etc.). Children that reference `--section-color` re-skin automatically.

### 11.5 Feature card

For product detail blocks (Kiss & Tell, Kiss My Ads, etc.).

**Base layout:**
- Sharp-corner plate.
- Headline H1 in Stolzl Book mixed case (e.g. "Kiss & Tell"), color `--kma-white`.
- Two-paragraph body, B1 size.
- Single `kma-btn--primary` CTA ("Explore engine").
- Optional right-rail visual: green wireframe-3D sphere, 3D blob from Endless Tool, or dot-grid excerpt.

**Hover spec (rich multi-layer reveal — production pattern `article.hoverable`):**

On hover, the entire card inverts to a light surface and several hidden layers reveal:
- Card surface flips to `--kma-white` and text color flips to `--kma-black`.
- A hidden background layer (`.kma-card__bg`) at `opacity: 0` fades to `opacity: 1` — usually a dot pattern or brand-color wash that becomes visible only on hover.
- A hidden image (`.kma-card__image`) fades in from `opacity: 0 → 1` — secondary visual that pre-loads on first paint, reveals only on hover.
- The CTA action plate inverts (dark bg → light, or vice-versa).
- The product/partner logo darkens via `filter: brightness(0)`.
- Decorative dot patterns inside the card (4×4, 6×6) shift their fill to dark.
- The card footer border darkens.

```html
<article class="kma-card kma-card--hoverable">
  <div class="kma-card__bg" aria-hidden="true"></div>
  <img class="kma-card__image" src="/products/preview.png" alt="" />
  <header class="kma-card__header">
    <img class="kma-card__logo" src="/logos/kiss-and-tell.svg" alt="Kiss & Tell logo" />
  </header>
  <div class="kma-card__body">
    <h3 class="kma-card__title">Kiss &amp; Tell</h3>
    <p>The core of the platform that combines all data gathered over the years…</p>
  </div>
  <div class="kma-card__dot-grid kma-card__dot-grid--4x4" aria-hidden="true"></div>
  <footer class="kma-card__footer">
    <a class="kma-card__action" href="/products/kiss-and-tell">Explore engine →</a>
  </footer>
</article>
```

```css
.kma-card {
  position: relative;
  isolation: isolate;
  padding: var(--kma-space-8);
  background: var(--kma-surface-elevated);
  color: var(--kma-white);
  border-radius: var(--kma-radius-sharp);
  overflow: hidden;
  transition:
    background-color var(--kma-dur-quick) var(--kma-ease),
    color           var(--kma-dur-fast)  var(--kma-ease);
}

/* Hidden layers — all positioned absolute, fade in on hover */
.kma-card__bg,
.kma-card__image {
  position: absolute; inset: 0;
  opacity: 0;
  pointer-events: none;
  transition: opacity var(--kma-dur-fast) var(--kma-ease);
  z-index: -1;
}
.kma-card__bg {
  background-image: url("../assets/textures/dots-emerald.png");
  background-size: 12px 12px;
}
.kma-card__image {
  object-fit: cover;
  filter: grayscale(0.4);
}

.kma-card__logo {
  transition: filter var(--kma-dur-fast) var(--kma-ease);
}

.kma-card__action {
  display: inline-block;
  padding: var(--kma-space-3) var(--kma-space-6);
  background: var(--kma-black);
  color: var(--kma-white);
  font-family: var(--kma-font-display);
  text-transform: uppercase;
  transition:
    background-color var(--kma-dur-fast) var(--kma-ease),
    color           var(--kma-dur-fast) var(--kma-ease);
}

.kma-card__dot-grid {
  /* dot patterns at corners — reveal pattern on hover */
  background-image: radial-gradient(circle, var(--kma-gray-40) 1px, transparent 1px);
  background-size: 8px 8px;
  transition: background-color var(--kma-dur-fast) var(--kma-ease);
}

.kma-card__footer {
  border-top: 1px solid var(--kma-border);
  margin-top: var(--kma-space-8);
  padding-top: var(--kma-space-4);
  transition: border-color var(--kma-dur-fast) var(--kma-ease);
}

/* The hover state — multi-layer reveal */
.kma-card--hoverable:hover {
  background-color: var(--kma-white);
  color: var(--kma-black);
}
.kma-card--hoverable:hover .kma-card__bg,
.kma-card--hoverable:hover .kma-card__image {
  opacity: 1;
}
.kma-card--hoverable:hover .kma-card__logo {
  filter: brightness(0);  /* logo darkens to match inverted card */
}
.kma-card--hoverable:hover .kma-card__action {
  background-color: var(--kma-white);
  color: var(--kma-black);
}
.kma-card--hoverable:hover .kma-card__dot-grid {
  background-image: radial-gradient(circle, var(--kma-black) 1px, transparent 1px);
}
.kma-card--hoverable:hover .kma-card__footer {
  border-color: var(--kma-black);
}

@media (prefers-reduced-motion: reduce) {
  .kma-card, .kma-card * { transition: none !important; }
}
```

**Rules:**
- Only one of the hidden layers (`__bg` *or* `__image`) per card — not both. Two simultaneous reveals fight for attention.
- Always provide a non-hover affordance too (the visible base card must read as a complete card without hover). The reveal is a delight bonus, not the only state that communicates value.
- Touch devices: trigger the same reveal on `:active` so the hover behavior survives without a mouse. Or treat the card as a link and skip the hover state entirely on touch.

### 11.6 Marquee / text-repeater

Horizontal scrolling tape of repeated text. Production uses the [`vue3-marquee`](https://www.npmjs.com/package/vue3-marquee) package; the CSS contract below is framework-agnostic and matches its variables so a Vue project can drop in the package directly.

**Default behavior:**
- One huge stroke-only word in Stolzl Heavy at A1 size, repeated horizontally with `--kma-space-12` spacing.
- Translates left at constant speed; loop wraps via `translateX(-50%)` modulus or via the vue3-marquee component.
- **Pauses on hover** (`--pauseOnHover: paused`) and **pauses on click** (`--pauseOnClick: paused`) — confirmed on the live site. Use these CSS variables to control state declaratively, not JS event listeners.
- `prefers-reduced-motion`: freeze the strip in place (`--pauseAnimation: paused`).

```html
<div class="kma-marquee" style="--duration: 30s; --direction: normal;">
  <div class="kma-marquee__track">
    <span class="kma-marquee__word">BUILD</span>
    <span class="kma-marquee__word">SCALE</span>
    <span class="kma-marquee__word">REPEAT</span>
    <!-- duplicate to avoid gap on loop wrap -->
    <span class="kma-marquee__word" aria-hidden="true">BUILD</span>
    <span class="kma-marquee__word" aria-hidden="true">SCALE</span>
    <span class="kma-marquee__word" aria-hidden="true">REPEAT</span>
  </div>
</div>
```

```css
.kma-marquee {
  --pauseAnimation: running;
  --pauseOnHover: running;
  --pauseOnClick: running;
  --direction: normal;
  --duration: 30s;

  overflow: hidden;
  display: flex;
  padding: var(--kma-space-12) 0;
}

.kma-marquee:hover  { --pauseOnHover: paused; }
.kma-marquee:active { --pauseOnClick: paused; }

.kma-marquee__track {
  display: flex;
  gap: var(--kma-space-12);
  flex: 0 0 auto;
  animation: kma-marquee-scroll var(--duration) linear infinite var(--direction);
  animation-play-state: var(--pauseAnimation);
}
.kma-marquee:hover  .kma-marquee__track { animation-play-state: var(--pauseOnHover); }
.kma-marquee:active .kma-marquee__track { animation-play-state: var(--pauseOnClick); }

@keyframes kma-marquee-scroll {
  from { transform: translateX(0); }
  to   { transform: translateX(-50%); }
}

@media (prefers-reduced-motion: reduce) {
  .kma-marquee { --pauseAnimation: paused; }
}

.kma-marquee__word {
  font-family: var(--kma-font-display);
  font-size: clamp(4rem, 12vw, 12rem);
  text-transform: uppercase;
  letter-spacing: var(--kma-ls-display);
  color: transparent;
  -webkit-text-stroke: 2px var(--kma-white);  /* stroke-only by default */
  white-space: nowrap;
}
```

For the **paper variant with striped letterforms** (`BUILD / SCALE / REPEAT` on cream), see §9.5.B — that's the layered-typography moment, distinct from this scrolling marquee.

### 11.7 Drenched panel

Full-bleed brand-color rail (e.g. the "IT'S A PEOPLE THING" right rail).

- Background: `--kma-emerald` (or Blueberry, depending on section accent).
- Text color: `--kma-emerald-dark` (the dark twin), or `--kma-black`.
- Padding: `--kma-space-12` all sides.
- Used for value-list content, bulleted explanations, manifesto blocks.

### 11.8 Footer

Tall (≈ 1160 px on desktop). Multi-block layout.

- **Newsroom strip** at top: scrolling carousel of recent posts with chip tags.
- **Media-logo bar:** monochrome logos of publications that have covered KMA, single row, `--kma-gray-40` color, hover to full color.
- **Sitemap:** three columns of links in Stolzl Book 16 px.
- **Address block(s):** date-block typography for the street numbers ("16 28"), followed by city / country. One block per office (Kyiv, Warsaw, Lisbon).
- **Wireframe-3D sphere** bottom-right as decorative anchor.
- **Bottom bar:** copyright, legal links, language toggle (mirroring nav).

### 11.9 Form input

```css
.kma-input {
  width: 100%; padding: 1rem; height: 3.5rem;
  background: transparent; color: var(--kma-text);
  border: 0; border-bottom: 1px solid var(--kma-gray-40);
  font-family: var(--kma-font-sans); font-size: 1.125rem;
  transition: border-color var(--kma-dur-fast) var(--kma-ease);
}
.kma-input:focus,
.kma-input:focus-visible {
  border-color: var(--kma-emerald);
  outline: none;
}
.kma-input::placeholder { color: var(--kma-gray-40); }

@supports selector(:has(*)) {
  .kma-input:user-invalid:not(:focus) {
    border-color: var(--kma-red);
  }
}
```

No filled inputs by default. The underline is the affordance. Don't introduce filled / boxed inputs — this single-line underlined input is the closest to the brand's typographic restraint.

### 11.10 Cookie banner

- Full-width sticky bottom strip.
- Background `--kma-emerald`, text `--kma-black`.
- Left: short copy ("This site uses cookies.").
- Right: dismiss CTA ("I REALISE AND ACCEPT IT") in Stolzl Heavy uppercase.
- Single dismiss action; no preferences dialog by default.

### 11.11 Metric panel pair

Two square (or near-square) panels side by side, each presenting **one giant metric** with a thin dark label bar at the bottom. The pair always alternates tones — one panel is paper/cream, the other is drenched brand color. The whole pair lives as one section in an otherwise-dark page (§3.2 Mode B).

Production reference: `130M+ / Users` (paper, dotted circle outline behind) + `X3 / YoY average growth` (Blueberry drenched, Emerald label text).

```html
<section class="kma-metric-pair">
  <article class="kma-metric kma-metric--paper">
    <div class="kma-metric__figure">130M+</div>
    <div class="kma-metric__label">Users</div>
  </article>
  <article class="kma-metric kma-metric--drenched-blueberry">
    <div class="kma-metric__figure">X3</div>
    <div class="kma-metric__label">YoY average growth</div>
  </article>
</section>
```

```css
.kma-metric-pair {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0; /* panels touch; the border between them is the dark page bg or a 2px black gutter */
  min-height: 60vh;
}

.kma-metric {
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: var(--kma-space-16);
  isolation: isolate;
}

.kma-metric--paper {
  background: var(--kma-paper);
  color: var(--kma-black);
}

.kma-metric--drenched-blueberry {
  background: var(--kma-blueberry);
  color: var(--kma-black);
}

.kma-metric--drenched-emerald {
  background: var(--kma-emerald);
  color: var(--kma-black);
}

/* Mandatory grain (§9.4) */
.kma-metric::after {
  content: "";
  position: absolute;
  inset: 0;
  background-image: url("../assets/textures/grain.png");
  background-size: 256px;
  mix-blend-mode: soft-light;
  opacity: 0.6;
  pointer-events: none;
  z-index: -1;
}

.kma-metric__figure {
  font-family: var(--kma-font-display);
  font-size: clamp(5rem, 12vw, 12rem);
  line-height: 0.92;
  letter-spacing: var(--kma-ls-display);
}

.kma-metric__label {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background: var(--kma-black);
  color: var(--kma-white);
  font-family: var(--kma-font-display);
  font-size: 1rem;
  text-transform: uppercase;
  letter-spacing: var(--kma-ls-tag);
  text-align: center;
  padding: var(--kma-space-2) var(--kma-space-4);
}

/* When the drenched panel uses Emerald accent text on the label: */
.kma-metric--drenched-blueberry .kma-metric__label {
  color: var(--kma-emerald);
}
```

**Rules:**
- **Always pairs.** A single metric panel reads as a hero metric template (banned, §16.1). Two pairs (4 panels) on the same row is also legal.
- **Alternate the tones.** Paper + drenched, never paper + paper or drenched + drenched in the same pair.
- **One metric per panel, one label.** No body copy underneath.
- **Grain on both.**
- **Dotted/dashed outline circles or other paper-print marks** are optional decoration on the paper panel — they reinforce the print-poster mood.

### 11.12 Product browser

Vertical menu of product names on the left, content card on the right that contains a dark image-plate above a drenched colored sub-plate. The pattern KMA uses for the "Products that succeeded on our platform" section.

```html
<section class="kma-product-browser">
  <nav class="kma-product-nav">
    <h2 class="kma-product-nav__title">Products that succeeded on our platform</h2>
    <ul class="kma-product-nav__list">
      <li class="kma-product-nav__item kma-product-nav__item--active">
        <span class="kma-product-nav__arrow">→</span> AI Remodel
      </li>
      <li class="kma-product-nav__item">Printer App</li>
      <li class="kma-product-nav__item">Lumify</li>
      <li class="kma-product-nav__item">Chi</li>
      <li class="kma-product-nav__item">Botan</li>
    </ul>
  </nav>
  <article class="kma-product-card">
    <div class="kma-product-card__image">
      <img src="/products/ai-remodel-thumb.jpg" alt="AI Remodel interior preview" />
    </div>
    <div class="kma-product-card__plate kma-product-card__plate--violet">
      <h3 class="kma-product-card__title">AI REMODEL</h3>
      <p class="kma-product-card__sub">#1 AI-TOOL FOR INTERIOR DESIGN</p>
      <p class="kma-product-card__tag">Interior Design +1</p>
    </div>
    <p class="kma-product-card__body">
      This app was launched twice, as the first version was ahead of both
      the market and tech. Once the moment was right, the app became the
      #1 AI-based interior design app in 3 months, based on predictions
      and signals from the Analytics Module.
    </p>
  </article>
</section>
```

```css
.kma-product-browser {
  display: grid;
  grid-template-columns: minmax(0, 30%) minmax(0, 70%);
  gap: var(--kma-space-12);
  padding: var(--kma-space-16) var(--kma-grid-margin);
  min-height: 100vh;
  background: var(--kma-black);
  color: var(--kma-white);
}

.kma-product-nav__title {
  font-family: var(--kma-font-sans);
  font-size: var(--kma-fs-b1);
  font-weight: 400;
  color: var(--kma-gray-25);
  max-width: 12em;
  margin-bottom: var(--kma-space-12);
}

.kma-product-nav__list {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  flex-direction: column;
  gap: var(--kma-space-3);
}

.kma-product-nav__item {
  font-family: var(--kma-font-display);
  font-size: var(--kma-fs-h3);
  text-transform: uppercase;
  color: var(--kma-white);
  cursor: pointer;
  transition: color var(--kma-dur-fast) var(--kma-ease);
}

.kma-product-nav__item--active {
  color: var(--kma-blueberry);
}

.kma-product-nav__arrow {
  display: inline-block;
  margin-right: var(--kma-space-2);
}

.kma-product-card {
  display: grid;
  grid-template-columns: 1fr;
  gap: var(--kma-space-6);
  max-width: 36rem;
}

.kma-product-card__image {
  aspect-ratio: 4 / 3;
  background: var(--kma-surface-elevated);
  overflow: hidden;
}

.kma-product-card__plate--violet  { background: var(--kma-violet-app); }
.kma-product-card__plate--emerald  { background: var(--kma-emerald); }
.kma-product-card__plate--blueberry { background: var(--kma-blueberry); }

.kma-product-card__plate {
  position: relative;
  padding: var(--kma-space-8);
  color: var(--kma-black);
}

.kma-product-card__plate::after {
  /* grain — same pattern as metric panel */
  content: "";
  position: absolute;
  inset: 0;
  background-image: url("../assets/textures/grain.png");
  background-size: 256px;
  mix-blend-mode: soft-light;
  opacity: 0.5;
  pointer-events: none;
}

.kma-product-card__title {
  font-family: var(--kma-font-display);
  font-size: clamp(2rem, 5vw, 4rem);
  text-transform: uppercase;
  margin: 0 0 var(--kma-space-2);
}

.kma-product-card__sub {
  font-family: var(--kma-font-display);
  font-size: var(--kma-fs-tag);
  text-transform: uppercase;
  letter-spacing: var(--kma-ls-tag);
  margin: 0;
}

.kma-product-card__tag {
  font-family: var(--kma-font-sans);
  font-size: 0.875rem;
  color: var(--kma-black);
  opacity: 0.75;
  margin-top: var(--kma-space-3);
}

.kma-product-card__body {
  font-family: var(--kma-font-sans);
  font-size: var(--kma-fs-b1);
  line-height: var(--kma-lh-snug);
  color: var(--kma-white);
}
```

**Rules:**
- **One drenched sub-plate per product card.** Each product gets its own color (AI Remodel = Violet-app, Botan = Emerald, etc.). Use the assigned product color consistently across surfaces.
- **Active state is single-color, not background-tint.** Active nav item changes color (white → Blueberry), does not get a filled background.
- The right rail can also be a wireframe-3D scene rather than a card — `kissmyapps.com` rotates between these two arrangements in the section.

### 11.13 Active-nav indicator

A short Emerald bar above the active nav item. Subtle, ~2 px tall, half the width of the label.

```html
<nav class="kma-nav">
  <a class="kma-nav__item kma-nav__item--active" href="/co-founding">Co-founding</a>
  <a class="kma-nav__item" href="/products">Product Hub</a>
</nav>
```

```css
.kma-nav__item {
  position: relative;
  display: inline-block;
  padding: var(--kma-space-2) var(--kma-space-3);
  font-family: var(--kma-font-sans);
  font-size: var(--kma-fs-tag);
  color: var(--kma-white);
  text-decoration: none;
}

.kma-nav__item--active::before {
  content: "";
  position: absolute;
  top: 0;
  left: var(--kma-space-3);
  width: 1.5rem;
  height: 2px;
  background: var(--kma-emerald);
}
```

The indicator is above the label, not below or underline. This reads as "section heading marker" rather than "hover affordance", which matches the brand's editorial vibe.

### 11.15 Stroked link

The canonical KMA in-line link — text plus a slow-growing underline that scales from left on hover. Production class: `.stroked-link`. Used on nav items, footer links, in-body link cluster.

```html
<a class="kma-stroked-link" href="/co-founding">
  <span>Co-founding</span>
</a>
```

```css
.kma-stroked-link {
  display: inline-block;
  color: inherit;
  text-decoration: none;
  font-family: var(--kma-font-sans);
}
.kma-stroked-link span {
  position: relative;
  display: inline-block;
}
.kma-stroked-link span::after {
  content: "";
  position: absolute;
  left: 0; right: 0; bottom: -2px;
  height: 1px;
  background: currentColor;
  transform: scaleX(0);
  transform-origin: 0% 50%;  /* grows from LEFT on hover */
  transition: transform var(--kma-dur-fast) var(--kma-ease);
}
.kma-stroked-link:hover span::after {
  transform: scaleX(1);
}

/* When the link is the active route — underline already present, retracts on hover */
.kma-stroked-link.is-active span::after {
  transform: scaleX(1);
  transform-origin: 0% 50%;
}
.kma-stroked-link.is-active:hover span::after {
  transform: scaleX(0);
  transform-origin: 100% 50%;  /* retracts to the RIGHT */
}

.kma-stroked-link:focus-visible {
  outline: 2px solid var(--kma-emerald);
  outline-offset: 4px;
  border-radius: 1px;
}
```

**Rules:**
- Underline always grows from left on rest-state → hover. Active state inverts: underline retracts to right.
- Single underline pixel; thicker reads as decorative.
- Don't combine with `text-decoration: underline` — the pseudo-underline is the system.

### 11.16 Job listing row (`.row` invert)

For careers job board / similar-jobs strips. Each row is a single horizontal lozenge with department / title / location / chip on the left and an arrow CTA on the right. On hover the entire row inverts (background ↔ text colors).

```html
<a class="kma-row" href="/jobs/user-acquisition-manager-meta">
  <div class="kma-row__team">Marketing Department</div>
  <div class="kma-row__title">User Acquisition Manager (Meta)</div>
  <div class="kma-row__chip">Remote</div>
  <div class="kma-row__chip">Ukraine</div>
  <div class="kma-row__action" aria-hidden="true">→</div>
</a>
```

```css
.kma-row {
  display: grid;
  grid-template-columns: minmax(0, 1.5fr) minmax(0, 3fr) auto auto auto;
  gap: var(--kma-space-6);
  align-items: center;
  padding: var(--kma-space-6) var(--kma-space-8);
  color: var(--kma-white);
  background: transparent;
  border-bottom: 1px solid var(--kma-border);
  text-decoration: none;
  cursor: pointer;
  transition:
    background-color var(--kma-dur-quick) var(--kma-ease),
    color           var(--kma-dur-fast)  var(--kma-ease);
}
.kma-row__team { font-family: var(--kma-font-sans); font-size: 0.875rem; color: var(--kma-text-muted); text-transform: uppercase; letter-spacing: var(--kma-ls-tag); }
.kma-row__title { font-family: var(--kma-font-display); font-size: var(--kma-fs-h3); text-transform: uppercase; }
.kma-row__chip {
  font-family: var(--kma-font-sans); font-size: 0.875rem;
  padding: var(--kma-space-1) var(--kma-space-3);
  background: rgba(245, 245, 245, 0);
  border: 1px solid currentColor;
  border-radius: var(--kma-radius-pill);
  transition: background-color var(--kma-dur-fast) var(--kma-ease);
}
.kma-row__action {
  font-family: var(--kma-font-display);
  background: var(--kma-emerald);
  color: var(--kma-black);
  padding: var(--kma-space-3) var(--kma-space-6);
  transition:
    background-color var(--kma-dur-fast) var(--kma-ease),
    color           var(--kma-dur-fast) var(--kma-ease);
}

/* Default rest state: dark page, light text */
.kma-row:hover {
  background-color: var(--kma-black);
}
.kma-row:hover > * { color: var(--kma-white); }
.kma-row:hover .kma-row__chip { background-color: rgba(245, 245, 245, 0.08); }
.kma-row:hover .kma-row__action { background-color: var(--kma-white); color: var(--kma-black); }

/* Inverted variant: page bg is light, row sits on white, hover flips to dark */
.kma-row--inverted {
  color: var(--kma-black);
  background-color: var(--kma-white);
  border-bottom-color: var(--kma-gray-40);
}
.kma-row--inverted:hover {
  background-color: var(--kma-black);
}
.kma-row--inverted:hover > * { color: var(--kma-white); }
.kma-row--inverted:hover .kma-row__chip { background-color: rgba(30, 30, 32, 0.08); }
.kma-row--inverted:hover .kma-row__action { color: var(--kma-white); }

.kma-row:focus-visible {
  outline: 2px solid var(--kma-emerald);
  outline-offset: -2px;
}
```

**Rules:**
- Use `.kma-row` on dark pages and `.kma-row--inverted` on paper / light pages. Don't mix on the same surface.
- The action chip flips its fill on hover too — keeps it readable in both states.
- Whole row is one anchor — entire row is the click target.

### 11.17 Microinteractions

Tiny delightful moments that show up across the site. Document them so they're consistent, not unique to whoever built each one.

**A. Icon double-image shake on hover**

Used in white-column "feature icon" cells (typically a 2-layered illustration: foreground + background image). On hover the two layers translate apart and rotate in opposite directions — playful pop without changing scale.

```html
<div class="kma-icon-shake">
  <img class="kma-icon-shake__layer kma-icon-shake__layer--1" src="/icons/box-1.svg" alt="" />
  <img class="kma-icon-shake__layer kma-icon-shake__layer--2" src="/icons/box-2.svg" alt="" />
</div>
```

```css
.kma-icon-shake { position: relative; display: inline-block; width: 4rem; height: 4rem; }
.kma-icon-shake__layer {
  position: absolute; inset: 0;
  transition: transform var(--kma-dur-ease) var(--kma-ease);
}
.kma-icon-shake:hover .kma-icon-shake__layer--1 {
  transform: translate(-8px, -10px) rotate(-16deg);
}
.kma-icon-shake:hover .kma-icon-shake__layer--2 {
  transform: translate(8px, -10px) rotate(4deg);
}
@media (prefers-reduced-motion: reduce) {
  .kma-icon-shake__layer { transition: none; }
  .kma-icon-shake:hover .kma-icon-shake__layer { transform: none; }
}
```

**B. Lottie reveal on subsection hover**

A hidden Lottie animation pre-loaded inside a subsection wrapper; on hover the wrapper makes the lottie visible (`opacity 0 → 1`). Use for small accent animations that don't deserve to run all the time. Production uses [`lottie-web`](https://www.npmjs.com/package/lottie-web).

```css
.kma-subsection .kma-subsection__lottie {
  opacity: 0;
  transition: opacity var(--kma-dur-fast) var(--kma-ease);
}
.kma-subsection:hover .kma-subsection__lottie { opacity: 1; }
```

Lottie playback should auto-loop while visible. When `prefers-reduced-motion`, replace with the lottie's first frame as a static PNG.

**C. SlideUpCard on scroll-snap engage**

When a card section snaps into view, the card content rises from below at scale 0.5 and lands at scale 1 / 0vh. Production timing: `0.8s cubic-bezier(0.85, 0, 0.15, 1)`.

```css
.kma-slide-card {
  transform: scale(0.5) translateY(150vh);
  transition: transform var(--kma-dur-slow) var(--kma-ease);
}
.kma-slide-card.is-active {
  transform: scale(1) translateY(0);
}
@media (prefers-reduced-motion: reduce) {
  .kma-slide-card { transform: none; transition: none; }
}
```

Trigger `.is-active` via `IntersectionObserver` when the section snaps (or use a scroll-snap-event listener if the browser supports it). The animation runs once per page load, not repeatedly.

**D. Hamburger → cross morph (mobile menu)**

Mobile menu icon morphs from three lines into an X on open, back on close. Production duration: `0.6s cubic-bezier(0.85, 0, 0.15, 1)`. Use two pseudo-elements (`::before` top stroke, `::after` bottom stroke) that translate + rotate to form the X.

```css
.kma-burger {
  position: relative;
  width: 24px; height: 18px;
  background: none; border: 0; cursor: pointer;
  /* The middle stroke is a real <span> child, omitted here for brevity */
}
.kma-burger::before,
.kma-burger::after {
  content: "";
  position: absolute;
  left: 0; right: 0;
  height: 2px;
  background: currentColor;
  transition: transform var(--kma-dur-mid) var(--kma-ease);
}
.kma-burger::before { top: 0; }
.kma-burger::after  { bottom: 0; }

.kma-burger.is-active::before { transform: translateY(8px) rotate(45deg); }
.kma-burger.is-active::after  { transform: translateY(-8px) rotate(-45deg); }
```

**E. Checkmark sweep on success**

Animated checkmark for completion states (form submit, step done, item activated). Production keyframe: `0.6s ease-out`, often delayed by a couple of seconds after the success signal so the user sees the state change before the celebration. Build with an SVG `<path>` and `stroke-dasharray` / `stroke-dashoffset` animation, or via a Lottie.

### 11.14 Hero callout box

A small dark bento callout pinned to the **bottom-right** of a hero block, carrying secondary context (a Q&A dialogue, a stat, a tagline). Lives inside the hero, not below it. Doesn't compete with the main headline.

```html
<section class="kma-hero">
  <h1>Kiss My Apps is a platform company that scales businesses with own AI ecosystem</h1>
  <figure class="kma-hero__visual">
    <!-- wireframe sphere or LED-matrix canvas -->
  </figure>
  <aside class="kma-hero__callout">
    <p>— In 3 years, we became a 9-figure company purely on a bootstrap.</p>
    <p class="kma-hero__callout-q">— How?</p>
    <p>— Building a launchpad for businesses with Product Engine and M&A</p>
  </aside>
</section>
```

```css
.kma-hero {
  position: relative;
  min-height: 100vh;
  padding: var(--kma-space-16) var(--kma-grid-margin);
}

.kma-hero__callout {
  position: absolute;
  right: var(--kma-grid-margin);
  bottom: var(--kma-space-12);
  width: min(28rem, 36vw);
  padding: var(--kma-space-6);
  background: rgba(30, 30, 32, 0.85); /* dark with slight transparency over the hero visual */
  backdrop-filter: blur(8px); /* purposeful glass, not decorative — see §16.1 */
  font-family: var(--kma-font-sans);
  font-size: var(--kma-fs-b1);
  line-height: var(--kma-lh-snug);
  color: var(--kma-white);
}

.kma-hero__callout-q {
  color: var(--kma-emerald); /* inline-accent on body — §5.6 */
}
```

**Rules:**
- **Always bottom-right** on hero. Not top, not centered, not bottom-left.
- **Width capped at ~28 rem.** A wide callout competes with the headline.
- **Content is conversational** — Q&A, two-line stat, or a single-sentence aside. Never a paragraph of body copy.
- **Em dashes legal here** (§5.6 / §13.1 — Q&A constructions are exempt from the no-em-dash rule).
- Glass effect with `backdrop-filter` is allowed for this component **specifically** — the dark hero visual behind the callout provides legitimate purpose for glass. Don't use glass elsewhere by default (§16.1).

---

## 12. Page archetypes

How to compose a new page from §11 primitives.

### 12.1 Marketing landing page

Default flow for any new campaign or product micro-site. The page is **predominantly dark with alternating paper sections** (§3.2 Mode B). The paper sections earn their place — they slow the eye, anchor a fact.

| # | Block | Tone | Voice |
|---|---|---|---|
| 1 | **Hero** | Dark | LED-matrix canvas, hero A1 headline, B1 subtitle, two CTAs. Section accent: Emerald. |
| 2 | **About / company narrative** | Dark | H1 statement of purpose + wireframe-3D accent (§9.3.B) + Q&A callout in bottom-right (§11.14). |
| 3 | **Metric panel pair** | **Paper + drenched** | One paper, one drenched (Blueberry or Emerald). §11.11. |
| 4 | **Platform / product engine title** | Dark | H1 in stacked layout, section accent rotates per page (Emerald default). |
| 5 | **Feature cards** | Dark | 3–5 cards with chip tag, headline, body, Emerald CTA. Each card may contain a drenched sub-plate (§11.5 / §11.12). |
| 6 | **Marquee / text-repeater** | **Paper** | Striped letter fill (§9.5.B) — `BUILD / SCALE / REPEAT`. |
| 7 | **Product showcase** | Dark | Vertical browser + content card (§11.12 / §12.7). |
| 8 | **Co-founding pitch hero** | Dark | Hero-style block with pill-word emphasis (§6.4.A) — `LET'S LAUNCH YOUR [CO-FOUNDING] FUTURE TOGETHER`. |
| 9 | **People / values block** | Dark | H1 + Emerald drenched right rail with value list. |
| 10 | **Job/CTA block** | Dark | H1 "BUILD NEW TYPE OF TECH PLATFORM WITH US" + open-roles row or single CTA. |
| 11 | **Newsroom strip** | Dark | Latest posts carousel. |
| 12 | **Footer** | Dark | §11.8. |

Each block uses `scroll-snap-align: start`. Total page height is generous (~13 viewports on desktop is normal); short pages read as light on KMA.

**Rhythm rule:** the paper sections (3 and 6) account for ~15 – 20% of total scroll. Two paper interludes between 8–10 dark blocks. More than that and the alternation reads as inconsistent; fewer and the page feels monotone.

### 12.2 Product detail page

For pages dedicated to a single product or service.

1. Hero with the product name in Stolzl Book mixed case (not all-caps — product names sit one register softer than slogans). Subtitle in Stolzl Book 24 px.
2. Side rail with a single fake-3D accent.
3. Feature card stack: 3 – 5 cards explaining capabilities.
4. CTA block ("Explore engine" or "Talk to a co-founder").
5. Related products row (chip pills).
6. Footer.

### 12.3 Job board / careers index

1. Hero with H1 "BUILD WITH US" or similar, B1 supporting paragraph.
2. Filter row (department, location, remote).
3. Open-roles list as a single column of stacked rows: each row is a department label (small caps) + job title (H3 size) + chip with location/remote + right arrow.
4. Hover: row inverts to `--kma-emerald` background with `--kma-black` text.
5. CTA block at bottom: "Don't see your role? Talk to us." with `kma-btn--secondary`.
6. Footer.

### 12.4 Job detail page

1. Sticky back-to-list link at top.
2. H1 title in Stolzl Heavy. Department + location chips below.
3. Long-form body in two columns at desktop, single at mobile: requirements left, responsibilities right.
4. Apply-CTA banner sticky at bottom on mobile, in-line at desktop.
5. Related-roles strip.
6. Footer.

### 12.5 Newsroom / article page

1. Article hero: H1 in Stolzl Heavy, date and author in Stolzl Book 16 px.
2. Hero image (heavily treated — bitmap, posterize, or 3D-blob accent).
3. Article body in single column, body line length 65 – 75 ch, Stolzl Book 20 px.
4. Inline pull-quotes set in Stolzl Heavy A1 with `color: var(--kma-emerald)`.
5. End-of-article share row + author bio + related articles strip.
6. Footer.

### 12.6 Single-purpose form / co-founding inquiry page

1. Hero with H1 stating the intent ("Become a co-founder").
2. Underlined-input form (§11.9) in single column, max-width 480 px.
3. `kma-btn--primary` "Send".
4. Footer.

No multi-step wizard, no progress bar — KMA forms are short or they're not on the page.

### 12.7 Product showcase

A standalone page (or page section, see §12.1 row 7) dedicated to the KMA product portfolio. Uses the product browser component (§11.12) as the backbone.

1. **Section title** — small subtitle ("Products that succeeded on our platform") in Stolzl Book 20 px, top-left.
2. **Vertical product nav** on the left rail — Stolzl Heavy uppercase, active item carries the `→` arrow and inherits the assigned product color. List 4–6 products max.
3. **Content card** on the right — split into:
   - **Image plate** (square or 4:3, dark surface, product thumbnail image).
   - **Drenched colored sub-plate** (the product's assigned color: AI Remodel → Violet-app, Botan → Emerald, etc.) carrying product name (Stolzl Heavy uppercase), positioning sub-line, optional ornament (laurel wreath, `#1 AI-TOOL FOR INTERIOR DESIGN`).
   - **Body copy** below the card — one tight paragraph (60–80 words) explaining the product's success story.
4. **Background** — subtle dark texture (concentric scratched circles, radial mesh). Reads as engineering-blueprint, not flat fill.
5. **Transition between products** — clicking a different product nav item swaps the card content with a fade (`opacity` only, `--kma-dur-mid --kma-ease`), nav indicator slides.
6. **Mobile (<768 px)** — collapse the vertical nav into a horizontal scrollable strip at top, card below stacks vertically.

Footer at bottom.

This archetype works as a full page or as one section inside a longer marketing landing.

---

## 13. Copy voice

KMA copy is declarative, ironic, addresses the reader directly, drops emoji as punctuation, and mixes languages without apology. Hero copy is unironic ambition; social and body copy is self-aware and cheeky. Both modes are on-brand.

### 13.1 Voice rules

- Every word earns its place. No "Welcome to…" intros. No restated headings.
- **No em dashes in body copy**, except Q&A constructions (`— How?` `— Result?`). No `--` ever.
- Russian, Ukrainian, English all legal; match the audience. Partner-facing decks default English; internal content runs in Ukrainian/Russian; web is English-default with a Ukrainian toggle.
- Bilingual one-liners are on-brand and add personality: `Kiss My Apps is in the тоР-5`, `айтівець оптиміст перед новим роком`. Don't sanitize them.
- Hero slogans are uppercase and unironic ("AI PLATFORM THAT FUELS PRODUCTS FOR MILLIONS").
- Body copy is mixed-case and self-aware ("In 3 years, we became a 9-figure company purely on a bootstrap").
- Q&A pattern: `— Question?` (inline color emphasis) → `— Answer.` (white). The em dash is part of the rhythm.

### 13.2 Sample headlines

For idea seeds. Don't copy verbatim; sample the rhythm.

- "AI PLATFORM THAT FUELS PRODUCTS FOR MILLIONS"
- "Let's launch the future together"
- "Kiss My Apps is a platform company that scales businesses with own AI ecosystem"
- "Got a strong idea and proven expertise, but missing a partner-in-scale?"
- "LET'S LAUNCH YOUR CO-FOUNDING FUTURE TOGETHER"
- "BUILD NEW TYPE OF TECH PLATFORM WITH US"
- "IT'S A PEOPLE THING"
- "PRODUCT ENGINE INFRASTRUCTURE FOR SCALE"
- "BUILD / SCALE / REPEAT"

### 13.3 Sample body / Q&A

- "— In 3 years, we became a 9-figure company purely on a bootstrap. — How? — Building a launchpad for businesses with Product Engine and M&A."
- "Meet our full-cycle AI platform that empowers product development and growth. We use data and insights to back any B2C solutions, to scale. — Result? — Over an 80% success rate across any launches based on a platform."
- "We give both growth and creative freedom to build something worth millions of users. You are free to create this with us."
- "Mature Freedom — Yes, we really give freedom to create. But freedom here is not about chaos — it's about your ownership and execution."
- "No-bullshit Support — We're here to make cool things together, so you'll receive support and mentorship from day one."

### 13.4 CTA labels

Short, all-caps, Stolzl Heavy.

- WORK WITH US
- CO-FOUND WITH US
- EXPLORE ENGINE
- SEE OPEN ROLES
- EXPLORE CO-FOUNDING TRACK
- EXPLORE MORE CONTENT

### 13.5 Voice patterns to imitate

- Standalone numerals at large scale for visual weight (`+30`, `TOP-5`, `16 28` for street numbers).
- Inline color for one key noun or question per paragraph.
- Sentence fragments are legal ("Single dominant idea per fold.").
- Ironic asides bracketed with em dashes (legal in Q&A) or commas.
- Direct address ("You are free to create this with us.").
- British spelling occasional, voice-marker ("I REALISE AND ACCEPT IT").

### 13.6 Voice patterns to avoid

- "Trusted by industry leaders."
- "Our solution empowers businesses to…"
- "World-class team of experts."
- "Click here to learn more."
- "Solutions for the modern enterprise."
- "Innovation at scale."
- Any phrase that could appear on a Salesforce landing page.

---

## 14. Imagery

KMA's web pages are mostly photo-light: hero canvases use the LED-matrix, sections use fake-3D blobs, marketing photos appear in newsroom strips and careers content.

When photos are used:

### 14.1 Tags

`#sincere #punk #punk-fashion #expression #friendly #bright #high-color-contrast`

Real people, real moments, high saturation, edge-of-frame energy. Studio-stock-photo cleanliness is not the voice.

### 14.2 Treatments

| Treatment | Look | Where |
|---|---|---|
| **Bitmap color** | Duotone halftone (black + Emerald, white + Blueberry). | Hero pics, reels covers. |
| **B/W bitmap** | 1-bit halftone. | Hero photos in monochrome compositions. |
| **Distortion** | Wave / glitch via Photoshop or Figma Displace. | Hero / special-moment shots. |
| **Two-color posterize** | Flatten to two flat regions of brand color + dark twin. | Color-block accents. |
| **Photo grain** | Film grain at low opacity. | Most photos. |

### 14.3 Composition

- Regular photo with brand padding around.
- Cutout photo on a brand-color plate.
- Brand-filter photo (bitmap / posterize / dither).

### 14.4 Anti-patterns

- Stock photos repeated post-after-post. Content must feel unique.
- Low-resolution sources.
- Generic happy-business-people stock. Generic finance-chart stock. Generic team-high-fives stock.

### 14.5 Endless Tool (3D assets)

For fake-3D objects, use `https://endless.tools/` as the asset source. Pull, re-color in a brand color, export PNG, drop into a sharp-corner plate. One per composition.

---

## 15. Accessibility

KMA's brand uses high-saturation colors that don't always clear WCAG AA at small text sizes. Hard requirements:

- **Body text on color plates: use the dark-twin pairing** (§5.5 #3). Black-on-Blueberry fails AA; Dark-Blueberry-on-Blueberry passes.
- **Hero CTA exception:** `--kma-black` on `--kma-emerald` clears AA by ≈ 9 : 1. Document the choice where it appears.
- **Logo on photo: always plate it.** Reading the wordmark on busy texture is harder than the contrast ratio suggests.
- **Animated content respects `prefers-reduced-motion`.** Disable the LED canvas, glitch, distortion, parallax, scroll-snap auto-engage, and large entrance choreography when the OS flag is set. Keep opacity transitions ≤ 200 ms.
- **Decorative graphics get `alt=""`.** Fake-3D objects and the LED matrix are decorative. Photos with captioning context get descriptive alt text in the voice.
- **Focus rings visible.** Default outline: `2px solid var(--kma-emerald)`, `outline-offset: 2px`.
- **Hit targets ≥ 44 × 44 px** on touch.
- **Touch device:** disable hover-only affordances (the row-invert in §12.3 should also trigger on touch via active state).

---

## 16. Paste-ready tokens

### 16.1 CSS custom properties

```css
:root {
  /* Neutrals */
  --kma-black:     oklch(0.230 0.004 286);  /* #1E1E20 */
  --kma-white:     oklch(0.962 0.000 0);    /* #F5F5F5 */
  --kma-gray-25:   oklch(0.892 0.002 286);  /* #DFDFE0 */
  --kma-gray-40:   oklch(0.770 0.012 280);  /* #BBBCC4 */
  --kma-gray-60:   oklch(0.819 0.010 270);  /* #C8CAD0 */

  /* Primary */
  --kma-blueberry:      oklch(0.642 0.191 271.4);  /* #657FFF */
  --kma-emerald:        oklch(0.779 0.196 144.2);  /* #58D65E */
  --kma-blueberry-dark: oklch(0.341 0.090 272.5);  /* #293366 */
  --kma-emerald-dark:   oklch(0.409 0.096 144.3);  /* #245726 */

  /* Per-page accent (default Emerald) */
  --section-color: var(--kma-emerald);

  /* Secondary (use situationally) */
  --kma-light-blue:      oklch(0.804 0.119 232.7);  /* #66CCFF */
  --kma-purple:          oklch(0.696 0.182 296.6);  /* #AA80FF */
  --kma-pink:            oklch(0.762 0.168 350.8);  /* #FF80BF */
  --kma-red:             oklch(0.706 0.186 23.1);   /* #FF6767 */
  --kma-orange:          oklch(0.829 0.145 73.5);   /* #FFB74D */
  --kma-yellow:          oklch(0.926 0.184 102.4);  /* #FFEA30 */
  --kma-violet-app:      oklch(0.621 0.183 286.6);  /* #927DFF */
  --kma-light-blue-dark: oklch(0.486 0.069 232.8);  /* #336680 */
  --kma-purple-dark:     oklch(0.425 0.104 296.9);  /* #554080 */
  --kma-pink-dark:       oklch(0.462 0.097 350.3);  /* #804060 */
  --kma-red-dark:        oklch(0.429 0.107 22.7);   /* #803333 */
  --kma-orange-dark:     oklch(0.502 0.084 74.6);   /* #805C26 */
  --kma-yellow-dark:     oklch(0.556 0.108 102.2);  /* #807518 */

  /* Type */
  --kma-font-sans:    "book", Arial, Helvetica, sans-serif;
  --kma-font-display: "heavy", Arial, Helvetica, sans-serif;
  --kma-fs-a1:  clamp(4rem, 7vw + 1rem, 7rem);
  --kma-fs-h1:  clamp(2.5rem, 3vw + 1rem, 4.5rem);
  --kma-fs-h3:  clamp(1.75rem, 1vw + 1rem, 2.5rem);
  --kma-fs-b1:  clamp(1.125rem, 0.25vw + 1rem, 1.5rem);
  --kma-fs-tag: 1rem;
  --kma-lh-tight: 0.92;
  --kma-lh-h1:    1.00;
  --kma-lh-snug:  1.20;
  --kma-lh-body:  1.40;
  --kma-ls-display: -0.02em;
  --kma-ls-tag:      0.04em;

  /* Radius */
  --kma-radius-sharp: 1px;
  --kma-radius-pill:  9999px;
  --kma-radius-xs:    0.5rem;
  --kma-radius-sm:    1rem;
  --kma-radius-md:    1.5rem;
  --kma-radius-lg:    2rem;
  --kma-radius-xl:    3rem;
  --kma-radius-2xl:   4rem;

  /* Grid + spacing */
  --kma-grid-margin: 2.22rem;
  --kma-grid-gutter: 0.56rem;
  --kma-nav-h:       3.89rem;
  --kma-space-1:  0.25rem;
  --kma-space-2:  0.5rem;
  --kma-space-3:  0.75rem;
  --kma-space-4:  1rem;
  --kma-space-6:  1.5rem;
  --kma-space-8:  2rem;
  --kma-space-12: 3rem;
  --kma-space-16: 4rem;
  --kma-space-24: 6rem;

  /* Motion */
  --kma-ease:           cubic-bezier(0.85, 0, 0.15, 1);
  --kma-ease-out-quart: cubic-bezier(0.16, 1, 0.30, 1);
  --kma-dur-fast: 0.3s;
  --kma-dur-mid:  0.6s;
  --kma-dur-slow: 1.2s;
  --kma-dur-hero: 2.0s;
}

html, body {
  background: var(--kma-black);
  color: var(--kma-white);
  font-family: var(--kma-font-sans);
  font-size: var(--kma-fs-b1);
  line-height: var(--kma-lh-body);
  -webkit-font-smoothing: antialiased;
}

@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}
```

### 16.2 Tailwind v4 (`@theme`)

```css
@theme {
  --color-kma-black:        oklch(0.230 0.004 286);
  --color-kma-white:        oklch(0.962 0.000 0);
  --color-kma-gray-25:      oklch(0.892 0.002 286);
  --color-kma-gray-40:      oklch(0.770 0.012 280);
  --color-kma-gray-60:      oklch(0.819 0.010 270);

  --color-kma-blueberry:      oklch(0.642 0.191 271.4);
  --color-kma-emerald:        oklch(0.779 0.196 144.2);
  --color-kma-blueberry-dark: oklch(0.341 0.090 272.5);
  --color-kma-emerald-dark:   oklch(0.409 0.096 144.3);

  --color-kma-light-blue:      oklch(0.804 0.119 232.7);
  --color-kma-purple:          oklch(0.696 0.182 296.6);
  --color-kma-pink:            oklch(0.762 0.168 350.8);
  --color-kma-red:             oklch(0.706 0.186 23.1);
  --color-kma-orange:          oklch(0.829 0.145 73.5);
  --color-kma-yellow:          oklch(0.926 0.184 102.4);
  --color-kma-violet-app:      oklch(0.621 0.183 286.6);
  --color-kma-light-blue-dark: oklch(0.486 0.069 232.8);
  --color-kma-purple-dark:     oklch(0.425 0.104 296.9);
  --color-kma-pink-dark:       oklch(0.462 0.097 350.3);
  --color-kma-red-dark:        oklch(0.429 0.107 22.7);
  --color-kma-orange-dark:     oklch(0.502 0.084 74.6);
  --color-kma-yellow-dark:     oklch(0.556 0.108 102.2);

  --font-sans:    "book", Arial, Helvetica, sans-serif;
  --font-display: "heavy", Arial, Helvetica, sans-serif;

  --radius-sharp: 1px;
  --radius-pill:  9999px;
  --radius-xs:  0.5rem;
  --radius-sm:  1rem;
  --radius-md:  1.5rem;
  --radius-lg:  2rem;
  --radius-xl:  3rem;
  --radius-2xl: 4rem;

  --transition-duration-fast: 300ms;
  --transition-duration-mid:  600ms;
  --transition-duration-slow: 1200ms;
  --transition-timing-kma:    cubic-bezier(0.85, 0, 0.15, 1);
  --transition-timing-quart:  cubic-bezier(0.16, 1, 0.30, 1);
}
```

### 16.3 Style Dictionary / W3C tokens (JSON)

```json
{
  "color": {
    "kma": {
      "black":          { "$value": "#1E1E20", "$type": "color" },
      "white":          { "$value": "#F5F5F5", "$type": "color" },
      "gray-25":        { "$value": "#DFDFE0", "$type": "color" },
      "gray-40":        { "$value": "#BBBCC4", "$type": "color" },
      "gray-60":        { "$value": "#C8CAD0", "$type": "color" },
      "blueberry":      { "$value": "#657FFF", "$type": "color" },
      "emerald":        { "$value": "#58D65E", "$type": "color" },
      "blueberry-dark": { "$value": "#293366", "$type": "color" },
      "emerald-dark":   { "$value": "#245726", "$type": "color" },
      "light-blue":     { "$value": "#66CCFF", "$type": "color" },
      "purple":         { "$value": "#AA80FF", "$type": "color" },
      "pink":           { "$value": "#FF80BF", "$type": "color" },
      "red":            { "$value": "#FF6767", "$type": "color" },
      "orange":         { "$value": "#FFB74D", "$type": "color" },
      "yellow":         { "$value": "#FFEA30", "$type": "color" },
      "violet-app":     { "$value": "#927DFF", "$type": "color" }
    }
  },
  "font": {
    "family": {
      "sans":    { "$value": "book, Arial, Helvetica, sans-serif",  "$type": "fontFamily" },
      "display": { "$value": "heavy, Arial, Helvetica, sans-serif", "$type": "fontFamily" }
    }
  },
  "radius": {
    "sharp": { "$value": "1px",   "$type": "dimension" },
    "pill":  { "$value": "9999px","$type": "dimension" },
    "xs":    { "$value": "8px",   "$type": "dimension" },
    "sm":    { "$value": "16px",  "$type": "dimension" },
    "md":    { "$value": "24px",  "$type": "dimension" },
    "lg":    { "$value": "32px",  "$type": "dimension" },
    "xl":    { "$value": "48px",  "$type": "dimension" },
    "2xl":   { "$value": "64px",  "$type": "dimension" }
  },
  "motion": {
    "ease":          { "$value": "cubic-bezier(0.85, 0, 0.15, 1)", "$type": "cubicBezier" },
    "ease-out-quart":{ "$value": "cubic-bezier(0.16, 1, 0.30, 1)", "$type": "cubicBezier" },
    "duration-fast": { "$value": "300ms",  "$type": "duration" },
    "duration-mid":  { "$value": "600ms",  "$type": "duration" },
    "duration-slow": { "$value": "1200ms", "$type": "duration" }
  }
}
```

### 16.4 Logo combinations as code

```ts
type LogoVariant = 'long' | 'square' | 'no-outline';
type LogoMode    = 'filled' | 'stroke';
type LogoColor   = 'blueberry' | 'emerald' | 'black' | 'white';

const APPROVED: ReadonlyArray<{
  variant: LogoVariant;
  mode: LogoMode;
  color: LogoColor;
  background: 'black' | 'gray' | 'white' | 'textile';
}> = [
  { variant: 'long', mode: 'filled', color: 'blueberry', background: 'black' },
  { variant: 'long', mode: 'filled', color: 'emerald',   background: 'black' },
  { variant: 'long', mode: 'filled', color: 'black',     background: 'white' },
  { variant: 'long', mode: 'stroke', color: 'blueberry', background: 'black' },
  { variant: 'long', mode: 'stroke', color: 'emerald',   background: 'black' },
  { variant: 'long', mode: 'stroke', color: 'white',     background: 'black' },
  // Square mirrors Long with the same six combinations.
  // No-outline (textile) is print-only.
];
```

---

## 17. The slop test

Run on every artifact before shipping. If any of these slip through, rework.

### 17.1 Cross-register bans

- ❌ Side-stripe colored accents (`border-left: 4px solid`).
- ❌ Gradient text via `background-clip: text`.
- ❌ Glass card with no purpose.
- ❌ Hero metric template (giant number + tiny caption + gradient sparkle).
- ❌ Identical card grids (icon + heading + 2-line body × 6).
- ❌ Modal as the first thought for any interaction.
- ❌ Stock photography that could appear on any other company's site.

### 17.2 KMA-specific

- ❌ Looks like the first thing an AI would generate for "a B2C app studio" — clean white SaaS, navy + lime, lots of rounded cards.
- ❌ Editorial-magazine reflex (display serif italic, drop caps, ruled separators).
- ❌ Pure black/white with no grain — flat and template-looking.
- ❌ Single brand color across the whole composition with no contrast moment.
- ❌ Quokka used on web. Quokka is print/SMM only.
- ❌ Fake-3D objects in a grid instead of as a single focal accent.
- ❌ Stock illustrations of "diverse business team high-fives."
- ❌ Hero that is a static image with no motion — the voice includes some form of LED-matrix, animated 3D, or marquee. A static replacement is a downgrade.
- ❌ Body copy with em dashes outside Q&A.
- ❌ More than 1 secondary brand color on a single page without an explicit reason.

### 17.3 Category-reflex check

**First-order:** if someone could guess the palette from the category alone ("B2C app studio → dark + green, OR dark + violet"), you've landed on the obvious reflex. Push past it.

**Second-order:** if someone could guess the aesthetic family from category + anti-reference ("AI app studio that's not SaaS-cream → editorial-typographic"), that's the second reflex. KMA isn't tasteful editorial either; it's bento-cyberpunk **plus** grain + dither + 3D blob + LED-matrix. Both reflexes must fail.

### 17.4 Brand permissions (take them)

Brand surfaces have earned these permissions. Don't hedge.

- **Ambitious first-load motion.** Orchestrated reveals, scroll-triggered transitions, glitch-in entrances. Tech-minimal restraint is not the voice.
- **Single-purpose viewports.** One dominant idea per fold. Long scroll. Deliberate pacing via scroll-snap.
- **Typographic risk.** Stolzl Heavy at 110 px. One word as the hero. Stacked overlapping text. Stroke-only headlines.
- **Unexpected color strategies.** Drenched Emerald section. Blueberry-on-Black hi-fi. Per-page accent rotation.
- **Art direction per section.** Different sections, different visual worlds. Consistency of voice beats consistency of treatment.
- **Imagery as canvas.** Real photos treated heavily, or LED-matrix, or fake-3D scenes. Don't replace with a `<div>` placeholder.

### 17.5 When in doubt

1. Re-read §2 (voice & lane) and §5.5 (color combinating).
2. Pull up the live site, find a section that resembles what you're shipping, compare voice density.
3. Run the slop test in §17.1 / §17.2.
