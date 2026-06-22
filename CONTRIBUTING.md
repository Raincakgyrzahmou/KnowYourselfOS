# Contributing

Thanks for being here. This project is meant to be forked, remixed, and made personal — so contributions of all sizes are welcome.

## Ways to contribute

- **Improve the questions.** The 10 pillars are a starting point, not scripture. Sharper, kinder, or more universal prompts are valuable.
- **Add a module.** Trend charts, new pillars, encrypted export, etc. (see the roadmap in the README).
- **Translations.** The app is bilingual EN/中文; more languages are welcome.
- **Bug fixes & accessibility.** Keyboard navigation, screen-reader labels, contrast.
- **Docs.** Clearer setup, better examples, screenshots.

## Ground rules

1. **Stay private by default.** Any contribution must keep the no-server, local-first, no-tracking promise. Features that phone home, add analytics, or store user data remotely will not be merged.
2. **Stay dependency-free.** The whole app is one self-contained `index.html` with vanilla JS. Please don't add build steps, bundlers, or runtime dependencies. (CDN libraries are avoided on purpose.)
3. **AI stays optional.** Every feature must work by hand without an API key.
4. **Be kind in wellbeing-adjacent features.** The Reset flow and anything touching difficult emotions should be supportive, non-clinical, and should never reinforce harm. When in doubt, gently point people toward real human support.

## Dev setup

There isn't one. Open `index.html` in a browser and edit. To sanity-check logic without clicking through the UI, you can load the inline `<script>` in Node with a small DOM/`localStorage`/`fetch` stub (see the project history for examples).

## Submitting

- Open an issue first for anything substantial, so we can align before you build.
- Keep PRs focused and described in plain language.
- Test in at least one Chromium and one non-Chromium browser if you touch the UI.

## Code of conduct

Be decent. This is a tool about honesty and self-compassion; bring the same energy to the project.
