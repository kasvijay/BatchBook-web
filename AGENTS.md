# BatchBook Website — Agent Context

## Project Overview
- **Domain**: zuniclabs.com (bought on GoDaddy, nameservers changed to Cloudflare)
- **Hosting**: Cloudflare Worker with static assets (auto-deploy on git push)
- **Site type**: Plain HTML/CSS/JS (no build framework)
- **Brand**: ZunicLabs — "Simple tools for everyday work"
- **Product**: BatchBook — tuition management app for home tutors in India

## GitHub
- **Repo**: `kasvijay/BatchBook-web` (public)
- **Branch**: `main` triggers production deploy
- **Note**: Separate from the main `kasvijay/BatchBook` repo (which has android, ios, backend, etc.)

## Deployment
- **Platform**: Cloudflare Workers (not Pages — created via dashboard "Create a Worker" flow)
- **Cloudflare account**: zuniclabs@gmail.com
- **Account ID**: c2d7d1228c917c8def44fea71ce93e30
- **Worker name**: `batchbook-web`
- **Workers URL**: https://batchbook-web.zuniclabs.workers.dev
- **Config**: `wrangler.jsonc` in repo root — serves `./` as static assets
- **Build command**: `npx wrangler deploy` (auto-run by Cloudflare on push)
- **API token**: "ZunicLabs-website" — has Cloudflare Pages:Edit, Zone DNS:Edit, Account Settings:Read permissions. **Only use for this project.**

## Site Structure
```
/ (index.html)              → ZunicLabs landing page
/batchbook/download/        → BatchBook download page
/batchbook/privacy/         → BatchBook privacy policy
```

## Domain Setup
- **Registrar**: GoDaddy
- **Domain**: zuniclabs.com
- **Nameservers**: Pointing to Cloudflare
- **Custom domain**: zuniclabs.com added to the Worker
- **Zone ID**: 4ad8fa24ae3f874dd665999f589cb899
- **SSL**: Auto-provisioned by Cloudflare (Let's Encrypt)
- **Old A records**: Deleted (were pointing to 13.248.243.5 and 76.223.105.230)
- **Legacy domain**: zuniqlabs.com (with 'q') — has the same site content

## Workflow
```bash
# Make changes locally
git add .
git commit -m "Update something"
git push
# → Cloudflare auto-deploys in 1-3 minutes
```

## Known Issues
- App Store link has placeholder `id__APPSTORE_ID__` — update once iOS app is listed

## Preferences
- Keep it simple — plain HTML, no frameworks unless needed
- Offline-first philosophy for products
- Clean, minimal design using Inter font family
