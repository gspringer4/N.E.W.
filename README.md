# N.E.W. Tracker

A personal tracker across five life areas — Physical, Food/Nutrition, Adventure, Mental, Growth — plus a weekly planner with follow-through tracking.

This is a **standalone** version: a single HTML file with no build step, no server, and no account required. It runs entirely in your browser and saves data using `localStorage`, so everything stays on the device/browser you're using it in.

https://gspringer4.github.io/N.E.W./

## What's in each area

- **Physical** — Strength, Cardio, Recovery
- **Food/Nutrition** — Meals, Fuel, Supplements
- **Adventure** — Big Trips, Weekend, Side Quests
- **Mental** — Read/Listen, Write, Meditate
- **Growth** — Learning, Skills, Creating

You're not locked into these. Open the **Data** tab → **Manage categories & tags** to add or remove tags and groups yourself, right from the app — no code changes needed.

## Running it

**Option A — GitHub Pages (recommended for phone use)**
1. Push this repo to GitHub (see below).
2. In the repo settings, go to **Settings → Pages**, set the source to the `main` branch, root folder.
3. GitHub will give you a URL like `https://<your-username>.github.io/<repo-name>/`.
4. Open that URL on your phone, then use your browser's **"Add to Home Screen"** option (Safari: Share icon → Add to Home Screen; Chrome: ⋮ menu → Add to Home screen) to get an app-like icon.

**Option B — Open locally**
Just double-click `index.html`, or open it directly in any browser. No install needed.

## Data & backups

- All data — log entries, your recurring weekly template, each week's plan, and your custom categories/tags — is stored in your browser's `localStorage`, scoped to whatever URL you're opening this from.
- That means: **the same browser + same URL** will always see the same data. A different browser, a different phone, or incognito/private mode will start empty.
- Use the **Data** tab to:
  - Add/remove tags and groups under **Manage categories & tags**
  - Export your entries as a `.csv` (for spreadsheets)
  - Export a full `.json` backup (entries + template + plans + your custom categories) — keep this somewhere safe (e.g. committed to this repo, or a cloud drive)
  - Import a `.json` backup to restore or move data to a new browser/device

## Pushing this repo to GitHub

From this folder:

```bash
git init
git add .
git commit -m "Initial commit — N.E.W. Tracker"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

(Create the empty repo on GitHub first, then use the URL it gives you in place of the one above.)

## Updating later

When you want new UX changes down the road, replace `index.html` with the updated version and commit again:

```bash
git add index.html
git commit -m "Update tracker: <what changed>"
git push
```

Day-to-day category and tag changes don't need this at all — those live in the **Data → Manage categories & tags** screen inside the app itself. Your logged data isn't affected by updating the file either way — it lives separately in the browser's storage, not in the code.
