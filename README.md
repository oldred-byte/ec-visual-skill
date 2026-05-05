# EC Visual Skill

EC Visual is a Codex skill for creating e-commerce visual systems from product
images and visual references.

It helps an agent analyze references, adapt the visual direction to the actual
product, plan marketplace head images and product detail-page screens, write
generation prompts, validate outputs, regenerate failed images, and save the
final deliverables.

## What It Produces

By default, the skill plans a complete e-commerce visual set:

- 5 square marketplace head images
- 10 vertical product detail-page screens
- Reference analysis
- Product-adapted color system
- One generation prompt per final image
- Validation and regeneration guidance

When the user asks for final image deliverables, the workflow expects each image
to be generated as an independent model-native bitmap, then checked and saved as
a separate file.

## Core Workflow

1. Inspect product images and reference images.
2. Classify what each reference can contribute.
3. Extract the reference flavor: camera attitude, layout rhythm, typography,
   whitespace, commercial genre, and product-human relationship.
4. Rebuild the color and visual system around the real product.
5. Plan 5 head images, each with its own sales role.
6. Plan 10 detail-page screens as a coherent purchase narrative.
7. Write one prompt per image or screen.
8. Generate, validate, diagnose failures, regenerate, and save final files.

## Important Principles

- Product accuracy outranks reference style.
- References are not templates to copy blindly.
- Do not copy reference brands, prices, original text, certifications, people,
  or product-specific claims.
- Do not invent medical effects, official certifications, test results, prices,
  or brand authorization.
- Every visible claim should be supported by the product image or by user-
  supplied product facts.
- Final commercial images should come directly from the image model, not from
  local text overlays or deterministic compositing.

## Repository Structure

```text
.
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── color-adaptation.md
    ├── detail-pages.md
    ├── head-images.md
    ├── production-loop.md
    └── reference-analysis.md
```

## Installation

Copy this folder into your Codex skills directory:

```bash
cp -R ec-visual ~/.agents/skills/ec-visual
```

If you clone this repository directly, you can also symlink it:

```bash
ln -s "$(pwd)" ~/.agents/skills/ec-visual
```

Then restart Codex or reload skills if your environment requires it.

## License

MIT
