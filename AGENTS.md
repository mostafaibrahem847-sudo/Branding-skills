# AGENTS.md — Branding Skills Collection

This folder (`branding-skills/`) is a set of 12 skills for an interview-first, prompt-first branding workflow — identity → logo research/concepting → mockups → posters/campaigns → HTML presentation → visual/written guidelines. Build images or HTML only when the user explicitly asks for the artifact. You are an agent that has access to these files on disk. This file tells you how to use the collection.

## What a "skill" means here

Each skill folder under `skills/` is a self-contained instruction set: a `SKILL.md` plus a `references/` folder and sometimes `templates/`. Every skill's `references/reference.md` is mandatory and must be read together with `skills/shared-references/research-reference-standard.md` before acting. These are plain Markdown files — there is no special runtime. **Reading a `SKILL.md` and its referenced files IS "activating" the skill.** When a skill's SKILL.md tells you to read another file before doing something, actually read it — don't skip straight to generating output from the SKILL.md summary alone.

## The 12 skills

| Folder | Role |
|---|---|
| `lets-brand/` | Orchestrator — read this first when starting a new brand project or when asked to run the full pipeline |
| `brand-identity/` | Step 1 — the approved strategy and connected identity system (logo, palette, type, graphics, imagery, voice, and application rules) |
| `logo-guidelines/` | Step 2 for a new logo — researches actual logo projects and sets pre-design direction rules; also writes evidence-based use rules for an approved mark |
| `logo-design/` | Step 3 for a new logo — asks at least five or six missing logo decisions, confirms a route, then writes the concept prompt |
| `logo-text/` | Optional — interview and prompts for a text-only Arabic, Latin, or bilingual wordmark |
| `logo-colors/` | Optional — specifies approved logo color, monochrome, reverse, and contrast variants from exact palette values |
| `logo-pattern/` | Optional after logo approval — derives a controlled repeat pattern from the real approved mark |
| `logo-prompting/` | Revision compatibility — refines an existing mark or repairs an earlier logo prompt |
| `mockup-prompting/` | Step 4 — AI product/application mockup prompts, matched to business type and logo style |
| `brand-presentation/` | Step 5 — assembling everything into one single-page, Behance-style HTML file |
| `banner-design/` | Optional — social/ad/web-hero banners at correct platform sizes |
| `brand-guidelines-doc/` | Optional — a written guidelines document (voice, usage rules, checklists) |
| `shared-references/` | Shared resource — 60 global, 50 Arabic-market, and 27 logo-specific project references, intake interview, prompt-pack template, and visual-research method |

Full detail on each is in `README.md` and inside each skill's own `SKILL.md`.

The shared reference folder is not a skill. Keep it alongside all twelve skill folders so cross-skill relative links resolve. Use its case studies to learn design methods, not to copy logos, palettes, typography, layouts, or signature graphics. Portfolio pages may be conceptual or self-published; label their status and do not claim verified commercial results unless the source proves them.

The default deliverable is a detailed prompt pack for the user's chosen image generator or coding agent. Do not assume the agent should generate images or execute an HTML prompt unless the user explicitly asks for those artifacts.

## How to behave when a branding request comes in

1. **Identify which stage is being asked for.** "Let's brand X" / "ابدأ مشروع براندينج" → load `skills/lets-brand/SKILL.md` and follow its staged workflow. A request for just one piece ("اديني برومبت لوجو", "اعمل الصفحة بتاعة البراند") → go straight to that skill's own `SKILL.md`.
2. **Interview and audit before output.** Read `skills/shared-references/brand-intake-interview.md`; inspect any supplied `brand identity.txt`, logo, guidelines, copy, and project files first. Reuse facts already provided, ask only missing or conflicting high-impact details, and confirm a concise brand summary before producing prompts. Wait for approval before project-specific web/image research or output unless that exact scope is already approved. When the user says “Let's brand,” do not paste prompts or long design details in chat: ask questions, confirm the brief, then put the prompt set in `prompts.md`. Never write a logo, mockup, poster, story, guideline, or presentation prompt without a locked brief for its required inputs.
3. **Follow the project folder convention** so every skill can find what the others produced:
   ```
   /project-name/
     AGENTS.md                   ← project-specific instructions, if supplied
     brand identity.txt          ← approved identity; create only if absent
     prompts.md                  ← all requested, ready-to-paste prompts
     /assets/
       /logo/                    ← approved logo
       /mockups/                 ← approved mockups
     /output/
       brand-presentation.html
       banners/
   ```
   If `brand identity.txt` already exists, read and preserve it; do not create a duplicate or overwrite it. If `prompts.md` exists, preserve unrelated approved prompt content and update only requested sections.
4. **Confirm before moving to the next stage.** Don't silently chain identity → logo → mockups → presentation without showing the user each stage's result — this is explicitly how `lets-brand` is designed to work.
5. **Respect every "Hard Rules" / "Non-negotiables" section** in each skill's `SKILL.md` — these exist because of real, observed failure cases (see especially `logo-prompting/references/common-pitfalls.md`), not generic caution.

### New-logo sequence

- If no approved logo exists, run `logo-guidelines` first in pre-design mode. Open at least five relevant direct project pages and visually inspect their actual logo/guideline images before recommending a direction. Share the concise research-based direction and wait for approval.
- After that approval, run `logo-design` and ask at least five or six unanswered logo-specific questions. Reuse the identity brief and do not repeat settled intake questions. If the user wants only lettering, use `logo-text` after confirming that route.
- `logo-colors` uses only approved palette HEX values. `logo-pattern` requires an approved logo source and must derive from its real geometry. Both are optional modules and need user selection/approval.
- If an approved logo already exists, do not start a new-concept workflow unless requested. `logo-guidelines` can document actual usage rules from the authoritative file, but must not invent dimensions or variants.

### Research and skill routing

- Every design-facing skill must research at least five distinct, relevant real projects and inspect the actual images before finalizing a direction or prompt. Read that skill's `references/reference.md` for its research focus, log observations and originality boundaries, and distinguish facts from interpretation. Search previews and library descriptions alone are not visual inspection. Follow `agent-reach` and stop on platform/login/rate-limit blocks. Mockup prompts retain the additional five-global plus five-Arabic requirement.
- Each `references/reference.md` routes decisions to the correct next skill. A text-only logo goes to `logo-text`; a new symbol/combination goes through `logo-guidelines` then `logo-design`; an existing-mark revision goes to `logo-prompting`; a missing palette returns to `brand-identity`; a pattern requires an approved mark.

## Output constraints that apply across the whole collection

- All deliverable code is standalone HTML/CSS/vanilla JS — no frameworks, no build step, single file per page, opens by double-click.
- All AI image-generation prompts must use exact hex codes from the locked brief, never vague color language.
- Any prompt involving a real-world setting (storefront, street, person) must state the country/region explicitly.
- Ask before inventing a missing detail (a color, a name, a mockup type) — never fill a gap with a guess that might ship to a real client unnoticed.
- Ask which prompt modules are needed: logo concept/refinement, name-only wordmark, logo color variants, logo-derived pattern, visual logo guidelines, mockups, posters/campaigns, story-led visuals, HTML presentation build prompt, or written guideline prompt. Include only relevant deliverables.
- For every prompt pack, specify exact supplied files to attach, exact approved Arabic/Latin spelling, composition and hierarchy, image ratio/placement, exclusions, and a quality check. If text rendering is unreliable, leave clean space for manual typesetting.
- Do not execute a prompt, generate an image, write HTML, or save a prompt pack unless the user asks for that artifact or file. Prompt requests default to copy-ready text.
- Exact brand colors in AI image prompts come from the locked brief. Keep unapproved colors and text as open decisions.
- Treat a complete identity as one coherent system, not a loose list of attractive choices. Connect logo, palette, type hierarchy, graphic language, imagery, voice, and applications to the same approved positioning. For “premium,” clarify the intended tier and value cues; do not default to black, gold, or luxury clichés. Use `skills/brand-identity/references/identity-system-framework.md`, including its cosmetics module when applicable.
- Every mockup prompt must name the exact approved logo image and instruct the image tool to use the uploaded file as the visible logo reference. Name the attached palette/design-system board as its visual reference when supplied, and repeat exact HEX values and roles in text. Name the role of each product/package reference. If the logo or a required design decision is missing, ask or keep the prompt provisional; never silently output a generic/unbranded mockup as final.
- Check current official platform or printer specifications before exporting banners or print files; the reference tables are starting points only.
- When research is requested, use `skills/shared-references/visual-analysis-workflow.md` to log direct sources, distinguish observation from interpretation, and count distinct projects.
- For a new logo, wordmark, or logo-guideline direction, read `skills/shared-references/logo-design-reference-library.md`, choose at least five relevant distinct projects, open the direct source pages, and visually inspect their actual logo images before finalizing a direction or prompt. A search preview or library description alone is not visual inspection. Follow `agent-reach` and stop on platform/login/rate-limit blocks.
- For mockup prompts and full prompt packs that include mockups, inspect at least five distinct global references and five distinct Arabic-market references from the two libraries. Open each source URL and visually inspect the actual case-study images; a title, text summary, or thumbnail alone does not count. Follow the `agent-reach` skill when accessing reference URLs and obey its read-only, login, rate-limit, and platform-block rules.
- Add the exact note `NOTE: Use the Agent Reach skill to access and visually inspect the reference URLs before finalizing these prompts.` to `prompts.md` when visual access is unavailable; identify inaccessible links and do not claim the scan is complete.
- For the full `Let's brand` workflow, create `brand identity.txt` only if absent, include the locked palette as exact hex values with roles, and write all requested prompt modules to `prompts.md`. Do not paste those prompts into chat; give a concise file-status note after creation.

See `README.md` for install locations per agent and more usage examples.

`skills/shared-references/` is a common resource folder, not a skill. Keep it beside all twelve skill folders so cross-skill links resolve. It contains libraries with 60 diverse global projects, 50 Arabic-market Behance projects, and 27 logo, wordmark, pattern, and guideline projects, plus the intake interview, prompt-pack template, and research method. Use the examples to understand design methods; do not copy distinctive artwork, and mark portfolio/concept work as such. A scheduled weekly audit prepares proposals only: do not add, remove, or rewrite canonical reference entries until a maintainer reviews the proposal. A 403 or login wall is not proof that a link is dead; distinguish access blocks from confirmed missing pages.
