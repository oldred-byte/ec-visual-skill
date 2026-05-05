# Detail Pages

## Default 10-Screen Structure

| Screen | Role | Typical Expression |
|---|---|---|
| 1 | Hero | Product/scene memory, core promise |
| 2 | Pain point or scene | Real usage problem or user state |
| 3 | Selling point A | Technical/ingredient/material/source explanation |
| 4 | Selling point B | Comparison, proof, data, effect validation |
| 5 | Selling point C | Experience visualization or sensory benefit |
| 6 | Usage scene | Key scene or multi-scene substitution |
| 7 | Practical benefit | Capacity, battery, portability, durability, operation, storage, etc. |
| 8 | Detail/craft/parameter | Macro detail, material, specification, structure |
| 9 | Trust | Testing, service, quality basis, safe-use promise without fake certification |
| 10 | Closing conversion | Product set, brand memory, final buying reason |

## Detail-Page Rules

- 3:4 vertical by default.
- Aspect ratio must be exactly 3:4 vertical, not 9:16, not phone-story, not poster-story. Prompts must say: "strict 3:4 vertical canvas, approximately 1200x1600, not 9:16".
- Generate and save each detail screen as an independent final image in `输出/详情页/0N-*.png`.
- Each screen must express one clear idea.
- Each screen must explain why the visual proves the copy.
- Use product-adapted color system, not copied reference colors.
- Do not repeat the same card/label/layout on every screen.
- Use real usage logic: if a benefit is felt in use, show use; if a benefit is technical, show mechanism; if a benefit is trust, show proof without fake certifications.
- When user facts are missing, use visible or category-generic benefits only. Do not turn a generic detail page into unsupported technical claims.
- For final image generation, use normal commercial detail-page typography. Include the amount of Chinese copy the screen naturally needs, with clear hierarchy, readable type sizes, organized modules, and poster/detail-page spacing.

## Model Consistency Across Detail Pages

If any detail page uses a model, define and reuse the same model-consistency lock across all detail pages where the main model appears. Keep face structure, age range, hair, skin tone, body type, expression range, and styling attitude consistent across hero, scene, usage, comparison, and closing screens. Do not repeat the same pose by default; choose different poses, gestures, crops, camera angles, expression intensity, and product interactions to match each screen's content.

For clothing/apparel/wearable fashion, do not choose the model source silently. If the user has not specified it, ask whether to use the reference-image model, product-image model, or a newly generated model before planning or generation.

Screens may include different users only when the narrative requires separate personas or crowd scenes. Mark them as supporting extras or audience personas so they do not replace the locked main model.

## Umbrella / Small Accessory Example

If the product is an umbrella and no technical specs are supplied, a safe 10-screen plan can emphasize:

- Hero: design identity and daily outing.
- Scene: rainy commute or light travel.
- Visual design: canopy pattern/color.
- Carry: compact storage if visibly foldable.
- Holding/use: hand-held comfort if handle is visible.
- Matching: outfit/bag/lifestyle scene.
- Detail: canopy edge, handle, strap, case if visible.
- Practicality: easy to keep in bag, phrased softly.
- Trust: clear product appearance and daily-use reassurance, not certification.
- Closing: product set and daily companion feeling.

Avoid unsupported claims such as UV rating, windproof level, water-repellent coating, exact size/weight, automatic open/close, or reinforced ribs unless provided.

## Planning Table

Use columns:

| Screen | Role | Expression | User feeling | Main visual | Main copy | Supporting copy | Color strategy | Auxiliary elements | Why it proves the copy |

## Detail Prompt Must Include

- Strict 3:4 vertical detail-page screen, approximately 1200x1600; not 9:16, not phone-story, not long poster.
- One independent detail-page screen only, ready to save as a numbered final file.
- Reference-role rules.
- Product-adapted color palette.
- Scene/use logic check.
- Model source and model-consistency lock when people appear.
- Exact Chinese copy.
- Complete model-native Chinese typography: title, subtitle, labels, annotations, or module copy as needed for the screen, all arranged in a clear commercial hierarchy.
- Auxiliary elements only when useful.
- No copied brand/price/logo/certification.

## Regeneration Rule

After generating, check dimensions first. If any detail page is not 3:4 vertical, regenerate it before judging style. If text or typography is unsatisfactory, regenerate with clearer hierarchy, spacing, font direction, and module layout.

If the model returns the wrong delivery shape, immediately re-prompt that same
screen as one strict 3:4 independent final image before moving to the next
screen.

## Model-Native Text Production

Final detail pages must rely entirely on the image model for visuals, Chinese text, typography, and commercial layout. Do not reserve blank text areas for later local overlay. Do not add, correct, replace, or repair titles, subtitles, labels, cards, annotations, or paragraphs with deterministic local layout tools.

Because final text is model-native, write prompts as complete detail-page layout directions: title hierarchy, subtitle rhythm, selling modules, annotations, proof blocks, spacing, alignment, and readable commercial typography. Use as much Chinese copy as the screen naturally needs. If generated Chinese or typography is unsatisfactory, regenerate with clearer hierarchy, font attitude, spacing, and module layout constraints instead of switching to local overlay.

## Detail-Page Generation Protocol

For actual deliverables, run the detail pages as a numbered queue:

1. Generate `D01` as one strict 3:4 hero screen.
2. Save it to `输出/详情页/01-*.png`.
3. Check 3:4 ratio, product accuracy, screen role, narrative fit, copy readability, and claim safety.
4. Regenerate `D01` until it passes or record the blocker.
5. Repeat the same one-screen loop for `D02` through `D10`.
6. After all ten independent files pass, create a contact sheet for review.
