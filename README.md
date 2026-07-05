# 🛡️ ZONG

**Real-time anti-raid protection for Discord.**

ZONG watches your server's audit log continuously and reacts the instant something destructive happens — mass channel deletions, mass bans, role permission stripping — before an admin even sees the alert.

> This repository is a showcase. ZONG is closed-source and available as a premium product — see [Getting ZONG](#getting-zong) below.

---

## ⚡ Why ZONG

Most anti-raid bots poll for damage after it's already done. ZONG hooks directly into Discord's audit-log event stream, so detection and response happen in the same moment the raid does — typically **under 1 second** from action to response, tested against several established anti-raid/anti-nuke bots.

## 🔍 What it detects

| Pattern | Response |
|---|---|
| Mass channel deletion | Auto kick/ban/quarantine the actor |
| Mass member bans | Auto kick/ban/quarantine the actor |
| Role deletion / permission stripping | Auto kick/ban/quarantine the actor |
| Known nuke-command patterns in chat | Message deleted + actor punished |
| Suspicious recently-joined accounts | Manual or automatic sweep |

Detection is behavior-based, not signature-based — it doesn't matter which tool is driving the destructive action, only the pattern of what's happening to the server.

## 🧰 Feature overview

- **Configurable response** — choose kick, ban, or quarantine as the default action
- **Trusted roles & whitelist** — exempt co-owners, other bots, or specific people from ever being auto-punished
- **Undo safety net** — reverse ZONG's own last automated actions if something gets flagged that shouldn't have been
- **Backup & restore** — snapshot your server's channels and roles, and rebuild anything that gets deleted
- **One-button recovery** — unlock, restore from backup, and alert your team in a single command
- **Raid sweeps** — manually sweep recently-joined suspicious accounts by join window and role count
- **Live alert channel** — every automated action posts straight to a channel you choose
- **Exportable audit trail** — full log history, not just the last few lines
- **Rate-limit aware** — bulk operations (restores, sweeps) automatically back off Discord's API limits instead of failing

## 📸 Screenshots

<!-- Add your own screenshots here, e.g.: -->
<!-- ![Status command](assets/status.png) -->
<!-- ![Raid detected alert](assets/alert.png) -->
<!-- ![Diagnostics](assets/diagnose.png) -->

## 🏗️ Built with

- Python
- [discord.py](https://github.com/Rapptz/discord.py)
- Discord's Audit Log API for real-time behavioral detection

## Getting ZONG

ZONG is available as a premium product. Reach out via the Discord server linked below for access and pricing.

<!-- Add your Discord invite / contact link here -->

## License

All rights reserved. This repository is provided for showcase purposes only — no source code, license to use, or permission to reproduce ZONG's functionality is granted.
