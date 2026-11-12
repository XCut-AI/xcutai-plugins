---
name: analyze-post
description: Break down one Instagram, TikTok, YouTube or Facebook post or video from its link with XCut AI: transcript, stats, hook, format, topic, structure and why it worked. Use when the user pastes a post link and asks to analyze it, what made it work, or for its transcript, without asking for a rewrite yet.
---

# Analyze one post

Explicit user instructions take priority over these steps.

1. Bring the post in with `xcut_import_post` (the post or video link). Don't ask which canvas: with none named it goes to the user's "From AI apps" canvas. Pass `canvas_id` only if the user names a canvas.
2. If it returns a `job_id`, call `xcut_get_job` until it is done. Tell the user it is still running while you wait. The finished result has the transcript and the stats.
3. Write the breakdown with these sections, using only what the tools returned:
   - **Stats**: views, likes, comments and, when the result has it, how far the post beat the account's usual.
   - **Hook**: the first line word for word, and why it stops the scroll.
   - **Format and topic**: the video format (talking head, tutorial, list, story, reaction, demo) and the angle on the topic.
   - **Structure**: the beats in order, with timestamps when the transcript has them.
   - **Visuals and on-screen text**, and the **call to action**.
   - **Why it worked**: three points, each tied to something in the post.
4. End with one line offering the next step: "Want your version of this? I can write it in your brand voice." If they say yes, follow the outlier-to-script skill.

If a step fails:
- Sign-in needed: say XCut AI will ask them to sign in once, then retry.
- Not enough credits: call `xcut_get_account`, tell them their balance, and stop.
- Private, deleted or unsupported link: say so plainly and ask for a public post link.
