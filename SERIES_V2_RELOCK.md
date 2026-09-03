# TALKSHOW — SERIES V2 RELOCK

Updated: 2026-09-03 KST  
Status: **ACTIVE — visual/voice/reaction baseline is being re-locked before further P001 production**

This file records the deliberate reopening of the series baseline after the first P001 visual lock. It exists so later sessions do not accidentally revert to the earlier sparse-room / restrained-performance assumptions.

## Why V2 was reopened

The earlier `SET_MASTER_01` was intentionally sparse because richer rooms had caused character/furniture grounding failures. That solved reproducibility, but the accepted result exposed a higher-level product problem:

- the empty beige room + one low table + floor-seated three-person composition looked too cheap and under-produced
- it did not feel like a strong recurring casual-chat series environment
- the gray-hoodie male looked visually under-designed compared with the rest of the cast
- native/random Seedance voices were not acceptable as recurring character identity
- acting/reaction controls were too restrained; the resulting energy was closer to a calm information/education channel than a comedy/chat channel

Therefore V2 intentionally accepts a little more visual complexity while preserving reproducibility through stricter reference hierarchy and locked first-frame stills.

## Relationship to P001 V1

Keep all P001 V1 files and locks as historical evidence. Do not delete them.

However, the following prior next-actions are PAUSED/SUPERSEDED during V2 relock:
- do not treat `episodes/P001/SCENE_B_PACKAGE.md` as the immediate next action
- Scene B QC is skipped for now by explicit user decision
- Scene A may be regenerated later; the previous `do not regenerate` rule is no longer a series-level constraint
- `SET_MASTER_01` remains a validated reproducibility baseline, not the preferred final series set

Once V2 visual + voice + reaction baseline is locked, P001 can be regenerated/recut using the new baseline.

## Series V2 locked decisions

### 1. Recurring cast
Keep the current three-person recurring core:
- `CHAR_B` / white-T-shirt woman
- `CHAR_06`
- current gray-hoodie male identity, redesigned visually as `RIGHT_MASTER_V2`

Character face identity and base drawing language remain the authority. V2 changes the male styling, sets, voice profiles, and acting range; it does not invent a new person.

### 2. RIGHT male redesign
The gray hoodie and messy hair are retired as the preferred recurring styling.

Target:
- ordinary but put-together Seoul man in his 20s/early 30s
- contemporary Korean daily/minimal casual rather than streetwear costume or idol styling
- no bag / no bag strap
- no glasses
- simple enough to reproduce in low-fi 2D

Final V2 styling is defined in `assets/RIGHT_MASTER_V2_SPEC.md`.

### 3. Four recurring sets, all retained
V2 uses a set pool rather than one universal room.

- `SET_A_HOME` — Seoul studio/officetel living room; **main/default**
- `SET_B_CONVENIENCE` — convenience-store-front table; **signature/high-energy**
- `SET_C_HANGANG` — Hangang night picnic; **variation/special**
- `SET_D_ROOFTOP` — Seoul villa rooftop night hangout; **variation/special**

All four are valid production sets. Do not discard C/D merely because A/B are used more often.

### 4. Reproducibility architecture V2

The V2 architecture is:

> **CHARACTER MASTER PACKS → four EMPTY SET MASTERS → per-set 3-person CAST STILL → fixed-first-frame I2V → edit/crop**

Do NOT ask the video model to rebuild a location from prose every episode.

For each set:
1. generate and lock one empty set master
2. use that exact set image as strict spatial/style reference
3. attach the three existing character packs, including `RIGHT_MASTER_V2`
4. generate one canonical three-person still for that set
5. lock that still as the first frame for clips using the set

This deliberately separates background generation from character compositing, matching the user's requested workflow.

### 5. Shared composition geometry
To improve cross-set consistency:
- generation master remains 16:9
- default camera remains fixed, frontal or very slightly above eye level
- medium-wide group framing
- three faces clearly visible at similar scale across all sets
- stable LEFT / CENTER / RIGHT screen zones within a given cast still
- enough upper-body/hand room for gestures
- furniture may change by location, but the interaction triangle and face scale should remain similar

Seat assignment is episode-specific unless a later lock changes this.

### 6. Voice direction V2
Use fixed recurring voice IDs. Seedance audio remains performance/lip-sync guide only.

V2 character direction:
- `CHAR_B`: ordinary 20s/30s Korean woman, friendly everyday tone, somewhat lively; retains skeptical/indignant edge but is NOT cold, monotone or permanently deadpan
- `CHAR_06`: noticeably more lively, bright and energetic; sincere, confident, conversational; not influencer/MC or anime-cute
- `RIGHT_MASTER_V2`: ordinary 20s/30s Korean man, playful low-mid everyday tone, quick social timing, short natural laugh; not announcer/comedy-actor macho voice

Detailed audition rules live in `assets/VOICE_REGISTRY.md`.

### 7. Reaction / acting V2
V1 over-optimized for stability. V2 increases entertainment energy.

Keep causal staggering, but increase visible reaction amplitude.

Allowed:
- clear eye direction changes
- more readable head turns
- visible smiles / incredulous expressions / offended stares
- short torso lean or recoil
- shoulder bounce on laughter
- one-hand gestures
- two-hand gestures when motivated
- brief raised fist / small celebratory fist
- open-palmed disbelief gesture
- brief table tap if geometry remains stable

Still avoid:
- everybody reacting at once
- constant gesturing
- full-body flailing
- extreme mouth opening
- tightly squeezed/deformed eyes
- neck/hand/body warping
- gestures crossing another character's face for long periods

Target principle:
> **bigger and funnier, but causally staged and model-safe.**

### 8. Content/source rules remain unchanged
The V2 relock does NOT change the editorial source discipline:
- real Korean community posts/comments remain primary source
- AI-written spoken beats <= 30%
- AI-invented comedic payoff should remain approximately 0%
- performance/distribution learning should change selection/experiments, not automatically rewrite dialogue into generic optimized copy

## Current execution order — updated 2026-09-04

1. ~~Finalize/generate `RIGHT_MASTER_V2`.~~ **DONE**
2. ~~Generate/QC the four recurring visual environments.~~ **DONE**
3. ~~Build and QC four three-character set-specific cast stills.~~ **DONE**
4. Preserve canonical binaries and SHA256 records in `assets/V2_VISUAL_LOCK_20260904.md`. **DONE**
5. Review the free 3+3+3 TopView voice preview shortlist. **DONE — Gaeun outdoors / Harin / Taemin selected**
6. Package the three selected free catalog previews as audio references. **DONE — 0 credits**
7. Prepare P001 Scene B as the first V2 Omni Reference pilot. **DONE — not submitted**
8. Obtain explicit user approval immediately before the one credit-consuming video generation. **ACTIVE**
9. QC speaker assignment, timbre similarity, exact dialogue and V2 reaction grammar.
10. Lock the free reference-audio route if it passes; use exact-line TTS/audio replacement only if it fails materially.
11. Resume distribution master (9:16), publishing and performance loop.

## What must NOT be lost in later sessions

- V2 was reopened intentionally because V1 looked too sparse/cheap and too restrained, not because V1 failed basic reproducibility.
- Four sets are wanted, not one replacement set.
- Reference fidelity/reproducibility remains a top priority.
- The male keeps his identity but receives new hair + clothing.
- CHAR_B voice must be more lively than the old dry/deadpan direction.
- CHAR_06 voice must be distinctly more energetic than the old calm profile.
- Larger reactions and one/two-hand gestures, including a brief fist gesture, are explicitly allowed.
