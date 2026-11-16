<div align="center">

# 🎨 Branding Skills

### An interview-first branding workflow for AI agents

Create a clear brand brief, then turn it into detailed, production-ready prompts for logos, mockups, campaigns, visual guidelines, and presentations.

[![Agent Ready](https://img.shields.io/badge/AI_Agent-Ready-6C5CE7?style=for-the-badge)](#supported-agents)
[![Markdown](https://img.shields.io/badge/Format-Markdown-2563EB?style=for-the-badge&logo=markdown&logoColor=white)](#the-twelve-skills)
[![Arabic Research](https://img.shields.io/badge/Research-Arabic_Market-00856A?style=for-the-badge)](#reference-libraries)
[![npm version](https://img.shields.io/npm/v/branding-skills?style=for-the-badge)](https://www.npmjs.com/package/branding-skills)

</div>

---

## Overview

Branding Skills is a collection of twelve reusable skills for Codex, Claude Code, and other agents that can read Markdown. It interviews the user, locks the brand brief, researches real visual references, and prepares detailed prompts for image-generation tools or coding agents.

> **File-first by design:** during “Let's brand,” the agent asks questions and confirms the brief in chat, then writes `brand identity.txt` only if it is missing and saves all requested prompts in `prompts.md`. It does not paste the prompt pack into chat. Images, HTML, and guideline documents are created only when you explicitly request those artifacts.

## Why use it

- 🧭 **Start with the brief:** review the logo, files, existing guidelines, approved copy, and project context before asking questions.
- 💬 **Ask useful questions:** resolve only the missing details that could change the work.
- 🔒 **Lock the direction:** confirm one concise brand brief before writing production prompts.
- 🧩 **Build one coherent identity system:** connect positioning, logo, exact palette roles, typography, graphic language, imagery, voice, and real applications; define premium behavior from the brand's audience and tier instead of relying on generic luxury clichés.
- ✍️ **Get detailed prompts:** specify assets, composition, exact colors, typography direction, format, exclusions, and quality checks.
- 🖼️ **Bind mockups to real assets:** name the exact logo, palette/system board, and product files to upload, and tell image tools how to use each reference.
- 🤝 **Keep the user in control:** review each stage before continuing to another deliverable.
- 🌍 **Use relevant references:** draw on global and Arabic-market case studies without copying another brand's work.
- 🔠 **Handle logo work as a system:** research logo precedents first, ask logo-specific questions before concept prompts, and support wordmarks, exact-color variants, and logo-derived patterns.

## Supported agents

The skills are plain Markdown instruction sets. They can be used by any coding agent that can read local Markdown files. The workflows are written with **Codex** and **Claude Code** in mind.

## Installation

### Use from GitHub

```bash
git clone https://github.com/mostafaibrahem847-sudo/Branding-skills.git
```

Open the cloned folder in your coding agent and ask it to follow [`skills/lets-brand/SKILL.md`](skills/lets-brand/SKILL.md). For a single deliverable, open the matching skill listed below.

Claude Code users can copy the skills into the project-level discovery folder. Keep `shared-references/` beside all twelve skill folders so their relative links continue to work.

```powershell
New-Item -ItemType Directory -Force .claude/skills | Out-Null
Copy-Item skills/* .claude/skills/ -Recurse -Force
```

### Install from npm

Run these commands from the root of the project where you want to use the skills—not from the `branding-skills` source repository:

```bash
npm i branding-skills
```
```bash
npx skills add https://github.com/mostafaibrahem847-sudo/Branding-skills
```
The first command installs `branding-skills`. The second runs the Skills CLI and registers the package's skills with detected agents. The npm-package sync workflow is currently experimental; see the [Skills CLI reference](https://github.com/vercel-labs/skills/blob/main/docs/commands.md).

`skills/` is a folder inside the `branding-skills` package, not a separate npm package. Install `branding-skills`, then let the Skills CLI discover and link its skills.

To update an existing installation to the newest published version, run this from the consuming project root:

```bash
npm i branding-skills
npx skills add https://github.com/mostafaibrahem847-sudo/Branding-skills
```

## Workflow

1. **Audit** `brand identity.txt`, the existing logo, assets, guidelines, approved copy, and previous decisions.
2. **Interview** the user about decision-critical gaps: offer, market, audience, brand story, language and dialect, colors, assets, channels, and desired deliverables.
3. **Confirm** a concise brand summary. Reuse known facts; do not ask the user to repeat them.
4. **Create the identity file only if missing.** Preserve an existing `brand identity.txt`; after approval, create it only when absent, including the exact approved colors and their roles.
5. **Research before prompts.** For a new logo, inspect at least five relevant logo project pages and their actual logo images. For mockup work, inspect five distinct global and five distinct Arabic-market projects. Follow Agent Reach access rules; report anything that could not be visually checked.
6. **Write `prompts.md`.** Put every requested prompt in this file, with source links and observations. Keep prompt contents out of chat.

The workflow does not invent names, claims, colors, copy, mockup types, or cultural details. If an unknown detail could materially change the result, the agent asks before proceeding. If reference images cannot be accessed, the agent adds the note `NOTE: Use the Agent Reach skill to access and visually inspect the reference URLs before finalizing these prompts.` and identifies what remains unverified.

### New logo workflow

When no approved logo exists, run [`logo-guidelines`](skills/logo-guidelines/SKILL.md) first. It researches direct project pages and produces a user-reviewable logo direction guide. After approval, [`logo-design`](skills/logo-design/SKILL.md) asks at least five or six unanswered logo decisions and prepares the concept prompt. Route a name-only logo to [`logo-text`](skills/logo-text/SKILL.md). Add [`logo-colors`](skills/logo-colors/SKILL.md) only for approved palette variants and [`logo-pattern`](skills/logo-pattern/SKILL.md) only after a logo is approved. Existing-logo usage guidance stays in `logo-guidelines` post-design mode.

## The twelve skills

| Skill | What it does |
|---|---|
| [`lets-brand`](skills/lets-brand/SKILL.md) | Leads the interview, protects the identity file, researches references, and writes the prompt pack. |
| [`brand-identity`](skills/brand-identity/SKILL.md) | Builds the approved strategy and coherent identity system, including exact palette roles, in `brand identity.txt` when absent. |
| [`logo-guidelines`](skills/logo-guidelines/SKILL.md) | Researches logo precedents and sets the pre-design direction; documents verified use rules for an approved mark. |
| [`logo-design`](skills/logo-design/SKILL.md) | Interviews for logo-specific decisions and writes one focused, original logo-concept prompt. |
| [`logo-text`](skills/logo-text/SKILL.md) | Creates language-aware prompts for Arabic, Latin, or bilingual text-only wordmarks. |
| [`logo-colors`](skills/logo-colors/SKILL.md) | Specifies approved full-color, monochrome, reverse, and contrast-tested logo variants. |
| [`logo-pattern`](skills/logo-pattern/SKILL.md) | Derives a repeatable secondary pattern from an approved logo's actual geometry. |
| [`logo-prompting`](skills/logo-prompting/SKILL.md) | Refines existing logo files or repairs a failed AI logo prompt. |
| [`mockup-prompting`](skills/mockup-prompting/SKILL.md) | Visually researches global and Arabic case studies, then writes asset-bound prompts that use the approved logo, palette/system, and real product references. |
| [`brand-presentation`](skills/brand-presentation/SKILL.md) | Prepares a coding-agent prompt for a standalone HTML brand presentation. |
| [`banner-design`](skills/banner-design/SKILL.md) | Creates prompts for posters, launches, social posts, ads, and web heroes. |
| [`brand-guidelines-doc`](skills/brand-guidelines-doc/SKILL.md) | Prepares prompts for a practical written guide or visual guidelines board. |

The [`shared-references`](skills/shared-references/) folder supports these skills. It is a shared resource, not an additional skill.

## Prompt deliverables

Choose only the materials relevant to the brand and project:

- Research-based logo direction guidelines, logo concepts, and existing-mark revisions.
- Text-only Arabic, Latin, or bilingual wordmark prompts.
- Logo color-variant and logo-derived pattern prompts, based on approved assets and palette values.
- Product, packaging, retail, and digital mockup prompts.
- Campaign, launch, event, and story-led poster prompts.
- Social, advertising, and website-hero visual prompts.
- Brand-story prompts based only on user-approved facts.
- Written brand-guidelines prompts.
- A detailed coding-agent prompt for a responsive, standalone HTML presentation.

### Prompt quality standards

- Use exact approved hex values and approved spelling from the locked brief.
- Name the country or region for any real-world setting, person, or location.
- Name and attach the approved logo and palette/design-system references in each mockup prompt; state what each uploaded file should control.
- If a generator may distort Arabic lettering or the supplied logo, use an image-editing/compositing step or reserve a clearly provisional placement area for the exact supplied asset. Do not present a missing or fabricated logo as the finished brand mockup.
- State composition, subject, lighting, camera angle, hierarchy, materials, output dimensions, exclusions, and review criteria when relevant.

## Reference libraries

- [Logo Design Reference Library](skills/shared-references/logo-design-reference-library.md) — 27 distinct project pages for logo design, Arabic/Latin wordmarks, logo patterns, colors, and guidelines. Preview notes are discovery aids; the agent must open the direct source and inspect actual images for the current task.
- [Brand Design Reference Library](skills/shared-references/brand-design-reference-library.md) — 60 global brand-design precedents selected across varied sectors.
- [Arabic Brand Design Reference Library](skills/shared-references/arabic-brand-design-reference-library.md) — 50 Behance project pages for Arabic-market references: 40 Egypt-focused, 9 Saudi-market, and 1 Qatar event identity, across varied sectors.
- [Visual Analysis Workflow](skills/shared-references/visual-analysis-workflow.md) — a method for checking sources and separating observation from interpretation.
- [Research Reference Standard](skills/shared-references/research-reference-standard.md) — shared question-gating, image research, analysis, prompt synthesis, and skill routing required by all skills.
- [Reference Library Audit](skills/shared-references/reference-library-audit.md) — current counts, source-access limits, and research-quality notes for the latest snapshot.
- [Complete Brand System Framework](skills/brand-identity/references/identity-system-framework.md) — strategy-to-design-system completeness, premium positioning, and beauty/cosmetics identity checks.

Every design-facing skill must inspect at least **five distinct, relevant project images** before finalizing a direction or prompt. For mockup work, it must also inspect at least **five global and five Arabic-market projects**. Each skill has a required `references/reference.md` explaining its interview gate, research focus, and routing decisions; read it with the shared research standard before work. Ask only missing, high-impact questions and wait for approval before project-specific research unless the same scope is already approved. Record direct links, observations, visual-inspection status, transferable methods, and what must not be copied in `prompts.md`. Search snippets, titles, thumbnails, and text-only summaries do not count as direct image inspection. Follow the `agent-reach` skill for public source access; if images remain unavailable, add the Agent Reach note above and mark affected prompts provisional.

The Agent Reach skill is a companion capability and may not be installed in every agent environment. When it is unavailable, the agent may use its native read-only web and visual tools. If it still cannot open and inspect the source images, it must report that limitation instead of claiming the reference scan is complete.

Some references are self-published, conceptual, or unclear about launch status. The libraries label known uncertainty and link to public case pages. Use references to study design methods; do not copy another brand's logo, palette, typeface, illustration, layout, or signature device.

## Reference maintenance

The reference libraries are reviewed weekly. A scheduled review prepares a proposed additions/removals report for a maintainer to review; it must not edit the canonical libraries or commit changes before approval. Keep the general library at 60 diverse projects and the Arabic-market library at 50 unique Behance project pages. Prefer a broad sector mix, with the Arabic set led by Egyptian and other Arab-market work. Check the canonical project page and its market/category before proposing an entry, classify concept/client status only as far as the source supports, and distinguish a genuine missing page from a 403, login wall, or temporary network block. For visual claims, open and inspect the actual project images with Agent Reach; search results and text snippets do not count as visual inspection.

## Recommended project structure

```text
project-name/
├── AGENTS.md                      # project instructions, if needed
├── brand identity.txt             # approved identity; create only if absent
├── prompts.md                     # requested prompt pack; no prompts pasted in chat
├── assets/
│   ├── logo/                      # approved logo files
│   └── mockups/                   # user-approved mockup images
└── output/
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


---

<div align="center">

**Build a stronger brand brief. Create better prompts. Keep every decision grounded in the brand.**

</div>
