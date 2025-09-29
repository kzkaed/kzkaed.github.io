# kzkaed.github.io

A minimal Astro site configured for GitHub Pages.

## Quick start
- Prereqs: Node.js 20+
- Install: `npm ci`
- Dev: `npm run dev` then open http://localhost:4321
- Build: `npm run build` (outputs to `dist/`)

## Deploy (GitHub Pages via Actions)
This repo includes a workflow at `.github/workflows/deploy.yml` that:
- Builds the site on pushes to `main`.
- Publishes the built `dist/` to GitHub Pages.

One-time setup in GitHub:
1. Settings → Pages → Build and deployment → Source: GitHub Actions.
2. Merge to `main` and the workflow will publish. First deploy may take a minute.

Site URL: https://kzkaed.github.io

## Project structure
- `src/pages/` — routes. Edit `index.astro` to change the home page.
- `plans.md` — kept in the repo root; the site links to it from `/plans` for now.
- `astro.config.mjs` — site configuration.

## Notes
- The `/plans` page currently links to the repository version of `plans.md` to keep things simple. We can render the Markdown in-site later using Astro content collections.
