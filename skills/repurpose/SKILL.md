---
name: repurpose
description: Get more out of a brand's best social media posts with Ignix — find what performed best, explain why, and turn it into new posts adapted to other networks or recycle evergreen ones. Use when the user asks to repurpose, reuse, recycle or cross-post content, or "do more of what works".
license: MIT
---

# Repurpose what worked with Ignix

Requires the Ignix connector.

1. `get_top_posts` (default the last 90 days) — the best performers.
2. For each of the top three, say in one line WHY it worked: hook, format, topic or timing.
3. Adapt each one to the networks where it was not published with `adapt_caption`, so every version is native to its network rather than a copy.
4. An evergreen post that can simply run again: `recycle_post` (it needs the Ignix post id from `list_posts`).
5. Leave the new versions as drafts with `create_post` and list what you created.

AI writing tools return a quote first; confirm the credits with the user before calling them with `confirm: true`.
