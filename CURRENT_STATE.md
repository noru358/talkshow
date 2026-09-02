# CURRENT STATE

Updated: 2026-09-02 KST

## Current phase
**4/7 Character Asset Package — in progress**

Progress:
1. 제작 원칙 확정 — done
2. 저장소/MD 체계 — done (repo rename still manual if not yet done)
3. 캐릭터/그림체 확정 — done
4. 에셋 패키지 제작 — current
5. 대본·콘티 결합 — next
6. 음성·렌더 파이프라인 — next
7. Pilot 001 완성 — pending

## Repository
현재 작업 저장소: `noru358/-`
사용자 의도: 저장소 이름을 `talkshow`로 변경 후 이 프로젝트 전용으로 사용.
현재 연결된 GitHub 액션에는 repository rename이 없어 이름 변경만 수동 필요. 이름이 이미 바뀌었다면 다음 세션에서 `noru358/talkshow`를 우선 확인할 것.

## Locked concept decisions
- 단순 커뮤니티 낭독/캡처 채널이 아니다.
- 핵심 정의: **커뮤 말투로 세상 얘기하는 3인 캐릭터 토크쇼**.
- 실제 본문과 댓글을 반드시 원소스로 참고한다.
- 좋은 실제 댓글은 최소 변형한다. AI의 주역은 새 대사 발명보다 선택·캐스팅·축약·브리지다.
- 3인 캐스트 우선. 매 에피소드에서 3명 모두 균등 발화할 필요 없음.
- 세 번째 인물은 종종 관객/댓글창처럼 웃음, 정색, 당황 등 리액션만 담당할 수 있음.
- 역할은 캐릭터별로 고정하지 않는다. 누가 헛소리/반박/팩트체크/리액션을 맡는지는 에피소드·비트마다 유동적.
- 캐릭터는 성별/외형/아주 핵심적인 인상 같은 최소 정체성만 고정.
- 해석 가능한 뜬금포/latent-context 드립은 적극 허용.
- Creative QC 최소화. 이상함 자체를 결함으로 보지 않는다.
- 수집 단계에서는 욕설/혐오 표현을 사전 순화하지 않고 맥락 보존. 공개본에서 비프/컷/자막 마스킹/화면 전환 등으로 처리.

## Visual lock — CRITICAL
- 최종 그림체는 이전 스타일 비교안의 **A안**.
- 특징: 초단순, 거친 손그림 선, 평면적인 채색, 최소 디테일, 커뮤니티 웹툰/낙서 만화 느낌, 일부러 과하게 매끈하지 않음.
- **B/C/D 계열처럼 AI 애니/웹툰 느낌으로 미려해지면 실패.**
- 앞으로 모든 캐릭터·배경·소품·컷어웨이는 이 A안 그림체와 동일한 시각언어를 유지한다.
- 사용자는 현재 최종 10인 시안의 퀄리티 자체는 OK 판정함.

## Cast pool lock
확정 캐릭터 디자인 10명:
`B, C, E, F, G, K, L, M, Q, R`

Pilot 001 임시 3인:
`C / E / K`
- 영구 주연 확정 아님.
- 첫 영상에서 실루엣·복장·표정 대비가 좋아 테스트용으로 선택.
- 이후 역할/멤버 구성은 유동적.

## Asset deliverable rule — CRITICAL
사용자가 **인포그래픽 형태를 명시적으로 금지**함.
다음 세션에서 에셋을 만들 때:
- 보기 좋은 concept board/infographic 한 장으로 합치지 말 것.
- AI/렌더러가 실제 재사용 가능한 형태로 만들 것.
- 우선순위: 개별 PNG(가능하면 투명 배경) + manifest/MD/JSON.
- 캐릭터별 pose/expression/mouth/eye state를 개별 파일로 분리.
- 배경은 캐릭터 없는 clean plate로 별도 파일.
- 소품도 필요 시 개별 파일.
- 한 이미지 안에 설명 문구/라벨/테이블/비교표를 넣지 말 것.
- 사용자 QC용 preview가 필요하더라도 실제 원본 개별 에셋이 우선이며 preview는 부차적이어야 함.

### Important mistake to avoid
직전 에셋 제작 시 생성 결과가 다시 스티커 시트/보드/인포그래픽 성격으로 나와 사용자 요구를 충족하지 못했음.
다음 세션은 이 부분을 재시도하는 데서 시작해야 함.

## Character asset production target
`assets/CHARACTER_ASSET_SPEC.md` 기준.
Pilot-first rule: 10명 전체 풀팩을 먼저 만들지 않는다. C/E/K 3명만 최소 에셋으로 P001을 완성하고, 영상에서 실제 부족한 에셋만 추가한다.

Minimal Pilot pack per C/E/K:
- seated neutral
- seated explaining
- seated deadpan
- seated big laugh
- seated shocked
- seated annoyed
- standing neutral
- mouth closed / mid / wide
- eyes open / half / closed

### Preferred machine-readable organization
Example:
```text
assets/
  characters/
    C/
      base/
      expressions/
      mouths/
      eyes/
      poses/
      manifest.json
    E/
    K/
  set/
    background_clean.png
    desk.png
    props/
  STYLE_LOCK.md
```

## Fixed talk-show set target
Next visual task includes a clean, reusable 9:16 talk-show set in the SAME A-style.
Requirements:
- no characters in master background
- 3-seat/3-position composition
- can crop to 3-shot, 2-shot, 1-shot
- open area for topic/source/cutaway insert
- minimal detail; should not visually overpower dialogue
- separate clean plate / foreground desk if compositing benefits from it

## Pilot 001 source
DCInside dcbest URL:
`https://gall.dcinside.com/board/view/?id=dcbest&no=459446&_dcbest=6&page=1`

관련 현상: 373년 동안 풀리지 않았다고 알려진 암호를 AI가 빠르게 해독했다는 이야기.

사용자가 직접 확인해 전달한 핵심 댓글 흐름:
- 댓글 A: `좆도 쓸모없는 거구만`
- 댓글 B: `사람들이 저기에 시간을 안들이게 되었으니 엄청 쓸모있음`
- 주변 리액션: `병신 ㅋㅋ`, `천재노 ㅋㅋㅋ` 등

## Immediate next actions
1. **C/E/K 실제 개별 제작용 에셋 생성 재시도** — no infographic, A-style lock.
2. **고정 토크쇼 세트 clean plate 생성** — no characters, A-style lock.
3. 생성 파일을 실제 asset naming/manifest 구조로 정리.
4. 에셋 QC 후 P001 대본을 C/E/K에 캐스팅.
5. shot-by-shot storyboard + censor events 작성.
6. voice identity test.
7. low-frame mouth switching + Remotion prototype.
8. 20–35초 P001 렌더.

## Session handoff rule
사용자가 `다음 세션에서 이어가자`라고 하면:
1. 이 파일을 최신 상태로 덮어쓴다.
2. 결정이 장기 규칙이면 PROJECT_BIBLE.md 반영.
3. 제작 방식 변경이면 PRODUCTION_PIPELINE.md 반영.
4. 진행 중 에피소드는 해당 `episodes/Pxxx/EPISODE_SPEC.md`에 반영.
5. 별도 handoff 파일이 있으면 함께 갱신.
6. 다음 세션은 CURRENT_STATE.md부터 읽고 재기획하지 않는다.
