# Nightwatch — iPad bedside clock

A single-file HTML dashboard built for an old iPad Mini 4 in landscape.
No frameworks, no build step, no accounts — just open it in Safari.

<img width="2076" height="960" alt="NightStand-1-1-Day" src="https://github.com/user-attachments/assets/282a69e0-c911-4e43-9147-e4937a26e164" />

## Features

**Layout (v1.1)** — top info bar with local weather (icon, temperature, condition,
feels-like, humidity, wind, sunrise/sunset) and Bitcoin (USD price, 24h change,
sparkline graph, green = up / red = down); a dominant clock below; bottom bar with
date, Czech name day (svátek) and tomorrow's forecast.

**Clock styles** — choose in ⚙︎ settings:

| Style | Look |
|---|---|
| Digital — flip cards | 70's flip clock (default, like the cover photo) |
| Digital — LED 7-segment | classic LED alarm clock with blinking colon |
| Analog — 70's square | rounded-square face, hour dashes, no numbers |
| Analog — minimal round | Braun-style circle, dashes only |
| Analog — Swiss station | minute ticks + red second hand with disc |
<div align="center">
<img width="75%" alt="4watchfaces" src="https://github.com/user-attachments/assets/3e1c64f8-5d84-41a8-9eb4-1debe66ad547" />
</div>
**Night red mode** — switches the whole page to dim red automatically (default
22:00–07:00, configurable), or force on/off; ☾ button toggles manually.
Weather icons are tinted red, the BTC graph dims.

**Customization** — 9 fonts (Helvetica, Comic Sans/Chalkboard, Arial Rounded,
Avenir Next, Futura, American Typewriter, Menlo, Georgia, Marker Felt) with live
preview; digit stretch up to +100%; clock-size and info-bar-size sliders (live);
°C/°F; location by geolocation or typed city name (geocoded automatically).

<div align="center">
<img width="50%" alt="NightStand-1-1-Setting" src="https://github.com/user-attachments/assets/ffb037b3-1cc6-4aa4-ab64-a5ef756807a7" />
</div>

**Keep-awake** — uses the Wake Lock API on newer devices, an invisible looping
micro-video fallback on older iOS. Still set Auto-Lock → Never for certainty.

**Data sources** (all free, no API keys):
[Open-Meteo](https://open-meteo.com) weather + geocoding,
[CoinGecko](https://coingecko.com) Bitcoin,
[svatkyapi.cz](https://svatkyapi.cz) Czech name days.
Weather refreshes every 15 min, BTC every 5 min. Everything degrades gracefully
offline — the clock itself never needs internet.

## Files

- `index.html` — promotional landing page (light/dark theme switcher)
- `clock.html` — **the clock itself, latest version** (linked from the landing page)
- `nightwatch-v1.1.html` — same as clock.html, versioned name
- `nightwatch-v1.0.html` — original layout (clock left 2/3, panels right)
- `NightStand-1-1-*.png` — screenshots used on the landing page

## Live

Nightwatch is available at:

**https://paolocortezcz.github.io/Old-iPad-HTML-NightStand-Clock/**

HTTPS hosting is what makes Safari allow geolocation — local files and plain
`http://` LAN servers can't auto-detect your location.

## iPad setup

1. Open the URL in Safari → allow location.
2. Share → **Add to Home Screen** → launch from the icon (fullscreen, no toolbars).
3. Settings → Display & Brightness → Auto-Lock → **Never**.
4. Tweak everything via the ⚙︎ button (bottom-left corner of the page).

## Updating

Replace `index.html` in the repo (Add file → Upload files overwrites).
The iPad picks up the new version on next reload.
