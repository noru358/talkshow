# TALKSHOW — FULL AUTHORITATIVE NEW SESSION HANDOFF

**Last updated:** 2026-09-03 KST

> **CURRENT OVERRIDE:** Production pipeline lock is complete. The active phase is `PHASE 2 — real episode production / P001 manual generation ready`. The user will generate/edit manually; ChatGPT supplies prompts and the user's action list only. Use `CURRENT_STATE.md` and `episodes/P001/PRODUCTION_PACKAGE.md` before following any older Phase-1 instructions below.

This is the authoritative continuation file. A fresh session must be able to continue the project from this document without re-planning or losing the prompt history, failed-test lessons, current character status, set design decisions, or next actions.

---

# 0. ABSOLUTE CURRENT STAGE

## PHASE 1 — production pipeline lock / set reproducibility lock

Broad concept planning is mostly complete.

We are now locking a reproducible visual/video production system before making the real 3-character episodes.

The main bottleneck is **no longer character identity**. The current bottleneck is:

> **set simplicity / set continuity / correct physical grounding of 2–4 characters, with 3 characters as the default.**

Do NOT restart the project from scratch.
Do NOT return to endless “test for the sake of testing.”
Only run tests that directly prove production viability.

---

# 1. HIGH-LEVEL PROJECT DIRECTION

The final content is a casual AI-character talkshow based on real Korean internet/community posts and comments.

Core principles:
- usually 3 characters per episode, but 2 or 4 may appear
- roles are NOT permanently fixed as boke/tsukkomi or fact-checker/reaction character
- character functions can change beat by beat: speaker, deadpan, disbelief, nonsense, laugh amplification, rebuttal, reaction, etc.
- real community post/comment wording should be the primary source material
- AI should lightly transform / recombine human-written reactions rather than invent generic “AI dialogue”
- the social/comedic value often comes from the comment-flow itself, not from a formal scripted premise
- visual feel should be friends clustered in an ordinary Korean room / livestream environment, not a polished TV studio or podcast stage

Expected output lengths:
- Shorts / short-mid: roughly 30–60 sec
- possible later long-form: roughly 3 min

Important production principle:
**Do not generate 30–180 sec as one continuous AI clip.**
Build final episodes from short fixed clips and edit them together.

---

# 2. AUTHORITATIVE WORKFLOW — MANUAL TOPVIEW PROMPT LOOP

Automation / Work-mode prompt rewriting is PAUSED.

Reason:
- automated rewriting degraded visual quality
- a Work-generated prompt incorrectly added round glasses to CHAR_06 despite glasses being forbidden
- automatic reference selection / prompt summarization introduced drift
- manual prompt entry produced materially better results

Current production loop:
1. ChatGPT writes the exact final prompt manually.
2. User manually uploads the chosen references and prompt to TopView.
3. User generates one result.
4. User uploads the result to ChatGPT.
5. ChatGPT performs QC.
6. Move forward unless a real production blocker exists.

Do NOT reopen Work automation / automatic TopView execution unless the user explicitly asks.

---

# 3. MODEL / SETTINGS SO FAR

Default video model selected by user:
**Seedance 2.0 Mini**

Current validation settings used:
- 480p
- 16:9
- short clips around 5–6 sec

5 seconds often makes Korean dialogue too fast when there are multiple lines.
This is not a reason to over-compress the dialogue; in real production use 6–8 sec when necessary.

---

# 4. GLOBAL CHARACTER STYLE PRINCIPLE

Character sheets are the main visual authority.

Target style:
- simple low-fi 2D webcomic
- thick slightly imperfect black outlines
- flat muted colors
- minimal shading
- simple cheap-cute / slightly clumsy proportions
- modest visual detail
- intentionally not polished

Avoid:
- generic GPT illustration polish
- polished anime
- polished Korean webtoon rendering
- realism / semi-realism
- glossy render
- cinematic lighting
- detailed textures
- elegant thin linework
- beautification or modernization

Important reference wording:
> Use the provided reference sheet as the strict character and style reference, but do not reproduce the sheet layout itself. Create a new single scene in the same design language.

Meaning:
- use the sheet as DESIGN + STYLE authority
- do NOT literally reproduce or animate the character-sheet grid

---

# 5. CHARACTER POOL / CURRENT STATUS

## CHAR_06
Canonical visual:
- young woman
- long wavy dark hair with bangs
- large round eyes
- NO glasses / eyewear
- light beige cardigan/top
- dark wide-leg pants
- white sneakers if visible
- low-fi 2D webcomic style

Status:
- single-character talkshow result is passable
- mouth movement / facial acting acceptable
- style not perfectly identical to master sheet; generated version became slightly cleaner / more colored, but still usable
- current conclusion: CHAR_06 itself is not the main bottleneck anymore

## CHAR_B — white T-shirt woman
Provided sheet:
- young woman
- straight medium-length light-brown bob
- large round eyes
- plain white fitted short-sleeve T-shirt
- light-blue high-waist jeans
- white sneakers
- simple soft proportions

Status:
- character generation passable
- main issue in its test was that the room/furniture changed versus the CHAR_06 result

## Gray-hoodie male
Provided sheet:
- young man
- messy short black hair
- large round eyes
- gray hoodie
- loose black pants
- white sneakers
- simple boyish proportions

Status:
- character itself reproduced reasonably well
- latest failure was physical placement / set geometry, NOT identity

## Other provided character sheets
### Long-haired woman
- long wavy brown hair
- black long-sleeve top
- dark gray long skirt
- black shoes
- calmer / more composed impression

### Black-jacket male
- short black hair
- sleepy / half-lidded eyes
- black jacket over dark shirt
- light beige pants
- black sneakers
- dry / deadpan impression

Do NOT run isolated character tests merely for completeness if the character itself is already clear.

---

# 6. IMPORTANT VIDEO QC HISTORY

## `260902_0019_video_edit_1279.mp4` — CHAR_06
Useful passable result.

Positives:
- character identity survived
- mouth movement acceptable
- facial acting acceptable
- tablet-reading situation readable
- no catastrophic anatomy failure

Issues:
- dialogue too fast because too much Korean dialogue was packed into ~5 sec
- drawing style not 100% identical to sheet; somewhat cleaner/more colored
- tablet could look like iPad/laptop hybrid
- Apple-like logo appeared
- set/background interpretation was not fully reusable

Decision:
- CHARACTER = passable
- style = acceptable enough for current production testing
- pacing can be solved by longer clips

## `260902_0025_video_edit_4946.mp4` — CHAR_B
Positives:
- character itself acceptable
- drawing style acceptable enough
- dialogue slightly fast but tolerable

Main issue:
- background / furniture / chair / table changed from 1279

Decision:
> **Set consistency must be locked separately from character identity.**

## `260902_0027_video_edit_6351.mp4` — gray hoodie male + richer room
Major failure:
- person appeared visually pasted / seated on top of the background
- depth relationship among person / table / floor chair / room was wrong
- richer room anchor contained too many fixed objects

Additional issues:
- too many props reduced reproducibility
- fixed chairs already embedded in set reference conflicted with newly inserted character
- tablet became visually dominant
- richer room geometry made multi-character placement harder

Decision:
> **Do not fix this by adding more prompt text. Simplify the actual set anchor.**

---

# 7. COMMUNITY CONTENT TEST USED — FABLE 5.1

Source used:
https://gall.dcinside.com/board/view/?id=dcbest&no=459446&_dcbest=6&page=1

Post theme:
- Fable 5.1 allegedly solved a roughly 373-year-old cipher
- post framed it as a major AI achievement

User-selected comment flow:
1. “좆도 쓸모 없는 거구만”
2. reply approximately: “사람들이 저기에 시간을 안 들이게 되었으니 엄청 쓸모 있음”
3. comedic reaction / laugh beat

User-preferred dialogue version:
- “373년 묵은 암호를 AI가 풀었대.”
- “근데 첫댓이 '좆도 쓸모 없는 거구만' ㅋㅋㅋ 이게 뭐야 ㅋㅋ.”
- “그런데 바로 밑에 '사람들이 저기에 시간을 안들이게 되었으니 엄청 쓸모있음'이래 ㅋㅋㅋㅋㅋ”

Compressed test version later used:
- “373년 묵은 암호를 AI가 풀었대.”
- “근데 첫댓이 '좆도 쓸모 없는 거구만' ㅋㅋㅋ”
- “바로 밑엔 '시간 안 들이게 됐으니 쓸모 있는 거지'래. 맞말이네 ㅋㅋ”

Lesson:
- dialogue + action should be tested TOGETHER
- isolated visual tests are insufficient
- production tests should resemble actual episode workload

---

# 8. EXACT SUCCESSFUL LONG PROMPT — KEEP AS BASELINE

This is the user's manually entered combined CHAR_06 prompt that produced `260902_0019_video_edit_1279.mp4`.

```text
@Image1
Use the provided CHAR_06 master sheet as the strict visual authority. 단, 이걸 그대로 사용하라는 게 아니라 디자인만 참고하라는 것임.
Preserve exactly the same character and drawing style:
young woman, long wavy dark hair with bangs, large round eyes, no glasses, light beige cardigan/top, dark wide-leg pants, white sneakers if visible.
Highest priority is exact style fidelity to the master sheet:
simple low-fi 2D webcomic, thick slightly imperfect black outlines, flat muted colors, minimal shading, slightly rough cheap-cute proportions.
Do not beautify, polish, modernize, or reinterpret the character.
Avoid generic AI illustration, polished anime, polished webtoon rendering, realism, glossy lighting, cinematic lighting, detailed textures, or elegant linework.
The master sheet is the maximum allowed visual complexity.
Create one clean 16:9 talk-show still.
One character only.
CHAR_06 is seated behind a simple desk in a small talk-show studio.
Show a medium shot.
Place one tabletop microphone on the desk.
Also place an iPad on the desk in front of her, and she is looking at the iPad as if reading something funny from it.
Her expression should be mildly amused and attentive, as if she is about to comment on what she is reading.
Keep the studio background simple and flat in the same low-fi style.
No subtitles, no captions, no logos, no speech bubbles, no watermark, no collage, no storyboard, no character-sheet layout.
Do not render readable text on the iPad screen. Just imply that content is displayed on it.

Preserve the exact first-frame character identity, low-fi drawing style, desk, microphone, iPad, studio background, and overall composition.
Create a 5-second image-to-video talk-show clip.
Camera stays fixed.
One character only.
Keep the performance subtle, stable, and readable.
No scene change, no camera move, no extra props, no subtitles, and no visual redesign.
CHAR_06 is seated at the desk, looking at the iPad and reacting to what she is reading.
She speaks in Korean with natural mouth movement and subtle facial acting.
Dialogue:
"373년 묵은 암호를 AI가 풀었대."
"근데 첫댓이 '좆도 쓸모 없는 거구만' ㅋㅋㅋ 이게 뭐야 ㅋㅋ."
"그런데 바로 밑에 '사람들이 저기에 시간을 안들이게 되었으니 엄청 쓸모있음'이래 ㅋㅋㅋㅋㅋ"
Performance direction:
- Start calm and matter-of-fact on the first line.
- On the second line, she becomes amused and slightly incredulous.
- On the third line, she looks more entertained and lightly laughs while quoting the comment.
- Keep shoulders, hands, desk, microphone, and iPad stable.
- No exaggerated gestures.
```

Important lesson:
- long prompt worked reasonably well
- prompt limit is 10,000 characters
- future goal is compression WITHOUT losing the constraints that actually matter

---

# 9. COMPRESSED PRODUCTION PROMPT BLOCKS

## 9.1 Global style block
```text
Use the provided reference sheet as the strict character and style reference, but do not reproduce the sheet layout itself. Create a new single scene in the same design language.

Match the same low-fi 2D webcomic style: thick slightly imperfect black outlines, flat muted colors, minimal shading, simple cheap-cute proportions, and modest visual detail.

Do not beautify, polish, modernize, or redesign the character. Avoid glossy rendering, realism, cinematic lighting, polished anime, polished webtoon detail, or added texture.

One clean scene only. No collage, no storyboard, no character-sheet layout, no subtitles, no captions, no logos, no watermark.
```

## 9.2 Compact character mini-prompts
### Gray hoodie male
```text
Preserve this exact character: young man, messy short black hair, large round eyes, light gray hoodie, loose black pants, white sneakers, simple boyish proportions.
```

### White T-shirt woman / CHAR_B
```text
Preserve this exact character: young woman, straight medium-length light brown bob hair, large round eyes, plain white short-sleeve T-shirt, light blue high-waist jeans, white sneakers, simple soft proportions.
```

### Long-haired black-top woman
```text
Preserve this exact character: young woman, long wavy brown hair, calm oval face, black long-sleeve top, dark gray long skirt, black shoes, slightly calmer and more composed impression.
```

### Black-jacket male
```text
Preserve this exact character: young man, short black hair, sleepy or half-lidded eyes, black jacket over a dark shirt, light beige pants, black sneakers, slightly dry and deadpan impression.
```

---

# 10. SET DESIGN HISTORY — WHAT WAS REJECTED AND WHY

Several set concepts were explored.

## Professional studio / podcast studio
Rejected because:
- too grand
- too obviously “set-like”
- user wants people clustered in an ordinary room

## Warm modern cozy living-room style
Rejected because:
- too clean
- too modern
- too “lifestyle interior”

## Basement / cracked / heavily worn room
Rejected because:
- too dilapidated
- user explicitly does NOT want basement misery / cracked-wall aesthetic

## Rich Korean room concept — temporarily chosen, later abandoned
Had:
- frontal 2D composition
- centered window + Seoul night
- low rectangular table
- 3-person floor seating
- left standing lamp
- right low cabinet + small plant/lamp
- right pegboard
- left neon LED text “수다맛집 오늘도 굿토크”
- ordinary Korean room feeling

Problem:
- too many props and fixed seats reduced reproducibility
- gray hoodie test physically mis-grounded the person

Therefore this richer room is **NOT the current production anchor**.

---

# 11. CURRENT SET DIRECTION — `TALKSHOW_SET_01_SIMPLE`

Current set should be even simpler.

## Core target
- straight-on frontal 2D view
- 16:9
- plain warm beige wall
- centered simple rectangular window
- very simple Seoul night skyline through the window
- one low rectangular wooden table
- simple wooden floor
- little or NO fixed seating in the EMPTY anchor image
- optional one small floor lamp only

## Explicit exclusions
- NO microphones
- NO neon sign for now
- NO pegboard
- NO cabinet unless later proven necessary
- NO plants
- NO shelves
- NO rug if avoidable
- NO decorative clutter
- NO professional studio look
- NO café / office / designer-room look

Intended feeling:
> **plain Korean small studio-apartment / livestream room, ordinary rather than stylish, where friends gather and talk**

Critical production idea:
> **The set anchor should be an EMPTY ROOM / EMPTY TABLE scene.**

Do not bake complicated fixed chairs or people into the set reference.
Characters should be added by the shot-generation prompt.

---

# 12. CURRENT SIMPLE SET PROMPT

```text
Create a very simple ordinary Korean studio-apartment room in a straight-on 2D view.

SET:
- plain warm beige wall
- one simple centered rectangular window
- very simple Seoul night skyline visible through the window
- one low rectangular wooden table centered in the foreground
- simple wooden floor
- little or no fixed seating in the empty-room anchor
- optionally one small floor lamp on one side only

Keep the room sparse, ordinary, and easy to reproduce.
It should feel like a casual Korean self-broadcast / livestream room, not a professional studio, café, office, or designer interior.

Do not add shelves, cabinets, plants, posters, pegboards, neon signs, microphones, rugs, decorative objects, or extra furniture.

Straight-on frontal composition.
Simple low-fi 2D webcomic style.
Flat muted colors, thick slightly imperfect outlines, minimal shading.
```

Note:
Earlier version included three floor cushions by default. After the physical-grounding failure, the stronger recommendation is that the EMPTY anchor contain little or no fixed seating.

---

# 13. CAMERA / SHOT SYSTEM — CURRENT DECISION

We considered:
- keeping all 3 characters in one view
- zooming in/out on each character

Current recommendation:
**Do NOT rely on AI-generated zoom/pan/tilt.**

Reasons:
- adds instability
- makes character/set continuity harder
- can increase “AI video” feel
- can be replaced safely in editing

Use separate fixed shots instead.

## MASTER SHOT
All 3 characters visible.

Minimal shot line:
```text
Create one straight-on 16:9 master shot with all three characters visible at the same time.
```

## SINGLE SHOT
One character visible.

Minimal shot line:
```text
Create one straight-on 16:9 single-character talk-show shot.
```

## REACTION SHOT
Optional one-character reaction shot.

Important prompt-budget decision:
> **Shot prompt is one line, not a large section.**

---

# 14. EARLIER 3-PERSON MASTER SHOT PROMPT

Historical reference; adjust to empty-room anchor next time.

```text
Use @Image1, @Image2, and @Image3 as the strict character references.
Use TALKSHOW_SET_01_SIMPLE as the strict room layout.

Create one straight-on 16:9 master shot with all three characters visible at the same time.

Seat the three characters naturally around the low rectangular table:
- one character on the left
- one character in the center
- one character on the right

All three characters must be clearly separated and physically grounded behind or around the table.
Do not place any character on top of the background, table, window, or other furniture.

Keep the camera fixed, frontal, and wide enough to show all three upper bodies clearly.

Preserve each character's exact identity, hairstyle, outfit, proportions, and low-fi webcomic drawing style.

No microphones.
No camera move.
No zoom.
No extra props.
No text.
No visual redesign.
```

Potential improvement only if needed after the simpler anchor:
- explicit floor/body contact language
- explicit table in foreground / seated bodies behind it

Do NOT add these extra constraints unless the simpler anchor still fails.

---

# 15. EARLIER SINGLE SHOT PROMPT

```text
Use @Image1 as the strict character reference.
Use TALKSHOW_SET_01_SIMPLE as the strict room reference.

Create one straight-on 16:9 single-character talk-show shot.

Show the same character seated naturally at the low table.
Frame from approximately waist/chest upward.

Keep enough of the room visible to clearly preserve the same location:
the beige wall, centered window with simple Seoul night skyline, and part of the same low wooden table.

Preserve the exact character identity and low-fi webcomic drawing style.

Camera fixed and frontal.
No zoom, pan, tilt, or camera movement.
No microphones.
No extra props.
No text.
No visual redesign.
```

---

# 16. PROMPT-BUDGET STRATEGY — IMPORTANT

TopView prompt limit provided by user:
**10,000 characters**

Concern:
Future prompt may need:
- base prompt
- character prompt(s)
- place prompt
- shot prompt
- script/action prompt

Current strategy:

## Do NOT make five giant blocks.
Use:
1. short shared style block
2. short per-character block(s)
3. short set block
4. ONE-LINE shot instruction
5. dialogue/action block as the main variable budget

Reference images should carry most visual information.

Compression does NOT mean blindly making prompts tiny. Remove duplicated wording but preserve behaviorally important constraints.

Earlier rule of thumb:
- do not compress 100 → 30 immediately
- reduce roughly 25–35% while preserving model behavior
- validate naturally during the next real generation instead of creating separate “prompt compression tests”

## Current compact base style block
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

---

# 17. REAL PRODUCTION STRATEGY FOR 30–60 SEC / ~3 MIN

## 30–60 sec
Likely final structure:
- short clips around 5–8 sec
- master shots + single shots + reaction shots
- 3 people alternate dialogue
- edit together later

## ~3 min
Possible later, but still an edited composition of many short shots.
Do NOT aim for a single 3-minute AI generation.

Possible long-form structure:
- short dialogue clips
- recurring fixed room
- fixed camera families
- reaction inserts
- post-edit transitions / digital crops if desired

---

# 18. CURRENT NEXT ACTION — DO THIS FIRST IN THE NEXT SESSION

## STEP 1 — FINALIZE ULTRA-SIMPLE EMPTY ROOM ANCHOR
Generate one image for **`TALKSHOW_SET_01_SIMPLE`**.

Target:
- straight-on frontal 16:9
- plain beige wall
- centered simple window
- simple Seoul night skyline
- low rectangular wooden table
- wooden floor
- little/no fixed seating
- optional one small floor lamp
- no other clutter

Do NOT optimize for prettiness.
Optimize for:
- clear depth
- enough horizontal space for 3 people
- compatibility with 2 or 4 people later
- easy reproducibility

## STEP 2 — ONE 3-PERSON MASTER SHOT
Use 3 character references + the empty-room anchor.

QC only:
1. Are all 3 people physically grounded?
2. Are they actually around/behind the table rather than pasted on the background?
3. Is the room/table geometry stable?
4. Are all 3 characters individually recognizable?
5. Is the composition usable as a real master shot?

If YES:
**PASS. Do not add more arbitrary set tests.**

## STEP 3 — SINGLE SHOTS
Create single-character speaking/reaction shots in the same room.

## STEP 4 — REAL EPISODE PRODUCTION
Move immediately to actual community-sourced 3-person dialogue.

---

# 19. QC PRIORITY ORDER

For future generations, inspect in this order:
1. physical grounding / impossible layering
2. character identity
3. drawing-style fidelity
4. set continuity
5. dialogue/action readability
6. anatomy / hands / small morphing
7. cost / efficiency

Do NOT fail a clip over tiny imperfections that will not matter in the actual short.

---

# 20. USER OPERATING PREFERENCE

The user wants:
- direct execution
- do as much as possible in one turn
- avoid repeated “want me to do X next?”
- avoid endless branching experiments
- identify the real bottleneck and test only that
- if something is good enough, move forward

Do NOT respond with one tiny step when the whole next sequence can be handled at once.

---

# 21. NEXT-SESSION START COMMAND

Use this exact instruction with this handoff:

> Use this handoff as the authoritative state. Do not re-plan the talkshow project. Continue immediately from `TALKSHOW_SET_01_SIMPLE`. First finalize the ultra-simple empty-room anchor, then prepare one 3-character master-shot prompt using three existing character sheets. Prioritize physical grounding and reproducibility over decoration. If the master shot passes, move directly to single shots and real community-based dialogue rather than adding more tests.

---

# 22. GITHUB / PERSISTENCE

Canonical repository is now confirmed as:
**`noru358/talkshow`**

Default branch:
**`main`**

At every future handoff:
1. update `CURRENT_STATE.md`
2. update `NEW_SESSION_HANDOFF.md`
3. preserve exact reusable prompt blocks and important successful prompt examples
4. update any changed workflow docs if necessary
5. push to `noru358/talkshow`
6. verify the remote file/commit before reporting handoff complete

Do NOT fall back to the old `noru358/-` name now that `noru358/talkshow` is confirmed.

---

# 23. NON-NEGOTIABLE CONTINUITY RULE

A future handoff must NOT be a short summary only.
It must preserve:
- current phase
- all meaningful decisions
- exact latest/reusable prompt blocks
- known character descriptions/status
- set specification
- important QC failures and why
- community-source/dialogue examples used
- next exact action
- GitHub persistence state

This file is the authoritative continuity document.
