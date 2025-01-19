# Expo Constants.deviceId returns null or undefined in async function

This repository demonstrates a common issue encountered when using `Constants.deviceId` within asynchronous operations in Expo applications.  The problem stems from the asynchronous nature of fetching the device ID; if the value is accessed before it's fully retrieved, it will be `null` or `undefined`, resulting in errors.

The `bug.js` file showcases the problematic code.  The solution, implemented in `bugSolution.js`, demonstrates how to resolve the issue by appropriately handling the asynchronous operation and waiting for the `deviceId` to be available before usage.

## Reproducing the Bug
1. Clone this repository.
2. Navigate to the directory in your terminal.
3. Run `expo start`.
4. Observe the console logs and the app's behavior in both `bug.js` and `bugSolution.js` files.