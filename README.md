# TALKSHOW

한국 커뮤니티의 실제 글·댓글을 원재료로 만드는 반복 캐스트 2D 토크쇼.

## 단일 진입점

이 `README.md`만 진입점으로 사용한다. “latest”, “handoff”, “new session” 파일을 새로 만들지 않는다.

권위 순서:
1. `CURRENT_STATE.md` — 지금 단계와 바로 다음 행동
2. `PROJECT_BIBLE.md` — 바뀌기 어려운 편집 원칙
3. `PRODUCTION_PIPELINE.md` — 역할·게이트·성과 루프
4. `SERIES_V2_RELOCK.md` — 현재 V2에서 의도적으로 재오픈/재정의한 visual/voice/reaction/first-frame baseline
5. `CORE_DESIGN_AND_PROMPTS.md` — reusable historical/current grammar; V2와 충돌하는 sparse-set / restrained-performance / universal-first-pose 부분은 `SERIES_V2_RELOCK.md`가 supersede
6. `episodes/Pxxx/` — 회차별 source, prompt, QC, performance. active episode package는 그 회차의 실행 세부를 통제한다.

충돌하면 `CURRENT_STATE.md`가 현재 행동을 우선 통제한다. V2 변경은 `SERIES_V2_RELOCK.md`를 따른다. 과거 결정은 Git history와 P001 V1 파일로 보존한다.

## 현재

**FIRST COMPLETE V2 EPISODE BUILD ACTIVE — P002**

- isolated P001 Scene B / Omni pilot generation is no longer the active next action
- recurring sets: HOME / CONVENIENCE / HANGANG / ROOFTOP
- current P002 visual authority: user-supplied convenience-store-front three-person image from the 2026-09-04 session
- selected recurring voice references: LEFT `Gaeun outdoors` / CENTER `Harin` / RIGHT `Taemin`
- reaction V2: causal staggering 유지 + clearly readable facial/head/torso reactions and motivated one/two-hand gestures
- real-episode first-frame grammar: canonical cast still → minimum shot-specific derived first-frame stills → fixed-first-frame I2V → editorial hard cut/crop/punch-in
- `fixed first frame` means the literal start of each generated clip, not one universal resting pose for the whole edited episode
- P002 source provenance: `episodes/P002/SOURCE_PACK.md`
- P002 full storyboard: `episodes/P002/FULL_EPISODE_PACKAGE.md`
- P002 target: about 16 sec = 2 x 8 sec Seedance clips → 9:16 distribution edit
- immediate next asset: one `P002_OPENING_STILL` derived from the current convenience image, changing only CENTER so she already holds a smartphone
- no explanatory outro; subtitle/localization is post-production, not baked into generation

## Repository integrity note

A 2026-09-04 inspection found that older prose claimed `assets/V2_VISUAL_LOCK_20260904.md` and binaries under `assets/v2_locked/` were preserved, but those paths were not present on inspected `main`. Treat those binary-preservation claims as unverified until an actual upload is confirmed.

세부 상태: [CURRENT_STATE.md](CURRENT_STATE.md)  
V2 변경 이유/락: [SERIES_V2_RELOCK.md](SERIES_V2_RELOCK.md)  
P002 full episode: [episodes/P002/FULL_EPISODE_PACKAGE.md](episodes/P002/FULL_EPISODE_PACKAGE.md)
