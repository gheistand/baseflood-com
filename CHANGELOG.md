# Changelog

## 2026-05-08 — Initial Launch (Migration from WordPress)

### Migration
- Decommissioned WordPress site hosted on Northwest Registered Agent (NWRA) at 66.223.49.89
- WordPress site archived to `gheistand/baseflood-wordpress-archive` (private) before cutover
- Moved static site content from `gheistand/gheistand-dev` → `baseflood/` into this dedicated repo
- Set up Cloudflare Pages project `baseflood-com`
- Added custom domains `baseflood.com` and `www.baseflood.com` to Pages project
- Updated Cloudflare DNS: deleted old NWRA A records, added CNAME records to Pages
- Configured GitHub Actions auto-deploy (`CLOUDFLARE_API_TOKEN` secret set)
- **Result:** https://baseflood.com live on Cloudflare Pages ✅

### Content Changes Applied
- Replaced all em dashes with regular dashes across all pages
- Removed: Storm Surge Modeling and all coastal flood / coastal zone references
- Removed: Substantial Improvement Analysis section
- Removed: Stormwater Engineering sections (about, services)
- Removed: Parallel Processing bullet (training)
- Removed: "Can you help with coastal flooding or storm surge?" FAQ item
- Fixed broken link: FEMA Guidance Documents → `/flood-maps/guidance-reports/guidelines-standards`
- Fixed broken link: LOMC Application Portal → `msc.fema.gov/portal/resources/lomc`
- Corrected FEMA review fees FAQ: LOMAs are free; LOMRs/CLOMRs carry $6,500–$9,000+ in FEMA fees
- Added phone (+1 217-689-5221) and office address (2501 Chatham Rd Suite N, Springfield IL 62704) to contact page
