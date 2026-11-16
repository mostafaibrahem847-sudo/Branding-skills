# Security Policy

## About this project

`branding-skills` is a collection of plain-Markdown instruction files (`SKILL.md` + `references/`) for AI coding agents. It has no runtime dependencies, no server component, and no build step — the "attack surface" is limited mostly to:

- A reference link pointing somewhere unsafe or misleading
- Instructions in a skill file that could cause an agent to take an unsafe or unintended action
- Dependency risk from the npm package wrapper (`package.json`) itself

## Supported versions

Only the latest published version on npm (and the latest commit on the `main` branch) is supported with security fixes.

| Version | Supported |
|---|---|
| Latest (npm `branding-skills@latest`) | ✅ |
| Older published versions | ❌ |

## Reporting a vulnerability or concern

If you find:

- A reference link in `skills/shared-references/` that leads to something unsafe, malicious, or inappropriate
- Wording in a `SKILL.md` or `references/*.md` file that could cause an AI agent to take a harmful, unintended, or unsafe action
- A dependency or supply-chain issue in `package.json` / `package-lock.json`

Please **do not open a public GitHub issue** for it. Instead, report it privately via GitHub: open a [private security advisory](https://github.com/mostafaibrahem847-sudo/Branding-skills/security/advisories/new) on this repository, or contact the maintainer directly through their GitHub profile: [@mostafaibrahem847-sudo](https://github.com/mostafaibrahem847-sudo).

Please include:
- The affected file(s) and a link/line reference
- What the issue is and why it's a concern
- A suggested fix, if you have one

## Response

This is a solo-maintained project. There's no guaranteed response time, but security reports will be prioritized over regular feature requests and reviewed as soon as possible.

## Out of scope

- General bugs or quality issues with a skill's output (open a regular issue for these — see `CONTRIBUTING.md`)
- Disagreements over design/creative direction in a reference entry
