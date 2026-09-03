# TALKSHOW — PERFORMANCE / AUDIO / ANIMATION ARCHITECTURE

Updated: 2026-09-04 KST  
Status: **ACTIVE — supersedes the earlier voice-reference-first / fixed-duration assumption**

This document records the production architecture learned from the first real P002 generations. It exists to prevent later sessions from returning to fixed-duration-first dialogue, line-by-line audio repair, tiny reactions, phoneme-perfect mouth animation, or blanket bans on natural eye acting.

## 1. Core conclusion

The production order is **PERFORMANCE FIRST**, not video-duration first and not audio-only first.

> **real community source → PERFORMANCE MASTER (speech + nonverbal actions + reaction gaps) → whole-scene dialogue audio → automatic timing extraction → video duration derived from actual performance → Omni generation using the same dialogue master as timing authority → final edit uses that original dialogue master audio**

The scene's natural spoken rhythm and motivated nonverbal beats determine the required video length. Do not decide `10 sec` first and force all dialogue to fit it.

## 2. PERFORMANCE MASTER is the single source of timing truth

Before voice or video generation, write one compact performance score containing:
- exact spoken line
- speaker
- emotion / delivery intent
- action that can happen **while speaking**
- nonverbal action that requires a **pause between lines**
- reaction order / social causality

Example structure:

```text
BEAT A
CENTER: "야 이거 봐..."
WHILE SPEAKING: extends the phone toward the group.
LEFT notices first; RIGHT follows.

BEAT B
RIGHT: short dry reaction.
WHILE SPEAKING: leans/recoils slightly.

BEAT C
NONVERBAL GAP: LEFT gives RIGHT one quick playful tap on the upper arm.
LEFT then speaks, using a larger forward hand gesture.

BEAT D
CENTER final realization.
END REACTION: delayed silent group recognition.
```

The audio and video prompts are both derived from this same PERFORMANCE MASTER. Do not invent separate independent timing plans for audio and video.

## 3. Audio architecture — whole scene once, not line-by-line

### Problem found in P002
The TopView/Seedance voice-reference route produced recognizable timbre but the speech itself was too mechanical. Because the video duration was preselected, some lines were unnaturally accelerated or stretched to satisfy the requested duration.

Line-by-line TTS plus manual placement is also rejected as the default workflow because it creates too much editing labor and reintroduces synchronization work.

### New direction
Generate the **entire multi-speaker scene as one dialogue master** in one dialogue-capable voice system.

Candidates for the next A/B:
- ElevenLabs v3 Dialogue
- Typecast multi-speaker / contextual Korean dialogue

Selection criterion is not prettiest isolated voice. Prioritize:
1. natural Korean conversational prosody
2. believable turn-taking and pauses
3. character separation
4. emotional range / laughter / breath without actor-like overperformance
5. repeated-listening durability
6. ability to reproduce the same recurring character voices across episodes

The existing TopView voices remain useful as historical/interim references:
- LEFT: Gaeun outdoors
- CENTER: Harin
- RIGHT: Taemin

But they are **not yet final recurring production voices** because the first real generation sounded too synthetic.

## 4. Audio should include nonverbal timing indirectly

A nonverbal action can be either:

### Concurrent action — no extra audio gap required
Examples:
- showing the phone while speaking
- extending one arm while explaining
- leaning back while delivering a line

Describe these as `WHILE SPEAKING` in the video prompt. The dialogue audio does not need extra silence.

### Exclusive nonverbal beat — requires temporal space
Examples:
- playful arm tap before the next line
- laugh / breath / sigh before continuing
- mutual look before someone answers
- recoil followed by a response

The PERFORMANCE MASTER must reserve a short dialogue gap or natural breath for these. The whole-scene dialogue generator should therefore create the pause as part of the scene performance rather than relying on later manual insertion.

## 5. One final dialogue master; no manual segment-by-segment sync

Create one file such as:

`P002_DIALOGUE_MASTER.wav`

It already contains all speaker turns and natural gaps in the intended order.

Then automatically extract speaker-turn / silence timestamps with alignment or speech analysis. Example derived timing:

```text
0.00–2.85 CENTER line + phone extension
2.85–3.10 short reaction gap
3.10–4.20 RIGHT line + recoil
4.20–4.55 nonverbal gap / LEFT arm tap
4.55–7.20 LEFT line + forward gesture
7.35–8.35 CENTER final line
8.35–8.90 silent reaction hold
```

These timestamps are generated from the completed master audio / performance score; the user should not hand-place every sentence.

## 6. Video duration is derived, not imposed

### Seedance 2.0 Mini / fixed-duration UI route
If the final dialogue master has duration `A`, choose video duration from the nearest supported value that leaves a small reaction tail.

Baseline calculation:

> `VIDEO_DURATION ≈ ceil(A + 0.4–0.7 sec)`

Examples:
- dialogue master 7.1 sec → video around 8 sec
- dialogue master 8.3 sec → video around 9 sec
- dialogue master 9.4 sec → video around 10 sec

Do not stretch/compress the dialogue merely to fill the chosen video duration.

### Smart-duration route
Seedance 2.5 smart-duration / automatic-duration capability is a candidate production route where actually accessible in the active TopView/API workflow. Do not assume a UI control exists without verifying it in the current execution environment.

## 7. Omni synchronization strategy

Feed the **same whole-scene dialogue master** into Omni as the scene's timing/performance reference.

Prompt principle:

```text
The supplied dialogue master is the timing and performance authority.
Preserve its natural speaking speed, turn order, pauses, and rhythm.
Match character speaking turns and motivated body reactions to that timeline.
Do not stretch or compress speech to fill the video duration.
```

The generated/native Seedance audio is not a second final audio production pass. It is disposable guide/output audio.

For the publishable master:
- mute/discard generated dialogue audio if needed;
- place the original `Pxxx_DIALOGUE_MASTER.wav` at time 0;
- because that same file drove the generation timing, only global alignment should be required, not hand-syncing every line.

This architecture must still be validated in one real generation. The success criterion is **turn-level sync**, not sample-perfect phoneme sync.

## 8. Mouth animation — stylized plausibility over phoneme perfection

The first P002 real generation showed that realistic Korean phoneme-shaped lip sync looks uncanny on the simple low-fi webcomic faces.

New rule:
- prioritize believable 2D mouth-flap rhythm
- speaker-turn timing should be correct
- phoneme-perfect mouth shapes are NOT required
- use a limited small set of mouth states

Reusable prompt block:

```text
MOUTH ANIMATION:
Use limited stylized 2D mouth animation, not realistic phoneme-perfect lip sync.
Keep mouth movement small and consistent with the original drawing style.
Use only a few simple states such as closed, slightly open, and small relaxed open.
Match the rhythm and active speaker plausibly, but do not form exaggerated Korean vowel/consonant mouth shapes.
No wide stretched mouth, large jaw movement, realistic lip pursing, or facial reshaping around the mouth.
```

## 9. Eye animation — natural expression is allowed; malformed transitions are not

Do **not** ban blinking, winking, eye-smiles, squeezed-eye laughter, or other motivated eye expression. Those are important emotional tools.

The failure to prevent is an ambiguous morph state where the eye is neither cleanly open nor intentionally closed.

Reusable prompt block:

```text
EYE / FACE TRANSITION QUALITY:
Natural blinking, winking, eye-smiles, wide-eyed surprise, and motivated eye closure are allowed and encouraged when emotionally appropriate.
Every eye action must resolve as one clean intentional expression.
A blink should read as open → clean closure → open.
A wink should read as one deliberate closed eye with the other eye stable.
An eye-smile should close both eyes naturally and symmetrically when appropriate.
Never create melted, misaligned, asymmetrically half-closed, or ambiguous in-between eye shapes.
Preserve the original eye design before and after the expression.
```

## 10. Reaction / physical acting amplitude — increase it further

V2 must not collapse back into tiny head turns and polite palm-up gestures.

Friends should have larger socially motivated reactions when the beat supports them.

Allowed / desired examples:
- clear torso recoil / lean-in
- phone extended toward the other two
- arm stretched out while making a point
- two-hand disbelief
- body turning toward another character
- repositioning / fidgeting / shifting seated posture
- brief table tap when geometry is safe
- hand to forehead / covering face
- bending forward while laughing
- visibly irritated body language
- quick celebratory motion
- one friend giving another a **brief playful tap on the upper arm / shoulder**

Contact actions are allowed. Specify them precisely to reduce geometry errors, e.g.:

```text
LEFT gives RIGHT one quick playful open-hand tap on his upper arm, then immediately returns her hand.
```

Do not use vague `hits him` instructions.

Baseline for a ~8–12 sec short:
- approximately 1–2 larger physical beats
- plus eye / face / head / torso social reactions
- keep causality staggered instead of everybody moving simultaneously

Avoid only genuinely unstable behavior:
- prolonged complex body contact
- hands crossing faces for long periods
- full-body flailing with no story reason
- anatomy warping / object intersection

## 11. Visual fidelity lesson from P002 generation

One failed generation reinterpreted the drawing style and composition from the first frame. The failed output was vertically recomposed even though the source still was 16:9.

A later 16:9 Omni generation using a shorter visual-lock prompt preserved the style materially better.

Current lesson:
- **generation master stays 16:9**
- final 9:16 distribution crop happens later
- do not ask Omni to vertically redesign the 16:9 cast still
- use the active image as visual authority
- do not redundantly re-describe every face/clothing/style detail in prose; that can encourage reinterpretation
- video prompt should describe **motion/performance**, with one compact visual-lock block

Compact lock:

```text
Use IMAGE 1 as the strict visual authority.
Animate the existing illustration only.
Do not redraw, redesign, restyle, beautify, modernize, or reinterpret it.
Preserve the original faces, eye designs, hairstyles, linework, proportions, colors, clothing, objects, background, and 16:9 composition.
```

## 12. Resolution / upscale lesson

The first viable P002 test was low-resolution (~480p class). A 2x post upscale can improve display sharpness but cannot restore missing detail or fix malformed eyes/mouths.

Therefore:
- upscale is acceptable for preview/recovery
- facial-animation defects must be solved at generation, not by upscale
- use a higher generation resolution for final production when the quality/cost tradeoff is acceptable

## 13. P002 real-generation evidence

The first viable single-clip P002 attempt established several useful facts:
- `16:9 + concise visual lock` preserved the low-fi drawing style far better than the earlier failed vertical recomposition
- a single short clip can carry opener + several comment beats, so **single-clip first** is preferable when the source permits it
- voice-reference loudness can be normalized; Taemin was materially quieter and was raised roughly +10 dB to match the other two
- larger social reactions are feasible without automatically destroying geometry

But that attempt is **not publishable final** because:
- speech sounded synthetic/mechanical
- fixed requested duration distorted natural speech pacing
- mouth animation was uncanny because it tried to track phonemes too literally
- CENTER had a malformed eye-closing transition near the beginning

These are production-architecture defects, not reasons to return to tiny reactions or ban expressive eye acting.

## 14. QC hierarchy — updated after missed eye artifact

A representative-frame montage is not enough. Short uncanny transitions can last only a few frames.

Mandatory QC order:
1. **first 0.5 sec frame-by-frame** — opening defects are high severity
2. every blink / wink / eye-closure transition frame-by-frame
3. speaker handoff windows approximately ±0.2 sec — wrong mouth / wrong speaker movement
4. maximum-mouth-opening frames — mouth/jaw/face deformation
5. identity/style at first / middle / end
6. hands / contact actions / table and prop intersection
7. reaction amplitude and causal readability
8. audio naturalness / pacing / speaker separation / loudness
9. minor expression-tone differences only after the above

Hard FAIL examples:
- malformed eye transition / uncanny face artifact
- wrong speaker lip movement
- style or identity redesign
- severe hand/body/object intersection
- obviously synthetic or tempo-forced dialogue that damages the scene

Minor issues such as two characters blinking near the same moment or an ending expression being slightly brighter than intended are not regeneration reasons by themselves.

## 15. Default short-form assembly going forward

Prefer:

> **one compact generated clip of whatever duration the completed performance actually needs**

rather than automatically splitting every episode into 2 x 8 sec.

Use multiple clips only when the source has enough real material or a genuine shot/state change requires it.

Recurring opening grammar remains:
- one friend has found something on the phone
- natural opener such as `야 이거 봐` / `이거 봤어?` / direct claim
- friends physically attend to the phone
- conversation immediately follows

A Post Card / community-card insert is **optional, not default**. Do not add a separate graphic production step unless it materially improves comprehension or hook strength.

## 16. Immediate next experiment

Do NOT spend another generation merely changing tiny animation details.

Next session should:
1. take P002's current compact source-driven dialogue and write the final PERFORMANCE MASTER with 1–2 larger physical beats;
2. A/B the full scene in **ElevenLabs v3 Dialogue vs Typecast** (or the strongest accessible Korean dialogue engine at execution time), generated as one multi-speaker conversation;
3. choose the more natural recurring voice set / engine;
4. produce one `P002_DIALOGUE_MASTER.wav`;
5. measure its actual duration and automatically derive the video duration with a short reaction tail;
6. extract/derive speaker-turn timestamps;
7. generate **one** new 16:9 Omni clip using the dialogue master as timing authority, compact visual lock, larger physical reactions, clean eye transitions, and limited 2D mouth animation;
8. QC using the frame-level hierarchy above;
9. only after this passes, create the final 9:16 edit / subtitles / thumbnail and publish.

Do not return to pilot-for-pilot testing beyond this architecture-validation generation.