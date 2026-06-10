# Nightwatch — iPad bedside clock

Flip/analog/LED clock with weather, BTC price, Czech name days and night red mode.
Built for an iPad Mini 4 in landscape.

## Publish on GitHub Pages (one-time, ~5 min)

1. Go to https://github.com/new — repository name: `nightwatch`, Public, Create.
2. On the repo page: **Add file → Upload files** — drag the three HTML files
   from this folder (`index.html`, `nightwatch-v1.1.html`, `nightwatch-v1.0.html`), Commit.
3. **Settings → Pages** — under *Build and deployment*: Source = `Deploy from a branch`,
   Branch = `main`, folder = `/ (root)`, Save.
4. Wait ~1 minute. Your clock lives at:
   `https://YOUR-USERNAME.github.io/nightwatch/`

## On the iPad

1. Open that URL in Safari → allow location when asked.
2. Share → **Add to Home Screen** → launch from the icon: fullscreen, no toolbars.
3. Settings → Display & Brightness → Auto-Lock → **Never**.

## Updating later

Edit/replace `index.html` in the repo (Add file → Upload files again — it overwrites).
The iPad picks the new version up on next launch/reload.
