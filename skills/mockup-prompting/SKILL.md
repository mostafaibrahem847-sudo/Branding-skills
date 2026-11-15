---
name: mockup-prompting
description: Interviews the user about the intended touchpoints and existing assets, then writes detailed image-generator prompts for brand mockups. Activate whenever the user asks for product mockups or brand applications.
argument-hint: "[brand-name] [mockup-type]"
metadata:
  author: mostafa
  version: "1.0.0"
---

# Mockup Prompting

Writes precise, ready-to-paste image-generation or compositing prompts that show an approved identity on relevant physical or digital touchpoints. Prompt-only handoff is the default; the user runs the prompts in their chosen image tool. Requires a locked brief from `../brand-identity` and the approved logo asset from `../logo-prompting` unless the user explicitly asks for an early concept mockup.

## When to Use

- User wants to see the logo "in context" (on a bag, a sign, a t-shirt, packaging, a vehicle, etc.)
- Building the mockup section of a `../brand-presentation` page
- An earlier mockup came out wrong (wrong business category, wrong country, clashing photography style)

## Step 0 — Interview and audit

Read `../shared-references/brand-intake-interview.md`. Inspect the approved brief, actual logo, product images, selected campaign, and existing mockups before asking. Confirm only missing details that change the scene or asset: which touchpoints, clean mockup versus marketing lifestyle image, market/geography, target image tool/aspect ratio, and required copy. Show the input lock and wait for confirmation before writing the prompts.

## Step 1 — Pick mockups that actually fit the business type

Never default to a generic mockup set. Use `references/mockup-types-by-business.md` to propose 3–6 relevant applications, ranked by customer visibility and business value. Ask which real touchpoints to prompt when the brief does not identify them. For research examples, consult `../shared-references/brand-design-reference-library.md` and, for Arabic-market work, `../shared-references/arabic-brand-design-reference-library.md`; adapt the system logic, not recognizable artwork.

## Step 2 — Match the photography style to the logo's own style

Choose the image treatment for the job. For guideline presentations, default to a clean studio object shot with readable material and a neutral exact-hex background. For campaign/lifestyle requests, use a narrative scene only when the user asks for it, the brief supports it, and geography/context are specified. A flat logo can appear on a realistic object; avoid effects that compete with or misrepresent the logo.

Only use narrative/lifestyle photography (a real setting, a real person) if the user explicitly asks for that style AND it's for marketing content, not for a brand-identity presentation page.

## Step 3 — Attach the real logo file, don't re-describe it

Attach the actual approved logo image to every prompt when the tool supports references. Do not ask an image model to redraw precise lettering. If it cannot preserve the mark reliably, generate a blank/unbranded object and composite the logo file afterward.

## Step 4 — Geography and context

If a mockup includes a real-world setting (storefront, street, workplace, home, or person), use the country/region and economic context already locked in the brief. If absent, ask before generating. Avoid broad stereotypes; specify only the observable environmental details the user actually wants.

## Step 5 — Write and review the prompt

1. Read `references/prompt-patterns.md` and fill its fields with verified details: object, material, scale, print method, logo position, colors by exact hex, camera, light, crop, and realism level.
2. State whether the image is a clean identity mockup, an actual UI/device mockup, or campaign photography.
3. Keep the generated image free of invented copy, fake branding, labels, watermarks, and interface text. Place accurate copy and the approved logo with real assets in a later design/compositing step. State which files the user should attach and which elements should remain blank for reliable compositing.
4. Check every prompt against the brief, selected touchpoint, reference source, and platform requirements. Ask before adding a new color, product variation, or scene.

## Rules

- Never put a flat/minimal logo into a hyper-realistic cinematic scene unless the user explicitly wants that specific contrast.
- Never generate a mockup type that doesn't match the business (no staff-uniform mockups for a brand with no staff-facing retail presence, no clothing-brand studio shoots for a corner shop).
- Always isolate product mockups against a plain/neutral background unless lifestyle/marketing photography was explicitly requested — isolation is what makes a mockup usable in a guidelines doc or presentation page.
- All image prompts must use exact approved hex codes for brand colors and background. Do not use vague substitute color names; ask if a required value has not been locked.
- Treat a generated image as a presentation mockup, not proof that a package is manufacturable or that required regulatory copy is correct.
- Make every prompt paste-ready: specify one deliverable, subject/object, materials, scale, logo placement, exact hex colors and roles, background, lighting, camera/crop, aspect ratio, realism level, exclusions, and a short quality checklist. Avoid contradictory adjective piles.
- Do not generate image files unless the user explicitly asks and an image-generation capability is available. A prompt request means return the prompt for the user's external tool.
- For story-led image requests, read `../brand-identity/references/story-to-visual-prompt.md` and use only approved story facts. Do not use national/cultural shorthand as a substitute for a confirmed story.
