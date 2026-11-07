# HTC Sense Weather Flip Clock (Android)

Home-screen **4×2 flip clock** widget in the classic **HTC Sense** style, rebuilt for **modern Android**. Weather uses **Open-Meteo** (no AccuWeather or HTC weather account required).

**All-in-one:** the widget fetches its own weather. You don't need to install a separate weather app (no HTC Weather, Breezy Weather, or AccuWeather app) or create an account.

**As close to the original as possible:** this is HTC's own Weather Clock APK (`10.10.1059527`, package `com.htc.widget.weatherclock`) with HTC's layouts, artwork, settings screens and Sense 3 flip. Only the parts that no longer work on modern Android were replaced: the dead weather backend, background timing, and Android 16 compatibility.

**Four clock styles (v1.2.11+):** keep HTC's original look, or switch to the HTC One X (Sense 4) digits, cards and weather bar, each with the Sense 3 or the Sense 4 flip.

**Animated weather icon (v1.2.12+):** each time you unlock, the weather icon grows in as it does on the HTC One X, using HTC's own Sense 4 icon animations.

**Weather animation on unlock (v1.2.13+, optional):** HTC's full-screen Sense 4 weather (sun, clouds, rain, snow, storms) plays over the home screen right after you unlock, centred on the screen as on the One X. Off by default; see [Weather animation on unlock](#weather-animation-on-unlock-v1213).

**Companion weather app (optional):** install **[HTC Sense 4 Weather](https://github.com/neptaligonzalez7-afk/htc-sense4-weather-app)** and tapping the weather on the clock (v1.2.11+) opens it, with the One X's animated weather scenes and forecast. Without it, the tap opens weather.com.

> **Not affiliated with HTC.** Community port for phones where the original widget no longer works correctly.

## Screenshots

| Home screen | Flip animation |
|-------------|----------------|
| ![Widget on home screen](./screenshots/home-widget.jpg) | [Watch flip demo (MP4)](./screenshots/flip-animation.mp4) |

**Weather icon animation (v1.2.12+)**, played once after each unlock:

![Weather icons growing in](./screenshots/weather-icon-animation.gif)

Location name is blurred for privacy in these media files.

## What was broken (original APK / old port)

On **recent Android versions** (including current **Android 15 / 16**–class builds on devices like Samsung S24/S25/S26 Ultra), the classic **HTC Weather Clock** often:

- **Weather blank or stuck** — legacy **AccuWeather / HTC weather** backends are gone or blocked; the strip never updates.
- **Time stops updating** — digits freeze on old minutes or hours until you force-remove the widget.
- **No flip animation** — digits swap instantly or not at all; the Sense flip effect is lost.
- **Widget crashes or fails to load** — older builds target outdated APIs and break under stricter background and network rules.

Installing the old Play/APKMirror package alone does **not** fix this on a current phone.

## What this APK fixes (what works now)

This release line (**`HTC-WeatherClock-10.10.1059527-android36-*.apk`**) is built for **today’s Android**:

| Area | Status |
|------|--------|
| **Latest Android compatibility** | **minSdk 24**, **targetSdk 36** — intended for current flagship / stock Android versions, not just old ROMs. |
| **Weather** | **Works** via **Open-Meteo** (current conditions + forecast data wired into the widget). |
| **Flip clock** | **HTC Sense 3 flip** (v1.2.7+) — the flap folds down at the hinge and the new half drops into place (0.67 s). On unlock the hour flips once and the minute twice, as on Sense. **Sense 4 flip** (v1.2.11+) — the One X's steady fall with a sweeping shadow, fading digits and a sinking card. |
| **Clock style** | **Four styles** (v1.2.11+): HTC or One X (Sense 4) design, each with the Sense 3 or Sense 4 flip. See [Clock styles](#clock-styles). |
| **Weather icon** | **Animated** (v1.2.12+, Android 9+): after each unlock the icon grows in over about a second, from the One X's own icon animations (`WeatherVideo.apk`), then holds still. Can be turned off. |
| **Unlock weather** | **Optional** (v1.2.13+, Android 9+): HTC's full-screen Sense 4 weather scene for the current conditions plays for about 6 seconds after you unlock to the home screen. Touches go through to the home screen; the first one fades it out. |
| **Time updates** | **Clock keeps time** — updates with system time / refresh paths; **does not stay stuck** like the broken legacy behavior. |
| **Location / sync** | Bridge layer replaces dead HTC sync with a local weather provider and modern refresh behavior. |
| **Manual city** | Choose a city in widget settings (list or search/add); selection is persisted for the widget. |
| **Temperature unit** | Switch **°F** and **°C** in settings; the widget follows your choice. |

Exact layout may vary slightly by launcher and screen size; core clock, flip, and weather strip are what this port restores.

## Widget settings (manual city & °F / °C)

1. Add the **4×2 Weather Clock** widget, then open its **settings** (tap the widget or use the widget’s configure action).
2. **City**
   - Tap **Current location** to use GPS weather and local time for where you are.
   - Or tap any city in the list (e.g. cities you added earlier).
   - Use **+** / search to find and add a city (e.g. Los Angeles, San Diego), then tap it to select.
3. **Temperature**
   - Use the **°F / °C** control in settings. The widget should refresh with the unit you picked.
4. **Clock style (v1.2.11+)**
   - Tap **Clock style** at the bottom of settings and pick one of the four styles below. The widget switches right away.
5. **Animated weather icon (v1.2.12+)**
   - On by default. Tap **Animated weather icon** at the bottom of settings to turn it off; the icon then stays still.
6. **Weather animation on unlock (v1.2.13+)**
   - Off by default. Tap **Weather animation on unlock** at the bottom of settings to turn it on, then allow the two permissions it asks for (see [below](#weather-animation-on-unlock-v1213)). Once both are allowed it plays once as a preview.
7. **Language (v1.1.4+)**
   - City names, forecast day/date labels, and the widget date line follow **system language** (Open-Meteo geocoding + locale date formats). After changing language in Android settings, weather refreshes automatically.

If a city does not stick after you leave settings, install the **latest release** from GitHub. Uninstall older sideloads of the same app if install or behavior is inconsistent.

## Clock styles

Pick a style under **Clock style** in the widget's settings. The design sets the digits, cards and weather bar; the flip sets how each minute turns over.

| Style | What it looks like |
|-------|--------------------|
| **HTC design, Sense 3 flip** (default) | The original HTC flip clock. Slim digits with a smooth gradient on white cards with a soft grey lower half. Each minute the top card eases into its fall and settles gently as it lands. |
| **HTC design, Sense 4 flip** | The original HTC cards and digits with the One X's livelier flip: the top card drops at a steady pace while a shadow sweeps across, the new digits fade in behind it and the old half sinks away. |
| **One X design, Sense 3 flip** | The HTC One X (Sense 4) look: bolder, wider digits with an embossed highlight on bright white cards split by a thin hinge, and the One X's pinstriped black weather bar. Flips with the original HTC motion: an eased fall and a gentle landing. |
| **One X design, Sense 4 flip** | The One X as it shipped: its digits, cards and weather bar with its own flip, a steady drop with a sweeping shadow, fading digits and a sinking card. The most faithful Sense 4 look. |

The Sense 4 design and flip come from the One X's own clock widget (`HtcClockWidget.apk`, Sense 4).

## Weather animation on unlock (v1.2.13+)

On the HTC One X, unlocking to the home screen played the current weather full screen: sun rays, drifting clouds, rain on the glass, snow, lightning. Turn it on under **Weather animation on unlock** in the widget's settings. It plays for about 6 seconds, centred on the screen, then fades; touch the home screen and it fades right away (your tap still goes through). It doesn't play when you unlock straight into an app.

A widget can only draw inside its own box, so the scene needs two permissions. The settings screen takes you to each one:

| Permission | Why |
|------------|-----|
| **Display over other apps** | To draw the scene over the home screen. |
| **Usage access** (Samsung: **Usage data access**) | To know you just unlocked and that the home screen, not an app, is in front. Nothing is collected or sent anywhere. |

If a switch is greyed out as a **restricted setting** (Android 13+ for sideloaded apps): **Settings → Apps → Weather Clock → ⋮ → Allow restricted settings**, then try again.

**Samsung:** set **Settings → Apps → Weather Clock → Battery** to **Unrestricted**. On **Optimized**, One UI can tell the widget about an unlock several seconds late; the scene is then skipped rather than played late.

Android 12+ only lets touches pass through another app's window at up to 80% opacity, so the scene shows slightly fainter than on the One X. No sound.

## Download

Get the latest APK from **[Releases](https://github.com/neptaligonzalez7-afk/htc-weather-flip-clock/releases)**.

| Release | File | versionCode | Notes |
|---------|------|-------------|--------|
| **Latest (Nov 2026)** — tag **`v1.2.13`** | `HTC-WeatherClock-10.10.1059527-android36-v1.2.13.apk` | `663091332` | **Weather animation on unlock**: HTC's full-screen Sense 4 weather after unlocking (optional) |
| v1.2.12 | `HTC-WeatherClock-10.10.1059527-android36-v1.2.12.apk` | `663091331` | **Animated weather icon**: grows in like the One X after each unlock |
| v1.2.11 | `HTC-WeatherClock-10.10.1059527-android36-v1.2.11.apk` | `663091330` | **Clock style**: HTC or One X (Sense 4) design with the Sense 3 or Sense 4 flip; faster city search; weather tap opens Sense 4 Weather if installed |
| v1.2.8 | `HTC-WeatherClock-10.10.1059527-android36-v1.2.8.apk` | `663091327` | **Fixes blank weather on fresh installs**: follows current location by default and asks for location permission |
| v1.2.7 | `HTC-WeatherClock-10.10.1059527-android36-v1.2.7.apk` | `663091326` | **HTC Sense 3 flip animation** (hinge fold, unlock flip); weather provider readable by Weather Sky wallpaper |
| v1.2.5 | `HTC-WeatherClock-10.10.1059527-android36-v1.2.5.apk` | `663091324` | Open-Meteo auto-detect/GPS follow-up (v1.2.4 + stronger first fix) |
| v1.2.4 | `HTC-WeatherClock-10.10.1059527-android36-v1.2.4.apk` | `663091323` | Auto-detect location fix (Android 16/17); includes v1.2.3 weather cache + clock sync |
| v1.2.3 | `HTC-WeatherClock-10.10.1059527-android36-v1.2.3.apk` | `663091322` | Weather rate-limit + cache; clock catch-up; includes language + battery fixes below |
| Previous — tag **`v1.1.4`** | `…-v1.1.4.apk` | `663091313` | **System language** for city + forecast labels |
| Previous — tag **`v1.1.3`** | `…-v1.1.3.apk` | `663091312` | First **battery** background reductions |
| Previous — tag **`v1.1.2`** | `…-v1.1.2.apk` | `663091311` | °F/°C high/low + forecast |
| First release — tag **`v10.10.1059527-android36`** | `…-baseline.apk` | `663091309` | Flip clock + Open-Meteo baseline |

**Naming:** base `HTC-WeatherClock-10.10.1059527-android36` + **`-v<TAG>.apk`** or **`-baseline.apk`**. Always pick **Releases → Latest**.

**Latest versionCode:** `663091332` · **targetSdk 36**

## Requirements

- Android **7.0+** (API 24) through **current Android** (this build targets **API 36**)
- Internet for weather sync
- Location permission optional (for automatic local weather)

## Install

1. Download the latest release APK from **Releases**.
2. On the phone: allow **Install unknown apps** for your browser or Files app.
3. Open the APK and install.
4. If install fails with **“App not installed”** or **signature conflict**:
   - Uninstall any existing **`com.htc.widget.weatherclock`** app (Play, OEM, or older APK), then retry.
   - *(This removes the widget from home screens; add it again after install.)*

Developers: `adb install -r HTC-WeatherClock-10.10.1059527-android36-v1.2.13.apk`

## Add the widget

1. Long-press home screen → **Widgets**.
2. Find **Weather Clock** (HTC) → **4×2**.
3. Place on home screen. The widget's settings open: **allow location** when asked (since v1.2.8), then tap **OK** to follow your current location, or **Edit city** to pick a fixed city. **°F or °C** is at the bottom of the same screen.

## Battery / background usage (v1.2.0+)

This port keeps the clock on time with **one alarm per minute while unlocked and interactive** (plus system `TIME_TICK` when the app is in memory). It does **not** wake the phone every 60 seconds while idle on the lock screen or in doze.

- **Screen off / locked** — the in-app timer loop stops. Since v1.2.7 the minute alarm stays armed but is **non-wakeup**: it never wakes the phone, it just fires as soon as the screen comes back on, so the clock is on time right away.
- **Fixed city** — no live GPS seeding or motion location watches; much lower overnight drain than early Open-Meteo builds.
- **Current location / travel** — network and fused fixes only; passive motion hints (no continuous GPS fixes for routine widget reads).
- **Weather** — sync is throttled (about **20–30 minutes** between automatic refreshes); Open-Meteo calls are spaced to avoid rate limits.
- **No widget on home screen** — pending alarms and jobs are cancelled.

On Samsung **Settings → Battery**, if you previously set this app to **Unrestricted** only for flip timing, you can try **Optimized** again on **v1.2.0+** and confirm the clock still flips on the home screen when unlocked.

## Flip animation not visible?

There is **no setting in the widget to turn flip animation on or off** (**Clock style** only changes which flip plays). The clock can show the **correct time** while digits **change instantly** — that usually means the flip path did not run, or your **launcher only applied the last widget frame** of a short animation.

Since v1.2.7 the flip is HTC's Sense 3 flip, played by the home screen itself: the app sends one update per flip and the launcher runs the fold-and-drop animation (ported from [BuksaPC/htc-honor-weather-flip-clock](https://github.com/BuksaPC/htc-honor-weather-flip-clock)). It runs when the **minute rolls over** while you are on the home screen, and once more right after you **unlock** (hour once, minute twice).

### Try this

1. Install the **[latest release](https://github.com/neptaligonzalez7-afk/htc-weather-flip-clock/releases/latest)** (`…-v1.2.7.apk` or newer). Old APKMirror / pre-bridge builds often never flip on modern Android.
2. Use **Weather Clock → 4×2** only. Smaller or alternate clock widgets may not use the same flip layout.
3. Remove the widget from the home screen and **add it again** after installing.
4. At **:58**, stay on the **home screen**, **unlocked**, and watch the **minute** digit change at **:00**.
5. **Exact alarms (Pixel / stock Android):** **Settings → Apps → ⋮ → Special app access → Alarms & reminders** → allow this app. It does **not** appear as a line on the app’s main **App info** page (Notifications / Permissions / Battery only).
6. **Samsung / One UI:** **Settings → Battery → Background usage limits** — set this app to **Unrestricted** if the clock lags while unlocked.
7. Optional: turn **off** **Remove animations** (Accessibility) and set **Animator duration scale** to **1x** (Developer options). These rarely fix the issue alone but are worth ruling out.

### Still no flip?

Some launchers (including One UI on S24/S25/S26-class devices) **throttle** widget updates. The app may animate internally while the home screen only shows the final digit — it can look like an instant change. If that matches your phone, say so in an issue; device and launcher details help.

## Signing

APKs are **debug-signed** for sideloading. They are not Play Store builds. Do not install over a differently signed build of the same package without uninstalling first.

## License

See [LICENSE](./LICENSE). HTC Sense names and assets are trademarks of their respective owners.

## Reporting issues

Open a **GitHub Issue** with device model, **Android version**, **One UI / launcher** name, **APK filename** (from Releases), and a **short screen recording** across a minute change (home screen, unlocked). For flip problems, note whether the **time is correct** but only the **animation** is missing.

## Support (optional)

If this widget is useful on your phone, you can [buy me a coffee](https://buymeacoffee.com/neta4457). Thanks for trying it.
