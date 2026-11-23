# 06 — SOP (standard operating procedure)

> Filled once for this project. The stages are the template; the rhythm and the
> clinical gate are this project's.

---

## 1. Toolchain

| Job | Tool | Notes |
|---|---|---|
| Video generation | Veo (8 s/clip), Omni (10 s/clip) | Locked camera; 6 s default |
| Stills (props, objects, textures) | Flux / Midjourney / Ideogram | Build the door, chair and coat once; reuse the edited still |
| Editing + text + captions | CapCut | All text, steps and numbers built here, never generated |
| Intro & outro | CapCut / After Effects | Built once; see `_SHARED/intro-outro.md` and `02_BRAND_SKIN.md` §3 |
| Data, steps, phone numbers | After Effects / CapCut | Never AI-generate figures or phone numbers |
| Voice | ElevenLabs (locked settings, "The Guide") | One voice for the channel |
| Real clinic footage | GJBHS phone / consented staff | Signed release on file before publishing |
| Archive / stock | Licensed or owned only | Never AI for a real place or real event |
| Storage | GJBHS Drive folder | Mirror of git-tracked files only |
| Repo | GitHub | Source of truth for words and prompts |
| Clinical review | GJBHS clinical lead (named in Drive) | Required gate before generation |

**Rule:** video, audio and footage never enter git. If a file is over ~5 MB it
does not belong in the repo.

---

## 2. Weekly rhythm

| Day | Work |
|---|---|
| Mon | Pick topics; check rotation; write hooks; send scripts to clinical review |
| Tue | **Clinical review sign-off** (accuracy, claims, safety); write clip tables |
| Wed | Generate AI clips (batch by category/technique) |
| Thu | Edit, add text and labels, build the fixed intro/outro, voice |
| Fri | Publish the strongest post; schedule the rest |
| Sat | Community: reply, pin, collect comments; route clinical questions to the front desk |
| Sun | Log numbers in `05_PROOF_TRACKER.md`; weekly review; update the queue |

Two fixed days: **Tuesday review**, **Friday publish**. Nothing is generated
before the clinical sign-off.

---

## 3. Per-post pipeline

```
1 PLAN       topic → pillar → category (differs from last post) → hook
2 SCRIPT     clip table, one irreversible action per clip
3 CLINICAL   clinical lead signs off: accuracy, claims, safety, no PHI
4 PROMPT     six parts + negatives, palette clause, no faces
5 VALIDATE   node tools/validate-posts.js 03_POST_BANK.md
6 GENERATE   AI clips first; real footage only for real GJBHS spaces
7 EDIT       text, series stamp, step number, light-leak cuts, sound
8 ASSEMBLE   wrap with the project's intro and outro (built once)
9 CAPTION    platform caption + hashtags + disclaimer + pinned comment
10 PUBLISH   publish, pin immediately, reply; never confirm patient status
11 LOG       row in 05_PROOF_TRACKER.md at 24h / 7d / 30d
```

---

## 4. Quality gates (all must pass before render)

**Script gate**

- [ ] Hook is the interrupt, inside 0.8 s
- [ ] One idea only
- [ ] Payoff delivered before the CTA
- [ ] Category differs from the previous post
- [ ] Pillar respects the standing instruction

**Clinical gate (this project)**

- [ ] No diagnosis, no individualized advice, no outcome promise
- [ ] No client or identifiable person in distress; no AI faces in a care context
- [ ] No PHI anywhere (captions, comments, screenshots, DMs)
- [ ] Service claims (Medicaid, CARF, programs, hours) verified with the front office
- [ ] Crisis line (988) present wherever symptoms or substance use are mentioned
- [ ] Education disclaimer in the caption
- [ ] Staff on camera has a signed release on file

**Prompt gate**

- [ ] Six parts present, in order
- [ ] Effect stated as verb + direction
- [ ] Camera locked or motion explicitly resolved
- [ ] Negative prompt on every clip, including `text, letters, watermark`
- [ ] Palette clause included (`02_BRAND_SKIN.md` §3)
- [ ] Clip within the model limit (Veo 8 s / Omni 10 s)

**Integrity gate**

- [ ] Proof is real (screenshots only of real, permissioned material)
- [ ] No AI standing in for archive, staff or evidence
- [ ] No fabricated testimonials, reviews or accreditation marks
- [ ] Sources ready for every claim that matters

**Packaging gate**

- [ ] Intro is the project's own, ≤1.5 s, hard-cut into Clip 1
- [ ] Outro is the project's own, 1.5–3 s, one CTA, no seam
- [ ] Intro and outro are the same files used on every other post
- [ ] Door-click + chime land on the same frames every time
- [ ] Published runtime (content + intro + outro) stays inside 22–35 s / 40–60 s
- [ ] Captions and series stamps read at 40 px and on mute

**Publish gate**

- [ ] Caption's first line is the hook
- [ ] 8–12 hashtags across three tiers
- [ ] Disclaimer + 988 line in place
- [ ] Pinned comment ready
- [ ] Logged in the tracker

---

## 5. Batch production (the efficiency rule)

Batch by **technique**, not by post:

1. Generate every "door / light spill" clip in one session.
2. Generate every "empty room / object" clip in one session.
3. Then assemble per post.

This keeps the model's look consistent across the catalogue and halves generation
time.

---

## 6. Failure handling

| Failure | Fix |
|---|---|
| Camera drift | Add `locked camera, no zoom pan tilt or rotation`; move the effect to the object |
| Text garbled in generation | Remove all text from the prompt; build it in the editor |
| Object too small in frame | State scale explicitly: "filling the frame", "lower two-thirds" |
| The scene reads as sad-porn | Remove the sad music, raise the light, cut the slow zoom; replace a "head in hands" idea with the object |
| A face appears in a care context | Regenerate or crop; faces only for consented staff |
| Effect looks decorative | Re-read the selection matrix; the category must mean something |
| Post underperforms | Check 3 s hold first. Low hold = hook. High hold + low completion = payoff |
| A claim is challenged in comments | Do not argue; verify with the front office, correct publicly, keep the receipt |

---

## 7. Repo hygiene

- Commit posts as they are written; the post number in the message.
- Never hand-edit generated files.
- Update the standing instruction in the same commit as the evidence.
- When a rule conflicts with a newer decision, update the manual in the same
  commit — never leave the repo self-contradictory.
- Never commit PHI, client names, staff personal data or unapproved screenshots.
