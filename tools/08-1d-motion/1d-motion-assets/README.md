# 1-D Motion Lab assets

## Files in use by `index.html`

| Filename | Role |
| --- | --- |
| `greencar.png` | Car A sprite. Native art noses right, so `index.html` only flips it (CSS `scaleX`) when velocity is negative. |
| `redcar.png` | Car B sprite. Same orientation/flip convention as Car A. |
| `pipe.png` | The reference-point marker each car passes (the "starting point" the scenario is measured from). One copy is placed per lane. |
| `track-strip.png` | The road texture actually drawn behind the cars — see below. |

## `track-strip.png` is derived from `track.png`

`track.png` (the original drop-in) has a huge transparent margin above and
below the actual road art — the visible strip (curb/asphalt/grass/dirt) is
only about 18% of the image's height, vertically centered in a much taller
transparent canvas. Stretched directly as a CSS background, that meant most
of each lane's height was invisible padding.

`track-strip.png` is that same art with the transparent margin cropped off
(rows ~320–462 of the original 724px-tall image, full width), so
`background-size: 100% 100%` in `.track-band` fills the lane with actual
road, no dead space, and no visible tiling seam since it's a plain stretch
rather than `background-repeat`.

If you swap in a new `track.png`, regenerate `track-strip.png` to match (crop
to the non-transparent rows) or the road will shrink back down inside its
lane the way it did before.

## Layout notes for `index.html`

- The scene has two stacked lanes (Car A on top, Car B below) so cars with
  different start times/positions don't visually overlap. Each lane gets its
  own `.track-band`, pipe, and car sprite, positioned via percentages of the
  `.motion-scene` box in the CSS.
- Cars and the pipe are anchored so their base sits on the road surface line
  within `track-strip.png` (measured at ~51% up from the cropped strip's own
  bottom edge) — if the art changes, that fraction (and the `.car-sprite`
  / `.pipe-sprite` `bottom:` values that use it) may need re-tuning.
