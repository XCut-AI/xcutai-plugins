---
name: outlier-to-script
description: Turn a post that performed into the user's own Reel, TikTok, Short, YouTube script, hooks or captions with XCut AI, written in their brand voice. Use when the user pastes a post link to break down, asks why a video went viral, or wants scripts, hooks or captions based on posts that worked.
---

# From an outlier to the user's script

Explicit user instructions take priority over these steps.

1. Bring the post in with `xcut_import_post` (a post or video link). Don't ask which canvas: with none named it goes to the user's "From AI apps" canvas. Pass `canvas_id` only if the user names a canvas (find it with `xcut_list_canvases`).
2. If it returns a `job_id`, call `xcut_get_job` until it is done: the finished result includes the transcript.
3. Use `xcut_get_content` only if you need the full breakdown again later.
4. Write with `xcut_write_content` (same canvas as the import). Pass the user's request in their own words, for example "Write 3 TikTok scripts from this video for my brand". Use `item_ids` to limit it to the imported post. Leave `agent` as `auto` unless the user asks for a specific format.
5. Check the brand first. If `xcut_get_brand` shows no brand memory, ask for the voice, audience and offer in one question, then save it with `xcut_save_memory`.

For quick hooks without a canvas or sign-in, use `xcut_find_hooks`. For captions, bios, titles or script scores, use `xcut_quick_tool`.

Show the result in the chat and mention it is also saved on the user's XCut AI canvas.
