# brand/

Assets for the BioLens lens-skin intro and outro. The full build and QC spec is
in `07_INTRO_OUTRO.md`.

## Included

| File | Use |
|---|---|
| `iris-motif.svg` | Six-blade aperture; the signature motif. Import at 2x, or export a 1024 px PNG if your editor rejects SVG. |
| `wordmark.svg` | BioLens wordmark; white display type, teal rule, cyan dot. |

## To render and add

| File | Spec |
|---|---|
| `intro-9x16.mp4` | 1.2 s, 1080x1920, 30 fps, H.264 |
| `outro-9x16.mp4` | 2.4 s, 1080x1920, 30 fps, H.264 |
| `intro-16x9.mp4` | optional, long-form |
| `outro-16x9.mp4` | optional, long-form |
| `audio/whoosh.wav` | glass focus tick plus sub-thud |
| `audio/sting.wav` | short teal tonal sting |
| `audio/outro-tone.wav` | one second, identical every post |
| `intro-template/` | optional CapCut project with replaceable layers |

## Rules

- Each committed file must be **under 5 MB**. Masters (ProRes, `.aep`, CapCut
  projects) live in Drive, not git.
- `.gitignore` allows the four named stinger `.mp4` files and
  `brand/audio/*.wav`; everything else media is still excluded.
- Name with the project and version, e.g. `biolens-intro-9x16-v1.mp4`. Bump the
  version; never overwrite.
