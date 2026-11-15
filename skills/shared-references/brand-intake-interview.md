# Brand Intake Interview

Use this before producing any branding output, including one-off image prompts. The interview is the work: do not treat missing brand inputs as permission to guess. Reuse facts and files the user already supplied; ask only questions that can change the result.

## Interview sequence

### 1. Audit what is already available

Inspect the project folder and user-provided links/files before asking. Look specifically for `brand identity.txt`, `prompts.md`, a locked `AGENTS.md` or `brief.md`, approved logo files and variants, current brand guidelines, palette/type specifications, product or service imagery, existing campaign copy, and earlier approved prompts. If `brand identity.txt` exists, read and preserve it; never make a duplicate or overwrite it. If it is absent, create it only after the user approves the compact brief summary. Do not infer approval from a file merely existing; check its status or ask.

Create a quiet working table with three states:

| State | Meaning | Handling |
|---|---|---|
| Confirmed | Explicit in the user brief or approved asset | Reuse exactly; do not ask again |
| Needs confirmation | Conflicting versions, unclear ownership/status, or a consequential ambiguity | Ask one specific question |
| Missing | Required to write the selected prompt | Ask before drafting that prompt |

Separate confirmed user facts from interpretations and recommendations. Never present an inference as a client-approved decision.

### 2. Ask a compact first round

Ask only for missing, decision-critical information. Group questions so the user can reply in one message, and state which facts you already found so they can correct them. Prefer concrete prompts over vague questions like “What style do you like?”

#### Brand and business

- Exact brand name and approved spelling in every script; attach the current logo if available.
- What the brand sells or does, where it operates, and what is actually different about the offer.
- Is this a new concept, a live brand, or a refresh? Which existing elements must remain?

#### Audience and story

- Who is the priority audience, in which country/city and language or dialect?
- What customer need, moment, ritual, founder origin, ingredient, craft, or place should the brand story be built from? Ask what is factual and what is only a desired direction.
- What customer promise and supporting proof are approved? Which product, health, sustainability, heritage, or performance claims are prohibited or unverified?

#### Visual system and source files

- Which logo files and variants are approved, and what must not be redrawn or altered?
- Exact approved hex colors and roles; exact typefaces/scripts if known. If either is not locked, ask whether the user wants options proposed for approval before any generation prompt.
- Existing guidelines, competitor references, prior outputs, licensed imagery, and “must avoid” directions.

#### Deliverables and use

- Which prompt outputs are wanted now: logo concept/refinement, visual logo-guideline board, mockups, product or campaign posters, social/ad banners, story-led imagery, standalone HTML presentation build prompt, or written guideline document prompt?
- For each image: the target generator if known, aspect ratio or platform, number of variants, and whether it is a clean presentation mockup or marketing scene.
- For each code-agent prompt: should the recipient create the HTML file, or should it only review the files and return an implementation plan?
- Exact approved headline/CTA/legal copy, or permission to draft copy as unapproved options.

Do not ask every sub-question when the user has already answered it. If the user asks for a full prompt pack, confirm the selected deliverables and create a compact inventory; do not bury the user in unrelated production questions.

### 3. Resolve critical gaps before drafting

If a missing answer changes brand strategy, copy, color, audience, country/region, logo fidelity, selected deliverable, or production format, ask and wait. You may continue independent research or file inventory while waiting, but do not draft a dependent prompt using a guess.

When several decisions are open, offer 2–3 short, clearly different options with their trade-offs. Keep proposals labelled **options**, not approved facts. For questions with a clear factual answer (such as exact logo text or platform placement), ask directly rather than inventing options.

### 4. Lock and show the input summary

Before making project files, show the user a concise confirmation block. This is a brief summary, not prompt output:

```text
Brand / exact scripts:
Offer / category:
Market / audience / language:
Approved story / promise / proof:
Approved identity assets:
Locked colors and type:
Selected deliverables and target formats:
Must-keep / must-avoid constraints:
Open items:
```

Keep open items visible. Ask the user to correct the summary or approve it before producing prompts. If the user already explicitly approved the same brief in the current project, do not force a redundant second approval; summarize the inherited lock and ask only about changed or newly required details.

## Interview behavior

- Let the user answer in natural language or by attaching a brief/logo. Do not require them to know design vocabulary.
- Ask about goals and evidence before asking for style labels. Translate “premium,” “Egyptian,” “modern,” or “luxury” into concrete customer, material, tone, and channel choices only after the user clarifies what they mean.
- Keep Egyptian and other Arabic-market contexts distinct. Ask which country, city, dialect, and customer norms matter; do not treat Arabic markets as interchangeable.
- For people, storefronts, streets, homes, or other real settings, confirm country/region and any important cultural or wardrobe details. Avoid stereotypes.
- Preserve the user's exact approved Arabic spelling and punctuation. Ask before transliterating or normalizing wording.
- Ask before inventing a missing name, slogan, product, claim, font, color, mockup type, scene, or deliverable.
- When the user does not know an answer, show 2–3 grounded directions or label the field open. Get approval before locking a choice.
- For a “Let's brand” request, ask questions and show only the concise brief summary in chat. Keep copy-ready prompts and long research analysis inside `prompts.md`.
- If colors are missing, ask for exact colors or offer proposed palettes for approval. Never place unapproved colors in the identity file as locked values or in final prompts.

## After the interview

Use the approved summary as the single source of truth for every selected prompt. For a full branding workflow, create `brand identity.txt` in the project root only if absent; if it already exists, use it and do not recreate or overwrite it. Write all requested prompt modules to `prompts.md`, preserving unrelated approved content if that file already exists. If later answers change the brief, update the identity lock only after approval and regenerate only affected prompt sections.

Before mockup prompts, complete the required visual scan: at least five distinct global source pages and five distinct Arabic-market source pages, opened and visually inspected. Follow `../visual-analysis-workflow.md` and the `agent-reach` skill's access rules. If a source image cannot be inspected, it does not count; add the required Agent Reach note to `prompts.md` and leave affected prompts provisional.

After writing files, reply only with a concise completion note and paths. Do not paste prompt contents into chat.
