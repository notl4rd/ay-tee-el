# FAQ & troubleshooting

Quick answers to the most common questions about *ay tee el*.

---

## General

<details>
<summary><b>How do I invite the bot?</b></summary>

Use the invite link: **[Add ay tee el to your server](https://discord.com/api/oauth2/authorize?client_id=1096149126888050809&permissions=8&scope=bot%20applications.commands)**

You need **Manage Server** permission on the target server.
</details>

<details>
<summary><b>Is the bot free?</b></summary>

Yes — moderation, leveling, economy, tickets, utility, fun and radio are free. Premium adds AI, temp voice, stats, feeds and more. See [premium.md](premium.md).
</details>

<details>
<summary><b>Where can I configure everything?</b></summary>

Two places:

1. **In Discord** — `/setup` opens the main configuration menu.
2. **Web dashboard** — [ayteeel.cfd/dashboard](https://ayteeel.cfd/dashboard), sign in with Discord.
</details>

<details>
<summary><b>Is the source code public?</b></summary>

No. Only this documentation is public; the bot is closed source.
</details>

---

## Commands

<details>
<summary><b>Slash commands don't appear in Discord.</b></summary>

1. Re-invite with the `applications.commands` scope: [invite link](https://discord.com/api/oauth2/authorize?client_id=1096149126888050809&permissions=8&scope=bot%20applications.commands).
2. Commands are registered per-server — they can take up to **an hour** to appear globally, or refresh immediately after the bot joins.
3. Someone may have disabled it: check `/togglecommand`.
4. Still missing? Ask in the [support server](https://discord.gg/EEHuxXM97H).
</details>

<details>
<summary><b>Prefix commands (!help) don't respond.</b></summary>

- **Message Content Intent** must be enabled: Server Settings → Integrations → *ay tee el* → enable *Message Content Intent*.
- The prefix may have been changed — check with `/setup prefix` (1–5 characters) and make sure prefix commands are enabled there.
- In DMs, prefix commands are limited by Discord's intents.
</details>

<details>
<summary><b>A command says "You need permission".</b></summary>

You need the **admin**, **moderator** or a command-specific role. Ask an admin to:
- set roles via `/setup roles admin:` / `mod:`
- or grant a single command with `/cmdperm set command: role:`
</details>

<details>
<summary><b>Can I disable a command for my server?</b></summary>

Yes: `/togglecommand command:<name> enabled:false`.
</details>

---

## Music & radio

<details>
<summary><b>The radio won't play / bot doesn't join voice.</b></summary>

- Make sure the bot has **Connect** and **Speak** permissions in the voice channel.
- Try another station — some upstream stations go offline.
- Use `/fm stop` then `/fm play` again to reset the connection.
</details>

<details>
<summary><b>Audio is choppy.</b></summary>

Voice quality depends on the host's connection to the station. Try `/fm volume` lower, pick a different station, or switch to a voice channel closer to the bot's region (Server Settings → Overview → Server Location).
</details>

---

## Features

<details>
<summary><b>Modmail DMs are being ignored.</b></summary>

- The bot must be **in a server where modmail is enabled** and you must be a **member of that server**.
- Staff: run `/modmail status` — the channel must exist and be a normal text channel.
- If you were blacklisted, staff can lift it with `/modmail unban`.
- Diagnostics: type `.modmail` in the bot's DMs — it lists which servers are available to you.
</details>

<details>
<summary><b>Sticky message stopped reposting.</b></summary>

- `/sticky list` to confirm it's set, `/sticky set` to recreate it.
- The bot needs **Manage Messages** in that channel.
- Sticky messages don't repost inside threads.
</details>

<details>
<summary><b>Leveling / XP isn't awarding.</b></summary>

- Enable it: `/setup leveling enabled:true`
- Check for an **XP-only channel** restriction (if set, only that channel grants XP).
- Bots and the bot's own messages never earn XP.
</details>

<details>
<summary><b>Feeds aren't posting.</b></summary>

- Free plan supports **1 platform** — Premium unlocks all.
- YouTube needs a channel ID starting with `UC`.
- Feeds poll every **10 minutes**; new posts appear with a small delay.
- `/setup feed list` to verify the feed and target channel.
</details>

<details>
<summary><b>Invites show 0 / aren't tracked.</b></summary>

- Enable with `/setupinvites enabled:true`.
- Only **vanity and instant invites created while the bot was present** are tracked; existing invite counts can be corrected with `/editinvites`.
- The bot needs the **Manage Guild (server)** permission to read invites.
</details>

<details>
<summary><b>Welcome cards aren't sending.</b></summary>

- Channel welcome/leave **image cards are Premium** — check `/redeem`.
- Set both message and channel: `/setup welcomeimage`
- The bot needs permission to send messages (and embed links) in the target channel.
- Welcome **DMs** may be blocked if the user has DMs closed or rejects server DMs.
</details>

---

## Dashboard & account

<details>
<summary><b>I can't sign in to the dashboard.</b></summary>

- Use the **Login with Discord** button and approve the OAuth prompt.
- Make sure you're signed into the correct Discord account.
- Clear cookies for the site and try again, or use a private window.
</details>

<details>
<summary><b>The dashboard doesn't show my server.</b></summary>

You must be an **administrator** (Manage Server) on that server, and the bot must be a member of it.
</details>

<details>
<summary><b>My Premium purchase didn't activate.</b></summary>

Purchases apply automatically to the server selected at checkout. If it's missing, contact the bot owner in the [support server](https://discord.gg/EEHuxXM97H) with your receipt. See [premium.md](premium.md).
</details>

---

## Still stuck?

Join the **[support server](https://discord.gg/EEHuxXM97H)** and open a ticket — include:

1. The command you ran (and the exact error message)
2. Server ID and channel
3. Whether it happens in other servers too
