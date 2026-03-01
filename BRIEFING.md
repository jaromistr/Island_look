# Island Look Boutique — Website Briefing
> Připraveno pro předání do Claude Code

---

## O projektu

**Klient:** Island Look Boutique  
**Lokace:** Nusa Lembongan, Bali, Indonesia  
**Instagram:** https://www.instagram.com/islandlook_/  
**Typ webu:** One-page website (žádný e-shop)  
**Cíl:** SEO — přivést turisty do fyzického obchodu + kontakt přes WhatsApp  

---

## Hotový startovní bod

Máš k dispozici soubor `island-look-v2.html` — to je vizuálně schválený design základ.  
**Nezačínáš od nuly. Iteruješ na tomto souboru.**

---

## Design identita

### Vibe
Luxury island boutique — ne rustic boho, ale **čistá, elegantní, vzdušná** estetika.  
Inspirace: interiér obchodu (zlaté regály, mramorová podlaha, teplé světlo).

### Barvy (přesně tyto)
```
--cream:       #F5F0E8
--warm-white:  #FAF7F2
--sand:        #E8DEC8
--sand-mid:    #D4C8A8
--gold:        #C9A84C        ← hlavní accent, barva loga
--gold-light:  #E2C46A
--ink:         #1E1A14
--ink-mid:     #3A3228
--mist:        #9A8E7A
--marble:      #EDE8DF
```

### Typografie
- **Display / nadpisy:** Cormorant Garamond (serif, italic pro akcenty)
- **UI / navigace / labely:** Josefin Sans (velmi light, spaced caps)
- Žádné generické fonty (Inter, Roboto, Arial)

### Logo
Obchod má vlastní logo s palmovým listem — při implementaci použij jako `<img>` tag.  
Prozatím placeholder `IL` v Cormorant Garamond italic.  
Podtitul: **"ISLAND LOOK · BOUTIQUE"** nebo **"Fashion & Souvenir"**

---

## Struktura stránky (sekce v pořadí)

### 1. NAV (fixed, průhledná → frosted glass při scrollu)
- Logo vlevo
- Odkazy uprostřed: Our Story · Shop · Visit Us · Contact
- Vpravo: EN · ID language toggle
- Na mobilu: hamburger menu

### 2. HERO
- Split layout: text vlevo, velká fotka vpravo
- Headline: "ISLAND / LOOK" (Josefin Sans, large)
- Subline: "A luxury boutique on Nusa Lembongan..."
- 2 CTA buttony: **WhatsApp** (gold filled) + **Find the Boutique** (ghost)
- Fotka: placeholder → nahradit reálnou fotkou interiéru/exteriéru

### 3. OUR STORY
- Tmavé pozadí (`--ink`)
- Text vlevo, grid fotek vpravo (3 fotky — tall + 2 malé)
- Příběh vzniku obchodu (text viz sekce Texty níže)

### 4. SHOP / PRODUCTS
- 4 kategorie produktů v gridu (ne e-shop, jen přehled)
- Každá karta: foto placeholder, kategorie, název, popis, "Ask on WhatsApp →" link
- Kategorie: Clothing · Accessories · Beauty & Wellness · Souvenirs
- WA link na každé kartě s předvyplněnou zprávou

### 5. BRANDS
- Sekce pro loga/jména brandů které obchod prodává
- **Placeholder — doplnit při návštěvě obchodu**
- Prozatím: 6 placeholder chipů "Brand Name"

### 6. FIND US / MAPA
- Google Maps embed (iframe)
- Adresa, otevírací doba, WA číslo
- "Open in Google Maps →" button
- **Pozor: přesnou adresu a coords doplnit!**

### 7. CONTACT
- Tmavé pozadí
- 3 buttony: WhatsApp · Instagram · Google Maps

### 8. FOOTER
- Minimální: název + copyright

---

## Jazyky

Stránka je **EN + ID (indonésky)** s přepínačem.  
Implementace: `data-en="..."` a `data-id="..."` atributy + JS toggle.  
Defaultní jazyk: **EN**

Příklad:
```html
<p data-en="Our Story" data-id="Kisah Kami">Our Story</p>
```

---

## Texty (schválené)

### Hero
- **EN:** "A luxury boutique on Nusa Lembongan, curating the finest in island fashion, handcrafted accessories & local finds."
- **ID:** "Butik mewah di Nusa Lembongan, menghadirkan fashion terbaik, aksesori buatan tangan & temuan lokal."

### Our Story
- **EN:** "Island Look Boutique was born from a deep love for island life — the warm light, the ocean breeze, and the belief that style should feel as effortless as the tide. Nestled in the heart of Nusa Lembongan, we bring together island fashion, handcrafted pieces and carefully curated local brands — all under one beautifully designed roof. Every piece is chosen with intention — to help you carry a little piece of this island magic wherever you go next."
- **ID:** "Island Look Boutique lahir dari kecintaan mendalam terhadap kehidupan pulau — cahaya hangat, angin laut, dan keyakinan bahwa gaya hidup haruslah sealami ombak. Berlokasi di jantung Nusa Lembongan, kami menghadirkan fashion pulau, karya buatan tangan, dan brand lokal pilihan — semua di bawah satu atap yang indah. Setiap koleksi dipilih dengan cermat — untuk membantumu membawa sedikit keajaiban pulau ini ke manapun."

---

## Co je potřeba doplnit (TODO)

| Co | Status |
|----|--------|
| WhatsApp číslo | ✅ máme — doplnit do všech `wa.me/` odkazů |
| Reálné fotky (interiér, produkty, tým) | ⏳ nafotit při návštěvě |
| Přesná adresa + GPS coords pro mapu | ⏳ ověřit |
| Skutečné brandy (názvy/loga) | ⏳ zjistit při návštěvě |
| Otevírací doba | ⏳ ověřit |
| Logo soubor (PNG/SVG) | ⏳ získat od obchodu |
| Google Business Profile odkaz | ⏳ vytvořit / propojit |

---

## SEO požadavky

```html
<title>Island Look Boutique – Fashion & Souvenir | Nusa Lembongan, Bali</title>
<meta name="description" content="Island Look is a luxury boutique on Nusa Lembongan island, Bali. Shop island fashion, handcrafted accessories, beauty & souvenirs. Visit us or contact via WhatsApp." />
<meta name="keywords" content="nusa lembongan boutique, lembongan clothing store, bali island fashion, island look boutique, lembongan souvenir shop, bali beach boutique" />
```

**Schema markup** (LocalBusiness) — zahrnout v `<head>`:
```json
{
  "@context": "https://schema.org",
  "@type": "ClothingStore",
  "name": "Island Look Boutique",
  "description": "Luxury fashion & souvenir boutique on Nusa Lembongan, Bali",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "DOPLNIT",
    "addressLocality": "Nusa Lembongan",
    "addressRegion": "Bali",
    "addressCountry": "ID"
  },
  "telephone": "DOPLNIT",
  "openingHours": "Mo-Su 09:00-20:00",
  "sameAs": ["https://www.instagram.com/islandlook_/"]
}
```

---

## WhatsApp deep links

Formát pro všechny WA tlačítka:
```
https://wa.me/62XXXXXXXXXX?text=Hi%20Island%20Look!%20I%20would%20like%20to%20know%20more%20about%20your%20products.
```

Pro produktové karty přidat kontext:
```
https://wa.me/62XXXXXXXXXX?text=Hi!%20I%27m%20interested%20in%20your%20[kategorie].%20Can%20you%20tell%20me%20more?
```

---

## Technické požadavky

- **Čistý HTML/CSS/JS** — žádný framework, žádný build tool → snadný hosting (Netlify, Vercel, GitHub Pages)
- **Single file** nebo max `index.html` + `style.css` + `script.js`
- **Mobile-first** — turisté browsují na telefonu
- **Performance:** lazy loading obrázků, minifikované assety
- **Fonty:** Google Fonts (Cormorant Garamond + Josefin Sans)
- **Animace:** CSS transitions + Intersection Observer pro reveal efekty

---

## Jak začít v Claude Code

1. Otevři `island-look-v2.html` — to je schválený vizuální základ
2. Doplň WA číslo do všech odkazů
3. Až budeš mít fotky → nahraď placeholder divy za `<img>` tagy
4. Až budeš mít brandy → doplň do sekce #brands
5. Ověř / oprav Google Maps embed s přesnou adresou
6. Finální SEO check před deployem
