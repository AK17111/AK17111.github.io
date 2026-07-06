# Publishing this site to AK17111.github.io

## 1. Create the repo (one-time)
1. Go to https://github.com/new
2. Repository name must be exactly: `AK17111.github.io`
3. Public, no README/template — leave it empty.
4. Click **Create repository**.

## 2. Upload the files
Simplest way (no git needed):
1. Open your new repo on github.com.
2. Click **Add file → Upload files**.
3. Drag in `index.html` and `resume.pdf` from this folder.
4. Commit directly to `main`.

Or with git from a terminal:
```bash
cd path/to/this/folder
git init
git remote add origin https://github.com/AK17111/AK17111.github.io.git
git add index.html resume.pdf
git commit -m "Initial portfolio site"
git branch -M main
git push -u origin main
```

## 3. Turn on Pages
1. In the repo, go to **Settings → Pages**.
2. Under "Build and deployment", Source = **Deploy from a branch**.
3. Branch = `main`, folder = `/ (root)`. Save.
4. Wait ~1 minute, then visit **https://AK17111.github.io**.

## 4. Adding your real projects
Open `index.html` and find the `<section id="projects">` block. Each project is a
`<div class="card">`. To add one:

1. Duplicate one of the existing project `<div class="card">...</div>` blocks.
2. Edit the title, dates, place/tech line, and bullet points.
3. Update the `<div class="tags">` chips to match the tech used.
4. Change the `Repo →` link's `href="#"` to your real GitHub repo URL, e.g.
   `href="https://github.com/AK17111/your-repo-name"`.
5. Delete the "More projects coming soon" placeholder card once you have enough real ones,
   or just leave it at the end — it'll always show as a dashed placeholder.
6. Save, then re-upload/push `index.html` — the live site updates within a minute or two.

If a project has a live demo (not just code), add a second link next to "Repo →" like:
```html
<div class="project-links">
  <a href="https://github.com/AK17111/your-repo-name" target="_blank">Repo →</a>
  <a href="https://your-demo-url.com" target="_blank">Live demo →</a>
</div>
```

## 5. Keeping your resume link current
The "Resume (PDF)" button in the hero links to `resume.pdf` in this same folder.
Whenever you update your resume, just re-upload a file named `resume.pdf` to overwrite it.
