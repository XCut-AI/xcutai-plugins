---
name: analytics-review
description: Review how an Instagram, TikTok, YouTube or Facebook account is performing and which posts stood out. Use when the user asks how their or a competitor's account is doing, for a performance review, engagement stats, best and worst posts, or to compare accounts.
---

# Account performance review

Explicit user instructions take priority over these steps.

1. Ask for the profile link or @handle and platform if they are missing.
2. Call `xcut_profile_analytics` for the per-post metrics over the last posts or days the user wants (default the last 20 posts).
3. Call `xcut_find_outliers` on the same account to see which posts beat its own median and by how much.
4. If either returns a `job_id`, call `xcut_get_job` until it is done and tell the user it is still running.
5. Report: average views and engagement, the top 3 posts with how far each beat the median, the weakest posts, and 3 concrete next steps based on what the outliers share (hook, format, topic, length).

To compare accounts, run steps 2-3 for each and put the numbers side by side. Use only numbers the tools returned.
