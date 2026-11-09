# StudyMate AI — Android starter project

This is an Android Studio starter app built with Kotlin and Jetpack Compose.

## Open
1. Install Android Studio.
2. Choose **Open** and select this project folder.
3. Allow Gradle sync.
4. Run on an Android emulator or connected phone.

## Current prototype features
- Home dashboard and bottom navigation
- Tutor chat screen (demo response only)
- Android PDF document picker
- Sample NPV practice question with answer feedback
- Study checklist

## Important: AI and PDF analysis are not connected yet
The screens are a working UI prototype. Real AI chat, PDF text extraction, document-grounded answers, assignment analysis and generated study plans require a secure backend service.

Do **not** put a private AI provider API key inside the Android app. The app should call your own backend; the backend stores the secret and calls the AI provider. Configure the backend URL in `app/build.gradle.kts` and implement authenticated API calls before production.

## Next development milestones
1. Build a secure backend endpoint for tutor chat.
2. Add PDF upload and server-side text extraction.
3. Add retrieval so answers cite the uploaded lecture pages.
4. Add assignment workspace and exam question generation.
5. Add persistent planner, progress and account sync.
6. Test, sign and build a release APK.

This project is a source-code starter, not a prebuilt APK.

## Build an APK using GitHub Actions
This project includes `.github/workflows/build-apk.yml`.
1. Create a GitHub repository and upload the contents of this project.
2. Open the repository's **Actions** tab.
3. Run **Build StudyMate AI APK** (or push to the `main` branch).
4. When the workflow succeeds, open its run and download the `StudyMateAI-debug-apk` artifact.
5. Extract the artifact ZIP to get `app-debug.apk`, then install it on an Android device.

The APK is a debug prototype. It does not yet contain a live AI backend or real PDF analysis.
