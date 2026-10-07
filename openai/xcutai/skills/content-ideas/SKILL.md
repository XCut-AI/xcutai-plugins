---
name: content-ideas
description: Come up with content ideas, topics and angles for Instagram, TikTok, YouTube or Facebook based on what is performing now in the user's niche. Use when the user asks what to post, for video or post ideas, trending topics, or fresh angles for their niche or brand.
---

# Content ideas grounded in what performs

Explicit user instructions (platform, niche, number of ideas, tone) take priority over these steps.

1. If the niche or platform is unclear, ask one short question. Otherwise continue.
2. Call `xcut_search_viral` with `mode: "keyword"` for the niche on that platform. If the user named creators or competitors, also call `xcut_find_outliers` on one or two of them.
3. Call `xcut_get_playbook` with the goal (for example "Reel ideas for a skincare brand") to match each idea to a format that performed.
4. If the user is signed in and has a brand, call `xcut_get_brand` and fit the ideas to its voice, audience and offer.
5. Return 5-10 ideas. For each: the hook line, the format, why it should work (cite the post or outlier it comes from, with its numbers), and the platform.

Do not invent view counts or trends: every "why" must point to a real result from the tools. Offer to write the scripts next (the `outlier-to-script` skill) or plan them (the `content-plan` skill).
