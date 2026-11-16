# Reference Instructions — `lets-brand`

This is the orchestration guide for the complete branding workflow. Read it before asking questions or starting research, then read `../../shared-references/research-reference-standard.md`. Also read each selected specialist's own `references/reference.md` before invoking that specialist. Do not activate all 12 specialists by default.

## Before doing project work

1. Inspect the project directory, `brand identity.txt`, `prompts.md`, logo/design-system files, previous decisions, and any source links. Do not edit or create output files yet.
2. Ask the user which outcomes they want now. Use only the module choices that could change the deliverables: identity/refresh; new logo or revision; text-only wordmark; color variants; logo-derived pattern; mockups; posters/campaigns; presentation build prompt/HTML; written guidelines. Ask which prompt tool receives the prompts only if its behavior affects the format.
3. Ask only missing pivotal facts: offer/differentiator, priority audience and market, approved story/claims, exact name/script, palette status, actual logo status, must-keep/avoid, and actual channels. Skip anything clear from supplied files. Keep this batch to 3–6 questions and put related decisions together.
4. Present one concise brand lock, selected modules, and unresolved questions. Wait for approval before starting project-specific web/image research, drafting prompts, writing `brand identity.txt`, or creating any artifact. Create `brand identity.txt` only if absent; preserve existing content otherwise.

## Research plan by module

Create a research row for every selected module before searching. Each row names the user decision, library/query, at least five distinct real project pages, image type to inspect, and what will be learned. Reuse a source across modules only when the exact relevant image was inspected and actually answers both questions.

| Selected module | Research focus | Inspect |
|---|---|---|
| New logo | Five distinct logo projects, script/category/market-relevant | Actual marks, variants, guideline pages; use logo reference library |
| Wordmark | Five actual Arabic/Latin/bilingual lettering projects | Glyph forms, joins, rhythm, proportions, text hierarchy |
| Logo colors | Five logo/guideline color examples | Logo/background pairings, reversals, monochrome behavior, labels/roles |
| Logo pattern | Five actual repeat systems | Mark derivation, tile, density, scale, color, application |
| Mockups | Five global plus five Arabic-market projects | Exact touchpoints, asset placement, materials and scene choices |
| Posters/banners | Five relevant campaign/ad/poster projects plus current official specs | Message order, crop, copy area, focal image, placement size |
| Presentation | Five identity case-study/presentation pages | Story sequencing, hierarchy, whitespace, pacing and mobile reading |
| Written guidelines | Five relevant guidelines/system documents | Evidence vs rule, ownership, actionable examples, governance |
| Brand identity | Five real identities in relevant categories/markets | Positioning reflected in logo, palette, type, imagery and applications |

Use Agent Reach for the public channels it supports and follow its read-only/login/block rules. If it returns text only, use a visual-capable browser/viewer or permitted temporary image retrieval for actual pixel inspection. Record any images not seen; never call a search caption “visual analysis.” Apply the full direct-source card from the shared research standard. The exact note for an unmet visual threshold belongs in `prompts.md`.

## Stage gates and routing

1. **Identity gate:** If the brand brief is absent, run `../../brand-identity/SKILL.md`; lock exact spelling, audience, market, differentiators, factual story, claims, and palette roles. Don't research a style direction before the brand context is known.
2. **No-logo gate:** Run `../../logo-guidelines/SKILL.md` in pre-design mode. Analyze at least five relevant actual logo images, then present a short Logo Direction Guide. Wait for approval.
3. **Logo decision gate:** If symbol/combination is approved, route to `../../logo-design/SKILL.md`; if name-only is approved, route to `../../logo-text/SKILL.md`. Ask 5–6 pivot questions after the guide, skipping answered facts. If an approved mark exists and only an edit is wanted, use `../../logo-prompting/SKILL.md` instead of starting concepting.
4. **System extensions:** `../../logo-colors/SKILL.md` requires approved HEX roles; missing palette returns to identity. `../../logo-pattern/SKILL.md` requires approved master/vector and permitted component use. Neither is automatic.
5. **Applications:** `../../mockup-prompting/SKILL.md` covers real product/touchpoint scenes, `../../banner-design/SKILL.md` covers campaign placements and exact copy, `../../brand-presentation/SKILL.md` covers a single-page HTML case-study, and `../../brand-guidelines-doc/SKILL.md` covers voice/written usage/checklist documents. Choose only what the user asked for.
6. **Approval:** show each stage summary, wait for user confirmation, then continue. Never turn one “Let's brand” request into silent approvals for all downstream directions.

## Evidence-to-prompt chain

For each selected output, put a compact trace in `prompts.md`: approved brand fact → source observation (URL + visual status) → transferable design method → prompt instruction → quality check. Keep examples relevant to the user's market and channel. Use each source to learn one method, explicitly state what not to copy, and don't mix unrelated designs into a style collage.

Each prompt lists exact user assets to attach and their role, exact Arabic/Latin spelling, approved HEX values and roles, layout/hierarchy, ratio/placement, environment/materials as relevant, exclusions, unresolved inputs, and a concrete pass/fail review checklist. Keep the approved logo immutable in mockups. Keep prompts in the requested project file; do not paste the full pack into chat.
