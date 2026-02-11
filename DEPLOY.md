# Deploy to alphahawk-dev6.github.io

This folder is a clone of **https://github.com/alphahawk-dev6/alphahawk-dev6.github.io**.

## Push updates (from this EIA project)

1. **From a terminal in the EIA project:**

   ```powershell
   cd c:\Users\alexa\OneDrive\EIA\_pages
   git status
   git add .
   git commit -m "Add Natural Gas dashboard, APA Stock Pitch, commodities homepage"
   git push origin main
   ```
   (Use `master` instead of `main` if that's your default branch.)

2. **Refresh dashboard data later:**  
   From EIA root run `python scripts/export_for_github_pages.py`, then copy  
   `site\data\dashboard_data.json` into `_pages\data\dashboard_data.json`,  
   then from `_pages` run `git add data/dashboard_data.json`, `git commit`, `git push`.

## What was integrated

- **index.html** — Homepage is more commodities-focused; nav includes Natural Gas and APA Stock Pitch.
- **markets.html** — Natural Gas dashboard (EIA storage, 5-yr avg, Henry Hub, Plotly charts). Reads `data/dashboard_data.json`.
- **apa-stock-pitch.html** — APA stock pitch page; add your PDF/PPT link or embed in the file.
- **data/dashboard_data.json** — Snapshot for the dashboard (regenerate with the export script).
- **Nav** — All pages (Home, About, Projects, Contact) now include Natural Gas and APA Stock Pitch links; Dashboards dropdown includes Natural Gas.
