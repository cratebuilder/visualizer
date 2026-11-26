CRATE DESIGNER 3D — NATIVE INSTALLER BUILD PACKAGE

This folder contains the app source and build configuration for:
- Android APK (Capacitor)
- Windows 64-bit EXE installer (Electron + NSIS)

BUILD BOTH INSTALLERS AUTOMATICALLY (recommended)
1. Create a new GitHub repository.
2. Upload the CONTENTS of this folder to the repository root (including the hidden .github folder).
3. Open the repository's Actions tab.
4. Select “Build Crate Designer 3D installers” and click “Run workflow”.
   Alternatively, pushing to the main or master branch starts the build automatically.
5. When both jobs finish, open the workflow run and download these Artifacts:
   - Crate-Designer-3D-Android-APK
   - Crate-Designer-3D-Windows-EXE

ANDROID
- The workflow creates a debug APK at android/app/build/outputs/apk/debug/app-debug.apk.
- It can be installed on Android after allowing installation from the source used to download it.
- A release APK signed with your own private signing key is required for Play Store distribution.

WINDOWS
- The workflow creates a 64-bit NSIS setup EXE in dist/.
- It is currently unsigned. Windows SmartScreen may show an unknown-publisher warning.
- Commercial distribution should use a code-signing certificate.

IMPORTANT
- The original Crate Designer 3D HTML interface is bundled locally in both apps.
- The HTML app loads several libraries and fonts from public CDNs. Internet is needed for those resources unless they are later vendored locally. The native shell itself opens from bundled files.
- The APK/EXE are built by GitHub Actions because this build environment does not have the Android SDK/Gradle toolchain or a Windows host required to produce these installers here.
