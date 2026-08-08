# Instagram Followers Analyzer

A 100% client-side tool that analyzes your Instagram data export and shows who doesn't follow you back, who you don't follow back, recently unfollowed accounts, pending requests, blocked/restricted profiles, and more.

**Live demo:** https://mahdialaaaldin.github.io/instagram-analyzer/

Everything runs locally in your browser. No backend, no servers, no data collection — your ZIP file and its contents never leave your device.

## Features

- **Drag-and-drop upload** of your Instagram data export ZIP
- **Dashboard** with followers, following, non-mutual, unfollowed, pending, blocked, and restricted counts
- **Interactive data visualizations** — donut chart and bar chart breakdowns of your follow stats
- **Shareable stats card** — generate and download a summary image to share your results
- **Searchable, sortable, paginated tables** for every list
- **Bulk actions** — select profiles and open them in bulk, copy usernames/URLs, or export to CSV, JSON, or Excel
- **Responsive grid layout** — works great on desktop, tablet, and mobile
- **Light and dark theme**
- **Built-in step-by-step guide** (with screenshots) on how to request and download your Instagram data export
- **PWA-ready** with an app icon for adding to your home screen

## Getting Started

1. Open the [live demo](https://mahdialaaaldin.github.io/instagram-analyzer/) or open `index.html` locally in your browser.
2. Follow the in-app guide to request your data export from Instagram (Settings → Accounts Center → Your information and permissions → Download your information), choosing **JSON** format and the **"Followers and following"** category.
3. Once Instagram emails you the export, download the ZIP file.
4. Drop the ZIP into the upload box.
5. Explore your dashboard and charts.

## Running Locally

No build step or dependencies required.

```bash
git clone https://github.com/mahdialaaaldin/instagram-analyzer.git
cd instagram-analyzer
```

Then just open `index.html` in your browser.

## Deployment (GitHub Pages)

This project is a single static HTML file, so it deploys directly with GitHub Pages:

1. Push the repository to GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to `Deploy from a branch`.
4. Select the `main` branch and `/ (root)` folder, then save.
5. Your site will be published at `https://mahdialaaaldin.github.io/instagram-analyzer/`.

## Privacy

All parsing and analysis happens in the browser using JavaScript. No file is ever uploaded to a server. This is a static site with no backend.

## Tech Stack

- Vanilla HTML, CSS, and JavaScript
- [JSZip](https://stuk.github.io/jszip/) for reading the Instagram export ZIP client-side

## License

MIT
