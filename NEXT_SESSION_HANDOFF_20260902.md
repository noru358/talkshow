# TALKSHOW — NEXT SESSION HANDOFF

Date: 2026-09-02 KST

## Read this first
Do **not** re-plan the project from scratch.
Open `CURRENT_STATE.md` first, then `PROJECT_BIBLE.md`, `PRODUCTION_PIPELINE.md`, `assets/CHARACTER_ASSET_SPEC.md`, and `episodes/P001/EPISODE_SPEC.md` only as needed.

## Current position
**Phase 4/7 — Character Asset Package, in progress.**

Completed:
- core show concept
- 3-person flexible-role format
- source/comment driven writing rule
- A-style visual direction
- 10-character cast pool
- Pilot 001 source selection
- asset specification skeleton

Next immediate task:
**Produce actual reusable individual asset files for C/E/K + clean talk-show set, preserving the exact A-style.**

## Critical user requirements
1. Visual style must remain the exact previously approved **A-style**: crude/simple hand-drawn community-webtoon look. Do not polish it into generic AI anime/webtoon art.
2. **Do not output an infographic, character board, sticker sheet, comparison sheet, or labeled concept poster.**
3. Deliver assets in forms another AI/tool can actually consume: separate PNGs (prefer transparent backgrounds where appropriate), clean background plates, plus manifest/MD/JSON.
4. User has already approved overall character quality and wants to move fast into production.
5. Do not stop after generating an image. After every deliverable, state the current pipeline phase and continue to the next executable step unless a real tool/account blocker exists.

## Locked cast pool
B, C, E, F, G, K, L, M, Q, R

Pilot 001 temporary cast:
C / E / K

## Minimum Pilot asset set per character
- seated_neutral
- seated_explaining
- seated_deadpan
- seated_big_laugh
- seated_shocked
- seated_annoyed
- standing_neutral
- mouth_closed
- mouth_mid
- mouth_wide
- eyes_open
- eyes_half
- eyes_closed

Use naming that can later be called deterministically by episode JSON.

## Set asset target
Create a reusable 9:16 clean talk-show set in the same A-style:
- no characters on master background
- three seating positions
- supports 3-shot / 2-shot / 1-shot crops
- empty area for topic/source/cutaway visual
- minimal props/details
- separate desk/foreground layer if useful for compositing

## Pilot 001 content source
DCInside dcbest:
https://gall.dcinside.com/board/view/?id=dcbest&no=459446&_dcbest=6&page=1

User-provided key human comment chain:
- `좆도 쓸모없는 거구만`
- `사람들이 저기에 시간을 안들이게 되었으니 엄청 쓸모있음`
- surrounding reactions include `병신 ㅋㅋ`, `천재노 ㅋㅋㅋ`

Writing principle:
- preserve actual human phrasing as much as possible
- AI should select/cast/trim/bridge, not rewrite everything
- do not pre-sanitize raw source
- public edit may use beep/cut/masking after script is assembled

## Full pipeline reminder
1. Production principles — DONE
2. Repository/MD system — DONE
3. Character/style selection — DONE
4. Asset package — CURRENT
5. Script + storyboard integration — NEXT
6. Voice + renderer pipeline
7. Pilot 001 final video

## Handoff success condition
The next session should begin by restoring the repo state and then immediately continue with individual C/E/K asset production and the clean talk-show set. Do not ask the user to repeat decisions already recorded here.
