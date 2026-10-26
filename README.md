# One — Single Focus (Tauri / Rust → APK)

The app UI is `dist/index.html` (unchanged), wrapped in a Rust (Tauri 2) shell.

## Get the APK
1. Push this repo to GitHub (branch `main`).
2. Open the **Actions** tab → **Build Android APK** (runs on every push, or click *Run workflow*).
3. When it finishes, download the **One-apk** artifact from the run page and unzip it.

The APK is debug-signed, so it installs directly on a phone (enable "install unknown apps").

## Custom icon
Replace `app-icon.png` with your own square 1024×1024 PNG.

## Offline behaviour
On the very first launch the app downloads Tailwind and the Plus Jakarta Sans font once
(it shows a "Connect to internet" screen if there is no connection and retries automatically).
They are cached in IndexedDB, so every later launch works fully offline.
Clearing the app's storage makes it download them again.
