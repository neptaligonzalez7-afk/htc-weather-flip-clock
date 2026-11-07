## HTC Weather Flip Clock - v1.2.12 (Nov 2026)

**New: animated weather icon.** Each time you unlock, the weather icon grows in, as it does on the HTC One X.

### New

- **Animated weather icon.** After you unlock, the icon fades and grows into place over about a second, then holds still until the next unlock. The animations are HTC's own: the small icon scenes from the One X's `WeatherVideo.apk` (Sense 4), rendered at 60 frames per second for every weather condition the clock shows, day and night.
- **On/off setting.** Open the widget's settings and tap **Animated weather icon** at the bottom (under **Clock style**). It's on by default; turned off, the icon stays still as before.

### Notes

- Plays only after unlocking. Weather updates and settings changes don't replay it, and nothing keeps running once it has played, so there's no battery cost while it's still.
- The animation's resting frame is the same Sense 4 artwork as before, so the icon looks the same when it's still.
- Needs Android 9 or later. On older versions the icon stays still.
- Some phones (Samsung especially) pause widgets in the background, so the icon may occasionally stay still after an unlock. Setting the app to **Unrestricted** under **Settings → Battery** helps.
- The APK is larger (about 31 MB) because of the animation frames.

### Upgrading

Install over v1.2.11 or older; no need to uninstall, and your widget stays on the home screen with your city and settings.

### Package info

- **versionCode:** `663091331`
- **versionName:** `10.10.1059527-android36-v1.2.12`
