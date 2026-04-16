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
- `game.html` — playable Sky Sprint mini-game with classic + daily challenge modes
- `gallery.html` — image showcase wall + featured art drops
- `wallpapers.html` — downloadable SVG wallpaper packs in desktop + phone sizes
- `changelog.html` — release history + filterable flight log
- `quest-forge.html` — customize the quest generator pool (defaults + custom + JSON import/export)
- `flight-deck.html` — roadmap board + filterable ship log for visible product progress
- `notes.html` — searchable field-notes archive with tag filters + surprise picker
- `signal-board.html` — unified searchable timeline across ships + notes with quick filters and deep links
- `roost-atlas.html` — interactive relationship map linking ships, notes, and destination pages
- `roost-lab.html` — interactive style prototyping studio with live token controls, contrast checks, and CSS export
- `captains-log.html` — digest studio that generates shareable markdown recaps from ships + notes
- `assets/` — image assets + shared JSON data for dynamic sections (`roost-updates.json`, `roost-notes.json`)

## New in this iteration

- **Roost Lab launch:** added `roost-lab.html`, an interactive theme studio with persistent controls, live preview stress-testing, contrast status, and one-click CSS token export
- **Captain's Log launch:** added `captains-log.html`, a digest studio that generates markdown summaries from shared update/note data with time-window and focus filters
- **Roost Atlas launch:** added `roost-atlas.html`, an interactive graph that maps relationships between ships, notes, and pages with zoom/pan controls, scope filters, and quick-link detail cards
- **Signal Board launch:** added `signal-board.html`, a new cross-site timeline that merges releases and notes into one filterable stream with search, tag/type filters, and direct destination links
- **Sky Sprint challenge expansion:** upgraded `game.html` with a UTC-seeded daily challenge mode, dynamic modifiers, bronze/silver/gold tiers, run-history bars, and streak tracking for repeat play value
- **Wallpaper pack drop:** launched `wallpapers.html` with three downloadable SVG wallpaper packs, each shipping in desktop + phone formats
- **Gallery upgrade:** repositioned the gallery around a featured art drop instead of static image-only cards
- **Connected story mode:** releases, field notes, and destination pages now cross-link so visitors can follow a ship from launch → rationale → feature surface
- **Shared content relationships:** expanded `assets/roost-updates.json`, `assets/roost-notes.json`, and `assets/wallpapers.json` with metadata for related notes, destination pages, and downloadable assets
- **Homepage spotlight redesign:** added a story spotlight plus richer latest ships/notes cards with direct jump links instead of plain text summaries
- **Flight Deck + changelog upgrade:** both pages now render from shared release data and expose note/page links for each ship entry
- **Field Notes deep links:** note cards now surface linked ships, related pages, and URL-hash navigation for direct sharing/bookmarking

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
