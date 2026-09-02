# CURRENT STATE

Updated: 2026-09-02 KST

## Current phase
**4/7 Character Asset Package — in progress**

Progress:
1. 제작 원칙 확정 — done
2. 저장소/MD 체계 — done (repo rename still manual)
3. 캐릭터/그림체 확정 — done
4. 에셋 패키지 제작 — current
5. 대본·콘티 결합 — next
6. 음성·렌더 파이프라인 — next
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
- 최종 그림체: 이전 비교안의 **A안**, 초단순/거친 손그림 커뮤니티 웹툰 스타일.
- B/C/E/F/G/K/L/M/Q/R 10개 캐릭터 디자인을 cast pool로 확정.
- 캐릭터 역할은 고정하지 않는다.
- Pilot 001 임시 3인은 C/E/K로 시작. 이유는 실루엣·복장·에너지 대비가 크기 때문이며 영구 고정이 아님.
- 장기 자동화 렌더러 후보: Remotion.

## Character asset production
`assets/CHARACTER_ASSET_SPEC.md` created.
Pilot-first rule: 10명 전체 풀팩을 먼저 만들지 않는다. C/E/K 3명만 최소 에셋으로 P001을 완성하고, 영상에서 실제 부족한 에셋만 추가한다.

Minimal Pilot pack per C/E/K:
- seated neutral
- seated explaining
- seated deadpan
- seated big laugh
- seated shocked
- seated annoyed
- standing neutral
- mouth closed/mid/wide
- eyes open/half/closed

## Pilot 001 source
DCInside dcbest URL:
`https://gall.dcinside.com/board/view/?id=dcbest&no=459446&_dcbest=6&page=1`

관련 현상: 373년 동안 풀리지 않았다고 알려진 암호를 AI가 빠르게 해독했다는 이야기.

사용자가 직접 확인해 전달한 핵심 댓글 흐름:
- 댓글 A: `좆도 쓸모없는 거구만`
- 댓글 B: `사람들이 저기에 시간을 안들이게 되었으니 엄청 쓸모있음`
- 주변 리액션: `병신 ㅋㅋ`, `천재노 ㅋㅋㅋ` 등

## Next actions
1. C/E/K Pilot 최소 character asset sheet 제작
2. Pilot 고정 배경/좌석 layout 제작
3. P001 대본을 C/E/K에 실제 캐스팅
4. shot-by-shot storyboard + censor events 작성
5. voice identity test
6. low-frame mouth switching + Remotion prototype
7. 20–35초 P001 렌더

## Session handoff rule
사용자가 `다음 세션에서 이어가자`라고 하면:
1. 이 파일을 최신 상태로 덮어쓴다.
2. 결정이 장기 규칙이면 PROJECT_BIBLE.md 반영.
3. 제작 방식 변경이면 PRODUCTION_PIPELINE.md 반영.
4. 진행 중 에피소드는 해당 `episodes/Pxxx/EPISODE_SPEC.md`에 반영.
5. 다음 세션은 CURRENT_STATE.md부터 읽고 재기획하지 않는다.
