SchoolTrack EAPIHS — Firebase web app package

Files:
- public/index.html, app.js, style.css, config.js, manifest.json, service-worker.js, icon.svg
- firestore.rules

Important:
1. The app's Firebase config is filled for project school-track-9985f and admin UID supplied in chat.
2. The UID in firestore.rules matches config.js. Verify it matches the UID of the intended admin account in Firebase Authentication.
3. Rules included in this package are a local copy; publishing this file does NOT publish rules to Firebase automatically. Check Firestore > Rules in Firebase Console and confirm the published rules contain the same UID.
4. Host the contents of the public folder using Firebase Hosting or another HTTPS static host. Firebase Hosting CLI usually requires Node.js/npm and a terminal; it cannot be completed just by opening this ZIP on a phone.
5. Authentication providers Email/Password and Anonymous must be enabled.
6. This app uses Firebase Authentication and Cloud Firestore. First sign-in/data load requires internet. Firestore offline cache is best-effort; test offline behavior before relying on it.
7. Security rules allow any authenticated user, including anonymous guests, to read inventory, settings, and activity; only the configured admin UID can write. Do not store confidential student information in these collections.
8. Firebase client config values are not a substitute for security rules. Never include a service-account private key or password in public files.
