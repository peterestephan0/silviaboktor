# Silvia Boktor Artworks — Website

A single-page site for Silvia Boktor: hero, four work categories (Spiritual /
Emotional / Nature / Cities, Atmosphere & Architecture), a Limited Prints
teaser, process, about, and contact.

## Deploy to GitHub Pages

**Option A — New repository (easiest)**
1. Go to https://github.com/new and create a new repository (e.g. `silvia-boktor-artworks`). Public repos get free Pages hosting.
2. On your computer, unzip this folder, then from inside it run:
   ```
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
   git push -u origin main
   ```
3. In the repo on GitHub: **Settings → Pages**.
4. Under "Build and deployment," set **Source** to `Deploy from a branch`, **Branch** to `main` and folder to `/ (root)`, then **Save**.
5. GitHub will give you a live URL, typically `https://YOUR-USERNAME.github.io/YOUR-REPO/` — it can take a minute or two to go live after the first push.

**Option B — Upload via the GitHub website (no command line)**
1. Create a new repository at https://github.com/new
2. Click "uploading an existing file" on the empty repo page.
3. Drag in `index.html`, `.nojekyll`, `README.md`, and the whole `images` folder (drag the folder itself — GitHub keeps the folder structure).
4. Commit the changes.
5. Go to **Settings → Pages**, set Source to the `main` branch, root folder, and save.

**Option C — User/organization homepage**
If you name the repo exactly `YOUR-USERNAME.github.io`, GitHub Pages serves it at `https://YOUR-USERNAME.github.io/` (no sub-path) automatically once Pages is enabled, with no extra branch config needed beyond the same Settings → Pages step above.

### Using a custom domain (optional)
In **Settings → Pages → Custom domain**, enter your domain (e.g. `silviaboktor.com`) and follow GitHub's DNS instructions (a `CNAME` file is added to the repo automatically). Enable "Enforce HTTPS" once the certificate is issued.

## Files

- `index.html` — the entire site (HTML, CSS, and JS in one file)
- `images/` — all artwork photos, the studio/process photo, and the artist portrait, referenced with relative paths (`images/em1.jpg`, etc.) so they work as-is on GitHub Pages
- `.nojekyll` — tells GitHub Pages to skip Jekyll processing, so files/folders starting with `_` or similar aren't ignored (harmless to keep even though this site doesn't use any)

## Editing content later

Open `index.html` in any text editor:
- Painting titles/sizes/medium/status/image: search for `const works = [`
- Print teaser items: search for `const prints = [`
- Bio text: search for `id="about"`
- Email / Instagram links: search for `mailto:` and `instagram.com`
- Slogan: search for `hero-quote`

After editing, commit and push the change (`git add . && git commit -m "update" && git push`) — GitHub Pages redeploys automatically within a minute or two.
