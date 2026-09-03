# P002 — FIRST FULL EPISODE PACKAGE

Updated: 2026-09-04 KST  
Status: **STORYBOARD LOCK CANDIDATE / NO VIDEO GENERATED YET**

## Goal

Stop doing isolated pilot-for-pilot tests. Build the first episode as an actual publishable short.

Target final length: about 16 seconds before optional end-hold.  
Generation plan: **2 x 8-second clips**, then 9:16 editorial crop/punch-in and subtitle/localization in post.

## Set / visual authority

Use the user-supplied convenience-store-front three-person image from the 2026-09-04 session as the active visual authority for P002.

Important hierarchy:
- the attached image controls the exact current faces, drawing style, clothing, table, props, seating and LEFT/CENTER/RIGHT geometry for this episode;
- do not force older prose descriptions from V1/V2 documents onto the image if they conflict with what is visibly locked in this current still;
- this binary is not yet mirrored in the GitHub repository, so the repository must not falsely claim that it is stored under `assets/v2_locked/`.

## New first-frame rule for real episodes

A canonical cast still is the **visual authority**, but it does not have to be the literal first frame of every generated shot.

For real episodes, make the minimum number of shot-specific derived first-frame stills needed for visible starting actions.

Each derived still must preserve the canonical image exactly except for the one required starting pose/prop state.

Do not chain every next clip from the previous AI video's last frame. That accumulates visual drift. Prefer a hard editorial cut between canon-derived stills.

## Opening grammar

Do not use a formal repeated line such as `오늘의 주제!` by default. It sounds like a host format and delays the hook.

Recurring visual device:
- CENTER has a phone and brings the internet post into the group.

Recurring linguistic device should stay flexible and natural:
- `야 이거 봐.`
- `이거 봤어?`
- or start directly on the source claim when the claim itself is strong enough.

The **visual routine can repeat; the exact spoken opener should not feel templated.**

## Clip 1 — 8 sec — hook + first social reaction

### First frame
Create one derived still from the user-supplied convenience cast image:
- preserve absolutely everything;
- only change CENTER so she is already holding a plain smartphone at chest height in one hand and looking at the screen;
- no readable phone-screen text;
- LEFT and RIGHT remain naturally idle and do not anticipate the topic.

This derived still is `P002_OPENING_STILL`.

### Dialogue
CENTER, reading the phone naturally:
`야 이거 봐. 회사들이 신입을 안 뽑아서 공무원으로 쏠린대.`

LEFT, after CENTER finishes:
`중고신입밭이라 신입연봉으로 괜찮은 사람 뽑기 최적기네.`

RIGHT stays silent in Clip 1.

### Performance beats
- CENTER starts already looking at the phone; small upward phone tilt while speaking.
- LEFT listens first, then turns clearly toward CENTER after the setup lands.
- LEFT delivers her line matter-of-factly, not as a prepared joke, with one visible palm-up explanatory gesture.
- RIGHT registers the implication late: eyes move first, then a clear head turn toward LEFT near the end.
- reactions are visibly larger than V1 but causally staggered.
- no simultaneous big laugh.

### End beat
Hold approximately 0.3–0.5 sec on RIGHT's `did you just say that?` look. This creates the cut point into Clip 2.

## Clip 2 — 8 sec — sting + reframing

### First frame
Use the original user-supplied convenience cast image as the first-frame authority if possible.

This is an intentional hard cut, not a fake continuous shot. The phone does not need to remain in CENTER's hand after the cut.

### Dialogue
RIGHT:
`진짜 신입이 뒤져감.`

CENTER:
`사다리가 치워져서 중간층이 최하층 된 거임.`

LEFT:
`최하층 급여로 중간층 쓰니까 회사 입장에선 좋겠지.`

### Performance beats
- RIGHT opens immediately with the dry sting, short head tilt and one brief shoulder bounce.
- CENTER reacts after RIGHT finishes, then gives the ladder line while leaning slightly forward with one hand.
- LEFT speaks last, calm and grimly practical; small open-palmed gesture, then the other two give a delayed `아...` facial reaction.
- avoid making the ending moralistic. End on the group's uncomfortable recognition.

## Final edit grammar

Generation master: 16:9.  
Distribution master: 9:16.

Recommended edit:
1. Clip 1 first 2–3 sec: crop/punch-in favoring CENTER + phone.
2. Widen or recenter on LEFT for her line.
3. Cut to Clip 2 on RIGHT's face/upper body for `진짜 신입이 뒤져감.`
4. Recenter toward CENTER, then LEFT for the final two beats.
5. No AI-generated zoom/pan is required; the apparent shot variation comes from editorial crop/punch-in.
6. Add Korean/English subtitle treatment in post for the publishable global version; do not bake subtitles into Seedance generation.
7. No explanatory outro. End immediately after the final social reaction if the beat lands.

## Why this is the new baseline

This tests the thing that matters now: whether a complete source-driven episode can be produced coherently with the locked recurring cast and set.

It simultaneously validates:
- a repeatable internet-post opening device;
- shot-specific first-frame stills without abandoning canonical visual authority;
- 2 x 8 sec complete-episode assembly;
- larger V2 reactions;
- editorial 9:16 shot grammar;
- source provenance and <=30% AI-written spoken beats.

It does **not** justify further isolated P001 Scene B pilot generation before a real episode is attempted.
