# P001 PRODUCTION PACKAGE — `쓸모없는 암호`

Status: **READY FOR MANUAL TOPVIEW GENERATION**  
Target: 16:9 / 480p generation / approximately 34–39 sec final / 3 characters  
Model: Seedance 2.0 Mini  
Visual authority: the already locked canonical 3-person master first frame. Do not recreate the set.

## 1. Cast and fixed screen positions

The names below are production labels for this episode; roles are not permanent.

| Position | Visual identity | Episode function |
|---|---|---|
| LEFT | white fitted T-shirt woman, light-brown bob, no glasses | dismisses the achievement, then tries to recover |
| CENTER | CHAR_06, long wavy dark hair with bangs, beige top, no glasses | setup and literal reversal |
| RIGHT | gray-hoodie male, messy short black hair, no glasses | comment-section laugh/reaction |

Never swap positions. Reuse the exact same master first frame for every clip.

## 2. Locked dialogue

### Internal master

1. CENTER: `373년 동안 못 풀던 암호를 AI가 44분 만에 풀었다는 주장이 나왔대.`
2. LEFT: `좆도 쓸모없는 거구만.`
3. CENTER: `사람들이 저기에 시간을 안 들이게 됐으니까 엄청 쓸모있는 거 아님?`
4. RIGHT: `병신 ㅋㅋ`
5. LEFT: `아니 씨발 그 뜻이 아니라—`
6. RIGHT: `천재노ㅋㅋㅋ`

### Public audio/censor master

1. CENTER: unchanged
2. LEFT: `좆-[BLEEP] 쓸모없는 거구만.`
3. CENTER: unchanged
4. RIGHT: `병-[BLEEP] ㅋㅋ`
5. LEFT: `아니 씨-[BLEEP] 그 뜻이 아니라—`
6. RIGHT: unchanged

Generate the I2V clips with the internal master wording so mouth movement remains natural. Apply BLEEP and audio dips only in the final edit.

## 3. Runtime and edit plan

| Shot | Final time | Source clip | Edit framing | Dialogue / event |
|---|---:|---:|---|---|
| H01 | 0.0–2.2 | user-made hook card | full frame | old cipher texture, `373년 → 44분?` |
| S01 | 2.2–9.0 | 7 sec | master → 112% center crop | CENTER setup |
| S02 | 9.0–14.5 | 6 sec | 118% left crop | LEFT dismissal; BLEEP lands before the noun |
| S03 | 14.5–22.5 | 8 sec | 112% center crop | CENTER literal reversal; tiny pause before `엄청` |
| S04 | 22.5–27.5 | 5 sec | 122% right crop | RIGHT `병-[BLEEP] ㅋㅋ`; LEFT begins to bristle silently |
| S05 | 27.5–33.5 | 6 sec | 118% left crop | LEFT failed recovery, cut off at dash |
| S06 | 33.5–38.5 | 5 sec | 125% right crop | RIGHT `천재노ㅋㅋㅋ`; hard cut on laugh peak |

Expected final duration: **about 38.5 sec**. Do not add an outro, lesson, or explanatory tag.

## 4. Exact TopView prompts

Global generation settings for all six clips:
- Seedance 2.0 Mini
- 480p
- 16:9
- first frame: the exact same locked 3-person master still
- one generation per shot
- no subtitles, captions, text, logos, or music generated into the clip

### S01 — setup — 7 sec

```text
Use the provided image as the exact first frame. Fixed frontal three-person master shot; keep the same room, table, identities, clothing, proportions, and exact LEFT/CENTER/RIGHT positions for the entire clip. Do not add glasses and do not swap anyone.

Only the CENTER woman with long wavy dark hair and a beige top speaks in natural Korean, calmly as if sharing a strange news item:
"373년 동안 못 풀던 암호를 AI가 44분 만에 풀었다는 주장이 나왔대."

The LEFT woman and RIGHT man stay silent and listen with tiny eye and head turns. Subtle conversational motion, natural blinking, restrained mouth movement, no broad gestures. Keep the camera completely fixed. No subtitles, text, logos, or new objects.
```

### S02 — dismissal — 6 sec

```text
Use the same provided master image as the exact first frame. Keep the fixed frontal three-person composition, exact identities, clothing, set, and LEFT/CENTER/RIGHT positions. No glasses, no position swap, no camera movement.

Only the LEFT woman in the white fitted T-shirt speaks in natural Korean with casual dismissive disbelief:
"좆도 쓸모없는 거구만."

After speaking, she gives a tiny unimpressed exhale. The CENTER woman stays silent and turns her eyes slightly toward LEFT. The RIGHT man stays silent with the beginning of a suppressed smile. Motion is subtle and socially connected, never frozen and never exaggerated. No subtitles, text, logos, or new objects.
```

### S03 — reversal — 8 sec

```text
Use the same provided master image as the exact first frame. Fixed frontal three-person master shot. Preserve every character, the room, table, clothing, proportions, and exact LEFT/CENTER/RIGHT placement. No glasses, no swapping, no camera motion.

Only the CENTER woman with long wavy dark hair and a beige top speaks in natural Korean, matter-of-fact and completely sincere rather than performing a joke:
"사람들이 저기에 시간을 안 들이게 됐으니까, 엄청 쓸모있는 거 아님?"

She makes only one small open-hand gesture near the end. The LEFT woman remains silent and slowly turns to stare at CENTER. The RIGHT man stays silent, registers the logic, and starts trying not to laugh. Natural subtle blinking and tiny head motion. No subtitles, text, logos, or new objects.
```

### S04 — first reaction — 5 sec

```text
Use the same provided master image as the exact first frame. Keep the exact fixed three-person composition and positions; do not change identity, clothing, room, table, or framing. No glasses and no character swap.

Only the RIGHT man in the gray hoodie speaks in natural Korean, dry at first and then breaking into a short laugh:
"병신, ㅋㅋ."

The LEFT woman stays silent, stiffens slightly, and looks offended. The CENTER woman stays silent with a small confused smile. RIGHT's laugh is brief and controlled; avoid huge mouth deformation or tightly squeezed eyes. Fixed camera. No subtitles, text, logos, or new objects.
```

### S05 — failed recovery — 6 sec

```text
Use the same provided master image as the exact first frame. Fixed frontal three-person composition. Preserve all identities, clothes, set geometry, proportions, and exact LEFT/CENTER/RIGHT positions. No glasses, no swapping, no camera movement.

Only the LEFT woman in the white fitted T-shirt speaks in natural Korean, flustered and trying to interrupt:
"아니 씨발, 그 뜻이 아니라—"

She leans forward only slightly and stops mid-thought. The CENTER woman silently watches her. The RIGHT man silently tries not to laugh, with a small shoulder movement only. No exaggerated gestures, no subtitles, text, logos, or new objects.
```

### S06 — final sting — 5 sec

```text
Use the same provided master image as the exact first frame. Keep the fixed room, table, identities, clothing, proportions, and exact LEFT/CENTER/RIGHT positions. No glasses, no swaps, no camera motion.

Only the RIGHT man in the gray hoodie speaks in natural Korean with amused admiration and then gives one short laugh:
"천재노, ㅋㅋㅋ."

The LEFT woman stays silent and gives him a flat annoyed stare. The CENTER woman stays silent, looks between them, and lets out a very small smile. Keep RIGHT's blink and smile anatomically stable: no hard eye squeeze, no face warping, no oversized mouth. End on the laugh peak. No subtitles, text, logos, or new objects.
```

## 5. Generation order and stop rule

Generate in edit order: `S01 → S02 → S03 → S04 → S05 → S06`.

For each shot, generate exactly once and then inspect only these production defects:
- wrong speaker / another character's mouth speaking
- identity or seat swap
- glasses appearing
- visible detachment from floor/table/set
- severe eye, mouth, hand, or face deformation
- unusably fast or truncated Korean dialogue

Do not reject for harmless micro-motion or minor style variation. If a shot fails, regenerate only that shot with one corrected control line; do not return to set or character tests.

## 6. Edit instructions

- In CapCut, make H01 yourself as a 2.2-second still: muted beige paper background, faint old cipher-like characters, large centered text `373년 → 44분?`. Do not use a screenshot of the original post.
- Use straight cuts. No cross-dissolves.
- All punch-ins are post-production crops from the master shot; do not generate singles.
- BLEEP length: approximately 180–240 ms, placed after the first syllable.
- Duck original speech under each BLEEP by 12–18 dB rather than muting the entire line.
- Optional micro-SFX: one soft click on H01 and one very short dry pop on the S06 hard cut. Nothing else.
- Final audio should feel like room conversation, not a TV variety show.
- No end card. Hard cut to black immediately after the final laugh peak.

## 7. Pass condition for P001 picture lock

PASS when all six clips are usable in sequence, speaker identity is unambiguous, no character/set continuity failure distracts from the lines, and the final cut lands between 30 and 60 seconds. Minor blink or lip imperfections may remain if they do not interrupt comprehension.
