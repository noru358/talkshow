# TALKSHOW — VOICE REFERENCE RUNTIME RULES

Updated: 2026-09-04 KST
Status: **INTERIM RUNTIME EVIDENCE — NOT FINAL VOICE ARCHITECTURE**

## Why this exists

TopView / Seedance 2.0 Mini R2V rejected a generation when the total attached audio-reference duration exceeded 15.2 seconds. The failed request was refunded.

This file preserves the observed runtime constraint and the reusable trimmed references, but **the 4-second reference route is no longer the preferred final production voice architecture** after a real P002 generation sounded too mechanical and tempo-forced.

Current higher-level authority: `PERFORMANCE_AUDIO_ARCHITECTURE.md`.

## Interim 4-second reference rule

When using TopView catalog previews as Omni timbre references:
- target duration per recurring voice reference: about **4.0 sec**
- three speakers at 4 sec each total about 12 sec, below the observed 15.2-sec ceiling
- attach only speaking-character references when possible
- trim from a clean single-speaker region with no music, overlap, or long silence

Prepared labels:
- LEFT / CHAR_B: `VOICE_REF_LEFT_GAEUN_4S`
- CENTER / CHAR_06: `VOICE_REF_CENTER_HARIN_4S`
- RIGHT / recurring male: `VOICE_REF_RIGHT_TAEMIN_4S`

## Loudness finding

The Taemin source preview was materially quieter than Gaeun/Harin. For the prepared 4-sec references, Taemin required approximately **+10 dB** gain to bring average loudness close to the other two without clipping.

This was useful evidence: reference loudness balance can be normalized, and the resulting generated speaker loudness became much more even.

Do not treat raw catalog-preview loudness as a character-design property.

## Why this is not the final route

The viable 16:9 P002 Omni test showed:
- voice timbre could be guided;
- speaker loudness could be balanced;
- but the actual speech remained synthetic/mechanical;
- preselected video duration encouraged unnatural pacing / tempo adjustment;
- short timbre references did not solve natural multi-speaker conversation timing.

Therefore the current target architecture is:

> **PERFORMANCE MASTER → whole-scene multi-speaker dialogue generation once → one dialogue-master file → derive timing/video duration → feed the same master into Omni as timing authority**

Candidate dialogue engines for the next A/B:
- ElevenLabs v3 Dialogue
- Typecast / strongest accessible Korean dialogue engine

The objective is one natural whole-scene conversation, not separate manually placed lines.

## If the interim 4-second route is used again

Prompt must explicitly:
- map each audio reference to a screen role;
- state that reference words must not be copied;
- state that silent characters do not speak/lip-sync;
- keep total reference duration under the active model ceiling.

But do not return to this route by default merely because the files already exist.
