# CURRENT STATE

Updated: 2026-09-04 KST
Status: **SERIES V2 VISUALS LOCKED — FREE 3-VOICE REFERENCE PACK READY / FIRST OMNI PILOT AWAITING USER APPROVAL**

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

## 2026-09-04 visual completion

`assets/V2_VISUAL_LOCK_20260904.md` is now the canonical visual lock record.

- `RIGHT_MASTER_V2` master pack locked
- four set-specific 16:9 cast stills locked
- canonical binaries preserved under `assets/v2_locked/`
- HOME / CONVENIENCE / HANGANG / ROOFTOP usage conditions recorded
- do not return to empty-set or cast-still regeneration without a newly identified hard defect

## 바로 다음 행동

### Step 1 — USER REVIEW OF FREE VOICE PREVIEWS — DONE
- LEFT / CHAR_B: Gaeun outdoors
- CENTER / CHAR_06: Harin
- RIGHT / RIGHT_MASTER_V2: Taemin
- this review consumed 0 credits

### Step 2 — FREE REFERENCE PACK — DONE
- LEFT / CHAR_B: Gaeun outdoors catalog preview
- CENTER / CHAR_06: Harin catalog preview
- RIGHT / RIGHT_MASTER_V2: Taemin catalog preview
- packaged as `TALKSHOW_V2_SELECTED_VOICE_REFERENCE_PACK.zip`
- no new TTS generation; 0 credits consumed

### Step 3 — FIRST OMNI REFERENCE PILOT — READY / NOT SUBMITTED
- authority: `episodes/P001/V2_OMNI_REFERENCE_PILOT_PACKAGE.md`
- use the V2 HOME cast still plus the three free catalog audio previews
- generate P001 Scene B once only after explicit user approval
- first QC determines whether free audio references are sufficient voice anchors
- do not buy exact-line TTS before this test proves it is necessary

### Step 4 이후
- lock the reference-audio route if speaker assignment and timbre are stable
- use exact-line TTS/audio replacement only as a fallback for material drift
- 9:16 edit → publish → 24h/7d learning

## 현재 실제 blocker

The visual and free-voice-pack blockers are cleared. The only active blocker is explicit user approval immediately before one credit-consuming Omni Reference video generation. Voice names in prose are not treated as a lock; the three actual audio files must be attached and mapped to LEFT/CENTER/RIGHT.

## Mandatory pre-generation inheritance check

Before presenting or submitting any scene prompt, compare the executable prompt against every active series-level lock. Do not assume that a rule stored in a core document will influence generation unless it is written directly into the scene prompt.

Required checks:
- visual identity / set / position lock is present in the executable prompt
- selected voice-reference files and speaker mapping are present
- `REACTION_RULES_V2` is translated into scene-specific visible actions, not generic wording
- reactions remain causally staggered, but are visibly larger than V1 at the actual framing scale
- the prompt does not reintroduce superseded V1 phrases such as `subtle acting`, `small reactions`, or blanket `no large gestures`
- generation count, model, resolution, duration and credit gate match the current approved task

If any check fails, revise the execution package before requesting approval or spending credits.

## 응답 규칙

모든 talkshow 응답은 다음으로 시작한다.
1. 큰 흐름
2. 현재 세부 단계
3. 이번 턴 완료조건
