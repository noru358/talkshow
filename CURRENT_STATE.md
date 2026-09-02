# CURRENT STATE

Updated: 2026-09-02 KST

## Current phase
**2/7 저장소/MD 체계 + Pilot 001 원소스 준비**

Progress:
1. 제작 원칙 확정 — mostly done
2. 저장소/MD 체계 — in progress
3. 원소스 수집 — Pilot 001 source selected
4. 대본 — next
5. 비주얼 바이블 — next
6. 제작 파이프라인/툴 — initial decision made
7. Pilot 001 완성 — pending

## Repository
현재 저장소: `noru358/-`
사용자 의도: 저장소 이름을 `talkshow`로 변경 후 이 프로젝트 전용으로 사용.
현재 연결된 GitHub 액션에는 repository rename이 없어 이름 변경만 수동 필요. 내용 작업은 현재 저장소에서 계속 진행 가능.

## Locked decisions
- 단순 커뮤니티 낭독/캡처 채널이 아니다.
- '커뮤 말투로 세상 얘기하는 채널'이 핵심.
- 실제 본문과 댓글을 반드시 원소스로 참고.
- 좋은 실제 댓글은 최소 변형.
- 3인 캐스트 우선.
- 세 번째 인물은 종종 관객/댓글창처럼 웃음, 정색, 당황만 담당할 수 있음.
- 역할은 캐릭터별로 고정하지 않음.
- 최소 정체성만 고정하고 논쟁/리액션 기능은 매회 유동적.
- 해석 가능한 뜬금포는 적극 허용.
- Creative QC 최소화.
- 수집 단계에서는 욕설/혐오 표현을 사전 순화하지 않고 맥락 보존. 공개본에서 비프/컷/자막 마스킹 등으로 처리.
- 초기 비주얼 방향: 저프레임 2D 컷아웃 + 커뮤니티 만화 감성.
- 장기 자동화 렌더러 후보: Remotion.

## Pilot 001 source
DCInside dcbest URL:
`https://gall.dcinside.com/board/view/?id=dcbest&no=459446&_dcbest=6&page=1`

관련 현상: 373년 동안 풀리지 않았다고 알려진 암호를 AI가 빠르게 해독했다는 이야기.

사용자가 직접 확인해 전달한 핵심 댓글 흐름:
- 댓글 A: `좆도 쓸모없는 거구만`
- 댓글 B: `사람들이 저기에 시간을 안들이게 되었으니 엄청 쓸모있음`
- 주변 리액션: `병신 ㅋㅋ`, `천재노 ㅋㅋㅋ` 등

주의: 현재 브라우징 경로에서는 DC 본문/댓글 직접 fetch가 차단되어 있어 위 댓글은 사용자 제공 원소스로 취급. 관련 사건 자체는 별도 기사에서 확인 가능.

## Next actions
1. Pilot 001 SOURCE → GOLD extraction
2. 실제 댓글을 거의 그대로 사용해 3인 script v0.1 제작
3. 같은 대본에 공개본 censor event 설계
4. 3인 캐릭터 최소 identity 초안
5. visual style 3안 제작/비교
6. 최종 스타일 선택 후 character asset pack 생성
7. 음성 테스트 → 립싱크 → Remotion/대체툴로 20~35초 영상 렌더

## Session handoff rule
사용자가 `다음 세션에서 이어가자`라고 하면:
1. 이 파일을 최신 상태로 덮어쓴다.
2. 결정이 장기 규칙이면 PROJECT_BIBLE.md 반영.
3. 제작 방식 변경이면 PRODUCTION_PIPELINE.md 반영.
4. 진행 중 에피소드는 해당 `episodes/Pxxx/EPISODE_SPEC.md`에 반영.
5. 다음 세션은 CURRENT_STATE.md부터 읽고 재기획하지 않는다.
