# TALKSHOW

한국 커뮤니티의 실제 글·댓글을 원재료로 만드는 반복 캐스트 2D 토크쇼.

## 단일 진입점

이 `README.md`만 진입점으로 사용한다. “latest”, “handoff”, “new session” 파일을 새로 만들지 않는다.

권위 순서:
1. `CURRENT_STATE.md` — 지금 단계와 바로 다음 행동
2. `PROJECT_BIBLE.md` — 바뀌기 어려운 편집 원칙
3. `PRODUCTION_PIPELINE.md` — 역할·게이트·성과 루프
4. `SERIES_V2_RELOCK.md` — 현재 V2 visual / cast / set / reaction / first-frame baseline
5. `PERFORMANCE_AUDIO_ARCHITECTURE.md` — **현재 performance-first timing / voice / mouth / eye / physical acting / QC architecture**
6. `CORE_DESIGN_AND_PROMPTS.md` — reusable historical/current grammar; V2와 충돌하는 sparse-set / restrained-performance / universal-first-pose 부분은 newer V2 docs가 supersede
7. `MASTER_STYLE_PROMPT.md` — 캐릭터/배경 생성·리마스터 시 쓰는 authoritative copy-paste visual style lock. 개별 캐릭터 identity reference가 generic style 문구보다 우선한다.
8. `episodes/Pxxx/` — 회차별 source, prompt, QC, performance. active episode package는 그 회차 실행 세부를 통제한다.

충돌하면 `CURRENT_STATE.md`가 현재 행동을 우선 통제한다. Performance/audio/animation execution은 `PERFORMANCE_AUDIO_ARCHITECTURE.md`를 따른다. 캐릭터 얼굴·눈·머리 등 identity는 해당 active reference image가 일반 스타일 문구보다 우선한다. 과거 결정은 Git history와 P001/P002 evidence로 보존한다.

## 현재

**P002 PERFORMANCE-FIRST ARCHITECTURE RETRY ACTIVE**

- isolated P001 pilots are no longer active work
- recurring sets: HOME / CONVENIENCE / HANGANG / ROOFTOP
- current P002 visual authority: user-supplied convenience-store-front three-person image / opening-still family from the 2026-09-04 session
- generation master stays **16:9**; final Shorts distribution becomes 9:16 in edit
- one failed vertical/recomposition attempt changed the drawing style; a later concise-lock 16:9 Omni attempt preserved style materially better
- the later single ~10 sec P002 attempt proved that **single compact clip first** is viable
- however that attempt is not publishable final: mechanical voice, tempo forced by preselected duration, uncanny phoneme-heavy mouth animation, malformed CENTER eye-close transition near the start
- selected TopView references `Gaeun outdoors / Harin / Taemin` remain interim evidence, not final production voice lock
- 4-sec references were prepared due Seedance 2.0 Mini's observed 15.2-sec total reference-audio ceiling; Taemin required about +10 dB loudness compensation
- next voice architecture: whole-scene multi-speaker dialogue master in one pass; A/B ElevenLabs v3 Dialogue vs Typecast/strongest accessible Korean dialogue engine
- **PERFORMANCE MASTER** includes exact dialogue + while-speaking action + pause-requiring nonverbal beats + reaction order
- natural whole-scene audio determines the required video duration; do not choose 10 sec first and force speech into it
- feed the same dialogue master to Omni as turn/pacing authority; final edit reuses that same master audio rather than manually syncing separate lines
- mouth animation: limited stylized 2D mouth flap; turn-level sync > phoneme-perfect lip sync
- eye acting: blink / wink / eye-smile / motivated closure allowed; malformed ambiguous half-closed morphs are hard fail
- physical acting should be **larger than earlier V2 tests**: clear lean/recoil, arms extended, posture changes, irritated/laughing body language, precise brief playful upper-arm/shoulder contact where motivated
- Post Card is optional, not a mandatory overlay/hard-cut production step
- QC now includes first 0.5 sec frame-by-frame, every eye-close transition, speaker handoff windows, max mouth-open frames, identity/style and contact geometry

## 다음 세션 시작점

Read `CURRENT_STATE.md` first, then `PERFORMANCE_AUDIO_ARCHITECTURE.md`, then `episodes/P002/FULL_EPISODE_PACKAGE.md`.

Immediate sequence:
1. finalize P002 `PERFORMANCE MASTER` with compact source-driven dialogue + 1–2 larger physical beats;
2. generate the entire multi-speaker scene once in two dialogue engines and A/B naturalness;
3. lock one `P002_DIALOGUE_MASTER.wav`;
4. measure actual duration / derive turn timestamps / derive video duration;
5. make exactly one new 16:9 Omni generation using the same dialogue master as timing authority, concise visual lock, clean eye transitions and limited 2D mouth animation;
6. frame-level QC;
7. if pass, final 9:16 edit / subtitles / thumbnail / publish.

Do not return to 2 x 8 sec by default and do not return to pilot-for-pilot testing.

## Repository integrity note

A 2026-09-04 inspection found that older prose claimed `assets/V2_VISUAL_LOCK_20260904.md` and binaries under `assets/v2_locked/` were preserved, but those paths were not present on inspected `main`. Treat those binary-preservation claims as unverified until an actual upload is confirmed.

세부 상태: [CURRENT_STATE.md](CURRENT_STATE.md)  
Performance/audio architecture: [PERFORMANCE_AUDIO_ARCHITECTURE.md](PERFORMANCE_AUDIO_ARCHITECTURE.md)  
V2 baseline: [SERIES_V2_RELOCK.md](SERIES_V2_RELOCK.md)  
복붙용 마스터 스타일: [MASTER_STYLE_PROMPT.md](MASTER_STYLE_PROMPT.md)  
P002 active package: [episodes/P002/FULL_EPISODE_PACKAGE.md](episodes/P002/FULL_EPISODE_PACKAGE.md)
