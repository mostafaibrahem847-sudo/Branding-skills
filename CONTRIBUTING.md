# Contributing to Branding Skills

Thanks for considering a contribution. This project is a collection of plain-Markdown skills (`SKILL.md` + `references/`) for AI coding agents (Codex, Claude Code, and similar). There is no build step and no runtime dependency — contributions are mostly writing/editing Markdown carefully.

## Ways to contribute

- **Fix or improve a skill's `SKILL.md`** — clearer workflow steps, missing edge cases, better rules.
- **Add or correct a reference file** (`references/*.md`) — a new mockup pattern, a corrected prompt pattern, a documented failure case.
- **Propose a new reference-library entry** (in `skills/shared-references/`) — see the rules below; this is the most sensitive category.
- **Report a bug in the workflow** — a skill that gives bad instructions, a broken relative link between skills, a prompt pattern that reliably produces bad output.
- **Improve the docs** — `README.md`, `AGENTS.md`, `CLAUDE.md`, or this file.

## Before you open a pull request

1. **Open an issue first** for anything beyond a small typo fix, so the change can be discussed before work is done on it.
2. **Keep the skill folder structure intact.** Every skill folder needs a `SKILL.md` with valid frontmatter (`name`, `description`, at minimum). Sub-skills reference each other and `shared-references/` by relative path (`../brand-identity`, `../shared-references`) — don't rename or move a skill folder without updating every file that links to it.
3. **Test your change against a real (or fake-client) brand project** before submitting — run the skill as instructed and confirm the output still makes sense end to end.

## Adding to the reference libraries

The `skills/shared-references/` libraries (global brand references, Arabic-market references, logo references) are curated, not a dumping ground. Before adding an entry:

- Link directly to the real project page (Behance, Dribbble, the brand's own site) — not a search result, a thumbnail, or a secondhand screenshot.
- Confirm you (or the agent reviewing the PR) can actually open and visually inspect the images at that link — a dead link or a login-walled page doesn't qualify.
- Note the market/sector and whether the project is a shipped brand or a concept/portfolio piece — label uncertainty honestly rather than guessing.
- **Never submit an entry, example, or prompt that reproduces another brand's actual logo, wordmark, color system, or distinctive visual device as if it were original work.** References exist to study method, not to copy output. See `skills/shared-references/research-reference-standard.md` for the full standard this project already follows.

Significant additions or removals to the canonical libraries (keeping the global library at 60 entries, the Arabic-market library at 50 entries) should be proposed as a report in the PR description for the maintainer to review — not pushed directly.

## Style for `SKILL.md` and reference files

- Write instructions as direct, actionable rules an agent can follow — not vague advice.
- Where a rule exists because of an observed failure (a specific prompt that produced bad output), say so briefly — it helps future contributors understand why the rule is there instead of "softening" it away later.
- Keep frontmatter (`name`, `description`, `argument-hint`, `metadata`) consistent with the existing skills' format.

## Reporting a security or privacy concern

Don't open a public issue for anything sensitive — see `SECURITY.md`.

## Code of Conduct

Participation in this project is governed by `CODE_OF_CONDUCT.md`.
