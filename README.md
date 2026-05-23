# Citizen Stewardship

Citizen Stewardship is a nonpartisan, citizen-created public project for American democratic renewal, practical reform, and civic responsibility.

The repo remains an Astro static site deployed through Cloudflare Pages at `https://citizenstewardship.org`. It does not include:

- custom backend functions
- analytics
- secrets
- database code
- client-side tracking

Public discussion runs through GitHub Discussions. The public contact email is `contact@citizenstewardship.org`, and the contact page uses the Formspree endpoint currently configured in `src/pages/contact.astro`.

Official social links:

- Substack: <https://citizenstewardship.substack.com/>
- Facebook: <https://facebook.com/CitizenStewardship>
- Bluesky: <https://bsky.app/profile/citizenstewardship.org>
- X: <https://x.com/CitizenStewards>

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
- `/terms/`
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

Site links to these GitHub Discussions categories should use `target="_blank"` and `rel="noopener noreferrer"` so they open in a new browser tab safely.

## Submission Moderation Workflow

- New suggestions go into Public Submissions.
- Review submissions for relevance, seriousness, nonpartisanship, rights compatibility, and basic factual grounding.
- Serious, relevant, nonpartisan, rights-compatible suggestions can be moved or copied to Approved Submissions.
- Approval does not mean final adoption or full endorsement.
- Approved submissions can later be manually listed in the Approved Public Submissions area on the Community page.
- Public discussion should remain constructive, nonpartisan, and grounded in improving the proposals.
- The Submit page uses the full Citizen Stewardship Core Pillars list, not a shortened Core Principles list.

## Terms of Use

The `/terms/` page covers plain-English site rules, community conduct, public
submissions, third-party services, downloadable proposal drafts, and submission
permission. It should stay consistent with the static-site workflow, GitHub
Discussions, Formspree contact handling, Cloudflare Pages hosting, and the
Privacy Policy.

## Sharing

Share buttons are implemented locally in `src/components/ShareButtons.astro`. They use the native Web Share API when available, provide a local copy-link fallback, and include direct Facebook, X, and Bluesky share/compose links. No third-party share widgets, analytics, or tracking scripts are used.

## Site Images and Metadata

The shared Citizen Stewardship graphic is stored at:

- `public/assets/images/citizen-stewardship-social.png`

The site uses that image in the header, homepage, and Open Graph/social sharing metadata. The public social image URL is:

- `https://citizenstewardship.org/assets/images/citizen-stewardship-social.png`

The browser tab icon remains a simplified `public/favicon.svg` mark because the full social graphic is too detailed to read well at tiny favicon sizes. A simplified PNG favicon can be added later if a raster icon is needed.

## Contact Form Setup

Do not change the contact form endpoint unless contact handling is intentionally being updated. The public contact email is `contact@citizenstewardship.org`.

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
public/assets/images/ Shared public graphics
public/assets/pdfs/ Public proposal PDFs
```
