# Citizen Stewardship

Citizen Stewardship is a static Astro website for publishing nonpartisan, citizen-created public proposals about democratic renewal and practical civic reform.

The site is intentionally static:

- no backend
- no analytics
- no online forms
- no secrets
- no client-side tracking

## Pages

The current site routes are:

- `/`
- `/proposal-one/`
- `/proposal-two/`
- `/community/`
- `/submit/`
- `/about/`
- `/contact/`
- `/privacy/`
- `/404.html`

## Proposal PDFs

The public PDFs are stored under `public/assets/pdfs/` and are referenced by these exact public paths:

- `/assets/pdfs/democratic-renewal-full-proposal.pdf`
- `/assets/pdfs/feasible-democratic-reform-proposal.pdf`

Do not move these files unless the page links are updated intentionally.

## Local Development

Install dependencies:

```bash
npm install
```

Start the local Astro dev server:

```bash
npm run dev
```

Build the static site:

```bash
npm run build
```

The production output is written to `dist/`.

## Project Structure

```text
src/components/     Shared Astro components
src/layouts/        Site layout wrapper
src/pages/          Static routes
src/styles/         Global CSS
public/assets/pdfs/ Public proposal PDFs
```
