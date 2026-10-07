---
name: viral-research
description: Find what is performing on Instagram, TikTok, YouTube, Facebook or the Meta Ad Library with XCut AI. Use when the user asks what is going viral, trending or working in a niche, which posts of a creator or competitor were outliers, how an account is performing, or what ads competitors run.
---

# Viral research with XCut AI

Pick the tool from the question:

| The user asks | Call |
|---|---|
| What's going viral / trending for a topic | `xcut_search_viral` with `mode: "keyword"` |
| What a specific creator posts that works | `xcut_search_viral` with `mode: "profile"`, or `xcut_find_outliers` |
| Which posts beat an account's normal | `xcut_find_outliers` (`posts`: 20, 30, 50 or 100) |
| Views, likes, engagement over N posts or days | `xcut_profile_analytics` |
| What's breaking out among accounts they watch | `xcut_get_breakouts` |
| Competitors' Facebook / Instagram ads | `xcut_search_viral` with `platform: "meta_ads"` |

Rules:

- Ask for the platform only when the question doesn't make it clear.
- An outlier is a post that beat that account's own median. Always say by how much (for example "4.2x their median views"), not just "it did well".
- Long reads return a `job_id`. Call `xcut_get_job` with it until the result is ready, and tell the user it's still working.
- Meta Ad Library has no spend data. Use how long an ad has run as the signal and say so.
- Lead with the 3-5 strongest results and why each worked (hook, format, topic). Offer next steps: break one down, or write the user's version (the `outlier-to-script` skill).
- If a tool says the user must sign in or is out of credits, pass that on plainly and link to https://xcut.ai/pricing only when it is about credits.
