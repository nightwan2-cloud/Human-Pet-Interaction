---
name: north-american-rug-human-pet-scenes
description: Create realistic North American home scenes centered on a strong, believable interaction between a person and a pet, using a supplied rug image and declared rug style. Produces a copy-ready image prompt, and generates the scene image when requested.
---

# North American Rug Human-Pet Scenes

Create a believable, inviting North American residential moment in which a person and a pet share a clear, lively interaction. Build the prompt around the sequence **life context → human-pet relationship → reciprocal event → space and contact → camera → light and color → material realism**. The image should feel like a lived moment, not a staged showroom or a generic lifestyle ad.

There are two output modes:

- **Prompt mode:** return one integrated, directly usable image-generation prompt.
- **Image mode:** when the user asks to generate the scene image, compose the prompt and use the built-in image-generation tool. Follow the available `imagegen` skill. Treat the uploaded rug as a style reference, not an edit target.

## Inputs and defaults

Use the user's supplied details as authoritative. Typical inputs are:

- Rug image and declared rug style.
- Season; room such as living room, bedroom, or dining area.
- Person identity, age, gender, and count/relationship (for example one woman or a couple).
- Pet type and traits, if specified.
- Activity, aspect ratio, desired rug prominence, and whether to return a prompt or an image.

Ask one concise question only when a missing detail materially blocks a coherent or identity-sensitive result. Do not silently override explicit instructions. If the user delegates a choice, choose a plausible option and proceed. If the user has already established person, season, or composition in the conversation, reuse it rather than asking again.

If the rug style is not named but an image is supplied, infer a concise style label from its visual language and state it briefly before the prompt only if helpful. If the user has named the style, that label is authoritative; use visible image traits as secondary cues. Do not output a separate rug analysis or reasoning section.

## Human character and clothing

For the person's North American appearance, natural facial realism, and outfit, read [references/character-and-clothing.md](references/character-and-clothing.md). This bundled reference carries the relevant character-skill guidance, so no separately installed character or wardrobe skill is required. Apply it together with the scene-specific rules below:

Every final prompt must include the following fixed person-control description, with only the bracketed identity fields filled for the requested person. Keep it with the outfit and human-pet interaction in the same grouped passage. Translate it faithfully if the prompt language is not Chinese; do not drop the skin, proportion, pose, or photographic-realism constraints for brevity:

> 一位[年龄段][性别]的北美[人种/族裔]人物，面部比例自然，保留轻微真实的不对称感，五官结构与身体比例符合真实人体。呈现自然的肤色细微变化、克制可见的皮肤纹理与柔和细小的面部绒毛，皮肤反光自然柔和，不油腻、不泛亮。表情和姿态松弛可信，不过度美颜、磨皮或塑造网红式比例。以真实生活方式摄影呈现，人物处于自然观看距离，采用环境中景或三分之四身构图，画面清晰干净，不过度锐化，不出现塑料皮肤、粗糙噪点或夸张微纹理。

- Create the requested person or people as part of the human-pet scene, not as an isolated portrait.
- Do not add close-up eye-detail instructions, oily/plastic skin, excessive retouching, artificial symmetry, gritty over-texturing, or image noise.
- Keep skin marks restrained and believable. A few faint, naturally scattered freckles or small marks may be used when they suit the person, but do not make them dense, high-contrast, or spread across the face, arms, hands, and body. Do not invent conspicuous spots by default. Show realism mainly through gentle tonal variation and subtle skin texture; hands should retain ordinary skin detail without stippled-looking dots.
- Apply the bundled face-realism rules: natural facial proportions and mild asymmetry, anatomically continuous features, subtle pores and fine vellus hair, and soft controlled reflectance. Skin should look comfortably natural and hydrated, never greasy, slick, wet, shiny, or over-detailed. Do not turn pores, freckles, or skin texture into visible noise or dense speckling.
- Make clothing believable for the season, room temperature, and activity. Apply the bundled outfit workflow: original garment combinations, rug-related analogous or restrained complementary colors rather than exact rug-color matches, and newly designed related patterns. “Not overly casual” means polished everyday dressing unless the user explicitly requests business or occasionwear; do not reduce it to suits, dress shoes, or evening dresses. Check recent outfits for repetition rather than forcing one silhouette.
- Do not add indoor bags or bag accessories.
- The rug reference is **not** an instruction to reproduce its exact rug. Ignore any conflicting rug-copy requirement from other contexts; this skill's rug rule below takes precedence.

For a group, establish each person's requested identity and relationship distinctly. Avoid turning ethnicity into a fixed facial or styling stereotype. Do not introduce children unless requested.

## Rug: style cue, not a reproduction target

Use the supplied rug to understand both the declared style and its **broad color palette**. Keep the scene rug in a compatible overall tonal family and preserve the reference's dominant-to-secondary color balance where practical; color harmony is required even though exact product replication is not. Mention the rug concisely, for example, “a softly distressed Persian-inspired rug in muted blue, ivory, and sand tones.” Do **not** instruct the image model to recreate the reference rug or preserve its exact motif, border, layout, dimensions, or color placement. Do not describe it as “the same rug as image 1.”

The rug may be a visible design anchor when the user wants a rug-focused commercial composition. Otherwise, give it a natural role in the home scene; do not force it to dominate every human-pet lifestyle image. Keep its appearance simple in the prompt so the model can create a style-compatible rug freely.

## Scene zone and rug placement

Use the following mapping internally to establish the requested scene's actual activity zone, rug type, placement, and orientation before choosing furniture or interaction. These are spatial planning rules, not a fixed paragraph to paste into the final prompt.

| Requested scene | Rug type and placement | Scene anchor |
| --- | --- | --- |
| Kitchen | A runner laid lengthwise in the aisle beside the kitchen island, between the island and the opposing cabinets/counter. | Place the human-pet interaction in this island aisle, not in a breakfast nook or dining area. |
| Living room | An area rug in front of the sofa. | Build the interaction around the sofa and its front rug zone. |
| Bedroom | An area rug laid crosswise beneath the foot end of the bed, extending into the open floor beyond it. | Anchor the scene to the bed's foot-end zone, not a bedside runner. |
| Single-chair setting | An area rug. | Build the interaction around one chair and its surrounding rug zone; do not turn it into a sofa-group scene. |
| Hallway | A runner laid lengthwise along the hallway passage. | Place the interaction within the hallway circulation zone. |
| Dining room | An area rug beneath the dining table. | Anchor the interaction to the table-and-chair zone, with credible legroom and contact. |

Apply this mapping unless the user explicitly specifies a different placement. The requested scene determines rug format and orientation even when the uploaded reference has a different aspect ratio or another skill suggests preserving its orientation; continue using the reference only for style and broad palette. Adapt the action, furniture spacing, and camera to the mapped zone, preserving plausible circulation and readable contact. Supporting branded furniture must fit this zone rather than shifting the scene into another room or adding furniture just to fill a quota. Keep the final prompt concise: naturally express only the spatial facts needed to render the scene correctly, without exposing the mapping, its rationale, or a verbatim checklist.

## Residential style and furniture

Select one coherent residential interior direction based on the declared rug style and room. Do not combine several competing styles in one scene. Use these mappings as starting points, not rigid taxonomies:

| Rug visual language | Suitable interior directions |
| --- | --- |
| Animal, biomorphic, or nature-inspired | Refined eclectic minimal, contemporary American estate, modern coastal/Hamptons, or polished tropical casual |
| Persian or bohemian | American vintage/country or relaxed modern country |
| Abstract texture | Organic modern, modern California casual, or modern transitional |
| Geometric | Modern graphic, soft modern/cream minimal, or curved modern |
| Botanical or floral | Lush modern bohemian, vintage country, or refined tropical casual |

When image cues and the user's style label differ, retain the user's label and choose the closest coherent interior direction without overclaiming authenticity. If later-supplied furniture rules or room references apply, prioritize those rules.

Describe only the furniture and accessories needed to make the selected room, action, and composition credible. Keep the set intentional and moderate rather than generating an exhaustive shopping list. Include a few lived-in details that support the activity (for example a casually placed book near a reading chair), not decorative clutter or unrelated props.

Keep furniture-and-decor copy concise and visual rather than exhaustive. In one compact paragraph, first describe the rug's style and dominant-to-secondary palette; then name **two or three recognizable, design-led furniture pieces** with accurate brand/model names, colors, and primary materials; finish with **three or four distinctive supporting accessories**, separate from the furniture count. Use the compact format: brand/model + furniture type + color + primary material, with one identifying silhouette or tactile cue only when useful. Supporting accessories should have a clear design/material identity but need not all be branded. Do not itemize construction details, surface microtexture, styling rationale, and palette logic for every object. Preserve the rug's broad palette relationship, avoid generic unnamed furniture, and do not overfill the room with accessories or brand names. Do not embed specific furniture models, example descriptions, or recurring furniture sets in this skill as defaults.

### Supporting accessories and related patterns

For every rug style and room, select three or four supporting accessories appropriate to the visible space and activity. Derive their palette from the rug and create related patterns using its motif language, shapes, line rhythm, or ornamental character. Explicitly describe the related pattern on pattern-bearing accessories, including cushions and artwork when selected; changing only their colors is insufficient. Reinterpret rather than duplicate the rug's exact design, varying pattern scale and density to avoid a matching-set effect or competing visual clutter. Simple sculptural or botanical accessories may relate through color and form without an added surface pattern. Describe each accessory in one short phrase combining item, rug-derived color, material where useful, and its relevant pattern or shape. Keep all accessories in the furnishings paragraph, with no separate design rationale or fixed accessory set. Preserve circulation, interaction visibility, and the requested rug coverage.

### Rug-specific furniture selection and variety

Apply this process to every rug style and room, not only modern or geometric rugs. Plan internally from the individual rug's visible traits, rather than mapping a broad style label directly to a familiar furniture set:

1. Assess dominant and secondary colors, contrast, motif scale and density, line direction, angular or curved forms, visual weight, texture, and ornamental character. Respect the declared style while distinguishing this rug from others in the same family.
2. Select one compatible residential direction and establish furniture proportions, silhouettes, structural character, and material relationships that suit those traits, the room's activity zone, the interaction, and rug visibility. Furniture may echo or balance the rug; do not turn any trait into a fixed furniture recipe.
3. Select accurate brand/model identities that fit those design decisions, then choose coherent finishes and upholstery. Familiarity with a brand is not a selection reason. Verify uncertain model attribution or choose a reliably identified alternative. Keep this planning out of the final prompt.
4. Compare with the latest three available same-room schemes in the current conversation, across all rug styles, including earlier outputs in the current batch. By default, avoid repeating their primary furniture model and never consecutively reuse the same primary/secondary furniture pairing. Recoloring a model, changing only brand names, or selecting near-identical silhouettes and materials does not constitute meaningful variety.
5. For different rugs in a same-room batch, make each furniture scheme differ from the others in at least two dimensions: primary furniture silhouette/volume, secondary furniture shape/structure, and principal material pairing. Tie the differences to the rugs and retain stylistic coherence rather than choosing arbitrary novelty. Adapt distinctive accessories to the new scheme without accumulating extra objects.

Explicit furniture requests and intentional same-home series continuity override rotation. If the constraints leave no coherent alternative, prioritize suitability and briefly disclose any necessary repetition outside the copy-ready prompt. Use only accessible conversation history; do not claim cross-conversation deduplication or invent previous selections. When history is unavailable, derive a fresh scheme from the rug without claiming it is unique. Keep these checks internal unless the user asks for a comparison.

### Upholstery material specificity

- Avoid vague phrases such as “textured upholstery” when a particular tactile result matters; a brand/model name does not determine its fabric.
- When velvet is requested or clearly intended, say “velvet” and add only a compact cue such as “short, dense pile with a soft directional nap.” Do not bury the material under lengthy technical texture descriptions or mix it with contradictory coarse-weave/bouclé cues. Do not make velvet the default when another fabric is requested.
- Keep the fabric's surface visible under the selected light; protect pale and plush upholstery from blown highlights that flatten its texture.

Make the chosen interior direction legible in the architecture and furniture silhouettes, not just by naming it. For Persian/bohemian rugs, a refined American vintage or relaxed modern-country room can use collected but edited pieces, graceful traditional outlines, warm wood, and restrained vintage detail. Avoid drifting into a heavy rustic lodge/cabin look unless specifically requested. Keep the number of furnishings moderate, but provide enough coherent, specific pieces for the selected style and rug palette to read clearly.

The house must feel like a plausible North American home, with believable room proportions and useful circulation. Avoid empty model homes, furniture showrooms, white-background product staging, hotel lobbies, excessive luxury, or a rigid “catalog set” arrangement. Use brand/model names to identify the selected furniture accurately, not as prestige claims or substitutes for its visible design.

## Pet choice and strong reciprocal interaction

- When composing the interaction, first consult [references/interaction-action-index.md](references/interaction-action-index.md) to match the user's posture and activity. Read its linked source-image records for the selected action; use [references/pet-type-library.md](references/pet-type-library.md) when choosing or describing a pet. These bundled references are part of this skill and require no access to the original PDF or image folder. Source IDs and classifications are internal retrieval aids, not final-prompt text.
- If the user specifies sitting on a sofa, choose an action that keeps the person seated there; likewise preserve specified standing, kneeling, floor sitting, feeding, playing, grooming, room, and pet count. When an exact combination is absent, adapt a nearby action relationship while keeping the user's constraints and plausible body support. Choose one primary reciprocal event; for multiple pets give each a distinct spatial role and response.
- Treat the library as observed moments, not ready-made prompts. Extract how the person moves or touches, how the pet responds, where weight rests, and which expressions are visibly supported. Adapt the moment to the requested adult/child composition, pet size/species, and scene. Do not import the source photo's ethnicity, clothing, furniture design, decor, light, text, or camera framing. Do not present an obscured pet face, a waiting posture, or an open mouth alone as proof of happiness; compose the requested happy, relaxed result using coherent species-appropriate face and body cues.
- For consecutive outputs, vary the action family and, when the user leaves pet choice open, the pet's appearance/type as the scene permits. Do not favor a repeated golden retriever or generic cat merely because those appeared in earlier examples. Near-duplicate reference frames count as one action, not extra preference weight. A breed-like label in the library describes appearance, not pedigree or a fixed personality.
- If the user specifies a pet, follow that choice and any stated breed/type, size, age, coat, or behavior. Do not substitute another animal.
- If the user does not specify a pet, choose a plausible household pet that fits the requested activity, household, and overall visual direction. Rug style may inform the setting and mood, but must not be treated as evidence that a particular animal belongs to the user.
- Describe recognizable species, plausible adult/young size as appropriate, coat/color, and visible posture. Keep anatomy and scale realistic. Do not anthropomorphize the animal or add pet products as decor; include a collar or toy only if it makes sense for the requested event.
- Describe the pet's coat with a small number of species-appropriate cues: coat length and layering (such as soft undercoat beneath guard hairs for a double-coated dog), natural hair direction and clumping, subtle tonal variation between areas, and believable light catching the outer strands. Show compression or parting where the body touches a person's hand, lap, cushion, or floor. Keep fur integrated with the animal's form; avoid synthetic plush texture, individually spiky hairs, noisy outlines, or excessive micro-detail. Use only the details that fit the named species and coat.
- Default to **strong, readable interaction**. Build one specific reciprocal event: say what the person does, what the pet does in response, and how their expressions/postures show familiarity. Favor natural close contact such as an embrace, pet leaning into a hand, a dog placing its muzzle near the person's shoulder, or a cat pressing against a seated person. Choose an action appropriate to the species, size, age, and setting.
- Describe **both expressions explicitly** as part of the same moment. Capture the pet in a happy, relaxed instant of enjoying the person's company, using affectionate delight or comfortable contentment plus two or three compatible, species-appropriate facial and body cues. Do not use “attentive,” “waiting,” “looking up,” focused staring, or food anticipation as the pet's emotional description. For dogs, use a soft relaxed face, natural ear position, and a loose body comfortably leaning into the person's touch; when the action permits, show a gently open mouth and a slightly visible tongue. For cats, use a contented expression, relaxed ears/body, and affectionate cheek rubbing or leaning into a hand; an upright gently curved tail may complement a standing pose. Pair this with the person's warm smile or spontaneous affectionate laughter. Keep the expression natural to the species, without human-like grins or exaggerated teeth.
- For feeding scenes, capture a happy, relaxed moment within the feeding interaction, preferably immediately after a small treat as the pet enjoys affectionate touch and the person still holds the remaining treats. If the user specifies active eating, convey relaxed enjoyment with a physically appropriate mouth state; do not demand chewing and an open-mouth smile at once. For several pets, give each a distinct happy, relaxed response. Keep bodies and any tail gesture crisp without motion blur.
- Make the pet's happy expression readable in the requested room/rug composition: keep its face large enough to interpret, mouth and ears unobstructed by hands or furniture, and a natural front or three-quarter face visible during contact. Preserve the user's camera angle and rug coverage without using an upward stare as the emotional cue or adding a facial close-up.
- State the actual contact points and spatial relationship (hand on shoulder/neck/back, pet against lap/leg, paws on floor/cushion, etc.). Keep the action physically safe and anatomically plausible. Avoid a merely decorative pet nearby when the user asked for interaction.
- Preserve a clear instantaneous action with crisp bodies, faces, paws, and contact points. Do not rely on motion blur, smeared trails, or a blurred tail to imply life. Life comes from gaze direction, weight shift, touch, posture, and the pet's response.

## Seven-layer scene construction

Use these layers as prompt-planning questions. Do not expose the checklist or analysis in the final prompt.

1. **Life context — Why is this happening now?** Establish a simple daily situation and a believable reason for any visible object.
2. **Human-pet relationship — How familiar are they?** Show trust through proximity, relaxed posture, and reciprocal attention rather than generic words such as “warm” or “happy.”
3. **Reciprocal event — What does each do?** Specify one primary action by the person and the pet's visible response.
4. **Space and contact — Where are they and what supports them?** State body placement, pet position, contact points, weight support, floor/furniture contact, and enough room layout to prevent floating, intersections, or excess limbs.
5. **Camera — How can the relationship and room be read?** Prefer a natural environmental medium or medium-wide view at a plausible human viewpoint. Keep the people, pet, contact, and relevant room/rug visible, and preserve enough depth of field for background furniture and room details to remain clearly recognizable. Favor moderate-to-deep depth of field and balanced environmental sharpness; avoid portrait-mode separation, very shallow focus, heavy background blur, and conspicuous bokeh. Keep the interaction sharp without making the background look smeared. Do not force a face close-up or dramatic wide-angle distortion. Adjust framing to the user's requested aspect ratio and focal priority.
6. **Light and color — Why does the room feel comfortable?** Vary the lighting presentation to suit the room, time of day, season, and mood rather than repeating one fixed setup. Choose a plausible soft source such as diffused side-window light, bright overcast daylight, gentle morning or late-afternoon ambient light, or a subtle mix of window light and warm practical lamps. Weave its direction and color temperature into the scene. Keep exposure balanced, highlights controlled, shadows soft with visible detail, and faces, furniture, and textiles readable. Avoid blown highlights, hard sunlight, pronounced light-dark patches, high-contrast chiaroscuro, strong dappled shadows, glowing haze, harsh studio light, and flat generic commercial lighting.
7. **Material realism — What proves this is a lived-in photograph?** Use restrained, visible evidence such as natural skin and layered fur, fabric folds/compression, rug pile or weave, furniture grain, floor contact shadows, and believable room reflections. Prefer concrete material cues over extra filters or artificial effects.

## Prompt and image generation

Return one concise, copy-ready prompt per requested scene, not separate analysis, rationale, style assessment, or revision notes. Unless the user requests another language, write the prompt in **English** so furniture descriptions and image instructions are consistently usable. Begin every final prompt with this exact scene-positioning prefix, then continue with the scene-specific context: “An independent-brand lifestyle editorial photograph set in a distinctive North American home—candid, personal, and art-directed, with authentic lived-in details and a natural human–pet connection.” Present the full prompt as continuous scene prose divided into short, unlabelled paragraphs—no headings, numbered modules, or field names inside the prompt. Follow this paragraph sequence, adapting or combining paragraphs only when the scene genuinely needs it:

1. **Scene aim and context:** after the fixed positioning prefix, use one sentence establishing the original North American home-scene intent, room, season, and lived moment.
2. **Person:** identity, age if given, appearance, complete outfit, and the full fixed person-control description. Fill its identity fields and preserve its realism controls; do not shorten it away.
3. **Pet and interaction:** pet species/type and visible traits, a happy and relaxed instant of enjoying the interaction expressed through two or three compatible facial/body cues, the person's reciprocal response and expression, the specific action/contact points/body support, and a few useful coat/fur cues. Keep the pet's face readable and its emotion consistent with the action. Keep the human-and-pet relationship together as one readable event.
4. **Room and furnishings:** rug described briefly using its style and broad reference palette without copying its exact design, followed by two or three recognizable furniture pieces and three or four supporting accessories in concise English noun phrases. Give accessories rug-derived colors and related patterns where applicable, incorporating a small lived-in detail without expanding the decor count.
5. **Camera and composition:** requested angle, framing, focal distance/perspective, visibility of the interaction, room, and rug; use moderate-to-deep depth of field so background furnishings and architectural details stay legible, avoiding strong bokeh or portrait-style background separation.
6. **Light and color:** credible source and direction, atmosphere and shadow quality, tonal relationship among rug, furnishings, clothing, and pet.
7. **Fixed closing paragraph:** always end English prompts with the exact paragraph below, unchanged and without any text after it: “Clearly capture ongoing interactions, showcasing the natural layering of pet fur, realistic skin texture, fabric weaves, and soft shadows. The overall image must be clean, smooth, and cohesive, emphasizing storytelling through large color blocks and distinct silhouettes. Avoid fine noise, high-frequency textures, or gritty artifacts; ensure edges are crisp and clean, surfaces are pristine, and the composition feels open and airy.” Include any essential scene-specific material cues earlier in the appropriate paragraph; do not append another material or negative-prompt section after this fixed closing. Translate this closing faithfully only if the user explicitly requests another output language.

Use the seven-paragraph organization above without copying subjects, actions, colors, or furnishings from previous outputs. Keep the entire copy-ready prompt in one plain-text code block. Unless the user explicitly requests another language, keep it entirely in English, including the full person-control description and fixed closing paragraph.

### Concise final-prompt writing

Preserve the fixed opening prefix, complete person-control description, fixed closing paragraph, and seven-paragraph sequence. Shorten only variable wording; do not remove user requirements or compress away required furniture, accessories, expressions, contact, fur, rug placement, or background clarity.

- Context: add only one scene-specific sentence after the fixed prefix.
- Person: combine selected appearance cues and the complete outfit into one compact sentence per person before the full realism controls. For groups, shared controls may apply explicitly to all people.
- Interaction: aim for two sentences covering reciprocal action, both expressions, contact and support, plus one short species-appropriate fur sentence. Avoid repeating generic realism language from the fixed closing.
- Furnishings: use one short sentence for the residential setting and rug, then two or three compact sentences for the two or three furniture pieces and three or four accessories. Keep each item to its identity, color, material, and essential shape or related pattern. Do not explain the selection rationale.
- Camera: use up to two sentences for viewpoint, framing, rug visibility, and readable background depth.
- Light: use one or two sentences for source, color relationship, soft contrast, and controlled exposure.
- State each variable requirement once in its appropriate paragraph. Do not restate the full palette in the lighting paragraph or repeat skin controls, background clarity, and exposure restrictions across paragraphs. Required fixed text is exempt from deduplication.

Aim for roughly 20–25 percent fewer words than an otherwise equivalent expanded prompt, as an editing guide rather than a hard word limit. Preserve extra wording when needed for multiple people, pets, or a complex requested action. Keep internal checks and styling explanations out of the copy-ready prompt.

If the user asks only for a prompt, do not generate an image. If they ask for an image, use the built-in image-generation tool and identify the uploaded rug as a **visual style reference only**, not the target to preserve or edit. Follow the host's image-generation skill when available. If no image-generation capability is available, provide the prompt and explain that rendering requires an image-capable host; do not claim an image was generated. Do not switch to an API/CLI image route unless the user explicitly requests or confirms it. Inspect the generated result for the requested subject, strong interaction, contact anatomy, plausible room and furniture, visible style-compatible rug, and photographic coherence. If a defect is found, make a targeted regeneration/edit request; do not silently claim it passed.

## Final quality check

Before returning the result, verify:

- The user's stated people, identities, season, room, pet, activity, and output mode are respected.
- Rug type, orientation, placement, and interaction zone follow the scene mapping unless explicitly overridden by the user; furniture and camera reinforce that zone, and the mapping is not pasted verbatim into the final prompt.
- The people follow the bundled character reference, with natural face/skin and season-appropriate clothing.
- Outfits are newly composed from garment categories rather than copied reference ensembles. Unless explicitly overridden, clothing colors relate to the rug through analogous or restrained complementary choices without exact shade matching; garment motifs reinterpret its visual language. Different-rug outputs change color pairing and at least two of garment combination, cut, fabric treatment, and motif/placement. “Not overly casual” does not automatically become business or evening attire.
- The final prompt contains the complete fixed person-control description above, adapted only for the requested identity and language.
- Skin follows the character skill: natural proportions, mild asymmetry, subtle texture, and soft controlled reflectance; no greasy/slick appearance or overemphasized pores. Any freckles or small marks are sparse, faint, and localized rather than dense or distributed over the whole body.
- The pet is specified or plausibly chosen, realistically scaled, and active in the scene.
- Pet fur has believable species-appropriate layering, direction, restrained color variation, light response, and contact compression without synthetic or noisy detail.
- One clear, strong, reciprocal interaction is legible; both the person's and pet's expressions read clearly and suit the action, with credible touch, posture, weight support, and anatomy.
- The selected reference action matches the user's requested posture and activity; source-photo identity, wardrobe, furniture, lighting, and framing have not leaked into the final prompt. Consecutive unspecified-pet outputs use varied compatible action families and pet appearances.
- Every pet visibly appears happy and relaxed through a coherent combination of facial and body cues; final pet descriptions do not substitute attention, waiting, upward staring, or food anticipation for this emotional state. Feeding and mouth-state descriptions remain consistent, and faces stay readable within the requested camera angle and rug coverage.
- Only one compatible interior direction is used; the rug, two or three recognizable branded/design-led furniture pieces, and three or four distinctive supporting accessories are described together in a concise paragraph without excessive item-by-item detailing.
- Furniture brand/model identities are accurate; do not invent attributions or over-brand every object. Accessories use rug-derived colors and explicitly related patterns on pattern-bearing items, with varied scale/density rather than exact motif duplication; simple sculptural or botanical items may relate through color and form.
- Furniture choices follow this individual rug's visual traits and the room's activity zone, rather than a fixed style-to-model mapping. Check the latest three available same-room schemes for repeated primary models, recurring pairings, and superficial color/brand swaps; honor explicit model requests or same-home continuity.
- Different rugs in a same-room batch produce furniture schemes differing in at least two of primary silhouette/volume, secondary shape/structure, and principal material pairing, while preserving rug harmony and concise furniture descriptions.
- Upholstery is named clearly when tactile appearance matters; requested velvet gets a brief pile/nap cue, not lengthy microtexture directions, and the selected light keeps it visible.
- Rug description is brief and style-level; its broad palette and color balance harmonize with the reference, without copying the exact design.
- Lighting varies naturally between prompts while remaining soft and balanced, with controlled exposure, readable shadows, and no harsh contrast or blown highlights; it supports a lived-in North American home rather than a showroom.
- The final prompt starts with the fixed independent-brand positioning prefix and uses concise, unlabelled prose paragraphs in the required scene → person → pet interaction → room/furnishings → camera → light/color order, with person and interaction paragraphs adjacent and furnishings kept together; default output is entirely English and ends with the exact fixed English closing paragraph and nothing after it. Use a faithful translation only when the user explicitly requests another output language.
- Camera wording keeps the interaction and the background room details clearly visible, with moderate-to-deep depth of field rather than pronounced shallow-focus blur or bokeh.
- Variable prose is concise and non-repetitive; the fixed prefix, complete person controls, fixed closing, seven-paragraph sequence, and all requested scene details remain intact.
- The image is sharp at the interaction points and does not depend on motion blur; no plastic skin, image noise, warped anatomy, floating objects, or visible text/watermarks.
