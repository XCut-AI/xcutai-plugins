---
name: creator-report
description: Build an in-depth report on an Instagram, TikTok, YouTube or Facebook creator with XCut AI: their posts from the last few months, the top 7 or 8 against their own usual, why those beat the rest, and charts. Use when the user asks to study a creator or competitor in depth, why their best posts work, or for a creator report.
---

# Creator report

Explicit user instructions take priority over these steps.

1. Get the @handle or profile link and the platform if they are missing. Default window: the last 90 days.
2. Call `xcut_get_account` and tell the user roughly what this uses (scoring 50 posts is a few credits; each transcript adds more). Continue unless they say stop.
3. Call `xcut_find_outliers` on the account with `posts` set to 50 (100 for accounts that post daily). It scores each post against the account's own median.
4. Call `xcut_profile_analytics` on the same account with `days` set to the window, for the full field of posts.
5. If either returns a `job_id`, call `xcut_get_job` until it is done and tell the user it is still running.
6. Take the top 7 or 8 posts by how far they beat the median. Bring in the top 3 to 5 with `xcut_import_post` (then `xcut_get_job`) for their transcripts. Ask before importing all 8.
7. Write the report. If you can make an artifact (a page or document with charts), build one; otherwise use tables.
   - **Headline**: one sentence on what wins for this creator.
   - **Chart**: each post's views against the account's median over time, with the top posts marked.
   - **Top posts table**: link, views, how many times the median, format, hook, length.
   - **What the winners share**: hook type, format, topic, length and structure, each with the posts that show it.
   - **What the rest do differently**: the pattern in the posts that stayed near or below the median.
   - **Your playbook**: three video ideas built on the winning pattern, each with a hook line.
8. Tell the user the posts are saved on their XCut AI canvas. In Claude, open the artifact in the browser to use the charts.

Use only numbers the tools returned. If the account is private or has fewer than 10 recent posts, say so and suggest a similar creator. Not enough credits: show the balance from `xcut_get_account` and stop.
