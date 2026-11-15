---
name: lets-brand
description: Orchestrator for the full branding workflow — interviews the user, locks the brief, and prepares detailed prompts for logo, mockups, campaign posters, story visuals, HTML presentation, and guidelines. Activate when the user says "let's brand [name]", asks to start or refresh a brand, or asks for a full branding prompt pack.
argument-hint: "[brand-name] [industry] [notes]"
metadata:
  author: mostafa
  version: "1.0.0"
---

# Lets Brand — Full Branding Workflow Orchestrator

Runs the branding workflow for one brand by interviewing the user, checking supplied assets, locking the brief, then preparing a detailed prompt pack for the requested deliverables. Each sibling skill also works on its own — call it directly when only one stage is needed. Prompt generation is the default handoff: do not assume this agent can generate images or that the user wants HTML/code executed.

## When to Use

- User says "لِتس براند [اسم]" / "let's brand [name]" / "ابدأ لي مشروع براندينج جديد"
- A new fake-client or real-client branding project is starting from zero
- User wants the full pipeline: identity → logo → mockups → presentation → banners → guidelines doc
- User wants to resume a branding project that already has some assets and continue from where it stopped

## Sibling Skills (invoked in order)

| Order | Skill | Produces |
|-------|-------|----------|
| 0 | `../shared-references/brand-intake-interview.md` | Asset audit, focused questions, and a user-approved brand lock before output |
| 1 | `../brand-identity` | Confirmed brand brief and, when selected, a prompt for story-led visual direction |
| 2 | `../logo-prompting` | Ready-to-paste prompts for logo concepts/refinement and optional visual logo-guideline boards |
| 3 | `../mockup-prompting` | Ready-to-paste prompts for user-selected physical and digital touchpoints |
| 4 | `../brand-presentation` | A detailed prompt for a standalone HTML brand presentation; build only when explicitly requested |
| 5 | `../banner-design` | Ready-to-paste prompts for selected posters, social/ad banners, and campaign visuals |
| 6 | `../brand-guidelines-doc` | Prompts for a written guideline document and/or visual guideline board, as selected |

## Workflow

### Step 1 — Interview and audit before output
Read `../shared-references/brand-intake-interview.md`. Inspect the project folder, brief, logo, guidelines, exact palette/type, campaign copy, prior approvals, and links before asking anything. Reuse known facts and ask only missing, decision-critical questions. Confirm brand, market, audience, real story, script/dialect, approved assets, constraints, and which prompt modules/formats are wanted. Do not produce even a single prompt until the user has corrected or approved the compact brief summary. Never redo an approved stage without being asked.

If the user requests visual inspiration or a broad scan, use `../shared-references/visual-analysis-workflow.md` and select relevant projects from both `../shared-references/brand-design-reference-library.md` and `../shared-references/arabic-brand-design-reference-library.md`. Count distinct projects, record direct source links, separate facts from interpretation, and mark self-published or conceptual work. For Arabic-market work, ask which country, city, dialect, and audience norms apply. Do not begin an unnecessary scan and never copy a recognizable design element.

### Step 2 — Lock the brief, then build the requested prompt pack
Run `../brand-identity` to confirm name/scripts, offer, market/audience, approved story and claims, personality, exact approved colors, typography/language, approved logo files, channels, and constraints. Do not call proposals “locked” until the user approves them.

Read `../shared-references/brand-prompt-pack-template.md`. Include only modules the user selected or clearly requested:

1. Logo concept/refinement prompt, preserving approved files and exact text.
2. Optional visual logo-guidelines board prompt (logo usage, color, type, approved rules only).
3. Mockup prompt for each confirmed touchpoint, matched to the actual business and user-selected setting.
4. Campaign poster/social/ad banner prompts, with verified dimensions and exact approved copy or blank typesetting areas.
5. Story-led visual prompts derived from `../brand-identity/references/story-to-visual-prompt.md` and only the confirmed story facts.
6. HTML presentation build prompt from `../brand-presentation/references/build-prompt.md`.
7. Optional written brand-guidelines authoring prompt.

Present one organized, copy-ready prompt pack with the brand lock, required reference files to attach, one prompt per distinct deliverable, relevant exclusions, target format, and unresolved items. Image generation and code execution are not implied by the pack. If the user explicitly asks the agent to build HTML or produce another artifact, execute only the selected module using its skill and confirm the result before moving to another production stage.

### Step 3 — Never skip the brief or interview
No logo, mockup, poster, story, guideline, or presentation prompt is written before the selected output's required inputs are confirmed. If the user has an existing brief and logo, audit and reuse them; do not restart identity from zero. If any prompt-critical detail is missing, ask before filling it.

Keep all seven skill folders and `../shared-references/` together in the collection directory. Shared references include the two design libraries, interview, prompt-pack template, and analysis method; this folder is a resource, not another skill.

## Running One Stage Only

If the user asks for one piece ("اديني برومبت لوجو", "عايز prompt للبوستر"), load that sibling skill directly, but still run the relevant part of the intake: inspect existing inputs and ask for any missing facts before returning a prompt. A direct request to build a page or create an asset overrides prompt-only default for that selected deliverable.
