# Web-Slinger Training Log

A 12-week full-body training tracker. Single static HTML page, no backend, no build step. Progress saves in your browser via `localStorage` — per-device, private, no account needed.

## What's in it

- Week-by-week (1–12) exercise checklist, split into 3 phases (Foundation → Accumulation → Intensification)
- Automatic deload flag on week 10
- Diet/cardio targets per phase
- Progress bar + persistent checkboxes (saved locally in your browser)

## Deploy to GitHub Pages (free, ~2 minutes)

1. **Create a new repo on GitHub** (github.com → New repository). Name it whatever you want, e.g. `training-tracker`. Public repo (required for free GitHub Pages on a personal account).

2. **Push this project to it:**
   ```bash
   cd spidey-tracker
   git add -A
   git commit -m "Initial commit: training tracker"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
   git push -u origin main
   ```

3. **Enable Pages:**
   - Go to your repo → **Settings** → **Pages**
   - Under "Build and deployment", Source: **GitHub Actions** (the included workflow will handle it — see `.github/workflows/deploy.yml`)
   - Push to `main` and it deploys automatically. First deploy takes ~1 min.

4. **Your live URL** will be:
   ```
   https://YOUR_USERNAME.github.io/YOUR_REPO/
   ```
   Shown in the Pages settings tab once the first deploy finishes.

## Local preview (before deploying)

Just open `index.html` directly in a browser — no server needed, it's a single self-contained file.

## Notes

- Data is stored per-browser via `localStorage`. Clearing browser data wipes your checkmarks. It does not sync across devices — this is a static site with no backend, by design (keeps it free and dependency-free).
- To reset a week's checkboxes, use the "clear" button in the app itself.
- Edit `index.html` directly to change exercises, targets, or phase lengths — it's one file, all inline CSS/JS, no build tooling required.
