# 02 — BRAND SKIN: BIOLENS

> **The skin is the part that must never be identical to another project.**
> The shared engine (hook architecture, 12 categories, prompt formula, post
> format) is identical in every repo. This file is BioLens only.

---

## 0. The one law: be the opposite of the feed

**The expected look in this niche:** stock-footage macro clips, generic 3D
organ renders, purple-and-orange science gradients, shocked-face thumbnails,
and captions that fight the footage.

**Our opposite:** a quiet optical instrument. Dark slate, bio teal and lens cyan.
Real texture. A locked camera looking at something that should not be visible.
No face, no arrows, no hype typography.

The channel should read as a microscope someone left running — intimate,
clinical, slightly alien.

---

## 1. Skin brief

```markdown
SKIN BRIEF — BioLens

Archetype:            The Lens (optical, intimate, macro)
The expected look in this niche:   stock macro plus generic 3D organs, neon
                                    gradients, shocked-face thumbnails
Our opposite:         a quiet clinical instrument: dark slate, teal and cyan,
                      locked macro frames, no faces, no arrows

Palette
  background:  #1A2A3A   dark slate
  accent:      #0A9B8C   bio teal
  highlight:   #00D4FF   lens cyan
  text:        #FFFFFF   white
  secondary:   #7FE3D4   pale teal  (allowed only for: thin rules, scale ticks)
  ratio rule:  60 slate/near-black / 25 teal / 10 cyan / 5 white

Type
  display:     Poppins Bold
  body:        Inter Regular
  mono:        JetBrains Mono  (magnification, measurements, figure labels)

Fingerprints
  1 signature motif:    the lens iris / aperture blades
  2 frame furniture:    magnification chip, top-left; circular vignette
  3 transition:         lens-iris wipe plus a 0.15 s focus-pull
  4 label system:       specimen tag plus scale ruler, editor-built
  5 caption rule:       bottom third, Poppins Bold, six words maximum,
                        the key noun in lens cyan
  6 intro / sign-off:   iris opens to the wordmark; fixed sign-off line

Intro (see 07_INTRO_OUTRO.md)
  0.00–0.15 s:   black frame, silence
  0.15–0.45 s:   iris opens from a point to full frame, cyan edge glow, one hit
  0.45–0.90 s:   BioLens wordmark in Poppins Bold plus a ×40 chip snapping in
  0.90–1.20 s:   hard cut into Clip 1 with two frames of fine grain
  audio logo:    a glass focus tick plus a low sub-thud at 0.15 s

Outro
  end card:      iris closes to a teal ring around the wordmark
  CTA line:      Follow BioLens to see life differently.
  loop or cut:   cut clean, or loop to the iris point for rewatch bait

Motion grammar:   see section 3
Sound signature:  intro glass tick and sub-thud / bed minus 20 LUFS /
                  cue focus-pull tick / outro single low teal tone
Voice:            ElevenLabs, low stability, close mic, unhurried;
                  internally named The Curator
Sign-off line:    Follow BioLens to see life differently.
Handles:          @biolens on TikTok, YouTube, Instagram, Facebook
```

---

## 2. Palette rules

| Role | Hex | Use | Never |
|---|---|---|---|
| Background / shadow | `#1A2A3A` | frame base, negative space, vignette | as a flat full-frame wash with no texture |
| Primary accent | `#0A9B8C` | tissue rim light, fluid glow, key label underline | covering more than a quarter of the frame |
| Highlight | `#00D4FF` | edges, refraction, iris glow, magnification chip | as a gradient background |
| Text | `#FFFFFF` | captions, labels, scale numbers | more than six words per card |
| Thin rule | `#7FE3D4` | scale ticks, hairline rules, specimen tag border | as a fill |

**Ratio rule:** 60 slate/near-black · 25 teal · 10 cyan · 5 white. The accent is
an accent. If a frame looks like a teal poster, it is wrong.

**Palette clause for prompts:**
`colour palette: dark slate #1A2A3A background, bio teal #0A9B8C tissue and fluid highlights, lens cyan #00D4FF edge light, white #FFFFFF specular peaks, never neon purple or orange gradient.`

---

## 3. Motion grammar (every post runs this)

| Beat | Time | On screen | Editor-built |
|---|---|---|---|
| Signal | 0.00–0.15 s | black | intro |
| Iris open | 0.15–0.45 s | aperture blades open from a point | intro |
| Identity | 0.45–0.90 s | wordmark plus ×40 chip | intro |
| Clip 1: GRAB | 0.90 s+ | impossible first frame, hook spoken | no |
| Label | 2.0–4.0 s | specimen tag: series, species, scale | yes |
| Teach | 4–20 s | mechanism, one irreversible action per clip | no |
| Focus pull | any cut | 0.15 s rack focus bridging clips | yes |
| Escalation chip | 20–26 s | ×40 flips to ×400 at the reveal | yes |
| Payoff | 26–30 s | promise delivered on screen | no |
| Sign-off | last 1–1.5 s | iris ring plus CTA line | yes |

**Transitions are never requested from the model.** The prompt keeps the camera
locked. Every wipe, rack focus and chip is added in the editor so the optical
language stays identical across the catalogue.

---

## 4. The six fingerprints, defined

1. **Lens iris / aperture blades.** The signature mark. Intro, outro, and the
   thumbnail frame all use the same six-blade aperture. It is the only logo-like
   element allowed.
2. **Magnification chip.** Top-left, JetBrains Mono, white on a thin teal rule:
   `×40` for the opening frame, `×400` at the reveal. It is editor-built and
   accurate to the subject, never decorative.
3. **Lens-iris wipe and focus pull.** Cuts between clips pass through a 0.12 s
   iris wipe, then a 0.15 s rack focus. No hard cuts mid-mechanism; hard cut only
   from intro to Clip 1.
4. **Specimen tag plus scale ruler.** Bottom-left: series name, species name
   where relevant, and a ruler in micrometres or millimetres. The ruler appears
   only when scale is the point.
5. **Caption rule.** Bottom third, Poppins Bold, maximum six words, key noun in
   lens cyan. Captions are short enough to read in one glance and never cover
   the mechanism.
6. **Intro and sign-off.** Iris opens; iris closes. The same CTA line, spoken and
   written: "Follow BioLens to see life differently."

---

## 5. Intro and outro: build spec

> Working file: `07_INTRO_OUTRO.md`. Vector assets: `brand/iris-motif.svg` and
> `brand/wordmark.svg`.

### Intro — 1.2 s, 1080×1920, 30 fps

| Beat | Time | Visual | Audio |
|---|---|---|---|
| Cut in | 0.00–0.15 | pure `#1A2A3A`, no logo | silence |
| Signal hit | 0.15–0.45 | six-blade iris opens from a 4 px point to full frame, cyan rim light on the blades | glass focus tick plus low sub-thud |
| Identity | 0.45–0.90 | BioLens wordmark in Poppins Bold, white, centred; a `×40` chip snaps in top-left | short teal tonal sting |
| Snap out | 0.90–1.20 | two frames of fine grain, then hard cut to Clip 1 | cut to bed |

Rules: no fade, no logo animation longer than 0.5 s, no "hey guys", no subscribe
reminder. The last frame hard-cuts to Clip 1.

### Outro — 2.4 s, 1080×1920, 30 fps

| Beat | Time | Visual | Audio |
|---|---|---|---|
| Resolve | 0.0–0.4 | the final frame holds, colour matched to the last clip | bed continues |
| End card | 0.4–1.6 | iris closes to a teal ring around the wordmark; one line: Follow BioLens to see life differently. | sting, then bed fades |
| Hold or loop | 1.6–2.4 | hold the ring, or cut to the 0.00 frame for a loop | low teal tone, then silence |

The CTA overlay and the spoken CTA are the same sentence. Never put a URL in the
video.

### Audio logo

- **Cue:** glass focus tick (high, dry) plus a low sub-thud, layered on the same
  frame at 0.15 s.
- **Mix:** bed at −20 LUFS; tick peaks without clipping; outro tone is the same
  1 s every post.
- **Test:** eyes closed, one second. If it is not identifiable, it is not done.

---

## 6. Voice

- **Model:** ElevenLabs, one locked voice.
- **Name:** The Curator — quiet, precise, slightly awed. Not a narrator reading
  copy; a person who has just seen the thing through the lens.
- **Pace:** 135–150 words per minute. One full stop per clip. Never stack clauses.
- **Person:** second person when the process is inside the viewer; third person
  when the subject is non-human.
- **Forbidden:** "in this video", "scientists are baffled", "you won't believe",
  "nature is wild", exclamation marks, rhetorical questions in the narration.

---

## 7. Handles, bios, avatar

| Platform | Handle | Display name | Bio |
|---|---|---|---|
| TikTok | @biolens | BioLens | See life differently. The invisible machinery of life, in 32 seconds. Follow for the next one. |
| YouTube | @biolens | BioLens | See life differently. One hidden biological mechanism per short, sourced in the description. |
| Instagram | @biolens | BioLens | See life differently. Macro biology, magnified. New lens every weekday. |
| Facebook | @biolens | BioLens | See life differently. The biology you were never shown, one mechanism at a time. |

**Avatar:** the six-blade iris with a teal ring and the wordmark's B as the
centre. Designed inside the centre 80 percent circle. Must read at 40 px.
**Banner:** dark slate field, one macro texture strip, wordmark left, tagline
right. No faces.

---

## 8. Consistency checklist

- [ ] One archetype: The Lens
- [ ] Palette with hex codes and a written 60/25/10/5 ratio
- [ ] Three type roles: Poppins Bold, Inter, JetBrains Mono
- [ ] Five named fingerprints plus the intro/sign-off
- [ ] Fixed motion grammar table
- [ ] One voice, fixed settings
- [ ] One sound signature
- [ ] Named persona and fixed sign-off
- [ ] Captions work muted at 40 px
- [ ] Avatar legible at 40 px
- [ ] Two posts side by side read as one brand
- [ ] One post next to a competitor reads as a different species

---

## 9. Anti-patterns

- Neon gradients, purple/orange, chromatic aberration, glossy 3D organs.
- Shocked faces, red arrows, "you won't believe" thumbnails.
- More than five colours, or teal used as a background wash.
- A magnification chip that lies about the scale.
- Camera drift requested from the model to fake a transition.
- Changing the intro, the sign-off or the palette because one post
  underperformed. One post is a data point, not a trend.
