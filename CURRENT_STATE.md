# CURRENT STATE

Updated: 2026-09-03 KST

## Absolute current phase
**PHASE 1 — CHAR_06 single-character production lock**

Current operating mode: **MANUAL PROMPT WORKFLOW ONLY**

Do not advance to other characters, the 3-character pilot, real community episode production, or an automated Work/TopView execution pipeline until CHAR_06 is locked.

## Latest authoritative decision
The automated Work-mode production path is paused because prompt rewriting and automatic reference handling degraded style fidelity and introduced incorrect character details.

Current loop:
1. ChatGPT writes one exact final prompt manually.
2. The user manually uploads the selected reference(s) and prompt to TopView.
3. The user generates one result and returns it.
4. ChatGPT performs QC and writes the next exact prompt.

Do not autonomously rewrite, summarize, optimize, or execute the production prompt unless the user explicitly reopens automation.

## CHAR_06 visual authority
Primary authority: `CHAR06_MASTER_SHEET.png`

Canonical lock:
- young woman
- long wavy dark hair with bangs
- large round eyes
- no glasses or eyewear
- light beige cardigan/top
- dark wide-leg pants
- white sneakers
- low-fi 2D webcomic style
- thick black outlines
- flat muted colors
- minimal shading
- slightly rough, clumsy, cheap-cute proportions

Never beautify or reinterpret CHAR_06 as generic GPT illustration, polished anime, detailed webtoon, realistic art, glossy rendering, or cinematic lighting.

## Current findings and failures
- Seedance 2.0 Mini is the default validation model.
- Default validation settings: 480p, 4–5 seconds, 16:9.
- Style fidelity is the first QC criterion, ahead of identity, action readability, prop/set stability, anatomy, and cost.
- A master sheet plus many cropped references correlated with stronger style drift; prefer the master sheet as the main authority.
- `260902_0014_video_edit_3311.mp4`: direction usable, but not lock-ready due to neck/shoulder/hand ambiguity and too many beats.
- `260902_0018_image_to_video_2015.mp4`: failed due to major style drift, generic clean AI illustration, glasses, and identity reinterpretation.
- `Video Draft.mp4`: failed as a production method because the character-sheet grid itself behaved like the animated frame.

## Locked production direction
Use this sequence:

`CHAR06_MASTER_SHEET.png → clean 16:9 talk-show scene still → selected still as I2V first frame → 5-second Seedance 2.0 Mini clip → QC`

Do not directly animate the master-sheet grid.

Scene-still requirements:
- one CHAR_06 only
- simple desk and tabletop microphone
- simple studio
- seated medium shot
- exact master-sheet drawing language
- no text, subtitles, logos, or glasses

## Next exact action
Provide one exact TopView image-generation prompt for a clean CHAR_06 16:9 seated talk-show still. The user manually generates and returns the still. After still QC, provide one exact 5-second Seedance 2.0 Mini I2V prompt.

## Repository
Canonical repository: `noru358/-`
Default branch: `main`

The repository may later be renamed to `talkshow`, but do not assume the rename has happened. Check `noru358/talkshow` first, then fall back to `noru358/-`.

## Handoff persistence rule
At every session handoff:
1. Update `CURRENT_STATE.md`.
2. Update `NEW_SESSION_HANDOFF.md`.
3. Update any workflow documents changed by the session.
4. Commit and push to the active branch.
5. Verify the remote branch points to the new commit before reporting completion.
