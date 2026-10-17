---
name: inbox
description: Work through a brand's social media inbox with Ignix — direct messages from Instagram, Facebook, WhatsApp, TikTok and the website chat, plus comments and reviews — drafting replies in the brand voice, triaging and escalating to a human. Use when the user wants to answer messages, clear the inbox, reply to comments or reviews, or see what customers are asking.
license: MIT
---

# Answer the inbox with Ignix

Requires the Ignix connector.

1. `list_conversations` (use `unreadOnly` or `needsHumanOnly` to focus), then `get_conversation` to read each thread.
2. Before answering anything factual (prices, hours, policies, stock, how a product works): `search_knowledge` and `list_catalog`. Do not guess.
3. Check `list_saved_replies`; reuse the team's wording when one fits.
4. Show every reply to the user BEFORE sending. Only call `send_message`, `reply_to_comment` or `reply_to_review` after a clear yes: these reach a real person.
5. Complaints, refunds or anything you cannot answer with certainty: `update_conversation` with `escalateToHuman: true` instead of replying. Use `add_conversation_note` to leave context for the team.
6. Triage with `update_conversation` (stage, labels, assignee) when the user asks.

Reply in the language the customer wrote in. Links go in `buttons`, never also in the text.
