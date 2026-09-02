# CURRENT STATE

Updated: 2026-09-03 KST

## Absolute current phase
**PHASE 2 — real episode production / P001 manual generation ready**

The user has confirmed that the production pipeline lock is complete. The user will perform video generation and editing manually. ChatGPT's current responsibility is limited to supplying the exact prompts, source-grounded dialogue, generation order, QC criteria, and user action checklist.

Do not return to set tests, isolated character tests, or 3-person reproducibility tests.

Broad concept planning is complete enough. Do not restart or return to design-for-design's-sake.

The current bottleneck is now:
> **manual generation of P001's six real episode clips from the already locked master first frame.**

Current operating mode: **MANUAL TOPVIEW PROMPT WORKFLOW ONLY**.

## High-level format
- Real Korean community posts/comments are source material.
- Usually 3 characters; 2 or 4 may appear.
- Character functions are fluid beat-by-beat, not permanently fixed boke/tsukkomi roles.
- Final feel: casual people talking in an ordinary room/livestream, not a polished TV/podcast studio.
- Expected output: ~30–60 sec shorts/short-mid; later possible ~3 min.
- Final episodes are assembled from short clips, never one continuous 30–180 sec AI generation.

## Generation settings
- Default: **Seedance 2.0 Mini**
- 480p, 16:9
- short clips ~5–6 sec; use 6–8 sec when Korean dialogue needs it

## Character lock status
- **CHAR_06**: long wavy dark hair with bangs, beige top, **NO GLASSES**. Single-character viability passable.
- **CHAR_B / white T-shirt woman**: light-brown bob, white fitted short-sleeve T-shirt, light-blue jeans, **NO GLASSES**. Identity broadly passable.
- **Gray-hoodie male**: messy short black hair, gray hoodie, dark pants, **NO GLASSES**. Identity broadly passable.
- Do not run isolated character tests just for completeness.

## Key QC history
- `260902_0019_video_edit_1279.mp4`: CHAR_06 viable; dialogue fast at 5 sec; style slightly cleaner than master; character itself acceptable.
- `260902_0025_video_edit_4946.mp4`: CHAR_B acceptable; room/furniture changed, proving set consistency is a separate issue.
- `260902_0027_video_edit_6351.mp4`: richer room failed physical grounding; character looked pasted on background. Decision: simplify set rather than add more prompt prose.
- `260902_0028_video_edit_3438.mp4`: **latest authoritative 3-person test.** Ultra-simple room improved grounding and reproducibility substantially. Remaining failures: glasses-like drift on the center/white-T-shirt character, intended left/center assignment was not respected, and acting was too static / socially disconnected. Background is somewhat plain but this is low priority.

## Latest 3-person test — intended vs actual
Intended:
- Left = white T-shirt woman
- Center = CHAR_06
- Right = gray-hoodie male

Actual visual read:
- Left = CHAR_06
- Center = white T-shirt woman with glasses-like drift
- Right = gray-hoodie male

Therefore seat-position lock and identity lock are not yet production-safe.

## Set direction — keep it simple
Current background direction is basically accepted:
- plain warm beige wall
- simple wooden floor
- one low rectangular wooden table
- little/no fixed seating
- no microphones
- no decorative clutter

A centered simple window OR one small floor lamp may be added later if the room feels too empty, but only after reproducibility is locked. Do not reopen broad interior design now.

## Critical reproducibility strategy — UPDATED
Do **not** regenerate the whole room + three-character composition from textual instructions for every clip if avoidable.

Preferred production grammar:
1. Create/approve **one canonical 3-person MASTER FIRST-FRAME/STILL** with correct identities, positions, room, table, and style.
2. Reuse that same master still as the I2V first frame for repeated dialogue clips.
3. Video prompts should then mostly contain **dialogue + acting**, not repeated long character/set descriptions.
4. For tighter shots, first try **editorial crop/scale from the master**. Do not generate three separate single shots by default.
5. Only generate and lock a separate SINGLE/REACTION anchor when a real episode needs a close reaction that crop/scale cannot deliver acceptably.

Reason: this maximizes visual reproducibility and minimizes both prompt length and generation cost.

## Shot policy — UPDATED
Do not create a large shot system in advance.

Default:
- **MASTER**: fixed frontal 3-person shot, reused heavily.
- **EDIT CROP**: punch in on a character in post when sufficient.
- **SINGLE / REACTION**: optional, generated only when a specific comedic beat actually needs it.

Therefore the earlier idea of generating CHAR_06 + CHAR_B + gray-hoodie single shots immediately after master lock is **too much by default** and is superseded.

Shot instructions remain short prompt lines, e.g.:
`Fixed frontal 3-person master shot. Keep the same composition.`

## Current dialogue test
Korean dialogue:
1. `373년 묵은 암호를 AI가 풀었대.`
2. `근데 첫댓이 '좆도 쓸모 없는 거구만' ㅋㅋ`
3. `ㅋㅋㅋ 틀린 말은 아니야`

Current acting correction:
- Center speaker delivers line 1 calmly.
- Left speaker delivers line 2 with amused disbelief.
- Right speaker delivers line 3 dryly / half-amused.
- Non-speaking characters should subtly listen: tiny eye/head turns, small smiles/laugh reactions.
- Keep motion subtle but not frozen; no exaggerated gestures.

## Next exact action
1. Open `episodes/P001/PRODUCTION_PACKAGE.md`.
2. In TopView, reuse the exact locked canonical 3-person master still.
3. The user generates `S01 → S06` once each with the exact prompts.
4. The user uploads each result for production QC.
5. Do not pre-generate singles or return to any test stage.

Active real source: https://m.dcinside.com/board/thesingularity/1382660

Target final duration: approximately 38.5 seconds.

## Manual production loop
1. ChatGPT writes exact prompt.
2. User manually pastes prompt + references into TopView.
3. User generates once.
4. User uploads result.
5. ChatGPT QC.
6. Move forward unless a real blocker exists.

## Repository
Canonical repository: **`noru358/talkshow`**
Default branch: `main`.

## Response continuity rule
Every talkshow response begins with:
1. **큰 흐름**
2. **현재 세부 단계**
3. **이번 턴 완료조건**

Do not end obvious next steps with permission-seeking such as “원하면 ~해주겠다.” Continue the task directly when the next action is clear.

## Handoff continuity rule
Every future handoff must preserve:
- current phase
- meaningful decisions
- exact reusable prompt blocks / successful prompt examples
- character status
- set spec
- QC failures and why
- source/dialogue examples
- next exact action
- GitHub persistence status
