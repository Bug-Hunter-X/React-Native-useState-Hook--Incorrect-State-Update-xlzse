# React Native useState Bug

This repository demonstrates a common error when using the `useState` hook in React Native. The issue arises from an incorrect way of updating the state object. Directly mutating the state object doesn't trigger a re-render, resulting in the UI not reflecting changes.

## Bug Description
The `bug.js` file shows the incorrect implementation.  The `incrementCount` function attempts to increment `myState.count` directly. This doesn't trigger a re-render, causing the UI to remain unchanged even after the button press. 

## Solution
The solution in `bugSolution.js` demonstrates the correct approach. The `setMyState` function should be used to update the state object immutably using a functional update. This ensures the component correctly re-renders and the UI accurately reflects the changes.

## How to Reproduce
1. Clone the repository.
2. Run `npm install` to install the necessary dependencies.
3. Run `npx react-native run-android` or `npx react-native run-ios` to run the app.
4. Observe the unexpected behavior in the `bug.js` example and the correct behavior in the `bugSolution.js` example.