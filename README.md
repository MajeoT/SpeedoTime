# SpeedoTime

A car-style speedometer (half circle, 0–150 mph) that shows **trip time** as well as speed.
Enter a distance and a baseline speed, then drag the needle: the dial shows how long the trip
takes at each speed and how much time you save (or lose) compared with the baseline.

The idea illustrates the **time-saving bias**: people overestimate the time saved by speeding up
from an already high speed. Trip time is distance ÷ speed, so each extra 10 mph saves less than the one before.

## Features

- Half-circle speedo, 0–150 mph, red line from 120 mph, draggable needle (mouse or touch)
- Orange ring around the dial shows trip time at every 10 mph for your distance
- Distance in miles or km; baseline speed marked in blue on the dial
- Trip time, arrival time, time saved/lost vs baseline
- Table of every 10 mph step with the time gained from each extra 10 mph
- Remembers your last inputs in the browser

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
