# CURRENT STATE

Updated: 2026-09-04 KST
Status: **P002 ARCHITECTURE RELOCKED — PERFORMANCE-FIRST AUDIO / SINGLE-CLIP RETRY NEXT**

## 지금의 단일 결론

P002의 첫 viable 10초 단일클립 테스트는 visual fidelity와 single-clip 가능성을 확인했지만 **publishable final은 아니다**.

실제 문제는:
- 음성이 기계적이고 고정 영상길이에 맞춰 속도가 왜곡됨
- phoneme-perfect lip sync가 단순 2D 얼굴에 기괴하게 보임
- 시작부 CENTER eye-close transition이 malformed 상태로 지나감

따라서 다음 단계는 tiny prompt tweak가 아니라 **PERFORMANCE FIRST** 구조로 한 번 재생성하는 것이다.

현재 권위 문서:
- current action: `CURRENT_STATE.md`
- immutable editorial principles: `PROJECT_BIBLE.md`
- V2 visual/reaction baseline: `SERIES_V2_RELOCK.md`
- **performance/audio/face-animation architecture: `PERFORMANCE_AUDIO_ARCHITECTURE.md`**
- reusable prompt/style grammar: `CORE_DESIGN_AND_PROMPTS.md`, `MASTER_STYLE_PROMPT.md`
- P002 source: `episodes/P002/SOURCE_PACK.md`
- P002 active production package: `episodes/P002/FULL_EPISODE_PACKAGE.md`

## 큰 파이프라인

`Real Community Source → Gold Comments → PERFORMANCE MASTER → Whole-Scene Dialogue Master → Timing Extraction → Derived Video Duration → Omni Generation → Frame-level QC → 9:16 Edit → Publish → Performance Learning`

## 고정 체크포인트

- 쇼츠 우선
- 실제 한국 커뮤니티 원문/댓글 우선
- opener는 친구가 폰에서 뭔가 발견한 자연스러운 `야 이거 봐` 계열
- Post Card는 optional, 기본 공정 아님
- 기준 이미지 / 캐릭터 identity 절대 우선
- generation master 16:9 → distribution 9:16
- **자연스러운 performance가 영상 길이를 결정**
- single compact clip 우선; 소스가 필요할 때만 multi-clip
- 입은 그럴듯한 limited 2D mouth flap; phoneme-perfect realism 금지
- blink / wink / eye-smile / 눈 질끈 감기 등 자연스러운 눈 감정표현은 허용
- 단, malformed half-closed morph transition은 hard fail
- 리액션/행동은 더 크게: 1–2 large physical beats + causal social reactions

## Recurring cast / set

### Cast
- LEFT: CHAR_B / white-T-shirt woman
- CENTER: CHAR_06
- RIGHT: recurring male identity

### Set pool
1. `SET_A_HOME`
2. `SET_B_CONVENIENCE`
3. `SET_C_HANGANG`
4. `SET_D_ROOFTOP`

Current P002 visual authority remains the user-supplied convenience-store-front three-person image / opening-still family from the 2026-09-04 session. If old prose conflicts with the active image, the image controls.

## P002 evidence from real generations

### Failed vertical/restyle attempt
A generated result was vertically recomposed despite a 16:9 source still and visibly changed faces/linework/style from the first frames.

Current lesson:
- do not generate the recurring cast master as a new 9:16 composition
- keep Omni generation 16:9
- final 9:16 comes from editorial crop/punch-in
- do not redundantly re-describe every visible face/outfit/style feature in the prompt

### Viable 16:9 single-clip attempt
A later 10-sec 16:9 Omni generation with a concise visual-lock prompt preserved the source drawing style materially better and demonstrated that opener + multiple response beats can fit one short clip.

Good evidence:
- visual identity/style remained much more stable
- single-clip structure is feasible
- staggered social reactions worked
- larger gestures were feasible
- normalized voice-reference loudness worked; Taemin was approximately +10 dB quieter in the source preview and was raised to roughly match Gaeun/Harin

But the clip is **not final** because:
- generated dialogue sounded synthetic/mechanical
- fixed video duration pushed speech pacing unnaturally
- mouth shapes were too literal / uncanny
- CENTER's eye-close transition near the opening contained malformed ambiguous frames

Do not spend time repairing small ending-expression details on this clip; architecture-level defects dominate.

## Voice status — important correction

Historical/interim selected TopView references:
- LEFT: `Gaeun outdoors`
- CENTER: `Harin`
- RIGHT: `Taemin`

4-second trimmed reference files were prepared because Seedance 2.0 Mini R2V rejected total reference audio above 15.2 sec.

However, **the 4-sec TopView reference architecture is now interim evidence, not the desired final production voice system**. The first real result sounded too mechanical.

Next direction:
- generate the whole multi-speaker scene once in a dialogue-capable external engine
- first A/B candidates: ElevenLabs v3 Dialogue vs Typecast
- prioritize natural Korean prosody, turn-taking, pauses, emotion, stable recurring voices, and low manual labor
- output one `P002_DIALOGUE_MASTER.wav`, not separate manually placed lines

Authority: `PERFORMANCE_AUDIO_ARCHITECTURE.md`.

## PERFORMANCE FIRST — current core architecture

Do not choose `10 sec` first.

1. Write one `PERFORMANCE MASTER` containing exact dialogue + emotion + while-speaking actions + pause-requiring nonverbal beats + reaction order.
2. Generate the **whole scene audio in one pass**.
3. Measure actual dialogue-master duration.
4. Extract/derive speaker-turn and silence timestamps automatically.
5. Derive required video duration from actual performance, leaving approximately 0.4–0.7 sec reaction tail for fixed-duration Mini routes.
6. Feed the same whole-scene dialogue master to Omni as the timing/performance authority.
7. Generate one 16:9 clip.
8. For publishable audio, use the original dialogue master at time 0 rather than manually syncing separate lines.

This still needs one real validation generation. Target is **turn-level sync**, not phoneme-perfect lip sync.

## Face animation lock — corrected

### Mouth
Use limited stylized 2D mouth animation:
- closed
- slightly open
- small relaxed open

Do not demand realistic Korean phoneme mouth shapes. The goal is visually plausible mouth-flap rhythm with correct active-speaker timing.

### Eyes
Do NOT ban blinking or eye closure.

Allowed/desired when motivated:
- natural blink
- wink
- eye-smile
- wide-eyed surprise
- brief squeezed-eye laugh / frustration

Hard fail:
- melted / misaligned / asymmetric half-closed intermediate states
- an eye that looks neither intentionally open nor intentionally closed

Expression transitions must be clean and return to the locked reference eye design.

## Reaction / physical performance — increase further

V2 should not regress to tiny head turns and polite micro-gestures.

Desired when motivated:
- strong torso lean/recoil
- phone clearly extended toward the others
- arm fully extended while making a point
- two-hand disbelief
- shifting/repositioning seated posture
- irritated body language
- hand to forehead / covering face
- bending forward laughing
- brief table tap
- **brief playful contact**, e.g. one friend taps another's upper arm/shoulder

For contact actions, specify exact target and duration; do not use vague `hits him` language.

Baseline for an ~8–12 sec short:
- about 1–2 larger physical beats
- plus eye / face / head / torso social reactions
- causal staggering remains important

## Current opening grammar

Default:
- one friend already holds the phone in the opening still when required
- natural opener (`야 이거 봐`, `이거 봤어?`, or direct claim)
- the others visibly attend to the phone
- conversation immediately follows

`Post Card` / community-card insert is **optional only**. It is not a mandatory overlay, hard cut, third clip, or recurring production burden.

## Current duration / clip policy

The previous fixed `2 x 8 sec` and later `10 + 10` assumptions are superseded.

New default:
> **one compact clip of whatever duration the completed performance naturally requires**

Use multiple clips only if:
- the source contains enough real additional material;
- there is a genuine shot/state change;
- one clip would force rushed speech or overloaded motion.

For Seedance 2.0 Mini fixed-duration routes, derive duration from the completed audio master, not vice versa.

## Mandatory QC hierarchy — updated

Representative-frame montage alone is insufficient.

Before PASS:
1. inspect the **first 0.5 sec frame-by-frame**
2. inspect every blink / wink / eye-close transition frame-by-frame
3. inspect speaker handoff windows around ±0.2 sec
4. inspect maximum-mouth-opening frames
5. compare identity/style at first / middle / end
6. inspect hands, physical contact, table/prop intersections
7. assess reaction amplitude and causal readability
8. assess audio naturalness, pacing, speaker separation, loudness
9. only then consider minor expression-tone details

Hard fail includes uncanny face morphs even if they last only a few frames.

## 바로 다음 행동 — NEXT SESSION START HERE

### Step 1 — build final P002 PERFORMANCE MASTER
Keep the real-source logic, but redesign the 8–12 sec-ish performance with:
- compact dialogue
- 1–2 larger motivated physical beats
- explicit concurrent actions vs pause-requiring nonverbal beats
- clean reaction order

### Step 2 — whole-scene voice A/B
Generate the complete three-speaker conversation once in:
- ElevenLabs v3 Dialogue
- Typecast or the strongest accessible Korean multi-speaker dialogue engine

Compare naturalness and recurring-voice viability. Do not generate line-by-line and manually place each sentence.

### Step 3 — lock one dialogue master
Create `P002_DIALOGUE_MASTER.wav`, then measure duration and extract turn timestamps.

### Step 4 — derive video duration
For Mini/fixed-duration route, use roughly `ceil(dialogue duration + 0.4–0.7 sec)` or the nearest supported duration.
If a verified smart-duration route is accessible in the actual execution environment, it may be tested instead.

### Step 5 — one new production generation only
- Omni Reference
- active P002 opening still
- generation master 16:9
- higher generation resolution than 480p if cost/availability is acceptable
- dialogue master audio as timing/performance authority
- compact visual-lock prompt
- larger physical acting
- clean eye transitions
- limited 2D mouth animation
- exactly one generation before QC

### Step 6 — frame-level QC
Use the hierarchy above. Only after this architecture-validation clip passes, proceed to final 9:16 edit/subtitles/thumbnail/publish.

## Repository integrity note

Older prose once claimed canonical binaries under `assets/v2_locked/`; that claim was not verified on inspected `main`. Do not claim current opening/base image binaries are GitHub-preserved unless an actual binary upload is verified.

## 응답 규칙

모든 talkshow 응답은 다음으로 시작한다.
1. 큰 흐름
2. 현재 세부 단계
3. 이번 턴 완료조건

Near the top also retain the concise fixed checkpoint so long sessions do not lose the production priorities.

## Generic media preflight checkpoint

Talkshow now adopts the same AutoPipeline project-agnostic media-conditioning contract used by other children.

Before the next P002 production generation, requirements must be declared as data rather than implicit UI assumptions. At minimum, when applicable:
- locked opening still / first frame;
- character identity masters;
- dialogue master timing audio;
- fixed voice references for any stage that consumes them.

Provider capability and actual supplied evidence must be checked before generation.
If the chosen provider cannot accept a required media input, switch provider/adapter or block; prompt-only approximation is not an acceptable fallback.

This does not claim that the currently referenced session-local P002 images/audio have been Git-preserved. Availability and supplied-to-provider are separate facts.
