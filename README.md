# TALKSHOW

한국 커뮤니티의 실제 글·댓글을 원재료로 만드는 반복 캐스트 2D 토크쇼.

## 단일 진입점

이 `README.md`만 진입점으로 사용한다. “latest”, “handoff”, “new session” 파일을 새로 만들지 않는다.

권위 순서:
1. `CURRENT_STATE.md` — 지금 단계와 바로 다음 행동
2. `PROJECT_BIBLE.md` — 바뀌기 어려운 편집 원칙
3. `PRODUCTION_PIPELINE.md` — 역할·게이트·성과 루프
4. `CORE_DESIGN_AND_PROMPTS.md` — 시각/음성/프롬프트 락
5. `episodes/Pxxx/` — 회차별 source, prompt, QC, performance

충돌하면 위 순서를 따른다. 과거 결정은 Git history로 확인한다.

## 현재

- P001 Scene A: 영상 잠금, 재생성 금지
- 다음: `episodes/P001/SCENE_B_PACKAGE.md` 그대로 Scene B 10초 1회 수동 생성
- 생성: Seedance 2.0 Mini, 잠긴 16:9 cast-master 재사용
- 배포: 9:16 편집본
- 음성: `assets/VOICE_REGISTRY.md`의 고정 voice ID로 voice-to-voice 변환; 실제 ID는 P001 게시 전 배정
- 사용자: TopView 생성·CapCut/Resolve 편집·게시
- ChatGPT: source/GOLD/package/prompt, defect QC, performance learning

세부 상태: [CURRENT_STATE.md](CURRENT_STATE.md)
