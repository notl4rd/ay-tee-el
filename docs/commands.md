# Command reference

*ay tee el* supports **slash commands** (`/`) and **prefix commands** (default `!`, configurable via `/setup prefix`).
Every command below works in both forms unless noted otherwise.

> **Categories:** [Leveling](#leveling) · [Configuration](#configuration) · [Fun](#fun) · [Economy](#economy) · [Moderation](#moderation) · [Utility](#utility) · [Premium](#premium) · [Music](#music) · [Giveaway](#giveaway) · [Owner](#owner)

---

## Leveling

| Command | Description |
| --- | --- |
| `/level` | Check your level or another user's level (optional `user`) |
| `/leaderboard` | XP / Level leaderboard for the server |

Leveling is configured with `/setup leveling` (enable, XP-only channel, weekend double XP) and `/setuplevels` to create level reward roles.

---

## Configuration

Server setup commands. Most require admin permission.

| Command | Description |
| --- | --- |
| `/language` | Set your personal language (`server` / `user` / `reset`) |
| `/setup` | Main configuration menu — see [subcommands](#setup-subcommands) |
| `/setupcrime` | Enable/disable the `/crime` command |
| `/cmdperm` | Require a role to use a command (`set` / `clear` / `list`) |
| `/ticket` | Ticket management — add/remove users from the current ticket |
| `/setupinviterewards` | Invite reward roles (`add` / `remove` / `list` / `clear`) |
| `/register` | Register system — Boy/Girl roles, panel (`setup` / `panel`) |
| `/setupeconomy` | Economy & gambling settings (min/max bet, daily amount, currency) |
| `/setupsuggest` | Suggestion system (channel + staff role) |
| `/setupmessagelog` | Log deleted & edited messages to a channel |
| `/rolemenu` | Modern role menu — select menu or buttons (`create` / `addrole`) |
| `/setupjail` | Jail system (jail role) |
| `/setupinvites` | Invite tracking with join/leave messages |
| `/reactionrole` | Reaction roles (`add` / `remove` / `list`) |
| `/togglecommand` | Enable or disable a specific command in this server |
| `/supportsetup` | Create the support ticket panel |
| `/setuplevels` | Create level reward roles |

### `/setup` subcommands

| Subcommand | Description |
| --- | --- |
| `antinuke` | Enable/disable Anti-Nuke protection |
| `aifilter` | AI bad-word filter |
| `logchannel` | Set the log channel |
| `autorole` | Auto-roles for new members / bots |
| `leveling` | Leveling system (enable, XP channel, double XP weekends) |
| `ai` | AI chat channels & personality (Premium, off by default) |
| `welcome` | Welcome DM message (`{user}` `{server}` `{mention}`) |
| `welcomeimage` | Image welcome/leave cards in a channel (Premium) |
| `roles` | Add/remove admin & moderator roles |
| `tickets` | Ticket category, support role, abuse role |
| `giveawaychannel` | Channel where giveaways are posted |
| `stats` | Server stats voice channels (Premium) |
| `tempvoice` | Temp voice channel system (Premium) |
| `feed` | YouTube / RSS / Atom / Twitch feeds (Free: 1 platform) |
| `prefix` | Set message prefix (1–5 chars) and enable/disable prefix commands |
| `view` | View the current bot configuration |

---

## Fun

| Command | Description |
| --- | --- |
| `/duel` | Duel another user |
| `/trivia` | Random trivia question |
| `/meme` | Random meme |
| `/joke` | Random joke |
| `/dadjoke` | Random dad joke |
| `/fact` | Random useless fact |
| `/rps` | Rock, paper, scissors against the bot |
| `/ship` | Ship two users together |
| `/wyr` | Would you rather… |
| `/roast` | Roast a user (all in good fun) |
| `/compliment` | Compliment a user |
| `/choose` | Let the bot choose between comma-separated options |
| `/8ball` | Ask the magic 8-ball |
| `/rate` | Rate something out of 10 |

---

## Economy

| Command | Description |
| --- | --- |
| `/balance` | Check your (or another user's) balance |
| `/deposit` | Deposit coins into your bank (`all` supported) |
| `/withdraw` | Withdraw coins from your bank (`all` supported) |
| `/daily` | Redeem your daily coins |
| `/pay` | Give coins to another user |
| `/crime` | Commit a crime for coins (risky!) |
| `/bet` | Gambling hub: `coinflip`, `slots`, `dice`, `roulette`, `double` |
| `/shop` | See the role shop |
| `/buy` | Buy a role from the shop |
| `/addshop` | Add a role to the shop (Manager) |
| `/removeshop` | Remove a role from the shop |
| `/setbalance` | Adjust a user's balance (Manager) |

**Bet games:** coin flip (2×, heads/tails) · slot machine · dice (guess 1–6, ×5) · roulette (red/black ×2, green ×14) · double or nothing.

---

## Moderation

| Command | Description |
| --- | --- |
| `/punish` | Warn / Timeout / Kick / Ban / Blacklist / Force Ban / Soft Ban — with duration, reason & proof |
| `/jail` / `/unjail` | Jail a member (temporarily or until released) |
| `/case` | Moderation case system: `view`, `reason`, `user`, `proof` |
| `/warnings` / `/clearwarnings` | View or clear a user's warnings |
| `/lock` / `/unlock` | Lock or unlock the current channel |
| `/lockdown` | Lock or unlock the **whole server** (anti-raid) |
| `/slowmode` | Set channel slowmode (0–21600s) |
| `/clear` | Delete messages (1–100, optional user filter) |
| `/addrole` / `/removerole` | Give or remove a role |
| `/setnick` | Change a member's nickname (empty = reset) |
| `/modstats` | Show a moderator's moderation stats |
| `/timedrole` | Give a temporary role (`give` / `remove` / `list`) — Premium |
| `/timedrole` … — see also | `/editinvites`, `/unban`, `/unblacklist` |
| `/voicekick` | Disconnect a user from voice (temp voice owner or staff) |
| `/disconnectall` | Disconnect everyone from a temp voice channel |
| `/voicemove` | Move a member to another voice channel |
| `/unban` | Unban a user by ID |
| `/unblacklist` | Unblacklist a user |

---

## Utility

| Command | Description |
| --- | --- |
| `/help` | Show all bot commands |
| `/status` | Bot info (uptime, ping, system stats) |
| `/avatar` | Show a user's avatar |
| `/userinfo` | Information about a user |
| `/serverinfo` | Information about the server |
| `/invite` | Bot invite link + support server |
| `/poll` | Poll with up to 5 options and optional duration |
| `/suggest` | Send a suggestion to your server's suggestion channel |
| `/botsuggest` | Send a suggestion directly to the bot owner (global) |
| `/remind` | Personal reminder (`10m`, `2h`, `1d`…) |
| `/highlight` | Get a DM when a word is said (`add` / `remove` / `list`) |
| `/afk` | Set an AFK status |
| `/snipe` / `/editsnipe` | Show the last deleted / edited message |
| `/translate` | Translate text to a target language |
| `/weather` | Current weather for a city |
| `/birthday` | Birthday system (`set` / `remove` / `setup`) |
| `/invites` | Check a user's invite count |
| `/newusers` | Members who joined recently (default 7 days) |
| `/firstmessage` | Jump to the first message in the channel |

---

## Premium

| Command | Description |
| --- | --- |
| `/redeem` | Redeem a premium code for this server |
| `/backup` | Server backup: `create` / `load` from JSON (Premium, owner only) |
| `/proxy` | Send an anonymous message via webhook (Premium) |
| `/roleall` | Give or remove a role from everyone (Premium) |
| `/allowedbots` | Manage which bots may join the server (`Add` / `Remove` / `List`) |

See [docs/premium.md](premium.md) for plans and activation.

---

## Music / Radio

| Command | Description |
| --- | --- |
| `/fm` | Worldwide FM & internet radio |
| └ `play` | Search and play a station |
| └ `search` | Search stations without playing |
| └ `top` | Play one of the most popular stations |
| └ `random` | Play a random station |
| └ `country` | Play a station from a country (e.g. `Turkey`, `Germany`) |
| └ `genre` | Play by genre (`lofi`, `jazz`, `rock`, `news`, `pop`…) |
| └ `stop` | Stop the radio and leave the voice channel |
| └ `nowplaying` | Show the currently playing station |
| └ `volume` | Change volume (0–100) |

---

## Giveaway

| Command | Description |
| --- | --- |
| `/giveaway` | Create a giveaway (`duration`, `prize`, `winners`) |
| `/endgiveaway` | End a giveaway early by message ID |

---

## Owner

Staff-only commands for the bot owner.

| Command | Description |
| --- | --- |
| `/premium` | Premium management: `grant`, `revoke`, `check`, `generate`, `listcodes` |
| `/reboot` | Restart the bot |

---

## Additional feature commands

Registered per-server (guild commands):

| Command | Description |
| --- | --- |
| `/sticky` | Sticky messages — `set`, `remove`, `list` (reposts on delete) |
| `/modmail` | DM mail system — `setup`, `disable`, `status`, `close`, `ban`, `unban`, `banlist` |
| `/altprotect` | Alt-account protection — `enable` (days, action: timeout/kick/verify), `disable`, `status` |
| `/summarize` | AI summary of the last 50–100 messages (Premium) |

---

## Permission levels

Most commands respect these roles (configurable in the dashboard / `/setup roles`):

- **Admin role** — full access to setup and administration commands.
- **Moderator role** — moderation commands (`punish`, `jail`, `lock`, `clear`, …).
- **Per-command roles** — `/cmdperm set` requires a specific role for a specific command.
- **Manager-only** — economy shop editing (`/addshop`, `/setbalance`).
- **Owner only** — `/premium`, `/reboot`, `/backup`.

> Tip: use `/togglecommand` to disable a command entirely for your server.
