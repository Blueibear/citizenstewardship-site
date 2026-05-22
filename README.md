# Citizen Stewardship (Astro)

Citizen Stewardship is a citizen-created public review website for two civic reform proposals. The site is built with Astro and deployed as a static output for Cloudflare Pages.

## Project structure

```text
/
├─ public/
│  ├─ assets/
│  │  └─ pdfs/
│  │     ├─ democratic-renewal-full-proposal.pdf
│  │     └─ feasible-democratic-reform-proposal.pdf
│  ├─ favicon.svg
│  └─ fonts/
├─ src/
│  ├─ components/
│  │  ├─ BaseHead.astro
│  │  ├─ Footer.astro
│  │  └─ Header.astro
│  ├─ layouts/
│  │  └─ SiteLayout.astro
│  ├─ pages/
│  │  ├─ 404.astro
│  │  ├─ about.astro
│  │  ├─ community.astro
│  │  ├─ contact.astro
│  │  ├─ index.astro
│  │  ├─ privacy.astro
│  │  ├─ proposal-one.astro
│  │  ├─ proposal-two.astro
│  │  └─ submit.astro
│  └─ styles/
│     └─ global.css
├─ astro.config.mjs
├─ package.json
└─ README.md
```

## Proposal PDFs

Keep PDFs in `public/assets/pdfs/` with these exact filenames:

- `democratic-renewal-full-proposal.pdf`
- `feasible-democratic-reform-proposal.pdf`

These are served at:

- `/assets/pdfs/democratic-renewal-full-proposal.pdf`
- `/assets/pdfs/feasible-democratic-reform-proposal.pdf`

## Local development

```bash
npm install
npm run dev
```

Open the local URL printed by Astro (typically `http://localhost:4321`).

## Local production build

```bash
npm run build
```

## Deploy to Cloudflare Pages (GitHub integration)

1. In Cloudflare Dashboard, open **Workers & Pages**.
2. Click **Create** → **Pages**.
3. Connect GitHub and select `citizen-stewardship-site`.
4. Use these settings:
   - **Framework preset:** Astro
   - **Build command:** `npm run build`
   - **Output directory:** `dist`
   - **Node version:** 22 or newer (if prompted)
5. Deploy.

## Add custom domain

1. Open the Pages project in Cloudflare.
2. Go to **Custom domains**.
3. Add `citizenstewardship.org`.
4. Optionally add `www.citizenstewardship.org`.

## Configure Giscus (comment placeholders)

1. Make the repository public.
2. Enable GitHub Discussions.
3. Create categories:
   - Proposal One Discussion
   - Proposal Two Discussion
   - Public Proposals
   - Site Improvements
4. Go to `https://giscus.app`.
5. Generate scripts for each target page.
6. Replace the placeholder blocks in:
   - `src/pages/proposal-one.astro`
   - `src/pages/proposal-two.astro`
   - `src/pages/community.astro`

## Security note

Do not commit secrets, passwords, API keys, Microsoft credentials, Apple credentials, Cloudflare cookies, or Cloudflare tokens.
