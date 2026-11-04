## HTC Weather Flip Clock — v1.2.8 (Nov 2026)

**Fixes blank weather on a fresh install.** On a brand-new install, v1.2.7 never set up a location and never asked for location permission, so the weather bar showed "Location unavailable" / "Weather unavailable" until location was granted by hand. This happened in every launcher. v1.2.8 sets it up the way HTC did.

### Fixed

- **Current location by default.** When no city is saved, the widget now follows your current location automatically. This matches HTC's own "By default, this widget's time and weather always update for your current location" prompt.
- **Asks for location permission.** Opening the widget's settings now asks for location access if it's missing. As soon as you allow it, the weather is fetched right away.
- **"Allow all the time" asked once.** After location is allowed, Android's "Allow all the time" screen opens once, so the town keeps updating while the widget is in the background (for example when you travel). You can choose "Only while using the app" instead; the widget then updates its location when you open its settings.

Nothing else changes: same Sense 3 flip animation, same Open-Meteo weather.

### Upgrading

Install over v1.2.7 or older; no need to uninstall, and your widget stays on the home screen. If your widget already shows your town, nothing changes for you.

### Package info

- **versionCode:** `663091327`
- **versionName:** `10.10.1059527-android36-v1.2.8`
