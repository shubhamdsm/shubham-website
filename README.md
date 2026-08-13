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

## Deploy to shubh.wtf

This site deploys to [Vercel](https://vercel.com) from the `main` branch. Pushes to `main` go live automatically after DNS is configured.

### 1. Connect Vercel to GitHub

1. Sign in at [vercel.com](https://vercel.com) with GitHub.
2. Import `shubhamdsm/shubham-website`.
3. Keep defaults: framework **Astro**, build command `pnpm build`, output directory `dist`.
4. Add the domain `shubh.wtf` (and optionally `www.shubh.wtf`) under **Project → Settings → Domains**.

### 2. Namecheap DNS records

In Namecheap: **Domain List → shubh.wtf → Manage → Advanced DNS**.

| Type  | Host | Value                 | TTL  |
|-------|------|-----------------------|------|
| A     | `@`  | `76.76.21.21`         | Auto |
| CNAME | `www`| `cname.vercel-dns.com`| Auto |

Remove any old GitHub Pages A/CNAME records if they exist.

DNS can take up to an hour to propagate. Vercel issues SSL automatically once DNS resolves.

### 3. Verify

After deploy finishes, open [https://shubh.wtf](https://shubh.wtf). `www.shubh.wtf` redirects to the apex domain.
