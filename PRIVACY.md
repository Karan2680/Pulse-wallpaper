# Pulse Wallpaper Privacy Notice

**Applies to Pulse Wallpaper and Pulse Wallpaper Web Audio v0.1.0**

## Desktop app

Windows setup asks for consent to access playback from supported music apps on your device. Pulse reads player identity and playback status to detect when to animate. It uses a verified player's audio samples or volume peaks when Windows can isolate that player. If you enable the optional album cover, Pulse reads available cover artwork from the Windows media session and draws it on the wallpaper.

Audio samples, cover artwork, and playback state are processed locally in memory. Pulse stores your consent and preferences on this PC. It does not create audio recordings, retain listening history, send telemetry, or request music-service credentials.

## Optional browser extension

The extension starts when you click its icon on a supported music tab. It uses the tab's URL to match the official music site. It analyzes the audio playing in that tab in browser memory and sends 32 frequency levels and the service identity to the desktop app through Chromium's local native messaging connection. The extension does not send raw audio to the desktop app, capture video, or upload data. It does not read browsing history, cookies, credentials, or unrelated tabs.

| Browser permission | Purpose |
| --- | --- |
| `activeTab` | Read the selected tab's address after you click Pulse to check that the tab is a supported music site. |
| `tabCapture` | Capture audio from the tab you select. |
| `offscreen` | Keep the selected tab audible and calculate frequency levels in the browser. |
| `nativeMessaging` | Send levels and service identity to Pulse Wallpaper on the same PC. |

## Your choices

Click the extension again or close the selected tab to stop web audio. Loading a new page, switching the tab to a different site, or losing the connection to Pulse also stops capture. You can remove the extension through the browser's extension manager. In Pulse Studio, clear **Music → Allow access to supported players**, then select **Apply to desktop** to stop music access. The wallpaper can still display a static design. You can decline the desktop consent terms by cancelling setup.

For privacy questions, contact the maintainer through this repository. Keep personal details out of public issues.
