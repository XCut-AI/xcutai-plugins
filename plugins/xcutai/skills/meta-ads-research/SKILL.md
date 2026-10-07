---
name: meta-ads-research
description: Research competitors' Facebook and Instagram ads in the Meta Ad Library and write new ad copy from what runs longest. Use when the user asks what ads competitors run, for ad angles, ad hooks, ad copy or creative briefs for Meta (Facebook or Instagram) ads.
---

# Meta ad research

Explicit user instructions take priority over these steps.

1. Find the ads: call `xcut_search_viral` with `platform: "meta_ads"` and the competitor or topic as `query`.
2. For an ad the user wants studied in depth, call `xcut_import_meta_ad` with its Meta Ad Library link to get the full copy, media and video transcript.
3. Explain each strong ad: angle, hook, offer and call to action. The Ad Library publishes no spend, so use how long an ad has run as the performance signal and say so.
4. To write the user's version, call `xcut_write_content` with `agent: "meta_ad"`, or `xcut_run_playbook` with `playbook: "angles"` for an ad-angle gap map or `"adcreatives"` for ad creatives.

Never state spend, CTR or ROAS: the Ad Library does not provide them.
