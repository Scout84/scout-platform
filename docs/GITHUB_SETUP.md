# Moving SCOUT to GitHub — Step-by-Step

## 1. Create your GitHub account

Go to GitHub and create/sign in to your account.

## 2. Create a repository

Create a new repository.

Suggested name:

```text
scout-platform
```

For early prototype testing you can make it **Public** if you want to use GitHub Pages on the free plan.

Important: do not upload real candidate compliance documents or personal information.

## 3. Upload the SCOUT files

Extract `SCOUT_GITHUB_READY.zip`.

Inside the extracted folder you will see:

```text
index.html
business/
worker/
admin/
docs/
.github/
.nojekyll
README.md
```

In GitHub:

1. Open your new repository.
2. Choose **Add file → Upload files**.
3. Drag all the files and folders from the extracted SCOUT folder into the upload area.
4. Enter a commit message such as:

```text
Initial SCOUT prototype
```

5. Commit the files to the `main` branch.

If your browser upload does not preserve hidden folders such as `.github`, use GitHub Desktop instead.

## 4. Turn on GitHub Pages

After the upload:

1. Open **Settings** in the repository.
2. Select **Pages**.
3. Under **Build and deployment**, set **Source** to **GitHub Actions**.
4. Open the **Actions** tab.
5. The `Deploy SCOUT to GitHub Pages` workflow should run.
6. When complete, GitHub will provide your Pages URL.

It will normally look similar to:

```text
https://YOUR-USERNAME.github.io/scout-platform/
```

Your three prototype routes will then be:

```text
https://YOUR-USERNAME.github.io/scout-platform/business/
https://YOUR-USERNAME.github.io/scout-platform/worker/
https://YOUR-USERNAME.github.io/scout-platform/admin/
```

## 5. How to update SCOUT after this

When a new version is created:

1. Download the revised files.
2. Replace the relevant folder in your local copy:
   - Business change → `business/index.html`
   - Worker change → `worker/index.html`
   - Admin/website change → `admin/index.html`
3. Upload/commit the changed file to GitHub.
4. GitHub Actions automatically republishes the Pages website.

You do not need to recreate the repository each time.

## Recommended workflow with GitHub Desktop

GitHub Desktop is easier than repeatedly uploading through the browser.

1. Install GitHub Desktop.
2. Clone your `scout-platform` repository.
3. You will get a normal SCOUT folder on your computer.
4. Replace files in that folder when you receive updates.
5. GitHub Desktop will show exactly what changed.
6. Enter a short summary such as:

```text
Update Business dispatch workflow
```

7. Choose **Commit to main**.
8. Choose **Push origin**.
9. GitHub Pages republishes the site automatically.

## What GitHub can do now

GitHub Pages is suitable for:

- UX testing
- business app navigation
- worker app navigation
- admin portal prototype
- award/pay engine demonstrations
- dispatch workflow demonstrations
- WHS workflow demonstrations
- candidate compliance dashboard demonstrations
- stakeholder demos

## What should NOT go into GitHub Pages yet

Do not use the static GitHub prototype for real:

- candidate identity documents
- criminal history documents
- bank details
- TFNs
- superannuation information
- real payment card data
- passwords
- private business information
- production compliance records

Those require secure authentication and backend storage later.

## Future architecture

A sensible progression is:

```text
GitHub
   ↓
GitHub Pages / front-end testing
   ↓
Backend API
   ↓
Authentication
   ↓
Database
   ↓
Private document storage
   ↓
Payments / notifications / payroll
```

GitHub remains useful even after the backend is introduced because it becomes the source repository for SCOUT.
