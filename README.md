# CounterCore — Landing Site

Static site for the CounterCore product URL submitted to the Riot Developer Portal.

## Files

```
landing/
├── index.html          Landing page
├── privacy.html        Privacy policy page
├── styles.css          Shared styles (Tactical Obsidian design system)
├── fonts/
│   └── inter.woff2     Self-hosted Inter (copied from src/renderer/fonts/)
└── README.md           This file
```

**Zero build step.** Plain HTML + CSS. No compilation, no npm install, no framework.

---

## Deploy to Cloudflare Pages (chosen host)

1. Sign in at [dash.cloudflare.com](https://dash.cloudflare.com) → **Workers & Pages** →
   **Create application** → **Pages** tab → **Connect to Git**.
2. Authorize Cloudflare to access GitHub if prompted, then select the
   `Ikeem11/counter-core` repository → **Begin setup**.
3. **Project name:** `counter-core` (becomes the subdomain). Production branch: `main`.
4. **Build settings:**
   - Framework preset: **None**
   - Build command: *(leave blank)*
   - Build output directory: **`landing`**
   - Root directory (Advanced): *(leave blank — defaults to repo root)*
5. **Save and Deploy.**

Cloudflare publishes at `https://counter-core.pages.dev` (or a project-specific subdomain
shown after the first deploy). Every push to `main` triggers a redeploy automatically.

**Custom domain (optional):** Project → **Custom domains** → add `countercore.app` (or
whatever you buy). Cloudflare proxies HTTPS automatically; if the domain is registered at
Cloudflare it's a single click, otherwise add the CNAME at your DNS provider.

---

## Other deploy targets

- **GitHub Pages** (alternative): rename `landing/` → `docs/` and enable Pages with
  `main /docs`, or add a static-deploy GitHub Action that uploads `landing/` as the Pages
  artifact.
- **Netlify** (alternative): import the repo, publish directory = `landing`, build
  command blank.

---

## Before submitting to Riot Developer Portal

- Replace `https://countercore.app` with the real deployed URL everywhere in the portal form.
- Replace `https://countercore.app/privacy` with the real privacy page URL.
- Confirm the Riot disclaimer is visible on both pages (it is — it appears in the footer
  of `index.html` and `privacy.html`).
- Do not publish until Riot registration reaches "Approved" or "Acknowledged" status
  (`COMPLIANCE.md §8` pre-launch gate).
