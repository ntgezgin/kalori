# Kalori
- Stack: vanilla HTML/CSS/JS in a single `index.html`; PWA via `manifest.webmanifest` + `sw.js`. No npm, no build, no frameworks.
- UI text is Turkish; code, comments and commits are English.
- Data lives only in localStorage under one key (`kalori-data`); keep `validate()` in sync with any schema change.
- Always escape user text (`esc()`) before innerHTML; parse numbers with `num()` (accepts `,` and `.`); display with tr-TR.
- Colors only via `:root` CSS variables (light + dark). Mobile-first, max-width 560px.
- After changing any cached file, bump `CACHE` in `sw.js`.
- Test: extract the `<script>` to a temp file and run `node --check`; then serve with `python3 -m http.server` and drive with Playwright from outside the repo.
- Never commit test dependencies (no package.json / node_modules).
