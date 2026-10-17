---
name: performance-report
description: Explain how a brand's social media is doing with Ignix analytics — reach, engagement, followers, best posts, posting rhythm and inbox activity — in plain language with concrete next steps. Use when the user asks how their accounts are performing, wants a monthly report, a client report or a PDF, or asks what works and what does not.
license: MIT
---

# Social media performance report with Ignix

Requires the Ignix connector.

Gather the data first (default window: 30 days; use the user's if given):
- `get_analytics` — totals with the previous period for comparison.
- `get_top_posts` — what worked; read the captions and formats.
- `get_follower_growth` and `get_engagement_trend` — is it improving?
- `get_posting_cadence` — is the rhythm right?
- `get_inbox_analytics` — if the business handles messages.
- `get_audience` — who follows them, when available.

Then write for a business owner, not an analyst:
1. What happened, in three lines.
2. What worked and the concrete reason (format, hook, topic, timing).
3. What did not work.
4. Three specific actions for the coming weeks, each tied to a number you actually read.

Never invent a metric; if something has no data, say so. For a shareable PDF, `build_report_link` returns a link the user opens and saves as PDF.
