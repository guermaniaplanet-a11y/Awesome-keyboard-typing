# Instructions for Claude Code (owner: Adil)

## 1. Skills: use them automatically, never ask

This repository ships a full skill library in `.claude/skills/` (92 skills).
These rules are mandatory for every task in this repository:

1. Before starting ANY task, review the names and descriptions of all available
   skills (the ones in `.claude/skills/` AND the ones synced from the owner's
   claude.ai account).
2. Pick every skill that fits the task: one, several, or all of them. Read their
   SKILL.md and follow them.
3. Do NOT ask Adil which skill to use, and do NOT ask permission to use a skill.
   He asks for the work; the work gets done.
4. If no skill fits, do the task directly without mentioning it.

### Skill families available
- **Video / Shorts production**: `viral-story-engine`, `video`, `yt-*` (yt-script,
  yt-package, yt-edit, yt-comment, yt-plan, yt-viral, yt-retention, yt-shorts,
  yt-seo, yt-chapters, yt-audit). YouTube voice template: `.claude/templates/youtube/`.
- **Marketing / SEO / growth** (coreyhaines31/marketingskills): seo-audit, ai-seo,
  programmatic-seo, schema, site-architecture, link-building, copywriting,
  copy-editing, cro, signup, onboarding, popups, paywalls, pricing, offers, ads,
  ad-creative, emails, cold-email, social, content-strategy, analytics,
  conversion-tracking, ab-testing, launch, churn-prevention, customer-research,
  competitors, marketing-plan, and more.
- **Writing quality**: `stop-slop` (remove AI writing tells). Apply it to any
  public-facing text (site copy, descriptions, posts, scripts).
- **UI / UX / design** (ui-ux-pro-max): ui-ux-pro-max, ui-styling, design,
  design-system, brand, banner-design, slides.
- **Agent & context engineering**: context-fundamentals, context-optimization,
  context-compression, context-degradation, memory-systems, multi-agent-patterns,
  tool-design, filesystem-context, hosted-agents, evaluation, advanced-evaluation,
  project-development, harness-engineering, long-horizon-prompting, and more.
- **Reverse engineering**: `reverse-engineer-anything` (morluto/rea).

## 2. Working rules
- Always reply to Adil in **Arabic**, even for technical work.
- Work autonomously. Do not ask Adil to fetch links, copy code or edit by hand.
  Only involve him when strictly required (login, final approval, one click).
- Never report a task as done before verifying yourself that it really works
  (check the live result, run the build, open the page).
- Be frank: give honest opinions even when they differ from his expectations.
- Any generated content (prompts, scripts, texts) is also delivered as a TXT file.
