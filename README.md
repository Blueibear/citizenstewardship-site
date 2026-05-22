# Citizen Stewardship

Citizen Stewardship is a static Astro website for publishing nonpartisan, citizen-created public proposals about democratic renewal and practical civic reform.

The site is intentionally static:

- no custom backend
- no analytics
- no secrets
- no client-side tracking

Public discussion is intended to run through GitHub Discussions. The contact page includes a static HTML form shell, but it cannot receive messages until a real third-party or Cloudflare endpoint is configured.

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

## GitHub Discussions Setup

Use GitHub Discussions as the public forum for proposal review and citizen submissions:

1. Make the repository public.
2. Enable Discussions in the repository settings.
3. Create these Discussion categories:
   - Proposal One Discussion
   - Proposal Two Discussion
   - Public Submissions
   - Approved Submissions
   - Site Improvements
   - General Civic Discussion
4. Replace the placeholder links in `src/pages/community.astro` and `src/pages/submit.astro` with category-specific links if desired.
5. Use Discussions as the public forum for comments, challenges, proposed edits, and public submissions.

The current placeholder Discussions URL is:

```text
https://github.com/Blueibear/citizenstewardship-site/discussions
```

## Submission Moderation Workflow

- New suggestions go into Public Submissions.
- Review submissions for relevance, seriousness, nonpartisanship, rights compatibility, and basic factual grounding.
- Serious, relevant, nonpartisan, rights-compatible suggestions can be moved or copied to Approved Submissions.
- Approved does not mean final adoption or full endorsement.
- Approved submissions can later be manually listed in the Approved Public Submissions area on the Community page.

## Contact Form Setup

The Contact page includes a real HTML form structure, but the form action is a placeholder:

```html
https://formspree.io/f/REPLACE_WITH_FORM_ID
```

Before treating the form as live:

1. Create a Formspree, Tally, Basin, Formspark, or Cloudflare Pages Function endpoint.
2. Replace the placeholder form action URL in `src/pages/contact.astro`.
3. Test the form submission end to end.
4. Until then, use `contact@citizenstewardship.org`.

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
