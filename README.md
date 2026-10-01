# solominers Umbrel App Store

A community app store for umbrelOS with the solominers mining apps.

| App | What it does | Port |
| --- | --- | --- |
| **DATUM BTCB2** (`solominers-datum-gateway-btcb2`) | BLAKE2b DATUM Gateway pre-configured for the BTCB2 pool (`datum.btcb2.com:28915`). Your node builds the templates; miners connect on your LAN. | stratum `23340`, dashboard `21010` |
| **DATUM Verified** (`solominers-datum-verified`) | Discord and Telegram bots that verify members are mining through a DATUM Gateway before granting access. | `30047` |

## Add the store to your Umbrel

1. Open **App Store** on your Umbrel.
2. Click **⋮** (top right) → **Community App Stores**.
3. Paste `https://github.com/yudikorsou/solominersasic` and click **Add**.
4. Open **solominers** and install the apps you want.

## Moving from the older stores

These apps used to be published as `btcb2-datum-gateway-btcb2` (BTCB2 store)
and `datum-verified`. Umbrel treats apps from a different store as different
apps, and they use the same ports, so:

1. Note your settings: the payout address in the gateway's Config tab, and the
   Discord/Telegram bot tokens and server/chat ids in DATUM Verified.
2. Uninstall the old app.
3. Install the same app from **solominers** and enter the settings again.
4. Point miners at `stratum+tcp://<umbrel-lan-ip>:23340` as before.

## Layout

```text
umbrel-app-store.yml
solominers-datum-gateway-btcb2/
solominers-datum-verified/
```

App ids must start with the store id (`solominers-`) or Umbrel will not list
them.
