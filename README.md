<div align="center">

# 🎨 Branding Skills

### An interview-first branding workflow for AI coding agents

Create a clear brand brief, then turn it into detailed, production-ready prompts for logos, mockups, campaigns, visual guidelines, and presentations.

[![Agent Ready](https://img.shields.io/badge/AI_Agent-Ready-6C5CE7?style=for-the-badge)](#supported-agents)
[![Markdown](https://img.shields.io/badge/Format-Markdown-2563EB?style=for-the-badge&logo=markdown&logoColor=white)](#the-seven-skills)
[![Arabic Research](https://img.shields.io/badge/Research-Arabic_Market-00856A?style=for-the-badge)](#reference-libraries)
[![npm version](https://img.shields.io/npm/v/branding-skills?style=for-the-badge)](https://www.npmjs.com/package/branding-skills)

</div>

---

## Overview

Branding Skills is a collection of seven reusable skills for Codex, Claude Code, and other agents that can read Markdown. It helps an agent understand a brand before preparing detailed prompts for image-generation tools or coding agents.

> **Prompt-first by design:** the default deliverable is a copy-ready prompt pack. The agent creates images, builds the HTML presentation, or writes a complete guidelines document only when you ask for that deliverable.

## Why use it

- 🧭 **Start with the brief:** review the logo, files, existing guidelines, approved copy, and project context before asking questions.
- 💬 **Ask useful questions:** resolve only the missing details that could change the work.
- 🔒 **Lock the direction:** confirm one concise brand brief before writing production prompts.
- ✍️ **Get detailed prompts:** specify assets, composition, exact colors, typography direction, format, exclusions, and quality checks.
- 🤝 **Keep the user in control:** review each stage before continuing to another deliverable.
- 🌍 **Use relevant references:** draw on global and Arabic-market case studies without copying another brand's work.

## Supported agents

The skills are plain Markdown instruction sets. They can be used by any coding agent that can read local Markdown files. The workflows are written with **Codex** and **Claude Code** in mind.

## Installation

### Use from GitHub

```bash
git clone https://github.com/mostafaibrahem847-sudo/Branding-skills.git
```

Open the cloned folder in your coding agent and ask it to follow [`skills/lets-brand/SKILL.md`](skills/lets-brand/SKILL.md). For a single deliverable, open the matching skill listed below.

Claude Code users can copy the skills into the project-level discovery folder. Keep `shared-references/` beside the seven skill folders so their relative links continue to work.

```powershell
New-Item -ItemType Directory -Force .claude/skills | Out-Null
Copy-Item skills/* .claude/skills/ -Recurse -Force
```

### Install from npm

Run these commands from the root of the project where you want to use the skills—not from the `branding-skills` source repository:

```bash
npm i branding-skills
npx skills add https://github.com/mostafaibrahem847-sudo/Branding-skills
```

The first command installs `branding-skills`. The second runs the Skills CLI and registers the package's skills with detected agents. The npm-package sync workflow is currently experimental; see the [Skills CLI reference](https://github.com/vercel-labs/skills/blob/main/docs/commands.md).

`skills/` is a folder inside the `branding-skills` package, not a separate npm package. Install `branding-skills`, then let the Skills CLI discover and link its skills.

## Workflow

1. **Audit** the existing logo, brief, assets, guidelines, approved copy, and previous decisions.
2. **Interview** the user about decision-critical gaps: offer, market, audience, brand story, language and dialect, colors, assets, channels, and desired deliverables.
3. **Confirm** a concise brand summary. Reuse known facts; do not ask the user to repeat them.
4. **Prepare** only the requested prompts, grounded in the approved brief and available assets.
5. **Review** each prompt or result with the user before moving to another production stage.

The workflow does not invent names, claims, colors, copy, mockup types, or cultural details. If an unknown detail could materially change the result, the agent asks before proceeding.

## The seven skills

| Skill | What it does |
|---|---|
| [`lets-brand`](skills/lets-brand/SKILL.md) | Leads the interview, locks the brief, and assembles the requested prompt pack. |
| [`brand-identity`](skills/brand-identity/SKILL.md) | Builds a clear identity brief from the brand story, audience, and visual direction. |
| [`logo-prompting`](skills/logo-prompting/SKILL.md) | Writes prompts for logo concepts, refinement, and visual logo-guideline boards. |
| [`mockup-prompting`](skills/mockup-prompting/SKILL.md) | Plans relevant physical, product, and digital touchpoints and writes their prompts. |
| [`brand-presentation`](skills/brand-presentation/SKILL.md) | Prepares a coding-agent prompt for a standalone HTML brand presentation. |
| [`banner-design`](skills/banner-design/SKILL.md) | Creates prompts for posters, launches, social posts, ads, and web heroes. |
| [`brand-guidelines-doc`](skills/brand-guidelines-doc/SKILL.md) | Prepares prompts for a practical written guide or visual guidelines board. |

The [`shared-references`](skills/shared-references/) folder supports these skills. It is a shared resource, not an additional skill.

## Prompt deliverables

Choose only the materials relevant to the brand and project:

- Logo concept, refinement, and usage-board prompts.
- Product, packaging, retail, and digital mockup prompts.
- Campaign, launch, event, and story-led poster prompts.
- Social, advertising, and website-hero visual prompts.
- Brand-story prompts based only on user-approved facts.
- Written brand-guidelines prompts.
- A detailed coding-agent prompt for a responsive, standalone HTML presentation.

### Prompt quality standards

- Use exact approved hex values and approved spelling from the locked brief.
- Name the country or region for any real-world setting, person, or location.
- Attach the approved logo and reference assets when the image tool supports them.
- If a generator may distort Arabic lettering or the supplied logo, reserve clean space for the real assets to be added afterward.
- State composition, subject, lighting, camera angle, hierarchy, materials, output dimensions, exclusions, and review criteria when relevant.

## Reference libraries

- [Brand Design Reference Library](skills/shared-references/brand-design-reference-library.md) — 60 general brand-design precedents.
- [Arabic Brand Design Reference Library](skills/shared-references/arabic-brand-design-reference-library.md) — 50 Arabic-market projects: 36 Egypt-centered examples and 14 from Saudi Arabia, the UAE, and Lebanon.
- [Visual Analysis Workflow](skills/shared-references/visual-analysis-workflow.md) — a method for checking sources and separating observation from interpretation.

Some references are self-published, conceptual, or unclear about launch status. The libraries label known uncertainty and link to public case pages. Use references to study design methods; do not copy another brand's logo, palette, typeface, illustration, layout, or signature device.

## Recommended project structure

```text
project-name/
├── AGENTS.md or brief.md          # approved brand brief
├── assets/
│   ├── logo/                      # approved logo files
│   └── mockups/                   # user-approved mockup images
└── output/
    ├── prompts/                   # prompt packs, when requested
    ├── brand-presentation.html    # standalone HTML, when requested
    └── banners/                   # campaign exports, when requested
```

## Package details

- **Package:** `branding-skills`
- **Format:** Markdown instructions and references
- **Runtime dependencies:** none
- **Build step:** none
- **Repository:** [mostafaibrahem847-sudo/Branding-skills](https://github.com/mostafaibrahem847-sudo/Branding-skills)

The published `1.0.0` package currently has no license declared in `package.json`. Add the selected SPDX license before a future release. The skills include adapted material credited in their files, so make sure the chosen license covers the complete collection.

## Maintainer release

This section is for maintainers publishing future npm versions. End users installing the skills can skip it. Increment the package version and complete the metadata before publishing from the package root:

```bash
npm login --auth-type=web
npm whoami
npm publish
```

The package name is unscoped, so npm publishes it publicly. See [npm's unscoped package publishing guide](https://docs.npmjs.com/creating-and-publishing-unscoped-public-packages/).

---

<div align="center">

**Build a stronger brand brief. Create better prompts. Keep every decision grounded in the brand.**

</div>
