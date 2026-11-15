# Branding Skills

**An interview-first, prompt-first branding workflow for Codex, Claude Code, and other agents that can read Markdown.** It helps an agent understand a brand, confirm the brief, and prepare detailed prompts for image-generation tools and coding agents.

> **بالعربي:** مجموعة مهارات تساعد الـagent يفهم البراند ويسأل عن التفاصيل الناقصة الأول، وبعدها يجهز prompts واضحة ومفصلة للّوجو والـmockups والبوسترات والـguidelines وصفحة العرض.

The default output is copy-ready prompts. The agent creates images, writes the HTML presentation, or produces a full guidelines document only when you explicitly ask it to create that deliverable.

## What you get

- A focused intake interview that checks your existing logo, brief, guidelines, approved copy, and project files before asking questions.
- One confirmed brand brief that acts as the source of truth for every selected prompt.
- Detailed prompts for logo concepts, mockups, campaign posters, social and ad banners, story-led visuals, visual logo-guidelines boards, written guidelines, and standalone HTML presentations.
- Arabic-market research resources, including a new library with an Egyptian-centered majority.
- Clear approval points between the brief and later production stages.

## Workflow

1. **Audit** the logo, brief, files, existing brand rules, and previous approvals.
2. **Interview** the user about decision-critical gaps: offer, market, audience, story, scripts and dialects, approved colors, assets, channels, and desired deliverables.
3. **Confirm** a concise brand summary. The agent reuses known facts and does not ask the user to repeat them.
4. **Prepare** only the requested prompts, with exact approved colors and copy, source assets to attach, composition, output format, exclusions, and quality checks.
5. **Review** each prompt or generated result with the user before moving to another production stage.

No prompt should invent missing names, claims, colors, mockup types, copy, or cultural details. If an input affects the result and is unknown, the agent asks first.

## Included skills

| Skill | Purpose |
|---|---|
| [`lets-brand`](skills/lets-brand/SKILL.md) | Runs the interview and assembles the selected prompt pack. |
| [`brand-identity`](skills/brand-identity/SKILL.md) | Audits and confirms the brand brief, story, audience, and visual direction. |
| [`logo-prompting`](skills/logo-prompting/SKILL.md) | Writes prompts for logo concepts, refinements, and visual logo-guideline boards. |
| [`mockup-prompting`](skills/mockup-prompting/SKILL.md) | Writes prompts for relevant product, physical, and digital touchpoints. |
| [`brand-presentation`](skills/brand-presentation/SKILL.md) | Writes a coding-agent prompt for a standalone HTML brand presentation; builds the file only on request. |
| [`banner-design`](skills/banner-design/SKILL.md) | Writes prompts for campaign posters, launch visuals, social and ad banners, and web heroes. |
| [`brand-guidelines-doc`](skills/brand-guidelines-doc/SKILL.md) | Writes prompts for a practical written brand guide and/or a visual guidelines board. |

The `skills/shared-references/` folder is a shared resource, not an eighth skill. Keep it alongside all seven skills so their relative references continue to work.

## Install and use

### Clone from GitHub

```bash
git clone https://github.com/mostafaibrahem847-sudo/Branding-skills.git
```

For Codex and other Markdown-capable agents, open the project and ask the agent to read `skills/lets-brand/SKILL.md` and follow its instructions. For a single stage, open that skill's `SKILL.md` directly.

For Claude Code skill discovery, copy the contents of `skills/`—including `shared-references/`—into the project's `.claude/skills/` directory. In PowerShell, from the repository root:

```powershell
New-Item -ItemType Directory -Force .claude/skills | Out-Null
Copy-Item skills/* .claude/skills/ -Recurse -Force
```

### Install from npm

The npm package name is not set or published yet. After the maintainer fills in `package.json`, chooses a license, and publishes the package, install it with the actual package name:

```bash
npm install --save-dev @YOUR_NPM_USERNAME/branding-skills
```

The package contains the Markdown skills under `node_modules/@YOUR_NPM_USERNAME/branding-skills/skills/`. To make them discoverable by Claude Code, copy those skill folders into `.claude/skills/` as shown above. Replace the placeholder scope with the final npm username or organization before publishing and updating this section.

## Start a branding session

Use the full workflow:

```text
Let's brand [brand name]. I already have [logo / brief / guidelines]. Read the existing files, interview me about missing details, confirm the brief, then prepare prompts for [selected deliverables].
```

Or ask for one stage:

```text
عندي براند قائم وعايز prompt للّوجو. راجع اللوجو والـbrief الأول، اسألني عن أي تفاصيل ناقصة، وبعد ما أأكد الملخص اكتبلي prompt جاهز.
```

For an existing brand, provide the logo and any available brief or brand guidelines. The agent should audit those files first, summarize what is confirmed, and ask only about missing or conflicting information.

## Prompt deliverables

Choose only the outputs relevant to your brand and current project:

- Logo concept or refinement prompts.
- Visual logo-guidelines board prompts and written brand-guidelines prompts.
- Mockup prompts for confirmed customer touchpoints.
- Product, launch, campaign, event, and story-led poster prompts.
- Social, advertising, and website-hero visual prompts.
- Story-to-visual prompts based only on user-approved facts.
- A detailed coding-agent prompt for a responsive, standalone HTML brand presentation.

Image prompts use the exact approved hex colors and spelling from the brief. When an image generator may distort Arabic text or the supplied logo, the prompt asks it to leave clean space for the user to typeset or composite the real assets afterward.

## Design reference libraries

- [Brand Design Reference Library](skills/shared-references/brand-design-reference-library.md): 60 general design precedents.
- [Arabic Brand Design Reference Library](skills/shared-references/arabic-brand-design-reference-library.md): 50 additional Arabic-market projects. Thirty-six are Egypt-centered—including one Egyptian-cuisine concept for a Greek market—and fourteen are from Saudi Arabia, the UAE, and Lebanon.
- [Visual Analysis Workflow](skills/shared-references/visual-analysis-workflow.md): a method for checking sources, separating observation from interpretation, and adapting design principles without copying work.

Portfolio references may be self-published, conceptual, or unclear about launch status. The libraries label known uncertainty and link to the original public case pages. Use them to study methods; do not copy a logo, palette, typeface, illustration, layout, or signature device.

## Project folder structure

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

## Package notes

This collection is made of Markdown instructions and references. It has no runtime dependencies or build step. The root `package.json` is a publishing template: fill the package name, description, author, repository URL, and license before publishing. The npm install command above uses a placeholder until the package has a final name and is publicly available.

The skills include adapted material as credited in their files. Choose and declare a license that covers the complete collection before redistributing it through npm.
