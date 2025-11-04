# ReelOn (React Native CLI) - Source-only

This is a **source-only** React Native project for the "ReelOn" auth screen (Email/Password) using Firebase Auth and Firestore.

## What is included
- `App.js` - entry component
- `screens/AuthScreen.js` - Login / Signup screen (uses Firebase Web SDK modular imports)
- `firebaseConfig.js` - placeholder config (replace with your Firebase values)
- `package.json` - minimal dependencies (no node_modules included)
- `README.md` - this file

## Important notes for React Native CLI users
1. This zip does **NOT** include `node_modules`, Android/ iOS builds or native config.
2. The Firebase Web SDK (v9+) is included in `package.json`. Using Firebase with React Native CLI can require extra setup:
   - You may need to install additional polyfills (e.g., for `react-native-get-random-values`) or use `react-native-firebase` (native SDK) for a smoother experience.
   - If you use the Web SDK, follow these quick steps after extracting:
     - `npm install`
     - Install polyfills if required:
       - `npm install react-native-get-random-values`
       - and at top of `App.js` add: `import 'react-native-get-random-values';`
     - Then run Metro: `npx react-native start`
     - Run on Android: `npx react-native run-android`

3. If you prefer **react-native-firebase** (recommended for RN CLI):
   - Follow official docs: https://rnfirebase.io/
   - Replace `firebaseConfig.js` and firestore/auth usage with `@react-native-firebase/app`, `@react-native-firebase/auth`, `@react-native-firebase/firestore`.

## Run steps (React Native CLI)
1. Extract the zip.
2. In project root:
   ```
   npm install
   npx react-native start
   npx react-native run-android
   ```
3. For iOS (macOS):
   ```
   cd ios
   pod install
   cd ..
   npx react-native run-ios
   ```

## Replace Firebase config
Open `firebaseConfig.js` and paste your Firebase config (from Firebase Console → Project Settings → Add Web App).

## Troubleshooting
- If you see errors related to `crypto`, `URL`, or other Node shims, refer to React Native + Firebase web SDK polyfills or switch to `react-native-firebase`.

Enjoy! 🙌
