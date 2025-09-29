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
- `public/styles/` — centralized CSS served at `/styles/*` (e.g., `/styles/global.css`).
- `assets/` — images and other static assets referenced by pages (e.g., `/assets/drop.png`).
- `plans.md` — kept in the repo root; the site links to it from `/plans` for now.
- `astro.config.mjs` — site configuration.

## Styling approach
- Global, framework-agnostic styles live in `public/styles/global.css` and are linked from pages that use basic HTML (e.g., `index.astro`).
- Tailwind demo pages load Tailwind via CDN and avoid the global CSS to prevent conflicts; they rely on utility classes for styling.
- Rationale: separate presentation from markup and provide a single place to manage tokens (colors, spacing, typography) and common components.

## Notes
- The `/plans` page currently links to the repository version of `plans.md` to keep things simple. We can render the Markdown in-site later using Astro content collections.
