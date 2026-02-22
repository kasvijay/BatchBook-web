# BatchBook Website — Agent Context

## Project Overview
- **Domain**: zuniclabs.com (bought on GoDaddy, nameservers changed to Cloudflare)
- **Hosting**: Cloudflare Pages (free tier — static site auto-deploy on git push)
- **Site type**: Plain HTML/CSS/JS (no build framework)
- **Brand**: ZunicLabs — "Simple tools for everyday work"
- **Product**: BatchBook — tuition management app for teachers

## Deployment
- **Method**: GitHub repo connected to Cloudflare Pages
- **Branch**: `main` triggers production deploy
- **Build command**: (none — plain HTML)
- **Output directory**: `/`
- **Preview deploys**: Any non-main branch auto-generates a preview URL

## Site Structure (existing, from `../web/`)
```
/ (index.html)              → ZunicLabs landing page
/batchbook/download/        → BatchBook download page
/batchbook/privacy/         → BatchBook privacy policy
```

## Domain Setup
- GoDaddy domain: zuniclabs.com
- Nameservers: Already pointing to Cloudflare
- SSL: Auto-provisioned by Cloudflare (free)

## Preferences
- Keep it simple — plain HTML, no frameworks unless needed
- Offline-first philosophy for products
- Clean, minimal design using Inter font family
