# Reference Analysis

## Classify Every Input Image

For each image, identify its role. One image may have multiple roles, but state the primary role.

- Product image: source of product appearance, color, material, packaging, proportions, structure, visible real packaging text.
- First head-image reference: a marketplace main image with product, large headline, selling labels, spec/promo blocks, and square composition.
- Head-image set reference: multiple square marketplace images that show main image + selling-point images + user/persona image logic.
- Detail-page reference: vertical screens with sequential explanation, proof, scenes, parameters, or conversion flow.
- Poster/mood reference: a visual ad, poster, or mood image whose value is composition, lighting, typography, or creative approach, not literal e-commerce layout.
- Color/mood reference: useful for atmosphere and color relationship only, never a reason to copy dominant colors blindly.

## Poster Reference Handling

A poster reference is not automatically a first head-image reference. Treat it as a poster/mood reference when it is vertical, campaign-like, person-led, brand-led, or lacks marketplace main-image mechanics such as square composition, product selling labels, spec strips, price/promo blocks, and head-image scan order.

Poster references may transfer:

- Hero scale, low/high angle, product-in-hand drama, model emotion, clean whitespace, typography attitude, visual metaphor, lighting.
- The reference's flavor contract: what kind of brand world it creates and how the product feels in the viewer's body.

Poster references may not override:

- The first head-image marketplace skeleton when no clear first head-image reference exists.
- Brand/product-adapted color rules.
- Claim safety and user-provided facts.
- Product-use plausibility. If the reference product is held or used in a way that does not fit the target product category, translate the intent, not the pose.

If the input contains product image + poster reference only, state: "No clear first head-image reference exists; use default first-head-image skeleton while borrowing poster mood/creative methods."

Do not let that sentence become a generic-template excuse. "Borrowing poster mood" must be concrete: preserve at least 3-5 flavor dimensions from the reference.

## Flavor Contract

Before planning images, write a short flavor contract for the strongest reference image. For set-wide consistency and per-screen reference weight, also use `visual-dna.md`.

Analyze these dimensions:

- Commercial genre: marketplace conversion, premium poster, lifestyle campaign, technical proof, ingredient/science, editorial fashion, etc.
- Camera attitude: low angle, close foreground object, heroic scale, flat product catalog, macro, documentary scene, etc.
- Human-product relationship: hand-held dominance, person behind product, product as accessory, product in use, product as object only.
- Spatial tension: large whitespace, extreme crop, crowded modules, floating object, foreground/background depth.
- Typography behavior: oversized brand type, sparse headline, dense selling tags, poster-style bottom wordmark, small technical labels.
- Emotional temperature: clean, confident, playful, clinical, warm, high-energy, calm, premium, cheap-promotional.
- Material/light: glossy, matte, metallic, soft daylight, hard studio, translucent, wet, rain, etc.
- Information density: restrained poster, strong e-commerce, dense proof page, low-copy mood image.

Then decide:

- Must preserve (light/type/density/mood — language only):
- Can adapt:
- Must NOT preserve (specific scene elements — see Reference Is Language Not Scene):
- What would make the output lose the flavor:

## Reference Is Language, Not Scene (critical rule — see visual-dna.md for full text)

The flavor contract captures the reference's visual **language**. It does NOT capture the reference's **scene**. These are separate dimensions:

- **Language** (inheritable): light behavior, typography attitude, density rhythm, commercial temperature, module rhythm, color relationship logic.
- **Scene** (NOT inheritable by default): specific fabric, specific surface, specific location, specific background pattern, specific decorative props.

When writing the flavor contract, explicitly list the reference's scene elements separately and mark them as "may appear in at most 30% of outputs". This prevents the model from defaulting to "use the reference's scene everywhere".

Example for a baby-food reference image showing a picnic-cloth-on-grass scene with bold sans-serif Chinese headline and soft daylight:

- Must preserve (language): soft daylight, bold sans-serif headline attitude, generous whitespace, calm warm commercial temperature.
- Can adapt: product category, copy, color (rebuilt around product/brand).
- Must NOT preserve (scene): picnic cloth, grass surface, park setting, decorative botanical props. These may appear in at most 30% of outputs (e.g., 1 of 5 head images, or 3 of 10 detail screens).
- Flavor loss risk: copying the picnic-cloth scene across all outputs. Two screens with the same light and type but different scenes still feel like the same campaign; ten screens with the same picnic cloth and different copy do not.

## Product-Use Plausibility Map

Before turning a reference into prompts, write a short product-use plausibility map.

Analyze:

- How a real person normally holds, wears, carries, opens, applies, stores, or operates this product.
- Which product parts must stay in anatomically correct positions relative to the hand, face, body, ground, or environment.
- Which reference gestures are literal-transfer safe.
- Which reference gestures must be translated into a product-appropriate equivalent.
- What visual result would immediately feel fake, awkward, unsafe, or like "no real person would do this".

Reference action is not a pose template. First identify the action's intent, then translate it through the target product's real use logic:

| Reference action | Intended effect | Target-product equivalent | Forbidden transfer |
|---|---|---|---|
| What the reference person/object does | hero scale, intimacy, ease, confidence, proof, scene realism | how the target product can express the same effect naturally | copied pose or grip that would make the product look awkward, unsafe, or fake |

Examples:

- A toothbrush or hair dryer can be pushed toward camera in one hand because that is a plausible product-in-hand hero pose.
- An umbrella should usually be held by the handle or shaft, with the canopy above, beside, or behind the person. A low-angle hero can use canopy scale, diagonal shaft, handle close-up, or over-shoulder carrying, but should not make the person thrust an open umbrella horizontally into the camera like a small handheld gadget.
- A skincare bottle can be held near the face, but a heavy appliance may need countertop support or a natural grip.

If the desired reference flavor conflicts with realistic product use, preserve the emotion, camera attitude, whitespace, and typography first, then redesign the human-product pose.

Do not add a person by default. Use a person only when the screen's core message needs use, fit, scale, emotion, audience identification, comfort, taste acceptance, or scene credibility. If the best proof is macro material, parameter clarity, product structure, ingredient logic, or product set display, keep the image product-led.

## Transfer Permissions

Product image permits:

- Product appearance, package shape, colors, material, proportions, structural details, visible real labels.

Product image does not permit unless requested:

- Original background, original lighting, original layout, original text placement.

Reference images permit:

- Layout skeleton, information hierarchy, reading order, content combination logic, creative methods, module rhythm, typography style, proof method.
- Visual language: light behavior, type attitude, density rhythm, commercial temperature.

Reference images do NOT permit by default:

- Brand/logo, original copy, price, certification names, people (unless chosen as model source), category-specific claims, dominant color if it does not fit the product.
- **Specific scene elements** (fabric, surface, location, background pattern, decorative props) — these are subject to the Scene Cap rule: at most 30% of outputs in a set may use any one reference-scene element. The rest must use a different scene.

Reference people may be used only when the user chooses the reference-image model as the model source or explicitly asks to keep that model identity.

## Model Source And Consistency

When any planned output contains a person, define a model source before prompts:

- Reference-image model: use only when the user asks to use the reference model, or when the reference model is clearly intended as the campaign model.
- Product-image model: use when the product image already shows a wearer/model and the user wants that person carried through.
- Generated model: use when no model source is specified and the product is not clothing/apparel/wearable fashion, or when the user chooses a new campaign model.

For clothing, apparel, wearable fashion, or any product where the model materially affects fit, style, or conversion, ask before planning or generation unless the user has already specified the source: "人物用参考图模特、产品图模特，还是重新生成模特？"

After the model source is chosen, write a model-consistency lock: apparent age range, gender presentation when relevant, face shape, hair length/color/style, skin tone, body type, expression range, styling attitude, and any visible distinctive features. Use that same lock in every prompt where the recurring model appears. This lock preserves identity, not pose: choose the pose, gesture, crop, camera angle, expression intensity, and product interaction independently for each image based on its selling point and scene. Do not accidentally switch age, face, hairstyle, body proportions, or styling world across the 5 head images and 10 detail-page screens.

If an image needs multiple people or audience personas, decide whether they are supporting extras or separate personas. Supporting extras must not replace the locked main model. Separate personas are allowed only when the screen's role requires different audience groups.

## Claim Safety From Visual Evidence

Classify each proposed selling point as:

- Visible: directly supported by the product image, such as color, pattern, shape, handle type, compact body, visible case, visible canopy.
- Category-generic: common use of the product category, phrased softly, such as umbrella for rainy commutes or daily carry.
- User-provided: facts supplied by the user, such as UPF rating, windproof ribs, coating, automatic open, weight, size, certification.
- Unsupported: specific performance, technical rating, certification, medical/health result, official claim, or price not provided.

Use visible, category-generic, and user-provided points. Do not use unsupported points.

For umbrellas, "sun-rain dual use", "UV protection", "sunshade", "UPF", "stormproof", "windproof", "water-repellent coating", "automatic open/close", weight, size, or rib count are unsupported unless visible or supplied. Prefer safer wording like "rainy-day commute", "daily carry", "outdoor backup", and "easy to keep in a bag".

## First Head-Image Reference Rule

If a reference is clearly a first marketplace head image, the generated first head image must strongly follow its layout skeleton and information format.

Must follow structurally:

- Top brand/store strip position and relationship if present.
- Main headline position, scale, line count, and reading order.
- Product position, product scale, and product/background relationship.
- Selling-point capsules or labels: count, stacking direction, and placement style.
- Bottom spec strip, benefit bar, promo block, or price-area skeleton.
- Decorative frame, rounded rectangle, platform, badges, or corner blocks as layout functions.
- Overall density, commercial rhythm, and scan path.

Must replace:

- Product, copy, specs, tags, price, brand area, badges, color system.

Never copy:

- Original brand, original price, original certifications, original logo, original people, original product category claims, or incompatible dominant color.

## When No First Head-Image Reference Exists

Use the default first-head-image skeleton in `head-images.md`. This skeleton is a high-conversion marketplace layout: top label strip, large left headline, 2-3 selling capsules, large right product, small feature badges, bottom spec strip, bottom benefit slogan, and optional no-price promo label.

## Reference Feature Distribution

Before using any prominent reference feature, answer:

- What sales/design function does it serve?
- Which image or screen needs that function?
- Does the product/category support it?
- Does its color need to be rebuilt?

Do not repeat the same prominent feature across all outputs by default.

For full-set consistency, distribute reference features through `visual-dna.md`: each output should carry selected DNA elements without mechanically repeating the same composition, card, badge, action, or module.

## Taste Gap Audit

After a first generation pass, compare outputs to the reference on the flavor contract, not only on layout and colors.

Ask:

- Did we preserve the same commercial genre, or did we accidentally turn a premium poster into a generic marketplace template?
- Did the camera attitude survive?
- Did the product-human relationship survive when it was important?
- Is the product-human interaction believable for this exact product category, or did we copy a pose from the reference that only made sense for the reference product?
- Did information density drift too high or too low?
- Did safety rules remove claims but also flatten the visual idea?
- Are we using scene clichés instead of the reference's creative method?
- **Did we accidentally copy the reference's specific scene elements (fabric, surface, location) across most/all outputs?** If yes, this is the #1 root-cause failure mode. Re-plan with the Scene Cap rule.
- **Did the 5 head images / 10 detail screens actually achieve main-visual diversity, or do they all look like the same picture with different copy?** Check the diversity board against the threshold.
- **Did each screen pass the Picture Solo Test, or does the headline do the work the picture should be doing?**
- **Did any icons/pictograms slip in?** If yes, regenerate without them.

If the answer is no, patch prompts or skill rules before continuing.
