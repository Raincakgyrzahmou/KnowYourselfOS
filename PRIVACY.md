# Privacy

Know Yourself OS is built so that your most honest answers stay yours. This document explains exactly what happens to your data — no marketing, just the facts.

## The short version

- Your entries are stored **only in your own browser** (`localStorage`, key `knowYourselfOS_v2`).
- There is **no server, no database, no account, no analytics, and no tracking** in this app.
- **No one can read your answers** through this software, because nothing is transmitted to or stored by anyone — with one opt-in exception below.

## Local storage

Everything you type — pillar answers, distilled truths, experiments, daily check-ins, journal entries, mission, weekly plans, and your settings — is written to your browser's `localStorage` on the device you're using. It does not sync, upload, or back up anywhere automatically. If you clear your browser data or use the in-app **Reset all data**, it is permanently gone.

## The one exception: optional AI generation

The ✨ *Generate* buttons (distill, mission, weekly plan, intention suggestions, reset reframe, weekly summary) are **optional**. The app is fully usable by hand with no AI and no network connection at all.

When — and only when — you tap a Generate button:

1. The relevant section's text (e.g. that pillar's answers) is sent **directly from your browser** to the AI provider you configured.
2. That provider is either:
   - **Anthropic's API**, using the API key *you* entered in Settings (stored only on your device, sent via the official `api.anthropic.com` endpoint with the direct-browser-access header), or
   - **Claude inside Cowork**, if you're running the app there.
3. The provider returns the generated text, which is saved to your local storage like anything else.

This app does not add any intermediary. Your data goes from your browser to the provider and back. The provider's own handling of API requests is governed by their terms and privacy policy (for Anthropic, see their [privacy policy](https://www.anthropic.com/legal/privacy) and [commercial terms](https://www.anthropic.com/legal/commercial-terms); API inputs are generally not used to train models).

If you want **zero data to ever leave your device**, do not enter an API key and do not use the Generate buttons. Type your own distillations and plans — the system works completely without AI.

## Your API key

If you choose to use your own Anthropic key, it is stored in `localStorage` on your device and sent only to Anthropic on requests you trigger. It is never sent anywhere else. Anyone with physical or remote access to your browser profile could read it (as with any locally stored credential), so use this on a device you trust, and clear the key in Settings when you're done if you're on a shared machine.

## If you deploy this publicly

This app never embeds an API key in its code. Each visitor would enter their own key, stored in their own browser. So hosting the page publicly does not expose any secret of yours. Do **not** modify the code to hard-code a key into a public deployment — instead route AI calls through your own serverless proxy.

## Questions

Open an issue. But remember: the most private setup is the default one — just don't turn on AI.
