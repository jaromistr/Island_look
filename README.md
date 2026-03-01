# Island Look Boutique — Website

Single-page website for **Island Look**, a fashion & souvenir boutique on Nusa Lembongan, Bali.

## Tech Stack

- Pure HTML/CSS/JS (no frameworks, no build step)
- Google Fonts: Cormorant Garamond, Josefin Sans, Playfair Display
- Google Maps Embed API
- WhatsApp Business links (`wa.me/`)

## Project Structure

```
Island-look/
├── index.html          # Main website (single file)
├── BRIEFING.md         # Brand brief & content guide
├── README.md           # This file
└── .claude/
    └── launch.json     # Dev server config
```

## Local Development

Open `index.html` directly in a browser — no server required.

Or use any static server:

```bash
# Python
python3 -m http.server 8080

# Ruby
ruby -run -e httpd . -p 8080
```

## Sections

| Section    | Description                                      |
|------------|--------------------------------------------------|
| Hero       | Split layout — tagline left, shop photo right    |
| Our Story  | Brand story + 3-photo grid (interior/collection) |
| Shop       | 4 product categories with WhatsApp CTA           |
| Brands     | Curated brand logos (placeholder)                 |
| Visit Us   | Address, hours, WhatsApp + Google Maps embed      |
| Contact    | WhatsApp, Instagram, Google Maps buttons          |

## Features

- **Bilingual** — EN / ID toggle (client-side, no reload)
- **Mobile-first** — hamburger menu with fullscreen overlay
- **WhatsApp CTA** — category-specific pre-filled messages
- **SEO** — meta tags, Open Graph, Schema.org (ClothingStore)
- **Google Maps** — embedded map with exact pin on the boutique
- **Scroll animations** — fade-up reveal on intersection

## What Needs Real Content

Before going live, replace these placeholders:

- [ ] **Hero photo** — `<img class="hero-img" src="">` in hero section
- [ ] **Story photos** (3x) — interior, collection, detail in story section
- [ ] **Product photos** (4x) — clothing, accessories, beauty, souvenirs
- [ ] **Brand names** — replace "Brand 1–6" in #brands section
- [ ] **Logo file** — add favicon and OG image
- [ ] **Canonical URL** — update `<link rel="canonical">` with final domain
- [ ] **OG image** — add `og:image` meta tag with a share preview image

## Contact Info (Live)

- **Address:** Jl. Jungutbatu, Nusa Lembongan, Bali 80771
- **WhatsApp:** +62 878-8252-6990
- **Instagram:** [@islandlook_](https://www.instagram.com/islandlook_/)
- **Google Maps:** [Island Look](https://www.google.com/maps/place/Island+Look/@-8.6668134,115.4507592,17z/)

## Deploy

Static site — deploy anywhere:

- **Netlify** — drag & drop the folder
- **Vercel** — `vercel --prod`
- **GitHub Pages** — push to `main`, enable Pages in repo settings
