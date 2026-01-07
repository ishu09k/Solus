# Deploying this site (quick guide)

Option A — GitHub Pages (recommended)

1. Create a new repository on GitHub (or use an existing one).
2. From this project folder, initialize git (if not already):

```bash
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/USERNAME/REPO.git
git push -u origin main
```

3. The workflow `.github/workflows/deploy-pages.yml` will run on push and publish the repository root to GitHub Pages.
4. After the action completes, your site will be available at:

```
https://USERNAME.github.io/REPO/
```

Replace `USERNAME` and `REPO` with your GitHub username and repository name.

Option B — Netlify (drag & drop)

1. Zip the site files (or use the project folder).
2. Visit https://app.netlify.com/drop and drop the folder to publish instantly.

Option C — Vercel

1. Create an account at https://vercel.com/ and import the GitHub repo.
2. Vercel will auto-deploy on push and provide a live URL.

Notes
- The workflow deploys the repository root. If you prefer to publish a subfolder (e.g., `dist/`), update `publish_dir` in the workflow.
- GitHub Pages may take a minute to show the site after deploy.
