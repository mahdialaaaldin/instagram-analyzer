# Followers Analyzer for Instagram

See who doesn't follow you back, who you don't follow back, your mutuals, and even **who unfollowed you**. Everything runs 100% in your browser from your official Instagram data export. No login, no password, no uploads.

**Live:** https://mahdialaaaldin.github.io/instagram-analyzer/

> Not affiliated with, endorsed by, or connected to Instagram or Meta.

## Why it's different

- **No Instagram login.** It reads the data export Meta gives you, so your account is never at risk.
- **Nothing leaves your device.** The page is locked by a Content-Security-Policy (`connect-src 'none'`), so the browser itself blocks any attempt to send data anywhere.
- **Built for phones first.** Swipe through accounts, share your stats to Stories, and install it like an app.

## Features

### Review mode
Go through the accounts that don't follow you back one card at a time:
- Swipe **left** to mark as unfollowed, **right** to keep, or use the buttons
- "Open on Instagram" jumps straight to the profile (opens the app on mobile)
- Undo, progress bar, and a small celebration when you're done
- Desktop shortcuts: `←` done · `→` keep · `↓` skip · `Enter` open · `Z` undo

### Unfollower tracking
Instagram exports don't say who unfollowed you. This tool can save a snapshot of your followers on your device. Upload a fresh export later and you get exact **New followers** and **Lost followers** lists.

### Lists
- Don't follow you back · You don't follow back · Mutuals
- Followers · Following
- New followers · Lost followers (with snapshots)
- Requests you sent · Requests you received · Recent follow requests
- Recently unfollowed by you · Close friends · Blocked · Restricted · Custom lists

Every list has search, sorting, Kept/Done filters, multi-select (long-press on mobile), and infinite scroll.

### Export & share
- Copy @handles, usernames, or profile links
- Download CSV (Excel-ready), Excel (.xls), or JSON
- Share files through your phone's share sheet
- Generate a Story-sized (1080×1920) stats card

### Insights
Network breakdown chart, monthly follower/following activity, follow-back rate, follower ratio, oldest and newest followers, best month, longest one-sided follow, and more.

### Also
- **Try a demo** with fake data before requesting your own export
- Works with split exports (several ZIPs) or already-unzipped JSON files
- Light, dark, and system themes
- Remembers your progress if your phone reloads the tab
- Installable as an app and works offline (PWA)

## How to get your Instagram export

1. Open [Download your information](https://accountscenter.instagram.com/info_and_permissions/dyi/) (Instagram → Settings → Accounts Center → Your information and permissions → Download your information).
2. Choose **Some of your information** → tick only **Followers and following**.
3. Choose **Download to device**, date range **All time**, format **JSON** (HTML won't work).
4. Wait for Meta's email (usually minutes, sometimes up to 48 hours).
5. Download the ZIP and drop it into the app. No need to unzip it.

## FAQ

**Does "Recently unfollowed" show people who unfollowed me?**
No. That Instagram file lists accounts *you* unfollowed. Use snapshots to see who unfollowed you.

**Where is my data stored?**
Your export is only read in memory. If "Remember on this device" is on, a list of follower usernames and your review marks are saved in your browser's local storage. You can erase them anytime in Settings.

**Why don't the numbers exactly match the app?**
The export is a snapshot from when Meta created it, and deactivated accounts can still appear in it.

## Project structure

```
index.html            The whole app (HTML, CSS, JS)
manifest.webmanifest  App install info
sw.js                 Offline support
images/               Logo, icons, and guide screenshots
```

## Running locally

No build step or dependencies.

```bash
git clone https://github.com/mahdialaaaldin/instagram-analyzer.git
cd instagram-analyzer
```

Open `index.html` in your browser. Offline mode and app install need HTTPS or `localhost`, so for those run a local server:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deployment (GitHub Pages)

1. Go to **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to `Deploy from a branch`.
3. Select the `master` branch and the `/ (root)` folder, then save.
4. The site is published at `https://mahdialaaaldin.github.io/instagram-analyzer/`.

## Tech stack

- Vanilla HTML, CSS, and JavaScript (no frameworks, no build)
- [JSZip](https://stuk.github.io/jszip/) for reading the export ZIP in the browser

## Contributing

Issues and pull requests are welcome. If Instagram changes its export format and something breaks, please open an issue with the file name and a few anonymized entries.

## License

[MIT](LICENSE)