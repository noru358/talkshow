# CHARACTER ASSET SPEC

Updated: 2026-09-02 KST

## Visual style lock
- Style: previously selected **A style** only.
- Human-looking, rough hand-drawn community-webtoon feel.
- Flat colors, minimal detail, imperfect linework.
- Avoid polished anime look, glossy AI illustration, cinematic lighting, 3D, photorealism.
- Preserve visible hand-drawn irregularity.

## Confirmed character pool
B, C, E, F, G, K, L, M, Q, R

These are a **cast pool**, not fixed personality-role archetypes.
Only visual identity and a few core traits remain stable. Episode roles rotate freely.

## Pilot 001 temporary trio
- C
- E
- K

Reason: strongest silhouette/clothing/energy contrast for first production test.
This is not a permanent hierarchy.

## Asset layers per character
Each character must eventually have transparent PNG assets with consistent proportions and camera framing.

### 1. Base body poses
- P00 neutral standing
- P01 neutral seated at table
- P02 arms crossed
- P03 one hand pointing
- P04 one hand open / explaining
- P05 both hands reacting
- P06 leaning forward
- P07 leaning back
- P08 facepalm / hand on face
- P09 phone-looking / distracted

### 2. Face expressions
- F00 neutral
- F01 deadpan
- F02 slight smile
- F03 laugh-small
- F04 laugh-big
- F05 shocked
- F06 annoyed
- F07 disgusted / '그건 좀'
- F08 confused
- F09 smug
- F10 angry
- F11 embarrassed
- F12 trying-not-to-laugh
- F13 blank stare

### 3. Mouth shapes for low-frame lip sync
- M00 closed
- M01 small open
- M02 medium open
- M03 wide open
- M04 horizontal / 'ee'
- M05 round / 'o'
- M06 teeth / clenched

For Pilot 001, exact phoneme lip sync is optional. Start with amplitude-driven 3-state mouth switching if it looks better and faster.

### 4. Eyes
- E00 open
- E01 half-lidded
- E02 closed
- E03 wide
- E04 side-eye-left
- E05 side-eye-right

### 5. Reaction specials
- R00 tiny head turn
- R01 big laugh deform
- R02 freeze
- R03 sudden zoom face
- R04 disgust recoil
- R05 silent stare
- R06 off-screen look

## Pilot-first minimal pack
Do NOT make the full library before validating Pilot 001.
For C/E/K only, first produce:
- seated neutral
- seated explaining
- seated deadpan
- seated big laugh
- seated shocked
- seated annoyed
- standing neutral
- 3 mouth states: closed / mid / wide
- eyes: open / half / closed

That is enough for the first 20–35 second prototype.

## Naming convention
`CHAR_<ID>_<POSE>_<FACE>_<MOUTH>_<EYES>.png`

Examples:
- `CHAR_C_P01_F00_M00_E00.png`
- `CHAR_E_P01_F01_M01_E01.png`
- `CHAR_K_P03_F04_M03_E02.png`

## Quality constraints
- Same character identity across all poses.
- Same clothing for the episode unless intentionally changed.
- Same head/body proportion.
- No beautification drift.
- No anime-style eye enlargement drift.
- No detailed shading drift.
- No smoothing that removes rough line texture.
- Transparent background for character layers.

## Production principle
If a new expression is needed during editing, generate only that missing state. Do not regenerate the entire character set.
