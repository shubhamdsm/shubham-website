# Shubham Yadav

Minimal personal website built with Astro.

## Local development

```bash
pnpm install
pnpm dev
```

## Build

```bash
pnpm build
```

The site is static, so it can be deployed easily to Vercel, Netlify, Cloudflare Pages, or GitHub Pages.

## GitHub Pages

This repo includes a GitHub Actions workflow at `.github/workflows/deploy.yml`.

1. Create a GitHub repo named `shubham-website`.
2. Push the `main` branch.
3. In GitHub, open Settings -> Pages.
4. Set Source to `GitHub Actions`.

The workflow builds Astro with:

```bash
SITE_URL=https://shubhamdsm.github.io
BASE_PATH=/shubham-website
pnpm build
```

After the action completes, the site should be available at:

```text
https://shubhamdsm.github.io/shubham-website/
```
