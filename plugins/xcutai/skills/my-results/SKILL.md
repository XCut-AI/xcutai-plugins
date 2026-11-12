---
name: my-results
description: Show how the user's own posts are doing with XCut AI: whether recent posts beat their usual views, which formats and topics win, and what to post next, from their public profile. Use when the user asks how their posts did, whether a post beat their usual or what to post next.
---

# My results

Explicit user instructions take priority over these steps.

1. Ask for their profile link or @handle and platform if they are missing.
2. Call `xcut_profile_analytics` on their own account for the last 30 days (or what they ask for). If it returns a `job_id`, call `xcut_get_job` until it is done.
3. Call `xcut_find_outliers` on the same account: it shows which posts beat their usual (their median views) and by how much.
4. If they plan in XCut AI, call `xcut_list_calendar` for the same days and match the posts marked published to the posts above.
5. Report:
   - **What beat your usual**: each winning post, by how much, and what it had in common.
   - **What didn't**: the posts below their usual and the likely reason.
   - **Next step**: one concrete post to make next, based on the winners.

Use only numbers the tools returned. These are public numbers (views, likes, comments); say so if they ask about reach or saves.
