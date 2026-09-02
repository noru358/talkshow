# PILOT 001 — EPISODE SPEC

Status: SOURCE/GOLD prepared → script draft next
Target: 9:16 / 20–35 sec / 3 characters

## 1. Source

Primary community URL:
`https://gall.dcinside.com/board/view/?id=dcbest&no=459446&_dcbest=6&page=1`

Topic:
AI가 오랫동안 풀리지 않았다고 알려진 오래된 암호의 해독법을 빠르게 찾아냈다는 이야기.

Human-origin reaction material supplied from the comment thread:

- SOURCE_COMMENT_A: `좆도 쓸모없는 거구만`
- SOURCE_COMMENT_B: `사람들이 저기에 시간을 안들이게 되었으니 엄청 쓸모있음`
- SOURCE_REACTION_1: `병신 ㅋㅋ`
- SOURCE_REACTION_2: `천재노 ㅋㅋㅋ`

Do not polish these into formal Korean.

## 2. Gold extraction

### GOLD 01 — dismissive first reaction
`좆도 쓸모없는 거구만`

Why it works:
커다란 기술 성취를 즉시 '쓸모없음'으로 깎는 짧고 무례한 인간 반응.

### GOLD 02 — one-line reversal
`사람들이 저기에 시간을 안들이게 되었으니 엄청 쓸모있음`

Why it works:
A의 '쓸모' 정의를 그대로 받아서 역으로 뒤집는다. 설명이 길지 않고 한 줄로 A를 바보처럼 만든다.

### GOLD 03 — social proof / reaction
`병신 ㅋㅋ` / `천재노 ㅋㅋㅋ`

Why it works:
제3자의 웃음/조롱이 GOLD 02의 펀치라인을 사회적으로 인증한다.

## 3. Script constraints

- 실제 댓글을 중심으로 쓴다.
- 신규 AI 대사는 사건 소개와 최소 브리지 위주.
- 3명이 모두 균등하게 말하지 않는다.
- 결론/교훈을 붙이지 않는다.
- 마지막을 억지 뜬금포로 새로 발명하지 않는다.

## 4. Script v0.1 — RAW MASTER

CHAR_A: `373년 동안 못 풀던 암호를 AI가 44분 만에 풀었대.`

CHAR_B: `근데 이거 좆도 쓸모없는 거구만.`

CHAR_A: `사람들이 저기에 시간을 안 들이게 됐으니까 엄청 쓸모있는 거 아님?`

CHAR_C: `ㅋㅋㅋㅋ 병신.`

CHAR_B: `아니 씨발 그 뜻이 아니라—`

CHAR_C: `천재노ㅋㅋㅋ`

CUT.

Notes:
- CHAR_A/B/C는 아직 캐릭터 이름으로 lock하지 않는다. 캐스팅 테스트 후 데이빗/덕구/3번에게 배치.
- 핵심 웃음은 CHAR_A의 반박 이후 CHAR_C 반응. 마지막 설명 금지.
- `아니 씨발 그 뜻이 아니라—`는 bridge이므로 실제 음성 테스트에서 불필요하면 삭제 가능.

## 5. Public censor plan — draft

RAW는 내부 제작용으로 유지.

공개본 후보:
- `좆도` → 첫 음절 후 BLEEP 또는 단어 전체 짧은 BLEEP. 자막은 `좆□`/`ㅈㄴ` 같은 방식 중 비주얼 바이블에서 확정.
- `병신` → 첫 음절+BLEEP 또는 reaction zoom과 동시에 음소거.
- `씨발` → `씨-` + BLEEP, 또는 CHAR_C 웃음 컷으로 덮기.

검열 타이밍 자체를 코미디 리듬으로 사용 가능.

## 6. Beat skeleton — provisional

B0 0–3s: 사건을 1문장/시각 카드로 이해시킴.
B1: CHAR_B의 dismissive line.
B2: CHAR_A의 one-line reversal.
B3: CHAR_C가 즉시 터짐.
B4: CHAR_B가 말 돌리려 함.
B5: CHAR_C가 한 번 더 찌르고 바로 컷.

실제 초 단위 길이는 TTS 생성 후 확정.

## 7. Episode-specific visual needs

- `373년` / 오래된 암호라는 것을 1초 안에 보여주는 간단한 카드 또는 낡은 숫자열 이미지풍 재구성.
- 기본 3인 stage.
- CHAR_B close-up.
- CHAR_A 무심한 반박 shot.
- CHAR_C laugh/reaction close-up.
- censor용 punch-in / BLEEP visual event.

원문 DC 캡처를 메인 화면으로 사용하지 않는다.

## 8. Next

1. Character casting test
2. TTS voice prototype
3. TTS 길이 기반 beat timing
4. 3인 visual identity / stage style test
5. Render prototype
