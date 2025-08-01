# Jansuvidha Android App

This is a fully functional Android application for the website [https://www.jansuvidha.com](https://www.jansuvidha.com) built using WebView.

## Features

1.  **Splash Screen:** Displays the Jansuvidha logo and a "Press to Enter" button.
2.  **Main WebView Screen:** Loads `https://www.jansuvidha.com` in a WebView.
    *   All internal and external links open within the app.
    *   Supports file uploading and downloading.
    *   Supports opening PDF files within the app using Android’s native PDF viewer.
    *   Includes a fixed back button at the bottom-left corner.
    *   Prompts for exit confirmation if there is no page to go back to.
3.  **Additional Features:**
    *   Supports file upload/download from input forms.
    *   Compatible with Android 7 (API level 24) and above.
    *   Shows a loading indicator while the WebView loads pages.

## Project Structure

```
JansuvidhaApp/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── AndroidManifest.xml
│   │   │   ├── java/com/jansuvidha/app/
│   │   │   │   ├── MainActivity.kt
│   │   │   │   └── SplashActivity.kt
│   │   │   └── res/
│   │   │       ├── layout/
│   │   │       │   ├── activity_main.xml
│   │   │       │   └── activity_splash.xml
│   │   │       ├── mipmap/
│   │   │       │   └── jansuvidha_logo.png
│   │   │       └── values/
│   │   │           ├── colors.xml
│   │   │           ├── strings.xml
│   │   │           └── themes.xml
│   ├── build.gradle
├── build.gradle
├── gradle.properties
└── settings.gradle
```

## How to Build and Run

1.  **Prerequisites:**
    *   Android Studio installed.
    *   Android SDK Platform 34 installed.
    *   Kotlin plugin for Android Studio.

2.  **Open Project:**
    *   Open Android Studio.
    *   Select `File > Open` and navigate to the `JansuvidhaApp` directory.

3.  **Sync Gradle:**
    *   Android Studio will automatically try to sync the Gradle project. If it doesn't, click `File > Sync Project with Gradle Files`.

4.  **Run on Emulator/Device:**
    *   Connect an Android device or start an Android Emulator.
    *   Click the `Run` button (green triangle) in Android Studio to install and launch the app.

## Permissions

The app requires the following permissions, declared in `AndroidManifest.xml`:

*   `android.permission.INTERNET`: For WebView to load web content.
*   `android.permission.ACCESS_NETWORK_STATE`: To check network connectivity.
*   `android.permission.READ_EXTERNAL_STORAGE`: For file upload functionality.
*   `android.permission.WRITE_EXTERNAL_STORAGE`: For file download functionality.

## Customization

*   **Website URL:** To change the loaded website, modify the `websiteUrl` variable in `MainActivity.kt`.
*   **Splash Screen Logo:** Replace `jansuvidha_logo.png` in `app/src/main/res/mipmap/` with your desired logo.
*   **App Name:** Modify the `app_name` string in `app/src/main/res/values/strings.xml`.



