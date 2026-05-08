# baseflood.com

Static website for BaseFlood Engineering, PLLC — hosted on Cloudflare Pages.

**Live:** https://baseflood.com

## Stack

- Static HTML / CSS
- Cloudflare Pages (auto-deploy from `main` branch)
- Formspree for contact form

## Structure

```
├── index.html          # Home
├── about.html          # About
├── services.html       # Services
├── working-with-us.html
├── training.html
├── faq.html
├── resources.html
├── contact.html        # Contact (phone, address, form)
├── privacy.html
├── styles.css
└── images/
```

## Deployment

Pushes to `main` automatically deploy to Cloudflare Pages.
Custom domain: baseflood.com (DNS managed in Cloudflare).

## Contact Form

Uses [Formspree](https://formspree.io) — no backend required.
Form endpoint: configured in `contact.html`.
