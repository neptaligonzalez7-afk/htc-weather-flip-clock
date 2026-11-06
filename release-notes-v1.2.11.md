## HTC Weather Flip Clock — v1.2.11 (Nov 2026)

**New: Clock style.** Choose between HTC's original look and the HTC One X (Sense 4) look, each with the Sense 3 or the Sense 4 flip. Also faster city search and a smarter weather tap. This release includes everything from the unpublished v1.2.9 and v1.2.10 builds.

### New

- **Clock style setting.** Open the widget's settings and tap **Clock style** at the bottom (under °F / °C). Each style has a short description in the picker:

  | Style | Look | Flip |
  |-------|------|------|
  | **HTC design, Sense 3 flip** (default) | The original HTC flip clock: slim digits with a smooth gradient on white cards with a soft grey lower half. | The top card eases into its fall and settles gently as it lands. |
  | **HTC design, Sense 4 flip** | The original HTC cards and digits. | The One X's livelier flip: the top card drops at a steady pace while a shadow sweeps across, the new digits fade in behind it and the old half sinks away. |
  | **One X design, Sense 3 flip** | The HTC One X (Sense 4) look: bolder, wider digits with an embossed highlight on bright white cards split by a thin hinge. | The original HTC motion. |
  | **One X design, Sense 4 flip** | The One X digits and cards. | The One X's own flip. The most faithful Sense 4 look. |

- **One X weather bar.** The One X design also uses the One X's weather bar: near-black with fine pinstripes, white date, city and condition text, and high/low shown as "70°F / 64°F".
- **Sense 4 flip timing.** Taken from the One X's own widget (`HtcClockWidget.apk`): a steady fall, the new top digits fading in, a shadow on the lower half up to mid-flip, and the old bottom half sinking and fading as the new one lands. The flip length (0.67 s) and the unlock flip are the same as before.

### Improved

- **Faster city search.** Suggestions now appear in about 1 second instead of up to 5. City search no longer waits behind the weather-download rate limiter, and recent searches are cached.
- **Weather tap.** Tapping the weather icon, temperature or condition opens the **Sense 4 Weather** app if it's installed, and the city's weather.com forecast otherwise.

### Notes

- Your current look doesn't change when you upgrade: the default is still the HTC design with the Sense 3 flip.
- The One X files don't include Sense 4's shadow image, so the Sense 4 flip uses a soft gradient in its place. AM/PM uses HTC's artwork in both designs.
- If the widget doesn't switch right away after you pick a style, pick it again in **Clock style**.

### Upgrading

Install over v1.2.8 or older; no need to uninstall, and your widget stays on the home screen with your city and settings.

### Package info

- **versionCode:** `663091330`
- **versionName:** `10.10.1059527-android36-v1.2.11`
