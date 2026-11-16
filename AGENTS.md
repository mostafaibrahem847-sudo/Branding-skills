# AGENTS.md — Branding Skills Collection

This folder (`branding-skills/`) is a set of 7 skills for an interview-first, prompt-first branding workflow — identity → logo → mockups → posters/campaigns → HTML presentation → visual/written guidelines. Build images or HTML only when the user explicitly asks for the artifact. You are an agent that has access to these files on disk. This file tells you how to use the collection.

## What a "skill" means here

Each skill folder under `skills/` is a self-contained instruction set: a `SKILL.md` (what it does, when to use it, its workflow and hard rules) plus a `references/` folder and sometimes `templates/`. These are plain Markdown files — there is no special runtime. **Reading a `SKILL.md` and its referenced files IS "activating" the skill.** When a skill's SKILL.md tells you to read `references/some-file.md` before doing something, actually read that file before proceeding — don't skip straight to generating output from the SKILL.md summary alone.

## The 7 skills

| Folder | Role |
|---|---|
| `lets-brand/` | Orchestrator — read this first when starting a new brand project or when asked to run the full pipeline |
| `brand-identity/` | Step 1 — the approved strategy and connected identity system (logo, palette, type, graphics, imagery, voice, and application rules) |
| `logo-prompting/` | Step 2 — AI logo-generation prompts, plus hard-won rules on what fails and why |
| `mockup-prompting/` | Step 3 — AI product/application mockup prompts, matched to business type and logo style |
| `brand-presentation/` | Step 4 — assembling everything into one single-page, Behance-style HTML file |
| `banner-design/` | Optional — social/ad/web-hero banners at correct platform sizes |
| `brand-guidelines-doc/` | Optional — a written guidelines document (voice, usage rules, checklists) |
| `shared-references/` | Shared resource — 60 general and 50 Arabic-market design references, intake interview, prompt-pack template, and visual-research method |

Full detail on each is in `README.md` and inside each skill's own `SKILL.md`.

The shared reference folder is not an eighth skill. Keep it alongside all seven skill folders so cross-skill relative links resolve. Use its case studies to learn design methods, not to copy logos, palettes, typography, layouts, or signature graphics. Portfolio pages may be conceptual or self-published; label their status and do not claim verified commercial results unless the source proves them.

The default deliverable is a detailed prompt pack for the user's chosen image generator or coding agent. Do not assume the agent should generate images or execute an HTML prompt unless the user explicitly asks for those artifacts.

## How to behave when a branding request comes in

1. **Identify which stage is being asked for.** "Let's brand X" / "ابدأ مشروع براندينج" → load `skills/lets-brand/SKILL.md` and follow its staged workflow. A request for just one piece ("اديني برومبت لوجو", "اعمل الصفحة بتاعة البراند") → go straight to that skill's own `SKILL.md`.
2. **Interview and audit before output.** Read `skills/shared-references/brand-intake-interview.md`; inspect any supplied `brand identity.txt`, logo, guidelines, copy, and project files first. Reuse facts already provided, ask only missing or conflicting details, and confirm a concise brand summary before producing prompts. When the user says “Let's brand,” do not paste prompts or long design details in chat: ask questions, confirm the brief, then put the prompt set in `prompts.md`. Never write a logo, mockup, poster, story, guideline, or presentation prompt without a locked brief for its required inputs.
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

## Output constraints that apply across the whole collection

- All deliverable code is standalone HTML/CSS/vanilla JS — no frameworks, no build step, single file per page, opens by double-click.
- All AI image-generation prompts must use exact hex codes from the locked brief, never vague color language.
- Any prompt involving a real-world setting (storefront, street, person) must state the country/region explicitly.
- Ask before inventing a missing detail (a color, a name, a mockup type) — never fill a gap with a guess that might ship to a real client unnoticed.
- Ask which prompt modules are needed: logo or refinement, visual logo guidelines, mockups, posters/campaigns, story-led visuals, HTML presentation build prompt, or written guideline prompt. Include only relevant deliverables.
- For every prompt pack, specify exact supplied files to attach, exact approved Arabic/Latin spelling, composition and hierarchy, image ratio/placement, exclusions, and a quality check. If text rendering is unreliable, leave clean space for manual typesetting.
- Do not execute a prompt, generate an image, write HTML, or save a prompt pack unless the user asks for that artifact or file. Prompt requests default to copy-ready text.
- Exact brand colors in AI image prompts come from the locked brief. Keep unapproved colors and text as open decisions.
- Treat a complete identity as one coherent system, not a loose list of attractive choices. Connect logo, palette, type hierarchy, graphic language, imagery, voice, and applications to the same approved positioning. For “premium,” clarify the intended tier and value cues; do not default to black, gold, or luxury clichés. Use `skills/brand-identity/references/identity-system-framework.md`, including its cosmetics module when applicable.
- Every mockup prompt must name the exact approved logo image and instruct the image tool to use the uploaded file as the visible logo reference. Name the attached palette/design-system board as its visual reference when supplied, and repeat exact HEX values and roles in text. Name the role of each product/package reference. If the logo or a required design decision is missing, ask or keep the prompt provisional; never silently output a generic/unbranded mockup as final.
- Check current official platform or printer specifications before exporting banners or print files; the reference tables are starting points only.
- When research is requested, use `skills/shared-references/visual-analysis-workflow.md` to log direct sources, distinguish observation from interpretation, and count distinct projects.
- For mockup prompts and full prompt packs that include mockups, inspect at least five distinct global references and five distinct Arabic-market references from the two libraries. Open each source URL and visually inspect the actual case-study images; a title, text summary, or thumbnail alone does not count. Follow the `agent-reach` skill when accessing reference URLs and obey its read-only, login, rate-limit, and platform-block rules.
- Add the exact note `NOTE: Use the Agent Reach skill to access and visually inspect the reference URLs before finalizing these prompts.` to `prompts.md` when visual access is unavailable; identify inaccessible links and do not claim the scan is complete.
- For the full `Let's brand` workflow, create `brand identity.txt` only if absent, include the locked palette as exact hex values with roles, and write all requested prompt modules to `prompts.md`. Do not paste those prompts into chat; give a concise file-status note after creation.

See `README.md` for install locations per agent and more usage examples.

`skills/shared-references/` is a common resource folder, not an eighth skill. Keep it beside all seven skill folders so cross-skill links resolve. It contains two reference libraries with 60 general and 50 Arabic-market projects, plus the intake interview, prompt-pack template, and research method. Use the examples to understand design methods; do not copy distinctive artwork, and mark portfolio/concept work as such.
