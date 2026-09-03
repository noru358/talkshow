# CURRENT STATE

Updated: 2026-09-03 KST  
Status: **P001 Scene A locked / Scene B package next**

## 지금의 단일 결론

세트 테스트로 돌아가지 않는다. 사용자가 외부 도구에서 직접 제작한다.

`Radar/Source → Thread/Gold → Episode Package → User Production → Defect QC → Distribution/Performance Learning`

독립 소프트웨어 에이전트들이 배포된 상태는 아니다. 현재 ChatGPT가 상류 편집 역할과 QC/학습 역할을 합쳐 수행하고 사용자가 생성·편집·게시한다.

## P001

- source: `episodes/P001/SOURCE_PACK.md`
- Scene A: `260903_0001_video_edit_2387.mp4`, 7.104초, 영상 PASS, 재생성 금지
- Scene A exact prompt/QC: `episodes/P001/SCENE_A_LOCK.md`
- Scene B: 8–12초, 인간 원문 반전 + 사회적 펀치
- 최종: 약 15–22초, 2 scenes
- 폐기: 38.5초/6숏 계획, `BRIDGE_01`

## 잠금

### 영상 생성

- `SET_MASTER_01 → CAST_MASTER → fixed-first-frame I2V → edit crop`
- Seedance 2.0 Mini / 480p / 16:9
- 같은 3인 cast-master와 3개 master pack 재사용
- 반응은 trigger 이후 0.1–0.4초 간격으로 순차 시작

### 화면비

- **generation master: 16:9**
- **distribution master: 9:16**
- P001은 세로 캔버스 안에 16:9 원본을 그대로 작게 레터박스하는 방식으로 끝내지 않는다.
- 16:9 master를 이용하되 편집에서 speaker punch-in/crop, 상단 hook, 하단 subtitle safe zone으로 9:16을 구성한다.
- 이 결정은 기존 visual lock을 깨지 않으면서 Shorts/Reels/TikTok용 최종물을 세로 네이티브로 만든다.

### 음성

Seedance의 회차별 랜덤 음성을 최종 캐릭터 음성으로 수용하지 않는다.

잠금된 방식:
1. I2V에는 현재처럼 실제 대사를 넣어 입 모양·호흡·연기를 얻는다.
2. 생성 음성은 performance guide로만 사용한다.
3. 발화자별 오디오 구간을 분리한다.
4. ElevenLabs Voice Changer의 multilingual model로 캐릭터별 고정 voice ID에 변환한다.
5. 타이밍을 유지해 원 영상에 교체한다.
6. 웃음/겹말이 분리되지 않으면 그 짧은 구간만 같은 voice ID의 TTS로 대체한다.

따라서 무성 I2V로 바꾸지 않으며 기존 프롬프트 문법도 유지한다. P001 공개 전 세 캐릭터의 실제 voice ID를 한 번 정해 이후 변경하지 않는다. 현재 ID는 미지정이며 이는 **게시 blocker**, Scene B 영상 생성 blocker는 아니다.

### AI 신규 대사

측정 단위는 출처가 붙은 **spoken beat**다.

- 모든 AI-written spoken beats ≤ 30%
- AI가 새로 만든 comedic payoff = 원칙적으로 0%
- source-derived factual setup은 AI-written으로 계산
- P001은 `BRIDGE_01` 삭제 후 1/5 = 20%

## 성과 담당

별도 논리 역할 `Distribution & Performance`를 추가한다. 초기에는 ChatGPT가 담당한다.

- 1차 배포: YouTube Shorts
- 동일 9:16 마스터 교차 배포 후보: TikTok, Instagram Reels
- 핵심: 시청 선택률/초반 이탈, 평균 시청시간·완주율·재시청, 공유, 댓글, 구독/팔로우 전환
- 성과 데이터는 GOLD 유형·hook·길이·interaction 방식과 연결해 회차 폴더에 기록
- 성과 역할은 대사를 자동 재작성하지 않는다. 다음 소재 선택과 실험 가설만 제안한다.

## 다음 행동

1. `episodes/P001/PRODUCTION_PACKAGE.md` 기준으로 Scene B 프롬프트를 확정한다.
2. 사용자가 Scene B를 TopView에서 1회 생성한다.
3. ChatGPT가 defect QC한다.
4. P001 최종 편집 전에 세 voice ID를 배정하고 Scene A/B 발화를 voice-to-voice 변환한다.
5. 9:16 배포본을 만들고 게시 후 24h/7d 성과를 같은 package에 기록한다.

## 응답 규칙

모든 talkshow 응답은 다음으로 시작한다.
1. 큰 흐름
2. 현재 세부 단계
3. 이번 턴 완료조건
