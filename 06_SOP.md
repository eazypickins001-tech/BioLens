# 06 — SOP (standard operating procedure)

> Filled once for BioLens. The stages themselves are the template.

---

## 1. Toolchain

| Job | Tool | Notes |
|---|---|---|
| Video generation | Veo (primary), Omni (secondary) | 8 s clips on Veo, 10 s max on Omni; locked camera |
| Stills (props, textures, inserts) | Flux / Midjourney / Ideogram | Edit a near-miss over regenerating |
| Editing + text + captions | CapCut | All text, chips, rulers built here, never generated |
| Intro and outro | CapCut / After Effects | Built once from `02_BRAND_SKIN.md`; reused unchanged |
| Data, labels, magnification | CapCut / After Effects | Never AI-generate figures |
| Voice | ElevenLabs, one locked voice "The Curator" | 135–150 wpm, close mic, low stability |
| Music and sound | Licensed library | No trending audio |
| Storage | Project Drive folder | Mirror of git-tracked files only |
| Repo | GitHub `eazypickins001-tech/BioLens` | Source of truth for words and prompts |

**Rule:** video, audio and footage never enter git. If a file is over ~5 MB it
does not belong in the repo.

---

## 2. Weekly rhythm

| Day | Work |
|---|---|
| Mon | Pick 5 topics from the queue; check pillar and category rotation; write hooks |
| Tue | Write clip tables and six-part prompts for the week |
| Wed | Generate all clips, batched by technique, not by post |
| Thu | Edit, add chips, rulers and labels, record voice, build intro and outro |
| Fri | Publish the strongest post; schedule the rest; pin comments |
| Sat | Community: reply, pin, collect comments for next week's hooks |
| Sun | Log numbers, weekly review, update the queue and the standing instruction |

Adjust to the cadence in `00_DNA.md`, but keep **one** publishing day and **one**
review day.

---

## 3. Per-post pipeline

```
1 PLAN      topic, pillar, category differs from last post, hook
2 SCRIPT    four clips, one irreversible action per clip
3 PROMPT    six parts plus negatives, palette clause, locked camera
4 VALIDATE  node tools/validate-posts.js 03_POST_BANK.md
5 GENERATE  Veo clips first; all text is editor-built
6 EDIT      iris wipes, focus pulls, magnification chips, scale ruler, captions
7 ASSEMBLE  wrap with the BioLens intro and outro, unchanged
8 CAPTION   platform caption, hashtags, pinned comment, source line
9 PUBLISH   publish, pin immediately, reply
10 LOG      row in 05_PROOF_TRACKER.md at 24 h / 7 d / 30 d
```

---

## 4. Quality gates (all must pass before render)

**Script gate**

- [ ] Hook is the interrupt, inside 0.8 s
- [ ] One idea only
- [ ] Payoff delivered before the CTA
- [ ] Category differs from the previous post
- [ ] Pillar respects the 70/30 standing instruction

**Prompt gate**

- [ ] Six parts present, in order
- [ ] Effect stated as verb plus direction
- [ ] Camera locked or motion explicitly resolved
- [ ] Negative prompt on every clip
- [ ] No text requested from the model
- [ ] Clip within 8 s on Veo, 10 s on Omni
- [ ] Palette clause includes the BioLens hex codes

**Integrity gate**

- [ ] Proof is real
- [ ] No AI standing in for archive or evidence
- [ ] No fabricated documents or studies
- [ ] No identifiable person in a negative context
- [ ] Sources ready for every claim that matters
- [ ] No medical advice in human posts

**Packaging gate**

- [ ] Intro is the BioLens iris open, 1.2 s, hard cut into Clip 1
- [ ] Outro is the BioLens iris close, 2.4 s, one CTA, no seam from the last clip
- [ ] Intro and outro are the same files used on every other post
- [ ] Audio logo lands at 0.15 s on every post
- [ ] Published runtime stays inside 22–35 s for social, 40–48 s for story
- [ ] Captions and chips read at 40 px and on mute

**Publish gate**

- [ ] Caption's first line is the hook
- [ ] 8–12 hashtags across three tiers
- [ ] Pinned comment ready
- [ ] Source line present when needed
- [ ] Logged in the tracker

---

## 5. Batch production (the efficiency rule)

Batch by **technique**, not by post:

1. Generate every macro touch-down clip in one session.
2. Generate every cross-section or cutaway clip in one session.
3. Generate every pull-back or scale-reveal clip in one session.
4. Then assemble per post.

This keeps the optical look consistent across the catalogue and cuts generation
time roughly in half.

---

## 6. Failure handling

| Failure | Fix |
|---|---|
| Camera drift | Add `locked camera, no zoom pan tilt or rotation`; move the effect to the subject |
| Text garbled in generation | Remove all text from the prompt; build it in CapCut |
| Subject too small in frame | State scale explicitly: "filling the frame", "occupying the lower two-thirds" |
| Effect looks decorative | Re-read the selection matrix; the category must mean something |
| Anatomy looks wrong | Reduce to one structure per clip; add `anatomical accuracy, single specimen` and a strong negative list |
| Post underperforms | Check 3 s hold first. Low hold means the hook. High hold plus low completion means the payoff |

---

## 7. Repo hygiene

- Commit posts as they are written; the post number in the message.
- Never hand-edit generated files.
- Update the standing instruction in the same commit as the evidence.
- When a rule conflicts with a newer decision, update the manual in the same
  commit — never leave the repo self-contradictory.
