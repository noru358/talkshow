# TALKSHOW — MASTER STYLE PROMPT

**Status:** AUTHORITATIVE copy-paste visual style lock
**Updated:** 2026-09-04 KST

Use this file when generating or remastering characters/backgrounds so every scene stays in the same visual world.

The reference images remain the strict identity/style authority. This prompt describes the drawing grammar; it must not override a character's unique face, eye shape, hairstyle, outfit, or other identity features.

---

# 1. MASTER CHARACTER ART STYLE LOCK — COPY/PASTE

```text
MASTER CHARACTER ART STYLE LOCK

Create a full-body or scene-integrated 2D character illustration in a simple Korean web-comic character-sheet style.

STYLE:
Cute but adult semi-chibi proportions, approximately 3.7–4.1 heads tall.
Large rounded head, short rounded jaw, wide cheeks, narrow shoulders, small simple torso, slender simplified arms and legs, slightly oversized rounded shoes.

FACE CONSTRUCTION:
Very simple round youthful face.
Large rounded-oval white eyes.
Simple solid black circular pupils with one tiny white catchlight.
No detailed iris rendering.
Thin curved upper eyelids.
Minimal eyelashes, only one or two short strokes if needed.
Thin simple curved eyebrows.
Tiny dot-like or very short-line nose.
No realistic nose bridge or nostril detail.
Small simple curved mouth when neutral.
When speaking or laughing, use a simple rounded open mouth with a black interior and minimal red tongue.
Optional subtle blush made from two or three short pale-pink strokes on each cheek.
Simple C-shaped ears with almost no anatomical detail.

CRITICAL IDENTITY RULE:
Do NOT homogenize every character's eyes or face.
Preserve each reference character's exact eye shape, eyelid openness, face proportions, bangs, hairline, and expression language.
If a male reference has narrower or half-lidded eyes, keep them narrower or half-lidded rather than enlarging them into generic round anime eyes.
Reference identity overrides generic style description.

LINE ART:
Clean black hand-drawn ink outlines.
Slight natural irregularity, but no messy sketch lines.
Outer silhouette lines should be approximately 1.5–2 times heavier than interior detail lines.
Use thick clear contours around the hair, head, body and clothing.
Use thinner lines for facial features, folds, pockets and small details.
Avoid perfectly sterile vector-style lines.

HAIR:
Treat the hair as several large graphic masses rather than many individual strands.
Strong readable overall silhouette.
Only a few large locks or waves.
Very limited strand detail.
Minimal highlights consisting only of a few short soft strokes.
No glossy anime hair and no realistic individual hairs.
Male short hair should be neat, soft and tidy unless the reference explicitly says otherwise; avoid exaggerated spiky manga tufts.

BODY:
Highly simplified anatomy.
No visible musculature or skeletal anatomy.
Short thin neck.
Narrow shoulders.
Simple cylindrical limbs.
Hands and fingers should be simplified and rounded.
Feet and shoes slightly oversized for a cute stable silhouette.

CLOTHING:
Contemporary casual clothing suitable for a Korean person in their 20s or 30s.
Realistic clothing design but simplified drawing.
Prioritize overall clothing silhouette over detailed construction.
Only a few essential folds around joints and compression points.
Minimal seams and stitching.
Do not render complicated fabric physics.

COLOR AND RENDERING:
Mostly flat digital colors.
Muted, soft, slightly desaturated palette.
Very little shading.
No dramatic directional lighting.
No glossy highlights.
No strong gradients.
Subtle paper, colored-pencil, or watercolor-like grain may appear inside large color areas, especially denim or fabric.
Approximately 90% clean flat digital coloring and 10% subtle hand-made texture.

AESTHETIC:
Friendly, casual, slightly imperfect handmade Korean web-comic illustration.
Simple and charming rather than polished or glamorous.
Looks like a reusable character design sheet brought into a scene rather than a finished anime poster.

BACKGROUND:
If generating a standalone character, use a plain white or transparent background unless a scene is specified.
No unnecessary cast shadow unless specifically requested.

IMPORTANT:
Preserve this exact face-construction grammar, line-weight hierarchy, body proportion, simplification level, hair rendering method, and flat muted coloring across every new character.

Do not copy the hairstyle, clothing, accessories, pose, or identity of another reference character.
Copy only the drawing grammar and visual style, while preserving the target character's own identity.
```

---

# 2. NEGATIVE STYLE LOCK — COPY/PASTE

```text
NEGATIVE STYLE LOCK

Do not use photorealism.
Do not use semi-realistic anatomy.
Do not use polished Japanese anime rendering.
Do not use detailed manga eyes.
Do not replace a reference character's unique eye shape with generic large round eyes.
Do not use complex iris gradients.
Do not use sharp V-shaped jawlines.
Do not use realistic noses or lips.
Do not use individual realistic hair strands.
Do not use spiky manga hair unless explicitly present in the character reference.
Do not use glossy hair.
Do not use cinematic lighting.
Do not use strong cel shading.
Do not use 3D rendering.
Do not use Pixar-like rendering.
Do not use painterly digital illustration.
Do not use highly detailed fabric folds.
Do not use fashion-illustration proportions.
Do not use eight-head realistic human proportions.
Do not use tiny heads or broad realistic shoulders.
Do not use hyper-clean sterile vector graphics.
Do not over-render or beautify the character.
Do not redesign facial identity when integrating the character into a background.
```

---

# 3. MASTER BACKGROUND STYLE LOCK — COPY/PASTE

```text
MASTER BACKGROUND STYLE LOCK

Render the environment in the same visual world as the character references.

Use clean black hand-drawn outlines with slight natural irregularity.
Use clearly readable large shapes and simplified geometry.
Use thicker outer contours and thinner internal detail lines.
Use flat muted colors with very minimal shading.
Use subtle paper / colored-pencil texture inside broad color areas.

Keep props and architecture recognizable but simplified.
Prioritize silhouette and spatial readability over realistic detail.
Avoid excessive small objects, texture noise, photorealistic materials, complex reflections, dramatic shadows, cinematic lighting, or dense decoration.

For night scenes, keep the sky, buildings, windows, lamps, water, and skyline graphic and simplified rather than realistically rendered.
Lit windows may be simple warm rectangles.
City buildings should read as blocky graphic masses rather than detailed architecture.
Water reflections should be sparse simple strokes or shapes, not realistic ray-traced reflections.

The background should support the characters, not visually overpower them.
The final scene must look as if the characters and environment were drawn by the same artist using the same pen, simplification level, palette, and texture.
```

---

# 4. REFERENCE HIERARCHY — LOCKED

Use references in this priority order:

1. **Character identity reference** — controls face, eye shape, hairstyle, outfit and identity.
2. **Master style reference** — controls linework, proportions, simplification, coloring and texture.
3. **Background/layout reference** — controls location, furniture, object placement and camera composition.
4. **Text prompt** — fills gaps only; it must not override the references above.

Critical rule:

> STYLE CONSISTENCY does not mean FACE HOMOGENIZATION.

Characters should look like different people drawn by the same artist, not the same face wearing different hair.

---

# 5. CURRENT THREE-CHARACTER IDENTITY NOTES

These are identity constraints, not universal style rules.

## Female 1 / long-haired woman
- long wavy dark hair with bangs
- very large round eyes
- cream ribbed cardigan over light inner top
- dark wide pants
- no shoulder bag in current scene masters

## Female 2 / brown-bob woman
- straight shoulder-length brown bob
- large simple round eyes
- white fitted short-sleeve T-shirt
- light-blue jeans

## Male / blue-striped-shirt man
- short black hair
- hair must be neat, soft, tidy and non-spiky
- preserve the original reference eye design: narrower, relaxed / slightly half-lidded eyes
- do NOT enlarge his eyes into the round female-style eye shape
- light-blue vertically striped button-up shirt
- dark trousers
- black low-top sneakers in shoe-on scenes

---

# 6. GENERIC CHARACTER INSERT TEMPLATE

Append only the target character-specific description after the master block.

```text
CHARACTER ONLY:

[age / gender / Korean appearance]
[exact hairstyle]
[exact eye-shape identity note]
[exact outfit]
[shoe/sock state]
[neutral ordinary pose]
[expression]

Keep every other visual property exactly according to MASTER CHARACTER ART STYLE LOCK.
Preserve the target reference identity exactly; do not redesign the face.
```

---

# 7. QC CHECK BEFORE LOCK

Before accepting a generated still, verify:

- face identity matches the character reference, especially eye shape and bangs
- male eyes have not drifted into generic large round eyes
- male hair has not become spiky again
- outer lines are heavier than inner detail lines
- character proportions remain semi-chibi, not realistic
- clothing is simplified rather than over-rendered
- background rendering density does not exceed character rendering density
- characters and furniture are physically separated correctly
- no hands trapped in tabletops
- no legs intersecting table supports
- no body parts passing through furniture
- all characters appear to belong to the same drawing system

When identity and generic style instructions conflict, preserve the reference identity first.
