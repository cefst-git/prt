# prt-calc[README.md](https://github.com/user-attachments/files/26193914/README.md)
# Asset Participations

A single-file, zero-dependency web app for managing fractional ownership of co-owned assets across multiple scenarios.

![Dark Theme](screenshots/dark.png)

## Features

- **10 Assets × 3 Owners** — Configure fractional ownership for up to 10 assets shared between owners A, B, and C
- **Custom Parts** — Set any denominator per asset (3 for thirds, 12 for twelfths, 100 for percentages, etc.)
- **Custom Values** — Set asset values with +/−$100K steppers or type directly
- **Drag & Drop** — Transfer shares by dragging bar segments, owner chips, or dropping onto owner cards
- **5 Scenario Tabs** — Model different allocation scenarios side by side (double-click to rename)
- **Compare View** — Auto-generated comparison tab when 2+ scenarios are edited from default
- **Value-Proportional Bars** — Bar chart length scales to relative asset value
- **Delta Tracking** — Owner cards show Δ% and Δ$ from Scenario 1
- **Dark / Light Theme** — Toggle with one click
- **Save as HTML** — Export editable or read-only self-contained HTML files with all data baked in
- **Undo** — Up to 50 levels of undo
- **Fully Offline** — No server, no dependencies, runs in any modern browser
- **Mobile Responsive** — Optimised layout for phones and tablets

## Usage

### Quick Start

1. Open `index.html` in any modern browser
2. Click asset names, parts, or values to edit inline
3. Use +/− buttons or drag bar segments to transfer ownership shares
4. Switch between scenario tabs to model alternatives
5. Save as editable or read-only HTML via the save button

### Keyboard Shortcuts

- `Enter` — Confirm inline edit
- `Escape` — Cancel inline edit
- `Double-click` tab — Rename scenario

### Drag & Drop Targets

| Source | Target | Action |
|--------|--------|--------|
| Bar segment | Another owner's bar segment | Transfer 1 part |
| Owner chip (A:3) | Another owner's bar segment | Transfer 1 part |
| Bar segment | Owner pill (−[B:0]+) | Transfer 1 part (works even at 0) |
| Bar segment | Owner card (top) | Transfer 1 part to that owner |

### Saving

The save button offers two options:

- **Save as Editable HTML** — Full working app with your current data. Reopen and continue editing.
- **Save as Read-Only HTML** — Locked view for sharing. No editing controls shown.

Files are named `asset_participations_[editable|readonly]_YYYYMMDD_HHMM.html`.

## Technical Details

- **Single file**: ~35KB HTML with embedded CSS and JavaScript
- **Zero dependencies**: Only Google Fonts loaded externally (works without them)
- **State injection**: Save works by replacing marked code sections with serialised state
- **Vanilla JS**: No frameworks, no build step, no transpilation
- **CSS Custom Properties**: Theme switching via CSS variables

## Browser Support

Tested on:
- Chrome/Edge 90+
- Firefox 90+
- Safari 15+
- Mobile Safari / Chrome on iOS/Android

## File Structure

```
asset-participations/
├── index.html          # The complete app (single file)
├── README.md           # This file
├── LICENSE             # MIT License
└── screenshots/
    └── dark.png        # Screenshot placeholder
```

## License

MIT License — see [LICENSE](LICENSE) for details.
