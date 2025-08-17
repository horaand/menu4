
# Dark Classic Dock Menu (HTML + CSS)

Bottom **dock** navigation with a “More” submenu — pure CSS, responsive, and accessible-friendly.

## Structure
```text
dark-dock-menu/
├─ index.html
└─ styles.css
```

## Quick Start
1) Save the HTML to `index.html` and the CSS to `styles.css`.  
2) In `<head>` of `index.html` include:
```html
<link rel="stylesheet" href="styles.css" />
```
3) Open `index.html` in your browser.

## Features
- **Dock nav (fixed bottom):** glass panel with blur & soft border.
- **Active link:** `.dock-link.active` + subtle background.
- **Pure CSS submenu:** checkbox (`#more-toggle`) reveals `.submenu`.
- **Tokens:** theme via CSS variables in `:root`.
- **Responsive:** dock scrolls on small screens; content grid collapses.

## Customize (tokens)
- Colors: `--bg`, `--panel`, `--text`, `--muted`
- Accents: `--accent`, `--accent-2`
- Focus ring: `--ring`
- Glass level: `--glass` (used on dock background)

## Accessibility
- Submenu uses real `<input type="checkbox">` + `<label for="more-toggle">`.
- Focus states via `:focus-visible` on buttons/links.
- `role="menu"`/`menuitem` present on submenu list items.

## Notes
- Keep exactly **one** HTML document per page; CSS lives in `styles.css`.
- `backdrop-filter` (blur) requires browser support; provide a solid color fallback if needed.

## Troubleshooting
- **Submenu doesn’t open?** Confirm `id="more-toggle"` matches the label’s `for`, and DOM order: `input.more-toggle` → `label.more-label` → `.submenu`.
- **Overflow on mobile?** The dock enables horizontal scroll; reduce link text or widen paddings if needed.
