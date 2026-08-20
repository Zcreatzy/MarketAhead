<p align="center">
  <a href="./README.md"><img src="https://img.shields.io/badge/简体中文-Switch-334155?style=for-the-badge" alt="简体中文"></a>
  <a href="./README_EN.md"><img src="https://img.shields.io/badge/English-Current-2563eb?style=for-the-badge" alt="English"></a>
</p>

# MarketAhead

MarketAhead is a static daily market brief for A/H markets and US premarket sessions. It turns each trading day's notes into a browsable HTML dashboard with a calendar archive backed by JSON data.

Live site: [https://market-ahead-open.vercel.app/](https://market-ahead-open.vercel.app/)

## Overview

- A/H morning brief and US premarket brief in one static page
- Calendar archive for previous market notes
- Date-based JSON records under `history/data/`
- `history/manifest.json` metadata for archive navigation
- No backend required; it can run on GitHub Pages or any static host

## Repository Structure

- `index.html`: main dashboard and latest brief
- `history/index.html`: archive date view
- `history/manifest.json`: list of available brief dates
- `history/data/YYYY-MM-DD.json`: archived daily brief content

## View Locally

Open `index.html` directly in a browser, or serve the folder with any static file server.

```sh
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Update Flow

1. Update `index.html` with the latest market brief.
2. Add or refresh the matching `history/data/YYYY-MM-DD.json` record.
3. Update `history/manifest.json` so the archive calendar includes the new date.
4. Commit and publish the static files.

## Disclaimer

This project is for market research and information organization only. It is not investment advice.
