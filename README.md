# Metronome PWA (MVP)

A simple, precise metronome Progressive Web App built with React + Vite. It supports incremental tempo changes over a set number of measures with a distinctive 4-count cue between tempo changes. Works offline and installable as a PWA.

## Features
- Start/End BPM, step amount, measures per step
- Modes: Ascend, Descend, Both (up then down)
- 4-beat cue between tempo changes (higher pitch)
- Loop toggle
- Tight timing with Web Audio API scheduling (lookahead + schedule-ahead)
- Responsive UI, installable PWA, offline support
- Ad banner placeholder

## Getting Started

```bash
npm install
npm run dev
```

Open the printed local URL (default http://localhost:5173).

### Build
```bash
npm run build
npm run preview
```

## Deploy
You can host the `dist/` folder on any static host (Netlify, Vercel, S3 + CloudFront, your own server).

## Code Structure
- `src/AudioEngine.js` – Web Audio scheduling engine
- `src/App.jsx` – UI and controls
- `public/sw.js` – Service worker for offline caching
- `public/manifest.webmanifest` – PWA manifest
- `public/icons/*` – App icons

## Notes
- Beats per measure are fixed to 4 for MVP. We can expose this later.
- AdMob on the open web is typically via AdSense; native AdMob SDK applies to wrapped iOS/Android apps. The UI includes a placeholder container for future integration.
