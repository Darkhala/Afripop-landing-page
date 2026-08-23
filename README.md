# AfriPOP Landing Page

A single-file HTML landing page for AfriPOP soft drinks ("Refresh Our Pride" / "The Age of RE"), covering the hero, brand manifesto, flavour lineup, and store-locator sections.

## File

- `AfriPOP_updated.html` — the entire site (HTML + CSS + JS in one file, no build step required).

## How to use it

1. Open `AfriPOP_updated.html` directly in a browser to preview it, or upload it to any static web host (Netlify, Vercel, GitHub Pages, or your own server).
2. All images are referenced from a local `assets/` folder that sits next to the HTML file. Create that folder and drop in the files listed below before the page will display correctly — right now the `<img>` tags point to filenames that don't exist yet on your server.

## Required assets (place in `/assets`)

| Filename | Used for |
|---|---|
| `gold option 1_ (2).png` | Logo (nav, footer, final section) |
| `africa-pattern-map.png` | Faint repeating hero background texture |
| `cola.png` | Cola bottle (hero + flavour card) |
| `Orange.png` | Orange bottle |
| `Ginger.png` | Ginger bottle |
| `Lemonlime.png` | Lemon Lime bottle |
| `Blackcurrant.png` | Blackcurrant bottle |
| `1.png`–`6.png` (used: 1,2,3,5,6) | Bottle images shown in the "Age of RE" tap panels |
| `BIDCO QR CODE.jpeg` | QR code in the "Find AfriPOP" section |
| `Pride africa.png` | Small brand mark in the footer |

Filenames must match exactly (case-sensitive on most hosts, including spaces).

## Sections in the page (in order)

1. **Nav** — logo, links, "Find AfriPOP" button.
2. **Hero** — auto-cycles through the 5 flavours every 4.4s (background color, bottle image, and label all switch together). Dots at the top let a visitor jump to a flavour directly.
3. **Manifesto** — short animated line-by-line statement, fades in on scroll.
4. **About / Pillars** — brand statement plus 5 colour-coded cards, one per flavour, using the flavour copy from your shop description doc.
5. **Flavours** — horizontally scrollable flavour cards (same copy as the pillars).
6. **Age of RE** — clickable list; tapping a flavour name expands a panel with its bottle image and description.
7. **Find AfriPOP** — store-locator CTA with a QR code (labelled "AfriPOP Store," not "Pride Station").
8. **Final statement** — closing animated lines + logo + CTA.
9. **Footer** — nav links, social icons (Facebook, Instagram, TikTok — already linked to your real profiles), copyright line.

## Editing copy or links

Everything is plain HTML — search the file for the text you want to change and edit it directly. A few landmarks:

- Flavour descriptions appear in **three places** (pillar cards, flavour cards, and the Age of RE `data-desc` attributes) — update all three together to keep copy consistent.
- Social links are in the `<footer>` under `.foot-social` — swap the `href` values to update destinations, or replace the inline SVGs with your own icon images if you'd rather use official logo art.
- The word "Pride" is intentionally used only once, in the "Refresh Our Pride" tagline, to avoid any association with unrelated movements.

## Notes / things to double check

- No external JS libraries are used — everything (the hero rotation, scroll-reveal animations, and the Age of RE accordion) is vanilla JavaScript in the `<script>` tag at the bottom.
- Fonts (Comfortaa, Caveat, Poppins) load from Google Fonts via the `<link>` tags in `<head>` — an internet connection is needed for them to render as designed.
- The page is responsive down to mobile widths, with layout adjustments defined in the `@media (max-width:860px)` and `@media (max-width:960px)` blocks.