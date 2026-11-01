# Task Management App

A Flutter task manager with a profile setup, a task dashboard, local storage, and full English / Arabic support.

[Download APK](https://github.com/abdelrahmannagh70-dot/final_apprebo/releases/latest)

## Screenshots

| Create Profile | Camera | Gallery |
|---|---|---|
| <img src="screenshots/create_profile.png" width="200"> | <img src="screenshots/camera.png" width="200"> | <img src="screenshots/gallery.png" width="200"> |

| Home (EN) | Home (AR) | Add Task (EN) | Add Task (AR) |
|---|---|---|---|
| <img src="screenshots/home_en.png" width="200"> | <img src="screenshots/home_ar.png" width="200"> | <img src="screenshots/add_task_en.png" width="200"> | <img src="screenshots/add_task_ar.png" width="200"> |

## Features

- Create a profile (name and photo from camera or gallery)
- Home dashboard with task statistics (total, completed, pending)
- Today's tasks with status
- Add a task with title, description, status and color
- English and Arabic (with RTL layout) switchable from the app
- Responsive layout that adapts to different screen sizes

## Tech Stack

| Area | Package |
|---|---|
| Framework | Flutter / Dart |
| Responsive UI | flutter_screenutil |
| Localization | easy_localization |
| Local storage | hive, hive_flutter, hive_generator, build_runner |
| Image picking | image_picker |

## Project Structure

```
lib/
├── main.dart
├── todo_app.dart
└── features/
    ├── login/
    │   └── login_screen.dart
    ├── home/
    │   └── widgets/
    │       └── home_screen.dart
    └── add_task/
        └── add_task.dart

assets/
└── translations/
    ├── en.json
    └── ar.json
```

The project is organized by feature, so each screen keeps its own files together.

## How Responsive Design Works

The app is designed on a 420 x 812 canvas and scaled with `flutter_screenutil`:

```dart
ScreenUtilInit(
  designSize: const Size(420, 812),
  minTextAdapt: true,
  splitScreenMode: true,
)
```

| Unit | Meaning |
|---|---|
| `20.w` | width scaled to the screen |
| `20.h` | height scaled to the screen |
| `18.sp` | font size scaled to the screen |
| `12.r` | radius scaled to the screen |

## Localization

Translations live in `assets/translations/en.json` and `assets/translations/ar.json`, and are loaded with `easy_localization`.

## Getting Started

```bash
git clone https://github.com/abdelrahmannagh70-dot/final_apprebo.git
cd final_apprebo
flutter pub get
dart run build_runner build --delete-conflicting-outputs
flutter run
```

## Build a release APK

```bash
flutter build apk --release
```

Output: `build/app/outputs/flutter-apk/app-release.apk`

## Author

**Abdelrahman**: [GitHub](https://github.com/abdelrahmannagh70-dot)

