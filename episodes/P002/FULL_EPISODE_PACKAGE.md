# P002 — FIRST FULL EPISODE PACKAGE

Updated: 2026-09-04 KST  
Status: **REAL GENERATION EVIDENCE EXISTS / PERFORMANCE-FIRST RETRY NEXT**

## Goal

Build the first actual publishable short while locking the repeatable production architecture. Do not return to isolated pilot-for-pilot tests.

## Source / editorial authority

Source provenance remains in `SOURCE_PACK.md`.

Core source logic:
- entry-level hiring is being squeezed
- experienced applicants can be hired at entry-level pay
- `ladder removed / middle tier becomes bottom tier` framing

Keep real human-comment flavor. No AI-invented punchline or neat moral lesson.

## Visual authority

Use the user-supplied 2026-09-04 convenience-store-front three-person image / derived opening still as the active P002 visual authority.

It controls:
- character identity
- face / eye / hair design
- current outfits
- table / chairs / props
- convenience-store setting
- drawing style
- LEFT / CENTER / RIGHT geometry

If stale repo prose conflicts with the image, the active image wins.

## Opening grammar

CENTER brings the topic in through the phone.

Natural opener:
- `야 이거 봐`
- `이거 봤어?`
- or direct claim if stronger

The others physically attend to the phone, then conversation immediately starts.

Do NOT default to a formal MC line such as `오늘의 주제!`.

`Post Card` is optional only. It is not required as a hard cut, overlay, or third clip.

## Current clip architecture — supersedes 2 x 8 sec

The original `2 x 8 sec` plan is historical only.

A real 16:9 ~10-sec Omni generation showed that one compact clip can carry opener + several source-derived reactions.

Current default:
> **one compact clip of whatever duration the natural completed performance needs**

Use multiple clips only if the source or physical staging genuinely requires them.

## P002 latest compact dialogue candidate

The first single-clip test used a compressed version approximately like:

CENTER:
`야 이거 봐. 요즘 신입 안 뽑아서 공무원으로 몰린대.`

RIGHT:
`진짜 신입이 뒤져감.`

LEFT:
`회사야 좋지. 신입 연봉으로 경력자 뽑잖아.`

CENTER:
`사다리 치운 거네.`

This is a **performance draft**, not a sacred final transcript. Before the next generation, re-check oral naturalness against `SOURCE_PACK.md` and keep the human-origin logic intact.

## Real-generation evidence

### Attempt A — reject
A generated output vertically recomposed the source and changed faces/linework/style from the beginning.

Lesson:
- generation master must remain 16:9
- do not ask Omni to redesign the cast into 9:16
- final Shorts crop happens later
- avoid long visual re-description prompts that can encourage reinterpretation

### Attempt B — useful but not publishable
A later 16:9 single ~10-sec Omni generation with a concise visual lock preserved style much better.

Positive evidence:
- source drawing style largely survived
- single-clip structure works
- social reaction ordering was readable
- somewhat larger gestures were feasible
- three 4-sec reference audios fit the observed Seedance 2.0 Mini reference ceiling
- Taemin loudness normalization (~+10 dB relative source preview) produced much better speaker balance

Hard defects:
1. generated Korean voice sounded synthetic/mechanical
2. preselected video duration forced unnatural speech pacing
3. mouth animation tried to follow Korean phonemes too literally and looked uncanny
4. CENTER had a malformed eye-closing transition near the opening: ambiguous asymmetric half-closed frames rather than a clean blink/expression

This clip is evidence, not final master.

## Performance-first redesign for P002

Before any new video generation, create a `PERFORMANCE MASTER`.

It must define for each beat:
- exact dialogue
- speaker and emotional intent
- action that can happen while speaking
- nonverbal action that requires a pause/gap
- delayed reaction order

### Physical acting target

The next version should be more physically alive than the last test.

Use about **1–2 larger motivated physical beats** in addition to face/head reactions.

Possible P002 beats:
- CENTER clearly extends the phone toward the other two while opening
- RIGHT recoils / leans back more visibly on the grim reaction
- LEFT gives RIGHT one quick playful open-hand tap on the upper arm before/around her response
- LEFT extends one arm clearly while making the employer-logic point
- CENTER changes posture / looks from LEFT to RIGHT on the final realization

Do not include all of these merely for completeness. Choose the 1–2 strongest beats that fit the final dialogue rhythm.

For contact, specify exact target and brief duration. Do not use vague `hit` language.

## Eye / face animation target

Do not ban natural eye acting.

Allowed:
- blink
- wink
- eye-smile
- wide-eye reaction
- eyes squeezed shut briefly for laughter/frustration

Required:
- each eye expression reads cleanly and intentionally
- no melted/misaligned/asymmetric accidental half-closed morph
- original eye design restores after the expression

The opening 0.5 sec must be inspected frame-by-frame after generation.

## Mouth animation target

Do not request phoneme-perfect Korean lip sync.

Use limited stylized 2D mouth flap:
- closed
- slightly open
- small relaxed open

Correct active-speaker timing matters more than exact vowel/consonant shapes.

No wide stretched mouth, large jaw movement, realistic lip pursing, or face reshaping around speech.

## Audio architecture — active next step

Do not use fixed video duration as the timing authority.

Do not create four separate TTS lines and manually sync them one by one.

Instead:
1. finalize P002 PERFORMANCE MASTER;
2. generate the **whole three-speaker scene once** in a multi-speaker dialogue engine;
3. initial A/B candidates: ElevenLabs v3 Dialogue vs Typecast / strongest accessible Korean dialogue system;
4. choose one natural whole-scene `P002_DIALOGUE_MASTER.wav`;
5. measure actual duration;
6. extract/derive speaker-turn and silence timestamps automatically;
7. derive video duration from the natural performance;
8. feed that same dialogue master to Omni as the timing/performance reference;
9. generated/native Seedance audio is disposable; final edit reuses the original dialogue master at time 0.

Target is turn-level sync + plausible 2D mouth motion, not sample-perfect phoneme sync.

Full architecture: `../../PERFORMANCE_AUDIO_ARCHITECTURE.md`.

## Duration rule

For Seedance 2.0 Mini / fixed-duration UI:

> `VIDEO_DURATION ≈ ceil(DIALOGUE_MASTER_DURATION + 0.4–0.7 sec reaction tail)`

Use the nearest actually supported duration.

Do not accelerate/slow the final dialogue merely to hit a preselected length.

If a verified smart-duration route is accessible in the actual environment, it may be tested, but do not assume UI availability without checking.

## Visual prompt rule

Keep visual description compact.

```text
Use IMAGE 1 as the strict visual authority.
Animate the existing illustration only.
Do not redraw, redesign, restyle, beautify, modernize, or reinterpret it.
Preserve the original faces, eye designs, hairstyles, linework, proportions, colors, clothing, objects, background, and 16:9 composition.
```

Then spend prompt budget on actions, timing, reaction order and face-transition quality.

## Resolution

The viable test was low-resolution (~480p class). A 2x upscale improved display sharpness but cannot fix malformed animation.

For the next production retry, use a higher generation resolution than 480p if the active TopView/model route offers a reasonable quality/cost tradeoff.

## QC — mandatory after next generation

1. first 0.5 sec frame-by-frame
2. every blink/wink/eye-close transition
3. speaker handoff windows ±0.2 sec
4. maximum-mouth-opening frames
5. identity/style first/middle/end
6. hands / brief contact / table / prop intersections
7. reaction amplitude and social causality
8. voice naturalness / pacing / separation / loudness
9. minor ending-expression tone only after the above

Hard fail:
- uncanny eye/face morph even if only several frames
- wrong speaker mouth movement
- style redesign
- severe hand/body intersection
- obviously tempo-forced or synthetic dialogue

## Next session execution

1. Read `CURRENT_STATE.md` and `PERFORMANCE_AUDIO_ARCHITECTURE.md`.
2. Finalize the P002 PERFORMANCE MASTER and dialogue wording.
3. Choose 1–2 larger physical beats.
4. Generate whole-scene audio A/B in two dialogue engines.
5. Lock one `P002_DIALOGUE_MASTER.wav`.
6. Measure duration / derive turn timestamps / choose video duration.
7. Make exactly **one** new 16:9 Omni generation with the dialogue master as timing authority.
8. Frame-level QC.
9. If pass: final 9:16 edit, subtitles/localization, thumbnail, publish.

Do not generate another clip before the performance/audio architecture is ready.