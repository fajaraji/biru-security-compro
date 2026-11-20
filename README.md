# PT. Bangun Insan Reksa Utama (BIRU) — Security Services Company Profile

Bilingual Astro company profile for BIRU Security Services, with services, products, a photo gallery, and Indonesian and English pages.

## Explore the implementation

The site shares section components between its Indonesian and English routes. Start with the route for the language you want to change.

- [Indonesian homepage](src/pages/index.astro)
- [English homepage](src/pages/en/index.astro)
- [Services section](src/components/Services.astro)

## 🚀 Tech Stack

* **Framework**: [Astro](https://astro.build/) (Static Site Generator)
* **Styling**: [Tailwind CSS v4](https://tailwindcss.com/) (Mobile-First approach)
* **Icons**: `@lucide/astro` (Vektor SVG)

## ✨ Key Features

1. **High Performance**: Pre-rendered static pages with minimal client-side JavaScript for rapid loading times and optimal SEO.
2. **Multilingual Support (i18n)**: Fully localized static routing supporting:
   - Bahasa Indonesia (Default): `/`
   - English: `/en/`
3. **Accessibility (WCAG 2.1 AA Compliance)**:
   - **Color Contrast**: Complies with the 4.5:1 ratio minimum (utilizes a high-contrast White text `#FFFFFF` on Deep Security Blue `#004F9F` background with a contrast ratio of **6.55:1**).
   - **Touch Targets**: All interactive elements (buttons, links, language switchers) have a minimum click area of **44 x 44px**.
   - **Keyboard Navigation**: Enhanced focus indicators (`focus-visible:ring-2`) for all links and buttons.
4. **Custom Services Redesign**: Visual card-based presentation for all 9 core services using official transparent card image assets and security-focused copywriting.
5. **Infinite Scroll Snap Carousels**:
   - **Operational Gallery**: Loops through 10 official operational GIFs seamlessly.
   - **Clients Carousel**: Displays 10 client logos in full color without boxes, with responsive grid columns (6 on desktop, 4 on tablet, 2 on mobile) and infinite wrap-around navigation.
6. **Sticky Navigation & Dark Footer**: Features clean, sticky header controls and a simplified 3-column dark footer.

## 📁 Directory Structure

```text
/
├── public/
│   └── images/
│       ├── logo biru security.png      # Official company logo
│       ├── logo card/                  # Service card images
│       └── logo klien/                 # Client logo PNGs (transparent)
├── src/
│   ├── components/                     # Modular UI components (Hero, Services, WhyUs, Gallery, etc.)
│   ├── layouts/                        # Base page layout & SEO metadata
│   ├── pages/                          # Astro page routes (index.astro, en/index.astro)
│   └── styles/                         # Global Tailwind v4 styles
└── package.json
```

## Local development

All commands are run from the project root:

| Command | Action |
| :--- | :--- |
| `npm install` | Installs dependencies |
| `npm run dev` | Starts local development server at `http://localhost:4321` |
| `npm run build` | Builds the production static site into `./dist/` |
| `npm run preview` | Previews the built production site locally |
