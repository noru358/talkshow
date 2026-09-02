# CURRENT STATE

Updated: 2026-09-03 KST

## Absolute current phase
**PHASE 1 — production pipeline lock / set reproducibility lock**

Broad concept planning is mostly complete. Character identity has been tested enough. The current bottleneck is now **set simplicity, set continuity, and correct physical grounding of 2–4 characters (3 default)**.

Current operating mode: **MANUAL TOPVIEW PROMPT WORKFLOW ONLY**.

Do not restart the project from scratch. Do not return to CHAR_06-only testing unless a real failure specifically requires it. Do not reopen Work-mode automation unless the user explicitly asks.

## High-level format
- Real Korean community posts/comments are the source material.
- Usually 3 characters per episode; 2 or 4 may appear.
- Character functions are fluid by beat; no permanently fixed boke/tsukkomi role.
- AI should lightly transform/recombine human-written reactions rather than invent bland generic dialogue.
- Final feel: friends clustered in an ordinary Korean room / livestream, not a polished TV/podcast studio.
- Expected duration: Shorts/short-mid ~30–60 sec; possible later long-form ~3 min.
- Long outputs are assembled from short fixed shots, not generated as one continuous clip.

## Generation settings
- Default video model: **Seedance 2.0 Mini**.
- Validation used: 480p, 16:9, ~5–6 sec clips.
- 5 sec can make Korean dialogue too fast; use 6–8 sec when needed rather than over-compressing dialogue.

## Character status
- **CHAR_06**: passable single-character result. Identity/mouth/facial acting acceptable; style slightly cleaner/more colored than master but usable.
- **CHAR_B (white T-shirt / light-blue jeans woman)**: passable character result. Main issue was set changed versus CHAR_06 run.
- **Gray-hoodie male**: character itself reproduced reasonably; latest failure was physical placement in the richer room, not identity.
- Other provided sheets: long-haired woman in black top/dark long skirt; black-jacket male with beige pants.

Do not run isolated character tests merely for completeness.

## Key QC history
- `260902_0019_video_edit_1279.mp4`: CHAR_06 usable. Dialogue too fast at 5 sec; tablet/logo and set interpretation imperfect; character itself acceptable.
- `260902_0025_video_edit_4946.mp4`: CHAR_B acceptable; set/furniture/chair/table changed from 1279, proving set consistency must be locked separately.
- `260902_0027_video_edit_6351.mp4`: gray-hoodie character acceptable, but person appeared pasted / sitting on top of background. Rich room had too many fixed objects/seats and bad depth relationships.

## Current set direction — `TALKSHOW_SET_01_SIMPLE`
Use an **ultra-simple EMPTY ROOM anchor**, not the richer decorated Korean-room reference.

Target:
- straight-on frontal 2D view
- 16:9
- plain warm beige wall
- one simple centered rectangular window
- very simple Seoul night skyline
- one low rectangular wooden table centered in foreground
- simple wooden floor
- little or no fixed seating in the anchor image
- optional one small floor lamp only

Explicitly avoid microphones, neon sign, pegboard, cabinet, plants, shelves, rugs, decorative clutter, professional studio look, café/office/designer-interior look.

Reason: simplify geometry so characters can be physically grounded reliably. Do not solve the latest placement failure by adding more prompt prose; simplify the actual anchor.

## Camera / shot lock
Avoid AI-generated zoom/pan/tilt/camera motion for now. Use separate fixed shots and edit together.

- MASTER SHOT: `Create one straight-on 16:9 master shot with all three characters visible at the same time.`
- SINGLE SHOT: `Create one straight-on 16:9 single-character talk-show shot.`
- REACTION SHOT: optional fixed single-character reaction.

Shot instructions should remain one line; do not waste prompt budget on long camera blocks.

## Prompt-budget strategy
TopView prompt limit: 10,000 characters.

Use modular compression:
1. short shared style block
2. short character block(s)
3. short set block
4. one-line shot instruction
5. dialogue/action block (main variable budget)

Reference images should carry most visual information. Compression means removing duplicated constraints, not deleting behaviorally important constraints.

## Current compact style block
```text
Use the provided character reference as the strict character and drawing-style authority.

Match the same low-fi 2D webcomic style: thick slightly imperfect black outlines, flat muted colors, minimal shading, simple cheap-cute proportions.

Do not beautify, polish, modernize or redesign the character. Avoid polished anime/webtoon rendering, realism, glossy/cinematic lighting, and added visual detail.
```

## Current compact set block
```text
Use the provided set reference as the strict room/layout authority.

Preserve the same simple straight-on Korean room: plain warm beige wall, centered window with a simple Seoul night skyline, low rectangular wooden table, and simple wooden floor.

Keep the set sparse and physically readable. Do not add or redesign major furniture, decorations, microphones, shelves, plants, rugs, pegboards, neon signs, or extra props.
```

## Next exact action
1. Finalize one **ultra-simple empty-room `TALKSHOW_SET_01_SIMPLE` anchor**.
2. Use 3 existing character sheets + that anchor for **one 3-character master shot**.
3. QC only: physical grounding, table/room geometry, individual character identity, usable 3-person composition.
4. If pass, do not add more set experiments. Create single shots in the same room.
5. Then move immediately to a real community-sourced 3-person episode.

## Manual production loop
1. ChatGPT writes the exact final prompt.
2. User manually pastes prompt + references into TopView.
3. User generates once.
4. User uploads result.
5. ChatGPT QC.
6. Move forward unless a real blocker exists.

## Repository
Canonical repository: **`noru358/talkshow`**
Default branch: `main`.

## Handoff continuity rule
Every future handoff must preserve, not merely summarize:
- current phase
- meaningful decisions
- exact reusable prompt blocks / important successful prompt examples
- character status
- set spec
- relevant QC failures and why
- community-source/dialogue example(s)
- next exact action
- GitHub persistence status
