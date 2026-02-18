# Fibrix LLP - ISP & MSO Website

Static website for **fibrixllp.org** - an Internet Service Provider & Multi-System Operator based in South 24 Parganas, West Bengal.

## Pages

| Page | File | Description |
|------|------|-------------|
| Home | `index.html` | Hero, services, broadband plans, hardware catalog, CTA |
| About Us | `about.html` | Company info, mission, vision, values, infrastructure |
| Contact Us | `contact.html` | Contact form & company details |
| Pay Bill / Subscribe | `checkout.html` | New connection signup & bill payment |
| Privacy Policy | `privacy-policy.html` | ISP-specific data & privacy practices |
| Terms & Conditions | `terms.html` | Service terms for broadband & hardware |
| Refund Policy | `refund-policy.html` | Refund & cancellation for services & hardware |

## Logos

- **Header:** `Fibrix Logo Style 1.png`
- **Footer:** `Fibrix Logo Style 2.png`

## Deploy to GitHub Pages

```bash
git init
git add .
git commit -m "Fibrix LLP website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git push -u origin main
```

Then: **Settings → Pages → Deploy from branch (main) → Save**

### Custom Domain DNS (at your domain registrar)

**A Records** (for fibrixllp.org):
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**CNAME** (for www):
```
www → YOUR_USERNAME.github.io
```

## Customisation Notes

- **Broadband plans & pricing:** Edit the plan cards in `index.html` and plan dropdown in `checkout.html`
- **Payment integration:** Checkout form is a UI template - integrate Razorpay/Stripe/PayU for live payments
- **Contact form:** Integrate with [Formspree](https://formspree.io) or [EmailJS](https://www.emailjs.com) to receive actual emails
- **Color scheme:** Based on brand color `#c11111` - edit CSS variables in `css/style.css`

## Tech Stack

- Pure HTML5 + CSS3 + vanilla JavaScript
- Google Fonts (Inter)
- No build tools or dependencies
- Fully responsive (mobile, tablet, desktop)
