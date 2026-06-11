# Releases

This repository is the shared release channel and update feed for two local-first desktop apps.
Each app's in-app updater only reads its own tags, so the two never shadow each other.

| App     | Tag pattern       | Installer asset            |
|---------|-------------------|----------------------------|
| DEX     | `vX.Y.Z`          | `DEX-Setup-*.exe`          |
| Magnify | `magnify-vX.Y.Z`  | `Magnify_*_x64-setup.exe`  |

## Download

Open the [Releases](../../releases) page and pick the entry for the app you want:

- **DEX** — the plain `vX.Y.Z` releases (e.g. `v4.60.1`).
- **Magnify** — the `magnify-`-prefixed releases (e.g. `magnify-v0.8.1`).

Download the attached `.exe` and run it. Both are Windows x64 installers.

## Notes for maintainers

- Magnify releases are published with `--latest=false` so they never take the repository "Latest"
  badge from DEX (and vice-versa). Each app resolves its own newest version by filtering the
  releases list by its tag prefix.
- Keep the tag prefixes stable — the apps' in-app updaters depend on them.
