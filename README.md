# Fibrix Broadband - Website

Official website for **[fibrixllp.org](https://fibrixllp.org)** - Fibrix Broadband, a broadband internet, IPTV, and networking hardware provider based in Joynagar Mojilpur, South 24 Parganas, West Bengal.

**Fibrix Broadband** is the brand name of **Fibrix LLP** (LLP ID: ACT-8822).

## Pages

| Page | File | Description |
|------|------|-------------|
| Home | `index.html` | Hero, services, broadband plans (4 duration tabs), hardware catalog, CTA |
| OTT Bundles | `ott.html` | All OTT streaming bundles, platforms, pricing, FAQs |
| IPTV Plans | `iptv.html` | IPTV channel packages, pricing, device compatibility, setup |
| About Us | `about.html` | Company info, team, mission ("Internet for All"), vision, values |
| Contact Us | `contact.html` | Contact form (Google Form integration) & company details |
| Privacy Policy | `privacy-policy.html` | Data collection, usage, and privacy practices |
| Terms & Conditions | `terms.html` | Service terms for broadband & hardware |
| Refund Policy | `refund-policy.html` | Refund & cancellation for services & hardware |
| Blog | `blog.html` | Blog listing page with latest posts (Jekyll Liquid loop) |
| Blog Posts | `_posts/*.md` | Markdown blog articles (Jekyll + Decap CMS) |

## Broadband Plans

Plans are available in **Monthly**, **Quarterly (90 days)**, **Half-Yearly (180 days)**, and **Yearly (365 days)** durations with tabbed UI.

### Monthly Plans

| Plan | Speed | Price (incl. GST) |
|------|-------|--------------------|
| Connect 40 | 40 Mbps | ₹330/mo |
| Family 60 | 60 Mbps | ₹430/mo |
| Power 80 (Most Popular) | 80 Mbps | ₹530/mo |
| Turbo 100 | 100 Mbps | ₹600/mo |
| OTT + 30 | 30 Mbps | ₹550/mo |
| OTT + 60 | 60 Mbps | ₹650/mo |
| OTT + 80 | 80 Mbps | ₹750/mo |
| OTT + 100 | 100 Mbps | ₹820/mo |

Additional quarterly, half-yearly, and yearly pricing available on the website.

## IPTV Packages

| Package | Channels | Price (incl. GST) |
|---------|----------|--------------------|
| HD | 49 | ₹90/mo |
| HD+ | 56 | ₹120/mo |
| ACE HD | 74 | ₹150/mo |
| AXEL HD (Popular) | 95 | ₹200/mo |

Each package is available in 4 regional variants: Hindi, Marathi, Gujarati & Bangla. Channel lists are grouped by category (Entertainment, Movies, Kids, Sports, Infotainment, News, etc.) with expandable dropdowns. Channel data sourced from `iptvchannel.csv`.

### Channel Search

A search bar above the IPTV cards lets users find any channel and see which packs include it. Typing a channel name (min 2 chars) displays a results table with ✓/✗ availability across all 4 packages, helping users decide which pack to choose.

## OTT Platforms

Included with select broadband plans:

- **Premium OTT Pack** — 29 platforms
- **Prime Plus OTT Pack** — 27 platforms

## Networking Hardware

Listed as a catalog (no e-commerce): Routers & Switches, ONU/ONT Devices, GPON/EPON OLT, Fiber Optic Cables, Patch Cords & Connectors, Set-Top Boxes.

## Project Structure


```
fibrixllp.github.io/
├── _config.yml                 (Jekyll configuration)
├── _data/
│   └── authors.yml             (Multi-author data: shourjo, arka)
├── _includes/
│   ├── head.html               (Parameterised <head> with SEO)
│   ├── header.html             (Nav with active page detection)
│   ├── footer.html             (4-column footer)
│   ├── scripts.html            (Common JS: menu, header, loader, dark mode)
│   ├── jsonld-homepage.html    (LocalBusiness structured data)
│   ├── reading-time.html       (Auto reading time calc)
│   ├── share-buttons.html      (WhatsApp, Facebook, X sharing)
│   └── related-posts.html      (2 related posts by category)
├── _layouts/
│   ├── default.html            (Base HTML shell)
│   ├── page.html               (Standard pages with page-header)
│   └── post.html               (Blog post with author, tags, sharing)
├── _posts/
│   ├── 2026-01-15-welcome-to-fibrix-broadband.md
│   ├── 2026-01-20-choosing-the-right-broadband-plan.md
│   └── 2026-01-28-what-is-iptv-and-why-you-need-it.md
├── admin/
│   ├── index.html              (Decap CMS admin panel)
│   └── config.yml              (CMS collections & fields)
├── assets/
│   ├── css/
│   │   └── style.css
│   └── images/
│       ├── authors/            (Author avatars)
│       ├── blog/               (Blog featured images)
│       ├── logo-primary.png    (Header & favicon)
│       └── logo-footer.png     (Footer)
├── data/
│   └── iptvchannel.csv         (IPTV channel data source)
├── index.html
├── ott.html                    (OTT bundles page)
├── iptv.html                   (IPTV plans page)
├── about.html
├── contact.html
├── blog.html                   (Liquid loop for post cards)
├── privacy-policy.html
├── terms.html
├── refund-policy.html
├── feed.xml                    (RSS feed — auto-generated)
├── Gemfile                     (Jekyll dependencies)
├── manifest.json               (PWA manifest)
├── sw.js                       (Service worker)
├── CNAME
├── robots.txt
├── sitemap.xml                 (Auto-generated with Liquid)
└── README.md
```

## Logos

- **Header / Favicon:** `assets/images/logo-primary.png`
- **Footer:** `assets/images/logo-footer.png`

## Contact Form

The contact form submits to a Google Form via `fetch` (no-cors POST). Entry IDs:

| Website Field | Google Form Entry ID |
|---------------|----------------------|
| First Name | `entry.1423676904` |
| Last Name | `entry.1657985535` |
| Email Address | `entry.291522330` |
| Phone Number | `entry.350177398` |
| Subject | `entry.1065936945` |
| Message | `entry.1467988090` |

## Payment Portal

Bill payments are handled externally at **[pay.fibrixllp.org](https://pay.fibrixllp.org/customer_portal)**.

## UI Features

- **Collapsible header** — hides on scroll down, shows on scroll up (all pages, all screen sizes)
- **Navigation** — Home, IPTV, OTT, About Us, Contact Us, Blog, Pay Bill (IPTV & OTT link to homepage anchors from other pages)
- **Dark mode** — moon/sun toggle in header, persisted via localStorage, respects `prefers-color-scheme`
- **Page loader** — spinner overlay that fades out on page load
- **Scroll reveal** — sections animate in as they enter the viewport (IntersectionObserver)
- **Plan duration tabs** — pill-style Monthly / Quarterly / Half-Yearly / Yearly switcher
- **OTT platform tabs** — Premium / Prime Plus toggle with text-only grid
- **IPTV expandable cards** — "View Channel List" button reveals categorised channel grid per package
- **IPTV channel search** — real-time search bar to look up any channel across all 4 packs with ✓/✗ availability table
- **Hardware list cards** — numbered cards with red accent border, no images
- **WhatsApp integration** — floating chat button on all pages
- **Mobile-first responsive** — hamburger nav, stacked grids, optimised touch targets
- **Blog** — Jekyll-powered blog with multi-author support, reading time, social sharing, related posts, tags, and featured images
- **Decap CMS** — visual blog editor at `/admin/` for creating and editing posts via GitHub
- **PWA installable** — manifest.json + service worker for offline caching and Add to Home Screen

## Hosting & Deployment

Hosted on **GitHub Pages** with a custom domain.

- **Repository:** `shourjo-h/fibrixllp.github.io`
- **Branch:** `main`
- **Custom domain:** `fibrixllp.org`
- **CNAME file:** included

### DNS Configuration

**A Records** (for fibrixllp.org):
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**CNAME** (for www):
```
www -> shourjo-h.github.io
```

## SEO

- `robots.txt` — allows all crawlers, points to sitemap
- `sitemap.xml` — all pages + auto-generated blog post URLs via Liquid
- `feed.xml` — RSS feed for blog posts
- `<link rel="canonical">` on every page
- Open Graph meta tags on all pages (title, description, type, url, image, site_name)
- Twitter Card meta tags on all pages (summary_large_image)
- JSON-LD LocalBusiness structured data on homepage (name, address, phone, services, area served)
- Semantic `<title>` tags per page

## Customisation

- **Broadband plans & pricing:** Edit plan cards in `index.html` (inside `.plan-tab-content` divs)
- **IPTV packages:** Edit IPTV cards in `index.html` (inside `#iptv` section); update `data/iptvchannel.csv` for reference
- **Brand color:** `#c11111` — edit CSS variables in `assets/css/style.css`
- **Contact form:** Update Google Form entry IDs in `contact.html` if form fields change

## Tech Stack

- **Jekyll** — static site generator (GitHub Pages native)
- **Decap CMS** — visual content management (GitHub backend, PKCE auth)
- HTML5 + CSS3 + vanilla JavaScript
- Google Fonts (Inter, weights 400–800)
- GitHub Pages hosting
- Google Forms backend for contact form
- PWA (Progressive Web App) with service worker (`sw.js`) and `manifest.json`
- RSS feed (`feed.xml`)

## Team

- **Papia Banerjee** — Partner
- **Jibesh Mahato** — Partner
