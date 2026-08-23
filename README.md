# AfriPOP — Refresh Our Pride

A single-page marketing site for **AfriPOP** (Bidco Africa), built around the brand's "Age of RE" campaign — five flavours, five stories, one drink.

🔗 **Live site:** _add your GitHub Pages link here once deployed_

---

## What's in the page

| Section | What it does |
|---|---|
| **Hero** | Cycles through all five flavours automatically (Cola → Orange → Ginger → Lemon Lime → Blackcurrant), recolouring the background, swapping the bottle image, and updating the flavour tag in sync. Click a dot to jump to a flavour directly. |
| **Manifesto** | Scroll-triggered reveal of the "RE." statement line by line. |
| **The Movement** | Brand pillars (Rebuild, Rejoice, Reignite, Refresh, Reimagine), one per flavour. |
| **Flavours** | Horizontal scroll-snap card row for all five products. |
| **The Age of RE** | Interactive accordion — tap a flavour to see its story. |
| **Find AfriPOP** | Store-locator CTA with a QR code card, styled in the brand's cream/gold palette. |
| **Final statement** | Closing scroll-reveal + logo + CTA. |

Everything is plain **HTML, CSS, and vanilla JavaScript** — no build step, no dependencies.

---

## File structure

```
.
├── afripop.html            # the whole site (single file)
├── assets/
│   ├── gold_option_1___2_.png     # AfriPOP logo (nav + footer)
│   ├── africa-pattern-map.png     # Pride Mark pattern (hero texture + footer mark)
│   ├── AFRIPOP_PACKSOT.png        # full bottle range (used in flavours/footer if referenced)
│   ├── 1.png                      # Cola bottle
│   ├── 2.png                      # Orange bottle
│   ├── 3.png                      # Ginger bottle
│   ├── 5.png                      # Lemon Lime bottle
│   ├── 6.png                      # Blackcurrant bottle
│   └── BIDCO_QR_CODE.jpeg         # store-locator QR code
└── README.md
```

> **Note:** the asset filenames above are what the HTML expects. If you rename an image, update the matching `src=`/`background-image` reference in `afripop.html`, or vice versa.

---

## Running it locally

No build tools needed — just open the file:

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
open afripop.html   # or just double-click it
```

If you'd rather serve it (recommended, avoids some browser file:// restrictions):

```bash
python3 -m http.server 8000
# then visit http://localhost:8000/afripop.html
```

---

## Deploying with GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to `Deploy from a branch`, pick `main` (or your default branch) and `/ (root)`.
4. Save — GitHub gives you a live URL a minute or two later, e.g. `https://<username>.github.io/<repo>/afripop.html`.
5. If you want the page at the root of the URL instead of `/afripop.html`, rename `afripop.html` to `index.html`.

---

## Brand palette

| Colour | Hex | Use |
|---|---|---|
| White | `#FFFFFF` | Backgrounds, logo support, negative space |
| Premium tan | `#E8D8B8` | Premium backgrounds, hero graphics, high-impact brand moments |
| Cream | `#F3EBDD` | Page background |
| Tan | `#DFC58F` | Supporting/secondary surfaces |
| Gold | `#C9A227` | Accents, CTAs, hero base |
| Ink | `#2F2F2F` | Body text, dark surfaces |

| Flavour | Hex |
|---|---|
| Cola | `#E53935` |
| Orange | `#FF8A00` |
| Ginger (Tangawizi) | `#6D4C41` |
| Lemon Lime | `#21B14B` |
| Blackcurrant | `#7B1FA2` |

Flavour colours are reserved for flavour-specific moments (bottle glows, the Age of RE accordion, flavour cards). Brand-wide sections (hero base, Find AfriPOP) use the gold/cream family so no single flavour is favoured.

## Typography

- **Comfortaa Bold** — logo, brand name, main headlines
- **Caveat Bold** — slogans and campaign lines ("Refresh Our Pride!")
- **Poppins** — body text, descriptions

All loaded via Google Fonts in the `<head>`.

---

## Customising

- **Swap bottle/logo images** → replace the files in `assets/` (keep the same filenames, or update the `src` attributes in `afripop.html`).
- **Change hero timing** → in the `<script>` at the bottom of the file, edit `4400` (milliseconds) in `restartHeroTimer()`.
- **Edit copy** → all headline/body text lives directly in the HTML, no CMS.
- **Add social preview tags** → add `<title>`, `<meta name="description">`, and Open Graph tags to `<head>` so shared links show the right title/description/image.

---

## Credits

AfriPOP is a product of **Bidco Africa**. Site built as part of the "Age of RE" campaign concept.
