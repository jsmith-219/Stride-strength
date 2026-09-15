# Stride Strength

A mobile-friendly strength workout dashboard for track coaches and athletes, connected to Firebase Authentication and Cloud Firestore.

## Run locally

The easiest preview method is to unzip the project and double-click `index.html`.

You can also run a local web server:

```bash
npm run dev
```

Open `http://localhost:5173`. No installation or downloads are required. Use the **Athlete / Coach** switch in the lower-left corner (tap the STRIDE logo on mobile) to preview both roles.

## What works now

- Google sign-in restricted to the authorized coach and MVCS student domain
- Coach and athlete dashboard views determined by the signed-in account
- Editable daily workout in coach mode
- Athlete max-lift editing
- Automatic percentage-to-weight calculations, rounded to 5 lb
- Per-athlete workout completion tracking
- Cloud persistence through Firestore
- Responsive phone and desktop layouts

## Firebase setup

Enable Google Authentication and Cloud Firestore. In Firebase Console, open **Firestore Database → Rules**, replace the editor contents with `firestore.rules`, and publish. The authorized domain must include `jsmith-219.github.io`.

Never put service-account credentials or private Admin SDK keys in this project.

## Publish to GitHub

Create an empty repository on GitHub, then run:

```bash
git init
git add .
git commit -m "Create Stride Strength starter"
git branch -M main
git remote add origin YOUR_REPOSITORY_URL
git push -u origin main
```

For the eventual authenticated version, Firebase Hosting is recommended even though the source code remains on GitHub.
