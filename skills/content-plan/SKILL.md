---
name: content-plan
description: Plan and schedule social media content with Ignix — a week of posts, a campaign from a brief, or a month on autopilot — written in the brand's voice from what is working in its niche. Use when the user asks to plan, write, schedule or fill their content calendar for Instagram, TikTok, LinkedIn, X, Facebook, Threads, Pinterest, YouTube or another connected network.
license: MIT
---

# Plan and schedule content with Ignix

Requires the Ignix connector. Ignix only works with an active plan: if a tool says the plan is not active, stop and tell the user what it says: the account owner can fix it by opening the Ignix app.

1. `list_accounts` — which accounts and networks exist. Every publishing tool needs these ids.
2. `get_brand_profile` and `search_knowledge` on the topic — the brand voice and the facts (prices, products, policies). Never invent them.
3. Plan before creating:
   - A week or a period: `plan_campaign` (ideas from what works in the niche and on the brand's own account).
   - One brief: `plan_content` per network.
   Show the plan as a short table (date, network, format, idea, opening line) and let the user change it. Create nothing yet.
4. After the user agrees, for each piece: `plan_content` → `generate_image` where an image adds value → `validate_post` → `create_post`. Use `suggest_publish_times` for the time slot. Leave posts as DRAFTS unless the user asked to schedule them, and never publish immediately without a clear yes.
5. If the user just wants it done, `run_autopilot` makes the whole run as drafts.
6. Finish with a table of what was created: account, date, opening line, status.

Rules:
- Tools that spend AI credits first return a quote (what they will do and the credits). Tell the user and wait for a yes before calling again with `confirm: true`.
- Links go in the `buttons`/link fields, never pasted twice in the text.
- Write in the language of the account's audience, not in the language of this conversation, unless told otherwise.
