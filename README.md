# Citizen Stewardship

Citizen Stewardship is a static public review website where one citizen is publishing two democratic reform draft proposals for public reading, criticism, and improvement.

## Folder structure

```
/
  index.html
  proposal-one.html
  proposal-two.html
  community.html
  submit.html
  about.html
  contact.html
  privacy.html
  404.html
  README.md
  assets/
    css/styles.css
    js/main.js
    pdfs/
      democratic-renewal-full-proposal.pdf
      feasible-democratic-reform-proposal.pdf
```

## Required PDFs and exact filenames

Place these files in `assets/pdfs/`:

1. `assets/pdfs/democratic-renewal-full-proposal.pdf`
2. `assets/pdfs/feasible-democratic-reform-proposal.pdf`

If these files are missing, the embedded viewers and download links will not work.

## Preview locally

Open `index.html` directly in your browser, or run a simple local server:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Deploy with Cloudflare Pages (GitHub)

1. Cloudflare Dashboard
2. Workers & Pages
3. Create
4. Pages
5. Connect GitHub
6. Select repo `citizen-stewardship-site`
7. Framework preset: **None**
8. Build command: **leave blank**
9. Build output directory: `/` or blank/root
10. Deploy

## Add custom domain

1. Open the Pages project
2. Custom domains
3. Set up a domain
4. Add `citizenstewardship.org`
5. Add `www.citizenstewardship.org` if desired

## Configure Giscus

1. Make the repo public.
2. Enable GitHub Discussions.
3. Create categories:
   - Proposal One Discussion
   - Proposal Two Discussion
   - Public Proposals
   - Site Improvements
4. Go to https://giscus.app.
5. Generate the Giscus script.
6. Replace the placeholder Giscus blocks in:
   - `proposal-one.html`
   - `proposal-two.html`
   - `community.html`

## Update the site

1. Edit HTML/CSS/JS files.
2. Commit changes.
3. Push to GitHub.
4. Cloudflare Pages redeploys from the connected branch.

## Troubleshooting

- **PDF not showing**: Confirm file names and paths exactly match `assets/pdfs/*.pdf`.
- **Download links broken**: Verify links use root-relative paths beginning with `/assets/pdfs/`.
- **Comments not showing**: Confirm GitHub Discussions is enabled and Giscus script is installed correctly.
- **Custom domain not active**: Verify DNS records and domain assignment in Cloudflare Pages.
- **Cloudflare human verification**: Must be completed manually in Cloudflare by the human user.

## Security note

Do not commit secrets, passwords, API keys, Microsoft credentials, Apple credentials, Cloudflare cookies, or Cloudflare tokens.
