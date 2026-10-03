# Postal Warrior Performance Dashboard – HO / SO / FPO / BPC / BNPL / RMO
Head Quarter Region, Ahmedabad (India Post)

## Files
| File | Purpose |
|---|---|
| `index.html` | The dashboard (single page, no build step) |
| `HOSO_Dashboard.xlsx` | The data. Two worksheets: **HO Details** and **SO Details** |
| `config.json` | “As on” date, time, footer notes, optional `updatedAt` text for the LIVE banner |
| `netlify.toml` | Netlify settings (no build command, publish folder = root, no-cache headers) |

## 1. Upload to GitHub (first time)
1. Sign in at github.com → **New repository** → name it (e.g. `PostalWarriorHOSO2026-27`) → **Public** → Create.
2. In the new repository click **Add file → Upload files**.
3. Drag in **all files from this folder** (index.html, HOSO_Dashboard.xlsx, config.json, netlify.toml, README.md) → **Commit changes**.

## 2. Connect to Netlify (first time)
1. app.netlify.com → **Add new site → Import an existing project → GitHub** → pick the repository.
2. Build command: *(leave empty)* · Publish directory: `.` → **Deploy**.
3. Optional: Site configuration → Change site name, to get a clean public link.

## 3. Updating the data for everyone (every time)
1. Open the repository on GitHub → **Add file → Upload files** → drop the new Excel **with the same name** `HOSO_Dashboard.xlsx` (it replaces the old one) → **Commit changes**.
2. (Optional) Open `config.json` → pencil icon → change `asOn`, `time`, `updatedAt`, `note` → Commit.
3. Netlify redeploys automatically (about 1 minute). Open pages also re-check the data every 2 minutes, so visitors see the new figures without doing anything.

Notes
* The Excel must keep the same column layout and header names as the current file.
* The “Upload” control in **Data Management** only changes the viewer’s own browser; the public sees whatever is in GitHub.
* If the data file cannot be loaded (for example when opening `index.html` directly from a folder), the dashboard falls back to the copy of the data built into `index.html`.
