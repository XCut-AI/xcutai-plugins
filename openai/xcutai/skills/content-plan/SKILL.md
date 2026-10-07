---
name: content-plan
description: Build a week or month content plan, competitor teardown, ad-angle map or prospect audit with XCut AI playbooks and put the posts on the user's content calendar. Use when the user asks what to post this week or month, for a content calendar, or to schedule or reorganise planned posts.
---

# Content plans with XCut AI

Explicit user instructions take priority over these steps.

1. Pick the canvas that holds the user's research (`xcut_list_canvases`). A plan is only as good as what's on it. If the canvas is empty, run the `viral-research` skill first and import 2-5 outliers.
2. Run a playbook with `xcut_run_playbook`:
   - `month` or `week`: a content plan. Pass `days` (3-120) and `platform` when the user names them.
   - `teardown` or `benchmark`: what competitors do that the user doesn't.
   - `angles` or `adcreatives`: ad angles and ad copy.
   - `audit`: a prospect audit for agencies.
   - `hooks`, `scripts`, `remix`, `carousel`, `thumbnails`: batches of one asset type.
   Put any extra instructions from the user in `notes`.
3. Put posts on the calendar with `xcut_add_to_calendar`. Read it with `xcut_list_calendar`, move or edit with `xcut_update_calendar_post`, and use `xcut_delete_calendar_post` only when the user asks for a deletion.

XCut AI plans and drafts. It does not publish to social media, so never say a post was published.
