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

- `index.html` — home page with quest generator + status widgets
- `game.html` — playable Sky Sprint mini-game
- `gallery.html` — image showcase wall
- `changelog.html` — release history + filterable flight log
- `quest-forge.html` — customize the quest generator pool (defaults + custom + JSON import/export)
- `assets/` — image assets used on the page

## New in this iteration

- **Quest Forge page:** a dedicated builder where users can toggle default quests, add/remove custom quests, and immediately affect homepage rolls
- **Quest pool integration:** homepage generator now reads a shared forge state from `localStorage` and reports whether the pool is default or customized
- **Portable state:** JSON export/import on Quest Forge for quick backup or sharing of custom quest setups

## Daily quest behavior

- Avoids repeating any of the last 3 rolled quests (when enough unique quests are available)
- Persists last quest, recent quest history, and accent in `localStorage` (with safe fallback when storage is unavailable)
- Shows live persistence status on the page (so users can tell when browser storage is blocked)
- Includes a “copy quest” button with secure-clipboard + legacy fallback support for wider browser compatibility
- Adds accessibility polish (`aria-live`, visible keyboard focus, reduced-motion handling)
- Supports keyboard shortcuts for quest actions (`R` roll, `C` copy, `A` accent, `S` reset streak)
- Tracks a UTC-based daily quest streak (increments once per day when you roll a quest)
- Keeps streak/reset timing accurate if the tab stays open across UTC midnight
- Shows a live countdown to the next UTC quest reset
- Stores a rolling history of the last 5 quest rolls with UTC timestamps
- Lets you click any history entry to restore that quest into the output
- Adds a manual “clear history” action to wipe quest history and reset the short repeat-avoid cache (without touching streak progress)
- Adds a manual “reset streak” button to restart the counter when needed
