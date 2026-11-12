# lofi-radio-mirror

Static mirror of the content catalog of the Lofi Radio Android app (`dope.capybara.lofi`).
The app loads its station manifest, music and scene pictures from `packs.dopecapybara.com`;
this repository serves the same files at the same relative paths, so the app can fall back to
another host when the main one is slow or unreachable on a given network.

Served from:

- `https://dopecapybara.github.io/lofi-radio-mirror/<path>` (GitHub Pages)
- `https://cdn.jsdelivr.net/gh/dopecapybara/lofi-radio-mirror@main/<path>` (jsDelivr)

## Contents

- `lofi/content-manifest.json` - the station manifest, byte-identical to the live one.
- `lofi/v1/tracks/*.mp3` - the broadcast playlist, re-encoded to 128 kbit/s CBR.
- `lofi/v1/art/*.webp` - scene pictures, 360x540.

The paths are the same as on the main host, for example
`lofi/v1/tracks/last-train-home.mp3`.

## Licenses

- Music: tracks from [Open Lo-Fi](https://github.com/btahir/open-lofi), released under
  [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/).
- Pictures: original artwork by Dope Capybara, all rights reserved. They are provided for use
  inside the app only.

## Maintenance

The files are written by a sync script in the app repository, not by hand. Do not edit them
here: the next sync overwrites the manifest and adds new files.
