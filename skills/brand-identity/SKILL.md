---
name: brand-identity
description: Interviews the user, audits existing identity assets, and confirms the brand brief before any output. Activate at the start of a new brand, or when an existing logo/brief needs to drive a prompt pack.
argument-hint: "[brand-name] [industry]"
metadata:
  author: mostafa
  version: "1.0.0"
---

# Brand Identity — The Brief

The brief locked here is the source of truth for every later prompt (logo, logo-guideline board, mockups, story visuals, posters, presentation, banners, and written guidelines). Before drafting any output, read `../shared-references/brand-intake-interview.md`, `references/identity-questionnaire.md`, `references/personality-archetypes.md`, and `references/brief-authoring-prompt.md`. When Arabic-market research or a visual comparison is requested, also use `../shared-references/visual-analysis-workflow.md`, `../shared-references/brand-design-reference-library.md`, and `../shared-references/arabic-brand-design-reference-library.md`.

## When to Use

- First step of any new brand project, real or practice
- Before writing any logo-generation or mockup-generation prompt
- When a brand's personality or audience is vague and prompts keep coming out generic

## Workflow

1. **Audit and interview before output**: inspect all supplied briefs, logo files, guideline documents, campaign copy, and prior approvals. Use `../shared-references/brand-intake-interview.md`; extract known facts and ask only missing, decision-critical questions. Identify contradictions between the brief and logo/source assets before treating them as approved.
2. **Collect the brief** (use `references/identity-questionnaire.md`):
   - Brand name (and script: Arabic / English / both)
   - Industry / what the business actually does
   - Target audience (who, where, what they value)
   - Personality — pick from `references/personality-archetypes.md` or describe freely
   - Brand's concrete difference, proof, and primary customer promise; if these are not known, record them as open questions instead of fabricating claims
3. **Build a distinct direction** from the approved brief, not from a trend label. If research is requested, create a small, credited comparison set. Identify category conventions and one or two opportunities to differ; separate observation from interpretation. Never make a reference's logo, palette, pattern, or typography the new brand's default.
4. **Translate the approved direction into colors** using `references/color-psychology.md` — propose 3–4 candidate hex codes with named roles, state the reason, check contrast, and get approval before locking. Keep existing approved colors exactly. If the user only wants prompts based on an existing brand, do not reopen settled palette choices.
5. **Set typography and image directions** — describe letterform character, hierarchy, language/script needs, story source, image subjects, lighting, composition, and avoidances. Recommend actual font names only when asked or when availability/license has been checked. Use `references/story-to-visual-prompt.md` only when the user has approved story material and selected a story-led visual.
6. **Confirm the whole brief back in a compact block** before creating any prompt:
   ```
   Name and scripts: ...
   Offer/category: ...
   Market and audience: ...
   Promise and proof: ...
   Personality: ...
   Differentiation: ...
   Colors: #XXXXXX (role), #XXXXXX (role), ...
   Typography and language direction: ...
   Image/art direction: ...
   Constraints / open questions: ...
   ```
7. Save the approved brief in the project's `AGENTS.md` or `brief.md` (see `../brand-presentation/references/page-structure.md`) when the user asks to maintain project files. Label candidate versus locked values and record who approved the lock and when. For prompt-only requests, return the approved summary and relevant prompt inputs without creating project files unless asked.

## Rules

- Never silently invent a color palette, audience, proof claim, market, or personality. Offer clearly labeled options and get a decision before calling them locked.
- If the user already has a locked palette or name from an earlier session, read it back and confirm instead of re-asking from scratch.
- Geography matters: use the market from the brief, or ask if it is missing — it changes what "premium" or "everyday" looks like, and later stages need it to avoid producing scenes from the wrong country.
- Do not turn a competitor or inspiration reference into a close imitation. Keep a short originality note in the brief if a reference scan informed the direction.
- Keep functional requirements alongside personality: language/script, accessibility, environments, physical or digital touchpoints, production limits, and legal restrictions can change the identity decisions.
- The interview comes before output even if the user says “make it better.” Audit first, reuse confirmed information, ask about material gaps or contradictions, and wait for confirmation of the brief summary before writing prompts.
- Do not produce palette, story, typography, mockup, or campaign prompts from stereotype labels such as “Egyptian,” “Arabic,” or “premium.” Ask what the user means in terms of audience, factual story, script/dialect, and use context.
