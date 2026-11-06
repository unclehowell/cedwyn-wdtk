# Cedwyn FOI Requests — `/wdtk/`

This repository is the source of truth for the FOI Requests application published at:

- https://cedwyn.bucklerfamily.estate/wdtk/

## Source and layout

The application was split from `unclehowell/cedwyn`, branch `whatdotheyknow`, on 6 November 2026.

- `public/` is the static site assembled into Cedwyn at `/wdtk/`.
- `public/data/` contains the machine-readable request index and thread data.
- `public/r/` contains the corresponding rendered request pages.
- The static-site version is recorded in `.version`; release notes are in `CHANGELOG.md`.
- `APP-README.md` preserves the application-specific description that was on the source branch before the split.

The source tree was compared with the source branch tip `43d778bf95fa604ded88b331a5c0c418c0d996f1`: all 35 paths matched, and every application blob matched. The repository README is intentionally replaced with these repository instructions; the original application description is retained in `APP-README.md`.

## Where to make changes

The current `split-repos.json` entry in `unclehowell/cedwyn` sets this application to `mode: split-repo`. Make application changes here, on a feature branch, and open a pull request into this repository's `main`.

After changes are merged, Cedwyn's `sync-split-repos` workflow copies this repository back into the legacy `whatdotheyknow` branch. The central `build-cedwyn` workflow then assembles the unified site. The legacy branch and public URL are retained for compatibility; do not use the legacy branch as the development target.

Clone only this application:

```bash
git clone --depth 1 https://github.com/unclehowell/cedwyn-wdtk.git
```

## Rights and privacy

The repository's `LICENSE` and `NOTICE` govern reuse. In particular, correspondence is reproduced from WhatDoTheyKnow, the notice explains the public-sector material and redactions, and the static pages link to the full request threads. Preserve those protections when changing the application. Do not add private correspondence or unredacted personal information.

## History before the split

The application history remains on the legacy branch:

https://github.com/unclehowell/cedwyn/commits/whatdotheyknow
