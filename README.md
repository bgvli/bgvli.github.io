# BGVLI

**We build for builders.**

BGVLI is a studio for thoughtful apps, useful tools, and curious experiments. This repository contains the homepage at [bgvli.com](https://bgvli.com/), where apps will be discoverable as they launch on their own subdomains.

## Design

A minimal, editorial layout with a text-only wordmark, warm paper background, blue accents, translucent halos, and frosted app cards. The page adapts to desktop and mobile screens and respects reduced-motion preferences.

The app directory currently contains three “Coming soon” placeholders.

## Run locally

The site is plain HTML and CSS. No dependencies or build step are required.

From the repository root, run:

```sh
python3 -m http.server 8000
```

Open [localhost:8000](http://localhost:8000/). Stop the server with `Ctrl+C`.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | Homepage content, navigation, metadata, and structured data |
| `styles.css` | Responsive layout, typography, colors, and visual effects |
| `images/favicon.svg` | Text-based browser favicon |
| `images/social-card.png` | 1200 × 630 social sharing preview |
| `robots.txt` | Crawler access rules and sitemap location |
| `sitemap.xml` | Canonical homepage URL for search engines |
| `CNAME` | GitHub Pages custom domain: `bgvli.com` |

## Add an app

1. Replace a placeholder `<article class="app-card">` in `index.html` with the app’s name and a short description of what it helps people do.
2. Replace the placeholder label with an accurate release status and update its accessible label.
3. Add a descriptive link to the real app URL, such as `https://yourapp.bgvli.com/`. Use the app name in the link text and retain a visible keyboard focus indicator.
4. Check the card on mobile and desktop before publishing.

Each app’s hosting, subdomain DNS, and HTTPS must be configured separately. Adding a homepage card does not create or deploy an app.

## Search and sharing

The homepage includes a descriptive title and meta description, an HTTPS canonical URL, Open Graph and Twitter card metadata, and `Organization` and `WebSite` JSON-LD. Its content is rendered directly in HTML for crawlers.

Keep metadata and the social preview consistent with future content changes. Add new public pages on this domain to `sitemap.xml` as they launch; apps on other subdomains should manage their own indexing configuration.

After deployment, submit `https://bgvli.com/sitemap.xml` in Google Search Console and use URL Inspection to check indexing. Metadata and sitemaps support discovery but do not guarantee indexing or ranking.

## Publish

The homepage is hosted with GitHub Pages. Commit and push changes to the configured publishing branch (`main`) to trigger the existing Pages deployment. Keep `CNAME` intact to preserve the custom domain.
