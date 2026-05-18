# Changelog

All notable changes to this skill are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this skill adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] — 2026-05-18

### Added

- Initial release.
- Three-role mental model (`ig-post` / `ig-engage` / `ig-stealth`) for any Instagram account — business, creator, or personal.
- **Meta Business Suite as the only sane automation surface**: all DM + comment ops run through `business.facebook.com`, never against `instagram.com` directly. Canonical MBS URLs per tab (all, Messenger, Instagram DMs, IG comments, FB comments).
- **Playwright click + type + Enter flow** (DMs) and `@username` prefix + page-level textarea + send-arrow (comments) — both validated end-to-end. Documents the MBS "Reply-navigates-to-wrong-post" SPA bug and its workaround.
- **Action-block awareness**: tiered penalty system (24 h warning / 7 d second offense / permanent third+). Documented observed frequency thresholds per action type (follow, comment, proactive DM, like, post). Phase A / Phase B gating logic.
- **Comment + DM doctrine**: qualification rules for inbound threads, brand link policy (zero URLs in comment bodies; max one URL in DMs, never a shortener), reply template structure for Phase A and Phase B, and Reel-share skip logic.
- **Hashtag-shadowban discipline**: 3–5 hashtags per post (1 broad + 2–3 niche + 1 micro < 50k posts), monthly `ig-hashtag-state.md` registry check.
- **Reply qualification**: thread age, existing client recognition (`ig-clients-known.md`), 7-day dedupe window, Phase gating checks.
- **Hard quotas** calibrated under action-block thresholds: per-run and per-24h limits for DMs, comment replies, outbound DMs, follows, unfollows, and likes; minimum inter-action delays (15–60 s depending on phase).
- **Recovery playbook**: `status:stopped`, session expired, "Reauthenticate" banner, action-block toast, re-captcha, SPA error, comment Reply bug, overnight follower drop, consecutive comment removals.
- **Memory file inventory** (9 files): `ig-alerts-sent.md`, `ig-clients-known.md`, `ig-hashtag-state.md`, `ig-ideas.md`, `ig-learnings.md`, `ig-post-log.md`, `ig-recaps.md`, `ig-reply-log.md`, `ig-state.md`.
- Mandatory recap pattern: alert channel message template + `ig-recaps.md` append format.
- Phase A → Phase B transition logic with manual user confirmation required.
- Stability discipline (read before click, one-click-then-snapshot, tab-settle wait).
- First-run checklist (11 items) and FAQ (7 questions).
- `install.sh` for one-command install into Claude Code or OpenClaw skills directories.
- `init-memory.sh` for interactive or non-interactive memory dir bootstrap; idempotent.

[1.0.0]: https://github.com/AlexBloch-IA/instagram-account-operations/releases/tag/v1.0.0
