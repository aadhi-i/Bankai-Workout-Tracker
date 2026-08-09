# BANKAI — Workout Tracker

A minimal, black-and-red calendar workout tracker. Plan exercises for any day, log sets, reps, and weight, and check off your workouts as you go. Installs as a Progressive Web App (PWA), so it runs full-screen like a native app with offline support.

**Live app:** https://aadhi-i.github.io/Bankai-Workout-Tracker/

## Features

- 📅 **Calendar view** — tap any date to see that day's planned workout
- ➕ **Add exercises** — name, sets, reps, weight (kg/lb)
- ✅ **Check off sets** as you complete them
- 📋 **Upcoming tab** — see everything planned from today onward, grouped by day
- 💾 **Works offline** and saves data locally on your device
- 📱 **Installable** — add it to your home screen on Android or iPhone

## Install it on your phone

### Android (Chrome)

1. Open the [live app link](https://aadhi-i.github.io/Bankai-Workout-Tracker/) in **Chrome**
2. Tap the **⋮** menu in the top right
3. Tap **Install app** (or tap the install icon in the address bar if you see one)
4. Confirm — BANKAI now appears on your home screen and opens full-screen, with no browser bar

### iPhone / iPad (Safari)

> iOS only supports installing from **Safari**, not Chrome.

1. Open the [live app link](https://aadhi-i.github.io/Bankai-Workout-Tracker/) in **Safari**
2. Tap the **Share** icon (square with an arrow pointing up) at the bottom of the screen
3. Scroll down and tap **Add to Home Screen**
4. Tap **Add** in the top right — the icon appears on your home screen

### Desktop (Chrome / Edge)

1. Open the live app link
2. Click the install icon (a small monitor with a down arrow) at the right end of the address bar
3. Click **Install**

Once installed, your workout data is stored locally on that device — it won't sync across devices, but it works fully offline after the first load.

## Running it locally

This is a static site with no build step. Clone the repo and serve the folder with any static file server, for example:

```bash
npx serve .
```

Then open the printed local URL in your browser. Note: installability (the "Install app" prompt) and offline support require the site to be served over **HTTPS** or from **localhost** — opening `index.html` directly as a file won't trigger them.

## Tech

Vanilla HTML, CSS, and JavaScript — no frameworks or build tools. Data is stored in the browser's `localStorage`. Offline caching is handled by a service worker (`sw.js`).

## Project structure

```
.
├── index.html      # the app
├── manifest.json   # PWA manifest (name, icons, display mode)
├── sw.js           # service worker for offline caching
├── icon-192.png
├── icon-512.png
├── icon-192-maskable.png
└── icon-512-maskable.png
```