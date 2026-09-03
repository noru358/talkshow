# TALKSHOW — VOICE REFERENCE RUNTIME RULES

Updated: 2026-09-04 KST
Status: **ACTIVE RUNTIME LOCK**

## Why this exists

TopView / Seedance 2.0 Mini R2V rejected a generation when the total attached audio-reference duration exceeded 15.2 seconds. The failed request was refunded.

## Runtime rule

Use short clean recurring reference clips instead of the full catalog-preview files.

- target duration per recurring voice reference: **about 4.0 seconds**
- three-speaker maximum total at 4 sec each: **about 12 sec**, safely below the observed 15.2 sec R2V limit
- attach **only the voice references for characters who actually speak in that generated clip** whenever possible
- silent characters do not need an audio reference for that clip
- trim from a clean single-speaker region with no music, overlap, or long silence
- preserve natural connected speech; do not use a fragment so short that the timbre/prosody becomes unrepresentative

## Selected recurring references

- LEFT / CHAR_B: Gaeun outdoors → make `VOICE_REF_LEFT_GAEUN_4S`
- CENTER / CHAR_06: Harin → make `VOICE_REF_CENTER_HARIN_4S`
- RIGHT / recurring male: Taemin → make `VOICE_REF_RIGHT_TAEMIN_4S`

## Clip attachment rule

Examples:
- CENTER + RIGHT speak → attach Harin 4s + Taemin 4s only
- LEFT + CENTER speak → attach Gaeun 4s + Harin 4s only
- all three speak → attach all three 4s references; total about 12 sec

## Prompt rule

Every executable scene prompt must explicitly map the attached audio files to screen roles and must state that silent characters do not speak or lip-sync.

Do not go back to attaching the three full preview recordings by default.