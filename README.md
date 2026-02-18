# Fibrix Broadband - Website

Official website for **[fibrixllp.org](https://fibrixllp.org)** - Fibrix Broadband, a broadband internet and networking hardware provider based in Joynagar Mojilpur, South 24 Parganas, West Bengal.

**Fibrix Broadband** is the brand name of **Fibrix LLP** (LLP ID: ACT-8822).

## Pages

| Page | File | Description |
|------|------|-------------|
| Home | `index.html` | Hero, services, broadband plans, hardware catalog, CTA |
| About Us | `about.html` | Company info, team, mission ("Internet for All"), vision, values |
| Contact Us | `contact.html` | Contact form (Google Form integration) & company details |
| Privacy Policy | `privacy-policy.html` | Data collection, usage, and privacy practices |
| Terms & Conditions | `terms.html` | Service terms for broadband & hardware |
| Refund Policy | `refund-policy.html` | Refund & cancellation for services & hardware |

## Broadband Plans

| Plan | Speed | Price (incl. GST) |
|------|-------|--------------------|
| Start 30 | 30 Mbps | Rs.250/month |
| Connect 40 | 40 Mbps | Rs.330/month |
| Family 60 | 60 Mbps | Rs.430/month |
| Power 80 (Most Popular) | 80 Mbps | Rs.520/month |
| Turbo 100 | 100 Mbps | Rs.600/month |

## Logos

- **Header / Favicon:** `Fibrix Logo Style 1.png`
- **Footer:** `Fibrix Logo Style 2.png`

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

Bill payments are handled externally at **[pay.fibrixllp.org](https://pay.fibrixllp.org)**.

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

- `robots.txt` - allows all crawlers, points to sitemap
- `sitemap.xml` - all 6 pages with priorities
- Open Graph meta tags on all pages for social sharing previews

## Customisation

- **Broadband plans & pricing:** Edit plan cards in `index.html`
- **Brand color:** `#c11111` - edit CSS variables in `css/style.css`
- **Contact form:** Update Google Form entry IDs in `contact.html` if form fields change

## Tech Stack

- Pure HTML5 + CSS3 + vanilla JavaScript
- Google Fonts (Inter)
- GitHub Pages hosting
- Google Forms backend for contact form

## Team

- **Papia Banerjee** - Partner
- **Jibesh Mahato** - Partner
- **Shourjo Banerjee** - Head of Operations
