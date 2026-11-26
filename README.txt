CRATE DESIGNER 3D — ANDROID APK + WINDOWS EXE

This repository is configured for building native installers with GitHub Actions.

Before building, ensure the original app HTML is present at www/index.html, plus the Electron entry point at electron/main.cjs and the workflow at .github/workflows/build-native.yml.

The Android output is a debug APK (not Play Store signed). The Windows output is an unsigned 64-bit NSIS installer.
