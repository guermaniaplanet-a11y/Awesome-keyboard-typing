# Instructions for Claude Code (owner: Adil)

## 1. Skills: use them automatically, never ask

This repository ships a full skill library in `.claude/skills/` (180 skills).
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
- **AI video agent / editing**: `openfilm` (openfilm/openfilm): make any video
  (Shorts, explainers, launch films, music videos, motion graphics) as a web page,
  then edit, cut, grade and render it. Needs Node 22.2+ and ffmpeg; launch with
  `npx -y openfilm@latest`. Use it for any video creation or editing task.
- **HTML-to-video** (heygen-com/hyperframes): `hyperframes` (router, read it
  first for any video / animation / motion-graphics request), hyperframes-cli,
  hyperframes-registry, media-use, slideshow, style-sampling, figma,
  reverse-any-video, remotion-to-hyperframes. Renders MP4 from HTML, CLI via
  `npx hyperframes`. Choose between hyperframes and openfilm per task: hyperframes
  for programmatic Shorts / explainers / animated captions rendered to MP4;
  openfilm when a live visual editor is wanted. Use only real, credible visuals
  for Guermania Planet (no fantasy / fake CGI).
- **React video** (remotion-dev/skills, official): remotion-create,
  remotion-best-practices, remotion-captions, remotion-multimedia, remotion-render,
  remotion-studio, remotion-maps, remotion-markup, remotion-interactivity,
  remotion-saas, remotion-docs, remotion-upgrade, remotion-license. Use when a
  project already uses Remotion, or for data-driven / templated videos generated at
  scale from code (React). For new standalone videos, prefer hyperframes.
- **Marketing / SEO / growth** (coreyhaines31/marketingskills): seo-audit, ai-seo,
  programmatic-seo, schema, site-architecture, link-building, copywriting,
  copy-editing, cro, signup, onboarding, popups, paywalls, pricing, offers, ads,
  ad-creative, emails, cold-email, social, content-strategy, analytics,
  conversion-tracking, ab-testing, launch, churn-prevention, customer-research,
  competitors, marketing-plan, and more.
- **Writing quality**: `stop-slop` (remove AI writing tells). Apply it to any
  public-facing text (site copy, descriptions, posts, scripts).
- **Frontend design quality** (pbakaus/impeccable): `impeccable`: design, redesign,
  critique, audit, polish or animate any website, landing page, dashboard, app UI
  or component. Use it on every frontend task, together with ui-ux-pro-max.
- **UI components MCP** (21st-dev/magic-mcp, in `.mcp.json`): the `magic` MCP
  server generates polished React/Tailwind UI components inspired by the 21st.dev
  library, searches logos (JSX/TSX/SVG) and refines existing UI. Use it for any
  new UI component, together with impeccable and ui-ux-pro-max. Needs the
  environment variable MAGIC_API_KEY (never write the key in a file). If the
  server fails because the key is missing, tell Adil once and continue without it.
- **Up-to-date library docs MCP** (upstash/context7, in `.mcp.json`): the
  `context7` MCP server returns current, version-specific documentation and code
  examples for libraries and frameworks (React, Next.js, Tailwind, Supabase,
  Remotion, etc.). Use it BEFORE writing code that depends on a library API, so
  the code matches the current version instead of outdated memory. Works without
  a key (lower rate limits).
- **UI / UX / design** (ui-ux-pro-max): ui-ux-pro-max, ui-styling, design,
  design-system, brand, banner-design, slides.
- **Codebase knowledge graph** (Graphify-Labs/graphify): `graphify`. In any repo
  with real code, on the first coding task of a session run `/graphify .` (or
  `--update` if `graphify-out/` exists), then read `graphify-out/GRAPH_REPORT.md`
  and query the graph instead of grepping every file (saves tokens). The Python
  package `graphifyy` installs itself on first run. Commit `graphify-out/` only
  for private repos; in public repos add it to .gitignore.
- **Agent & context engineering**: context-fundamentals, context-optimization,
  context-compression, context-degradation, memory-systems, multi-agent-patterns,
  tool-design, filesystem-context, hosted-agents, evaluation, advanced-evaluation,
  project-development, harness-engineering, long-horizon-prompting, and more.
- **Software engineering workflow** (obra/superpowers): `using-superpowers`
  (read it FIRST at the start of any coding / website / app / automation task),
  brainstorming, writing-plans, executing-plans, test-driven-development,
  systematic-debugging, verification-before-completion, requesting-code-review,
  receiving-code-review, subagent-driven-development, dispatching-parallel-agents,
  using-git-worktrees, finishing-a-development-branch, writing-skills.
  PRIORITY: Adil's autonomy rule overrides superpowers. Where a superpowers skill
  says to ask the user questions or wait for approval (brainstorming, plans,
  design sign-off), decide yourself with the best reasonable choice, note it, and
  continue. Only stop for logins, payments or irreversible actions.
  References to `superpowers:<name>` mean the skill `<name>` in `.claude/skills/`.
- **Production engineering lifecycle** (addyosmani/agent-skills, 25 skills):
  using-agent-skills (router), idea-refine, spec-driven-development,
  planning-and-task-breakdown, incremental-implementation, source-driven-development,
  constraint-driven-development, doubt-driven-development, frontend-ui-engineering,
  api-and-interface-design, accessibility-engineering, performance-optimization,
  security-and-hardening, observability-and-instrumentation, debugging-and-error-recovery,
  code-review-and-quality, code-simplification, browser-testing-with-devtools,
  ci-cd-and-automation, git-workflow-and-versioning, deprecation-and-migration,
  documentation-and-adrs, context-engineering, shipping-and-launch, interview-me.
  Shared checklists live in `.claude/references/`. `test-driven-development` here
  is the superpowers one (same role). Use `interview-me` only when Adil asks to be
  interviewed; otherwise the autonomy rule applies.
- **Lean code** (DietrichGebert/ponytail): `ponytail` is ALWAYS ON for every
  coding task (write, refactor, fix): smallest complete change, reuse existing
  code / stdlib / native platform features, no unrequested abstractions, tests for
  risky logic. Also: ponytail-review (review a diff), ponytail-audit (whole-repo
  health check), ponytail-debt, ponytail-gain, ponytail-help.
  Ponytail never overrides: the Arabic reply rule, verification before reporting
  done, or the autonomy rule.
- **Security audit** (cloudflare/security-audit-skill): `security-audit`: 6-phase
  security audit with independently verified findings (web apps, APIs, bots,
  automations). Use when asked for a security review, before launching or
  deploying anything public, and after adding auth, payments, forms or API keys.
  Keep the skill's own output directory (outside the repo). NEVER commit audit
  findings to the repo (some repos are public: findings would expose the holes);
  deliver the report to Adil as a file and fix the issues. A full audit launches
  many sub-agents: start with a focused scope.
- **AI pentesting** (usestrix/strix, 9 skills): penetration-testing-with-strix,
  web-app-penetration-testing, api-security-testing, owasp-top-10-testing,
  application-security-testing, find-security-vulnerabilities-in-code,
  fix-security-vulnerabilities-with-strix, ci-security-scanning-with-strix,
  managed-pentesting-with-strix. Needs Docker, Python 3.12+ and an LLM API key.
  SCOPE RULE (strict): only test Adil's own repos and domains (typingtest.one,
  tikwell.com, thecatinsurance.com, arabpdf.com, his Lovable/Vercel apps). Never
  scan a third-party site. Live (black-box) scans of production sites: tell Adil
  first, since they send real attack traffic. Same reporting rule as
  security-audit: never commit findings.
- **WhatsApp automation** (gokapso/agent-skills, Kapso platform): integrate-whatsapp
  (connect a number, webhooks, send text/templates/media/interactive messages,
  WhatsApp Flows), integrate-whatsapp-calling, automate-whatsapp (workflows,
  triggers, AI agent nodes, functions), observe-whatsapp (delivery debugging,
  health checks). Needs a Kapso account and KAPSO_API_KEY; if missing, ask Adil
  once for the key (login is the one allowed interruption).
- **Skill discovery** (vercel-labs/skills): `find-skills`. When a task would clearly
  benefit from a capability none of the skills above covers, search skills.sh with
  `npx skills find <query>` and propose the best matches to Adil in one short
  message (name, source, installs, what it adds). Installing new third-party code
  is the one exception to the autonomy rule: install only after Adil says yes.
  PERSISTENCE: this session is temporary. After Adil approves, copy the new skill
  into this repo's `.claude/skills/`, add it to this list, commit and push, so it
  is still there next session.
- **Web scraping** (D4Vinci/Scrapling): `scrapling-official`. Scrape and crawl
  websites, extract data, render JavaScript, write spiders (competitor research,
  SEO data, prices, public lists, feeding content tools). Install with
  `pip install scrapling` when needed. USAGE RULE: scrape public data only,
  respect robots.txt and each site's terms, keep request rates low. Do NOT use
  the CAPTCHA / Cloudflare-solving or anti-bot bypass features on sites Adil does
  not own; if a site blocks scraping, report it and look for an official API.
  Never scrape personal data about private individuals.
- **Free services finder** (ripienaar/free-for-dev): `free-for-dev`. Whenever a
  task needs an external service (hosting, database, email, auth, CDN, storage,
  AI API, forms, analytics...), check this list first and prefer a free tier
  before proposing anything paid. Verify current limits on the provider's site.
- **Reverse engineering**: `reverse-engineer-anything` (morluto/rea).

## 2. Working rules
- Always reply to Adil in **Arabic**, even for technical work.
- Work autonomously. Do not ask Adil to fetch links, copy code or edit by hand.
  Only involve him when strictly required (login, final approval, one click).
- Never report a task as done before verifying yourself that it really works
  (check the live result, run the build, open the page).
- Be frank: give honest opinions even when they differ from his expectations.
- Any generated content (prompts, scripts, texts) is also delivered as a TXT file.
