# Visual DNA

## Purpose

Use reference images to build a coherent visual system for the full set, not to force every output into the same composition. Each head image or detail screen may solve a different message, but all outputs should feel like the same campaign world.

## Reference Is Language, Not Scene (hard rule)

This is the single most violated rule in practice and the #1 root cause of "5 images look identical" and "detail pages look like vertical head images".

**Reference provides** (inheritable):
- Light behavior (soft daylight, hard studio, glossy reflections, matte diffusion)
- Typography attitude (bold sparse headline, dense labels, technical annotations, premium wordmark)
- Density rhythm (low-copy mood vs. dense proof page)
- Commercial temperature (clean, premium, playful, clinical, warm, technical)
- Module rhythm (how modules are sized, spaced, aligned)
- Color relationship logic (contrast level, warm/cool balance, accent placement) — NOT specific hues

**Reference does NOT provide** (forbidden inheritance):
- Specific scene elements: the specific fabric (picnic cloth), specific surface (grass, marble, sand), specific location (kitchen counter, beach, studio cove), specific background pattern
- Specific decorative props that appear in the reference image
- Brand/product/claim-specific elements

**Scene Cap rule**: Any single reference-scene element (e.g., "picnic cloth background", "marble surface", "concrete floor") may appear in **at most 30%** of outputs in a set. For a 5-image set that's 1 image; for a 10-screen set that's 3 screens. The remaining outputs must use a different main visual.

**Scene Lock rule**: If the user explicitly wants a reference scene applied to all outputs, they must say so explicitly. Otherwise, the default is diversity.

## Why This Rule Matters

When the model reads a reference image with a strong scene (e.g., baby food on a picnic cloth in a park), it tends to use that scene as a default for every output. Result: 5 head images all on picnic cloth + 10 detail pages all on picnic cloth. The set looks "coherent" but actually has zero proof logic — every screen is the same picture with different copy.

The reference's value is its visual language (how light behaves, how type feels, how dense the layout is), not its literal scene. Two different scenes shot with the same light + type + density still feel like the same campaign. Five identical scenes with different copy do not.

## Set-Level Visual DNA Contract

Before planning outputs, extract a compact visual DNA contract from the strongest reference image(s):

- Commercial genre: marketplace conversion, premium poster, lifestyle campaign, technical proof, ingredient/science, editorial fashion, food appetite, etc.
- Color relationship: contrast level, warm/cool balance, accent placement, background/material relationship. Do not treat this as permission to copy hues.
- Typography attitude: bold sparse headline, dense selling labels, technical annotations, premium wordmark behavior, soft lifestyle copy, etc.
- Layout rhythm: large whitespace, centered hero, diagonal division, stacked cards, bottom strip, modular proof grid, product-and-copy balance.
- Light and material: glossy, matte, metallic, soft daylight, hard studio, translucent, wet, clinical, warm premium, technical glow.
- Camera language: macro, flat lay, low angle, close foreground, product hero, portrait scene, documentary scene, controlled product render.
- Graphic devices: icons, labels, arrows, ingredient bubbles, line annotations, numbers, table lines, frames, capsules, proof blocks.
- Emotional temperature: clean, premium, playful, warm, clinical, high-energy, calm, technical, trustworthy.

Then decide:

- Must carry across the set:
- Can vary by screen:
- Must not copy:
- What would make the set feel scattered:

## Reference Weight Routing

Reference weight changes by output role. Do not apply one reference equally to all images.

### Head Images

- H01: highest reference weight when the reference is clearly a first marketplace head image. Follow its layout skeleton and scan path while replacing product, copy, color, claims, and brand elements.
- H01 with poster/mood reference only: medium-high flavor weight. Use default marketplace click logic but bend camera, mood, typography restraint, and human-product relationship toward the reference.
- H02-H04: medium reference weight. The selling point and proof method decide the composition; carry 2-3 DNA elements such as type style, light, color relationship, module rhythm, or camera attitude.
- H05: medium reference weight. Persona or audience logic decides content; carry emotional temperature, typography attitude, and color system.

### Detail Pages

Detail pages are content-led. The screen's message and proof grammar decide the composition first; reference DNA keeps the set unified second.

- D01 hero: medium-high reference weight for campaign feel, product memory, typography, and light.
- D02 pain/scene and D06 usage scene: medium reference weight for mood, color relationship, typography, and scene treatment; real use logic overrides reference pose.
- D03-D05 selling points: medium-low reference weight for style; proof method overrides reference layout.
- D07 practical benefit and D08 detail/parameter: low-medium reference weight; clarity, scale, structure, and readability matter first.
- D09 trust and D10 closing: medium reference weight for brand memory, trust tone, product set display, and final rhythm.

For every planned output, state which 2-4 DNA elements it carries. If a screen carries no shared DNA, it will likely feel disconnected. If every screen carries the same composition or module, it will likely feel repetitive.

## Consistency Without Sameness

A coherent set should share:

- Product/brand color system.
- Typography attitude and hierarchy logic.
- Light/material world.
- Similar commercial temperature.
- A small set of recurring graphic devices.

A coherent set should vary:

- Proof method.
- Composition family.
- Camera distance.
- Whether people appear.
- Information density.
- Product scale and crop.
- Scene versus macro versus mechanism versus parameter treatment.

## Reference Feature Distribution

Before using a prominent reference feature, answer:

- What function does it serve: click, proof, trust, premium mood, usability, appetite, softness, technical credibility?
- Which output actually needs that function?
- Does the target product/category support it?
- Does the color need to be rebuilt around product or supplied brand colors?
- Would repeating it across multiple outputs create visual fatigue?

Use strong reference features selectively. A feature can define the set without appearing in every image.

## Set-Level Main-Visual Diversity Thresholds (hard gate)

In addition to the DNA contract, sets must satisfy main-visual diversity:

- **5 head images**: ≥4 distinct main visuals.
- **10 detail-page screens**: ≥7 distinct main visuals.

"Main visual" = scene + main subject + composition family. Two outputs sharing all three = same main visual. Two outputs sharing one or two dimensions = related but distinct.

Examples:

- ✅ Distinct 5-image set: H01 packaging hero on neutral / H02 three-ingredient bowls flat-lay / H03 macro of pouch tip / H04 hand opening pouch / H05 baby being fed scene. Five different main visuals — passes.
- ❌ Failing 5-image set: H01 pouch centered on picnic cloth / H02 pouch centered on picnic cloth with "natural" headline / H03 pouch centered on picnic cloth with "soft" headline / H04 pouch centered on picnic cloth with "flavors" headline / H05 pouch centered on picnic cloth with persona labels. Same scene + same subject + same composition = 1 main visual across 5 images. Fails.

When the planned set fails the threshold, regenerate the plan (not just the prompts). Pick a different message-to-picture pattern from `message-picture-patterns.md` for the duplicated outputs.

## Pre-Generation Diversity Board

Before writing any prompt, output a diversity board in table form:

| Output | Message | Pattern (from library) | Main visual (one-line scene) | Scene setting | Main subject | Composition family | Product presence |
|---|---|---|---|---|---|---|---|

Check the rightmost three columns (scene setting, main subject, composition family) across rows. If more than the allowed overlap share the same combination, regenerate rows that duplicate. Only after the diversity board passes may prompts be written.

This board is the operational enforcer of the diversity thresholds. Without it, the thresholds are abstract.
