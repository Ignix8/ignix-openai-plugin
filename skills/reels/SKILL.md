---
name: reels
description: Make short videos with Ignix — Reels, TikToks and Shorts with voice-over, subtitles and sound effects, AI video clips, or the user's own footage edited into clips. Use when the user asks for a reel, a short video, a video post, subtitles on their video, or the best clips from a long video.
license: MIT
---

# Make reels and short videos with Ignix

Requires the Ignix connector. Ignix only works with an active plan: if a tool says the plan is not active, stop and point the user to https://ignix.social/app/billing.

1. Decide what kind of video it is:
   - A new reel from an idea, a script or a product: `get_reel_playbook`.
   - The user's OWN videos (subtitles, a hook, zooms, cutting pauses, or the best clips from a long video): `get_edit_playbook`.
   - Reels that Autopilot already planned: `list_pending_reels`.
2. Follow the steps the playbook returns, in order. They cover the script, the voice, the scenes, the approvals and the export.
3. Rendering and editing run on the user's computer with Ignix Editor, so they need a terminal (Codex, or a desktop app with one). In a chat without a terminal, prepare the script and the storyboard and tell the user where to finish it.
4. Ask the user to approve the script and the scenes before exporting, and the finished video before posting it with `create_post`.

Rules:
- Tools that spend AI credits (images, voice-over, AI video) first return a quote (what they will do and the credits). Tell the user and wait for a yes before calling again with `confirm: true`.
- Only use footage, faces and voices the user owns or has permission to use.
- Write the script in the language of the account's audience unless told otherwise.
