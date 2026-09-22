# Bin Card — Pharmacy Stock Register (PWA package)

This folder is a ready-to-host Progressive Web App. Once it's hosted at a real
URL, it can be installed as an app icon on Android/iOS, and turned into a
real, sideloadable `.apk` file for Android.

## What's inside
- `index.html` — the app itself
- `manifest.json` — app name, icons, colors (lets phones "install" it)
- `service-worker.js` — lets it work offline once loaded once
- `icons/` — app icons

## Step 1 — Host it somewhere (free, ~5 minutes)
Any static host works. Two easy free options:

**GitHub Pages**
1. Create a free GitHub account and a new repository.
2. Upload all files in this folder (keeping the `icons/` folder structure).
3. Go to Settings → Pages → set source to the main branch → Save.
4. You'll get a URL like `https://yourname.github.io/reponame/`.

**Netlify Drop**
1. Go to https://app.netlify.com/drop
2. Drag this whole folder onto the page.
3. It gives you a live URL immediately, no account required for a quick test
   (create a free account to keep it permanent).

## Step 2 — Install directly (no APK needed)
Once hosted, open the URL on a phone:
- **Android (Chrome)**: menu → "Install app" / "Add to Home screen"
- **iOS (Safari)**: Share → "Add to Home Screen"

This already gives a full-screen home-screen app with no browser bar or app
store needed — for most teams this is enough on its own.

## Step 3 — Build a real .apk (optional, for sideloading without internet)
1. Go to https://www.pwabuilder.com
2. Enter your hosted URL (from Step 1) and click "Start".
3. PWABuilder scans the manifest and service worker (already set up here).
4. Choose the **Android** package option → download the generated `.apk`.
5. Send that `.apk` file to any Android phone and open it — the phone will
   ask to allow "install from unknown sources" the first time, then it
   installs like any app, no Play Store required.

Note: iOS does not support sideloaded `.apk`-style installs outside the
App Store — Step 2 (Add to Home Screen) is the closest equivalent on iPhone.

## Note on shared/synced data
This package always runs in **local, on-device storage mode** (each phone
keeps its own data). The live-synced version that shares data across your
team only works through the Claude-hosted link, since that sync depends on
Claude's own backend.
