---
name: llm-app-templates
description: Catalog of 100+ ready-to-run LLM app templates (Shubhamsaboo/awesome-llm-apps) - AI agents, multi-agent teams, voice agents, RAG, chat-with-X, LLM apps with memory, MCP agents, always-on agents, generative UI, fine-tuning. Use before building any AI-powered app, bot, agent, RAG system or automation, to start from a proven working template instead of from scratch.
---

# LLM app templates

Source: https://github.com/Shubhamsaboo/awesome-llm-apps (Apache-2.0), index snapshot in
`references/awesome-llm-apps.md` (taken 2026-11-18).

## How to use

1. Find candidates: `grep -n -i "<keyword>" references/awesome-llm-apps.md`
   (e.g. youtube, seo, rag, voice, whatsapp, memory, mcp, multi-agent, finance, travel).
   Sections: Agent Skills, Standalone Apps & Tools, Starter AI Agents, Advanced AI Agents,
   Always-on Agents, Multi-agent Teams, Voice AI Agents, Generative UI, Game-Playing Agents,
   MCP AI Agents, RAG, LLM Apps with Memory, Chat with X, LLM Optimization, Fine-tuning,
   Agent Framework Crash Courses.
2. Fetch only the chosen template folder (the repo is large):
   ```
   git clone --depth 1 --filter=blob:none --sparse https://github.com/Shubhamsaboo/awesome-llm-apps.git
   cd awesome-llm-apps && git sparse-checkout set <path/to/template>
   ```
3. Read its README and requirements, adapt it to the project (models, keys via env vars,
   the owner's stack), and verify it runs before reporting it done.
