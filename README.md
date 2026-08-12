# Ebraheem Alnaqer — Portfolio

Static site, no build step. Plain HTML/CSS/JS, so it deploys to GitHub Pages as-is.

## Publish to GitHub Pages

Set up for a **project page** — your site will live at:
`https://<your-username>.github.io/portfolio/`
(swap in your actual GitHub username; the repo name becomes the URL path, so name it whatever you like — `portfolio` is a good default).

**Option A — via github.com (no command line):**
1. Create a new repository on GitHub named `portfolio` (public).
2. On the repo page, click **Add file → Upload files**, then drag in *everything inside this folder* (including `.nojekyll` — enable "show hidden files" in your file browser if you don't see it).
3. Commit the upload.
4. Go to **Settings → Pages**.
5. Under **Build and deployment → Source**, choose **Deploy from a branch**.
6. Branch: `main`, folder: `/ (root)`. Click **Save**.
7. Wait 1–2 minutes, then your site is live at:
   `https://<your-username>.github.io/<repo-name>/`

**Option B — via git command line:**
```bash
cd ebraheem-portfolio
git init
git add .
git commit -m "Initial portfolio"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```
Then repeat steps 4–6 above in the repo's Settings → Pages.

## Notes specific to GitHub Pages

- **`.nojekyll`** is included — this stops GitHub's default Jekyll processing from ignoring or mangling any files. Keep it in the repo root.
- All links (`css/style.css`, `about.html`, `assets/...`) are **relative**, so the site works whether it's hosted at the root of `username.github.io` or under a project subpath like `username.github.io/portfolio/`. Don't change these to start with a leading `/`.
- If you want it at your root domain (`username.github.io`, no subpath), name the repository exactly `<your-username>.github.io`.
- To use a custom domain later, add a `CNAME` file with your domain, and configure DNS per GitHub's custom-domain docs.

## Updating content later

- Swap the résumé PDF at `assets/Ebraheem_Alnaqer_Resume.pdf` (keep the same filename, or update the links in `resume.html` and `index.html` if you rename it).
- Headshots are at `assets/headshot-portrait.jpg` (4:5, used on Home/About) and `assets/headshot-square.jpg` (1:1, spare for social profiles).
- Each project case study is its own file: `project-dataco.html`, `project-chinook.html`, `project-solar.html`.
