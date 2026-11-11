# SpeedoTime

A car-style speedometer (half circle, 0–150 mph) that shows **trip time** as well as speed.
Enter a distance, then drag the red and blue needles to compare two speeds: the dial shows how long
the trip takes at each speed and how much time the faster one saves.

The idea illustrates the **time-saving bias**: people overestimate the time saved by speeding up
from an already high speed. Trip time is distance ÷ speed, so each extra 10 mph saves less than the one before.

## Features

- Half-circle speedo, 0–150 mph, red line from 120 mph
- Two draggable needles (mouse or touch), Speed A (red) and Speed B (blue); you grab whichever is closest
- Green arc on the dial shows the gap between the two speeds, with the time saved in the centre
- Orange ring around the dial shows trip time at every 10 mph for your distance
- Distance in miles or km
- Trip time and arrival time for each speed, plus time saved by the faster one
- Table of every 10 mph step with the time gained from each extra 10 mph
- Remembers your last inputs in the browser
- Installable on a phone (PWA): **Android** shows an *Install app* button; on **iPhone** tap
  Share → *Add to Home Screen*. Works offline once opened.

## Run locally

Open `public/index.html` in a browser, or:

```sh
npx wrangler dev
```

## Deploy to Cloudflare

It's a single static file, so either of these works:

**Workers (static assets)**: uses `wrangler.jsonc`

```sh
npx wrangler login
npx wrangler deploy
```

**Pages**: in the Cloudflare dashboard, go to Workers & Pages → Create → Pages → connect this
repo. Leave the build command empty and set the build output directory to `public`.
