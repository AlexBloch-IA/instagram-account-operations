# Instagram Account Operations

> Keep an automated Instagram account out of action blocks — Meta Business Suite DMs, comments, quotas. Use when scheduling IG replies from a cron or agent. Trigger on "instagram bot", "action blocked", "instagram dm automation", "reply to instagram comments", "instagram shadowban".

[![License: MIT-0](https://img.shields.io/badge/License-MIT--0-blue.svg)](https://opensource.org/licenses/MIT-0)
[![ClawHub](https://img.shields.io/badge/ClawHub-Published-orange)](https://clawhub.ai/alexbloch-ia/skills/instagram-account-operations)
[![Version](https://img.shields.io/badge/version-2.0.1-green)](https://clawhub.ai/alexbloch-ia/skills/instagram-account-operations)

A Claude Code / [OpenClaw](https://openclaw.ai) skill, published on [ClawHub](https://clawhub.ai/alexbloch-ia/skills/instagram-account-operations). Portable operating doctrine — drop it into an agent's skills directory and follow it.

---

## What the doctrine covers

- Configure
- Meta Business Suite is the only surface
- Session check
- Phase gating
- Quotas
- Posting cadence and hashtags
- Qualify before replying
- Reply templates
- MBS flow
- MBS flow
- Content rules
- Identity and conduct

The full, load-bearing detail lives in [`SKILL.md`](./SKILL.md).

---

## Install

### Via ClawHub (recommended)

👉 **<https://clawhub.ai/alexbloch-ia/skills/instagram-account-operations>**

```bash
clawhub install instagram-account-operations
# or, from an OpenClaw agent:
openclaw skills install @alexbloch-ia/instagram-account-operations
```

### Via this repository (manual)

```bash
git clone https://github.com/AlexBloch-IA/instagram-account-operations.git
cd instagram-account-operations
./install.sh
```

The script copies the full skill payload into every supported stack it finds:

- `~/.claude/skills/instagram-account-operations/` (Claude Code)
- `~/.openclaw/skills/instagram-account-operations/` (OpenClaw)

### Manual copy

```bash
mkdir -p ~/.claude/skills/instagram-account-operations
cp -R SKILL.md ~/.claude/skills/instagram-account-operations/   # plus scripts/, references/, templates/… if present
```

---

## Repository structure

```
instagram-account-operations/
├── SKILL.md
├── README.md
├── LICENSE
└── install.sh
```

---

## License

Released under **MIT-0** (MIT No Attribution). Use, fork, adapt, redistribute — no attribution required.

---

## Author

[Alexandre Bloch](https://github.com/AlexBloch-IA) — founder of [OpenClaw](https://openclaw.ai).
Published on [ClawHub](https://clawhub.ai/alexbloch-ia).
