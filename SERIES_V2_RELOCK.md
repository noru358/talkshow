# TALKSHOW — SERIES V2 RELOCK

Updated: 2026-09-04 KST  
Status: **ACTIVE — visual baseline established; performance/audio baseline relocked from real P002 evidence**

This file records the deliberate V2 reopening after P001 and the subsequent P002 production learnings. It exists so later sessions do not accidentally revert to sparse sets, restrained reactions, fixed-duration-first speech, phoneme-perfect facial animation, or pilot-for-pilot testing.

## Why V2 was reopened

The earlier sparse-room architecture improved reproducibility but created a weak product:
- room looked under-produced
- recurring cast chemistry felt too restrained
- old male styling was under-designed
- random/native generated voices were not acceptable as recurring identity
- micro-reaction controls produced an education-channel energy instead of a lively friend-chat show

V2 therefore keeps strict visual authority while deliberately increasing social/physical performance amplitude.

## Relationship to earlier P001 work

P001 V1 files remain historical evidence. Do not delete them.

Superseded series-level assumptions:
- no need to keep testing isolated P001 Scene B before a real episode
- `SET_MASTER_01` is evidence, not the preferred final set
- `subtle acting`, `small reactions`, or blanket `no large gestures` are no longer V2 defaults
- `2 x 8 sec` is not a mandatory episode structure

## Series V2 locked decisions

### 1. Recurring cast
Core:
- `CHAR_B` / white-T-shirt woman
- `CHAR_06`
- current recurring male identity / `RIGHT_MASTER_V2`

Active reference image overrides stale prose for visible face, hairstyle, outfit, proportions and set details.

### 2. Male styling
Old gray hoodie / messy-hair styling is retired as preferred recurring styling.

Target:
- ordinary put-together Seoul man, 20s/early-30s
- contemporary Korean daily/minimal casual
- neat hair; avoid exaggerated spiky back hair / Japanese-manga silhouette
- no bag / strap
- no glasses
- simple enough for low-fi 2D reproduction

Episode-specific active image can supersede historical outfit prose.

### 3. Four recurring sets
Keep all four:
- `SET_A_HOME`
- `SET_B_CONVENIENCE`
- `SET_C_HANGANG`
- `SET_D_ROOFTOP`

No set is discarded merely because another is used more often.

### 4. Reproducibility architecture

> **CHARACTER MASTER PACKS → recurring SET / CANONICAL CAST STILL → minimum shot-specific derived first-frame only when required → video generation → edit/crop**

Do not rebuild locations or character identities from prose every episode.

For recurring internet-post openings, reusable opening stills are valuable because the phone contains no episode-specific readable text. A new still is required only when a genuinely new starting prop/pose is needed.

### 5. Composition
- generation master: **16:9**
- final Shorts distribution: 9:16 editorial crop / punch-in
- fixed frontal or slightly elevated camera baseline
- medium-wide group framing with hands/upper body visible enough for larger reactions
- do not ask Omni to vertically redesign a 16:9 canonical image as a new 9:16 scene

Real P002 evidence showed that vertical recomposition can cause style/face redesign, while a concise 16:9 visual-lock prompt preserved the source drawing language materially better.

### 6. Visual prompt principle

The active image controls appearance. Video text controls motion/performance.

Do not redundantly describe every visible face, outfit and drawing feature. Over-description can encourage reinterpretation.

Compact lock:

```text
Use IMAGE 1 as the strict visual authority.
Animate the existing illustration only.
Do not redraw, redesign, restyle, beautify, modernize, or reinterpret it.
Preserve the original faces, eye designs, hairstyles, linework, proportions, colors, clothing, objects, background, and 16:9 composition.
```

### 7. Voice status
Historical/interim TopView references:
- LEFT: Gaeun outdoors
- CENTER: Harin
- RIGHT: Taemin

These are **not final recurring production voices yet**.

The 4-sec trimmed previews solved the observed 15.2-sec reference-audio ceiling and Taemin loudness imbalance, but the real P002 speech still sounded too mechanical.

Current voice/performance architecture is defined in `PERFORMANCE_AUDIO_ARCHITECTURE.md`:
- whole-scene dialogue generated once
- natural timing first
- video duration derived from that performance
- same dialogue master drives Omni timing and is reused as final publishable audio

### 8. Performance / reaction amplitude — increased again

V2 target:
> **bigger, funnier, socially physical, causally staged, and still geometry-aware.**

Allowed / desired when motivated:
- clear eye direction and face changes
- strong head turn
- substantial torso lean/recoil
- arm fully extended while making a point
- phone clearly extended toward friends
- two-hand disbelief
- posture shift / fidget / turning body toward another character
- hand to forehead / face-covering
- bending forward laughing
- irritated/exasperated body language
- brief table tap
- quick celebratory movement
- **brief playful contact**, e.g. one friend taps another's upper arm/shoulder

For contact, specify exact contact location and brief duration rather than vague `hit` language.

Baseline for an ~8–12 sec-ish compact clip:
- about 1–2 larger physical beats
- plus facial/head/torso reactions
- reactions remain causally staggered rather than all firing simultaneously

Avoid only genuinely unstable behavior:
- prolonged complex body entanglement
- hands crossing faces for long periods
- full-body flailing without a story reason
- anatomy/object warping

### 9. Eye acting — expressive, but transitions must be clean

Do **not** ban blinking or closing eyes.

Allowed and useful:
- blink
- wink
- eye-smile
- wide-eyed surprise
- eyes squeezed shut for laughter/frustration

Hard fail:
- melted or misaligned eyes
- asymmetric accidental half-closure
- ambiguous intermediate state where the eye is neither intentionally open nor cleanly closed

Prompt principle:

```text
Natural blinking, winking, eye-smiles and motivated eye closure are allowed.
Every eye action must form one clean intentional expression.
Preserve the original eye design before and after the expression.
Never create melted, misaligned, ambiguously half-closed in-between eye shapes.
```

### 10. Mouth animation — plausibility over phoneme perfection

Real P002 evidence showed that phoneme-perfect Korean lip-sync looks uncanny on the simple webcomic faces.

New rule:
- correct active speaker / turn timing matters
- exact Korean mouth phonemes do not
- use a few small stylized 2D mouth states
- avoid large jaw motion, wide vowel shapes, realistic lip pursing, face reshaping

Target is believable hand-drawn mouth-flap rhythm.

### 11. Opening grammar
Recurring visual device:
- one friend already has the phone where useful
- opener varies naturally (`야 이거 봐`, `이거 봤어?`, direct claim)
- others physically attend to the phone
- conversation begins immediately

Do not make the recurring opener feel like a formal MC segment.

`Post Card` / community-card insert is **optional**, not default. Do not create a mandatory overlay/hard-cut production step unless the episode genuinely needs it.

### 12. Clip/duration policy — superseded from fixed 2 x 8

Default now:
> **one compact generated clip of whatever duration the completed performance naturally needs**

Use multiple clips only when:
- the real source has enough beats;
- there is a genuine shot/state change;
- one clip would force rushed dialogue or overloaded physical action.

Video duration must follow the completed natural performance, not the reverse. See `PERFORMANCE_AUDIO_ARCHITECTURE.md`.

### 13. Content/source rules unchanged
- real Korean community posts/comments remain primary
- AI-written spoken beats <= 30% target
- AI-invented comedic payoff approx 0%
- preserve human phrasing/attitude through light oralization
- no neat moralizing outro by default

## P002 real production evidence

### Evidence A — failed restyle/recomposition
A generated output changed drawing style/face proportions from the beginning while vertically recomposing a 16:9 source.

Lesson: preserve 16:9 generation authority and use concise motion-focused prompts.

### Evidence B — viable single-clip test
A later ~10-sec 16:9 Omni test preserved style much better and confirmed that opener + several response beats can work in one compact clip.

Useful positives:
- single-clip structure is viable
- social reaction order was readable
- larger gestures were feasible
- loudness normalization worked

Not publishable because:
- speech sounded mechanical
- preselected duration forced unnatural tempo
- mouth animation was uncanny
- CENTER had a malformed eye-close transition near the beginning

Do not interpret this as a reason to reduce acting amplitude or ban eye expressions. Fix the performance/audio/face-transition architecture instead.

## QC hierarchy — updated

Short malformed transitions can last only a few frames. Representative montage QC is insufficient.

Mandatory order:
1. first 0.5 sec frame-by-frame
2. every blink / wink / eye-close transition
3. speaker handoff windows around ±0.2 sec
4. maximum-mouth-opening frames
5. identity/style at first/middle/end
6. hands/contact/table/prop intersection
7. reaction amplitude and causal clarity
8. audio naturalness / pacing / speaker separation / loudness
9. minor expression-tone differences last

Hard fail includes an uncanny eye/face morph even if it lasts only a fraction of a second.

## Current execution order — NEXT SESSION

1. Read `CURRENT_STATE.md`.
2. Read `PERFORMANCE_AUDIO_ARCHITECTURE.md`.
3. Read active P002 source/package.
4. Finalize P002 `PERFORMANCE MASTER` with compact source-driven dialogue + **1–2 larger physical beats**.
5. Generate the whole multi-speaker dialogue once in two strong Korean dialogue engines (initial A/B: ElevenLabs v3 Dialogue vs Typecast / best accessible equivalent).
6. Choose one natural `P002_DIALOGUE_MASTER.wav`.
7. Measure actual duration and extract/derive turn timestamps automatically.
8. Derive video duration from the natural performance.
9. Make exactly one new 16:9 Omni generation using the dialogue master as timing authority, concise visual lock, larger physical acting, clean eye transitions and limited 2D mouth animation.
10. Run frame-level QC.
11. If pass: final 9:16 edit / subtitles / thumbnail / publish.

Do not return to pilot-for-pilot testing or fixed 2 x 8 sec by default.

## Repository integrity note

Older prose claimed some canonical binaries existed under `assets/v2_locked/`, but those paths were not verified on inspected `main`. Do not claim image binaries are GitHub-preserved unless actually verified.
