# Head Images

## Default 5-Image Structure

| Image | Role | Task | Typical Expression |
|---|---|---|---|
| 1 | Main/click image | Product recognition and strongest buying reason | Large product, large headline, key selling labels, spec/benefit strip |
| 2 | Selling point A | Prove quality/source/material/core technology | Proof module, source scene, process, checklist |
| 3 | Selling point B | Prove effect/performance/mechanism/comparison | Chart, comparison, mechanism diagram, before/after |
| 4 | Selling point C | Explain feature combination, details, usage value, capacity or long-term benefit | Ingredient/function bubbles, product detail, scene benefit |
| 5 | Audience/persona | Let users identify who should buy | 2-4 persona groups, real scenes, short pain/need labels |

## Planning Order

Before writing prompts:

1. Use `input-routing.md` to build the selling-point bank and decide which facts are supplied, inferred, or unsupported.
2. Use `visual-dna.md` to decide the head-image reference weight and which visual DNA elements should carry across the 5 images. Apply the **Reference Is Language, Not Scene** rule — inherit light/type/density/mood only, never inherit specific scene elements.
3. Use `visual-proof-grammar.md` to write a Picture Solo Statement for each of the 5 images.
4. Use `message-picture-patterns.md` to find a picture pattern for each image's message. Apply each pattern's product-presence rule.
5. Output the **5-Image Main-Visual Diversity Board** below. Reject the plan and regenerate if main-visual overlap exceeds the threshold.

The first head image may strongly follow a clear first-image reference. Images 2-5 must NOT simply repeat the first image with different copy; each must prove its own message with a different main visual.

## 5-Image Main-Visual Diversity Board (part of the unified approval gate)

This board is the head-image portion of the unified approval gate (see SKILL.md). It is output TOGETHER with the 10-screen detail-page board, never separately. The user reviews both as one batch before any prompt is written.

Output this table:

| Image | Message | Pattern (from library) | Picture Solo Statement | Main visual (one-line scene) | Scene setting | Main subject | Composition family | Product presence | Draft copy (consumer voice) |
|---|---|---|---|---|---|---|---|---|---|
| H01 | click/main | hero / closing-set | "The picture is ..., with text hidden it shows ..." | ... | ... | ... | ... | hero | 主文案（消费者视角）+ 可选副文案 |
| H02 | selling A | multi-variant / ingredients / etc. | "..." | ... | ... | ... | ... | none / partial | ... |
| H03 | selling B | soft-material / mechanism / etc. | "..." | ... | ... | ... | ... | none / partial | ... |
| H04 | selling C | operation / detail / etc. | "..." | ... | ... | ... | ... | partial / medium | ... |
| H05 | audience | audience-persona-grid / scene-fit | "..." | ... | ... | ... | ... | small / medium | ... |

**Diversity check**: scan the scene setting + main subject + composition family columns. At least 4 of the 5 images must have a unique combination. If two or more images share all three, the plan fails — pick a different pattern for the duplicate.

**Picture Solo check**: each image must have a written Picture Solo Statement that survives the "cover all copy" test.

**Consumer-voice copy check**: every draft copy must pass the "so what?" test. No manufacturer voice, no spec-sheet voice.

**Anti-template check**: no image's main visual may be "product packaging centered on the reference's scene surface" unless that image is H01 and the reference scene element budget allows it.

## Common Head-Image Anti-Patterns (must avoid)

- H02-H05 all being "product centered on the same background, just different headline text" — this is the #1 head-image failure mode and the primary symptom the user has reported.
- H02-H05 using icon rows to "express selling points" — no icons allowed, see `visual-proof-grammar.md`.
- H02-H05 ignoring the message-picture pattern library — pattern selection is mandatory before prompt writing.
- H05 being a generic "grid of 4 persona cards with role icons" — use a real-feel scene-based persona approach instead.
- All 5 images using the same reference scene element (picnic cloth, marble, grass, etc.) — Scene Cap allows at most 1 of 5.

## First Image: If Clear Reference Exists

Use the supplied first head-image reference as a layout mother-template. Match the information format closely while replacing content and rebuilding colors.

Prompt should explicitly say:

- Make the layout skeleton highly similar to the first head-image reference.
- Follow top strip, headline block, product block, selling labels, badges, bottom strip, promo area, frame/platform positions as applicable.
- Do not copy the reference's product, brand, copy, price, logos, certifications, category scene, or incompatible colors.

## First Image: If No Clear Reference Exists

Use this default strong e-commerce skeleton:

- 1:1 square.
- Top narrow strip for neutral product/category/store-like label; do not invent official store claims.
- Large headline on left or upper-left, 1-2 lines.
- Product hero large on right or center-right, 45-60% of canvas height.
- 2-3 stacked rounded selling-point capsules under headline.
- 1-2 small feature badges near product.
- Bottom spec strip with product name/spec/user-provided facts.
- Bottom large benefit slogan banner.
- Optional angled no-price promo block with a short selling label, not a made-up price.

This is a fallback. If the user provides a first head-image reference, the reference skeleton overrides this default.

Fallback does not mean generic. When the only reference is a poster/mood image, bend this default skeleton toward the poster's flavor contract:

- Keep the poster's camera attitude where possible, such as low-angle hand-held hero or close foreground product.
- Preserve the human-product relationship if it is central to the reference.
- Keep information density closer to the reference; if the poster is sparse and premium, reduce badges/modules.
- Keep the reference's spatial tension, such as large whitespace, extreme foreground product, or bold bottom wordmark behavior, while replacing brand text with product/category copy.
- Do not turn every poster reference into the same blue-card marketplace template.

For a poster reference with a person holding a product close to camera, the first head image should usually be a hybrid: marketplace-ready square image, but with a hand-held heroic product foreground and human emotion/background depth. Add only the minimum e-commerce labels needed for conversion.

Do not copy "hand-held close to camera" literally unless the target product is naturally used that way. Translate it through the product-use plausibility map:

- For an umbrella, use a natural handle/shaft grip, canopy over the shoulder or above the model, canopy edge as foreground scale, or a handle close-up with the opened canopy receding behind. Do not show an open umbrella being thrust horizontally at the viewer like a toothbrush, bottle, or hair dryer.
- For wearable products, the equivalent may be worn-on-body scale and confident posture rather than a hand pushing the object into camera.
- For large or heavy products, the equivalent may be a low-angle product hero beside the person, supported by the ground or furniture.

## Poster-Flavor Continuity Across 5 Head Images

When the strongest reference is a poster/mood image, do not preserve its flavor only in image 1. Before writing prompts, create a 5-image flavor transfer matrix:

- Image 1 should preserve 4-5 flavor dimensions from the contract, especially camera attitude, human-product relationship, whitespace, typography behavior, and commercial genre.
- Images 2-4 should each preserve at least 2-3 flavor dimensions while proving their own selling point. For example, keep sparse typography, white-space lifestyle, foreground product scale, or human warmth instead of defaulting to cards, charts, and icon rows.
- Image 5 should preserve the reference's emotional temperature and typography restraint even if it needs multiple people or scenes.
- If preserving a selling-point proof would force a generic infographic style, choose a more visual proof method first: product close-up, lifestyle scene, hand interaction, material/detail crop, or controlled comparison with minimal text.
- Add explicit anti-template negatives to every prompt when needed, such as "no dense marketplace modules, no blue card frame, no stacked capsules, no price/promo block".
- Add explicit product-use negatives to every prompt when the reference pose is risky, such as "do not hold the product in a physically awkward way" or a category-specific ban.

The set can vary by role, but it should still feel like one campaign world. A correct set should be recognizable as "the same product adapted from the same reference flavor", not five unrelated marketplace templates.

Use the visual distance matrix from `visual-proof-grammar.md` before prompting. Across the 5 images, vary proof form, camera distance, main subject, human role, density, and layout family while carrying shared visual DNA.

## Model Consistency Across Head Images

If any head image uses a model, define and reuse the same model-consistency lock across all head images where the main model appears. Keep face structure, age range, hair, skin tone, body type, expression range, and styling attitude consistent. Do not repeat the same pose by default; vary pose, gesture, crop, camera angle, expression intensity, and product interaction according to each head image's role.

For clothing/apparel/wearable fashion, do not choose the model source silently. If the user has not specified it, ask whether to use the reference-image model, product-image model, or a newly generated model before planning or generation.

Image 5 may show multiple audience groups only when the role requires persona identification. If it also includes the main campaign model, keep that person visually consistent and make other people clearly supporting personas, not accidental replacements.

## Image 2-4 Selling Point Rules

Each selling image must prove one claim. Choose the proof form by matching the message to a pattern in `message-picture-patterns.md`:

- Source/quality → "natural / simple ingredients" pattern, no packaging.
- Multi-variant / flavors / colors → "multi-flavor / multi-variant" pattern, no packaging, show contents arranged.
- Soft / skin-feel / material feel → "soft / skin-feel" pattern, no packaging, macro of contact.
- Micro-material / texture → "micro-material" pattern, no packaging, extreme macro.
- Mechanism / technology → "mechanism / structure" pattern, no full product, cutaway/exploded.
- Operation / how-to → "operation" pattern, medium product in use.
- Scene-fit / lifestyle → "scene-fit" pattern, small or no product, scene leads.
- Sensory result → "sensory result" pattern, no packaging, body/result detail leads.

Do not invent numeric data. If a chart is useful but no number is provided, use qualitative labels instead.

If the selling point naturally calls for a macro, mechanism, ingredient scene, comparison, or parameter proof, use that proof even when the reference image uses a different composition. The reference should shape light, type, rhythm, or mood only; it should NOT override the proof the message needs, and it should NOT impose its scene.

Each of H02, H03, H04 must use a different pattern. Three selling-point images all using "product centered with different headline" is a planning failure even if each has the right copy.

## Product Category Examples

For umbrellas or small outdoor accessories when only product appearance is provided:

- Good safe angles: pattern/design, portable daily carry, rainy-day commute, compact storage if the product is visibly foldable, grip/handle detail if visible, coverage/open canopy scene if shown or reasonable for an umbrella.
- Avoid unsupported specifics: sun-rain dual use, UV rating, sunscreen percentage, sunshade function, storm resistance, windproof ribs, waterproof coating, automatic open/close, weight, exact size, reinforced frame, certification, warranty.
- First image can use the default marketplace skeleton with brand/product-adapted blue/white/green palette when that fits the product, not the poster reference's brand color unless it fits.
- If poster reference shows person holding product, borrow "human scale, confidence, clean white background, low-angle product drama" as creative mood, not the literal hand pose. A plausible umbrella pose should usually show the hand gripping the handle/shaft naturally, with canopy above/behind/beside the person or the canopy edge close to camera.

## Image 5 Audience Rule

Use real, credible personas and needs. Avoid fear-based medicalized pain. For products like hair dryers, audience groups might be long-hair users, office commuters, family daily use, styling beginners, etc. Use 2-4 groups.

**Persona format**: prefer real-feel mini-scenes (one credible scene per persona, side-by-side or stacked) over abstract icon-persona cards. Each persona scene must show the audience in their actual context, not as a stick figure or role icon.

## Planning Table

Use columns:

| Image | Role | Message source | Core message | Proof form | Density | Visual distance note | Reference DNA carried | User takeaway | Main visual | Main copy | Labels | Color strategy | Why it proves the copy |

## Head-Image Prompt Must Include

- 1:1 square marketplace head image.
- One independent final head image only, ready to save as `<task-folder>/主图/0N-*.png`.
- **Picture Solo Statement** (the one-line "the picture is X, with text hidden it shows Y") at the top of the prompt.
- **Consumer-voice copy lock**: all copy in this image passes the "so what?" test — written from the consumer's perspective, no manufacturer/spec-sheet voice.
- Brand/product-adapted color palette.
- Whether first-image reference skeleton is used or default skeleton is used.
- Visual DNA notes: light behavior, typography attitude, density rhythm, commercial temperature. NOT scene/setting elements.
- **Scene element note**: if this image uses a reference-scene element, name it and confirm it's within the 1-of-5 budget; if not, state "no reference-scene elements used".
- Chosen message-picture pattern and pattern's product-presence rule.
- Chosen proof form and density level.
- Visual distance note: how this image's main visual differs from adjacent images in the set.
- Model source and model-consistency lock when people appear.
- Exact Chinese copy (consumer voice).
- **Explicit anti-icon line**: "no icons, no pictograms, no badge ribbons, no feature-icon rows, no ingredient bubbles".
- Text readability and no pseudo-Chinese.
- No copied price/logo/certification.

## Model-Native Text Production

Final head images must rely entirely on the image model for visuals, Chinese text, typography, and commercial layout. Do not create blank text areas for later local overlay. Do not add, correct, replace, or repair headlines, labels, strips, badges, or small finishing elements with deterministic local tools.

Because final text is model-native, write prompts as complete poster/layout directions: headline hierarchy, subtitle relationship, selling-label grouping, bottom strip logic, spacing, alignment, and readable commercial typography. Use as much Chinese copy as the image role naturally needs. If generated Chinese or typography is unsatisfactory, regenerate with clearer hierarchy, font attitude, spacing, and layout constraints instead of switching to local overlay.

## Head-Image Generation Protocol

For actual deliverables, run the head images as a numbered queue:

1. Generate `H01` as one square first/click image.
2. Save it to `<task-folder>/主图/01-*.png`.
3. Check product accuracy, square ratio, copy readability, and click-image role.
4. Regenerate `H01` until it passes or record the blocker.
5. Repeat the same one-image loop for `H02` through `H05`.
6. After all five independent files pass, create a contact sheet for review.
