# Pip website

Static site for Pip – Habit Tracker, hosted free on GitHub Pages. No build step, no JavaScript, no tracking.

| Page | File | Used for |
|---|---|---|
| Home (landing) | `index.html` | **Marketing URL** in App Store Connect (optional), links on social media |
| Support | `support/index.html` | **Support URL** in App Store Connect, `Links.support` (Settings → Help & support) |
| Privacy Policy | `privacy/index.html` | **Privacy Policy URL** in App Store Connect, `Links.privacy` |

Shared styles: `style.css` (light + dark, same tokens as the app). Images: `images/` (screenshots rendered from the
design boards; replace with real device screenshots before launch).

## Before launch
- Swap the "Coming soon to the App Store" pills (2 on the home page) for Apple's official
  "Download on the App Store" badge linking to the app — use Apple's badge artwork and follow its guidelines.
- Add `<meta name="apple-itunes-app" content="app-id=APP_ID">` to the home page for the Smart App Banner.
- Add an `og:image` (1200×630, absolute URL) for nicer link previews.
- Support email is mkunal065@gmail.com on the support and privacy pages, the footer, and `Links.feedback` — change
  them together.
- Keep the privacy policy in sync with the App Privacy label ("Data Not Collected") and `PrivacyInfo.xcprivacy`;
  update it (and its date) before shipping anything that changes data handling, e.g. Pip Pro (ADR 0005).

## Hosting on GitHub Pages
1. Create a public repo `pip-site` and push the contents of this folder (include the empty `.nojekyll` file).
2. Repo → Settings → Pages → Deploy from a branch → `main` / root.
3. URLs: `https://USERNAME.github.io/pip-site/` (home), `…/support/`, `…/privacy/`.

To publish changes: `cp -R ~/Documents/Pip/site/ ~/Documents/pip-site/ && cd ~/Documents/pip-site && git add . && git commit -m "Update site" && git push`
