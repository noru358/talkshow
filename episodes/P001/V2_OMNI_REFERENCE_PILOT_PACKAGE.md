# P001 — V2 OMNI REFERENCE PILOT PACKAGE

Updated: 2026-09-04 KST  
Status: **READY FOR USER REVIEW / DO NOT GENERATE WITHOUT EXPLICIT APPROVAL**

## Purpose

Test the cheapest viable recurring-voice architecture on the first actual V2 scene:

> locked V2 cast still + three free catalog audio references + exact scene dialogue

No paid exact-line TTS is required before this test. The only next credit-consuming action is one video generation.

## TopView settings

| Field | Value |
|---|---|
| Mode | Omni Reference |
| Model | Seedance 2.0 Mini |
| Resolution | 480p |
| Aspect ratio | 16:9 |
| Duration | 10 sec |
| Generation count | exactly 1 |

## Reference upload order

### Image

1. `assets/v2_locked/SET_A_HOME_CAST_STILL.png` — exact first frame and full visual authority

Do not add the separate character packs on this first pilot unless the TopView UI requires them. The locked cast still already contains the three identities, positions, clothing and set geometry; fewer competing visual references are safer.

### Audio

1. `LEFT_CHAR_B_Gaeun_outdoors.mp3`
2. `CENTER_CHAR06_Harin.mp3`
3. `RIGHT_MALE_Taemin.mp3`

## Exact copy-paste prompt

```text
Use Image Reference 1 as the exact first frame and visual authority.

Preserve the exact three character identities, clothing, facial designs, body proportions, HOME room, table, drawing style, and LEFT/CENTER/RIGHT positions throughout the clip.

Use Audio Reference 1 only as the voice and timbre reference for the LEFT woman in the white T-shirt.
Use Audio Reference 2 only as the voice and timbre reference for the CENTER woman with long dark hair and a beige top.
Use Audio Reference 3 only as the voice and timbre reference for the RIGHT man.

Do not copy any words or sentences from the audio reference recordings.
Speak only the dialogue written below.
Do not swap, blend, or share voices between characters.

Fixed frontal camera. No camera movement, zoom, scene change, position swap, character redesign, subtitles, captions, text, logos, music, or new objects.

This is one continuous casual Korean conversation between three friends.

DIALOGUE:

CENTER woman:
“사람들이 저기에 시간 안 들이게 됐으니까, 엄청 쓸모있는 거 아님?”

RIGHT man:
“병신, ㅋㅋ.”

After one short beat, the same RIGHT man:
“천재노, ㅋㅋㅋ.”

Only CENTER and RIGHT speak. LEFT remains completely silent and never lip-syncs.

PERFORMANCE:

CENTER speaks calmly and sincerely, as if the conclusion is obvious. She does not perform the line as a joke. While explaining, she leans slightly forward and makes one clearly visible open-palmed one-hand gesture, as if laying out an obvious conclusion. The gesture must be readable at medium-wide framing, not tiny background motion.

LEFT and RIGHT remain neutral until CENTER has fully finished “엄청 쓸모있는 거 아님?”. They must not anticipate the joke.

After CENTER finishes, LEFT visibly double-takes: her eyes move first, then she turns her head clearly toward CENTER and makes one short upper-body recoil as the logic lands.

About 0.2 seconds later, RIGHT turns clearly toward LEFT, leans slightly in her direction, and says “병신, ㅋㅋ” dryly. His shoulders bounce once with a short natural laugh. The reaction must be visibly larger than a glance, but not full-body flailing.

LEFT then snaps her gaze and head toward RIGHT, gives him a strongly readable offended stare, and raises one open palm in a silent “뭐?” reaction. She does not speak or lip-sync.

After one short pause, RIGHT turns back toward CENTER and says “천재노, ㅋㅋㅋ” with amused admiration. He gives one brief chest-level celebratory fist gesture and a second short shoulder bounce. Keep the fist compact and clear of every face.

CENTER reacts last with a clearly visible surprised grin, a small backward torso movement, and one brief shoulder lift. Her reaction is readable, not merely a tiny puzzled smile.

The causal order is:
CENTER finishes → LEFT registers the logic → RIGHT addresses LEFT → LEFT stares → RIGHT praises CENTER → CENTER reacts.

This is V2 performance, not the restrained V1 acting baseline. Reactions and gestures must be clearly readable at medium-wide framing: clear head turns, short torso lean/recoil, visible facial changes, open-palmed one-hand gesture, shoulder bounce, and one compact celebratory fist.

Keep every action causally staggered and give each reaction its own beat. Do not make multiple characters turn, gesture, smile, blink, or laugh simultaneously. Keep the seated positions, table, props, and body grounding stable. Avoid only full-body flailing, constant gesturing, gestures crossing another character's face, extreme mouth opening, squeezed-shut or deformed eyes, face warping, neck deformation, and hand deformation.

Use natural Korean speech and restrained accurate lip movement.
```

## PASS criteria

- exact HOME cast identity, clothes, seating and set remain stable
- Audio 2/Harin characterizes CENTER; Audio 3/Taemin characterizes RIGHT
- LEFT remains silent; no speaker or voice swap
- no catalog-preview wording leaks into the scene
- all three written lines are present and comprehensible
- RIGHT does not react before CENTER finishes
- reactions are causally staggered and visibly larger than V1 at medium-wide scale
- CENTER's open-palm explanation, LEFT's recoil/open-palm offense, RIGHT's shoulder bounce/fist, and CENTER's final body reaction are all present and readable
- no severe face, eye, mouth, neck or body deformation

## Voice-reference decision after one result

- **PASS:** keep the free three-audio-reference route for the next clip; no exact-line TTS purchase.
- **CONDITIONAL:** keep the picture and repair only the defective audio segment if practical.
- **FAIL:** do not retry automatically. Return for user QC, then decide whether exact-line TTS/audio replacement is worth the added credits.

## Credit gate

The preparation and three audio references cost 0 credits. Do not click Generate and do not submit via API until the user explicitly approves the single video-generation charge shown by TopView.
