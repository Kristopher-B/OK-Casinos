# AGENTS.md

## Cursor Cloud specific instructions

This is a static HTML/CSS/vanilla-JS website (OKCasinoGuide.com). There are no build tools, package managers, or backend services.

### Serving the site

Run a local HTTP server from the repo root:

```
python3 -m http.server 8080
```

Then open `http://localhost:8080/index.html` in a browser.

### Files

- `index.html` — Homepage (casino map, top casinos, comparison, visitor guides, news)
- `Choctaw-Durant.html` — Detailed casino guide page (note the capitalized filename)
- `style.css` — Shared stylesheet (the Choctaw page has its own inline styles)

### Gotchas

- **Case-sensitive filenames**: The homepage links to `casino-choctaw-durant.html` but the actual file is `Choctaw-Durant.html`. The dev server is case-sensitive.
- **No lint/test/build commands**: There is no package.json, no linter config, no test framework, and no build step. Validation is done by opening pages in a browser.
- **External fonts**: Google Fonts (Bebas Neue, Barlow, Barlow Condensed) are loaded via CDN. Pages will still render without internet but will fall back to system fonts.
