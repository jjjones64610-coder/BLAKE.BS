# BLAKE.BS

A small Vite + React + TypeScript project scaffolded as a web design preview. This folder contains a React app (with Tailwind/shadcn-ui patterns) alongside a couple of static preview HTML files. Use this README to run, develop, and build the project.

---

## Contents / Overview

- App entry: `main.tsx` → mounts `App.tsx`
- Routing: `App.tsx` uses React Router; main page component is `pages/Index`
- UI components: `src/components/*` (includes `ui` subcomponents)
- Static previews: `index_Version2.html`, `index-2.html` — simple static preview files you can open directly
- Vite config: `vite.config.ts` — dev server configured to run on port 8080 by default and uses `@vitejs/plugin-react-swc`
- Example helper files: `gitignore.txt`, other assets

---

## Technologies

- Vite (dev server and build)
- TypeScript
- React
- Tailwind CSS (utility styles)
- shadcn-ui style components patterns
- TanStack React Query (@tanstack/react-query)
- React Router
- Sonner/Toaster UI used for notifications
- Other third-party components (e.g., `input-otp`, `lucide-react`)

---

## Prerequisites

- Node.js (Recommended: Node 16+; Node 18+ is preferred)
- npm (or yarn / pnpm)
- A terminal + Git if you plan to work locally

---

## Quick start (local development)

1. Clone repository and open the BLAKE.BS folder:
   - git clone <YOUR_REPO_URL>
   - cd BLAKE.BS

2. Install dependencies:
   - npm install
   - (or `yarn` / `pnpm install`)

3. Start dev server:
   - npm run dev
   - By default Vite is configured to serve on port 8080 (see `vite.config.ts`). If your script differs, use the script that runs Vite.

4. Open in browser:
   - http://localhost:8080 (or the URL displayed in the terminal)

Note: If you only want to preview the static HTML, open `index_Version2.html` or `index-2.html` in a browser. Those are standalone static preview pages and do not require a dev server.

---

## Available scripts (typical)

These are the usual scripts for a Vite-based project. If your repo already has a `package.json`, use the exact scripts defined there. If not, these are the expected commands:

- npm run dev — start Vite dev server
- npm run build — produce production build (dist/)
- npm run preview — locally preview the built production bundle

---

## Build & Deploy

1. Build:
   - npm run build

2. Preview build locally:
   - npm run preview

3. Deploy:
   - The built output (commonly `dist/`) is static and can be deployed to any static host (Netlify, Vercel, GitHub Pages, S3, Cloudflare Pages, etc.)
   - Alternatively, if you use Lovable or another platform that expects a specific structure, place the production build files into the location required by that platform.

---

## Project structure (high level)

- BLAKE.BS/
  - src/
    - components/ — UI components, organized into subfolders (ui, layout, sections)
    - pages/ — route pages (Index, NotFound, etc.)
    - index.css (global styles) — imported by `main.tsx`
    - main.tsx — React entry
    - App.tsx — app composition and routing
  - vite.config.ts — Vite configuration (aliases, plugins, dev server)
  - index_Version2.html, index-2.html — static previews
  - gitignore.txt

---

## Notes & troubleshooting

- If the dev server fails to start, check:
  - Node version
  - Dependencies successfully installed
  - That `index.css` and other imported files exist at the expected paths
- Some components rely on third-party packages (e.g., `input-otp`, `lucide-react`, `@tanstack/react-query`). Make sure `npm install` completed without errors.
- If you use TypeScript and see type errors from third-party libs, try installing appropriate types or adjust tsconfig as needed.
- The Vite config sets `host: "::"` and `port: 8080`. If those conflict with your environment, change them in `vite.config.ts` or set environment variables.

---

## Contributing

- Edit files directly in your IDE or GitHub:
  - Clone, create a branch, make changes, run the dev server, and open a PR.
- If you use Lovable, edits made there may be committed automatically (check Lovable docs for details).

---

## Where to look next in the code

- `BLAKE.BS/main.tsx` — app bootstrap
- `BLAKE.BS/App.tsx` — providers (QueryClientProvider, TooltipProvider), routes
- `BLAKE.BS/src/pages/Index*` — main page content and layout
- `BLAKE.BS/src/components/*` — small UI pieces and sections
- `BLAKE.BS/vite.config.ts` — dev server options and path alias `@` → `./src`

---

## License & attribution

Add a LICENSE file to the repository if you want to make the license explicit. If none exists, indicate the intended license (MIT, Apache-2.0, etc.) before publishing.

---

If you want me to also add a package.json inferred from imports so `npm run dev` works, tell me and I will add it.