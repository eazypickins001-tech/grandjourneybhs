# 02 — BRAND SKIN

> **Every project gets its own skin. This file is the method, not the look.**
>
> The shared engine (hook architecture, 12 categories, prompt formula, post
> format) is identical in every repo. The **skin** is the part that must never be
> identical. Two projects built from this template should be recognisable as
> different brands in a blind scroll test.

---

## 0. The one law: be the opposite of the feed

Do not design a look you like. Design the look that is **missing from the feed**
the audience is already scrolling.

**The expected look in this niche:** a licensed therapist talking to a ring
light; sad stock footage (rain on a window, head in hands, a person alone on a
bed); pastel quote cards; "5 signs of…" listicles; purple-blue gradients.

**Our opposite:** quiet cinematic still-life in the brand's deep plum and warm
white — empty rooms, a door left ajar, a chair, a coat, light doing the emotional
work. No faces. No tears. Dignified, not clinical, not saccharine.

---

## 1. The invariants (what every skin must define)

| # | Device type | What it does | This project's choice |
|---|---|---|---|
| 1 | **Signature motif** | One recurring visual object or gesture the feed recognises instantly | **The open door** — a door standing ajar, warm light spilling across the floor |
| 2 | **Frame furniture** | One persistent overlay in the same corner on every post | Top-left tag `GJBHS · BALTIMORE`; bottom-right series + step number |
| 3 | **Transition** | One repeatable cut device bridging shots | A 0.15 s warm light-leak wipe |
| 4 | **Label system** | How the category / episode / series label looks | Series stamp + `STEP 01` / `MYTH 03`, Avenir Heavy, mauve on warm white |
| 5 | **Intro + sign-off** | A fixed 0.5–1 s opening beat and a fixed closing frame | Door-light bloom into the wordmark; end card on warm white |
| 6 | **Caption system** | Type, position, highlight rule — must work muted | Bottom-third, word-by-word, near-black on a warm-white pill, key word in plum |

Anchors:

- **One palette** — five values with a written ratio rule (below).
- **One voice** — one ElevenLabs voice, locked settings, never changed mid-channel.
- **One sound signature** — one wooden door-click + one warm chime; a soft light shimmer on the interrupt; the same tonal tail on every outro.

---

## 2. Design process (summary)

1. Read the feed; write the "expected look" in one sentence (done in §0).
2. Pick the archetype that is its opposite — here: **Warm human**, held still.
3. Derive the palette from the brand, not from taste (done from grandjourneybhs.com).
4. Three type roles, no more.
5. Name five fingerprints (§3).
6. Write the motion grammar (§3).
7. Design intro and outro once (§3).
8. Lock voice, sound and human anchor.
9. Test at 40 px, on mute, side by side with a competitor.

### Healthcare modifier (this project only)

**Warm human** normally shows people. This project cannot: no client may ever be
depicted, and AI faces in a mental-health context read as fake or exploitative.
So the archetype is expressed through **the objects and rooms that hold a
person's story** — the chair, the coat, the door, the phone on the table, the
light in an empty hallway. This is the "absence over depiction" rule turned into
an aesthetic. It is also a performance advantage: no face means no uncanny
valley, and the viewer supplies their own.

---

## 3. Skin brief

```markdown
SKIN BRIEF — Grand Journey Behavioral Health Solutions

Archetype:            Warm human, held still (object-led; no faces)
The expected look in this niche:   Ring-light therapist talking heads, sad stock
                      b-roll, pastel quote cards, "5 signs" listicles.
Our opposite:         Quiet cinematic still-life — empty rooms, doors, chairs and
                      objects in deep plum and warm white. Dignified, never sad-porn.

Palette
  background:  #FFFFF6   warm white (page background, caption pills, end card)
  accent:      #816E7C   mauve (labels, key caption word, one accent object)
  shadow:      #360C42   deep plum (the brand colour; door frames, backgrounds, logo field)
  text:        #202020   near-black
  secondary:   #555555   body-grey text
  positive:    #1FDF67   brand green — allowed only for a "next step / you are here"
                          marker, never as a background or a whole object
  ratio rule:  70% warm white / 20% deep plum / 10% mauve + green accents
               Accent is an accent — never the background, never the whole frame.

Type
  display:     Futura LT Book (fallback: Futura, Century Gothic) — headlines, slams
  body:        Helvetica (fallback: Arial) — captions, longer text
  mono/labels: Avenir LT 85 Heavy (fallback: Montserrat ExtraBold) — labels, numbers

Fingerprints
  1 signature motif:    The open door — ajar, warm light across the floor; opens,
                        holds, or closes once per post
  2 frame furniture:    Top-left `GJBHS · BALTIMORE` in plum; bottom-right series
                        + step/myth number
  3 transition:         0.15 s warm light-leak wipe on every scene change
  4 label system:       Series stamp (`FIRST SESSION`, `MYTH MONDAY`) + STEP/MYTH
                        number, Avenir Heavy, mauve on warm white
  5 caption rule:       Bottom-third, word-by-word, near-black on a warm-white pill;
                        the key word in plum
  6 intro / sign-off:   Door-light bloom into `Grand Journey BHS`; end card on warm
                        white with the sign-off line

Intro (see _SHARED/intro-outro.md)
  0.00–0.15 s:   black frame, faint door outline in plum
  0.15–0.45 s:   warm light blooms from the door gap, one soft impact
  0.45–0.90 s:   wordmark `Grand Journey BHS` in Futura, plum on warm white
  0.90–1.20 s:   hold, then HARD CUT into Clip 1
  audio logo:    wooden door-click at 0.15 s + warm low chime at 0.45 s

Outro
  end card:      warm white, door motif, wordmark, phone number
  CTA line:      Call 833-888-0805.
  loop or cut:   cut clean — never loop (healthcare posts end on a question)

Motion grammar
  0.0–0.5 s   light-leak open / object in frame
  0.5–1.0 s   identity tag `GJBHS · BALTIMORE`
  1.0 s+      the footage (one irreversible action per clip)
  2–4 s       series + step label
  4–12 s      teach
  any cut     0.15 s light-leak wipe
  last 1 s    sign-off `You don't have to do this alone.`

Sound signature:  intro door-click + chime / bed −22 to −18 LUFS / cue soft light
                  shimmer / outro same tonal tail. No trending audio, ever.
Voice:            ElevenLabs, calm documentary register, 0.9× pace, low warmth,
                  no smiley affect. Internal name: "The Guide".
Sign-off line:    You don't have to do this alone.
Handles:          IG @grandjourneybhs_ · TikTok @grandjourneybhs · YouTube
                  @grandjourneybhs · Facebook "Grand Journey Behavioral Health
                  Solutions" · LinkedIn "Grand Journey Behavioral Health Solutions"
```

---

## 4. Worked examples (range references, not presets)

These five are from other projects. Use them to calibrate range. This project's
brief above is not a copy of any of them.

### A. The hijacked broadcast
Analog TV, colour bars, test cards, static. Palette: CRT black `#0B0B0C`, bone
`#EFE9DC`, signal red-orange `#FF3B00`. Type: Anton, Archivo, IBM Plex Mono.
Motif: the floating object. Voice: calm, slightly low. Best for impossible things.

### B. The specimen
Clinical, unnervingly clean. Palette: paper white `#F7F7F5`, ink `#14171A`,
specimen grey `#9AA3A8`, diagnostic red `#C8102E`. Type: Inter Tight, Source
Serif, JetBrains Mono. Motif: crosshair and `FIG. 0X`. Voice: flat, factual.

### C. The error dialog
Operating-system failure as brand. Palette: system grey `#D4D0C8`, window white,
alert red `#D40000`, link blue `#0000EE`. Type: Consolas. Motif: the unresolved
pattern. Voice: deadpan.

### D. The lens
Macro, optical, intimate. Palette: bio teal `#0A9B8C`, lens cyan `#00D4FF`, dark
slate `#1A2A3A`. Type: Poppins, Inter, mono. Motif: the invisible made visible.
Voice: hushed, second person.

### E. Warm human (cause / education / service)
Documentary stills, natural light. Palette: warm sand `#F2E8DC`, deep brown
`#3B2A20`, terracotta `#C4643B`, soft green `#6B7F5E`. Type: Fraunces, Inter.
Motif: the ordinary object that carries the story. Voice: conversational. This
project is the no-faces, brand-palette version of E.

---

## 5. Universal asset specs

### Handles and bios

| Platform | Handle | Display name | Bio limit |
|---|---|---|---|
| Instagram | @grandjourneybhs_ (existing) | Grand Journey Behavioral Health Solutions | 150 |
| TikTok | @grandjourneybhs (to claim) | Grand Journey BHS | 80 |
| YouTube | @grandjourneybhs (to claim) | Grand Journey Behavioral Health Solutions | 1000 |
| Facebook | Grand Journey Behavioral Health Solutions (existing page) | same | 255 |
| LinkedIn | Grand Journey Behavioral Health Solutions | same | 2000 |

**Bio (Instagram, 150):**
```
Mental health & substance use care in Baltimore.
Real steps, no jargon. Maryland Medicaid accepted.
Call 833-888-0805.
```

**Bio (TikTok, 80):**
```
Baltimore mental health & recovery care. Call 833-888-0805.
```

**Bio (YouTube, under 1000):**
```
Grand Journey Behavioral Health Solutions is a mental health and substance use
treatment provider in Baltimore, Maryland. This channel explains what care
actually looks like: psychiatric rehabilitation (PRP), individual, group and
family therapy, psychiatric evaluation and medication management, and outpatient,
intensive outpatient and partial hospitalization substance use treatment.

Maryland Medicaid HMO plans are accepted — call to confirm your plan. Call
833-888-0805 or email
admin@grandjourneybhs.com. 2200 Garrison Blvd Suite 103, Baltimore, MD 21216.

These videos are educational and are not medical advice or a diagnosis. If you
are in crisis, call or text 988.
```

### Dimensions

| Asset | Size |
|---|---|
| Video (all short-form) | 1080×1920 (9:16), H.264, ≥8 Mbps |
| Short-form cover | 1080×1920 — keep text in the top two-thirds |
| YouTube long-form thumbnail | 1280×720 |
| YouTube channel art | 2560×1440 (safe area 1546×423) |
| Facebook cover | 820×312 desktop / 640×360 mobile |
| LinkedIn cover | 1128×191 |
| Avatar (master) | 512×512 — export 800 (YT), 400 (X), 320 (IG/FB), 200 (TikTok) |
| Watermark | 400×125, 40% opacity, bottom-right |

**Avatar rule:** use the real GJBHS mark — never the door motif — inside the
centre 80% circle. The current site logo is a raster JPG, so request a
transparent PNG/SVG from the client before launch. Test at 40 px.

---

## 6. Consistency checklist

- [ ] One archetype, stated in one sentence
- [ ] Palette with hex codes and a written ratio rule
- [ ] Three type roles, no more
- [ ] Five named fingerprints
- [ ] A fixed motion grammar table
- [ ] One voice, fixed settings, named internally
- [ ] One sound signature
- [ ] A named human persona and a fixed sign-off
- [ ] Caption system that works muted
- [ ] Avatar legible at 40 px
- [ ] Two posts side by side read as one brand
- [ ] One post next to a competitor reads as a different species

---

## 7. Anti-patterns

- Copying the default AI look: neon gradients, purple/orange, chromatic
  aberration, glossy 3D.
- Copying the category's clichés: stethoscopes, brains in hands, a head in hands,
  rain on a window, puzzle-piece autism imagery.
- Showing any client or identifiable person in distress.
- A "healing hands" or "light at the end of the tunnel" stock metaphor.
- More than five colours, or a palette with no ratio.
- A motif that cannot be rendered at 40 px.
- Changing the skin mid-channel because one post underperformed.
