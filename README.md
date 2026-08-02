# Barbell.calc — legal

Public hosting for the [Barbell.calc](https://github.com/jthalstead/Barbell.calc)
privacy policy. This repo is public **only** so GitHub Pages can serve the
policy at a URL Apple can reach — the app's source stays private.

| | |
|---|---|
| Published at | https://jthalstead.github.io/barbell-calc-legal/ |
| Served from | `main` branch, repo root |
| Page | `index.html` |

That URL is baked into the app (`AppConfig.privacyPolicyUrl`) and is what
must be entered in App Store Connect's "Privacy Policy URL" field. Changing
it means shipping an app update, so avoid renaming this repo.

## Updating the policy

The source of truth is `legal/privacy-policy.md` in the app repo. To publish
a change:

1. Edit `legal/privacy-policy.md` and `legal/privacy-policy.html` in the app
   repo, keeping the two in sync and bumping the "Last updated" date.
2. Copy the HTML over `index.html` here:
   ```
   cp ../Barbell.calc/legal/privacy-policy.html index.html
   ```
3. Commit and push. Pages redeploys within a minute or so.

`index.html` is self-contained — inline CSS, no external requests — so it
needs no build step and works offline.
