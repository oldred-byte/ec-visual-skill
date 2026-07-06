# Detail Pages

## Fixed Structure, Flexible Expression

The default 10-screen structure is a scaffold, not a visual template. If the user provides an existing 10-screen plan or screen directions, preserve that structure as the hard standard. Do not redesign the sequence unless the user explicitly asks for restructuring.

For every screen, translate the fixed direction into a mature expression:

1. What should the buyer feel, believe, or stop worrying about?
2. What exact visual evidence proves that expression?
3. Who or what should be the main subject?
4. How much of the product should appear?
5. What copy naturally grows from the visual evidence?

This prevents generic repetition such as product hero + big title + icon row on every screen. Product recognition matters, but the full product is not always the right subject. Some screens should be led by a body part, hand action, product component, mechanism, result state, or scene relationship when that better proves the assigned direction.

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

## Detail Pages Are Not Vertical Head Images (hard rule)

The most common detail-page failure mode is: each screen looks like a vertical version of the head image — same product centered, same scene background, just with longer copy. This is the primary symptom the user has reported and the skill is now designed to prevent it.

Detail pages have their own narrative logic. They progress through hero → scene/problem → proof → detail → trust → closing. Each screen's main visual must be designed for that screen's message, NOT inherited from the head image's main visual.

Hard rules:

- D01 hero may share visual language with H01 (campaign memory) but should NOT be a pixel-stretched version of H01.
- D02-D10 each have their own main visual, chosen by message, not by template.
- The packaging/packaging-on-same-background combination may appear in at most 3 of 10 screens (Scene Cap).
- The 10 screens must use ≥7 distinct main visuals.

## Planning Order

Detail pages are content-led. Before writing prompts:

1. Use `input-routing.md` to decide whether screen messages come from complete user facts, partial user facts, or conservative category/visible inference.
2. Capture user-provided screen directions. If they exist, keep them and improve each screen's expression rather than replacing the structure.
3. Use `input-routing.md` to build a consumer-angle map for category anxieties, buyer desires, safe wording boundaries, and evidence moments.
4. Use `visual-proof-grammar.md` to write a Picture Solo Statement for each of the 10 screens.
5. Use `message-picture-patterns.md` to find a picture pattern for each screen's message. Apply each pattern's product-presence rule — many screens will have NO packaging.
6. Use `visual-dna.md` to decide which 2-4 reference DNA elements each screen carries (light, type, density, mood only — NOT scene/setting). Apply Scene Cap (≤3 of 10 may use any one reference-scene element).
7. Use `color-adaptation.md` to apply supplied brand colors or product-first colors consistently.
8. Output the **10-Screen Main-Visual Diversity Board** below. Reject the plan and regenerate if main-visual overlap exceeds the threshold.

Do not start from the reference composition and force every screen into it. A flavors screen may be three ingredient bowls with no packaging; a texture screen may be a macro of the material; a usage-scene screen may need a real person in context. The picture should make the message obvious before the copy explains it.

## 10-Screen Main-Visual Diversity Board (part of the unified approval gate)

This board is the detail-page portion of the unified approval gate (see SKILL.md). It is output TOGETHER with the 5-image head-image board, never separately. The user reviews both as one batch before any prompt is written.

Output this table:

| Screen | Role | Fixed direction | Message | Pattern (library) | Picture Solo Statement | Main visual (one-line scene) | Scene setting | Main subject | Composition | Product presence | Draft copy (consumer voice) | Claim boundary |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| D01 | hero | ... | ... | closing-set / hero | "The picture is ..., with text hidden it shows ..." | ... | ... | ... | ... | hero | 主文案 + 可选副文案 | ... |
| D02 | pain/scene | ... | ... | scene-fit / sensory-result | "..." | ... | ... | ... | ... | small / none | ... | ... |
| D03 | selling A | ... | ... | multi-variant / natural-ingredients / etc. | "..." | ... | ... | ... | ... | none / partial | ... | ... |
| D04 | selling B | ... | ... | mechanism / soft-material / etc. | "..." | ... | ... | ... | ... | none / partial | ... | ... |
| D05 | selling C | ... | ... | sensory-result / operation / etc. | "..." | ... | ... | ... | ... | none / partial | ... | ... |
| D06 | usage scene | ... | ... | scene-fit | "..." | ... | ... | ... | ... | small / medium | ... | ... |
| D07 | practical | ... | ... | parameter / operation | "..." | ... | ... | ... | ... | partial | ... | ... |
| D08 | detail/craft | ... | ... | micro-material / parameter | "..." | ... | ... | ... | ... | partial | ... | ... |
| D09 | trust | ... | ... | trust / quality-basis | "..." | ... | ... | ... | ... | medium / partial | ... | ... |
| D10 | closing | ... | ... | closing-set | "..." | ... | ... | ... | ... | hero / set | ... | ... |

**Diversity check**: scan the scene setting + main subject + composition columns. At least 7 of the 10 screens must have a unique combination. If 4 or more screens share all three, the plan fails — pick different patterns.

**Scene Cap check**: no single reference-scene element (e.g., picnic cloth, marble, grass) may appear in more than 3 screens.

**Product-presence check**: at least 4 of the 10 screens should have "no packaging" or "partial only" as their product presence. If all 10 screens show the full packaging, the plan has failed — re-plan selling-point and sensory screens to remove packaging.

**Picture Solo check**: each screen must have a written Picture Solo Statement that survives the "cover all copy" test.

**Consumer-voice copy check**: every draft copy must pass the "so what?" test. No manufacturer voice, no spec-sheet voice.

Only after the unified approval (head images + detail pages together) passes may prompts be written.

## Detail-Page Rules

- 3:4 vertical by default.
- Aspect ratio must be exactly 3:4 vertical, not 9:16, not phone-story, not poster-story. Prompts must say: "strict 3:4 vertical canvas, approximately 1200x1600, not 9:16".
- Generate and save each detail screen as an independent final image in `<task-folder>/详情页/0N-*.png`.
- Each screen must express one clear idea.
- Each screen must explain why the visual proves the copy.
- Each screen must have a written Picture Solo Statement before prompting.
- Each screen must name its main subject and product exposure level before prompting.
- Use brand/product-adapted color system, not copied reference colors.
- Do not repeat the same card/label/layout on every screen.
- **No icons, no pictograms, no badge ribbons, no feature-icon rows, no ingredient bubbles, no decorative arc systems.** See `visual-proof-grammar.md` No-Icon Rule. The user will add icons later in their own pipeline if needed.
- Use real usage logic: if a benefit is felt in use, show use; if a benefit is technical, show mechanism; if a benefit is trust, show proof without fake certifications; if a benefit is ingredient/sensory, show the ingredient/sensory moment without packaging.
- When user facts are missing, use visible or category-generic benefits only. Do not turn a generic detail page into unsupported technical claims.
- For final image generation, use normal commercial detail-page typography. Include the amount of Chinese copy the screen naturally needs, with clear hierarchy, readable type sizes, organized modules, and poster/detail-page spacing.
- The product/packaging does NOT appear by default. Each screen decides packaging presence based on its message and the pattern's rule.

## Planning Approval Gate (part of the unified approval gate)

Detail-page approval is part of the **unified approval gate** in SKILL.md — head images and detail pages are planned and reviewed together as one batch. Do not output detail-page approval separately from head-image approval.

Before any prompt is written or any image is generated (for either head images or detail pages), output the unified approval which includes:

1. **5-Image Main-Visual Diversity Board** (see `references/head-images.md`) with draft consumer-voice copy.
2. **10-Screen Main-Visual Diversity Board** (above) with draft consumer-voice copy and claim boundary.
3. Brief set-level summary: visual DNA contract, color system, scene cap status, product-presence mix status.

User reviews both boards in one pass, asks for adjustments, or approves. Only after explicit approval (or user saying "skip review") may prompts be written and generation begin.

If a generated image drifts back into a generic full-product template, classify it as a prompt failure and regenerate that screen with stronger main-subject and exposure constraints.

## Reference Weight By Screen

Reference weight varies by screen:

- D01 hero: use stronger reference DNA for campaign memory, lighting, typography, and product mood.
- D02 pain/scene and D06 usage scene: use reference mood and typography, but real use logic decides the scene and pose.
- D03-D05 selling points: proof grammar decides the layout first; reference DNA shapes color relationship, typography, light, and module rhythm.
- D07 practical benefit and D08 detail/parameter: clarity and proof come first; keep set consistency through color, type, lines, and small recurring devices.
- D09 trust and D10 closing: use reference DNA for trust tone, product set display, brand memory, and final commercial rhythm.

For every screen, specify which DNA elements are inherited and which reference elements are intentionally ignored.

## Information Density Rhythm

Assign light, medium, or heavy density before prompting:

- Light screens: hero memory, emotional scene, premium mood, simple benefit.
- Medium screens: usage, practical value, most selling points.
- Heavy screens: mechanism, comparison, ingredient map, parameter table, trust proof.

The full 10-screen set should not be all heavy proof pages or all sparse mood pages. Use density rhythm to make the page feel deliberate.

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

| Screen | Role | Fixed direction | Message source | Consumer-facing expression | Visual evidence | Main subject | Product exposure | Proof form | Density | Reference weight | DNA carried | Main copy | Supporting copy | Claim boundary | Why it proves the copy |

## Detail Prompt Must Include

- Strict 3:4 vertical detail-page screen, approximately 1200x1600; not 9:16, not phone-story, not long poster.
- One independent detail-page screen only, ready to save as a numbered final file.
- **Picture Solo Statement** (the one-line "the picture is X, with text hidden it shows Y") at the top of the prompt.
- **Consumer-voice copy lock**: all copy in this screen passes the "so what?" test — written from the consumer's perspective, no manufacturer/spec-sheet voice.
- Reference-role rules: inherit light, type, density, mood only — NOT scene/setting.
- Brand/product-adapted color palette.
- Scene/use logic check.
- Chosen message-picture pattern and the pattern's product-presence rule.
- Chosen visual proof form and density level.
- Consumer-facing expression, main subject, and product exposure level (explicit: hero / medium / partial / small / none).
- Reference weight and visual DNA carried by this screen.
- **Scene element note**: if this screen uses a reference-scene element, name it and confirm it's within the 3-of-10 budget; if not, state "no reference-scene elements used".
- Visual distance note: how this screen's main visual differs from adjacent screens.
- Model source and model-consistency lock when people appear.
- Exact Chinese copy (consumer voice).
- Complete model-native Chinese typography: title, subtitle, optional short support copy. No icons.
- **Explicit anti-icon line**: "no icons, no pictograms, no badge ribbons, no feature-icon rows, no ingredient bubbles, no decorative arc systems".
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
2. Save it to `<task-folder>/详情页/01-*.png`.
3. Check 3:4 ratio, product accuracy, screen role, narrative fit, copy readability, and claim safety.
4. Regenerate `D01` until it passes or record the blocker.
5. Repeat the same one-screen loop for `D02` through `D10`.
6. After all ten independent files pass, create a contact sheet for review.
