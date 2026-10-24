# IngeniousClan

Astro v3 static site (single page) with Tailwind CSS, managed with pnpm.

## Commands

All run with pnpm (lockfile: `pnpm-lock.yaml`):

- `pnpm dev` — start dev server
- `pnpm build` — production build to `dist/`
- `pnpm preview` — preview production build locally
- `pnpm astro` — Astro CLI

No test framework, linter, or formatter is configured. Do not invent `test`, `lint`, or `format` scripts.

## Project structure

- `src/pages/index.astro` — the only page / entrypoint
- `src/layouts/Layout.astro` — wraps all pages (import it in frontmatter)
- `src/components/{shared,sections,elements,cards,blocks}` — section/page components, shared UI, and cards
- `public/` — static assets served at site root (e.g. `public/llms.txt` serves at `/llms.txt`)
- `favicon/`, `images/` live under `public/`

## Config notes

- `tsconfig.json` extends `astro/tsconfigs/strict` — no custom TS rules to add
- `tailwind.config.cjs` — `darkMode: "class"`, custom `midmd` screen (`880px`), content glob covers `.astro`, `.html`, `.js`, `.jsx`, `.md`, `.mdx`, `.svelte`, `.ts`, `.tsx`, `.vue`
- `astro.config.mjs` — only integration is `@astrojs/tailwind`
- `kilo.json` at root enables `web-design-guidelines` and `vercel-react-best-practices` skills

## Style

- Astro frontmatter uses `---` fences; components are `.astro` (no React/Vue in this repo)
- Tailwind utility classes inline; custom CSS variables referenced via `rgb(var(--...))` in `tailwind.config.cjs`
