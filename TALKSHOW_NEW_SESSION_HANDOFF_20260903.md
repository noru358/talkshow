# TALKSHOW — NEW SESSION HANDOFF

**Last updated:** 2026-09-03

## 0. ABSOLUTE CURRENT STAGE

**PHASE 1 — CHAR_06 single-character production lock**

Current operating mode:
**MANUAL PROMPT WORKFLOW ONLY**

Do NOT jump to:
- other characters
- 3-character pilot
- real community episode production
- automation / Work execution pipeline

First finish CHAR_06.

---

## 1. IMPORTANT LATEST DECISION

The attempted automation / Work-mode execution pipeline degraded quality and is PAUSED.

### DO NOT USE for now
- Work-generated rewritten prompts
- autonomous prompt summarization / rewriting
- Work execution packages as the production path
- automatic reference selection
- automatic TopView execution

### USE THIS WORKFLOW INSTEAD

1. User asks for next image/video scene.
2. ChatGPT writes the **final exact TopView prompt** manually.
3. User manually uploads the reference(s) and prompt to TopView.
4. User generates the image/video.
5. User uploads the result back to ChatGPT.
6. ChatGPT performs QC and writes the next exact prompt.

This manual loop previously produced materially better style fidelity.

---

## 2. CURRENT GOAL

Lock CHAR_06 so that:
- the exact low-fi drawing language survives generation
- identity remains stable
- no generic GPT-image polish appears
- motion/action can be introduced without large style drift

Only after this is proven should the same structure be replicated to other main characters.

---

## 3. CHAR_06 CANONICAL VISUAL AUTHORITY

Primary master sheet:
`CHAR06_MASTER_SHEET.png`

The current master sheet contains multiple full-body / seated / bust / expression examples and is the main visual authority.

Canonical identity / style:
- young woman
- long wavy dark hair with bangs
- large round eyes
- NO glasses / eyewear
- light beige cardigan / top
- dark wide-leg pants
- white sneakers
- simple low-fi 2D webcomic
- thick black outlines
- flat muted colors
- minimal shading
- slightly rough / clumsy cheap-cute proportions
- master sheet = maximum visual complexity

Never beautify or redraw into:
- generic GPT illustration
- polished anime
- detailed webtoon
- realistic / glossy render
- cinematic lighting

---

## 4. IMPORTANT FINDINGS SO FAR

### A. Seedance model choice
Default model:
**Seedance 2.0 Mini**

Reason:
- user selected Mini after A/B against Seedance 2.5
- cheaper and acceptable when prompting/reference handling is correct

Default validation settings:
- 480p
- short 4–5 sec clips
- 16:9 for current tests

### B. Style drift is the #1 QC priority
QC order:
1. exact style fidelity to master sheet
2. identity consistency
3. beat / action readability
4. props / set stability
5. morphing / anatomy
6. cost efficiency

### C. Previous successful-ish manual runs
When the user manually entered detailed prompts into TopView, results were much better than the later automated Work-mode run.

### D. Automated Work-mode failure
One Work-generated prompt incorrectly described CHAR_06 as having **round glasses** even though glasses are explicitly forbidden.

This proved that Work did not inherit the full canonical context reliably and rewrote the character incorrectly.

### E. Multiple cropped references may also be risky
A run using the master sheet plus multiple cropped references showed much stronger style drift than earlier master-sheet-oriented manual runs.

This is NOT fully isolated scientifically because Work also rewrote the prompt at the same time.

Current practical policy:
- prefer the master sheet as the main authority
- do not flood the model with many cropped refs
- only add a very specific auxiliary reference if a repeated production failure proves it is needed

### F. Master sheet used directly as I2V first frame can fail conceptually
Latest `Video Draft.mp4` behaved like the **master sheet/grid itself was being animated**, rather than generating one clean talk-show shot.

Therefore the preferred production flow is now:

`MASTER SHEET → generate a clean scene still → animate that still with I2V`

rather than directly animating the character-sheet grid.

This is a key current production hypothesis / practical direction.

---

## 5. LATEST QC RESULTS

### `260902_0014_video_edit_3311.mp4`
Overall: usable direction, but not lock-ready.
- style mostly acceptable
- some neck / shoulder / hand detail ambiguity
- too many performance beats in a short clip increased local anatomy instability

### `260902_0018_image_to_video_2015.mp4`
Overall: FAIL.
Problems:
- major style drift
- generic cleaner AI illustration look
- glasses appeared
- identity reinterpreted

Important confound:
- Work rewrote the prompt incorrectly
- multiple cropped refs were also used

### `Video Draft.mp4`
Overall: FAIL as a production method.
Problem:
- master sheet itself behaved like the animated frame / storyboard grid
- not a clean single talk-show scene

Conclusion:
**Do not directly animate the master-sheet grid as the actual first frame.**

---

## 6. CURRENT PRODUCTION WORKFLOW TO USE NEXT SESSION

### STEP 1 — Scene still generation
Use the CHAR_06 master sheet as the character/style reference.
Generate ONE clean 16:9 talk-show scene still.

Requirements:
- single CHAR_06
- simple desk
- tabletop mic
- simple studio
- seated medium shot
- exact low-fi master-sheet drawing language
- no text / subtitles / logos
- no glasses

### STEP 2 — User selects / uploads the generated still
Do not automatically accept a still if style drift is obvious.

### STEP 3 — I2V
Use the selected clean scene still as the I2V first frame.

ChatGPT provides ONE final prompt manually.
User enters it in TopView manually.

### STEP 4 — QC
User uploads result.
ChatGPT checks:
- style
- identity
- neck/shoulder continuity
- hands
- mic/desk stability
- action readability

### STEP 5 — Repeat only as needed
Do not create arbitrary experiments.
Only test what is necessary to reach a production-ready CHAR_06 lock.

---

## 7. NEXT EXACT ACTION

At the start of the next session:

1. Do NOT re-plan the whole project.
2. Confirm current stage at the top of the response:
   `[현재 단계: PHASE 1 — CHAR_06 단독 LOCK / 수동 프롬프트 방식]`
3. Continue with the **scene-still-first** workflow.
4. Provide the user with:
   - one exact TopView image-generation prompt for a clean CHAR_06 16:9 seated talk-show still
   - after user returns the still, one exact 5-second Seedance 2.0 Mini I2V prompt
5. Do not suggest Work automation unless the user explicitly reopens that topic.

---

## 8. USER OPERATING PREFERENCE

The user wants direct execution-oriented guidance.
Avoid endless experimental branches.
If a production path is already good enough, move forward rather than testing for testing's sake.

User explicitly decided:
> “자동화 때려치자. 걍 네가 프롬프트 주고, 내가 그거 탑뷰에 올리는 방식으로 하자.”

Treat this as the current authoritative workflow decision.

---

## 9. MAIN PROJECT ARCHITECTURE LATER (DO NOT EXECUTE YET)

After CHAR_06 production lock:
- replicate compact lock structure to other main characters
- build 5-character production-ready pool
- ingest real community posts/comments
- transform lightly rather than invent bland AI dialogue
- select 3/5 characters per episode dynamically
- generate real 3-character talk-show pilot
- later support both 9:16 and 16:9 as separate renders

But none of this should happen before CHAR_06 is locked.



---

# GitHub persistence protocol (MANDATORY at every session handoff)

Canonical repository: `noru358/-` (public). The repository may later be renamed to `noru358/talkshow`; check `talkshow` first and fall back to `-`.

Every time the user asks to move to a new session or says to prepare a handoff, do ALL of the following before saying the handoff is complete:

1. Update `CURRENT_STATE.md` with the exact current phase, latest decisions, failures, locks, and next action.
2. Update `NEW_SESSION_HANDOFF.md` with the same authoritative state plus first action for the next session.
3. Update any changed project docs/assets manifests/prompts/QC notes that are part of the canonical workflow.
4. Check Git status and verify the intended files are tracked.
5. Commit with a descriptive message, e.g. `handoff: update talkshow state 2026-09-03`.
6. Push to the current working branch on `origin`.
7. Verify the remote push succeeded (do not merely assume).
8. Only after successful verification say that the next-session handoff is complete.

If GitHub write access/tooling is unavailable in the current mode/session, explicitly mark this as a REAL BLOCKER and provide the exact commands below for the user/Work mode to execute. Do not silently skip GitHub persistence.

## Standard Git commands
```bash
git status
git add CURRENT_STATE.md NEW_SESSION_HANDOFF.md .
git commit -m "handoff: update talkshow state 2026-09-03"
git push origin HEAD
```

If the repo is not already cloned on the machine:
```bash
git clone https://github.com/noru358/-.git talkshow
cd talkshow
```

If authentication is required, use the existing GitHub CLI/account setup rather than creating a duplicate repo.

## Handoff completion gate
A handoff is NOT complete unless both are true:
- local handoff/state files are updated
- GitHub push is verified, OR an explicit blocker is recorded with exact commands to finish it

---
