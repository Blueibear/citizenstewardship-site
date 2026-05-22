# Citizen Stewardship

Citizen Stewardship is a static Astro website for publishing nonpartisan, citizen-created public proposals about democratic renewal and practical civic reform.

The site is intentionally static:

- no custom backend
- no analytics
- no secrets
- no client-side tracking

Public discussion runs through GitHub Discussions. The contact page includes a Formspree placeholder form shell, but it cannot receive messages until the placeholder Formspree action URL is replaced with a working form URL.

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

## GitHub Discussions

Use GitHub Discussions as the public forum for proposal review and citizen submissions.

The public categories are:

- [Proposal One Discussion](https://github.com/Blueibear/citizenstewardship-site/discussions/categories/proposal-one-discussion)
- [Proposal Two Discussion](https://github.com/Blueibear/citizenstewardship-site/discussions/categories/proposal-two-discussion)
- [Public Submissions](https://github.com/Blueibear/citizenstewardship-site/discussions/categories/public-submissions)
- [Approved Submissions](https://github.com/Blueibear/citizenstewardship-site/discussions/categories/approved-submissions)
- [Site Improvements](https://github.com/Blueibear/citizenstewardship-site/discussions/categories/site-improvements)
- [General Civic Discussion](https://github.com/Blueibear/citizenstewardship-site/discussions/categories/general-civic-discussion)

## Submission Moderation Workflow

- New suggestions go into Public Submissions.
- Review submissions for relevance, seriousness, nonpartisanship, rights compatibility, and basic factual grounding.
- Serious, relevant, nonpartisan, rights-compatible suggestions can be moved or copied to Approved Submissions.
- Approval does not mean final adoption or full endorsement.
- Approved submissions can later be manually listed in the Approved Public Submissions area on the Community page.
- Public discussion should remain constructive, nonpartisan, and grounded in improving the proposals.

## Contact Form Setup

The Contact page includes a real HTML form structure, but the form action is a placeholder:

```html
https://formspree.io/f/REPLACE_WITH_FORM_ID
```

Before treating the form as live:

1. Replace the placeholder Formspree action URL in `src/pages/contact.astro`.
2. Test the form submission end to end.
3. Until then, use `contact@citizenstewardship.org`.

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
