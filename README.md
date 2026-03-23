# Asset Participations

A zero-dependency PWA for managing fractional ownership of co-owned assets across multiple scenarios. Runs offline, installable on mobile home screens.

## Features

- **10 Assets × 3 Owners** — fractional ownership for owners A, B, and C
- **Custom Parts** — any denominator per asset (3 for thirds, 12 for twelfths, 100 for percentages)
- **Custom Values** — asset values with +/−$100K steppers or direct input
- **Drag & Drop** — transfer shares via bar segments, owner chips, pills, or owner cards
- **5 Scenario Tabs** — model different allocations (double-click to rename)
- **Compare View** — auto-generated when 2+ scenarios are edited from default
- **Value-Proportional Bars** — bar length scales to relative asset value
- **Delta Tracking** — Δ% and Δ$ from Scenario 1 in owner cards
- **Dark / Light Theme**
- **Save as HTML** — export editable or read-only self-contained files
- **Undo** — up to 50 levels
- **PWA / Offline** — service worker caches everything, installable on home screen
- **Mobile Responsive** — optimised for phones and tablets

## Installation

### Option 1: GitHub Pages (recommended)

1. Push this repo to GitHub
2. Go to Settings → Pages → Source: main branch, root folder
3. Your app is live at `https://yourusername.github.io/asset-participations/`
4. On mobile, open the URL → Share → "Add to Home Screen"

### Option 2: Any web server

Upload all files to any static host (Netlify, Vercel, S3, etc.). The service worker requires HTTPS.

### Option 3: Local file

Open `index.html` directly in a browser. Everything works except PWA install (service workers require HTTP/HTTPS).

## File Structure

```
asset-participations/
├── index.html        # Complete app (~37KB)
├── sw.js             # Service worker for offline caching
├── manifest.json     # PWA manifest (name, icons, display mode)
├── icon-192.png      # Home screen icon (192×192)
├── icon-512.png      # Splash screen icon (512×512)
├── README.md         # This file
├── LICENSE           # MIT License
├── .gitignore        # Git ignore rules
└── screenshots/
    └── .gitkeep      # Placeholder
```

## PWA Details

The service worker (`sw.js`) caches:
- `index.html` — the complete app
- `manifest.json` — PWA metadata
- Icons — for home screen and splash
- Google Fonts — cached on first load

After the first visit, the app works fully offline. Updates are picked up on the next visit when online — bump `CACHE_NAME` in `sw.js` to force a cache refresh.

## GitHub Setup

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/YOUR_USERNAME/asset-participations.git
git push -u origin main
```

Then enable GitHub Pages in the repo settings.

## License

MIT — see [LICENSE](LICENSE) for details.
