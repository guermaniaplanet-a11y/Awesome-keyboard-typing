---
name: public-apis
description: Directory of ~2,500 free public APIs (public-apis/public-apis) in 52 categories - weather, geocoding, maps, animals, science, space, entertainment, video, music, books, news, finance, currency, crypto, sports, games, open data, government, health, food, translation, text analysis, machine learning, photography, URL shorteners and more, with auth type, HTTPS and CORS flags. Use when a site, tool, bot, automation or video project needs data from an external API, or to find a free API instead of building or scraping.
---

# Public APIs

Source: https://github.com/public-apis/public-apis (MIT), snapshot in
`references/public-apis.md` (taken 2026-11-18, ~374 KB, ~2,500 APIs, 52 categories).

## How to use

1. Never read the whole file. List categories: `grep -n "^### " references/public-apis.md`
2. Read one category (`sed -n '<start>,<end>p'`) or grep a keyword
   (`grep -n -i "weather" references/public-apis.md`).
   Each row: API | Description | Auth (No / apiKey / OAuth) | HTTPS | CORS.
3. Prefer `Auth: No` or `apiKey` + HTTPS. CORS `Yes` is needed only for calls made
   directly from browser code; otherwise call the API from a server, edge function or n8n.
4. Open the API's docs before using it: confirm it is still online, its current free
   limits and terms. Put any key in an environment variable, never in committed code.
5. Newer copy: https://raw.githubusercontent.com/public-apis/public-apis/master/README.md
