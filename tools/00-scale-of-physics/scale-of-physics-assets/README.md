# Powers of Ten icon assets

This folder contains 29 transparent 512×512 PNG icons named to match the `id`
values in the scale slider's `STOPS` array.

Copy the PNG files to:

```text
tools/00-scale-of-physics/assets/
```

Then each stop can render its image as:

```html
<img src="assets/<id>.png" alt="">
```

## Asset IDs

```text
planck quark proton nucleus atom molecule lattice dna virus bacteria cell
hair insect sand human car plane building mountain continent earth moonorbit
sun au solsystem lightyear proxima galaxy universe
```

## Production details

- PNG with RGBA transparency
- 512×512 pixels
- Subject centered inside a maximum 358×358 visible region (at least 15%
  padding on the long dimension)
- Hard-edged retro pixel-art treatment
- Palette coordinated to the Powers of Ten page
- Transparent corners and alpha channels validated for all 29 files
