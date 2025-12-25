# TypingHub

A simple and effective typing practice application designed for speed and accuracy training.

## Features
- **PWA Support**: Installable on Desktop and Mobile. Works offline.
- **SSC Mock Mode**: Simulates SSC CGL typing test environment.
- **Real-time Stats**: WPM, Accuracy, and Timer.
- **Visual Feedback**: Highlight correct/incorrect characters (disabled in Exam Mode).

## How to Install (PWA)
1.  **Desktop**: Open in Chrome/Edge. Click the "Install" icon in the address bar.
2.  **Mobile**: Open in Chrome on Android. Tap "Add to Home Screen".

## How to Convert to TWA (Android App)
To publish this as a Trusted Web Activity (TWA) on the Google Play Store:

### Prerequisites
1.  Deploy this project to a public URL (e.g., GitHub Pages, Firebase, Vercel).
    - Ensure it is served over HTTPS.

### Using PWABuilder (Recommended)
1.  Go to [PWABuilder.com](https://www.pwabuilder.com/).
2.  Enter your live URL (e.g., `https://username.github.io/typinghub/`).
3.  Click **Start**.
4.  Once analyzed, click **Package for Stores**.
5.  Select **Android**.
6.  Follow the steps to generate your APK/AAB file.
    - You will need to sign the app with a keystore (PWABuilder can generate a test one for you).

### Digital Asset Links (Important for "Trusted" status)
To remove the browser address bar in the Android app, you must verify ownership of the domain.
1.  When generating the Android package, you will get a `assetlinks.json` file (or the content for it).
2.  Create a folder named `.well-known` in your project root.
3.  Place the `assetlinks.json` file inside it: `/.well-known/assetlinks.json`.
4.  Redeploy your website.
5.  The Android app will now verify the relationship and run in full-screen mode.

### Offline Support
The included `service-worker.js` ensures the app works offline after the first visit.