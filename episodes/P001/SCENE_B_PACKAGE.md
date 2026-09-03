# P001 — SCENE B GENERATION PACKAGE

Updated: 2026-09-03 KST  
Status: **READY FOR ONE MANUAL TOPVIEW GENERATION**

## Purpose

Finish P001 with the human-origin reversal and social punch. This is production, not a set or character test.

Target:
- UI duration: **10 sec**
- Seedance 2.0 Mini
- 480p
- 16:9
- audio/dialogue enabled
- no subtitles

## Upload stack

Use the exact same four inputs that produced Scene A:

1. locked 3-person cast-master still — exact first frame
2. white-T-shirt woman master pack
3. CHAR_06 master pack
4. gray-hoodie male master pack

Do not replace, regenerate or reorder the cast. Do not add a set reference.

## Exact copy-paste prompt

```text
Use the provided locked three-character master still as the exact first frame.

Preserve the exact character identities, clothing, facial designs, body proportions, room, table, low-fi drawing style, and LEFT/CENTER/RIGHT positions throughout the entire clip.

Fixed frontal camera.
No camera movement, zoom, scene change, or character redesign.
No glasses on any character.
Do not swap positions.

This is one continuous casual Korean conversation between three friends.

DIALOGUE:

CENTER woman with long wavy dark hair and a beige top:
“사람들이 저기에 시간 안 들이게 됐으니까, 엄청 쓸모있는 거 아님?”

RIGHT man in the gray hoodie:
“병신, ㅋㅋ.”

After one short beat, the same RIGHT man:
“천재노, ㅋㅋㅋ.”

Only CENTER and RIGHT speak.
LEFT remains completely silent.
Do not give any dialogue or lip-sync to LEFT.

PERFORMANCE AND INTERACTION:

CENTER delivers her line calmly and sincerely, as if stating an obvious practical conclusion. She is not performing a joke and does not look smug.

Until CENTER has fully finished the phrase “엄청 쓸모있는 거 아님?”, both LEFT and RIGHT must remain neutral. They listen without smiling, laughing, reacting, or anticipating the punchline.

Only after CENTER finishes:
- LEFT processes the logic first with one small delayed eye movement toward CENTER.
- About 0.2 seconds later, RIGHT gives LEFT one brief sideways glance and says “병신, ㅋㅋ” dryly, with only a tiny restrained laugh.
- LEFT then turns her eyes toward RIGHT and holds a flat, offended stare. She stays silent.
- After one short pause, RIGHT looks back toward CENTER and says “천재노, ㅋㅋㅋ” with amused admiration and one short controlled laugh.
- CENTER reacts last with a very small delayed puzzled smile.

The reactions must be causally ordered:
CENTER finishes → LEFT registers the logic → RIGHT addresses LEFT → LEFT stares → RIGHT praises CENTER → CENTER reacts.

Do not make two or three characters turn, blink, smile, or laugh at the same time.
Do not anticipate either joke.
No hand gestures.
Keep shoulders, torsos, table, and seated positions stable.
Use only small eye movements, slight head turns, and restrained mouth motion.

Use natural Korean speech and lip movement.
Avoid overly wide mouth shapes.
Keep eye shapes clean and stable during blinking and smiling.
RIGHT must not squeeze his eyes tightly shut while laughing.
No face warping, oversized mouth, exaggerated body motion, or neck deformation.

No subtitles.
No captions.
No on-screen text.
No logos.
No music.
No new objects.
```

## One-generation rule

Generate exactly once.

PASS unless one of these occurs:
- wrong speaker or LEFT speaks
- identity/seat/set drift
- glasses appear
- CENTER or RIGHT line is missing/truncated
- RIGHT smiles or laughs before CENTER finishes
- all three react simultaneously
- severe eye/mouth/neck/hand deformation
- dialogue is rushed beyond comprehension

Do not reject for harmless micro-motion or tiny style variation.

## Expected beat timing

This is an edit target, not a demand for frame-perfect model timing.

| Approx. time | Beat |
|---:|---|
| 0.0–4.5s | CENTER reversal |
| 4.5–5.0s | delayed processing |
| 5.0–6.2s | RIGHT: 병신 ㅋㅋ |
| 6.2–7.0s | LEFT silent stare |
| 7.0–8.6s | RIGHT: 천재노 ㅋㅋㅋ |
| 8.6–10.0s | CENTER delayed reaction / cut tail |

If the generated clip is shorter, keep GOLD_02 and GOLD_03 first. GOLD_04 may be dropped only if it is actually truncated or rushed; do not regenerate solely to force it in.

## User action

1. Open TopView.
2. Select Seedance 2.0 Mini / 480p / 16:9 / 10 sec.
3. Attach the same locked still and three master packs.
4. Paste the prompt unchanged.
5. Generate once.
6. Upload the result to ChatGPT without editing it first.
