# Nelearn Interior Design (GitHub Pages build)

A self-paced interior design learning site by Allen, built with Claude (Anthropic) as a collaborator.
It is a static, single-page site: no build step, no backend, no API keys.

## Structure
```
index.html   the whole site (HTML, CSS and JavaScript inline)
.nojekyll    tells GitHub Pages to serve files as they are
README.md    this file
```
Pages are reached with hash routes (`#/library`, `#/glossary`, `#/designers`, ...), so refreshing or sharing a link works under any repository path.

## Deploy on GitHub Pages
1. Create a repository (e.g. `nelearn`) and upload the three files at the repository root.
2. Open Settings > Pages. Under Build and deployment choose Source: Deploy from a branch, Branch: `main`, folder `/ (root)`. Save.
3. After about a minute the site is live at `https://USERNAME.github.io/REPOSITORY/`.

## External dependencies
- Google Fonts (Cormorant Garamond and Inter), loaded from fonts.googleapis.com. Without internet the site falls back to Georgia and system sans-serif. To self-host, download the two families, put the files in `fonts/` and replace the `<link>` in `index.html` with `@font-face` rules.
- Reference links (Wikipedia, Wikimedia Commons, software sites, journals) open external pages and are meant to stay external.
- Progress, notes and portfolio data are stored in the browser's localStorage (key `ida_v1`) on the `USERNAME.github.io` origin. Use "Export JSON" on the Progress page for backups. Data does not sync between browsers.
