# ay tee el — Documentation

<p align="center">
  <img src="https://ayteeel.cfd/atlantis-banner.png" alt="ay tee el banner" width="720" />
</p>

<p align="center">
  <b>Multi-purpose Discord bot — Moderation, Leveling, Economy, Music, Tickets, AI &amp; a clean web dashboard.</b>
</p>

<p align="center">
  <a href="https://discord.com/api/oauth2/authorize?client_id=1096149126888050809&permissions=8&scope=bot%20applications.commands"><img src="https://img.shields.io/badge/Invite-ay%20tee%20el-5865F2?style=for-the-badge&logo=discord&logoColor=white" alt="Invite" /></a>
  <a href="https://discord.gg/EEHuxXM97H"><img src="https://img.shields.io/badge/Support-Server-7289DA?style=for-the-badge&logo=discord&logoColor=white" alt="Support" /></a>
  <a href="https://ayteeel.cfd"><img src="https://img.shields.io/badge/Dashboard-ayteeel.cfd-3ba55d?style=for-the-badge" alt="Dashboard" /></a>
</p>

---

> **About this repository**
> This is the **public documentation repository** for *ay tee el*. It contains guides, the full command reference, feature docs and FAQs in Markdown.
> **No source code is published here.** The bot is closed source; see [License](#license).

## Table of contents

- [Overview](#overview)
- [Quick start](#quick-start)
- [Documentation](#documentation)
- [Key features](#key-features)
- [Premium](#premium)
- [Links](#links)
- [FAQ](#faq)
- [License](#license)

## Overview

*ay tee el* is an all-in-one Discord bot built for communities that want one tool instead of ten:

- **Slash commands + prefix commands** — every command works as `/command` or `!command` (configurable prefix).
- **Multi-language** — 16 interface languages (EN, TR, DE, FR, ES, PT, RU, PL, NL, JA, KO, ZH, AR, LV, LT, ET). Per-server *and* per-user language settings.
- **Web dashboard** — configure everything from [ayteeel.cfd](https://ayteeel.cfd): plugins, permissions, logs, feeds and Premium.
- **Optional MongoDB Atlas storage** — runs with cloud persistence, with a local file fallback mode.

## Quick start

1. **Invite the bot** → [Add ay tee el to your server](https://discord.com/api/oauth2/authorize?client_id=1096149126888050809&permissions=8&scope=bot%20applications.commands)
2. **Open the dashboard** → [ayteeel.cfd/dashboard](https://ayteeel.cfd/dashboard) and sign in with Discord.
3. **Run `/setup`** in your server to open the main configuration menu (anti-nuke, logs, autorole, leveling, AI, welcome, roles, tickets, feeds, prefix…).
4. **Type `/help`** (or `!help`) to browse all commands in Discord.
5. **Join the support server** → [discord.gg/EEHuxXM97H](https://discord.gg/EEHuxXM97H)

## Documentation

| Guide | Description |
| --- | --- |
| [Command reference](docs/commands.md) | Every command, grouped by category (100+ commands) |
| [Features](docs/features.md) | Deep dives: modmail, sticky, tickets, economy, feeds, anti-nuke… |
| [Premium](docs/premium.md) | Plans, premium features, redemption and billing FAQ |
| [FAQ & troubleshooting](docs/faq.md) | Common questions and fixes |

## Key features

| Area | What you get |
| --- | --- |
| **Moderation** | Punish (warn/timeout/kick/ban/soft-ban/force-ban/blacklist), jail, case system with proofs, lockdown, slowmode, message & edit snipe, mod stats |
| **Protection** | Anti-nuke with role/permission backups, AI bad-word filter, alt-account protection (account age checks), raid lockdown |
| **Tickets** | Panel-based support tickets, transcripts, abuse roles, `/modmail` DM gateway with private threads |
| **Leveling** | XP with weekend double XP, leaderboards, level reward roles |
| **Economy** | Coins, bank, daily rewards, role shop, gambling (coinflip, slots, dice, roulette, double) with staff-set limits |
| **Music & Radio** | Worldwide FM/radio stations by country, genre, top and random — `/fm` |
| **Utility** | Reminders, highlights, translate, weather, birthdays, polls, suggestions, AFK, invites tracking, userinfo/serverinfo |
| **Engagement** | Welcome/leave cards (image, Premium), reaction roles, role menus, giveaways, invite rewards, register (gender) system |
| **Automation** | Sticky messages, RSS/Atom/Twitch/YouTube feeds, timed roles, auto-logs, autorole, custom commands |
| **AI** | AI chat with personalities (friendly, savage, professional, gen-z), `/summarize` chat summaries (Premium) |
| **Dashboard** | Full web control panel, command permission editor, blog and docs site |

## Premium

Premium unlocks AI chat, temp voice channels, server stats voice channels, YouTube feeds, anti-raid, timed jail, image welcome cards and more.

- **Monthly** — $1.99/month
- **Yearly** — $19.99/year ($1.66/month)

Activate with `/redeem code:<code>` or buy directly from the [dashboard](https://ayteeel.cfd/dashboard). Full details: [docs/premium.md](docs/premium.md).

## Links

| | |
| --- | --- |
| 🌐 Website / Dashboard | [https://ayteeel.cfd](https://ayteeel.cfd) |
| ✉️ Invite | [Add to your server](https://discord.com/api/oauth2/authorize?client_id=1096149126888050809&permissions=8&scope=bot%20applications.commands) |
| 💬 Support server | [discord.gg/EEHuxXM97H](https://discord.gg/EEHuxXM97H) |
| 📖 Command reference | [docs/commands.md](docs/commands.md) |
| 🛡️ Privacy · Terms · License | [ayteeel.cfd/privacy](https://ayteeel.cfd/privacy) · [ayteeel.cfd/terms](https://ayteeel.cfd/terms) · [ayteeel.cfd/license](https://ayteeel.cfd/license) |

## FAQ

<details>
<summary><b>Is the bot free?</b></summary>

Yes. The core bot — moderation, leveling, economy, tickets, utility, fun and radio — is free. A separate Premium subscription unlocks the advanced systems listed above.
</details>

<details>
<summary><b>Is the source code public?</b></summary>

No. This repository only contains documentation. The source code is closed and is not distributed here.
</details>

<details>
<summary><b>Prefix commands stopped responding.</b></summary>

Make sure **Message Content Intent** is enabled for the bot in your server (Server Settings → Integrations), and check that the prefix hasn't been changed with `/setup prefix`. See [docs/faq.md](docs/faq.md).
</details>

<details>
<summary><b>How do I get help?</b></summary>

Join the [support server](https://discord.gg/EEHuxXM97H) and open a ticket, or use the dashboard's support chat.
</details>

More answers: [docs/faq.md](docs/faq.md)

## License

Documentation in this repository is provided for reference only.

```
Copyright © - Atlantis Studios
```

The *ay tee el* bot software, name, logo and branding are proprietary. You may read and link to this documentation, but you may **not** redistribute it as your own, and no rights to the bot's source code are granted by this repository.

See [ayteeel.cfd/license](https://ayteeel.cfd/license) for the full license text.
