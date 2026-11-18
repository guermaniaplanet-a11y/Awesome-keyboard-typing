---
name: free-for-dev
description: Find free tiers of SaaS, PaaS, IaaS and developer services (hosting, databases, email, auth, CDN, DNS, storage, monitoring, analytics, forms, AI APIs, payments, CI, search...). Use whenever a task needs an external service, before suggesting any paid tool, when choosing where to host or deploy, or when the user asks for a free or cheaper alternative.
---

# Free for Dev

Source: the community list ripienaar/free-for-dev (https://github.com/ripienaar/free-for-dev),
snapshot in `references/free-for-dev.md` (taken 2026-11-18, ~280 KB, 57 sections).

## How to use

1. Never read the whole file. Find the relevant section first:
   `grep -n "^## " references/free-for-dev.md`
   Sections include: Web Hosting, PaaS, BaaS, Managed Data Services, Email, Authentication,
   CDN and Protection, DNS, Domain, Storage and Media Processing, Generative AI, APIs Data and ML,
   Analytics, Monitoring, Log Management, Forms, Search, CI and CD, Payment and Billing,
   Screenshot APIs, Low-code Platform, Major Cloud Providers.
2. Read only that section (e.g. `sed -n '<start>,<end>p'`), or grep a keyword
   (`grep -n -i "postgres" references/free-for-dev.md`).
3. Shortlist 2-3 options that fit the project (stack, region, expected traffic, the owner's
   existing tools: Vercel, Cloudflare, Lovable, Bolt, Supabase, n8n, Make).
4. Free tiers change often. Before recommending one, check the provider's current pricing
   page (the snapshot can be stale). If the network allows it, the live list is at
   https://raw.githubusercontent.com/ripienaar/free-for-dev/master/README.md
5. State the limits that matter (requests, storage, bandwidth, sleep on idle, card required,
   commercial use allowed) and what happens when the limit is exceeded.
