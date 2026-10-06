# GBCL Worship Songs

Worship song library, setlist builder and slide presenter for Grace Baptist Church of Liloan. It is an installable web app (PWA) that works offline once loaded.

**Live app:** https://ptrjohnreysumayang.github.io/Worship-Songs/

## Features

- **Library**: 254 built-in songs. Search by title or lyrics, sort by recently added or A–Z, and browse as grid, list, details or tiles.
- **Import**: drag in or pick one or more PowerPoint (.pptx) song files. Duplicates are skipped.
- **Edit**: open a song to rename it or edit, add and remove its slides.
- **Setlist**: build a program, reorder songs and give it a name.
- **Present**: full-screen slideshow. Use ← → or Space to move, Esc to exit.
- **Lyrics view**: all of a song or setlist on one scrolling page. You can change the text size and show or hide section labels.
- **Export**
  - PowerPoint (.pptx) of the setlist, using your slide design
  - Lyrics as Print / PDF, Word (.doc) or plain text (.txt)
- **Slide design**: title and lyric font, color and size, a white, color, parchment or photo background, and an optional logo.

Imported songs, edits, setlists and design settings are saved in each device's browser storage.

## Files

```
index.html             the whole app (songs, artwork and code inlined)
manifest.webmanifest   app name, icons, theme color #14143c
sw.js                  service worker (offline cache)
icons/                 192, 512, maskable 512, apple-touch, favicon
```

## Hosting on GitHub Pages

1. Push these files to the root of the `main` branch.
2. On GitHub: **Settings → Pages → Build and deployment**. Set Source to *Deploy from a branch* and Branch to `main` / `(root)`.
3. Open the Pages URL. Install it from the browser:
   - Desktop Chrome/Edge: use the **Install** pill.
   - Android: use the **Install** pill or the browser banner.
   - iPhone/iPad: Share → **Add to Home Screen**.

Install only works over `https://` or `http://`. Opening `index.html` straight from disk runs the app, but it can't be installed.

## Updating

Every time you replace `index.html`, raise `VERSION` in `sw.js` (it is currently `gbcl-songs-v3`). Returning users will see a **"A new version is ready → Reload"** prompt. Their own songs and setlists are kept.

## Changelog

- **v3**: lyrics view (one page per song or setlist), with Print/PDF, Word and text export.
- **v2**: new GBC Liloan logo, navy/royal-blue palette, regenerated icons.
- **v1**: first PWA release.
