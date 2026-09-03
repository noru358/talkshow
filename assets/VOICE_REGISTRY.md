# TALKSHOW — VOICE REGISTRY

Updated: 2026-09-03 KST  
Status: **V2 audition profiles locked / voice IDs not yet assigned**

This is the single registry for recurring character voices. Once a voice ID is assigned, do not change it between episodes unless a deliberate series-level re-lock is recorded.

Seedance native audio is a performance and lip-sync guide. Final published dialogue uses fixed-ID multilingual voice-to-voice conversion.

## V2 registry

| Character | Production label | V2 voice profile | voice_id | Status |
|---|---|---|---|---|
| CHAR_06 | VOICE_CHAR06 | Native Korean woman, 20s/early-30s; bright lively mid register; energetic conversational pace; sincere/confident; ordinary friend, not host/influencer/anime | UNASSIGNED | blocks publish |
| White T-shirt woman / CHAR_B | VOICE_CHAR_B | Native Korean woman, 20s/early-30s; natural mid register; friendly everyday tone with somewhat elevated energy; skeptical/indignant edge when reacting; not cold/monotone | UNASSIGNED | blocks publish |
| RIGHT_MASTER_V2 male | VOICE_RIGHT_M | Native Korean man, 20s/early-30s; natural low-mid register; playful everyday Seoul-friend tone; quick social timing; short natural laugh; not announcer/comedy-actor macho | UNASSIGNED | blocks publish |

## Important V2 correction from earlier profile

The earlier registry made CHAR_06 too calm/medium-low and CHAR_B too dry. User review explicitly changed this:
- CHAR_B should still be capable of blunt/indignant reaction, but the baseline must sound like a normal 20s/30s Korean woman with more life and social energy.
- CHAR_06 should be clearly more lively and active than the old calm profile.
- RIGHT remains dry enough for punchlines, but should sound socially quick/playful rather than lazy or under-energized.

Do not revert to the older calmer profiles without an explicit new decision.

---

# VOICE_CHAR06 — BRIGHT / LIVELY MAIN SPEAKER

## Voice-design prompt

```text
A native Korean woman in her 20s or early 30s speaking natural conversational Seoul Korean.

Bright, lively mid-register voice with clear social energy and a slightly quick conversational pace.
She sounds like an ordinary energetic friend who is sincerely explaining her own logic with confidence.
Her delivery should feel spontaneous and alive, not slow, dry, detached, or lecture-like.

She can become amused, puzzled, excited, or mildly defensive without turning theatrical.
Clear natural Korean pronunciation, but not announcer-perfect.

No aegyo.
No anime tone.
No idol voice.
No influencer/YouTuber MC polish.
No luxury-commercial breathiness.
No customer-service tone.
```

### Audition lines

Neutral / explanation:
```text
내 말은, 사람들이 거기에 시간 안 써도 되면 되게 효율적인 거잖아.
```

Lively logic:
```text
생각해보면 이거 엄청 쓸모있는 거 아님?
```

Reactive:
```text
어? 왜, 맞는 말인데? 아니 잠깐만, 그 반응은 좀 이상한데?
```

### Select for
- lively without becoming tiring
- believable ordinary friend energy
- long explanation remains easy to follow
- sincere strange logic becomes funnier because she sounds convinced
- clear contrast from CHAR_B

---

# VOICE_CHAR_B — FRIENDLY / REACTIVE WOMAN

## Voice-design prompt

```text
A native Korean woman in her 20s or early 30s speaking natural conversational Seoul Korean.

Natural mid pitch with friendly everyday energy, slightly more lively than a flat deadpan delivery.
She sounds like a normal close friend, socially alert and expressive.
She can sound skeptical, indignant, incredulous, embarrassed, or amused quickly, but her baseline is not cold or monotone.

Her timing should be crisp and reactive, with natural casual consonants and believable small laughs.
Do not make her overly cute or high-pitched.

No aegyo.
No anime voice.
No nasal idol tone.
No announcer or commercial delivery.
No permanent deadpan monotone.
```

### Audition lines

Ordinary reaction:
```text
아니 근데 그건 좀 너무한 거 아니냐?
```

Indignant / incredulous:
```text
아 진짜 어이없네. 뭐래는 거야 지금.
```

Amused:
```text
야, 그건 좀 웃기다 ㅋㅋ. 와 진짜 황당하네 ㅋㅋ.
```

### Select for
- sounds immediately like a normal Korean female friend in her 20s/30s
- emotion changes are audible but not actor-like
- skeptical/annoyed reactions have energy
- small laugh remains natural
- clearly distinguishable from CHAR_06

---

# VOICE_RIGHT_M — PLAYFUL SOCIAL PUNCHLINE MALE

## Voice-design prompt

```text
A native Korean man in his 20s or early 30s speaking natural conversational Seoul Korean.

Natural low-mid register, relaxed but socially quick and playful.
He sounds like an ordinary male friend who is good at immediately teasing, reacting, or acknowledging a funny point.
Punchlines should land with short timing and a small natural breathy laugh, not a performed comedian laugh.

He may sound dry for a beat, but the overall energy must not feel sleepy, lazy, macho, or detached.
Natural casual pronunciation rather than broadcast diction.

No announcer tone.
No macho trailer voice.
No cartoon/comedy-actor performance.
No rapper/gangster affect.
```

### Audition lines

Short diss:
```text
병신, ㅋㅋ. 야 그건 진짜 아니다 ㅋㅋ.
```

Recognition:
```text
근데 또 천재노, ㅋㅋㅋ. 아 그건 인정이지 ㅋㅋ.
```

Fast reaction:
```text
뭔 개소리야 진짜 ㅋㅋ. 와, 발상은 또 웃기네.
```

### Select for
- short lines land rhythmically
- teasing / disbelief / admiration sound distinct
- laugh is integrated into speech
- ordinary male-friend realism
- pairs well with the updated visual styling in `RIGHT_MASTER_V2`

---

# Audition procedure

For each character:
1. audition up to 3 voice candidates
2. use the same audition-line set for all candidates of that character
3. shortlist top 2
4. listen to the three characters as a combined cast, not only individually
5. lock one final voice ID per character

Score each candidate /5 on:
- native Korean naturalness
- character fit
- emotional range
- repeated-listening durability
- separation from the other two voices

Total: /25.

## Reject a voice if
- Korean pronunciation sounds non-native or synthetic in a distracting way
- it sounds like an announcer, commercial narrator, idol, anime character, customer-service agent, or professional comedian
- laughter becomes a separate cartoon performance
- profanity pronunciation sounds forced
- CHAR_06 and CHAR_B cannot be distinguished immediately
- the voice only works for one emotion and collapses in ordinary speech

Select for cast recognizability and conversational chemistry, not for the prettiest standalone sample.

## File and segment naming

- `VOICE_CHAR06_<voice_id>.wav`
- `VOICE_CHAR_B_<voice_id>.wav`
- `VOICE_RIGHT_M_<voice_id>.wav`
- episode segments: `Pxxx_<scene>_<speaker>_<n>.wav`

## Conversion policy

1. Generate I2V with real dialogue so mouth timing, breath, and acting exist.
2. Treat generated/native audio only as performance guide.
3. Split by speaker.
4. Convert each segment to the character's fixed voice ID with multilingual voice-to-voice.
5. Preserve original timing as closely as possible.
6. For inseparable overlap/laughter, replace only that short segment with the same character voice ID via TTS if necessary.
7. Compare lip timing and loudness; do not regenerate picture for an audio-only defect.
