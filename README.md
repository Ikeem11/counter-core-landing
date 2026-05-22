# CounterCore — Landing Site

Public landing site for **CounterCore**, the League of Legends adaptive counter-build
overlay app. The main app repository lives privately at
[`Ikeem11/counter-core`](https://github.com/Ikeem11/counter-core); this repo holds only
the marketing site so it can be served by GitHub Pages on the free plan.

This site is the public **Product URL** submitted to the Riot Games Developer Portal
(`SPEC.md §11` / `DEVELOPER-PORTAL-REGISTRATION.md` in the main repo).

## Files

```
.
├── index.html          Landing page
├── privacy.html        Privacy policy page
├── styles.css          Shared styles (Tactical Obsidian design system)
├── fonts/
│   └── inter.woff2     Self-hosted Inter
└── README.md           This file
```

**Zero build step.** Plain HTML + CSS. No compilation, no `npm install`, no framework.

## Compliance

- Self-hosted Inter font only — **no third-party CDN / external network call at runtime.**
- Exact Riot disclaimer from `COMPLIANCE.md §6` (main repo) appears in the footer of both
  pages.
- "Coming Soon" CTA — no fake download link, no fake testimonials.
- Brand is distinct from Riot / League of Legends UI per `COMPLIANCE.md §6`.

## Deploy (GitHub Pages)

1. Repo Settings → **Pages**.
2. **Source:** `Deploy from a branch`.
3. **Branch:** `main`, **folder:** `/ (root)`. Save.
4. Site goes live at `https://ikeem11.github.io/counter-core-landing/` (~1 min).

Every push to `main` redeploys automatically.

## Custom domain (optional)

Add a `CNAME` file at the repo root containing the domain (e.g. `countercore.app`), then
point DNS at GitHub Pages (`ikeem11.github.io`).

## URLs used in the Riot Developer Portal submission

- **Product URL:** <https://ikeem11.github.io/counter-core-landing/>
- **Privacy policy URL:** <https://ikeem11.github.io/counter-core-landing/privacy.html>
- Riot disclaimer is in the footer of both pages (`index.html`, `privacy.html`).
- Do not publish the app until Riot registration reaches **"Approved" / "Acknowledged"**
  status (`COMPLIANCE.md §8` pre-launch gate in the main repo).
