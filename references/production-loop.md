# Production Loop

Use this file whenever producing real e-commerce images or maturing the skill through test generation.

## Definition Of Done

A task is not done until all requested deliverables exist on disk and a validation note is saved. A plan, prompt set, partial batch, or rule patch is not a completed image deliverable.

Each requested deliverable exists as its own final image file. The final folder
contains numbered head images and/or numbered detail pages. Contact sheets are
saved as separate review artifacts after the final files exist.

When the user asks to directly generate e-commerce visuals, the final files are
commercially polished generated bitmap images produced directly by the image
model. Do not use deterministic local compositing, local text overlay, local
retouching, or local layout repair on final deliverables. Local tools may only
copy/save outputs, inspect files, and assemble contact sheets or comparable
review artifacts after independent final files exist.

When the task is to mature this skill, the final deliverable is the updated skill folder plus validation evidence showing which generated failures were used to improve it.

## Operating Loop

For a new product/reference pairing:

1. **Create task folder (do this FIRST)**: create a fresh folder at `~/Desktop/YYYYMMDD-HHMM-<产品名或类别>/`. Use the current date/time and a short product/category slug (e.g., `20260705-1730-英式辅食`, `20260705-1945-小米耳机`). All outputs for this task go ONLY into this folder. Never write into a folder containing previous-task files. See Task Folder Isolation section below for full rules.
2. Analyze inputs: product facts, documents, information completeness route, reference roles, model source when people appear, visual DNA contract (language only, NOT scene), color system, product-use plausibility map, claim safety, and selling-point bank.
3. Preserve any user-approved screen directions as the hard scaffold. Build a consumer-angle map and translate each screen into a mature expression rather than replacing the structure.
4. Build the visual proof plan: Picture Solo Statement, consumer-facing expression, **consumer-voice copy**, visual evidence, main subject, product exposure, core message, pattern match (from `message-picture-patterns.md`), density, reference weight, DNA carried, and visual distance for every requested output.
5. **Output the unified approval** — ONE batch covering both head images AND detail pages together. Include:
   - **5-Image Main-Visual Diversity Board** with Picture Solo Statement, pattern, scene setting, main subject, composition, product presence, and draft consumer-voice copy for each of H01-H05.
   - **10-Screen Main-Visual Diversity Board** with the same columns plus claim boundary for each of D01-D10.
   - Set-level summary: visual DNA contract, color system, scene cap status, product-presence mix status.
   Reject the plan and regenerate if main-visual overlap exceeds the threshold (≥4 distinct main visuals for 5 images; ≥7 for 10 screens). Confirm Scene Cap (≤30% reference-scene element). Confirm product-presence mix (at least 4 of 10 detail screens have "no packaging" or "partial only").
6. **Wait for user approval** on the unified batch. The user may approve, ask for adjustments to specific rows, or reject the plan. Do not generate any image until approval is given, unless the user explicitly says to skip review.
7. After approval (or skip), optionally generate key sample(s) only as a preflight for obvious direction errors. Do not treat preflight as validation of the skill.
8. Build a numbered generation queue: `H01-H05` for head images and `D01-D10` for detail screens.
9. For each queue item, call the image generation tool with one prompt for one final image. Include the target ratio, the Picture Solo Statement, the pattern match, the product-presence rule, the consumer-voice copy lock, and the phrase "single independent final image only". Include the anti-icon line.
10. Copy each generated output into the task folder immediately after generation using the queue id in the filename.
11. After all requested files exist, make contact sheets or comparable visual review artifacts in `<task-folder>/记录/`.
12. Validate the complete set with the gate checklist and set-level checks.
13. Classify each failure as prompt-only, skill-rule, generator limitation, or input limitation.
14. Regenerate failed slices individually when failures are isolated; regenerate the full batch when the failure is systemic.
15. Repeat up to 5 validation/regeneration rounds.
16. Save validation report to `<task-folder>/验证报告.md`. Save prompt summary to `<task-folder>/记录/prompts.md`. Note unresolved risks.

If generation returns the wrong delivery shape, immediately re-prompt that queue
item as one independent final image before continuing.

## Task Folder Isolation (mandatory)

Every new task creates a fresh, isolated folder on the user's Desktop. This replaces the old "输出/" relative-folder approach which caused mixed-batch errors.

### Folder Location And Naming

- **Default location**: `~/Desktop/`
- **Format**: `YYYYMMDD-HHMM-<产品名或类别>`
- **Examples**:
  - `20260705-1730-英式辅食`
  - `20260705-1945-小米真无线耳机`
  - `20260706-0900-欧莱雅紫熨斗`
  - `20260706-1400-蕉内基础款`

The `<产品名或类别>` slug should be:

- The product brand or category, in the user's language (Chinese is fine)
- Short (2-10 characters typical)
- No spaces, no special characters that need escaping
- Based on what's visible in the product image or what the user calls it

### Folder Structure

```
<task-folder>/
  主图/
    01-<short-description>.png
    02-<short-description>.png
    03-<short-description>.png
    04-<short-description>.png
    05-<short-description>.png
  详情页/
    01-<short-description>.png
    ...
    10-<short-description>.png
  记录/
    主图-contact-sheet.png
    详情页-contact-sheet.png
    prompts.md
  验证报告.md
```

### Hard Rules

- **Always create a new folder**: never write into an existing folder that contains files from another task.
- **No mixing**: outputs from different tasks NEVER live in the same folder.
- **No reusing old folders**: even if the previous task was the same product, create a new timestamped folder. This makes version history explicit.
- **User can override location**: if the user says "put it in /path/to/folder", respect that. But still use the timestamp+slug naming convention.
- **If a folder with the same name exists**: append `-2`, `-3`, etc., or include a more specific slug.

### Why This Matters

Previous versions of this skill wrote outputs to a relative `输出/` folder. This caused real errors:

- Files from a previous task (different product) shipped as if they were the new batch.
- The user had to manually disambiguate which files were current.
- Version control was impossible because old and new files interleaved.

Task folder isolation makes every task self-contained, timestamped, and named — easy to find across tasks, easy to compare, impossible to accidentally mix.

## Gate Checklist

Each generated image must pass:

- **Picture Solo Test**: cover all copy in the generated image mentally; does the picture alone still convey the message? If no, regenerate.
- **Consumer-voice copy**: every line of copy passes the "so what?" test — the consumer instantly knows what's in it for them. No "采用XX技术", "本产品具有XX功能", "符合XX标准", "XXX工艺打造" voice. If found, regenerate.
- **No icons**: the image contains no pictograms, no feature-icon rows, no ingredient bubbles, no badge ribbons, no decorative arc systems. Labels allowed only when pointing to real visible parts.
- **Product presence match**: the product/packaging presence in the generated image matches the planned pattern's rule. If the pattern said "no packaging" but the image shows packaging, regenerate.
- **Reference-scene match**: if the planned screen was NOT in the reference-scene-element budget, the image must not contain the reference's specific scene elements.
- Product accuracy: shape, color, structure, distinctive pattern/packaging, and visible details remain true to the product image.
- Information route discipline: supplied facts are preserved, partial facts are improved without distortion, and missing facts are handled with visible/category-generic claims only.
- Model identity consistency: every recurring model appearance keeps the same face structure, age range, hair, skin tone, body type, expression range, and styling attitude. Poses, gestures, crops, camera angles, expression intensity, and product interactions may and should vary according to each image role. For clothing/apparel/wearable fashion, the chosen model source matches the user's answer.
- Product-use plausibility: a real person would hold, wear, place, operate, or interact with the product this way.
- Visual proof fit: the main visual is the most direct proof for the core message, and people/modules/macros/charts are used only when they help prove it.
- Screen expression fit: the output follows the approved consumer-facing expression, not just the broad screen role.
- Main-subject discipline: the chosen subject matches where the benefit is experienced or proven. The product is not forced into hero position when a body detail, component, action, mechanism, scene, or result state is the stronger proof.
- Product exposure discipline: full-product, partial-product, human/body, scene, and mechanism-led screens vary intentionally according to the plan.
- Reference DNA: selected reference dimensions (light/type/density/mood) survive beyond surface layout copying.
- Reference role discipline: use language/logic/creative method, not copied brand, person, claim, color, category-specific feature, OR specific scene/setting element.
- Layout/content fit: the visual actually proves the copy and does not create logic contradictions.
- Reference weight discipline: head images may use reference structure more strongly, while detail pages remain content-led and carry reference DNA selectively.
- Color adaptation: palette is rebuilt around supplied brand colors when present, otherwise around product and category, not blindly copied from the reference.
- Claim safety: no invented price, official status, certification, specs, ratings, medical effects, or unsupported performance.
- Aspect ratio: head images are square; detail pages are strict 3:4 vertical.
- Delivery shape: every requested head image or detail screen is saved as its own final file.
- Commercial finish: final output looks like a polished e-commerce visual with generated scene, light, product rendering, perspective, and campaign flavor.
- Text and typography readiness: generated Chinese, hierarchy, spacing, and commercial layout are suitable for final review using model-native output only; if not, refine layout/copy hierarchy in the prompt and regenerate instead of applying local text overlay.

## Set-Level Checks

Full-batch validation must check failures that single images cannot reveal:

- **Main-visual diversity (HARD)**: 5 head images use ≥4 distinct main visuals; 10 detail screens use ≥7. If the threshold fails, the set is broken — re-plan.
- **Scene Cap (HARD)**: no single reference-scene element appears in more than 30% of outputs.
- **Product-presence mix**: at least 4 of 10 detail screens have "no packaging" or "partial only". If all 10 show full packaging, the plan failed and the set is broken.
- **Icon-free across the set**: scan all outputs; if any icon/pictogram/feature-row slipped in, regenerate that output.
- **Consumer-voice copy across the set**: scan all copy in all outputs; no manufacturer/spec-sheet/deck voice anywhere. Headlines and support copy all speak to the consumer.
- **Detail-page ≠ vertical head image**: D01-D10 do not look like pixel-stretched versions of H01. Each screen has its own main visual.
- Head-image continuity: the 5 images feel like one campaign system, not five unrelated templates.
- Head-image visual distance: the 5 images do not repeat the same proof form, camera distance, card system, or product pose unless the repetition is intentionally justified.
- Model identity continuity: all recurring model appearances across head images and detail pages feel like the same campaign model, while poses and interactions vary naturally by scene, unless the plan explicitly uses separate personas.
- Role separation: image 1 is click/main, images 2-4 prove different selling points, image 5 addresses audience/persona.
- Detail-page narrative: the 10 screens progress from hero to scene/problem, selling points, details/trust, and closing without random order.
- Detail-page proof rhythm: each screen uses a message-appropriate proof form, with a deliberate mix of scene, macro, mechanism, comparison, parameter, trust, and closing where relevant.
- Detail-page expression rhythm: adjacent screens do not repeat the same full-product hero, headline position, and soft background unless the approved plan explicitly requires it.
- Fixed-structure respect: if the user supplied the screen directions, the generated set preserves those directions while improving expression inside each screen.
- Set-level visual DNA: all outputs carry shared color/type/light/module language while varying composition, density, and main visual.
- Repetition control: the same card, layout, or visual metaphor is not overused across the set.
- Claim consistency: claims do not contradict each other or become more specific than the input supports.
- Color consistency: brand/product-adapted palette remains coherent across all images without becoming one-note or copied from the reference.
- Ratio consistency: all head images are square; all detail pages are strict 3:4 vertical.
- Text-layout consistency: later detail pages maintain coherent model-native typography, spacing, hierarchy, and commercial rhythm.

## Key Sample Selection

Key samples are optional preflight, not final validation. Use them only to avoid wasting a full batch on an obviously wrong direction:

- Head-image-only task: generate one first head image.
- Detail-page-only task: generate one detail hero or one hardest detail screen.
- Complete head-image + detail-page task: generate one first head image and one detail hero screen before any full batch.
- Skill-maturity task: still requires full-batch validation after any preflight, because the skill must prove it works across the complete 5-head-image and 10-detail-page structure.

The head-image key sample tests marketplace click logic, reference flavor, product-use plausibility, and product hero composition.

The detail-page key sample tests vertical ratio, sequential detail-page language, typography/layout hierarchy, scene/copy logic, and whether the reference flavor still works in a tall explanatory screen.

## Failure Classification

Classify every failure before fixing it:

- Prompt-only failure: the skill already has the right rule, but the current prompt missed it. Fix the prompt and regenerate.
- Skill-rule failure: the rule is absent, too soft, too buried, or contradicted by another rule. Patch the skill before regenerating.
- Generator limitation: the model cannot reliably preserve product appearance, layout shape, text hierarchy, or intended commercial typography after repeated prompt repairs. Refine the prompt or record the blocker; do not switch to local compositing or local text overlay.
- Input limitation: required facts or product angles are missing. Use only visible/category-generic claims, or state the limitation.

Patch the skill only for reusable failures. Do not bloat the skill with one-off taste notes that belong only to a single product.

## Post-Iteration Skill-Learning Hook

Use this hook when all three conditions are true:

1. The user found a problem during use, such as similar outputs, wrong product interaction, bad density rhythm, weak reference DNA, unsupported claims, or a screen that did not visually prove its message.
2. The issue was adjusted through revised planning, prompts, regeneration, or rule clarification.
3. The user says the adjusted result is OK, accepted, approved, or good enough.

After acceptance, ask once, adapted to the user's language:

"This adjustment is accepted. Do you want me to summarize the root cause and decide whether it should be added back into the ec-visual skill as a reusable rule?"

If the user says yes:

- Summarize the symptom, root cause, reusable lesson, and which reference file should change.
- Patch only the most relevant skill file.
- Prefer general decision rules over one-off taste notes.
- Do not add product-specific claims, brand-specific preferences, or a single user's temporary taste preference as global rules.
- After patching, report what changed and why.

If the user says no:

- Do not patch the skill.
- Keep the current task result as accepted and move on.

If the issue is already covered by an existing rule, do not duplicate the rule. Record it as a prompt/application failure and improve the current prompt or validation behavior instead.

## Skill Feedback Rule

When a generated output fails in a way that could happen again with another product/reference, update the relevant reference file.

Folder and copy failures route to:

- **Folder mixing / wrong location / missing timestamp**: patch this file's Task Folder Isolation section or `SKILL.md`.
- **Manufacturer-voice copy / explanatory copy / spec-sheet copy**: patch `references/visual-proof-grammar.md` Copy Voice section.

Other failures route to:

- Product facts, document extraction, missing/partial information routing, or selling-point extraction issue: patch `references/input-routing.md`.
- Reference role, flavor, transfer, product-use, taste-gap, or **scene-template-copy** issue: patch `references/reference-analysis.md`.
- Set consistency, reference weight, visual DNA, coherent-but-not-repetitive, or **scene-cap / main-visual-diversity** issue: patch `references/visual-dna.md`.
- Picture Solo Test, message-to-picture fit, proof method, density rhythm, **no-icon rule**, or **product-presence** issue: patch `references/visual-proof-grammar.md`.
- **Message-to-picture pattern** library gap (new pattern needed, or existing pattern unclear): patch `references/message-picture-patterns.md`.
- Head-image composition, 5-image set logic, first-image fallback, persona/selling image, or **5-image diversity board** issue: patch `references/head-images.md`.
- Detail-page structure, aspect ratio, screen logic, typography/layout, or **10-screen diversity board / detail-page-≠-vertical-head-image** issue: patch `references/detail-pages.md`.
- Product-first palette or reference color-copy issue: patch `references/color-adaptation.md`.
- Delivery loop, validation, regeneration, definition-of-done, **output hygiene**, or **set-level pre-check** issue: patch this file or `SKILL.md`.

After patching, run the skill validator.

## Known Regression Tests

Use these failures as regression checks when validating future updates:

- Do not claim skill maturity from a single generated image. Maturity requires full-batch validation.
- When maturing a skill that covers both head images and detail pages, validate both sides as complete sets: 5 head images and 10 detail-page screens.
- **Do not let all 5 head images or all 10 detail screens share the same main visual** (same scene + same subject + same composition). This is the #1 user-reported failure. Reject the plan at the diversity board stage and regenerate.
- **Do not copy the reference's specific scene elements (fabric, surface, location) into more than 30% of outputs.** The reference provides language, not scene.
- **Do not let packaging appear on every screen by default.** Most selling-point, sensory, ingredient, and mechanism screens have NO packaging in the main visual.
- **Do not include any icons, pictograms, feature-icon rows, ingredient bubbles, badge ribbons, or decorative arc systems.** No exceptions.
- **Do not skip the Picture Solo Test.** Every output must work with all copy covered.
- **Do not skip the diversity board.** The plan is rejected before prompts if the diversity threshold fails.
- **Do not generate into a folder containing files from a previous task.** Create a fresh task folder at `~/Desktop/YYYYMMDD-HHMM-<产品名或类别>/` first.
- **Do not write copy in manufacturer/spec-sheet/deck voice.** Every line of copy must pass the consumer "so what?" test. No "采用XX技术", "本产品具有XX功能", "符合XX标准" voice.
- **Do not split head-image approval from detail-page approval.** Output ONE unified approval table (5 + 10 with draft copy) and let the user review both as one batch.
- Do not turn a poster/mood reference into a generic dense marketplace card template.
- Do not copy a reference hand pose when the target product is used differently.
- Do not let a reference composition override a detail page's core message and best visual proof.
- Do not add a person when the message is better proven by macro material, parameter clarity, product structure, ingredient logic, or product set display.
- Do not let the full set become scattered; every output should carry selected visual DNA from the same system.
- Do not let the full set become repetitive; vary proof form, camera distance, density, and main subject across the set.
- Do not ignore an approved 10-screen direction list. Preserve the structure and improve each screen's consumer expression.
- Do not make the full product the main hero on every detail screen. Product exposure should follow the proof task.
- For umbrellas, do not thrust an open canopy horizontally at the viewer like a small handheld gadget. Use natural handle/shaft grip and canopy placement.
- Do not let images 2-5 drift into unrelated templates after image 1 captures the reference flavor.
- Do not let recurring model identity drift across the set. Clothing/apparel/wearable fashion tasks must resolve the model source before generation: reference-image model, product-image model, or newly generated model.
- Do not copy reference dominant colors when they do not fit the product.
- Do not invent unsupported claims such as UV, windproof, certifications, official store, price, size, or weight.
- Do not accept detail pages that are 9:16; regenerate to strict 3:4 vertical.
- Do not accept a generated grid/contact sheet/collage as the final 5 head images or 10 detail pages. Save independent final files and use contact sheets only for review.
- Do not substitute flat local compositing for requested generated commercial visuals.
- Do not use local text overlay, local retouching, or deterministic compositing for final deliverables. Use model-native text and model-native commercial typography; regenerate with stronger hierarchy and layout direction when text or layout fails.

## Validation Report

Save a concise Markdown report near the output folder containing:

- Input files and reference roles.
- Information completeness route and selling-point bank summary.
- Visual DNA contract summary.
- Product-use plausibility map.
- Color system.
- Visual proof and density plan summary.
- Generated files.
- Failed checks and fixes.
- Skill files patched.
- Final pass/fail status and remaining risks.
