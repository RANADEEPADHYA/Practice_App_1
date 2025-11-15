# Practice_App_1

A Flutter project demonstrating Android 12 splash screen, adaptive launcher icons, and custom app name configuration.

## 🚀 Features

- Android 12–compatible splash screen
- Auto-generated launcher icons for Android, iOS, Web, Windows, macOS
- Custom app name using launcher_name
- Adaptive icon with YouTube-style foreground
- Proper 960×960 safe-zone Android 12 icon support

## 🛠️ Tech Stack

- Flutter SDK 3.9.2
- flutter_native_splash
- flutter_launcher_icons
- launcher_name

## 📂 Project Structure

```yaml
assets/
  images/
    social.png
    youtube_icon_960_safe.png
    youtube_foreground.png
lib/
  main.dart
pubspec.yaml
```

## 🔧 Splash Screen Setup

Configured using **flutter_native_splash**:

```yaml
flutter_native_splash:
  color: "#FFFFFF"
  image: assets/images/youtube_icon_960_safe.png
  android_12:
    image: assets/images/youtube_icon_960_safe.png
    icon_background_color: "#FFFFFF"
```

**Generate splash screen:**

```bash
flutter pub run flutter_native_splash:create
```

## 🎨 Launcher Icon Setup

Configured using **flutter_launcher_icons**:

```yaml
flutter_launcher_icons:
  android: true
  ios: true
  remove_alpha_ios: true
  image_path: "assets/images/social.png"
  adaptive_icon_foreground: "assets/images/youtube_foreground.png"
  adaptive_icon_background: "#FF0000"
  web:
    generate: true
    image_path: "assets/images/social.png"
  windows:
    generate: true
    image_path: "assets/images/social.png"
    icon_size: 48
  macos:
    generate: true
    image_path: "assets/images/social.png"
```

**Generate launcher icons:**

```bash
dart run flutter_launcher_icons
```

## 📝 Custom App Name

```yaml
launcher_name:
  default: "Practice App 1"
```

**Apply app name:**

```bash
flutter pub run launcher_name
```

## ▶️ Run the Project

```bash
flutter pub get
flutter run
```

## 🧪 Supported Platforms

- Android
- iOS
- Web
- Windows
- macOS

## 📌 Notes

- Android 12 requires 960×960 foreground icons.
- Adaptive icons must have transparent background around the safe zone.
- Ensure all assets listed in pubspec.yaml exist physically.
