# Writer's Keyboard (FlorisBoard-based)

This is the **custom-keyboard** project: FlorisBoard cloned and restructured for Writer's Keyboard.

## What’s done (Phase 1 restructure)

- **applicationId:** `com.writerskeyboard` (app installs as Writer's Keyboard, distinct from the original app in the parent folder)
- **App name:** "Writer's Keyboard" in all build types (debug, beta, release)
- **Project name:** WritersKeyboard (rootProject.name in settings.gradle.kts)
- **NOTICE:** FlorisBoard attribution (Copyright 2020-2026 The FlorisBoard Contributors); LICENSE is Apache 2.0 (unchanged)
- **Package:** Kept as `dev.patrickgold.florisboard` for stability; full rename to `com.writerskeyboard` can be done later

## How to build

From a terminal (avoid paths with apostrophes if you see script errors):

```bash
cd custom-keyboard
.\gradlew.bat assembleDebug
```

Or open the **custom-keyboard** folder in Android Studio and use **Build → Build Bundle(s) / APK(s) → Build APK(s)**.

Output: `app/build/outputs/apk/debug/app-debug.apk`

## Next steps (from EXECUTION_PLAN.md)

1. **Install and test:** Install the APK, enable "Writer's Keyboard" in system keyboard settings, verify typing.
2. **Phase 2:** Integrate the writer strip (thesaurus, search, AI) from the parent project’s `app` into this FlorisBoard codebase (see EXECUTION_PLAN.md in the repo root).
3. **Optional:** Replace launcher icons in `app/src/main/res/mipmap-*` with Writer's Keyboard assets from the parent `app/src/main/res/drawable/ic_launcher.xml` (or export to mipmaps).

## Parent project

The original Writer's Keyboard app (custom IME with strip, thesaurus, search, AI) lives in the parent folder:

- `../app/` — current Writer's Keyboard (standalone)
- `../EXECUTION_PLAN.md` — full migration and integration plan
