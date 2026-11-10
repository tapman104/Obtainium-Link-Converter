# Obtainium Link Converter

Single-page tool that turns GitHub, IzzyOnDroid, or F-Droid sources into shareable one-tap Obtainium import links.

## Files

| File | Purpose |
|------|---------|
| `auto.html` | Converter UI and logic (self-contained, no build step) |
| `_redirects` | Cloudflare Pages rewrite: serves the converter at the root URL `/` |
| `wrangler.toml` | Wrangler config for local dev (`wrangler pages dev .`) and deploys |
| `README.md` | This file |

## Deploy to Cloudflare Pages

### Option A: Connect GitHub (recommended)

1. Push `auto.html` and `README.md` to a GitHub repository.
2. In Cloudflare Dashboard, go to **Workers & Pages** → **Create application** → **Pages** → **Connect to Git**.
3. Select your repository.
4. Build settings:
   - **Framework preset:** `None`
   - **Build command:** (leave empty)
   - **Build output directory:** `/`
5. Click **Save and Deploy**.

### Option B: Direct upload

1. Go to **Workers & Pages** → **Create application** → **Pages** → **Upload assets**.
2. Drag and drop `auto.html` (and `README.md` if you want it in the repo).
3. Deploy.

## Serving at the root URL

A `_redirects` file is included, so the converter is served at the root URL out of the box:

```
https://your-project.pages.dev/
```

The redirect rewrites `/` to `/auto.html` with a `200`, so existing links to `/auto.html` keep working too. No renaming or build step is required.

## Local preview

If you have [Wrangler](https://developers.cloudflare.com/workers/wrangler/) installed:

```bash
wrangler pages dev .
```

Then open `http://localhost:5173`.

## Analytics

No analytics are included. If you want to add them later, enable **Cloudflare Web Analytics** in the Pages dashboard — it's cookie-free and requires no code changes.