# SCOUT

SCOUT is an on-demand staffing platform currently being developed as three connected experiences:

- **SCOUT Business** — mobile-first business app
- **SCOUT Worker** — mobile-first worker app
- **SCOUT Website/Admin** — public website + operations/admin portal

## Folder structure

```text
SCOUT/
├── index.html
├── business/
│   └── index.html
├── worker/
│   └── index.html
├── admin/
│   └── index.html
├── docs/
│   └── GITHUB_SETUP.md
├── .github/
│   └── workflows/
│       └── pages.yml
└── .nojekyll
```

## Local testing

Download the repository and open `index.html`.

For the most reliable local experience, run a simple local server:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## GitHub Pages

This repository includes a GitHub Actions workflow that can publish the site to GitHub Pages.

After uploading the project:

1. Open the repository in GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment → Source**, select **GitHub Actions**.
4. Open the **Actions** tab and allow the Pages workflow to complete.
5. GitHub will show the live URL under **Settings → Pages**.

## Current routes

```text
/
 /business/
 /worker/
 /admin/
```

## Important

This is currently a front-end prototype.

Do not store real candidate identity documents, criminal history checks, bank details, tax details, or other sensitive information in this repository or on GitHub Pages.

Production storage, authentication, payments and compliance records should be moved to secure backend services before handling real user data.
