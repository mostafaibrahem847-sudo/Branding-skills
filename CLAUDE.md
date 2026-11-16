# CLAUDE.md — Branding Skills Collection

This project uses the `branding-skills/` collection: 12 skills for an interview-first, prompt-first workflow spanning identity → logo research/concepting → mockups → posters/campaigns → HTML presentation → visual/written guidelines. Build images or HTML only when the user explicitly asks for the artifact.

The `skills/shared-references/` folder contains 60 global brand references, 50 Arabic-market references, 27 logo/wordmark/pattern/guideline references, a mandatory intake interview, a reusable prompt-pack template, and a visual-analysis method used by all twelve skills. The Arabic-market set has an Egyptian majority. Shared references are resources, not a thirteenth skill. Keep them beside all twelve skill folders when installing or linking the collection.

## Setup check

These are written as Claude Code skills (`SKILL.md` with frontmatter, `references/`, and optional `templates/`). For the `Skill` tool to list and invoke them by name, this folder's 12 skill subfolders need to live under a skills directory Claude Code actually scans:
- Project-level: `.claude/skills/`
- Global (all projects): `~/.claude/skills/`

If they're sitting here instead (e.g. this exact `branding-skills/skills/` folder at the project root, not yet moved into `.claude/skills/`), copy each of the 12 skill folders plus `shared-references/` so they appear as siblings inside `.claude/skills/`. The `README.md`, `AGENTS.md`, and `CLAUDE.md` at this folder's root are not skills themselves and don't need moving.

Once installed, invoke them with the `Skill` tool by name (e.g. `Skill(skill: "lets-brand")`), or just respond naturally to a branding request — the skill descriptions in each `SKILL.md`'s frontmatter are written to match how Mostafa actually asks for this work ("let's brand [name]", "اديني برومبتات لوجو", "اعمل الصفحة بتاعة البراند").

## If the skills aren't installed yet in this session

Read `skills/lets-brand/SKILL.md` directly from this folder and follow it as plain instructions — the content works identically whether it's loaded through the `Skill` tool or read directly as a file; only the lookup mechanism differs.

## Working conventions for this collection

- **Sub-skills reference each other and shared research by relative path** (`../brand-identity`, `../shared-references`, etc.) — these links resolve only when all 12 skill folders and `shared-references/` stay as siblings under the same skills directory. Don't move or rename them independently.
- **Always interview and audit before output.** Read `skills/shared-references/brand-intake-interview.md`, inspect the supplied brief/logo/guidelines/files, reuse confirmed facts, ask only about gaps or contradictions, and confirm the concise brand summary before writing prompts. Every output needs the required values from a locked brief.
- **Prompt-only is the default.** Return detailed, copy-ready prompts for the user's image generator or coding agent. Creating images, HTML, written guidelines, or files requires an explicit request for that artifact.
- **Confirm each stage with Mostafa before moving to the next one** when running the full `lets-brand` pipeline — don't chain identity → logo → mockups → presentation silently in one pass.
- **For a new logo, start with research.** Run `logo-guidelines` in pre-design mode, open and visually inspect at least five relevant direct project pages, present the concise logo direction, and wait for approval. Then `logo-design` asks at least five or six unanswered logo-specific questions before creating a concept prompt; use `logo-text` for an approved name-only route. `logo-colors` needs the locked palette; `logo-pattern` needs an approved logo master.
- **Treat each skill's "Hard Rules" / "Non-negotiables" section as binding**, not optional style advice — most of them encode a specific real failure already seen (garbled Arabic letters fused into shapes, mismatched storefront geography, cinematic photography clashing with a flat logo, etc.). `logo-prompting/references/common-pitfalls.md` has the fullest list.
- **Use reference work as study, not raw prompt material.** Log direct sources and transferable methods, mark conceptual portfolio cases, and do not copy logos, palettes, distinctive graphics, or compositions.
- **Verify volatile delivery specs.** Check current official platform or print-vendor requirements before exporting a banner or print-ready file.
- **When the user explicitly requests HTML execution** for `brand-presentation` or `banner-design`, output standalone HTML/CSS/vanilla JS — no React, no Tailwind CDN, no build step. Otherwise provide a detailed implementation prompt that names the approved assets, content, responsive behavior, accessibility needs, and review steps.

## Project folder convention

```
/project-name/
  AGENTS.md                   ← project-specific instructions, if supplied
  brand identity.txt          ← approved identity; create only if absent
  prompts.md                  ← all requested ready-to-paste prompts
  /assets/
    /logo/                    ← approved logo, from logo-design or logo-text
    /mockups/                 ← approved mockups, from mockup-prompting
  /output/
    brand-presentation.html   ← from brand-presentation
    banners/                  ← from banner-design, if used
```

See `README.md` for the full collection overview and per-agent install notes (this file covers Claude Code specifically; `AGENTS.md` covers the collection generically for other agents like Cursor or Codex CLI).
