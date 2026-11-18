---
name: mcp-server-finder
description: Catalog of ~5,000 MCP servers (punkpeye/awesome-mcp-servers) by category - browser automation, databases, search and data extraction, social media, marketing, multimedia, file systems, finance, e-commerce, communication, developer tools, cloud, knowledge and memory, location, translation and more. Use when a task needs to connect Claude Code to an external app, API or data source, or when the user asks for an MCP server for something.
---

# MCP server finder

Source: https://github.com/punkpeye/awesome-mcp-servers (MIT), snapshot in
`references/awesome-mcp-servers.md` (taken 2026-11-18, ~1.8 MB, ~5,000 entries).

## How to use

1. Never read the whole file. List categories: `grep -n "^### " references/awesome-mcp-servers.md`
   Useful ones: Browser Automation, Search & Data Extraction, Social Media, Marketing,
   Multimedia Process, Databases, File Systems, Communication, Developer Tools,
   Cloud Platforms, E-Commerce, Knowledge & Memory, Translation Services, Aggregators.
2. Read one category (`sed -n '<start>,<end>p'`) or grep a keyword
   (`grep -n -i "youtube" references/awesome-mcp-servers.md`).
   The legend near the top explains the icons (official, language, local or cloud, OS).
3. Prefer official servers from the vendor itself, then the most active repos.
   Check the repo (last commit, stars, license, install steps) before using one.
4. To add one to this project, add an entry to `.mcp.json` (stdio `command`/`args`, or
   `"type": "http"` with `url`). Put any API key in an environment variable referenced
   as `${VAR_NAME}`, never in the file. Commit and push so it persists across sessions,
   and add one line about it to CLAUDE.md.
5. Newer copy of the list:
   https://raw.githubusercontent.com/punkpeye/awesome-mcp-servers/main/README.md
