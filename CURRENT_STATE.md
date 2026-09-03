# CURRENT STATE

Updated: 2026-09-03 KST  
Status: **SERIES V2 RELOCK ACTIVE — RIGHT_MASTER_V2 + FOUR SET MASTERS are the immediate work**

## 지금의 단일 결론

P001 V1의 sparse-room / restrained-performance baseline을 최종 시리즈 형태로 밀지 않는다.

사용자 판단으로 시리즈 기본형을 한 번 재락한다. 이유는 V1이 재현성은 확보했지만 시각적으로 허전하고 저예산처럼 보였고, gray-hoodie male styling과 보이스/리액션 에너지도 반복 캐스트 채널 기준으로 부족했기 때문이다.

V2 기준과 변경 이유의 전체 기록은 `SERIES_V2_RELOCK.md`가 현재 작업의 상세 권위 문서다.

## 큰 파이프라인은 유지

`Radar/Source → Thread/Gold → Episode Package → User Production → Defect QC → Distribution/Performance Learning`

콘텐츠 원천성/성과 루프는 유지하고, 현재는 그 안의 **반복 제작 visual/voice/performance baseline**만 재락 중이다.

## P001 V1 상태 — 보존하되 현재 next action 아님

기존 파일은 삭제/덮어쓰기 금지. Git history가 아니라 실제 에피소드 증거로 보존한다.

- source: `episodes/P001/SOURCE_PACK.md`
- Scene A V1: `260903_0001_video_edit_2387.mp4`, 기존 PASS 기록 유지
- Scene A V1 exact prompt/QC: `episodes/P001/SCENE_A_LOCK.md`
- Scene B V1 package: `episodes/P001/SCENE_B_PACKAGE.md`
- Scene B QC는 사용자 지시로 현재 건너뜀
- Scene A의 과거 `재생성 금지`는 V1 내부 기록일 뿐이며, V2에서는 필요하면 P001 씬을 얼마든 다시 생성할 수 있음

## V2 visual architecture

> **CHARACTER MASTER PACKS → four EMPTY SET MASTERS → per-set 3-person CAST STILL → fixed-first-frame I2V → edit/crop**

### 반복 캐스트
- CHAR_B / white-T-shirt woman
- CHAR_06
- 기존 gray-hoodie male의 동일 identity를 유지하되 hair/outfit만 바꾼 `RIGHT_MASTER_V2`

### RIGHT_MASTER_V2
Exact spec: `assets/RIGHT_MASTER_V2_SPEC.md`

잠금 방향:
- 동일 얼굴/비율/그림체 유지
- black natural Korean 6:4 side part, medium-short, neat tapered sides
- dark brown ribbed cardigan
- plain white crew-neck T-shirt
- charcoal wide-straight trousers
- dark low-profile sneakers
- no glasses / no bag / no bag strap / no visible logo
- ordinary but put-together Seoul man in late 20s/early 30s; not idol, not luxury, not costume streetwear

### Four-set pool — 전부 사용
Exact prompts: `assets/SET_MASTER_V2_PACK.md`

1. `SET_A_HOME` — Seoul studio/officetel living room — **main/default**
2. `SET_B_CONVENIENCE` — Korean convenience-store-front table — **signature/high-energy**
3. `SET_C_HANGANG` — Hangang night picnic — **variation/special**
4. `SET_D_ROOFTOP` — Seoul villa rooftop — **variation/special**

세트 4개 중 하나만 고르는 계획이 아니다. 모두 empty master로 생성/락하고 회차별로 선택한다.

### Reproducibility rules
- 16:9 generation master 유지
- 배경 prose 재생성 대신 locked empty set image를 strict reference로 사용
- 각 세트마다 set image + three character packs로 canonical 3-person cast still 생성
- 이후 해당 still을 I2V exact first frame으로 재사용
- 4세트 모두 비슷한 face scale / LEFT-CENTER-RIGHT screen zones / medium-wide camera grammar 유지
- 상체와 손 제스처 공간을 확보

## Voice V2
Registry: `assets/VOICE_REGISTRY.md`

- CHAR_B: 평범한 2030 한국 여성 생활톤 + 기존 skeptical/indignant 결은 유지하되 **더 생기 있게**, cold/monotone 금지
- CHAR_06: 기존 calm 방향을 폐기하고 **더 밝고 활기찬 conversational energy**
- RIGHT_MASTER_V2: ordinary 2030 Korean male low-mid everyday voice, playful/quick social timing, natural short laugh
- final voice IDs 아직 UNASSIGNED
- Seedance native audio는 계속 performance/lip-sync guide; 최종은 fixed-ID voice-to-voice

## Reaction / acting V2
V1보다 명확히 크게 간다.

유지:
- punchline을 미리 예상하지 않기
- 인과적/순차적 반응
- 모두 동시에 같은 반응 금지

새로 허용/권장:
- 더 큰 eye movement / head turn / facial reaction
- short torso lean/recoil
- shoulder bounce
- one-hand gesture
- two-hand gesture
- brief raised fist / small celebratory fist
- open-palmed disbelief
- brief table tap if geometry remains stable

금지:
- full-body flailing
- constant gesturing
- extreme mouth opening / eye squeeze deformation
- hand/neck/body warping

원칙: **bigger and funnier, but causally staged and model-safe.**

## 콘텐츠/성과 락 — 변경 없음

- real Korean community posts/comments primary source
- AI-written spoken beats <= 30%
- AI-created comedic payoff approximately 0%
- generation master 16:9 / distribution master 9:16
- first distribution: YouTube Shorts; Reels/TikTok cross-post candidates
- Distribution & Performance는 다음 소재/실험가설에 피드백하되 자동 대사 최적화로 수렴시키지 않음

## 바로 다음 행동

### Step 1 — RIGHT_MASTER_V2
- `assets/RIGHT_MASTER_V2_SPEC.md`의 exact prompt를 사용
- 기존 recurring male master image/package를 reference로 반드시 첨부
- 얼굴/identity를 바꾸지 않고 hair/outfit만 update
- 생성 후 identity/style/outfit QC → lock

### Step 2 — FOUR EMPTY SET MASTERS
- `assets/SET_MASTER_V2_PACK.md`의 A/B/C/D exact prompts 사용
- 우선 empty set만 각각 생성
- 캐릭터를 동시에 합성하지 않음
- 네 empty set을 QC/lock한 다음 각 set + 3 character packs로 3-person cast still 생성

### Step 3 이후
- four set-specific cast still lock
- fixed voice ID auditions/lock
- V2 reaction grammar로 실제 P001 또는 다음 production clip 생성
- 9:16 edit → publish → 24h/7d learning

## 현재 실제 blocker

`RIGHT_MASTER_V2`를 ChatGPT image edit로 직접 생성하려면 이 세션에 기존 recurring male master image가 실제 이미지 입력으로 있어야 한다. GitHub에는 이미지 asset이 보존되어 있지만, repository binary reference만으로 이 세션의 image edit target을 자동 대체하지 않는다.

따라서 프롬프트/설계는 완료 상태이고, 실제 동일 identity 이미지 편집은 해당 male master 이미지가 이 세션에 제공되는 즉시 실행한다.

## 응답 규칙

모든 talkshow 응답은 다음으로 시작한다.
1. 큰 흐름
2. 현재 세부 단계
3. 이번 턴 완료조건
