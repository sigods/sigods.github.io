---
name: write-post
description: Front matter template and body structure for posts in this blog. Use whenever creating or editing a file in src/content/blog/.
---

# Writing a post

1. Read `src/content.config.ts` for the live front matter schema. If this file and
   the schema disagree, the schema wins.
2. Create `src/content/blog/<kebab-slug>.md`.
3. Body structure:
   - Opening paragraph on one concrete detail: a log line, a number, a wrong guess.
   - What was expected vs. what happened.
   - The trace, quoted verbatim. Never paraphrased.
   - The fix, and how it was confirmed.
   - `## Sources` with links to commits and issues.
4. No post ships without at least one primary source.
