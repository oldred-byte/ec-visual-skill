---
name: ec-visual
description: "Use when the user uploads product images and visual references to create or improve marketplace head images and product detail pages. Includes consumer-angle mapping, fixed-screen detail-page expression planning, visual proof selection, brand/product-adapted color, prompts, and optional final image generation."
---

# EC Visual

## Overview

Create e-commerce visual systems from product image(s), reference image(s), and optional product facts: 5 marketplace head images and/or 10 vertical detail-page screens. References are used as visual language sources, not rigid templates. Product facts, any user-approved screen directions, and each screen's consumer-facing expression task decide the content; reference DNA, product/brand color, and proof grammar decide how the set stays coherent and commercially useful.

## When To Use

Use this skill when the user asks to:

- Generate product head images, Taobao/Tmall/JD/Douyin main images, product main images, or marketplace listing images.
- Generate detail-page screens or a complete set containing both 5 head images and 10 detail-page screens.
- Turn product images plus poster/head-image/detail-page references into planned image prompts or final images.
- Build reusable e-commerce visual prompts from product facts, documents, and visual references.

If the user asks for only one e-commerce image, still use the relevant input, reference, color, product-use, and visual-proof rules.

## Workflow

1. Inspect all product images, reference images, and uploaded documents. Classify image roles with `references/reference-analysis.md`.
2. Route product information with `references/input-routing.md`: if the user uploaded only images and no product facts, ask once whether they have selling points, product information, brand colors, parameters, or documents to provide before planning. Complete facts are followed, partial facts are preserved and improved, missing facts are inferred conservatively from product image and category context.
3. Capture any user-provided page structure or screen directions as hard scaffolding. Do not replace an approved 10-screen direction with a new generic sequence; translate each fixed screen direction into a stronger consumer-facing expression.
4. Build a consumer-angle map with `references/input-routing.md`: category anxieties, desired outcomes, body/use moments, objections, and what evidence would make a buyer believe each point.
5. Extract a set-level visual DNA contract from the strongest reference(s) using `references/visual-dna.md`. Treat the reference as visual language only (light behavior, typography attitude, density rhythm, commercial temperature). Reference scene/setting elements (specific fabric, specific surface, specific location, specific background texture) are NOT inherited by default and may appear in at most 30% of outputs.
6. Build the color system with `references/color-adaptation.md`: user-provided brand colors first when supplied, otherwise product identity colors first. Reference colors are borrowed only as organization logic unless they fit the product/brand.
7. Build product-use plausibility, interaction translation, claim safety, and model consistency plans with `references/reference-analysis.md`.
8. For every image/screen, write a Picture Solo Statement first using `references/visual-proof-grammar.md`: one sentence describing the concrete picture, followed by what message it proves when all copy is covered. If the picture cannot convey the message alone, redesign the picture before continuing.
9. Decide product presence per screen using `references/message-picture-patterns.md`: match the screen's message to a pattern, then follow that pattern's product-exposure rule. The product does NOT appear by default; it appears only when the message requires it.
10. **Unified Plan + Approval Gate (mandatory)**: Plan head images and detail pages TOGETHER as one batch. Output ONE unified approval table that covers all 5 head images AND all 10 detail-page screens — each row containing: picture solo statement, pattern match, main subject, product exposure, scene setting, AND draft consumer-voice copy. User reviews this single table and approves or modifies before ANY prompt is written or ANY image is generated. Do not split head-image approval from detail-page approval. See `references/head-images.md` and `references/detail-pages.md` for table structure. Skip only when the user explicitly says to skip review.
11. For final image deliverables, write one prompt per image/screen and use the image generation tool. Follow `references/production-loop.md` for generation, validation, regeneration, saving, reporting, and the post-iteration skill-learning hook.

## Direct Generation Contract

When the user asks to make actual image deliverables:

- **Create a task folder first** before any generation. Default location: `~/Desktop/`. Folder name format: `YYYYMMDD-HHMM-<产品名或类别>` (e.g., `20260705-1730-英式辅食`). All outputs for this task go ONLY into this folder. Never write into a folder containing previous-task files. See `references/production-loop.md` for full Task Folder Isolation rules.
- Generate each requested deliverable as its own independent model-native image.
- Save head images as `<task-folder>/主图/01-*.png` through `<task-folder>/主图/05-*.png`.
- Save detail pages as `<task-folder>/详情页/01-*.png` through `<task-folder>/详情页/10-*.png`.
- Save contact sheets to `<task-folder>/记录/`, validation report to `<task-folder>/验证报告.md`.
- Use contact sheets only as review artifacts after independent final files exist.
- Do not use deterministic local compositing, local text overlay, local retouching, or local layout repair on final deliverables.
- Validate each file and the full set before reporting completion.

## Non-Negotiable Rules

- Product accuracy outranks reference style.
- **Task folder isolation (hard rule)**: every new task creates a fresh folder at `~/Desktop/YYYYMMDD-HHMM-<产品名或类别>/`. All outputs (主图, 详情页, 记录, 验证报告) live inside this folder. Never write into a folder containing files from a previous task. See `references/production-loop.md`.
- **Copy is consumer-facing, not explanatory (hard rule)**: every line of copy (headline, sub-headline, support copy, label) is written from the consumer's perspective — what they feel, get, or stop worrying about. Never write manufacturer/explanatory/spec-sheet voice ("采用XX技术", "本产品具有XX功能", "符合XX标准", "XXX工艺打造"). See `references/visual-proof-grammar.md` Copy Voice section.
- The visual must prove the message; do not add a model, scene, chart, macro, label, or decorative module unless it helps the viewer understand or believe the core message.
- **Picture Solo Test (hard gate)**: every output must work with all copy covered. Before writing a prompt, write one sentence: "The picture is [concrete scene], and with all text hidden it still shows [message]." If you cannot, the picture is failing its job — redesign it before prompting.
- **Product presence is decided by message, not by default**: the product/packaging does NOT appear in every output. It appears only when the message requires the packaging to be visible. Multi-flavor, multi-ingredient, micro-material, mechanism, sensory, scene-fit, and lifestyle-proof screens usually have NO packaging in the main visual. Use `references/message-picture-patterns.md` to decide.
- **No icons ever**: never include icon-shaped elements that "express a selling point" (checkmarks, gear icons, lightning, shield icons, ingredient bubbles, feature pictograms, decorative arc systems). Icons added later by the user are out of skill scope. A screen is composed of: main visual + main copy + optional short support copy. It is NOT composed of: icons, icon rows, icon grids, icon bubbles, badge ribbons, or pictogram systems.
- **Reference is language, not scene**: inherit light behavior, typography attitude, density rhythm, commercial temperature, and module rhythm from the reference. Do NOT inherit specific scene elements (fabric type, surface texture, location, background pattern). Reference scene elements may appear in at most 30% of outputs across the set; the remaining outputs must use a different main visual.
- **Unified approval gate (hard rule)**: head images and detail pages are planned and reviewed TOGETHER. Output ONE approval table covering all 5 + 10 outputs (with draft consumer-voice copy) before any prompt is written. User approves the whole batch in one pass. Do not generate head images first and detail pages separately without a unified approval.
- **Set-level diversity is mandatory**: 5 head images must use ≥4 distinct main visuals; 10 detail-page screens must use ≥7 distinct main visuals. "Main visual" = scene + main subject + composition family. Same main visual repeated = template failure, regenerate.
- The product image is a source of truth, not a requirement that the whole product must dominate every screen. Some screens may be led by skin, hand interaction, body contact, macro structure, mechanism, result state, scene context, or a partial product crop when that better proves the screen's task.
- References provide visual DNA, layout logic, proof methods, rhythm, typography attitude, and mood; they do not provide copied brands, people, claims, prices, logos, certifications, product-specific actions, OR specific scene/setting elements.
- Detail pages are content-led and sequence-led. A reference may shape style and consistency, but each screen's message decides its composition. Detail pages are NOT vertical extensions of head images; they have their own sequence logic.
- If the user has already defined the detail-page screen directions, preserve those directions and improve the expression inside each screen instead of inventing a new structure.
- Every human-product interaction must be physically and behaviorally plausible for the actual product category. Translate reference action intent instead of copying poses.
- Color is rebuilt around supplied brand colors when present, otherwise around the product identity and category. Do not copy reference dominant colors by default.
- Avoid mechanical repetition. A coherent set should share visual DNA while varying proof method, composition, density, and product-human relationship by role.
- Do not invent prices, official status, certifications, specs, ratings, medical effects, or unsupported performance claims.

## Output Shape

Default deliverable when not directly generating:

1. Input and reference role analysis.
2. Product information route and claim-safety summary.
3. Consumer-angle map and screen-structure capture.
4. Set-level visual DNA and color system.
5. **Unified approval table**: 5 head images + 10 detail-page screens, each with picture solo statement, pattern match, main subject, product exposure, scene setting, and draft consumer-voice copy.
6. Generation prompts for requested outputs.

Default deliverable when directly generating:

1. **Output the unified approval table** (5 head images + 10 detail-page screens with draft copy) and ask for user approval before any image generation. Skip only if the user explicitly says to skip review.
2. Brief planning summary after approval or when review is skipped.
3. Generate and save requested independent final image files into the task folder.
4. Create contact sheets only as secondary review artifacts.
5. Report saved paths and validation/regeneration notes.

## References

Read only the needed reference files:

- `references/input-routing.md`: product facts, documents, completeness routes, and selling-point extraction.
- `references/reference-analysis.md`: image role classification, reference transfer, product-use plausibility, model consistency, claim safety, and the reference-is-language-not-scene rule.
- `references/visual-dna.md`: set-level consistency, reference weighting, per-screen DNA inheritance, and set-level main-visual diversity thresholds.
- `references/color-adaptation.md`: brand/product-first color system and anti-color-copy rules.
- `references/visual-proof-grammar.md`: Picture Solo Test, message-first visual proof, product-presence decision, no-icon rule, consumer expression, and density rhythm.
- `references/message-picture-patterns.md`: high-frequency message-to-picture patterns (multi-flavor, ingredients, sensory, mechanism, scene, trust, etc.) with concrete picture patterns and product-presence rules.
- `references/head-images.md`: 5-head-image structure, 5-image main-visual diversity table, and prompt requirements.
- `references/detail-pages.md`: fixed 10-screen/detail-page expression planning, 10-screen main-visual diversity table, approval gate, and prompt requirements.
- `references/production-loop.md`: autonomous generation, validation, iteration, output hygiene, set-level pre-check, and skill feedback loop.
