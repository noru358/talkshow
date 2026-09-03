# TALKSHOW

한국 커뮤니티의 실제 글·댓글을 원재료로 만드는 반복 캐스트 2D 토크쇼.

## 단일 진입점

이 `README.md`만 진입점으로 사용한다. “latest”, “handoff”, “new session” 파일을 새로 만들지 않는다.

권위 순서:
1. `CURRENT_STATE.md` — 지금 단계와 바로 다음 행동
2. `PROJECT_BIBLE.md` — 바뀌기 어려운 편집 원칙
3. `PRODUCTION_PIPELINE.md` — 역할·게이트·성과 루프
4. `CORE_DESIGN_AND_PROMPTS.md` — 기존 reusable visual/voice/prompt grammar
5. `SERIES_V2_RELOCK.md` — 현재 V2에서 의도적으로 재오픈한 visual/voice/reaction baseline의 상세 변경 기록
6. `episodes/Pxxx/` — 회차별 source, prompt, QC, performance

충돌하면 `CURRENT_STATE.md`가 현재 행동을 우선 통제한다. `SERIES_V2_RELOCK.md`는 V2에서 기존 CORE의 sparse-set / restrained-performance 가정과 충돌하는 부분을 의도적으로 supersede한다. 과거 결정은 Git history와 P001 V1 파일로 보존한다.

## 현재

**SERIES V2 RELOCK ACTIVE**

- P001 V1 Scene B QC는 현재 건너뜀
- P001 V1 Scene A/B 파일은 보존하되 필요하면 V2 기준으로 다시 생성 가능
- Step 1: `assets/RIGHT_MASTER_V2_SPEC.md` — 기존 남캐 identity 유지, 2030 Seoul daily/minimal styling으로 hair/outfit 업데이트
- Step 2: `assets/SET_MASTER_V2_PACK.md` — empty set 4종 A/B/C/D 생성 및 lock
- set pool: Seoul officetel/home / convenience-store-front / Hangang / Seoul villa rooftop
- four set 모두 사용; A=main, B=signature, C/D=variation
- 이후 각 locked set + 3 character packs → set-specific 3-person cast still → fixed-first-frame I2V
- voice: `assets/VOICE_REGISTRY.md` V2 audition profiles; fixed voice IDs 아직 미배정
- reaction V2: sequential causality는 유지하되 facial/head/torso energy 및 one/two-hand gestures, brief fist gesture까지 확대
- 생성: 16:9 master
- 배포: 9:16 Shorts/Reels/TikTok master

세부 상태: [CURRENT_STATE.md](CURRENT_STATE.md)  
V2 변경 이유/락: [SERIES_V2_RELOCK.md](SERIES_V2_RELOCK.md)
