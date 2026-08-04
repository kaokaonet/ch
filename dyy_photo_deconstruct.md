---
name: dyy_photo_deconstruct
description: Turn a user's photo into a vertical, textless "ink-wash silhouette deconstruction" zine poster on aged paper. Each subject is reduced to its essential silhouette or a single gesture line, with only the minimum necessary interior marks (a few color blocks, dots, or thin strokes) to keep the scene readable. Huge negative space, no text, muted palette with one or two small accents. Use when the user supplies a real photo and wants a quiet Japanese/Korean indie-zine reinterpretation that feels painterly and abstract but still carries the original scene.
---

# Photo Deconstruction Zine Poster

Take a user's real photo and reinterpret it as a **textless ink/watercolor deconstruction** on a vertical aged-paper poster.

The guiding idea is **not** rigid geometry. It is:

> **剪影 + 最少必要记号** — each element becomes its essential silhouette or a single gesture line; interior detail is added only when it is needed to identify the element.

Think of the example look: a ship as a dark silhouette with a few mast lines; a bridge as one thin arc; a castle as a dark spired silhouette with small colored windows; water as a few horizontal strokes; trees as a green wash blob. The scene is still readable, but every mark earns its place.

---

## When to Use

- User gives a photo and asks for a minimal / zine / deconstructed / "poetic" reinterpretation.
- User references example looks where subjects are recognizable but abstracted to silhouettes and sparse marks.
- User explicitly wants **no text**.

Do **not** use when the user wants:
- A faithful / photographic render.
- Text, labels, dates, or titles on the poster.
- A full-bleed illustration, commercial poster, 3D / neon / cartoon look.

---

## Core Principle: Silhouette + Minimum Necessary Marks

For each key element in the photo, choose one of these treatments:

| Treatment | Use for |
|---|---|
| **Silhouette** (dark or colored wash shape) | the main subject: building, ship, castle, duck, butterfly wings, tree trunk, rock |
| **Single gesture line** | bridge arc, horizon, mast, fishing rod, branch, railing, spire outline |
| **Small wash blob / smear** | foliage mass, water surface, cloud, field, leaf pile |
| **Tiny dot** | moon, sun, lantern, person, bird, eye, beak, small light |
| **Tiny rectangle / block** | window, door, plaque, fountain base, boat hull (only when identity-critical) |

**Rules:**

1. **Keep the scene readable.** Every key element of the photo must appear in the deconstruction in roughly its original position.
2. **Reduce to silhouette first.** Ask: "What is the simplest outline that still reads as this object?" Use that.
3. **Add interior marks only when necessary.** Windows on a castle, masts on a ship, antennae on a pagoda, beaks on ducks — these are identity-critical. Bricks, roof tiles, fur, feathers, glass reflections are not.
4. **When something looks too literal / specific, soften it.** Replace hard edges with wash bleed; replace texture with flat silhouette.

---

## Deconstruction Mapping Dictionary

### Architecture & structures
- **High-rise / tower / castle / house**: a single **silhouette shape** in the subject's dominant color. Add tiny rectangular/dark dots for windows only if the building is the clear focal point (e.g., castle). Otherwise keep it plain.
- **Pagoda / tiered roofs**: layered **curved dark lines**; optional tiny warm dots for lights/lanterns.
- **Bridge**: usually a single **arc line** or a few straight lines; pylons/towers as small rectangles.
- **Pier / walkway / railing**: horizontal line + a few vertical lines for posts.
- **Plaque / sign**: tiny blank rectangle (no text).
- **Fountain / statue**: light-colored vertical silhouette or block in front of the building.

### Nature
- **Tree / forest / hedgerow**: one or two **green wash blobs** with soft edges. Do not draw individual leaves or branches.
- **Branch reaching over water / bare tree**: a few bold **curved dark lines** for main limbs only.
- **Water (lake / sea / river)**: a few **horizontal wash strokes** or a single horizontal wash band. No ripples, no reflections.
- **Moon / sun / round light**: a single pale **circle or dot**.
- **Fallen leaves / flower petals / scattered spots**: small colored wash dots or smears.
- **Grass / reeds**: a few vertical green wash strokes.

### Animals & people
- **Duck / bird / fish**: a small **silhouette wash** in the body color, plus a tiny dot for beak/eye if needed.
- **Butterfly / symmetric subjects**: symmetric wing shapes (can be soft washes, not rigid ellipses) around a thin body line.
- **Person / crowd**: tiny dots or small elongated dashes, placed where people are.

### Special / conceptual subjects
- **Ship**: dark ship silhouette + thin vertical lines for masts/antennae; water as scattered horizontal strokes.
- **Hot air balloon**: can be abstracted as a colored ring/wash framing a smaller center shape (the sky becomes part of the balloon mark).
- **Fireworks / radiating lights**: thin radiating dotted lines from a central point.
- **Balloons / lanterns in a row**: vertical colored dots or small ovals.

### Accents
- Keep one or two small high-saturation accents if the photo has a natural focal pop (pink boat, red leaves, orange balloon). Mute everything else.

---

## Canvas & Composition Rules

- **Format:** tall vertical **3:5** poster. Generate at `1024x1536`. Full-frame aged paper, no border, no mockup.
- **Negative space:** **85%–92%** empty warm cream paper. The cluster occupies roughly **8%–15%** of the canvas.
- **Placement:** lower-middle or center. Never full-bleed, never edge-hugging.
- **Paper:** warm cream / off-white aged paper; flat scanned-paper grain; matte; no hard shadow; no 3D depth.
- **Color:** muted palette from the photo. Paper + grey/black + subject color. One or two small accents allowed.
- **Texture:** ink wash, watercolor bleed, xerox softness, risograph grain, scan noise.

---

## Prompt Compiler (write the final prompt as 4 compact paragraphs)

1. **Canvas + paper + negative space + cluster size/location**
   > A tall vertical 3:5 minimal zine poster on warm cream aged paper. 85–92% empty paper, vast negative space. A small visual cluster occupying about X% of the canvas, placed in the [location].

2. **Subject → silhouette / gesture / minimum marks**
   > An ink-wash silhouette deconstruction of [scene]. Reduce each element to its essential silhouette or single gesture line: [element A] → [treatment], [element B] → [treatment], [element C] → [treatment]... Add only the minimum necessary interior marks (tiny window blocks, mast lines, beak dots) to keep the scene readable.

3. **Palette + texture + text rule**
   > Muted palette: [paper], [subject colors]. Soft watercolor bleed, dry-brush, lots of unpainted cream paper. No text, no caption, no numbers, no dates, no signature, no watermark.

4. **Mood + avoid-list**
   > Scanned paper grain, matte, flat, no shadow, no 3D, no border. Quiet, poetic, distant, nostalgic, Japanese/Korean indie zine mood. Avoid: detailed rendering, illustration, photo-realism, full scene, cartoon, 3D, neon, commercial, long text, rigid geometric blocks.

Be decisive: name each element and its treatment. Prefer "silhouette" and "gesture line" over "rectangle" and "ellipse".

---

## Workflow

1. **Receive the photo.** List 3–6 key elements and their spatial relationships.
2. **Choose the essential treatment for each element** using the Dictionary. Default to silhouette; use a gesture line only when the element is essentially a line (bridge, horizon, mast); add tiny interior marks only if identity-critical.
3. **Write the 4-paragraph prompt** using the Compiler.
4. **Generate the image.** Use image-to-image:
   - `image` = user's photo path.
   - `input_fidelity` = **`low`**.
   - `size` = **`1024x1536`**.
   - `quality` = `high`.
   - `prompt` = your 4-paragraph prompt.
5. **Inspect thumbnail.** Check:
   - Is it 85–92% empty paper?
   - Are all key elements present as silhouettes / gestures / minimum marks?
   - Does anything look like a rigid geometric block instead of a soft silhouette/wash? If yes, soften the wording.
   - Does anything look too detailed / literal? Degrade it to silhouette or remove texture.
   - Is there any text? If yes, regenerate with stronger "no text anywhere".
6. **Return the image and the final prompt.**

---

## Negative Constraints (always include)

Avoid:
- text, captions, numbers, dates, signatures, watermarks, titles
- full-bleed scene, detailed illustration, photo-realism, filtered photo
- rigid geometric blocks, perfect rectangles, perfect circles (unless the subject itself is strongly geometric)
- brick texture, roof tiles, individual leaves, branch twigs, water ripples, glass reflections, fur, feathers
- cute cartoon, kawaii, anime, fashion editorial drama
- 3D rendering, cinematic lighting, hard shadows, depth of field, neon, cyberpunk
- commercial poster, logo, CTA, brand campaign
- clean digital UI white, glossy paper mockup, heavy paper shadow
- too many objects, too many colors, dense scrapbook

---

## Output Format

```markdown
**生成图**

![photo deconstruction zine poster](absolute-image-path)

**最终 Prompt**

```text
[the 4-paragraph prompt actually used]
```

**说明**

- Mode: Photo Deconstruction (textless)
- Recipe: [element → treatment, ...]
- [one short note on any element that was softened to silhouette]
```

---

## Quality Gate

Before finalizing, confirm:
- Vertical 3:5 aged-paper poster, no border/mockup?
- 85–92% reads as empty cream paper?
- Cluster ~8–15% of canvas, not edge-hugging?
- Every key element of the photo is present as a silhouette / gesture / minimum mark?
- No rigid geometric blocks unless the subject is inherently geometric?
- Interior marks are minimal and identity-critical only?
- NO text / number / date / signature / watermark anywhere?
- Muted palette from the photo, at most one or two small accents?
- Flat scanned-paper texture, no 3D / shadow / neon / cartoon?
- The image was actually generated (not prompt-only)?

---

## Example Requests

- "用这张照片做一张解构 zine 海报"
- "把这张旅行照变成无文字的极简解构插画"
- "用 $dyy_photo_deconstruct 生成一张船的海报"
- "这张建筑照片，做成剪影解构的旧纸风 poster"

## Notes

- This skill outputs the **deconstruction layer only** on paper. If the user later wants a dual-panel layout (real photo on top + deconstruction below), that is a separate composition step.
- The default is strictly textless. Only add text if the user explicitly overrides this preference.
