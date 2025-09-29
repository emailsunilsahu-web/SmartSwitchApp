# SmartSwitchApp (Android, Kotlin, Jetpack Compose)

A tiny controller app for your ESP8266 Smart Switch firmware. Enter the device URL (e.g., `http://192.168.4.1` in AP mode or `http://<device-ip>` on your Wi‑Fi), then:
- ON → `/<on>`
- OFF → `/<off>`
- Stop Timer → `/stop`
- Set Timer → `/timer?m=..&s=..` (POST)
- Change Wi‑Fi → `/change`

## Build
1. Open this folder in Android Studio (Giraffe or newer).
2. Let Studio create/download a Gradle wrapper if prompted.
3. Run on your Android device (Internet permission is already declared).

## Notes
- The app polls `/status` every second to keep UI in sync.
- Works with the exact endpoints in your ESP8266 sketch.
- If you change endpoints on the device, update the buttons' URLs in `MainActivity.kt`.