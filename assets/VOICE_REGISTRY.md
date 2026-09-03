# TALKSHOW — VOICE REGISTRY

Updated: 2026-09-03 KST  
Status: **profiles locked / voice IDs not yet assigned**

This is the single registry for recurring character voices. Once a voice ID is assigned, do not change it between episodes.

Seedance native audio is a performance and lip-sync guide. Final published dialogue uses fixed-ID multilingual voice-to-voice conversion.

## Registry

| Character | Production label | Locked voice profile | voice_id | Status |
|---|---|---|---|---|
| CHAR_06 | VOICE_CHAR06 | Native Korean woman, mid-20s; calm medium-low register; measured conversational pace; dry matter-of-fact delivery; low theatricality | UNASSIGNED | blocks P001 publish |
| White T-shirt woman / CHAR_B | VOICE_CHAR_B | Native Korean woman, mid-20s; clear mid register; slightly quicker cadence; skeptical edge; crisp consonants; ordinary friend, not cute/anime | UNASSIGNED | blocks P001 publish |
| Gray-hoodie male | VOICE_GRAY_M | Native Korean man, mid-20s; dry low-mid register; relaxed slightly lazy cadence; restrained nasal laugh; ordinary friend, not announcer | UNASSIGNED | blocks P001 publish |

## ElevenLabs Voice Design prompts

### VOICE_CHAR06

```text
A native Korean woman in her mid-20s speaking conversational Seoul Korean. Medium-low pitch, calm and matter-of-fact, measured pace, dry understated humor, clear but not announcer-like. She sounds like an ordinary intelligent friend casually explaining something strange. Low theatricality, no aegyo, no anime tone, no influencer polish, no breathy luxury-ad voice.
```

Preview:

```text
373년 동안 못 풀던 암호를 AI가 44분 만에 풀었대. 사람들이 저기에 시간 안 들이게 됐으니까, 엄청 쓸모있는 거 아님?
```

### VOICE_CHAR_B

```text
A native Korean woman in her mid-20s speaking conversational Seoul Korean. Natural mid pitch, a little quicker than average, crisp consonants, skeptical and casually blunt without sounding aggressive. She sounds like an ordinary friend reacting immediately, not a host or actor. No aegyo, no cute anime voice, no nasal idol tone, no polished commercial delivery.
```

Preview:

```text
근데 이거 좆도 쓸모없는 거구만. 아니, 내 말은 그게 아니라.
```

### VOICE_GRAY_M

```text
A native Korean man in his mid-20s speaking conversational Seoul Korean. Dry low-mid register, relaxed slightly lazy cadence, understated sarcasm, and a short restrained laugh that does not become loud or theatrical. He sounds like an ordinary male friend sitting nearby, not a broadcaster, comedian, or cartoon character.
```

Preview:

```text
병신, ㅋㅋ. 아니 근데 그건 좀 천재인데? 천재노, ㅋㅋㅋ.
```

## Selection rule

Generate or audition up to three candidates per character, then select one.

Reject a voice if:
- Korean pronunciation sounds non-native
- it sounds like an announcer, commercial narrator, idol, anime character or customer-service agent
- emotion is exaggerated
- CHAR_06 and CHAR_B cannot be distinguished immediately
- laughter becomes a separate cartoon performance
- profanity pronunciation sounds forced

Select for recognizability across ordinary, skeptical and amused deliveries—not for the prettiest standalone sample.

## File and segment naming

- `VOICE_CHAR06_<voice_id>.wav`
- `VOICE_CHAR_B_<voice_id>.wav`
- `VOICE_GRAY_M_<voice_id>.wav`
- `P001_A_CENTER_001.wav`
- `P001_A_LEFT_002.wav`
- `P001_B_CENTER_003.wav`
- `P001_B_RIGHT_004.wav`
- `P001_B_RIGHT_005.wav`

## P001 conversion order

1. Scene A CENTER, approximately 0.00–4.15s → VOICE_CHAR06
2. Scene A LEFT, approximately 4.61–6.66s → VOICE_CHAR_B
3. Scene B CENTER → VOICE_CHAR06
4. Scene B RIGHT first line → VOICE_GRAY_M
5. Scene B RIGHT final line → VOICE_GRAY_M
6. Replace segments at their original start times.
7. Apply profanity BLEEP after conversion.
8. Compare lip timing and loudness; do not regenerate picture for an audio defect.
