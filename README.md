# Firebase onAuthStateChanged Listener Inconsistency

This repository demonstrates a bug where the Firebase `onAuthStateChanged` listener intermittently fails to update the UI when the user's authentication state changes. The problem might stem from network fluctuations, conflicts with other SDKs, or subtle timing issues. The solution offers a more robust approach using retries and error handling.

## Setup

1.  Clone this repository.
2.  Install Firebase:
    ```bash
    npm install firebase
    ```
3.  Configure Firebase (see `firebaseConfig.js`).

## Reproduction

Run `firebaseBug.js`. Observe that sometimes the authentication state change isn't reflected immediately in the console logs or UI updates (if you were to integrate with a visual element).