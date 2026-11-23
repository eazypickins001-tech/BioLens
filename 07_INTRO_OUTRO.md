# 07 — INTRO & OUTRO (BioLens)

> Working build file for the lens-skin intro and outro. The summary lives in
> `02_BRAND_SKIN.md` §5; the universal method (timings, build mechanics, export
> rules) lives in `_SHARED/intro-outro.md`. Open this file when you build,
> re-export or QC them.
>
> Generation prompts: `08_INTRO_OUTRO_PROMPTS.md`.

---

## 1. Non-negotiables

| Rule | Value |
|---|---|
| Intro length | 1.2 s (hard cap 1.5 s, absolute cap 2 s) |
| Outro length | 2.4 s (range 1.5–3 s) |
| Same every post | Same frames, same audio cue, same timing |
| Intro to Clip 1 | Hard cut, no fade or dissolve |
| Last clip to outro | No jump in light or colour |
| CTA | One line, spoken in Clip 4 and written in the outro |
| Muted | Motif, wordmark and CTA must read at 40 px |
| Audio | One audio logo, no trending audio |
| Branding | No "hey guys", no subscribe reminder, no logo animation over 0.5 s |

---

## 2. Assets in `brand/`

| File | Status | Notes |
|---|---|---|
| `brand/iris-motif.svg` | Included | Six-blade aperture, teal ring, cyan rim. Import at 2x. |
| `brand/wordmark.svg` | Included | BioLens wordmark, Poppins Bold style, white. |
| `brand/intro-9x16.mp4` | Included | 1.2 s, 1080x1920, 30 fps, H.264 with audio, 306 KB. |
| `brand/outro-9x16.mp4` | Included | 2.4 s, 1080x1920, 30 fps, H.264 with audio, 300 KB. |
| `brand/audio/whoosh.wav` | Mixed into the intro MP4 | Glass focus tick plus low sub-thud. |
| `brand/audio/sting.wav` | Mixed into the intro MP4 | Short teal tonal sting. |
| `brand/audio/outro-tone.wav` | Mixed into the outro MP4 | One second, same every post. |
| `brand/intro-template/` | Optional | CapCut project with replaceable layers. |

The repo ships the rendered MP4s, the vector assets and the spec. The MP4s
carry the audio cues on one mono track. Separate stems are optional; if you add
them, `.gitignore` allows `brand/audio/*.wav`, provided each file is under 5 MB.
Masters stay in Drive.

---

## 3. Intro — 1.2 s, 1080x1920, 30 fps

| Beat | Time | On screen | Audio |
|---|---|---|---|
| Cut in | 0.00–0.15 | Dark slate `#1A2A3A`, no logo | Silence |
| Signal hit | 0.15–0.45 | Six-blade iris opens from a 4 px point to full frame, cyan rim light on the blades, 2-frame scale pop 105 to 100 | Glass focus tick plus low sub-thud |
| Identity frame | 0.45–0.90 | BioLens wordmark in Poppins Bold, white, centred; `×40` chip snaps in top-left | Short teal tonal sting |
| Snap out | 0.90–1.20 | Two frames of fine grain or light leak at 30–50 percent opacity | Cut to the bed |

Rules: no fade, no greeting, no subscribe reminder. The final frame hard-cuts
into Clip 1.

---

## 4. Outro — 2.4 s, 1080x1920, 30 fps

| Beat | Time | On screen | Audio |
|---|---|---|---|
| Resolve | 0.0–0.4 | The last content frame holds, colour matched to the last clip | Bed continues |
| End card | 0.4–1.6 | Iris closes to a teal ring around the wordmark; one line: Follow BioLens to see life differently. | Sting, then bed fades |
| Hold or loop | 1.6–2.4 | Hold the ring, or cut back to the 0.00 iris point for a loop | Low teal tone, then silence |

The CTA overlay and the spoken CTA are the same sentence. Never put a URL in the
video; put it in the caption or bio.

---

## 5. Audio logo

- **Cue:** a dry glass focus tick layered with a low sub-thud, both landing on
  the same frame at 0.15 s.
- **Mix:** bed at −20 LUFS; the tick peaks without clipping; the outro tone is
  the same 1 s every post.
- **Test:** play the intro with your eyes closed. If you cannot identify the
  channel in one second, the cue is not distinctive enough yet.

---

## 6. Build in CapCut

First generate the visual plate with the prompts in `08_INTRO_OUTRO_PROMPTS.md`,
then build the text, chip and audio here.

1. New project: **1080x1920, 30 fps**.
2. Import `brand/iris-motif.svg` (export a 2x PNG if CapCut rejects SVG),
   `brand/wordmark.svg`, and one texture (fine grain or light leak).
3. **Intro, 1.2 s:** dark slate background; place the iris at 0.15 s and keyframe
   scale 105 to 100 (or opacity 0 to 100 to 0) so it hits rather than fades.
4. Place the wordmark at 0.45 s, centred, with a 2-frame scale pop 110 to 100.
   Add the `×40` chip top-left in JetBrains Mono, white on a thin teal rule.
5. Add two frames of grain or light leak at 0.90 s, then trim the total to 1.2 s.
6. **Outro, 2.4 s:** hold the last content frame to 0.4 s; animate the iris
   closing to a teal ring from 0.4 to 1.6 s; place the wordmark and the CTA line;
   hold or loop from 1.6 to 2.4 s.
7. Audio: glass tick and sub-thud at 0.15 s, sting at 0.45 s, outro tone under
   the end card. Match frames, not seconds, where possible.
8. Export both, then **save the project as a template** with replaceable layers:
   `biolens-intro-outro-9x16`.

For the detailed CapCut and After Effects mechanics, see
`_SHARED/intro-outro.md` §3–§4.

---

## 7. Export settings and naming

**Social exports:** H.264, 1080x1920, 30 fps, 8–12 Mbps, AAC 192 kbps.
**Masters:** ProRes 4444 or the editor project — keep these in Drive, not git.

```
brand/intro-9x16.mp4
brand/outro-9x16.mp4
brand/intro-16x9.mp4      optional, long-form
brand/outro-16x9.mp4      optional, long-form
brand/audio/whoosh.wav
brand/audio/sting.wav
brand/audio/outro-tone.wav
```

Name with the project and version: `biolens-intro-9x16-v1.mp4`. Bump the
version, never overwrite. Keep each committed file under 5 MB.

---

## 8. Wiring into every post

```
[INTRO 1.2 s] -> [CLIP 1 8 s] -> [CLIP 2 8 s] -> [CLIP 3 8 s] -> [CLIP 4 8 s] -> [OUTRO 2.4 s]
```

- Published runtime: 32 s content + 1.2 s intro + 2.4 s outro = **35.6 s**.
- Hard cut from intro to Clip 1.
- Outro's first frame continues the last clip's light and colour; no seam.
- The CTA overlay equals the CTA in the post block.
- Batch-assemble: apply the same intro and outro files to every post in one
  session.

---

## 9. QC checklist

- [ ] Intro is 1.2 s or less
- [ ] Outro is 2.4 s or less
- [ ] Both legible muted, at 40 px, in daylight
- [ ] Identity frame uses Poppins Bold, not a default
- [ ] Hard cut from intro to Clip 1
- [ ] No seam between the last clip and the outro
- [ ] One CTA, and it matches the post block
- [ ] Audio logo lands at 0.15 s and is identical every post
- [ ] No clipping; bed at −20 LUFS
- [ ] Exports named and versioned
- [ ] Template saved with replaceable layers
- [ ] Committed files are each under 5 MB

---

## 10. Rendered assets

`brand/intro-9x16.mp4` (1.2 s) and `brand/outro-9x16.mp4` (2.4 s) are included
and ready to place on the timeline: intro before Clip 1, outro after Clip 4.
They were rendered from this spec at 1080x1920, 30 fps, H.264 with AAC audio.
The iris motif and wordmark vectors remain in `brand/` for re-exports or edits.
If you re-render, keep each file under 5 MB and bump the version.
