# Portfolio site (single static page)

Files: `index.html`, `vercel.json`, `robots.txt`, `sitemap.xml`, `assets/` (screenshots + public CVs).
No build step and no dependencies. Fonts load from Google Fonts (non-blocking).

**Personal documents do not live here.** Cover letters, LinkedIn plans and the job tracker are in `../job-search-docs/`. Public CV PDFs only under `assets/cv/`.

## Hosting: Vercel + Cloudflare DNS

Domain DNS is on **Cloudflare**. This portfolio deploys from GitHub → **Vercel** at `gedeon.ndundecode.com`.

1. Push **only this folder** (never `../job-search-docs`).
2. Vercel project root = this repo. Framework: Other. Empty build/output.
3. Domain: `gedeon.ndundecode.com` (CNAME to Vercel in Cloudflare).

## Before you publish

- Contact email: built at the bottom of `index.html` from `parts` (`gedeon.gibango` + `gmail.com`). Change if you use another address.
- Screenshots: `assets/nducore.jpg`, `ndulearn.jpg`, `nducare.jpg` (keep each under ~150KB).
- Keep OpenFactor and client work off this site.
- After deploy: submit `https://gedeon.ndundecode.com/sitemap.xml` in Google Search Console once.
