# CURRENT EXECUTION OVERRIDE — 2026-09-03

Production pipeline lock is complete. The active workflow is **real-episode manual prompt entry in TopView by the user**.

- Pause autonomous Work/TopView execution, automatic prompt rewriting, and automatic reference selection.
- Reuse the already locked canonical 3-person master still as the first frame.
- Do not create a new set, character test, or master-composition test.
- Use `episodes/P001/PRODUCTION_PACKAGE.md` for the exact six prompts and user action order.
- ChatGPT does not generate the videos; the user generates and edits them manually.

The long-term reusable asset/renderer pipeline below remains the later project direction.

## Current logical role map

The intended operating chain is:

`Radar/Source Ingest → Thread Reconstruction/Gold Extraction → Episode Package/Storyboard → User Manual TopView/CapCut Production → Defect QC/Archive`

This is not yet a set of independently deployed agents. In the current pilot, ChatGPT performs the upstream source/editorial/package roles, the user performs generation/edit/publish, and ChatGPT performs defect-only QC.

Important boundaries:
- do not send a detected post directly to storyboard without reconstructing comments/replies and selecting GOLD
- QC may reject production defects or a weak source, but must not smooth human language into bland dialogue
- automatic prompt rewriting, automatic reference selection, and automatic TopView execution remain paused
- detailed audit: `WORKFLOW_AND_CORE_AUDIT_20260903.md`
- simple comment-chain default: 2 scenes / approximately 15–22 sec, not a forced 30–60 sec


---

# TALKSHOW PRODUCTION PIPELINE

## Goal
`EPISODE_SPEC.md`를 사람이든 AI 에이전트든 읽으면 동일한 쇼 자산을 사용해 영상까지 제작할 수 있게 한다.

---

# A. 한 번만 만드는 SHOW FOUNDATION

## A1. Character Bible
각 캐릭터에서 정말 고정할 것만 정의한다.
- 이름 / 성별 / 외형
- 목소리 ID 또는 음색 정의
- 매우 핵심적인 기질 2~3개
- 금지할 정체성 드리프트

역할(논리/바보/리액션/팩트체크)은 고정하지 않는다.

## A2. Visual Bible
초기 권장 방향: **저프레임 2D 컷아웃 + 커뮤니티 만화 감성**.

정해야 할 것:
- 선 굵기 / 채색 / 얼굴 단순화 정도
- 배경 밀도
- 카메라 기본 거리
- 자막 스타일
- 컷어웨이/낙서/자료화면 스타일
- 욕설 비프/자막 마스킹/화면전환 스타일

## A3. Character Asset Pack
캐릭터당 최소:
- 정면/3/4 기본 바디 포즈
- idle 2~3종
- 눈: 기본/감음/커짐/힘빠짐
- 입: 최소 6개 phoneme shape + idle
- 표정: 무표정/웃음/터짐/정색/당황/짜증/어이없음/우쭐/시무룩
- 손/팔 포즈 4~6종
- 특수 찌그러짐/과장 표정 2~3종

PNG 또는 SVG 레이어 자산으로 보관한다.

## A4. Stage / Background Pack
- 기본 대화 공간 1개
- 카메라 프리셋: 3-shot / 2-shot / 1-shot / reaction close-up
- 화면/모니터/휴대폰 등 자료 표시용 prop
- 컷어웨이용 빈 프레임 템플릿

## A5. Voice Pack
- 캐릭터별 고정 voice ID
- 평상/흥분/작게 말함/비웃음/웃음 등 허용 범위
- 한국어 인터넷 표현 발음 사전
- 욕설 공개본 처리 규칙

## A6. Renderer
장기 권장: **Remotion 기반 프로그램 렌더러**.
- 입력: episode JSON/MD + 음성 + PNG/SVG + SFX
- 출력: 1080x1920 mp4
- 담당: 컷, 줌, 자막, mouth sprite, reaction pose, BLEEP, 자료화면, SFX

초기 파일럿은 Cartoon Animator/Adobe Character Animator + CapCut으로 빠르게 검증할 수 있으나, 포맷이 확정되면 Remotion 쪽으로 옮기는 것이 자동화에 유리하다.

---

# B. 매회 만드는 EPISODE PIPELINE

## B1. Radar / Source Ingest
수집:
- URL
- 본문 원문
- 이미지/영상 설명 또는 로컬 파일
- 댓글 원문
- 댓글 답글 트리
- 게시 시간/반응량
- 사실 확인이 필요한 주장

원문을 이 단계에서 순화하지 않는다.

## B2. Gold Extraction
AI가 새 드립을 쓰기 전에 인간이 이미 만든 좋은 비트를 고른다.

출력 예:
- GOLD_01: 댓글 A → 댓글 B 한 줄 반박
- GOLD_02: 제3자 'ㅋㅋㅋㅋ'
- GOLD_03: 뜬금포 댓글

## B3. Script / Casting
- 3인에게 GOLD를 배치
- 원댓글을 최소 변형
- 꼭 필요할 때만 bridge 추가
- 발화량 균등 배분 금지

## B4. Disclosure / Censor Plan
대본 원형과 공개본을 분리한다.
- MASTER_DIALOGUE: 원래 맛 보존
- PUBLIC_DIALOGUE: 비프/묵음/자막마스킹 정보 포함

예:
`좆도` → 음성: `좆-[BLEEP]` 또는 해당 단어 전체 비프
화면: 반응 컷/줌/입 가림 등

## B5. Voice Generation
권장 후보: ElevenLabs 또는 OpenAI TTS.
- 문장별 별도 wav 생성 권장
- 파일명에 캐릭터/라인 번호 포함
- 감정 지시는 과도하게 넣지 않는다

## B6. Timing / Lip Sync
- 음성 길이 기준으로 실제 컷 길이를 확정
- mouth cue 생성
- 방법 1: Rhubarb Lip Sync phonetic recognizer → JSON mouth cues
- 방법 2: Live2D/Cartoon Animator/Character Animator 자체 lip sync

## B7. Beat & Shot Plan
각 비트에 지정:
- start/end
- speaker
- shot preset
- expression
- body pose
- camera punch-in 여부
- cutaway 여부
- on-screen text
- SFX
- censor event

## B8. Episode Visual Assets
그 회에만 필요한 것만 만든다.
- 떡밥 설명 카드
- 재연 그림
- 짧은 그래프/지도/낙서
- 밈성 prop

원문 캡처를 그대로 보여주는 것은 기본값이 아니다.

## B9. Render / Composite
권장 최종 구조:
1. TTS 생성
2. lip cue 생성
3. episode spec을 JSON으로 변환
4. Remotion 렌더
5. 필요한 경우 CapCut/Resolve에서 마지막 손맛 편집

## B10. Minimal QC
자동 수정하지 않고 결함만 체크:
- 음성 누락
- 잘못된 speaker
- mouth cue 깨짐
- 컷/자막 화면 밖 이탈
- 사실관계 반전
- 공개본에서 미처리된 플랫폼 리스크 표현

재미가 약하면 '대본 개선' 대신 원소스/비트 선택을 재검토한다.

---

# C. 권장 툴 스택

## Pilot 속도 우선
- Character/Background art: 이미지 생성 + 수동 레이어 정리
- Rig/Animation: Cartoon Animator 5 또는 Adobe Character Animator
- Voice: ElevenLabs
- Final edit: CapCut Desktop 또는 DaVinci Resolve

## Scale / 자동화 우선
- Script/Spec: Markdown canonical source
- Machine spec: MD에서 episode.json 생성
- Voice: ElevenLabs/OpenAI TTS API
- Lip sync: Rhubarb JSON 또는 Live2D SDK
- Renderer: Remotion
- Final: ffmpeg 자동 export, 필요할 때만 수동 편집

## Why
생성형 영상은 매회 캐릭터 일관성/립싱크/카메라를 다시 해결해야 하지만, 자산 기반 렌더러는 한 번 만든 캐릭터와 무대를 계속 재사용하면서 MD/JSON만 교체할 수 있다.
