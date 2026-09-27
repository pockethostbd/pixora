PIXORA ADMIN SETUP

1. Firebase Console -> Authentication -> Sign-in method -> enable Email/Password.
2. Create one admin user.
3. In firestore.rules replace YOUR_ADMIN_EMAIL@example.com with that exact admin email.
4. Publish the Firestore rules.
5. Host the whole Pixora folder. Open /admin/ once online so the service worker can cache the admin shell and Firebase modules after the first successful load.
6. The admin interface can then open offline. New URLs entered offline are stored locally and automatically synced when the device reconnects and the admin is signed in.

FIRESTORE COLLECTION
images/{autoId}
  imageUrl: string
  createdAt: server timestamp

IMPORTANT
The Firebase web apiKey is not a secret. Security comes from Firebase Authentication + Firestore Rules. Do not use public write rules.
