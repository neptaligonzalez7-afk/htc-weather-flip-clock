## HTC Weather Flip Clock - v1.2.13 (Nov 2026)

**New: weather animation on unlock.** HTC's full-screen Sense 4 weather plays over the home screen right after you unlock, as it did on the HTC One X.

### New

- **Weather animation on unlock (optional).** Sun rays, drifting clouds, rain on the glass, snow or lightning for the current conditions, played for about 6 seconds and centred on the screen, then faded out. These are HTC's own scenes from the One X. Touch the home screen and it fades right away; your tap still goes through. It doesn't play when you unlock straight into an app.
- **On/off setting.** Open the widget's settings and tap **Weather animation on unlock** at the bottom. It's off by default. Turning it on takes you to the two permissions it needs, then plays once as a preview.

### Permissions (only if you turn it on)

- **Display over other apps**, to draw the scene over the home screen (a widget can only draw inside its own box).
- **Usage access** (Samsung: **Usage data access**), to know you just unlocked and that the home screen is in front. Nothing is collected or sent anywhere.

If a switch is greyed out as a restricted setting (Android 13+ for sideloaded apps): **Settings → Apps → Weather Clock → ⋮ → Allow restricted settings**.

### Notes

- **Samsung:** set **Settings → Apps → Weather Clock → Battery** to **Unrestricted**. On Optimized, One UI can tell the widget about an unlock several seconds late; the scene is then skipped rather than played late.
- Android 12+ only lets touches pass through another app's window at up to 80% opacity, so the scene is slightly fainter than on the One X. No sound.
- Needs Android 9 or later.
- Fixed: the **Animated weather icon** switch didn't respond when you tapped the switch itself, and settings changes could be missed by the widget until it restarted.
- The APK is about 34 MB (the weather scenes add about 5 MB).

### Upgrading

Install over v1.2.12 or older; no need to uninstall, and your widget stays on the home screen with your city and settings.

### Package info

- **versionCode:** `663091332`
- **versionName:** `10.10.1059527-android36-v1.2.13`
