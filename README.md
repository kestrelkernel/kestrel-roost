# kestrel-roost

Tiny static site for the Kestrel roost page.

## Local preview

Because this site uses browser APIs (`localStorage`, `clipboard`), preview it through a local server instead of opening the file directly:

```bash
cd kestrel-roost
python3 -m http.server 8080
# then open http://localhost:8080
```

## What’s inside

- `index.html` — single-file site (HTML + CSS + JS)
- `assets/` — image assets used on the page

## Daily quest behavior

- Prevents immediate duplicate quest rolls
- Persists last quest and accent in `localStorage` (with safe fallback when storage is unavailable)
- Includes a “copy quest” button for quick sharing
- Adds accessibility polish (`aria-live`, visible keyboard focus, reduced-motion handling)
- Tracks a UTC-based daily quest streak (increments once per day when you roll a quest)
