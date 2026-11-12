---
name: watchlist-insights
description: Find what is working across the accounts on the user's XCut AI watchlist: the top videos, the topics, the formats and the hook patterns behind their breakouts. Use when the user asks what is working in their niche, for top videos, topics, formats or hooks from the creators they track, or what is breaking out right now.
---

# Watchlist insights

Explicit user instructions take priority over these steps.

1. Call `xcut_get_breakouts` with `limit` set to 50. It returns the breakout posts from the user's watchlist (views, how many times each account's median, format, caption) and trending keywords.
2. If the user wants fresh results, call `xcut_scan_watchlist` with `estimate` set to true, tell them the cost, then scan and call `xcut_get_breakouts` again.
3. Answer what they asked, using only the breakouts returned:
   - **Top videos**: the posts ranked by how far they beat their account's median, with the link, the account and one line on why each works.
   - **Topics**: group the breakouts into 3 to 6 topics from their captions and the trending keywords. For each topic give how many breakouts and the best example.
   - **Formats**: label each breakout's format (talking head, tutorial, list, story, reaction, demo, carousel). Rank formats by their average multiple and count. Use `xcut_get_playbook` with `kind` set to structure for how to make the winning format.
   - **Hooks**: take the first line of each top breakout's caption, group them into hook patterns, and write each pattern as a fill-in-the-blank template with a real example. `xcut_find_hooks` adds proven templates for the same topic.
4. Finish with the single strongest pattern and one video idea built on it.

If the watchlist is empty, say so: the user adds accounts on the Watchlist page in XCut AI (or ask them for 3 to 5 creators and use the viral-research skill). Sign-in needed: XCut AI asks once. Use only numbers the tools returned.
