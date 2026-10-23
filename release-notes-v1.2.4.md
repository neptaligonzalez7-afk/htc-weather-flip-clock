## HTC Weather Flip Clock — v1.2.4 (Oct 2026)

**Auto-detect location fix** for Android 16/17-class devices where manual city worked but **current location** stayed unavailable.

### Auto-detect (current location)

- When auto-detect is enabled and the system has **no recent last-known fix**, the bridge now runs a **single fused/network location update** (same as travel mode — not continuous GPS).
- Runs during **background weather sync** and from a **short async task** when the widget reads location on the main thread (avoids blocking the UI).
- **Retry throttle:** at most one fresh fix attempt every **15 minutes** once coords exist; **no throttle** while coords are still missing (first setup / after permission grant).
- **Fixed city** widgets unchanged — no extra location work when auto-detect is off.

### Package info

- **Package:** `com.htc.widget.weatherclock`
- **versionCode:** `663091323`
- **versionName:** `10.10.1059527-android36-v1.2.4`

### Install

1. Download **`HTC-WeatherClock-10.10.1059527-android36-v1.2.4.apk`** below.
2. Install over any **debug-signed** build from this repo, or uninstall older sideloads if Android reports a signature conflict.
3. After upgrading: open widget settings once, confirm **auto detect** and **location permission**, then remove/re-add the widget if weather was stuck on “unavailable.”
