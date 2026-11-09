## HTC Weather Flip Clock - v1.2.15 (Nov 2026)

**Fixes for issues reported on Pixel / Android 17:** a faster settings screen, real town names outside the US, a clock style menu that updates, and a widget that can't be resized too small.

### Fixed

- **Settings opened to a blank city list for 12-15 seconds** ([#2](https://github.com/neptaligonzalez7-afk/htc-weather-flip-clock/issues/2)). The widget waited for a fresh GPS fix and up to six online place-name lookups before answering the settings screen. The list now shows right away from what's saved, and the location and town name are looked up in the background.
- **Cities shown as numbers such as "16" or "31"** ([#2](https://github.com/neptaligonzalez7-afk/htc-weather-flip-clock/issues/2)). Outside the US the widget could end up with Android's geocoder result, which gives the house number as the place name. House numbers are no longer accepted as town names. Saved ones show as "Current location" until the real town is found, then they're renamed automatically. The place-name lookup also skips the US-only services outside the US.
- **Clock style didn't update the menu** ([#3](https://github.com/neptaligonzalez7-afk/htc-weather-flip-clock/issues/3)). The settings screen runs separately from the widget and kept showing the old style; changing another setting there could also save the old style back. It now reloads the saved settings each time it opens or comes back.
- **Resizing broke the clock** ([#4](https://github.com/neptaligonzalez7-afk/htc-weather-flip-clock/issues/4)). HTC's clock is built from fixed-size pieces (344 dp wide). Launchers could squeeze it smaller, which cut off the weather bar or pushed the digits past their cards. The widget now needs at least **344 × 220 dp**: about 4×2 on Samsung, 5 columns wide on Pixel. Larger sizes look as before.
- **Slow start of the widget's background process.** On every start the widget's data provider set itself up again hundreds of times before an error stopped it. It now sets up once.

### Upgrading

Install over v1.2.14 or older; no need to uninstall, and your widget stays on the home screen with your city and settings. On a Pixel, if your widget is narrower than 5 columns, resize it wider (or remove it and add it again).

### Package info

- **versionCode:** `663091334`
- **versionName:** `10.10.1059527-android36-v1.2.15`
