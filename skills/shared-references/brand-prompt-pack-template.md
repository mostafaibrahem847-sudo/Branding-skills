# Brand Prompt Pack Template

Use after the user completes `brand-intake-interview.md` and approves the compact brand lock. This template organizes prompts for an external image generator or coding agent. It does not assume the current agent can create or inspect images.

## Pack cover / input lock

```text
Brand:
Approved name and exact spelling by script:
Offer and category:
Market, priority audience, language/dialect:
Approved story, promise, proof, supplied copy:
Locked palette: #HEX — role; #HEX — role; ...
Locked typography / script behavior:
Approved logo files and variants:
Selected modules:
Target tools, aspect ratios, placements, output format:
Must preserve:
Must avoid:
Open items (do not fill with guesses):
```

## One prompt card per deliverable

Use this structure for each ready-to-paste prompt. Duplicate only for a distinct concept, channel, or asset.

```text
PROMPT TITLE:
PROMPT TYPE: image generation / image editing / HTML build / written guideline
TOOL OR RECIPIENT:
PURPOSE:
APPROVED INPUTS: [include only facts and assets from the locked brief]
SOURCE ASSETS: [exact file names; say which files must be attached]
DELIVERABLE: [what the result should contain]
AUDIENCE AND CONTEXT:
STORY / MESSAGE:
VISUAL IDEA: [one specific direction with reason; no reference imitation]
COMPOSITION AND HIERARCHY:
MATERIALS / ENVIRONMENT / LIGHT / CAMERA: [only as relevant]
BRAND COLOR SPECIFICATION: [exact approved hex values and roles]
TYPE AND COPY: [exact approved text; if the generator cannot render it, leave a clean area for later typesetting]
LOGO FIDELITY: [attach approved logo; preserve exact shape and spelling; otherwise generate unbranded space for manual placement]
SIZE / ASPECT RATIO / SAFE AREA:
OUTPUT AND TECHNICAL REQUIREMENTS:
NEGATIVE CONSTRAINTS: [relevant errors only; include no fake logo/text/watermark as needed]
QUALITY CHECK: [legibility, crop, script, contrast, brand fit, originality, asset fidelity]
```

## Image prompt rules

- A prompt must be specific enough to run without the agent inventing context, but it must not contain unsupported facts. Keep unresolved fields visible and ask before completing the affected prompt.
- Use exact hex values from the approved brief. If the generator may drift, specify both palette roles and the surfaces on which each color appears.
- Attach an approved logo as an image/reference input where supported. If exact Arabic/Latin lettering cannot be preserved, request a clean unbranded surface and composite the real logo and copy in a design tool.
- Tell the model what to render, what should remain blank, where the focal point sits, how the crop works, and what is excluded. Avoid huge keyword piles and contradictory adjectives.
- For real people and locations, specify the approved country/region and user-confirmed details. Do not use cultural stereotypes as shortcuts.
- Keep image generation separate from production claims: a visual mockup does not validate print mechanics, materials, safety, or regulatory copy.

## Code-agent prompt rules

- State whether the recipient should create a file or return a plan only. The prompt-only default is to return an implementation prompt, not execute it.
- For HTML assets, request one standalone HTML/CSS/vanilla JS file with no framework or build step, and name exact approved asset paths. Ask the user before substituting absent assets or copy.
- Include responsive, accessibility, exact-copy, asset-integrity, and local-open checks as requirements inside the downstream prompt. Do not claim those checks have run unless they actually have.

## Pack closeout

List prompts delivered, attached inputs required, remaining open items, and which prompt should be run first. Keep user approval checkpoints visible between identity, logo, mockup, presentation, campaign, and guideline stages.
