# P001 — SCENE A LOCK

Updated: 2026-09-03 KST  
Status: **PRODUCTION PASS / DO NOT REGENERATE**

## Output

- File: `260903_0001_video_edit_2387.mp4`
- Actual duration: 7.104 sec
- Frame: 864×496, 24fps
- Input stack:
  - locked 3-person cast master still
  - white-T-shirt woman master pack
  - CHAR_06 master pack
  - gray-hoodie male master pack
  - exact prompt below
- Model baseline: Seedance 2.0 Mini / 480p / 16:9 target / no subtitles

## Narrative function

- CENTER introduces the “373 years → 44 minutes” claim.
- LEFT dismisses it.
- RIGHT acts as the comment-section social reaction without dialogue.
- Scene B supplies the reversal and final sting.

## Exact prompt used

```text
Use the provided locked three-character master still as the exact first frame.

Preserve the exact character identities, clothing, facial designs, body proportions, room, table, drawing style, and LEFT/CENTER/RIGHT positions throughout the entire clip.

Fixed frontal camera.
No camera movement, zoom, scene change, or character redesign.
No glasses on any character.
Do not swap positions.

This is one continuous casual Korean conversation between three friends.

DIALOGUE:

CENTER woman with long wavy dark hair and a beige top:
“373년 동안 못 풀던 암호를 AI가 44분 만에 풀었대.”

LEFT woman with light-brown bob hair and a fitted white T-shirt:
“근데 이거 좆도 쓸모없는 거구만.”

PERFORMANCE AND INTERACTION:

CENTER begins calmly, as if casually sharing a strange news story.

While CENTER is speaking, LEFT listens but gradually develops a skeptical, unimpressed expression. She briefly glances at RIGHT and then back toward CENTER.

RIGHT remains silent. He first listens neutrally, then notices LEFT’s increasingly unimpressed expression and begins suppressing a smile.

Immediately after CENTER finishes, LEFT delivers her line with casual dismissive certainty. She does not shout and does not make a large gesture.

As LEFT says “좆도 쓸모없는 거구만,” RIGHT lets out one short involuntary snort of laughter and makes a small shoulder movement. He does not speak.

CENTER pauses, turns her eyes and head slightly toward LEFT, and gives her a quiet “seriously?” look.

The reactions must be staggered and socially connected:
LEFT reacts first, RIGHT reacts slightly later, and CENTER reacts last.
Do not make all three characters move, blink, smile, or turn at the same time.

Keep the acting lively enough to feel like a real conversation, but physically restrained:
small eye movements, slight head turns, one brief suppressed laugh, and different resting postures.

Use restrained natural Korean lip movement.
Avoid overly wide mouth shapes.
Keep eye shapes clean and stable during blinking and smiling.
RIGHT must not squeeze his eyes tightly shut while laughing.
No face warping, oversized mouth, exaggerated gestures, or large body movement.

Only CENTER and LEFT speak.
RIGHT’s mouth must not lip-sync dialogue.

No subtitles.
No captions.
No text.
No logos.
No music.
No new objects.
```

## QC

### PASS

- Identity, clothes, seating, room, and table remain stable.
- CENTER and LEFT are the correct speakers.
- RIGHT does not steal the dialogue.
- LEFT’s skepticism, RIGHT’s smile, and CENTER’s later look create a readable social chain.
- No production-blocking eye, mouth, hand, or body deformation.
- Physical grounding remains usable.

### Residual issue

RIGHT begins preparing the smile before LEFT actually delivers the trigger phrase. This reads slightly like an actor who knows the script.

Do not regenerate Scene A. Correct from Scene B onward with:

```text
Do not anticipate the joke.
Keep the listener completely neutral until the trigger phrase is actually spoken.
Begin the reaction only after hearing the trigger phrase.
Reactions must be staggered and causally timed, never simultaneous.
```

## Edit note

The prompt described a 10-second trial, but prompt prose does not control TopView duration. The exported clip is 7.104 seconds. Set the duration in the TopView UI for future clips. Scene A remains usable at its actual length.

## Final-audio status — voice lock

The picture remains `PRODUCTION PASS / DO NOT REGENERATE`.

The Seedance-generated CENTER and LEFT voices are **performance guides, not final recurring character voices**. Before P001 publication:
- split CENTER and LEFT speech segments,
- convert each to the character's fixed multilingual voice ID while preserving timing/delivery,
- replace audio without changing the locked picture,
- re-check lip timing, BLEEP placement and loudness.

This is an audio post-process, not a Scene A regeneration.
