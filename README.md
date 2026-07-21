# Shore to Summit — Life Tracker

A personal tracker for the five areas from the Shore to Summit operating manual — Physical, Nutrition, Adventure, Mental, Growth — plus a weekly planner with follow-through tracking.

This is a **standalone** version: a single HTML file with no build step, no server, and no account required. It runs entirely in your browser and saves data using `localStorage`, so everything stays on the device/browser you're using it in.

## Running it

**Option A — GitHub Pages (recommended for phone use)**
1. Push this repo to GitHub (see below).
2. In the repo settings, go to **Settings → Pages**, set the source to the `main` branch, root folder.
3. GitHub will give you a URL like `https://<your-username>.github.io/<repo-name>/`.
4. Open that URL on your phone, then use your browser's **"Add to Home Screen"** option (Safari: Share icon → Add to Home Screen; Chrome: ⋮ menu → Add to Home screen) to get an app-like icon.

**Option B — Open locally**
Just double-click `index.html`, or open it directly in any browser. No install needed.

## Data & backups

- All data (log entries, your recurring weekly template, and each week's plan) is stored in your browser's `localStorage`, scoped to whatever URL you're opening this from.
- That means: **the same browser + same URL** will always see the same data. A different browser, a different phone, or incognito/private mode will start empty.
- Use the **Data** tab in the app to:
  - Export your entries as a `.csv` (for spreadsheets)
  - Export a full `.json` backup (entries + template + plans) — keep this somewhere safe (e.g. committed to this repo, or a cloud drive)
  - Import a `.json` backup to restore or move data to a new browser/device

## Pushing this repo to GitHub

From this folder:

```bash
git init
git add .
git commit -m "Initial commit — Shore to Summit life tracker"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

(Create the empty repo on GitHub first, then use the URL it gives you in place of the one above.)

## Updating later

When you want new categories, tags, or UX changes, just replace `index.html` with the updated version and commit again:

```bash
git add index.html
git commit -m "Update tracker: <what changed>"
git push
```

Your data won't be affected by updating the file — it lives separately in the browser's storage, not in the code.
