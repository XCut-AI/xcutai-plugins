---
name: hooks-captions-bios
description: Write hooks, captions, profile bios, YouTube titles, script scores and repurposed versions for social media, free and without signing in. Use when the user asks for hooks or opening lines, a caption, a bio rewrite, video titles, feedback on a script, or to repurpose one piece of content across platforms.
---

# Fast content deliverables

Explicit user instructions take priority over these steps.

- Hooks or opening lines: call `xcut_find_hooks` with the topic for proven templates, then fill the slots with the user's subject. For 10 ready-made variations, call `xcut_quick_tool` with `tool: "hooks"`.
- Caption: `xcut_quick_tool` with `tool: "caption"`.
- Profile bio: `xcut_quick_tool` with `tool: "bio"`.
- YouTube titles and thumbnail ideas: `xcut_quick_tool` with `tool: "titles"`.
- Feedback on a script: `xcut_quick_tool` with `tool: "script_analysis"`.
- One piece into many platforms: `xcut_quick_tool` with `tool: "repurpose"`.

These need no account. If the user wants the output written in their saved brand voice or from their own posts, use the `outlier-to-script` skill instead (it signs in). Return the results ready to copy, and say which proven pattern each hook follows.
