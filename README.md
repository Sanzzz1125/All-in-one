# College Hub

A single page with quick shortcuts to every college portal and tool, so you're never hunting for a login link again.

**Live:** https://sanzzz1125.github.io/campus-hub/

## What's inside

- **College Portals** — Sraap, Sruniv, Canvas, GDB (OnlineGDB Classroom), Webminal, Timetable, Google Classroom
- **Quick Tools** — Timetable Clear, Empty Classroom Check
- Search bar to filter shortcuts by name
- Hover a card to see a short description of what it's for
- Light / dark theme toggle (remembers your choice)
- "Suggest a link / feedback" button that opens a Google Form
- Fully mobile responsive

## Structure

```
campus-hub/
├── index.html      # everything — markup, styles, and JS in one file
├── images/         # portal logos
└── README.md
```

## Running locally

No build step needed — it's a static page.

```bash
git clone https://github.com/Sanzzz1125/campus-hub.git
cd campus-hub
open index.html   # or just double-click it
```

## Adding a new shortcut

Inside `index.html`, find the relevant section (`College Portals` or `Quick Tools`) and add a card following this pattern:

```html
<a class="card" data-name="portal name" data-desc="Short description shown on hover" href="https://example.com" target="_blank" rel="noopener">
  <span class="icon">AB</span>
  <span class="card-name">Portal Name</span>
  <span class="card-url">example.com</span>
</a>
```

- `data-name` powers the search filter — keep it lowercase.
- `data-desc` is the tooltip text shown when someone hovers the card.
- `.icon` can hold either a two-letter initial or an `<img src="./images/...">` if you have a logo.
- Bump the `X links` count in that section's header.

## Deployment

Hosted via GitHub Pages from this repo. Pushing to `main` updates the live site.
