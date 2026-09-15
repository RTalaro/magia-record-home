# our-record
Magia Record Live2D home viewer. Static site, no build. Open `index.html`'s links: viewer, quotes/homescreen, sound mode.

## run it
Needs http (ES modules), so from repo root:

```
python3 -m http.server 8000
```

then http://localhost:8000/viewer.html

With auto-reload, watching only root + `magica` (skips the huge `assets/` etc):

```
npx --yes browser-sync start --server --files "*.html, magica/**/*" --port 8000 --no-open --no-notify
```

## notes
- Live2D models/BGM live in `assets/ma-re-data/` (local-only, not deployed). Missing = falls back to remote, don't panic.
- `S` stop, `C` snapshot. Mic lipsync needs https or localhost.
