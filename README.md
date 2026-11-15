# Pip website

Static site for Pip – Habit Tracker, hosted free on GitHub Pages. No build step, no JavaScript, no tracking.

| Page | File | Used for |
|---|---|---|
| Home (landing) | `index.html` | **Marketing URL** in App Store Connect (optional), links on social media |
| Support | `support/index.html` | **Support URL** in App Store Connect, `Links.support` (Settings → Help & support) |
| Privacy Policy | `privacy/index.html` | **Privacy Policy URL** in App Store Connect, `Links.privacy` |

Shared styles: `style.css` (light + dark, same tokens as the app). Images: `images/` (screenshots rendered from the
design boards; replace with real device screenshots before launch).

## Live on the App Store (Nov 2026)
- App Store: https://apps.apple.com/app/id6832249206 (App Store ID 6832249206).
- Home page uses Apple's official "Download on the App Store" badge, loaded from Apple's badge service
  (black in light mode, white in dark mode). Don't recolor or redraw it.
- Every page has the Smart App Banner (`apple-itunes-app`) and a "Get Pip" button in the top bar.
- Link previews: `images/og.png` (1200×630) via `og:image`.
- Support email is mkunal065@gmail.com on the support and privacy pages, the footer, and `Links.feedback` in the app.
- Keep the privacy policy in sync with the App Privacy label ("Data Not Collected"); update it (and its date)
  before shipping anything that changes data handling, e.g. Pip Pro (ADR 0005).
- To do: replace `images/*.webp` (design-board renders) with real screenshots from the live app.

## Hosting on GitHub Pages
1. This folder (`~/Documents/pip-site`) is the repo `kunalvmore/pip-habittracker`; it is the only copy of the site.
2. Repo → Settings → Pages → Deploy from a branch → `main` / root.
3. URLs: `https://kunalvmore.github.io/pip-habittracker/` (home), `…/support/`, `…/privacy/`.

To publish changes: `cd ~/Documents/pip-site && git add . && git commit -m "Update site" && git push`
