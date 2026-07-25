# dices-legal

Public legal pages (Impressum / Datenschutzerklärung / Legal Notice / Privacy Policy) for the
[Dices](https://github.com/benedikt-schreiner/dices) app, hosted via GitHub Pages.

Apple App Store Connect and Google Play Console both require a publicly reachable Privacy
Policy URL — this repo exists to serve that URL (in-app legal text alone is not sufficient).

## Structure

Static HTML, no build step. One folder per language, each containing an `index.html` with
both the Impressum and the Datenschutzerklärung/Privacy Policy on a single page:

```
/               language picker (auto-redirects based on browser language)
/de/            Deutsch
/en/            English
/es/            Español
/fr/            Français
/it/            Italiano
/ja/            日本語
/pl/            Polski
/pt-br/         Português (BR)
/assets/style.css
```

## Keeping content in sync

The legal text here is copied from `src/i18n/locales/*.ts` in the
[dices](https://github.com/benedikt-schreiner/dices) app repo (`privacy_sections` and the
`impressum_*` keys). There is no automated sync — when the in-app legal text changes, update
the matching page here by hand and commit.

## Deployment

Served via GitHub Pages from the `main` branch root. No build step required.
