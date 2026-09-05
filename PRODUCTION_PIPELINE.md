# TALKSHOW PRODUCTION PIPELINE

Updated: 2026-09-03 KST  
Status: **CURRENT / manual production**

## 역할과 소유권

| 단계 | 현재 담당 | 산출물 | 통과 조건 |
|---|---|---|---|
| Radar / Source Ingest | ChatGPT | 후보 URL·본문·미디어·댓글 트리 | 원문/답글 관계 보존 |
| Source Gate / Gold | ChatGPT + 사용자 최종 취향 | SOURCE_PACK | kill rule 통과, 강한 인간 beat ≥2 |
| Episode Package | ChatGPT | 대사 provenance, beat/shot, exact prompt | AI-written beats ≤30% |
| Manual Production | 사용자 | TopView clips, edit | 잠긴 references/prompt 사용 |
| Voice Lock / Mix | 사용자 실행, ChatGPT 사양/QC | fixed-voice final audio | 캐릭터 voice ID 일치 |
| Defect QC | ChatGPT | pass/fail + 한 줄 보정 | 제작 blocker 없음 |
| Distribution / Performance | 사용자 게시, ChatGPT 기록·해석 | 24h/7d performance record | 다음 실험 가설 1개 |

이것은 논리적 역할표다. 독립 실행 에이전트 소프트웨어가 완성됐다는 뜻이 아니다.

## 1. Radar / Source Ingest

기록:
- URL, 게시시각, 본문 원문
- 이미지/영상 맥락
- 댓글과 답글 parent 관계
- 당시 조회·추천·댓글
- 사실확인이 필요한 주장

수집 단계에서 순화·재작성하지 않는다. 반응량은 후보 신호일 뿐 자동 채택 기준이 아니다.

## 2. Source Gate

다음이면 보류/폐기:
- reply 구조 미복원
- 전제 설명이 punch보다 김
- 강한 인간 beat 2개 미만
- AI bridge 없이는 대화가 성립하지 않으며 AI-written 비중 30% 초과
- 반응이 대체 가능한 일반론뿐
- 공개 처리 후 핵심 재미 소멸

소재가 gate를 못 넘으면 고쳐 쓰지 않고 다른 소스로 간다.

## 3. Gold / Episode Package

각 spoken beat에 `SETUP/GOLD/BRIDGE`, origin, exact source, speaker, public treatment를 붙인다.

비율:
- AI-written spoken beats / all spoken beats ≤ 30%
- source-summary setup도 AI-written
- AI-original comedic payoff = 0% 기본
- 비언어 reaction은 별도 interaction beat로 기록하되 대사 비율 분모에는 넣지 않음

패키지:
- MASTER_DIALOGUE / PUBLIC_DIALOGUE
- speaker and silence reactions
- trigger와 reaction latency
- exact TopView prompt
- generation duration UI setting
- 9:16 edit plan
- voice segment plan

## 3.5 Generic media preflight

Before any image/video/audio generation step, map project-specific dependencies into the AutoPipeline MEDIA_INPUT_CONTRACT model.

Examples for Talkshow:
- locked opening still -> role=first_frame, media_type=image;
- recurring character master / master pack -> role=character_identity, media_type=image;
- fixed voice reference -> role=voice_identity, media_type=audio;
- whole-scene dialogue master used as performance/timing authority -> role=timing_audio, media_type=audio.

For each actual provider call:
1. declare requirements;
2. verify the chosen renderer/provider supports the required media types and explicit inputs;
3. record which exact sources were actually supplied;
4. authorize only after required MUST_SUPPLY_MEDIA items have supplied evidence.

A file being described in a prompt or merely available in Git/chat is not equivalent to provider conditioning.

If a provider cannot accept a required input:
- route to another capable provider/adapter; or
- block the step.

Do not generate once and hope QC catches identity/style/voice drift afterward.

## 4. Manual I2V

- Seedance 2.0 Mini / 480p / 16:9
- locked cast-master first frame + master packs
- 실제 대사를 넣어 lip motion과 performance 생성
- clip 1회 생성 후 defect QC
- prompt를 자동 재작성하지 않음
- 세트·캐릭터 테스트로 회귀하지 않음

## 5. Fixed voice post-process

Seedance native voice는 최종 identity가 아니다.

1. 발화 구간을 speaker별로 split
2. 캐릭터의 고정 ElevenLabs voice ID 선택
3. Voice Changer multilingual model로 변환
4. 원래 timing/delivery 유지
5. 변환본을 원 타임라인에 교체
6. 분리 불가능한 겹말/웃음만 fixed-ID TTS로 보수
7. room tone, BLEEP, loudness 정리

무성 I2V + 전체 TTS 방식은 현 파일럿 기본값이 아니다.

## 6. Defect QC

우선순위:
1. wrong speaker / missing line
2. identity, seat, set drift
3. severe face/eye/mouth/hand deformation
4. trigger 이전 anticipatory reaction
5. truncated/unnatural Korean timing
6. fixed voice mismatch
7. censor/public-risk failure
8. 9:16 crop에서 얼굴·자막 가림

재미가 약하면 자동 대사 개선 대신 source gate/GOLD 선택으로 되돌아간다.

## 7. Distribution / Performance

초기 채널 전략:
- primary learning surface: YouTube Shorts
- 같은 9:16 master의 cross-post 후보: TikTok, Instagram Reels
- 첫 10편은 포맷 탐색기. 회차마다 hook, 길이, GOLD 유형, interaction device 중 하나만 의도적으로 바꾼다.

기록:
- platform / URL / publish timestamp / version
- video length / first spoken word time / hook type
- GOLD types / AI-written beat share
- views or reach
- viewed vs swiped where available
- average view duration / average percentage viewed / completion
- rewatch or loops where available
- likes, comments, shares, saves per 1,000 views
- followers/subscribers gained per 1,000 views
- qualitative comment signals: quoted line, named character, confusion, source request

판정:
- 한 편의 조회수만으로 포맷을 바꾸지 않는다.
- 3편 이상 같은 신호가 반복되거나 명확한 retention cliff가 있을 때만 가설을 승격한다.
- 성과 담당은 다음 source/GOLD/hook 실험을 제안할 뿐 확정 대사를 자동 수정하지 않는다.

## 8. Archive

회차 폴더에 함께 남긴다:
- SOURCE_PACK
- final package/prompt
- used inputs and output filenames
- defect QC
- published version/URL
- 24h and 7d metrics
- keep/change/kill 판단과 다음 한 가지 실험
