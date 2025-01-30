# Expo Linking API Inconsistent Deep Link Handling on Android

This repository demonstrates a bug in Expo's `Linking` API on Android where the `Linking.addEventListener` for deep links does not always fire when the app is already running.  This can lead to deep links being ignored.

## Steps to Reproduce

1. Clone this repository.
2. Run the app on an Android device or emulator.
3. Open a web browser and navigate to a deep link that should open the app.  The app may not receive the link consistently.

## Workaround

The provided `bugSolution.js` offers a potential workaround involving more aggressive handling of the deep link or using a different method of handling such situations like checking for a URI on component mount.