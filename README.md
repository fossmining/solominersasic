# solominers Umbrel App Store

A community app store for umbrelOS with the DATUM Verified app.

| App | What it does | Port |
| --- | --- | --- |
| **DATUM Verified** (`solominers-datum-verified`) | Discord and Telegram bots that verify members are mining through a DATUM Gateway before granting access. | `30047` |

## Add the store to your Umbrel

1. Open **App Store** on your Umbrel.
2. Click **⋮** (top right) → **Community App Stores**.
3. Paste `https://github.com/yudikorsou/solominersasic` and click **Add**.
4. Open **solominers** and install the apps you want.

## Moving from the older stores

DATUM Verified used to be published as `datum-verified` (DATUM Verified
store). Umbrel treats apps from a different store as different apps, and they
use the same port, so:

1. Note your settings: the Discord/Telegram bot tokens and server/chat ids.
2. Uninstall the old app.
3. Install DATUM Verified from **solominers** and enter the settings again.

## Layout

```text
umbrel-app-store.yml
solominers-datum-verified/
```

App ids must start with the store id (`solominers-`) or Umbrel will not list
them.
