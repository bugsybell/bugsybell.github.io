# bugsybell.github.io

Host root for Circa's Universal Links (beta infrastructure).

- `.well-known/apple-app-site-association` — associates `/join/` and `/invite/` with the Circa iOS app.
- `join/index.html` — generic fallback page shown when the app isn't installed. It never validates or displays anything about a Circle.
- `.nojekyll` — required so GitHub Pages serves the `.well-known` folder.

The legal site lives in a separate repo (`circa-legal`) at `/circa-legal/` and is not affected by this repo.
Before public launch, links should move to a dedicated Circa domain; this host must keep working for previously shared links.
