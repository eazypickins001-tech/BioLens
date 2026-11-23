# 08 — INTRO & OUTRO GENERATION PROMPTS

> Two copy-paste prompts for Veo or Omni. They generate the **visual plate
> only** — iris, light, dust and palette. The BioLens wordmark, `×40` chip and
> CTA are added in CapCut, because AI video models garble text. The full build
> and QC spec is in `07_INTRO_OUTRO.md`.

**Settings for both prompts:** 9:16 vertical, 1080×1920, 30 fps, 8 s generation
(Veo max 8 s, Omni max 10 s). The mechanical move completes in the first
1–1.6 s, so trim the intro to 1.2 s and the outro to 2.4 s.

---

## 1. Intro prompt — iris opens

Copy this into the prompt box:

```text
Vertical 9:16 cinematic macro shot, locked camera, no zoom, no pan, no tilt, no rotation.

Subject: a precision six-blade mechanical iris, like a high-end camera aperture, machined from brushed bio-teal metal with a thin lens-cyan rim light.

Action: the iris begins as a tiny point of cyan light at the exact centre of the frame. The six blades rotate and retract outward in one continuous, fast mechanical movement, opening the aperture until the dark circular centre fills most of the frame and the blades sit at the edges. The movement completes in about one second, then the frame holds perfectly still.

Environment and light: deep dark-slate void, soft volumetric cyan haze, fine dust particles drifting through the opening, a hard rim light from the upper left, subtle teal reflections on the blade edges.

Style and palette: photoreal, clinical, high-detail, shallow depth of field, macro lens character. Dark slate background #1A2A3A, bio-teal blades #0A9B8C, lens-cyan edge light #00D4FF, white specular highlights. Keep the centre clean and uncluttered for a title overlay.
```

**Negative prompt:**

```text
text, letters, words, numbers, watermark, logo, subtitles, camera drift, zoom, pan, tilt, rotation, shaky camera, handheld, cartoon, plastic, CGI look, neon purple, orange, extra blades, deformed aperture, asymmetrical iris, blurry, low detail, flicker, people, hands
```

**After generation in CapCut:**

- Trim to **1.2 s**. If the open feels slow, speed the clip to 1.2–1.5× before trimming.
- Add **BioLens** in Poppins Bold, white, centred, from 0.45 s to 1.20 s, with a 2-frame scale pop 110→100.
- Add the `×40` chip top-left: JetBrains Mono, white on a thin teal rule.
- Audio: glass focus tick plus low sub-thud at 0.15 s; short teal sting at 0.45 s.
- Hard cut into Clip 1.

---

## 2. Outro prompt — iris closes

Copy this into the prompt box:

```text
Vertical 9:16 cinematic macro shot, locked camera, no zoom, no pan, no tilt, no rotation.

Subject: a precision six-blade mechanical iris, like a high-end camera aperture, machined from brushed bio-teal metal with a thin lens-cyan rim light.

Action: the iris starts fully open around a clean dark circular centre. The six blades rotate and glide inward in one continuous, smooth mechanical movement, closing the aperture to a perfect teal ring around the dark centre. The closing movement completes in about 1.6 seconds, then the ring holds perfectly still and pulses once with a faint cyan glow.

Environment and light: deep dark-slate void, soft volumetric cyan haze, fine dust particles, a hard rim light from the upper left, subtle teal reflections on the blade edges.

Style and palette: photoreal, clinical, high-detail, shallow depth of field, macro lens character. Dark slate background #1A2A3A, bio-teal blades #0A9B8C, lens-cyan edge light #00D4FF, white specular highlights. Keep the centre clean and uncluttered for a title and CTA overlay.
```

**Negative prompt:**

```text
text, letters, words, numbers, watermark, logo, subtitles, camera drift, zoom, pan, tilt, rotation, shaky camera, handheld, cartoon, plastic, CGI look, neon purple, orange, extra blades, deformed aperture, asymmetrical iris, blurry, low detail, flicker, people, hands
```

**After generation in CapCut:**

- Trim to **2.4 s**.
- Add **BioLens** in Poppins Bold, white, centred inside the ring, fading in from 0.4 s.
- Add the CTA from 0.8 s, two lines: **Follow BioLens** / **to see life differently.**
- Audio: soft sting at 0.4 s; low teal tone at 1.6 s.
- Hold the ring to 2.4 s, or loop back to the first frame.

---

## 3. Optional 16:9 versions

Use the same prompts and change the first line to `Horizontal 16:9 cinematic
macro shot`. Re-centre the wordmark and CTA for the wider frame. These are only
for long-form; the channel's shorts use 9:16.

---

## 4. Model notes

- **Veo:** 8 s max per generation, 9:16 supported. Generate 8 s, trim the useful part.
- **Omni:** 10 s max; 8 s is enough and trims faster.
- If the iris deforms or the camera drifts, regenerate with the negative prompt
  intact. Prefer a near-miss plus a speed ramp over endless retries.
- Keep the centre clean. The overlay needs a calm dark plate behind it.
- For a still end card or thumbnail, export the final frame.
- Do **not** ask the model to render "BioLens" or the CTA. Text comes out
  warped, and the channel's rule is that all text is editor-built.
