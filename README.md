# Clay Alternatives (clayalternatives.tech)

SEO/AEO-first static microsite comparing Clay alternatives for GTM teams. Neutral editorial tone with CTAs to [Bitscale.ai](https://bitscale.ai).

## Structure

```
clayalternatives/
├── index.html                              # Pillar: Best Clay Alternatives (2026)
├── clay-vs-bitscale.html                   # Head-to-head comparison
├── clay-vs-apollo.html                     # Head-to-head comparison
├── clay-alternatives-for-agencies.html     # Use case: agencies
├── clay-alternatives-for-data-enrichment.html  # Use case: enrichment
├── assets/
│   ├── styles.css                          # Shared mobile-first stylesheet
│   └── og-image.svg                        # Social share placeholder
├── robots.txt
├── sitemap.xml
└── README.md
```

## Local preview

From this directory:

```bash
# Python 3
python3 -m http.server 8080

# Or npx (Node.js)
npx serve .
```

Open [http://localhost:8080](http://localhost:8080).

## Deploy

Static site — deploy the `clayalternatives/` folder to any static host:

- **Vercel:** set root directory to `clayalternatives`, no build command needed
- **Netlify:** publish directory = `clayalternatives`
- **Cloudflare Pages:** same as above
- **Any S3/NGINX/static host:** upload all files as-is

Point `clayalternatives.tech` DNS to your host and set the custom domain.

## SEO checklist (built in)

- Unique `<title>` and meta description per page
- Canonical URLs, Open Graph, Twitter Card tags
- JSON-LD: `Article`, `FAQPage`, `BreadcrumbList`, `ItemList` (pillar)
- Semantic HTML5 (`header`, `main`, `article`, `section`, `nav`, `footer`)
- Internal linking: pillar ↔ spokes
- `robots.txt` + `sitemap.xml`
- Mobile-first responsive CSS, accessible focus states
- No JavaScript required for content rendering

## Bitscale CTAs

All Bitscale links include UTM parameters:

```
utm_source=clayalternatives
utm_medium=referral
utm_campaign=clay-alt
```

Primary destinations:
- Homepage: `https://bitscale.ai/`
- Pricing: `https://bitscale.ai/pricing`
- Data enrichment: `https://bitscale.ai/solutions/lp-data-enrichment`

Links use `rel="noopener sponsored"` where appropriate.

## Before publishing — verify pricing

Pricing and feature claims change frequently. **Confirm all numbers against official vendor sites before going live:**

| Vendor   | Pricing page                    |
|----------|---------------------------------|
| Clay     | https://www.clay.com/pricing    |
| Bitscale | https://bitscale.ai/pricing     |
| Apollo   | https://www.apollo.io/pricing   |
| Cognism  | https://www.cognism.com/pricing |
| ZoomInfo | https://www.zoominfo.com/pricing|

Known discrepancies in third-party sources (as of June 2026):
- Bitscale Growth: cited as both ~$314/mo and ~$349/mo (annual billing)
- Clay Launch/Growth: cited as ~$185/$495 and other figures post-2026 overhaul

Keep pricing **qualitative** in copy unless you've verified the exact current rate.

## Adding new pages

1. Copy any spoke page as a template
2. Update `<title>`, meta description, canonical, OG tags, JSON-LD
3. Write unique content (do not duplicate the pillar)
4. Add breadcrumb linking back to `/`
5. Add entry to `sitemap.xml`
6. Link from pillar `#use-cases` section and footer nav

Suggested future spokes:
- `clay-vs-cognism.html`
- `clay-vs-zoominfo.html`
- `clay-alternatives-for-outbound.html`

## Replacing the OG image

Replace `assets/og-image.svg` with a 1200×630 PNG or JPG for best social platform compatibility. Update `og:image` and `twitter:image` meta tags in each HTML file if you change the filename.
