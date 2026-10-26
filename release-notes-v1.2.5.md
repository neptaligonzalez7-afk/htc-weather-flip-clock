## HTC Weather Flip Clock — v1.2.5 (Oct 2026)

**Auto-detect location follow-up** (Open-Meteo only — no extra apps or Cloudflare).

### Auto-detect

- **One-shot GPS** after fused/network when setting up current location (not continuous tracking).
- **12 s** wait when there is no cached fix yet.
- **Immediate sync** when location permission is granted (setup flow).
- Use **stored `cur` coordinates** or last GPS prefs when a live fix is still pending.
- Clearer logs when **system Location is off**.

### Package info

- **versionCode:** `663091324`
- **versionName:** `10.10.1059527-android36-v1.2.5`
