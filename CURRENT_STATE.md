# CURRENT STATE

Updated: 2026-09-04 KST
Status: **V2 BASELINE ESTABLISHED — P002 IN REAL PRODUCTION / 4-SECOND VOICE REFERENCES REQUIRED**

## 지금의 단일 결론

P001 Scene B를 또 하나의 격리된 파일럿으로 생성하는 작업은 현재 active next action이 아니다.

사용자 판단대로 이제 테스트를 위한 테스트를 중단하고, 실제 공개 가능한 짧은 완성본을 만드는 과정에서 동시에 visual / voice / reaction / editing grammar를 검증한다.

현재 권위 문서:
- V2 series baseline: `SERIES_V2_RELOCK.md`
- P002 source provenance: `episodes/P002/SOURCE_PACK.md`
- P002 complete storyboard: `episodes/P002/FULL_EPISODE_PACKAGE.md`
- voice runtime constraint: `assets/VOICE_REFERENCE_RUNTIME_RULES.md`

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

### Voice-reference runtime lock — NEW
TopView / Seedance 2.0 Mini R2V rejected a request because total attached audio-reference duration exceeded **15.2 sec**. Credits were refunded.

New production rule:
- create one clean **~4.0 sec** recurring audio reference per character
- three 4-sec references total about 12 sec and fit below the observed 15.2-sec ceiling
- attach only the references for characters who actually speak in that clip whenever possible
- silent characters do not need an audio reference and must be explicitly marked silent/no lip-sync in the prompt
- do not attach the three full-length catalog preview files by default

Authority: `assets/VOICE_REFERENCE_RUNTIME_RULES.md`

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

## Important first-frame clarification

The fixed first frame is the literal visual start of **each generated AI clip**.

It is NOT a rule that the finished episode must always begin from one universal resting cast pose.

Real-episode architecture:

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
- this discrepancy is explicitly recorded rather than hidden by stale handoff prose.

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

Current production concept:
- two generated clips
- current generation duration target: **10 sec + 10 sec**, because dialogue + staggered social reactions need more room than the previous 8-sec test assumption
- final edited short is expected to be shorter than the raw 20 sec after dead-frame trimming
- SET_B_CONVENIENCE visual authority
- Clip 1 integrates the topic-opening device rather than adding a separate formal intro clip
- Post Card is a post-production overlay, not a Seedance-generated third clip
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

### Step 1 — prepare three short recurring audio references
Create clean ~4-second reference clips:
- `VOICE_REF_LEFT_GAEUN_4S`
- `VOICE_REF_CENTER_HARIN_4S`
- `VOICE_REF_RIGHT_TAEMIN_4S`

### Step 2 — generate P002 Clip 1 once
- Seedance 2.0 Mini
- 480p
- 16:9
- 10 sec
- generation count exactly 1
- first frame: P002 opening still with CENTER already holding phone
- attach only CENTER/Harin 4s + RIGHT/Taemin 4s because LEFT is silent
- QC this as actual production footage, not a pilot

### Step 3 — if no hard blocker, generate Clip 2 once
- 10 sec
- use the original convenience cast still / canon-derived neutral state as the new first frame
- attach only LEFT/Gaeun 4s + CENTER/Harin 4s because RIGHT is silent
- intentional editorial cut; do not chain from Clip 1 last frame

### Step 4 — assemble publishable 9:16 master
- editorial punch-ins instead of AI camera moves
- Post Card overlay during Clip 1; it is not a third generated clip
- Korean/English subtitle treatment in post
- no explanatory outro
- publish → 24h / 7d performance learning

## Mandatory pre-generation inheritance check

Before presenting or submitting any scene prompt:
- active episode image is the visual authority
- attached voice-reference total duration stays within the active model limit
- only speaking-character references are attached whenever possible
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
