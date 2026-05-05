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

1. Analyze inputs: product facts, reference roles, model source when people appear, flavor contract, color system, product-use plausibility map, claim safety.
2. Optionally generate key sample(s) only as a preflight for obvious direction errors. Do not treat preflight as validation of the skill.
3. Build a numbered generation queue: `H01-H05` for head images and `D01-D10` for detail screens.
4. For each queue item, call the image generation tool with one prompt for one final image. Include the target ratio and the phrase "single independent final image only".
5. Copy each generated output into the project folder immediately after generation using the queue id in the filename.
6. After all requested files exist, make contact sheets or comparable visual review artifacts for head images and detail pages.
7. Validate the complete set with the gate checklist and set-level checks.
8. Classify each failure as prompt-only, skill-rule, generator limitation, or input limitation.
9. Regenerate failed slices individually when failures are isolated; regenerate the full batch when the failure is systemic.
10. Repeat up to 5 validation/regeneration rounds.
11. Save final images, prompts or prompt summary, validation report, and unresolved risks.

If generation returns the wrong delivery shape, immediately re-prompt that queue
item as one independent final image before continuing.

## Gate Checklist

Each generated image must pass:

- Product accuracy: shape, color, structure, distinctive pattern/packaging, and visible details remain true to the product image.
- Model identity consistency: every recurring model appearance keeps the same face structure, age range, hair, skin tone, body type, expression range, and styling attitude. Poses, gestures, crops, camera angles, expression intensity, and product interactions may and should vary according to each image role. For clothing/apparel/wearable fashion, the chosen model source matches the user's answer.
- Product-use plausibility: a real person would hold, wear, place, operate, or interact with the product this way.
- Reference flavor: selected flavor dimensions survive beyond surface layout copying.
- Reference role discipline: use layout/logic/creative method, not copied brand, person, claim, color, or category-specific feature.
- Layout/content fit: the visual actually proves the copy and does not create logic contradictions.
- Color adaptation: palette is rebuilt around the product and category, not blindly copied from the reference.
- Claim safety: no invented price, official status, certification, specs, ratings, medical effects, or unsupported performance.
- Aspect ratio: head images are square; detail pages are strict 3:4 vertical.
- Delivery shape: every requested head image or detail screen is saved as its own final file.
- Commercial finish: final output looks like a polished e-commerce visual with generated scene, light, product rendering, perspective, and campaign flavor.
- Text and typography readiness: generated Chinese, hierarchy, spacing, and commercial layout are suitable for final review using model-native output only; if not, refine layout/copy hierarchy in the prompt and regenerate instead of applying local text overlay.

## Set-Level Checks

Full-batch validation must check failures that single images cannot reveal:

- Head-image continuity: the 5 images feel like one campaign system, not five unrelated templates.
- Model identity continuity: all recurring model appearances across head images and detail pages feel like the same campaign model, while poses and interactions vary naturally by scene, unless the plan explicitly uses separate personas.
- Role separation: image 1 is click/main, images 2-4 prove different selling points, image 5 addresses audience/persona.
- Detail-page narrative: the 10 screens progress from hero to scene/problem, selling points, details/trust, and closing without random order.
- Repetition control: the same card, icon row, badge, layout, or visual metaphor is not overused across the set.
- Claim consistency: claims do not contradict each other or become more specific than the input supports.
- Color consistency: product-adapted palette remains coherent across all images without becoming one-note or copied from the reference.
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

## Skill Feedback Rule

When a generated output fails in a way that could happen again with another product/reference, update the relevant reference file:

- Reference role, flavor, transfer, product-use, or taste-gap issue: patch `references/reference-analysis.md`.
- Head-image composition, 5-image set logic, first-image fallback, or persona/selling image issue: patch `references/head-images.md`.
- Detail-page structure, aspect ratio, screen logic, or typography/layout issue: patch `references/detail-pages.md`.
- Product-first palette or reference color-copy issue: patch `references/color-adaptation.md`.
- Delivery loop, validation, regeneration, or definition-of-done issue: patch this file or `SKILL.md`.

After patching, run the skill validator.

## Known Regression Tests

Use these failures as regression checks when validating future updates:

- Do not claim skill maturity from a single generated image. Maturity requires full-batch validation.
- When maturing a skill that covers both head images and detail pages, validate both sides as complete sets: 5 head images and 10 detail-page screens.
- Do not turn a poster/mood reference into a generic dense marketplace card template.
- Do not copy a reference hand pose when the target product is used differently.
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
- Flavor contract summary.
- Product-use plausibility map.
- Color system.
- Generated files.
- Failed checks and fixes.
- Skill files patched.
- Final pass/fail status and remaining risks.
