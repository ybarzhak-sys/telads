# Kiss My Apps — Font files

This directory ships Stolzl font files licensed to Kiss My Apps for use on KMA brand surfaces. `fonts.css` declares `@font-face` for the `book` (body) and `heavy` (display) family aliases.

## Files

| File | Family | Weight | Use |
|---|---|---|---|
| `Stolzl-Book.woff2`    | `book`  | 350 | Light reading, secondary captions |
| `Stolzl-Regular.woff2` | `book`  | 400 | Default body |
| `Stolzl-Medium.woff2`  | `book`  | 500 | Emphasis runs, mid-weight headlines |
| `Stolzl-Bold.woff2`    | `book`  | 700 | Inline bold, sub-heads |
| `heavy.woff2`          | `heavy` | 400 | Display — hero, A1, CTAs (uppercase) |

`heavy` is declared as a separate `font-family` so markup like `font-family: "heavy"; font-weight: 400;` renders the display weight regardless of the surrounding weight inheritance. Keep this convention — it matches the live site (kissmyapps.com).

## How to use

```css
/* Option 1 — import the @font-face block directly */
@import "./fonts.css";

/* Option 2 — inline @font-face into a global stylesheet, adjust url() paths */
```

Then in your CSS:

```css
:root {
  --kma-font-sans:    "book",  Arial, Helvetica, sans-serif;
  --kma-font-display: "heavy", Arial, Helvetica, sans-serif;
}

.title   { font-family: var(--kma-font-display); font-weight: 400; }  /* hero / display */
.body    { font-family: var(--kma-font-sans);    font-weight: 400; }  /* paragraph */
.body-b  { font-family: var(--kma-font-sans);    font-weight: 500; }  /* emphasis */
.body-bd { font-family: var(--kma-font-sans);    font-weight: 700; }  /* bold inline */
.body-l  { font-family: var(--kma-font-sans);    font-weight: 350; }  /* light reading */
```

## Licensing

Stolzl is a commercial typeface, licensed to KMA. Use these files only on KMA-branded surfaces.
