# Project

Personal technical blog: reverse engineering, Linux, static recompilation.
Astro, fully static, deployed to GitHub Pages by `.github/workflows/deploy.yml`.

## Commands

- Dev: `npm run dev`
- Build (must pass before any PR): `npm run build`
- Check: `npx astro check`
- Dependencies are locked. Use `npm ci`, never change versions.

## Layout

- `src/content/blog/` — posts, one Markdown file each. Schema: `src/content.config.ts`
  (older scaffolds: `src/content/config.ts`). The schema wins over any prose rule.
- `src/components/`, `src/layouts/`, `src/pages/` — site code.
- Never commit `dist/`, `.astro/`, `node_modules/`.

## Style

- Plain HTML/CSS. No frameworks, no Tailwind, no CSS-in-JS.
- No client-side JS unless the feature is impossible without it. Every page must
  be readable with JavaScript disabled.
- Dark only: bg `#0d1117`, text `#e6edf3`, muted `#7d8590`. No theme toggle.
- No analytics, no trackers, no third-party fonts, no embeds. Images live in the repo.
- Highlighting is configured in `astro.config.mjs`. Don't change Shiki settings.

## Truth rules (highest priority)

- Never invent command output, memory addresses, register values, log lines,
  version numbers, or file offsets. If a fact is not in the repo or the issue,
  write `<!-- TODO(source): ... -->` and stop.
- Never write first-person claims about events that aren't documented in a commit
  or issue. "I spent three days" is a factual claim, not a rhetorical one.
- Every post ends with `## Sources` linking the commits and issues behind it.

## Tone

First person, past tense for what happened, present tense for what's true.
No "in this article", no "delve", no "ever-evolving", no closing summary that
restates the introduction. If a sentence could appear in any blog, delete it.
