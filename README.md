<div align="center">

# 🗺️ Safe-Yatra — Navigation Module

**Flutter navigation module for the Safe-Yatra safe-routes platform, built on the Google Navigation SDK.**

[![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?style=flat-square&logo=flutter&logoColor=white)](https://flutter.dev/)
[![Dart](https://img.shields.io/badge/Dart-3.x-0175C2?style=flat-square&logo=dart&logoColor=white)](https://dart.dev/)
[![Android](https://img.shields.io/badge/Android-API%2023+-3DDC84?style=flat-square&logo=android&logoColor=white)](https://developer.android.com/)
[![iOS](https://img.shields.io/badge/iOS-15.0+-000000?style=flat-square&logo=apple)](https://developer.apple.com/ios/)

</div>

---

## Overview

This package provides a `GoogleNavigationView` widget for Flutter apps targeting Android and iOS. It wraps the [Google Navigation SDK](https://developers.google.com/maps/documentation/navigation) and powers turn-by-turn navigation inside the Safe-Yatra app, including Android Auto and CarPlay support.

> Built on top of Google's `google_navigation_flutter` plugin and adapted for the Safe-Yatra deployment.

## Requirements

|  | Android | iOS |
|---|---|---|
| Minimum OS | API 23+ | iOS 15.0+ |

You'll also need:
- A Flutter project
- A Google Cloud project with the Navigation SDK enabled
- An API key restricted to Navigation SDK + Maps SDK for Android/iOS
- Kotlin 2.0+ and Google Play Services on Android

## Quick Start

```bash
flutter pub add google_navigation_flutter
```

### Android (`android/app/build.gradle`)

```groovy
android {
    defaultConfig { minSdkVersion 23 }
    compileOptions {
        coreLibraryDesugaringEnabled true
    }
}
dependencies {
    coreLibraryDesugaring 'com.android.tools:desugar_jdk_libs_nio:2.0.4'
}
```

### iOS (`ios/Podfile`)

```ruby
platform :ios, '15.0'
```

In `Info.plist`, add `App registers for location updates` to **Required background modes**.

## Features

- 🧭 Turn-by-turn navigation widget
- 🚗 Android Auto support — see [`ANDROIDAUTO.md`](ANDROIDAUTO.md)
- 🚙 CarPlay support — see [`CARPLAY.MD`](CARPLAY.MD)
- 🛣️ Custom route styling, markers, polylines, circles
- 🔔 Navigation events streamed to Dart

## Repository Layout

```
.
├── android/                 # Android platform code (Kotlin)
├── ios/                     # iOS platform code (Swift)
├── lib/                     # Dart API surface
├── example/                 # Sample Flutter app
├── ANDROIDAUTO.md           # Android Auto integration guide
├── CARPLAY.MD               # CarPlay integration guide
├── CONTRIBUTING.md
└── CHANGELOG.md
```

## Contributing

See [`CONTRIBUTING.md`](CONTRIBUTING.md) for development workflow, formatting, and PR guidelines.

## License

Apache-2.0 — see [`LICENSE`](LICENSE).
