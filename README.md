# Portfolio site (single static page)

Files: `index.html` (the whole site), `vercel.json` (security headers), `robots.txt`, `assets/` (product screenshots when ready).
No build step and no dependencies. Fonts load from Google Fonts.

**Personal documents do not live here.** CVs, cover letters, LinkedIn plans and the job tracker are in the sibling folder `../job-search-docs/`. Do not move them back into this directory. `.gitignore` and `.vercelignore` also block `docs/`, `.docx`, `.xlsx` and `.pdf` from git and Vercel uploads.

## Hosting: Vercel + Bluehost DNS (recommended)

Keep **ndundecode.com registered / DNS on Bluehost**. Host this portfolio on **Vercel**.

Why: Vercel is better for a static portfolio (free HTTPS, CDN, git deploy, no PHP shared-hosting friction). Bluehost is fine as the place your domain’s DNS lives. You do **not** need to move the domain away from Bluehost to use Vercel.

1. Create a GitHub repo and push **only this folder** (never `../job-search-docs`).
2. Vercel → Add New → Project → import. Framework: Other. Empty build/output. Deploy.
3. Vercel → Domains → add `gedeon.ndundecode.com`.
4. In **Bluehost DNS**, add the CNAME Vercel shows (usually name `gedeon`, value from Vercel).
5. Wait for DNS; Vercel issues HTTPS. Test phone + laptop.

## Before you publish: personal checks

- Contact email: `index.html` builds the address from two parts near the bottom of the file
  (`var parts = ["gedeon.gibango", "gmail.com"]`). Change it if you set up an address on your own domain.
- Product screenshots: drop `nducore.png`, `ndulearn.png`, `nducare.png` into `assets/` (see `assets/README.md`). Empty frames show until the files exist.
- Keep OpenFactor and client work off this site. The page already says it is confidential.
- Search engines: `robots.txt` allows indexing so recruiters can find you. To keep the site unlisted for now,
  replace its contents with `User-agent: *` and `Disallow: /`, and add
  `<meta name="robots" content="noindex">` inside `<head>`. Remove both when you are ready.
- Update the "Open to" line and the Lead role end date (Nov 2026) when your situation changes.
