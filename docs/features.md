# Features

A deep dive into *ay tee el*'s systems. For the full command list see [commands.md](commands.md).

---

## Table of contents

- [Moderation & case system](#moderation--case-system)
- [Protection: anti-nuke, AI filter, alt protection](#protection-anti-nuke-ai-filter-alt-protection)
- [Modmail (DM gateway)](#modmail-dm-gateway)
- [Tickets](#tickets)
- [Sticky messages](#sticky-messages)
- [Leveling](#leveling)
- [Economy](#economy)
- [Invites & register](#invites--register)
- [Welcome & leave cards](#welcome--leave-cards)
- [Reaction roles & role menus](#reaction-roles--role-menus)
- [Feeds: YouTube / RSS / Twitch](#feeds-youtube--rss--twitch)
- [Music & radio](#music--radio)
- [AI chat & summarize](#ai-chat--summarize)
- [Giveaways](#giveaways)
- [Temp voice & server stats](#temp-voice--server-stats)
- [Web dashboard](#web-dashboard)
- [Multi-language](#multi-language)

---

## Moderation & case system

Every punishment goes through `/punish`, which supports:

| Action | Notes |
| --- | --- |
| Warn | Recorded in the case log |
| Timeout | Up to Discord's 28-day limit, with duration |
| Kick | With reason + optional proof screenshot |
| Ban | With duration (temporary bans auto-expire) |
| Force Ban | Ban without the member needing to be in the server |
| Soft Ban | Ban + immediate unban to purge messages |
| Blacklist | Blocks the user from the bot's services |

**Case system** — each action creates a numbered case:

- `/case view id:<n>` — view a case (action, target, moderator, reason, proof)
- `/case reason id:<n>` — update the reason
- `/case user user:@user` — list all cases for a user
- `/case proof id:<n>` — attach or update a proof screenshot

**Extra tools:** `/jail` & `/unjail` (isolated jail role), `/lockdown` (server-wide anti-raid lock), `/slowmode`, `/clear` (bulk delete with user filter), `/modstats` (per-moderator statistics), `/timedrole` (temporary roles, Premium).

Moderation activity can be logged to a channel with `/setup logchannel`.

---

## Protection: anti-nuke, AI filter, alt protection

### Anti-Nuke
Enabled via `/setup antinuke`. Backs up your server's roles and permission structure so that a mass role deletion or permission escalation (typical "nuke" attack) can be detected and reversed. Backups are stored per-server.

### AI bad-word filter
`/setup aifilter` — uses AI to catch insults, slurs and disguised bypasses that simple keyword filters miss.

### Alt-account protection
`/altprotect enable` — reacts when an account younger than **X days** joins:

- **Action:** `timeout` (with minutes), `kick`, or `verify` (role-gated verification)
- `/altprotect status` / `/altprotect disable`

### Raid lockdown
`/lockdown lock` instantly locks every channel in the server; `/lockdown unlock` reverts it.

---

## Modmail (DM gateway)

Lets members contact your staff team **privately, from DMs** — messages are forwarded into a **private thread** in your staff channel.

**Setup (staff):**
```
/modmail setup channel:#modmail role:@Support
```

**How it works:**

1. A user DMs the bot. If they're a member of multiple servers with modmail enabled, they get a **select menu** to pick the server.
2. A private thread (`mail-username`) is created in your configured channel. Only staff and the assigned role can see it.
3. The user's message (and attachments) is posted in the thread.
4. Staff reply **in the thread** — the reply is delivered to the user's DMs.
5. `/modmail close` archives + locks the thread (deletion is optional via button). The user is notified.

**Extras:**
- `/modmail ban` / `unban` / `banlist` — per-server blacklist (blocked users can't open tickets on *that* server)
- `.modmail` in DMs — diagnostic reply showing which servers are available
- `close` / `kapat` in DMs — the user can close their own ticket
- Threads auto-archive after 10 minutes–7 days (Discord archive setting) and are re-opened automatically when needed

---

## Tickets

A classic panel-based support system:

- `/supportsetup` creates the panel with a button.
- Clicking the button opens a ticket channel in your configured **category**, visible to the **support role**.
- Staff can `/ticket add` / `/ticket remove` users.
- Configurable: support role, abuse role (given to users who spam tickets), transcript recording.

Ticket transcripts preserve the conversation for review after the ticket is closed.

---

## Sticky messages

`/sticky set channel:#rules text:"..."` — the message is **reposted at the bottom** every time someone writes in the channel, so rules/announcements never get buried.

- New message in channel → old sticky is deleted, new one posted at the bottom
- Sticky message deleted manually → bot reposts it immediately
- `/sticky remove` and `/sticky list` to manage
- Rate-limit protection (1.5s cooldown per channel)
- Sticky entries added from the dashboard are automatically re-posted if the message disappears

---

## Leveling

- Members earn XP for chatting; `/level` shows a rank card, `/leaderboard` shows the top members.
- **Weekend double XP** toggle (`/setup leveling doublexp`)
- Optional XP-only channel restriction
- `/setuplevels` creates **level reward roles** that are granted automatically
- Fully configurable from the dashboard

---

## Economy

A complete coin economy with a **bank** and a **role shop**:

| Command | Purpose |
| --- | --- |
| `/balance` | Cash + bank balance |
| `/deposit` `/withdraw` | Move coins between wallet and bank |
| `/daily` | Daily reward (amount configurable) |
| `/pay` | Transfer coins |
| `/crime` | Risky gamble for coins |
| `/shop` `/buy` | Purchase roles with coins |
| `/addshop` `/removeshop` | Staff manages shop items |

**Gambling** (`/bet`): coinflip (2×) · slots · dice (×5) · roulette (red/black ×2, green ×14) · double-or-nothing.

Staff control the economy with `/setupeconomy`: minimum/minimum bet, minimum balance to gamble, daily reward amount, currency name. Limits prevent inflation and casino abuse.

---

## Invites & register

**Invite tracking** (`/setupinvites`):
- Tracks who invited whom, `/invites` shows counts
- Custom join/leave messages with `{user}` `{inviter}` `{invites}` variables
- `/setupinviterewards` — grant roles at invite milestones
- `/editinvites` — staff can correct a count

**Register system** (`/register`):
- `/register setup` — male/female roles + register channel
- `/register panel` — sends a panel users click to register
- Useful for servers that separate members by gender

---

## Welcome & leave cards

Two flavours:

1. **Welcome DM** (`/setup welcome`) — direct message with `{user}` `{server}` `{mention}` variables.
2. **Image cards** (`/setup welcomeimage`, **Premium**) — rendered cards posted in a channel:
   - Join message `{user}` `{server}` `{membercount}`
   - Leave message (goodbye) with the same variables
   - Custom background image URL
   - Seasonal auto-themes (spring/summer/autumn/winter)

---

## Reaction roles & role menus

- **Reaction roles** — `/reactionrole add message_id emoji role:` — classic emoji → role mapping
- **Role menus** (`/rolemenu`) — a modern dropdown or button menu:
  - `/rolemenu create title: type:select|button`
  - `/rolemenu addrole message_id role label emoji description`
- Roles are granted/removed live as members click

---

## Feeds: YouTube / RSS / Twitch

`/setup feed` — new content is posted to your channel automatically.

| Platform | Input |
| --- | --- |
| YouTube | Channel ID (`UC…`) — video uploads |
| RSS / Atom | Feed URL — blog posts, news |
| Twitch | Channel name — VODs |

- Free plan: **1 platform**, Premium: all platforms
- Polled every 10 minutes
- Multiple feeds per server, managed with `/setup feed add|remove|list`

---

## Music & radio

`/fm` brings **worldwide internet radio** into voice channels:

- Search by station name, play by **country** or **genre** (lofi, jazz, rock, news, pop…)
- `top` and `random` for discovery
- `nowplaying`, `volume` (0–100), `stop`
- Powered by `@discordjs/voice` with opus audio for high quality

---

## AI chat & summarize

**AI chat** (`/setup ai`, **Premium**, disabled by default):
- Designate channels where the bot replies
- Personalities: **Friendly · Savage · Professional · Gen Z**
- Powered by multiple AI providers with automatic fallback

**`/summarize`** (**Premium**) — summarizes the last 50–100 messages of a channel into a short digest. Handy after being away from a busy channel.

---

## Giveaways

- `/giveaway duration:10m prize:"Nitro" winners:1` — creates an embed with a join button
- Ends automatically, or early with `/endgiveaway messageid:`
- Winner count and entries are validated by Discord roles/reactions
- Optional dedicated giveaway channel (`/setup giveawaychannel`)

---

## Temp voice & server stats (Premium)

**Temp voice** (`/setup tempvoice`):
- Create a "Join to Create" hub channel
- When a user joins, a personal voice channel is created for them
- Owner can `/voicekick`, `/disconnectall`, `/voicemove`

**Server stats** (`/setup stats`):
- Auto-updating voice channels showing: members, online, visits, server count
- Updated continuously by the bot

---

## Web dashboard

Everything is manageable at **[ayteeel.cfd](https://ayteeel.cfd)**:

- Sign in with Discord (OAuth2)
- Toggle plugins, edit welcome/leveling/ticket settings, manage feeds
- Per-command permission editor
- Premium purchase & activation
- Privacy, terms and license pages, plus a blog

---

## Multi-language

16 languages available — set the server default with `/language server`, or your personal preference with `/language user`.

English · Türkçe · Deutsch · Français · Español · Português · Русский · Polski · Nederlands · 日本語 · 한국어 · 中文 · العربية · Latviešu · Lietuvių · Eesti

Command descriptions and bot replies follow the selected language automatically; missing strings fall back to English.
