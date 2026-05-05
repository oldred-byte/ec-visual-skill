---
name: ec-visual
description: "Use when the user uploads product images and visual references to create 5 marketplace head images and 10 product detail page screens with reference analysis, product-adapted color, planning, prompts, and optional final images."
---

# EC Visual

## Overview

Create a complete e-commerce visual set from product image(s) and visual reference(s): 5 square marketplace head images and 10 vertical detail-page screens. The skill is a closed-loop production workflow: analyze references, generate, validate, regenerate, and feed reusable failures back into the skill before reporting completion. References provide layout logic, information structure, creative methods, and visual rhythm without mechanically copying their products, colors, brands, prices, people, or claims.

## When To Use

Use this skill when the user asks to:

- Generate product head images, Taobao/Tmall/JD/Douyin main images, product main images, or marketplace listing images from product + reference images.
- Generate a complete set containing both 5 head images and 10 detail-page screens.
- Turn product images plus a poster/head-image/detail-page reference into planned image prompts or final images.
- Build reusable prompts for e-commerce visuals from visual references.

If the user asks only for a single generated image, still use the relevant reference rules from this skill when the task is e-commerce product imagery.

## Required Inputs

Identify what the user provided:

- Product image(s): define product appearance, color, material, packaging, structure, logo/packaging text if visible.
- Reference image(s): may be first head-image reference, head-image set reference, detail-page reference, poster reference, or mood/style reference.
- Product facts: name, category, specs, selling points, target users, usage scenes, price/promo. Do not invent missing facts.
- Model source when people appear: whether human images should use a model from the reference image, a model from the product image, or a newly generated campaign model.

When important facts are missing, make conservative generic claims or ask only if the omission prevents the work. For clothing, apparel, wearable fashion, or any product where the model is part of the product presentation, ask one question before planning or generation if the user has not specified the model source: "人物用参考图模特、产品图模特，还是重新生成模特？" Never invent prices, certifications, test results, medical effects, official stores, or brand authorization.

Use the visible-evidence rule: if a benefit is not visible in the product image and not provided by the user, do not state it as a specific capability. Category-generic copy is allowed only when phrased softly. For example, an umbrella can use "rainy-day commute" or "easy to carry", but cannot claim "UPF 50+", "sun-rain dual use", "stormproof", "automatic open/close", or "water-repellent coating" unless visible or supplied.

## Workflow

1. Inspect all images and classify each reference role using `references/reference-analysis.md`.
2. Extract a flavor contract from the strongest reference image: camera attitude, human/product relationship, whitespace tension, typography behavior, density, and commercial genre. Do not reduce a reference to surface labels like "white background" or "big product".
3. Build a model-consistency plan when any image will contain people: choose the model source, lock a stable model identity/persona, and keep all recurring model appearances consistent across head images and detail pages while allowing pose, gesture, crop, camera angle, expression intensity, and product interaction to change by image role.
4. Build a product-use plausibility map: how the product is normally held, worn, opened, applied, placed, or operated; which poses are impossible or awkward; which reference gestures must be translated rather than copied.
5. Build the product-adapted color system using `references/color-adaptation.md`.
6. Plan the 5 head images using `references/head-images.md`. If a poster/mood reference is the strongest reference, include a 5-image flavor transfer matrix before prompts so image 2-5 inherit the reference flavor instead of drifting into generic selling-point templates.
7. Plan the 10 detail-page screens using `references/detail-pages.md`.
8. Output planning tables first unless the user explicitly asked to directly generate.
9. For generation, write one prompt per image/screen. Use the imagegen skill/tool for bitmap generation.
10. When maturing or validating this skill, generate the full requested batch because many failures only appear across the set: continuity drift, repeated modules, inconsistent claims, ratio spread, typography/layout drift, and detail-page narrative gaps. Key samples are only optional preflight checks for obvious direction errors; they do not replace full-batch validation.
11. Save final generated images into the current project folder in clear subfolders, for example `输出/头图` and `输出/详情页`.
12. Use `references/production-loop.md` for validation, regeneration, and skill feedback. Self-check results: product consistency, text readability, color adaptation, reference-element overuse, layout logic, flavor match, product-use plausibility, and claim safety. Regenerate flawed images and patch reusable rules before calling the deliverable done.

## Direct Generation Contract

When the user asks to make actual image deliverables, use this production path:

1. Call the `imagegen` skill/tool for the final commercial visual.
2. Generate each requested deliverable as its own image: one prompt for one head image or one detail-page screen.
3. Save generated results from the default generated-images folder into the project output folder:
   - Head images: `输出/主图/01-...png` through `输出/主图/05-...png`.
   - Detail pages: `输出/详情页/01-...png` through `输出/详情页/10-...png`.
4. Use contact sheets only after the independent final files exist, as review artifacts named like `主图_contact_sheet.jpg` and `详情页_contact_sheet.jpg`.
5. Do not use deterministic local compositing, local text overlay, or local image repair on final deliverables. Final head images and detail screens must come directly from the image model. Local tools may only copy/save files, inspect dimensions, and assemble contact sheets for review artifacts.
6. Validate every saved file before reporting completion: file exists, aspect ratio is correct, product is accurate, visual quality is commercial, copy is readable/safe, and the image role matches the plan.

## Autonomous Delivery Loop

When the user asks for actual image deliverables, do not stop after planning, prompt writing, or a single failed/partial generation. Run an autonomous delivery loop:

1. Read and follow `references/production-loop.md`.
2. Optionally use key samples as preflight for obvious direction errors.
3. Generate the full requested batch for validation, with one final file per requested image or screen.
4. Validate the complete set, then repair prompts or skill rules based on batch-level failures.
5. Regenerate the full batch or failed slices as needed, depending on whether the failure is systemic or isolated.
6. Validate the full set visually, regenerate failed images individually, and feed reusable failures back into the skill.
7. Report completion only when requested files exist on disk, pass validation, and the validation report is saved. If the set cannot pass after the allowed loop count, report failure and the exact blocker.

Prompts for final deliverables should explicitly say "single independent final
image only" or "single independent detail-page screen only" so the image model
returns the delivery shape needed for saving and validation.

When testing or validating this skill, if the user requested real output, use the same autonomous delivery loop. A dry pass is only acceptable when the user explicitly asks for analysis, planning, or prompt design instead of generated deliverables.

For generated detail pages, check aspect ratio before anything else. Detail pages must be strict 3:4 vertical; if the image generator returns 9:16 or any other ratio, regenerate with stronger aspect wording. If Chinese text or typography does not match the intended poster/detail-page layout, regenerate with clearer copy hierarchy and layout direction.

## Model-Native Text Workflow

Final commercial outputs must rely on the image model for all visible image content, including Chinese text, typography, and commercial layout. Treat model-native multi-text poster generation as the default production path.

If direct generation produces incorrect Chinese, weak hierarchy, or unsatisfactory typography, repair by strengthening the prompt's copy hierarchy, font direction, spacing, module rhythm, and poster/detail-page layout requirements, then regenerate. Do not add, correct, replace, or repair text with PIL, HTML/CSS screenshots, local drawing, masks, inpainting outside the model, or any other deterministic compositor.

## Non-Negotiable Rules

- Reference images are not templates to copy blindly; they must be decomposed into roles.
- Final success means a complete usable deliverable plus a validation record, not only a plan, prompt set, partial batch, or skill patch.
- For actual deliverables, the agent owns the whole loop: generate, inspect, diagnose, patch reusable rules, regenerate, and save final files.
- Deliverables are independent generated image files; contact sheets are secondary review artifacts.
- Final deliverables must be model-native images with no local compositing, local text overlay, local retouching, or small layout repair. Contact sheets are allowed only as secondary review artifacts after independent final files exist.
- Product accuracy outranks reference style.
- When a model appears in more than one output, model identity consistency is mandatory: keep the same face structure, age range, hair, styling logic, body type, skin tone, and overall presence unless the plan explicitly calls for different personas. Do not keep the same pose by default; choose poses, gestures, crops, and product interactions separately for each image's content and sales role.
- If a clear first head-image reference exists, the first generated head image must strongly follow its layout skeleton and information format.
- If no clear first head-image reference exists, use the default strong e-commerce first-image skeleton in `references/head-images.md`.
- Color must be rebuilt around the product. Do not copy the reference's dominant color unless it fits the product and category.
- A reference can provide layout, module logic, information hierarchy, and creative methods even when its color is rejected.
- A poster/mood reference can provide the overall flavor. Default e-commerce skeletons must be bent toward that flavor, not allowed to erase it.
- Poster flavor is a set-level constraint, not only a first-image constraint. Images 2-5 may change proof method and content role, but they should still preserve selected flavor dimensions from the same contract.
- Every image must be visually and logically connected to its copy. Good-looking but irrelevant visuals fail.
- Every human-product interaction must be physically and behaviorally plausible for the actual product category. Translate reference gestures into equivalent product-appropriate gestures; do not copy a hand pose, camera angle, or foreground drama if it makes the product look awkward, unsafe, impossible, or unlike how people use it.
- Avoid mechanical repetition: do not place the same card, badge, icon row, large number, or background motif in every image unless the user explicitly asks.
- Do not copy reference brands, logos, prices, original text, certifications, scenes, or exact product-specific claims. Do not copy reference people unless the user has chosen the reference-image model as the model source.
- Do not make medical, therapeutic, or official certification claims unless supplied by the user.
- Do not mistake "category-safe" for "visually generic". Safety rules restrict claims, not visual ambition.

## Output Shape

Default deliverable when not directly generating:

1. Reference role analysis.
2. Flavor contract and taste-gap risks.
3. Product-adapted color system.
4. 5-head-image planning table.
5. 10-detail-page planning table.
6. 15 generation prompts: 5 head images plus 10 detail-page screens.

Default deliverable when directly generating:

1. Brief planning summary.
2. Generate and save 5 head images and/or 10 detail-page screens as requested, as separate final image files.
3. Create contact sheets only as review artifacts, not replacements for the separate final files.
4. Report saved paths and any regeneration/self-check notes.

## References

Read only the needed reference files:

- `references/reference-analysis.md`: classifying product/reference images and deciding what can transfer.
- `references/color-adaptation.md`: product-first color system and anti-color-copy rules.
- `references/head-images.md`: 5 head-image structure, including first-image layout-copy rule and default first-image skeleton.
- `references/detail-pages.md`: 10-screen detail-page structure and prompt format.
- `references/production-loop.md`: autonomous generation, validation, iteration, and skill feedback loop. Read this whenever producing real deliverables or validating the skill.
