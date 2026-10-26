# SmartBuzz website

Support page and privacy policy for SmartBuzz, served by GitHub Pages.

| Page | Planned URL | Used for |
|---|---|---|
| Support | https://snuffydan.github.io/smartbuzz-site/ | App Store Connect "Support URL", in-app links |
| Privacy | https://snuffydan.github.io/smartbuzz-site/privacy/ | App Store Connect "Privacy Policy URL", Settings › Privacy Policy |
| Terms | Apple's standard EULA | Settings › Terms of Use (no custom terms needed) |

## Publish (one-time)

1. On GitHub, create a **public** repository named `smartbuzz-site` under `snuffydan` (leave it empty).
2. Push this folder:
   ```bash
   git remote add origin https://github.com/snuffydan/smartbuzz-site.git
   git push -u origin main
   ```
3. In the repository, go to **Settings › Pages**, set **Source** to *Deploy from a branch*, branch **main**, folder **/ (root)**, then **Save**.
4. After a minute or two, check both URLs above load. Then paste them into App Store Connect.

If you choose a different repository name, the URLs change to `https://snuffydan.github.io/<name>/`, and `AppConfig.swift` in the app needs the same change.

## Updating

Edit the HTML, commit and push; Pages republishes automatically. When a release changes how data is handled (for example sign-in and sync in 1.1), update `privacy/index.html` and its "Last updated" date **before** that release goes live.

## Custom domain (optional, later)

Buy a domain (e.g. `smartbuzz.app`), add it under **Settings › Pages › Custom domain**, and follow GitHub's DNS instructions. Update the URLs in App Store Connect and `AppConfig.swift`.
