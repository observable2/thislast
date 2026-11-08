# THIS LAST

a looping kinetic-typography piece (version 3.0, spring 2026): THIS IS MY LAST TIME TO … with a verb (or “our”) rotating in.

Refactored (2026-11-08) from the Observable Framework project `thislast` into an
[Observable Notebook Kit](https://observablehq.com/notebook-kit/) project.
Co-implemented with Claude Sonnet 5.5.

## Commands

```sh
npm install
npm run preview   # http://localhost:5173
npm run build     # builds into dist/
```

## Where things went

- Framework → Notebook Kit: `index.md` + `globalstyle.css` → `nbks/index.html` (markup cell + animation cell), styles in `nbks/custom.tmpl`.
- Framework `observablehq.config.js`, `.observablehq/` cache and `rimraf` are no longer needed.
- Markup that JavaScript touches is created in a JS cell with `html` (cells run in dependency order, not page order, so the DOM must exist before code looks for it).

## Differences from the original

- Fonts: Nunito Sans is bundled from `@fontsource-variable/nunito-sans` (`full.css`, all axes) instead of the Google Fonts stylesheet; family name is `Nunito Sans Variable`.
- Page chrome (sidebar, header, footer, pager) is gone; Notebook Kit has none.
