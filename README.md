# One — Single Focus (Tauri / Rust → APK)

The app UI is `dist/index.html` (unchanged), wrapped in a Rust (Tauri 2) shell.

## Get the APK
1. Push this repo to GitHub (branch `main`).
2. Open the **Actions** tab → **Build Android APK** (runs on every push, or click *Run workflow*).
3. When it finishes, download the **One-final-release-apk** artifact from the run page and unzip it.

The APK is a fully optimized release build signed with v2/v3 signatures (`One-final.apk`), so it installs directly on your phone (enable "install unknown apps").

## Custom icon
Replace `app-icon.png` with your own square 1024×1024 PNG.

## Offline behaviour
The app is 100% offline and self-contained out of the box. All Tailwind styles are precompiled into `dist/style.css`, so the app boots instantly on first launch with zero network requests and no server dependencies.
