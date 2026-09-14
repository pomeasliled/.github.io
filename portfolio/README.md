# Victor Gardin — Portfolio Site

A static site (plain HTML/CSS, no build step). Free to host on GitHub Pages.

## Files
- `index.html` — home page (about, experience, projects, skills, contact)
- `agena-space.html` — full case study for the Agena Space mission-analysis/GNC project
- `css/style.css` — shared stylesheet
- `assets/img/` — figures pulled from the Agena Space internship report
- `assets/files/victor-gardin-resume.pdf` — downloadable résumé (linked from the "Résumé" button)

## Deploy on GitHub Pages (free)

1. **Create a GitHub account** if you don't already have one: https://github.com/join

2. **Create a new repository**
   - Go to https://github.com/new
   - Name it either `victor-gardin` (or anything you like) for a project site,
     or `<your-username>.github.io` for a personal site at the shortest possible URL.
   - Set it to **Public**, and don't initialize it with a README (you already have these files).

3. **Upload the files**
   - Easiest: on the new repo's page, click "uploading an existing file" and drag in
     `index.html`, `agena-space.html`, the `css/` folder, and the `assets/` folder
     (keep the folder structure — GitHub's uploader preserves it if you drag folders directly
     in a Chromium-based browser; otherwise use the `git` steps below).
   - Or via `git`, from inside this unzipped folder:
     ```
     git init
     git add .
     git commit -m "Initial portfolio"
     git branch -M main
     git remote add origin https://github.com/<your-username>/<repo-name>.git
     git push -u origin main
     ```

4. **Turn on GitHub Pages**
   - In the repo, go to **Settings → Pages**.
   - Under "Build and deployment", set **Source** to "Deploy from a branch".
   - Set **Branch** to `main` and folder to `/ (root)`, then **Save**.
   - GitHub will give you a URL after a minute or two:
     - `https://<your-username>.github.io/<repo-name>/` (project site), or
     - `https://<your-username>.github.io/` (if you named the repo `<your-username>.github.io`)

5. **Put the link on your résumé/LinkedIn** once it's live.

## Updating later
- To update your résumé PDF: replace `assets/files/victor-gardin-resume.pdf` with the new
  file (keep the same filename so the "Résumé" button keeps working), commit, and push.
- To add a new project deep-dive page, copy `agena-space.html` as a template and link to it
  from the project card in `index.html`.

## Note on the phone number
The public site intentionally omits your phone number (email + LinkedIn only) to avoid
exposing it to scrapers on an open, indexable page. If you'd rather have it visible, add a
line under the `#contact` section in `index.html`.
