# bugsybell.github.io

Host root for Circa's Universal Links (beta infrastructure).

- `.well-known/apple-app-site-association` — associates `/join/` and `/invite/` with the Circa iOS app.
- `join/index.html` — fallback page for the persistent, reusable Circle link (`circle_invite_links`). Hands off to `circa://join#<token>`.
- `invite/index.html` — fallback page for the one-time, email-bound Circle invitation (`circle_invitations`). A separate mechanism from `join/` — hands off to `circa://invite?token=<token>` instead. Both pages never validate or display anything about a Circle; the token stays in the URL fragment (never sent to this server) until the local `circa://` hand-off.
- `.nojekyll` — required so GitHub Pages serves the `.well-known` folder.

The legal site lives in a separate repo (`circa-legal`) at `/circa-legal/` and is not affected by this repo.
Before public launch, links should move to a dedicated Circa domain; this host must keep working for previously shared links.
