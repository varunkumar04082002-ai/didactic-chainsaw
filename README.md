# Meal Diary Android project

This Android Studio project wraps the finalized HTML UI in a WebView and stores food records in a JSON file inside a user-selected folder using Android's Storage Access Framework.

## Storage behaviour
- First launch asks you to choose a folder using Android's folder picker.
- The app creates/updates `meal_diary_records.json` inside that folder.
- Food records are read from that file at startup; add/edit/delete operations write back to it.
- No import/export/backup controls are shown in the app.
- The dark/light theme preference remains in WebView local storage; food records do not.

## Build APK
1. Open this folder in Android Studio (current stable version).
2. Allow Android Studio to sync Gradle and install the Android SDK platform 35 if prompted.
3. Choose **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
4. Android Studio will show the generated APK path (normally `app/build/outputs/apk/debug/app-debug.apk`).

The APK must be tested on a real Android device. The app uses the selected folder's document provider; some cloud-backed providers may behave differently from local internal storage. Prefer a normal folder in Internal storage, e.g. `Documents/MealDiary`.
