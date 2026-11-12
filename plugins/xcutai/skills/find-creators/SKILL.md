---
name: find-creators
description: Find creators worth studying on Instagram, TikTok, YouTube or Facebook from a description of a niche or topic, with XCut AI. Use when the user asks who to follow, track or study in a niche, for creators like a given one, or for accounts to add to their watchlist.
---

# Find creators to study

Explicit user instructions take priority over these steps.

1. Get the niche or topic, the platforms and how many creators the user wants (default 10). Note any limits they give (size, platform, language).
2. For each platform, call `xcut_search_viral` with `mode` set to keyword, the niche as `query` and `limit` set to 30. Try 2 or 3 phrasings of the niche to widen the net.
3. Group the posts by account. Rank accounts by how many strong posts they have in the results and their best views. Drop accounts that do not fit the user's limits, and only use follower counts if the tool returned them.
4. For the top 3, offer to confirm they are consistent with `xcut_find_outliers` (it uses a few credits each) and run it if the user agrees.
5. Show a table: account, platform, why they are worth studying (their winning angle or format) and their standout post link.
6. Suggest the next step: add them to the Watchlist in XCut AI so breakouts from them arrive automatically, or run the creator-report skill on one.

Use only accounts and numbers the tools returned. If a search returns nothing, try a broader phrasing before saying so.
