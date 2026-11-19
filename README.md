# Neon Coast — Poster Cover Studio (recorded rebuild of V4)

[![make.fun](https://make.fun/badge/gta6-cover-art-01.svg)](https://make.fun/bounty/gta6-cover-art-01)
[![rank](https://make.fun/badge/gta6-cover-art-01/hqnsyhrn/gta6-cover-art-01-v4-recorded-2/rank.svg)](https://make.fun/bounty/gta6-cover-art-01)
[![reward](https://make.fun/badge/gta6-cover-art-01/hqnsyhrn/gta6-cover-art-01-v4-recorded-2/reward.svg)](https://make.fun/bounty/gta6-cover-art-01)

An offline web app that turns any photos into a GTA 6-style poster, built for the
[make.fun bounty gta6-cover-art-01](https://make.fun/bounty/gta6-cover-art-01).

This is a recorded rebuild of the V4 "duo hero" entry: the default cover is a real poster —
two original protagonists (a woman in a pink blazer and a bearded man in a floral shirt,
generated with an image model — NOT GTA characters) leaning on a red convertible at sunset,
with a huge title drawn OVER the image, a tagline with real hierarchy, and a strip of three
distinct photos along the bottom. The 9-panel grid is still there as a layout, but the
cover no longer looks like a photo grid. Every file in this repo was written in a recorded
harness session; all 17 sample photos were generated fresh in that session.

- **Duo Hero (default)**: two protagonists together in one cinematic photo, huge Anton title over the image, Pacifico subtitle, tagline, heat stars and badge ribbon
- **One-click poster presets**: Sunset Duo, Neon Harbour, Sunset Chase, Gold Hour, Vice Nights — each a DIFFERENT poster with its own hero, title and tagline
- **17 distinct sample photos** — no repeats in any default cover
- **7 layouts**: Poster Hero, 9-Panel Grid, Hero + 8, Hero + 3, Full-Bleed, Tilted Snaps, Classic Poster
- **Multi-photo**: upload your own photos or use the 17 built-in samples; crop and position each panel
- **6 colour grades**: Sunset, Neon Vice, Teal Night, Heat Wave, Gold Hour, Mono Noir
- **Bold lettering**: Anton title + Pacifico subtitle + tagline (all OFL, in `app/fonts/`), halftone title block on grid layouts
- **PNG export in 4 sizes**: 1080×1080, 1080×1350, 1920×1080 and 1080×1920 (story)
- **Undo / redo, shuffle, film grain and vignette** — everything runs offline in the browser; photos never leave your machine

## Try it

```sh
node serve.ts
# open http://localhost:8080
```

## Entry

`main.ts` (Node 22) copies `app/` and `screenshots/` to the output directory and writes
`dossier.json` with the vendored make.fun library, as the kit's starter does:

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
```

All art and lettering is original (Anton and Pacifico under the SIL Open Font License, in
`app/fonts/`). No Rockstar Games logo, artwork or fonts. Sample photos were made with an
image model in the recorded build session.
