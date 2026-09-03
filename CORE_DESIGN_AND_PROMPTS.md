# TALKSHOW — CORE DESIGN & PROMPT LIBRARY

**Status:** AUTHORITATIVE prompt and production-grammar library
**Updated:** 2026-09-03 KST

This file exists to prevent loss of the project's **core design decisions, production grammar, prompt blocks, character constraints, set logic, and validated QC lessons** across sessions.

Repository authority order is defined only in `README.md`. This file is authoritative for reusable visual, voice and prompt grammar; `CURRENT_STATE.md` and the active episode package control the current action.

---

# 1. PROJECT CORE

Final product:
- Korean internet/community-source talkshow
- usually 3 characters, but 2 or 4 may appear
- content-driven short-form: usually 15–22 sec for one strong comment chain; 22–35 sec only when the source has enough real beats
- possible later ~3 min format
- final episodes are assembled from multiple short AI video clips; do **not** generate 30–180 sec as one continuous AI clip

Content principle:
- real Korean community posts/comments are the primary source material
- AI should lightly transform/recombine human-written wording rather than invent bland generic dialogue
- character functions change beat-by-beat: speaker / reaction / deadpan / disbelief / fact-check / nonsense / laugh amplification etc.
- no permanently fixed boke/tsukkomi roles
- social reaction is often as important as the literal line

Desired feel:
- friends talking casually in an ordinary Korean room / livestream-like environment
- NOT polished TV studio
- NOT podcast studio
- NOT designer café / office / lifestyle interior

---

# 2. CURRENT PRODUCTION ARCHITECTURE — LOCKED

The accepted reproducibility architecture is:

> **SET_MASTER_01 → episode/cast-specific CAST_MASTER → I2V from the fixed cast-master first frame → edit/crop**

## 2.1 SET_MASTER_01
Reusable global room anchor.

Locked direction:
- straight-on frontal 2D composition
- 16:9
- plain warm beige wall
- simple wooden floor
- one low rectangular wooden table in foreground
- one small centered rectangular window
- minimal simplified Seoul night skyline through window
- little/no fixed seating baked into empty set
- no microphones
- no neon sign
- no pegboard
- no shelves
- no plants
- no rug
- no cabinet unless later concretely required
- no decorative clutter

Reason:
- richer room references caused physical grounding failures and character/furniture conflicts
- simplicity improved reproducibility materially

## 2.2 CAST_MASTER_xxx
For each episode or cast combination, create one canonical first-frame still from `SET_MASTER_01` + selected character sheets.

The cast master locks:
- room
- table geometry
- camera/composition
- left/center/right position
- character identities
- drawing style

Characters are NOT permanently tied to left/center/right. Seat assignment is episode-specific.

## 2.3 I2V
Reuse the exact same cast-master still as the I2V first frame for multiple clips in that episode.

Video prompt should focus primarily on:
- preserve first frame
- dialogue
- subtle acting/reactions
- no redesign / no camera movement

Do not re-describe the entire room and all character visual details in every video prompt unless a repeated failure proves it necessary.

## 2.4 Shot policy
Default:
- 3-person fixed frontal MASTER
- editorial crop/punch-in in post

Only if a real beat requires it:
- dedicated SINGLE / REACTION anchor

Do NOT pre-generate a full single-shot family by default. That was judged excessive because it increases cost, prompt load, and continuity drift.

Avoid AI-generated zoom/pan/tilt for now. Fixed camera is the production baseline.

---

# 3. MODEL / GENERATION BASELINE

Default video model:
- **Seedance 2.0 Mini**

Validation baseline:
- 480p
- 16:9
- short clips, usually 7–12 sec
- prefer 2 dense scenes per simple comment-chain episode; do not split one thin source into six clips

Do not mutilate natural dialogue merely to fit 5 sec.

Current manual workflow:
1. ChatGPT writes the exact final prompt.
2. User manually pastes references + prompt into TopView.
3. User generates once.
4. User uploads result.
5. ChatGPT QC.
6. Move forward unless there is a real blocker.

Automation / Work-mode prompt rewriting remains paused unless user explicitly reopens it.
Reason: prior automated rewriting hallucinated incorrect character details and degraded fidelity.

---

# 4. GLOBAL VISUAL STYLE LOCK

Character sheets are the main visual authority.

Target:
- simple low-fi 2D webcomic
- thick slightly imperfect black outlines
- flat muted colors
- minimal shading
- simple cheap-cute / slightly clumsy proportions
- modest visual detail
- intentional hand-drawn irregularity

Avoid:
- generic GPT illustration polish
- polished anime
- polished Korean webtoon rendering
- realism / semi-realism
- glossy render
- cinematic lighting
- detailed textures
- elegant thin linework
- beautification / modernization

Reference rule:
> Use the provided reference sheet as the strict character and style reference, but do not reproduce the sheet layout itself. Create a new single scene in the same design language.

The sheet controls DESIGN + STYLE. Do not animate/reproduce the character-sheet grid itself.

---

# 5. CHARACTER CONSTRAINTS CURRENTLY USED IN VALIDATED 3-PERSON CAST

## CHAR_06
- young woman
- long wavy dark hair with bangs
- large round eyes
- light beige cardigan/top
- dark wide-leg pants
- white sneakers if visible
- **NO GLASSES / NO EYEWEAR**
- low-fi 2D webcomic style

Historical note: unwanted round glasses were hallucinated in a prior automated prompt. Therefore `NO GLASSES` is a critical identity constraint.

## White T-shirt woman / CHAR_B
- young woman
- straight medium-length light-brown bob
- large round eyes
- plain white fitted short-sleeve T-shirt
- light-blue high-waist jeans
- white sneakers
- **NO GLASSES**
- simple soft proportions

## Gray-hoodie male
- young man
- messy short black hair
- large round eyes
- gray hoodie
- loose/dark black pants
- white sneakers
- **NO GLASSES**
- boyish/simple proportions

## Other previously provided characters
### Long-haired black-top woman
- long wavy brown hair
- black long-sleeve top
- dark gray long skirt
- black shoes
- calmer/composed impression

### Black-jacket male
- short black hair
- sleepy / half-lidded eyes
- black jacket over dark shirt
- light beige pants
- black sneakers
- dry/deadpan impression

General rule: do not run isolated character tests merely for completeness. Generate only what real production needs.

---

# 6. CORE PROMPT BLOCKS

## 6.1 Compact global style block
```text
Use the provided character reference as the strict character and drawing-style authority.

Match the same low-fi 2D webcomic style: thick slightly imperfect black outlines, flat muted colors, minimal shading, simple cheap-cute proportions.

Do not beautify, polish, modernize or redesign the character. Avoid polished anime/webtoon rendering, realism, glossy/cinematic lighting, and added visual detail.
```

## 6.2 Compact set block
```text
Use the provided set reference as the strict room/layout authority.

Preserve the same simple straight-on Korean room: plain warm beige wall, centered simple window with a minimal Seoul night skyline, low rectangular wooden table, and simple wooden floor.

Keep the set sparse and physically readable. Do not add or redesign major furniture, decorations, microphones, shelves, plants, rugs, pegboards, neon signs, or extra props.
```

## 6.3 Character mini-prompts
### Gray hoodie male
```text
Preserve this exact character: young man, messy short black hair, large round eyes, light gray hoodie, loose black pants, white sneakers, simple boyish proportions, no glasses.
```

### White T-shirt woman
```text
Preserve this exact character: young woman, straight medium-length light brown bob hair, large round eyes, plain white short-sleeve T-shirt, light blue high-waist jeans, white sneakers, simple soft proportions, no glasses.
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

# 7. EXACT SET_MASTER_01 PROMPT

Use this when a new clean global set anchor must be regenerated.

```text
Create one clean 16:9 empty-room reference image for a recurring casual talkshow.

This image will be reused as the strict SET MASTER for many future episodes, so reproducibility and simple geometry are the highest priorities.

Create a straight-on frontal 2D view of a very simple ordinary Korean room.

ROOM:
- plain warm beige wall
- simple wooden floor
- one low rectangular wooden table centered in the foreground
- one small simple rectangular window centered on the back wall
- through the window, show only a very minimal simplified Seoul night skyline
- no people
- no chairs or fixed seating
- no microphones
- no shelves
- no plants
- no posters
- no neon signs
- no rugs
- no cabinets
- no decorative clutter
- no extra furniture

The room should feel ordinary and slightly modest, like a casual Korean livestream room where friends gather, not a professional studio, café, office, or stylish designer interior.

Keep the spatial geometry extremely clear:
- flat back wall
- clearly readable floor
- table clearly in the foreground
- open empty space behind and around the table for 2–4 seated characters

Simple low-fi 2D webcomic drawing style:
thick slightly imperfect black outlines, flat muted colors, minimal shading, modest detail.

Do not make the room polished, cinematic, realistic, glossy, or highly decorated.

No text.
No logo.
No watermark.
No character.
One single scene only.
```

---

# 8. EXACT CAST_MASTER TEMPLATE — CURRENT VALIDATED CAST EXAMPLE

Reference mapping for this example:
- `@Image1` = SET_MASTER_01
- `@Image2` = white T-shirt woman
- `@Image3` = CHAR_06
- `@Image4` = gray-hoodie male

```text
@Image1 @Image2 @Image3 @Image4

Use Image1 as the strict room, camera, table, and composition reference.
Preserve the exact same room layout and drawing style.

Use Images2–4 only as strict character identity references.

Create one clean 16:9 three-character master still.

STRICT CHARACTER PLACEMENT:
- LEFT = Image2, young woman with straight medium-length light-brown bob hair, plain fitted white short-sleeve T-shirt and light-blue jeans
- CENTER = Image3, CHAR_06, young woman with long wavy dark hair with bangs and light beige top
- RIGHT = Image4, young man with messy short black hair and gray hoodie

CRITICAL:
- NO GLASSES on any character
- do not swap the characters
- do not swap left / center / right positions
- preserve each character's exact hairstyle, outfit, face design, proportions, and low-fi drawing style

All three characters are seated naturally behind and around the low table.

Keep the exact same:
- beige wall
- wooden floor
- centered small window
- minimal Seoul night skyline
- low wooden table
- straight-on frontal camera

The characters must be clearly separated and physically grounded in the room.
The table is clearly in front of their lower bodies.
Do not place anyone floating, pasted onto the wall, or sitting on top of the background.

Give the three characters slightly different natural resting postures:
- LEFT slightly turned toward the center
- CENTER mostly frontal
- RIGHT relaxed and slightly angled toward the others

Do not add microphones or props.
Do not redesign the room.
Do not add furniture or decorations.

Simple low-fi 2D webcomic style:
thick slightly imperfect black outlines, flat muted colors, minimal shading, simple cheap-cute proportions.

No text.
No subtitles.
No logo.
No watermark.
No collage.
One single scene only.
```

For another cast, preserve this template but replace only the character-reference mapping and placement lines.

---

# 9. EXACT BASELINE I2V PROMPT — CAST MASTER REUSE

```text
Preserve the exact first-frame character identities, left-center-right positions, room, table, drawing style, and composition throughout the entire clip.

Fixed frontal camera.
No camera movement and no scene change.

The three characters have a casual Korean conversation.
Keep them naturally alive, not frozen.
When one person speaks, the other two subtly listen and react with small eye movements, slight head turns, brief smiles, or tiny laugh reactions.
No exaggerated gestures.

Korean dialogue:

CENTER:
"373년 묵은 암호를 AI가 풀었대."

LEFT:
"근데 첫댓이 '좆도 쓸모 없는 거구만' ㅋㅋ"

RIGHT:
"ㅋㅋㅋ 틀린 말은 아니야"

Acting:
- CENTER delivers the first line casually and matter-of-factly.
- LEFT looks amused and gives a small laugh while delivering the second line.
- RIGHT reacts dryly with a faint laugh on the third line.
- During each line, the other two visibly listen and give subtle reactions.

Keep everyone seated in the exact same positions.
No glasses.
No redesign.
No new props.
No subtitles.
No on-screen text.
```

---

# 10. CURRENT I2V MICRO-CONTROLS FROM LATEST QC

Latest validated clips showed:
- one clip more stable but with minor mouth stiffness
- another more lively but with slight closed-eye smile deformation

Keep these reusable control lines available:

```text
Keep eye shapes anatomically clean and stable during smiling and blinking.
Avoid distorted closed-eye shapes.
```

```text
Reactions should be slightly staggered and natural, not simultaneous.
```

```text
Use restrained, natural Korean lip movement.
Avoid overly wide or exaggerated mouth shapes.
```

These are local quality controls, NOT a reason to reopen pipeline testing.

---

# 11. EARLIER SUCCESSFUL CHAR_06 LONG PROMPT — HISTORICAL BASELINE

This manually entered prompt produced one of the useful passable CHAR_06 results (`260902_0019_video_edit_1279.mp4`). Preserve it because it proves which style/identity constraints mattered.

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

Historical note: microphones/iPad/professional studio are no longer part of the current set concept. This prompt is kept for its character/style-control lessons, not as the current set template.

---

# 12. KNOWN FAILURE HISTORY / DO NOT REPEAT

## Rich room failure
A richer Korean room with fixed furniture, chairs, props, pegboard/neon/decor caused:
- pasted-on character appearance
- bad person/table/floor depth relationship
- seating conflict
- lower reproducibility

Decision: simplify actual geometry rather than adding more prose.

## Automated prompt rewriting failure
Automated Work-mode rewriting introduced incorrect character details including glasses on CHAR_06.
Decision: manual exact prompts are authoritative.

## Direct character-sheet I2V failure
Animating the master-sheet grid directly can make the sheet/grid itself behave as the scene.
Preferred principle: character sheet → clean scene/cast still → I2V.

## Over-designed shot library
Pre-generating master + every character single/reaction was judged wasteful.
Use master heavily and only generate missing close/reaction assets when a real edit proves the need.

---

# 13. QC PRIORITY ORDER

Current practical order:
1. physical grounding / impossible layering
2. character identity, including no unwanted glasses
3. correct left/center/right assignment
4. drawing-style fidelity
5. set continuity/reproducibility
6. dialogue/action readability and social reaction
7. anatomy / hands / small morphing
8. cost / efficiency

Do not reject a production clip over tiny imperfections that are not noticeable in the final short.

---

# 14. PROMPT-BUDGET RULE

TopView prompt limit previously noted: ~10,000 characters.

Do not use five giant duplicated prompt modules.
Prefer:
1. reference images carry visual identity
2. short style block
3. short set/position block when needed
4. one-line shot instruction
5. dialogue/action block as main variable content

After a CAST_MASTER is locked, video prompts should become especially short because the first frame already encodes character, room, layout, and style.

---

# 15. CONTINUITY / SESSION RULE

For every talkshow response, begin with:
1. **큰 흐름**
2. **현재 세부 단계**
3. **이번 턴 완료조건**

Do not ask permission for obvious next actions.
Do not end with `원하면 ~해주겠다` when the next work is clear.
Do as much as possible in one turn.

At session handoff, update GitHub before claiming completion.

---

# 16. CURRENT STATE POINTER

This file stores the stable **core design and prompt grammar**.
For the exact active episode / next action, always read:
- `CURRENT_STATE.md`
- current episode package under `episodes/<ID>/`

As of this file's update, `CURRENT_STATE.md` indicates the project has entered real episode production and points to the active P001 production package.


---

# 17. VALIDATED PILOT OPERATING RULES — 2026-09-03

## 17.1 Agent / human split

The intended logical workflow is:

> RADAR/SOURCE INGEST → THREAD RECONSTRUCTION → GOLD EXTRACTION → LIGHT ADAPTATION/CASTING → BEAT·SHOT·PROMPT PACKAGE → USER MANUAL GENERATION/EDIT → DEFECT QC/ARCHIVE

These are logical roles, not proof that independent agents are already implemented. Current pilot execution combines the upstream roles in ChatGPT; the user manually generates, selects, edits, and publishes.

Automate upstream first: detection, source preservation, comment-tree extraction, GOLD candidate tagging, and package drafting. Keep premise selection, final GOLD choice, TopView generation, clip choice, and final edit manual during the pilot.

The current role map, source gate and performance loop are maintained in `PRODUCTION_PIPELINE.md`.

## 17.2 Validated input stack

`260903_0001_video_edit_2387.mp4` proved this input stack can produce a stable scene:
- locked 3-person cast-master still
- the same three character master packs
- one exact dialogue/acting prompt

Do not add extra set references or shot-family assets unless a real failure requires them.

## 17.3 Content-driven duration

- one strong comment chain: 15–22 sec, normally 2 scenes
- richer source with multiple genuine GOLD beats: 22–35 sec
- never pad with explanation, lesson, repeated reaction, or outro
- do not treat 30–60 sec as a quota

## 17.4 Causal reaction timing

```text
Do not anticipate the joke.
Keep the listener completely neutral until the trigger phrase is actually spoken.
Begin the reaction only after hearing the trigger phrase.
Reactions must be staggered and causally timed, never simultaneous.
```

The order should read as trigger → first listener reaction → second listener reaction. A character must not smile early merely because the model knows the next line.

## 17.5 Visual variety without reopening the shot system

Default remains the fixed 3-person master plus post-production crops. Allow at most one episode-specific explanatory card or cutaway when the premise cannot be understood quickly without it. Do not create decorative B-roll or new backgrounds for every beat.

# 18. VOICE IDENTITY LOCK — 2026-09-03

Seedance native speech is a performance/lip-sync guide, not the final recurring identity.

Locked pilot method:
1. Keep spoken dialogue in I2V prompts.
2. Split the generated audio by speaker.
3. Convert each segment with ElevenLabs Voice Changer multilingual model to a fixed character voice ID.
4. Preserve original timing, delivery and emotion.
5. Use fixed-ID TTS only for a segment that cannot be cleanly converted.
6. Replace Scene A audio in the final edit; do not regenerate Scene A picture.

Voice slots are maintained in `assets/VOICE_REGISTRY.md`.

| Character | Fixed profile | voice_id |
|---|---|---|
| CHAR_06 / center woman | Korean young adult woman; calm, matter-of-fact, medium-low pitch, moderate tempo, low theatricality | UNASSIGNED — required before P001 publish |
| White T-shirt woman / CHAR_B | Korean young adult woman; brighter and slightly faster; skeptical edge; crisp consonants; not cute/anime | UNASSIGNED — required before P001 publish |
| Gray-hoodie male | Korean young adult man; dry low-mid register; restrained laugh; slightly lazy cadence; not announcer-like | UNASSIGNED — required before P001 publish |

Once assigned, voice IDs do not change by episode. Voice-ID assignment blocks publishing, not Scene B picture generation.

# 19. ASPECT-RATIO LOCK — 2026-09-03

- Generation master remains 16:9 because the validated 3-person cast-master and physical grounding depend on it.
- Distribution master is 9:16.
- Do not merely shrink the 16:9 frame with permanent black letterbox bars.
- Build a vertical edit using speaker crop/punch-in, a top hook zone and a bottom subtitle-safe zone.
- Do not regenerate the set or cast master for P001.

# 20. PROVENANCE / PERFORMANCE CONTROLS — 2026-09-03

- AI-written spoken beats must be ≤30%; source-summary setup counts.
- AI-original comedic payoff defaults to 0%.
- Remove a bridge before rewriting human GOLD.
- Reject a source before storyboard when it needs >30% AI connective dialogue or has fewer than two strong human beats.
- Post-publication performance feeds source/GOLD/hook hypotheses, never automatic smoothing of dialogue.
