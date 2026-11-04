# HD Video Downloader (Android)

An Android app for downloading **direct, non-DRM video file URLs** (for example MP4, WebM, MOV, M4V, MKV and 3GP), with download history and an in-app player.

## Supported and unsupported links

- Direct video file URLs: supported when the server allows access and the user has permission to download the file.
- YouTube and Instagram post/reel URLs: detected and can be opened in the official app/site, but this app does **not** extract or download their protected media. A normal post/reel URL is not a direct video file URL.
- DRM-protected streams and unauthorized/private content: not supported.

Only download content you own or are authorized to save. Follow the source service terms and applicable copyright law.

## Build an APK on GitHub (no computer required)

1. Create a new **public or private** GitHub repository.
2. Upload the complete contents of this folder (not just this ZIP) to the repository's `main` branch. Keep the `.github/workflows/android.yml` file.
3. Open the repository's **Actions** tab.
4. Select **Android APK Build**, tap **Run workflow**, and wait for the run to finish.
5. Open the successful run and download the artifact named `HD-Video-Downloader-debug-apk`.
6. Extract the artifact ZIP; install `app-debug.apk` on your Android phone. You may need to allow installation from that browser/file manager.

A new APK build also runs automatically whenever you push changes to `main` or `master`.

## Build locally

Requires JDK 17, Android SDK Platform 36, and Gradle 9.3.1:

```bash
gradle --no-daemon :app:assembleDebug
```

The debug APK is created at `app/build/outputs/apk/debug/app-debug.apk`. This repository workflow creates a **debug/test APK**, not a Play Store release-signed APK.
