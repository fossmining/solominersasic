# DATUM Verified for Umbrel

An Umbrel community app store that installs **DATUM Verified**: Discord and
Telegram bots that give miners access to your community only after they prove
they mine through a DATUM Gateway.

## How it works

1. A member proves they own a Bitcoin address.
2. The bots check that the address is submitting DATUM Gateway shares.
3. The member gets your verified role on Discord, or access in your Telegram chat.
4. The bots recheck every 24 hours. Access is removed only when every pool
   answers and none of them still show fresh DATUM shares, so a pool outage
   never strips access.

Discord and Telegram are supported. You can enable one or both, and add as many
Discord servers or Telegram communities as you want. Members verify once and
are unlocked in every configured community.

## Install

1. Open **App Store** on your Umbrel.
2. Click **⋮** (top right) → **Community App Stores**.
3. Paste `https://github.com/fossmining/solominersasic` and click **Add**.
4. Open the new store and install **DATUM Verified**.
5. Open the app and paste your bot settings in the browser. The bots stay off
   until you save.

The app uses port `30047`.

## Set up the bots

**Discord**
- Create one bot in the Discord Developer Portal.
- Invite it to each server with **Manage Roles**. Its own role must sit higher
  than the verified role.
- Add the bot token, application id, and each server id with its verified role id.

**Telegram**
- Create one bot with BotFather.
- Add it to each community as an admin with **Invite users** and **Ban users**.
- Send `/chatid` in each community and add those chat ids.

## Moving from the older store

DATUM Verified used to be published as `datum-verified` in the DATUM Verified
store. Umbrel treats apps from a different store as different apps, and both
use port `30047`, so:

1. Note your settings: the bot tokens and the server and chat ids.
2. Uninstall the old app.
3. Install DATUM Verified from this store and enter the settings again.

## Source

The bots and the app image are built from
[datum-gateway-verify-bot](https://github.com/fossmining/datum-gateway-verify-bot).
App ids in this store must start with the store id (`solominers-`) or Umbrel
will not list them.
