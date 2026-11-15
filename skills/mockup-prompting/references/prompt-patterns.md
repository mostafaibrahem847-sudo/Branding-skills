# Mockup Prompt Patterns

Read `brand identity.txt`, when present, and `mockup-types-by-business.md` first. In the full branding workflow, use the [Brand Design Reference Library](../../shared-references/brand-design-reference-library.md) and the [Arabic Brand Design Reference Library](../../shared-references/arabic-brand-design-reference-library.md) to visually inspect at least five global and five Arabic-market projects before drafting. Open direct case pages and inspect their actual identity/mockup imagery; titles, snippets, and text summaries do not count. Follow the `agent-reach` skill's access rules, and use a visual-capable browser/tool if text retrieval does not expose imagery. Do not copy any reference's product, composition, logo, palette, typeface, or distinctive treatment.

## Prompt inputs to collect

For each approved mockup, establish:

- The exact object, screen, or scene and why a customer would encounter it
- The intended market and country/region for any real-world setting
- Object dimensions or useful scale cue, construction, substrate, finish, and realistic condition
- The actual logo file and approved lockup; the prompt must not redraw or reinterpret it
- Exact approved hex codes for any brand-colored surfaces and the background
- Where the logo sits, approximate physical size, any approved clear-space rule, orientation, and whether it is printed, embossed, embroidered, etched, or shown on-screen
- Camera angle, lens feel, crop, lighting, surface shadows, and image aspect ratio
- Whether this is a clean brand-guidelines presentation or an explicitly requested campaign/lifestyle scene
- One or two general methods from visually inspected references that fit the approved brand, plus the original element that must not be copied
- Any exact visible copy; for image generation, default to no words and add verified text afterward

Ask for missing facts that materially change the prompt. Do not guess the country, economic tier, product substrate, audience, or required mockup type.

## 1. Clean studio object mockup

Use for brand presentations and guidelines when the goal is to inspect identity application clearly.

“Create a clean studio product photograph of [exact object and product type] for [brand], a [specific business]. The object is [dimensions or scale cue], made from [verified substrate/material], with [construction, edge, closure, finish, and realistic texture]. Use [exact HEX] for the brand-colored surface and [exact HEX] for the plain background; allow only the neutral material colors inherent to [specified material]. Apply the attached approved [logo lockup] at [exact position], at approximately [physical proportion], in [approved print/finish method]. Preserve the attached logo's spelling, silhouette, proportions, color, and clear space; do not redraw it. If logo fidelity cannot be guaranteed, leave a blank placement area for compositing the real logo afterward. Show [camera angle and crop] with soft, even [light direction], realistic contact shadows, legible material texture, and enough margin to inspect the whole object. Output one object, front-facing enough to evaluate, with no people, extra products, captions, invented marks, fake text, watermark, or decorative set dressing.”

## 2. Real-world place or person

Use only when the user wants context/lifestyle imagery or the actual customer touchpoint requires it. Use the geography already locked in the brief; if it is missing, ask first.

“Create a [documentary / campaign] photograph of [specific scene or person] for [brand] in [country, city/region, and neighborhood or setting type]. The location should read as [verified architectural, cultural, and economic context], not a generic stock-photo default. The person, if shown, is [non-sensitive, task-relevant description] doing [natural action] in [realistic context]. Show [object/touchpoint] with the attached approved logo placed at [position and approximate scale] using [realistic application method]. Use only [exact HEX codes] for brand-colored elements; set unbranded environmental colors/materials to [specific described context]. Composition: [camera distance, angle, lens feel, crop, negative space]. Lighting: [brand-matched light quality and direction], with [realistic level of contrast]. Keep the logo legible and physically plausible. No invented copy, extra logos, stereotypes, unrelated props, altered marks, or unapproved color accents.”

## 3. Packaging family or product range

Use when the user needs to demonstrate a system across multiple product variants. Do not invent flavors, claims, ingredients, sizes, or regulatory text.

“Photograph a coherent [number] item family for [brand and category]: [list only user-approved variants]. Keep the shared layout consistent: [logo position], [type hierarchy], [repeatable brand device], and [exact HEX palette and roles]. Differentiate variants only through [approved coding rule such as a named accent, illustration, or label field]; use [exact approved hex for each color]. Show [pack formats/materials] from [camera angle], arranged [specific grouping and spacing] so each label can be compared. Use [background HEX] and [lighting]. Preserve the attached logo artwork. Leave all small copy blank for accurate typesetting unless exact copy assets are supplied. Do not add unapproved ingredients, nutrition claims, seals, barcodes, regulatory marks, or decorative elements. The result should read as one family at a glance and as distinct products on closer inspection.”

## 4. Digital interface or device mockup

When possible, build the actual UI in standalone HTML/CSS and place a screenshot into the device scene. Image models frequently invent interface text and controls.

“Create a [device/context] product mockup showing the supplied interface screenshot exactly. Do not generate, alter, or paraphrase the interface, logo, words, numbers, icons, or controls. Device: [model/form factor if supplied, otherwise generic unbranded device], viewed from [angle], with [screen reflections and bezel detail]. Place it against [exact background HEX] with [lighting and shadow]. Keep the screenshot fully visible and undistorted; preserve a readable screen scale. No extra screen, invented notifications, interface copy, watermark, or brand mark outside the supplied UI.”

## 5. Presentation-ready versus campaign photography

- **Identity/guideline image:** clean lighting, clear material, controlled crop, little or no environment, faithful logo placement.
- **Campaign image:** a real narrative or lifestyle moment only if requested; follow the brand's image direction and market context. Give the story one subject and one action.
- **Stylized or illustrated mockup:** match the illustration/rendering style to the approved identity. Do not combine flat identity artwork with cinematic effects by default.

## Placement fidelity checklist

Before delivery, check: the correct attached logo variant; no distorted/misspelled mark; plausible scale and surface perspective; clear space; approved colors; material/print method; expected crop; no generated fake text; and fit with the audience, market, and actual business touchpoint. When a model cannot preserve the real logo, generate the unbranded object and composite the approved asset afterward.
