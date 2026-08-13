# Frith Uploader

Minimal Android media uploader for [frith](https://github.com/vloeibaarglas/frith) servers. Pick an image or share from any app.

## Stack

Kotlin, Jetpack Compose, Material 3, OkHttp, Coil

## Building

### Prerequisites
- JDK 17+
- Android SDK (compileSdk 34)

### Build
```bash
# Debug APK
./gradlew assembleDebug
# Output: app/build/outputs/apk/debug/app-debug.apk

# Release APK
./gradlew assembleRelease
# Output: app/build/outputs/apk/release/app-release.apk
```

## Upload API

Matches frith 1:1:

- `POST {server}/{path}` (default `/api/upload`) — multipart form field `file`
- Auth: `Authorization: Bearer <token>`
- Response: `{"files":[{"url":"https://.../u/abc.png"}]}` — the app copies `files[0].url`

## License

[MIT](https://github.com/vloeibaarglas/Frith-Uploader/blob/main/LICENSE)
