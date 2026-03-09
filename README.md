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
- Persists last quest and accent in `localStorage`
- Includes a “copy quest” button for quick sharing
