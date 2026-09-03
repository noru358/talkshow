# TALKSHOW — SERIES V2 RELOCK

Updated: 2026-09-04 KST  
Status: **ACTIVE — visuals/voices/reaction baseline established; production focus shifted to first complete episode**

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

The following prior next-actions are now superseded:
- do not treat `episodes/P001/SCENE_B_PACKAGE.md` as the immediate next action
- Scene B QC is skipped by explicit user decision
- `episodes/P001/V2_OMNI_REFERENCE_PILOT_PACKAGE.md` remains useful evidence but is no longer the active production target
- Scene A may be regenerated later; the previous `do not regenerate` rule is no longer a series-level constraint
- `SET_MASTER_01` remains a validated reproducibility baseline, not the preferred final series set

The current goal is to produce a real complete episode rather than another isolated pilot-for-pilot test.

## Series V2 locked decisions

### 1. Recurring cast
Keep the current three-person recurring core:
- `CHAR_B` / white-T-shirt woman
- `CHAR_06`
- current recurring male identity / `RIGHT_MASTER_V2`

Character face identity and base drawing language remain the authority. Episode-specific locked images may contain later clothing refinements; when prose and the active visual reference conflict, the active image controls that episode unless a newer explicit text lock says otherwise.

### 2. RIGHT male redesign
The old gray hoodie and messy-hair styling are retired as the preferred recurring styling.

The reusable target remains:
- ordinary but put-together Seoul man in his 20s/early 30s
- contemporary Korean daily/minimal casual rather than streetwear costume or idol styling
- no bag / no bag strap
- no glasses
- simple enough to reproduce in low-fi 2D

Historical exact V2 styling is defined in `assets/RIGHT_MASTER_V2_SPEC.md`, but later episode-specific visual locks can supersede outfit details visually.

### 3. Four recurring sets, all retained
V2 uses a set pool rather than one universal room.

- `SET_A_HOME` — Seoul studio/officetel living room; main/default
- `SET_B_CONVENIENCE` — convenience-store-front table; signature/high-energy
- `SET_C_HANGANG` — Hangang night picnic; variation/special
- `SET_D_ROOFTOP` — Seoul villa rooftop night hangout; variation/special

All four are valid production sets. Do not discard C/D merely because A/B are used more often.

### 4. Reproducibility architecture V2

Base V2 architecture:

> **CHARACTER MASTER PACKS → four EMPTY SET MASTERS → per-set 3-person CANONICAL CAST STILL → shot-specific derived first-frame only when needed → fixed-first-frame I2V → edit/crop**

Do NOT ask the video model to rebuild a location from prose every episode.

For each set:
1. generate and lock one empty set master
2. use that exact set image as strict spatial/style reference
3. attach the three existing character packs
4. generate one canonical three-person still for that set
5. use the canonical still directly for ordinary clips
6. when a scene must visibly begin with a different pose/prop state, make the minimum canon-derived first-frame still that changes only that starting state

Do not create a large shot-family for completeness.

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

Selected free voice references:
- LEFT / CHAR_B: `Gaeun outdoors`
- CENTER / CHAR_06: `Harin`
- RIGHT male: `Taemin`

V2 character direction:
- `CHAR_B`: ordinary 20s/30s Korean woman, friendly everyday tone, somewhat lively; retains skeptical/indignant edge but is NOT cold, monotone or permanently deadpan
- `CHAR_06`: noticeably more lively, bright and energetic; sincere, confident, conversational; not influencer/MC or anime-cute
- RIGHT male: ordinary 20s/30s Korean man, playful low-mid everyday tone, quick social timing, short natural laugh; not announcer/comedy-actor macho voice

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

### 9. Real-episode opening / first-frame grammar
The fixed first-frame rule applies to each generated clip, not necessarily to the entire edited episode.

A canonical cast still is the visual authority. It is not a command that every scene must literally begin from the same resting pose.

For a recurring internet-post opener:
- CENTER may already hold a smartphone in a canon-derived opening still;
- the clip then starts immediately on the topic hook instead of spending generation time reaching for a newly invented phone;
- the exact spoken phrase should remain flexible (`야 이거 봐`, `이거 봤어?`, or direct source claim) rather than using a formal canned `오늘의 주제!` every episode.

For continuity between AI clips:
- prefer intentional editorial hard cuts between canon-derived stills;
- do not automatically use the previous generated clip's last frame as the next first frame, because that compounds identity/style drift;
- use last-frame chaining only when a real continuous action requires it and the visual risk is worth it.

The final 9:16 short gets perceived shot variation from editorial crop/punch-in, not AI camera movement.

## Current execution order — updated 2026-09-04

1. V2 recurring visual direction — DONE.
2. Free recurring voice references selected — DONE (`Gaeun outdoors / Harin / Taemin`).
3. P001 Omni pilot package — preserved but no longer active.
4. User selected the convenience-store-front three-person image supplied in the 2026-09-04 session as the base for the first full episode — ACTIVE VISUAL AUTHORITY FOR P002.
5. Source/storyboard agent selected a real-source P002 topic and created `episodes/P002/SOURCE_PACK.md` — DONE.
6. Full two-clip episode storyboard created at `episodes/P002/FULL_EPISODE_PACKAGE.md` — DONE.
7. Create only one new visual asset next: `P002_OPENING_STILL`, derived from the user's current convenience image with CENTER already holding a phone. Do not redesign anything else.
8. Generate Clip 1 once at 8 sec, QC it as production footage rather than a pilot.
9. Generate Clip 2 once at 8 sec only if Clip 1 has no hard blocker.
10. Assemble 9:16 distribution master with editorial punch-ins and subtitle/localization in post.
11. Publish and enter 24h/7d performance-learning loop.

## Repository integrity note

As of the 2026-09-04 GitHub inspection, `CURRENT_STATE.md` / older handoff prose claimed that `assets/V2_VISUAL_LOCK_20260904.md` and binaries under `assets/v2_locked/` were preserved, but those paths were not present on the inspected `main` tree. Do not claim those binaries are safely mirrored until that is actually verified.

The user-supplied convenience image in the current session is therefore treated as an active external visual authority, not as a GitHub-resident binary.

## What must NOT be lost in later sessions

- V2 was reopened intentionally because V1 looked too sparse/cheap and too restrained, not because V1 failed basic reproducibility.
- Four sets are wanted, not one replacement set.
- Reference fidelity/reproducibility remains a top priority.
- Larger reactions and one/two-hand gestures are explicitly allowed.
- Fixed first frame means fixed start of each generated clip, not one universal pose for the whole finished episode.
- Real episodes may use a minimal canon-derived opening still such as CENTER already holding a phone.
- Do not drift back into pilot-for-pilot testing when a publishable 2 x 8 sec episode can validate the same system more usefully.
