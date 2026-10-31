## HTC Weather Flip Clock — v1.2.7 (Oct 2026)

**HTC Sense 3 flip animation.** The clock now flips the way it did on Sense 3: the top flap folds down at the hinge and the new bottom half drops into place, with HTC's own motion and timing (0.67 s per flip).

Ported from [BuksaPC/htc-honor-weather-flip-clock](https://github.com/BuksaPC/htc-honor-weather-flip-clock) (`FlipAnimV3`). Weather is still Open-Meteo; nothing else about the widget changes.

### Flip animation

- **Sense 3 flip-down** on every minute change: hinge fold, then the new half drops in.
- **Unlock flip, as on Sense:** after unlocking, the hour card flips once and the minute card twice, quickly, landing on the current time together.
- **Played by the home screen itself.** The app sends one update per flip and the launcher runs the animation, so it stays smooth instead of depending on many rapid widget updates.
- **Full-size half-digit images** cut at the hinge, so the flap digits line up exactly with the card.
- **Minute alarm stays armed while the screen is off** (non-wakeup, so it doesn't wake the phone), so the first tick after you turn the screen on is on time.

### Also included (v1.2.6, not released separately)

- The weather provider is readable by the **HTC Weather Sky** live wallpaper, so the wallpaper can follow the widget's current conditions.

### Location tip

If the widget shows a nearby bigger city (for example the county seat) instead of your town, check **Settings → Apps → Weather Clock → Permissions → Location → Allow all the time**. Without location access the widget keeps using an old saved position.

### Package info

- **versionCode:** `663091326`
- **versionName:** `10.10.1059527-android36-v1.2.7`
