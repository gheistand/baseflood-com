# baseflood.com

Static website for BaseFlood Engineering, PLLC — hosted on Cloudflare Pages.

**Live:** https://baseflood.com ✅  
**Pages URL:** https://baseflood-com.pages.dev  
**Status:** Production — auto-deploys on push to `main`

---

## Stack

| Layer | Tech |
|---|---|
| Hosting | Cloudflare Pages |
| Content | Static HTML / CSS |
| Contact form | Formspree |
| CI/CD | GitHub Actions (deploy on push to `main`) |
| DNS | Cloudflare (baseflood.com) |
| Email | Microsoft 365 (separate — do not touch DNS MX/SPF/DKIM) |

---

## Site Structure

```
├── index.html           # Home — "The Specialist's Specialist for FEMA Compliance"
├── about.html           # About the firm
├── services.html        # FEMA map revisions, hydraulic modeling, regulatory compliance
├── working-with-us.html # How the engagement process works
├── training.html        # Training offerings
├── faq.html             # Frequently asked questions
├── resources.html       # FEMA links, modeling tools, references
├── contact.html         # Contact form, phone, address
├── privacy.html         # Privacy policy & terms
├── styles.css
└── images/
```

---

## Deployment

### Automatic (GitHub Actions)
Every push to `main` triggers a deploy via `.github/workflows/deploy.yml`.
`CLOUDFLARE_API_TOKEN` repo secret is set ✅ — no further setup needed.

### Manual
```bash
cd ~/Projects/baseflood-com
npx wrangler pages deploy . --project-name baseflood-com --branch main
```

---

## DNS Setup (Cloudflare)

The domain is managed in Cloudflare DNS. Required records for the Pages deployment:

| Type | Name | Content | Proxied |
|---|---|---|---|
| CNAME | `@` | `baseflood-com.pages.dev` | Yes ✅ |
| CNAME | `www` | `baseflood-com.pages.dev` | Yes ✅ |

**Do not remove these M365 email records:**

| Type | Name | Content |
|---|---|---|
| MX | `@` | `baseflood-com.mail.protection.outlook.com` |
| TXT | `@` | `v=spf1 include:spf.protection.outlook.com ~all` |
| CNAME | `selector1._domainkey` | *(M365 DKIM)* |
| CNAME | `selector2._domainkey` | *(M365 DKIM)* |

---

## Contact

- **Address:** 2501 Chatham Rd, Suite N, Springfield, IL 62704
- **Phone:** +1 (217) 689-5221
- **Email:** info@baseflood.com (M365)
- **Contact form:** Formspree endpoint configured in `contact.html`

---

## Content Notes

- No founder bio or individual credentials — brand is the firm (conflict of interest w/ ISWS role)
- No coastal/storm surge content — riverine and pluvial focus only
- FEMA fee info: LOMAs are free; LOMRs/CLOMRs carry review fees of $6,500–$9,000+

---

## Related Repos

| Repo | Purpose |
|---|---|
| `gheistand/baseflood-wordpress-archive` | Static mirror of original WordPress site (private) |
| `gheistand/gheistand-dev` | Personal site; baseflood/ subdirectory was the draft source |
