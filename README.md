# BookNook

The sign-in module for **BookNook**, an online library web app. It uses **Firebase Authentication** so readers can log in with Google, Facebook or their phone number (OTP).

## Features

- **Google sign-in** with a popup
- **Facebook sign-in**
- **Phone number login** with an OTP sent by SMS and protected by reCAPTCHA
- Shows the signed-in user's name or phone number, with a logout option
- Set up for **Firebase Hosting**

## Tech stack

JavaScript (ES modules) · Firebase Auth v9 (modular SDK) · Vite · Firebase Hosting

## Project structure

```
├── auth.js             # Login page and Firebase Auth logic (Google, phone OTP)
├── main.js             # Button handlers: login, OTP send/verify, logout
├── firebaseConfig.js   # Firebase project config
├── firebaseInit.js     # Firebase app initialisation
├── firebase.json       # Firebase Hosting config
├── .firebaserc         # Firebase project alias
└── package.json
```

## Run locally

```bash
git clone https://github.com/Dracoindie/Booknook.git
cd Booknook
npm install
npm run dev
```

To use your own Firebase project:

1. Create a project in the [Firebase console](https://console.firebase.google.com/).
2. Under **Authentication → Sign-in method**, enable Google, Facebook and Phone.
3. Replace the values in `firebaseConfig.js` with your project's config.
4. Add `localhost` under **Authentication → Settings → Authorized domains**.

## Deploy

```bash
npm run build
firebase deploy
```

## Roadmap

- [ ] Book catalogue and search
- [ ] Personal reading list for signed-in users
- [ ] Protected routes after login

## Author

**Nishchay Singh**: [@Dracoindie](https://github.com/Dracoindie)
