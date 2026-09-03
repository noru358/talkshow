# CURRENT STATE

Updated: 2026-09-04 KST
Status: **V2 BASELINE ESTABLISHED — FIRST COMPLETE EPISODE P002 STORYBOARD READY / OPENING STILL IS NEXT**

## 지금의 단일 결론

P001 Scene B를 또 하나의 격리된 파일럿으로 생성하는 작업은 현재 active next action이 아니다.

사용자 판단대로 이제 테스트를 위한 테스트를 중단하고, 실제 공개 가능한 짧은 완성본을 만드는 과정에서 동시에 visual / voice / reaction / editing grammar를 검증한다.

현재 권위 문서:
- V2 series baseline: `SERIES_V2_RELOCK.md`
- P002 source provenance: `episodes/P002/SOURCE_PACK.md`
- P002 complete storyboard: `episodes/P002/FULL_EPISODE_PACKAGE.md`

## 큰 파이프라인

`Radar/Source → Thread/Gold → Episode Package → User Production → Defect QC → Distribution/Performance Learning`

콘텐츠 원천성/성과 루프는 유지한다.

## V2 recurring direction

### Cast
- LEFT: CHAR_B / white-T-shirt woman
- CENTER: CHAR_06
- RIGHT: recurring male identity

Selected free voice references:
- LEFT: Gaeun outdoors
- CENTER: Harin
- RIGHT: Taemin

### Set pool
1. `SET_A_HOME` — main/default
2. `SET_B_CONVENIENCE` — signature/high-energy
3. `SET_C_HANGANG` — variation/special
4. `SET_D_ROOFTOP` — variation/special

### Reaction grammar
V2 is intentionally more visible and energetic than V1.

Allowed/desired when causally motivated:
- readable eye changes and head turns
- visible facial reactions
- short torso lean/recoil
- shoulder bounce
- one/two-hand gestures
- open-palmed disbelief
- compact celebratory fist

Avoid simultaneous mass reaction, constant gesturing, full-body flailing and anatomy deformation.

## Important first-frame clarification — NEW

The fixed first frame is the literal visual start of **each generated AI clip**.

It is NOT a rule that the finished episode must always begin from one universal resting cast pose.

New real-episode architecture:

> **canonical cast still → minimum shot-specific derived first-frame stills → fixed-first-frame I2V clips → editorial hard cuts / crop / punch-in**

If a clip must start with CENTER already holding a smartphone, create one canon-derived opening still with only that starting state changed. Do not waste video time asking the model to invent the phone and perform a long reach from the neutral master.

Do not automatically chain the last frame of Clip 1 into Clip 2; that can compound drift. Prefer a hard cut between canon-derived states unless continuous physical action actually requires last-frame chaining.

## Current active visual authority

For P002, use the user-supplied 2026-09-04 convenience-store-front three-person image as the active exact visual authority.

It controls what is visibly present in this episode: faces, clothing, drawing style, seating, table, props and set geometry.

If older prose in the repository conflicts with this current locked image, do not force the stale prose back onto the image for P002.

## Repository integrity finding

During the 2026-09-04 GitHub inspection, the repository contained text claiming that `assets/V2_VISUAL_LOCK_20260904.md` and canonical binaries under `assets/v2_locked/` had been preserved, but those paths were not found on the inspected `main` tree.

Therefore:
- do not claim those visual binaries are safely mirrored in GitHub;
- the current convenience image is an external/session visual authority until a binary upload path is actually completed;
- this discrepancy is now explicitly recorded rather than hidden by stale handoff prose.

## P001 status

Preserve P001 as historical evidence.

- source: `episodes/P001/SOURCE_PACK.md`
- V1 Scene A lock remains evidence
- V1 Scene B package remains evidence
- V2 Omni reference pilot package remains prepared evidence
- **do not spend credits on the P001 Omni pilot as the current next step**

## P002 — first complete episode

Source/storyboard agent selected a real Korean community source about AI-era entry-level developer hiring.

Source pack:
- `episodes/P002/SOURCE_PACK.md`

Complete production concept:
- about 16 sec total
- 2 x 8 sec Seedance clips
- SET_B_CONVENIENCE visual authority
- Clip 1 integrates the topic-opening device rather than adding a separate formal intro clip
- Clip 2 delivers the later source reactions
- 16:9 generation master → 9:16 editorial distribution master
- subtitles/localization added in post, not baked into AI generation

### Opening device
Use the CENTER character + smartphone as a recurring internet-source device, but avoid formal canned hosting such as `오늘의 주제!` by default.

Preferred behavior:
- visual routine repeats
- spoken hook varies naturally: `야 이거 봐`, `이거 봤어?`, or direct source claim

This gets to the content faster and feels more like friends talking than a TV host segment.

## 바로 다음 행동

### Step 1 — create `P002_OPENING_STILL`
From the user's current convenience image:
- change only CENTER's starting pose so she already holds a plain smartphone at chest height and looks at it;
- no readable screen text;
- preserve every other character, face, outfit, prop, table, chair, set element, composition and drawing style.

### Step 2 — generate P002 Clip 1 once
- Seedance 2.0 Mini
- 480p
- 16:9
- 8 sec
- generation count exactly 1
- use the selected voice references if the active TopView route supports them cleanly
- QC this as actual production footage, not a pilot

### Step 3 — if no hard blocker, generate Clip 2 once
Use the original convenience cast still / canon-derived neutral state as the new first frame and make an intentional editorial cut.

### Step 4 — assemble publishable 9:16 master
- editorial punch-ins instead of AI camera moves
- Korean/English subtitle treatment in post
- no explanatory outro
- publish → 24h / 7d performance learning

## Mandatory pre-generation inheritance check

Before presenting or submitting any scene prompt:
- active episode image is the visual authority
- voice-reference speaker mapping is explicit
- V2 reaction rules are translated into visible scene-specific actions
- first frame matches the first visible action of that clip
- no superseded V1 phrases such as `subtle acting`, `small reactions`, or blanket `no large gestures`
- model / resolution / duration / generation count match the approved task
- no unnecessary extra pilot or reference test is inserted before the publishable episode

## 응답 규칙

모든 talkshow 응답은 다음으로 시작한다.
1. 큰 흐름
2. 현재 세부 단계
3. 이번 턴 완료조건
