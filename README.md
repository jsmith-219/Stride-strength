# Stride Strength

A mobile-friendly strength workout dashboard for track coaches and athletes. The current version runs immediately in demo mode and stores changes in the browser.

## Run locally

The easiest preview method is to unzip the project and double-click `index.html`.

You can also run a local web server:

```bash
npm run dev
```

Open `http://localhost:5173`. No installation or downloads are required. Use the **Athlete / Coach** switch in the lower-left corner (tap the STRIDE logo on mobile) to preview both roles.

## What works now

- Coach and athlete dashboard views
- Editable daily workout in coach mode
- Athlete max-lift editing
- Automatic percentage-to-weight calculations, rounded to 5 lb
- Per-athlete workout completion tracking
- Browser persistence with `localStorage`
- Responsive phone and desktop layouts

## Next step: Firebase

Create a Firebase project, enable Email/Password Authentication, and create a Firestore database. Then add a `.env.local` file containing the public Firebase web-app configuration:

```env
VITE_FIREBASE_API_KEY=
VITE_FIREBASE_AUTH_DOMAIN=
VITE_FIREBASE_PROJECT_ID=
VITE_FIREBASE_STORAGE_BUCKET=
VITE_FIREBASE_MESSAGING_SENDER_ID=
VITE_FIREBASE_APP_ID=
```

The production data model should use `users`, `athletes`, `workouts`, and `workoutAssignments` collections. Athlete documents should be accessible only to the athlete and authorized coaches through Firestore Security Rules. Do not put service-account credentials in this project or commit `.env.local` to GitHub.

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
