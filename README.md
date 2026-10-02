# RupeeRizz Android App

This folder is a lightweight Android WebView shell around the existing RupeeRizz web app. It keeps the existing Next.js + Supabase backend intact while giving the project a Play-Store-ready Android application layer.

## 1. Point the app at your deployed RupeeRizz site

Edit `android/gradle.properties`:

```properties
rupeeRizzUrl=https://YOUR-DOMAIN.example
```

The deployed site must use HTTPS.

## 2. Open in Android Studio

Open the `android/` folder in Android Studio and let Gradle sync. The project targets Android 16 / API 36, which is the current Google Play target for new apps as of August 31, 2026.

## 3. Build

Generate a signed Android App Bundle from Android Studio:

`Build > Generate Signed Bundle / APK > Android App Bundle`

Use your Play App Signing / upload key when prompted.

## What the shell supports

- RupeeRizz authentication/session inside the WebView
- Existing receipt OCR and receipt verification flow
- Direct camera/file chooser for receipt capture
- AI Financial Copilot screen
- Mutual-fund category research screen
- Payments / Auto-Sync placeholder for the future consent-based bank/UPI connection
- Back navigation inside the web app

The live UPI/Google Pay connection is intentionally not implemented in this first build.
