---
name: comment-to-dm
description: Build comment-to-DM and other chatbot automations with Ignix — when someone comments a keyword on a post, send them a DM with a link, a lead magnet or a booking — plus welcome messages and keyword replies. Use when the user wants to automate DMs, "comment GUIDE to get the link", capture leads from comments, or set up a chatbot on Instagram or Facebook.
license: MIT
---

# Comment-to-DM automations with Ignix

Requires the Ignix connector.

1. `list_accounts` — pick the Instagram or Facebook account.
2. Decide which post: a specific published post (`list_posts` / `list_account_media`) or the NEXT post the account publishes. "Next post" automations attach themselves when the post is actually published; a draft or a scheduled post does not claim them.
3. Agree the keyword, the public reply to the comment and the DM (text plus link buttons) with the user. Links go in `buttons`, never in the message text.
4. `create_comment_to_dm` for the classic flow. For anything richer (questions, tags, branches), `list_automation_templates` → `create_automation_from_template`, or `get_automation_node_types` → `create_automation`.
5. `preview_automation` to show exactly what the person will receive, then turn it on with `set_automation_active` only after the user approves: it messages real people.
6. Check results later with `get_automation_usage`.

Keep it human: vary the public replies (several variants) so the account does not look automated, and never DM people who did not comment.
