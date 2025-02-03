# React Native Dimensions API Undefined Initial Value

This repository demonstrates a common issue in React Native applications when using the `Dimensions` API to obtain screen dimensions.  The `Dimensions.get('window').width` property may return `undefined` during initial component rendering. This can lead to errors or unexpected behavior if you directly use the value before it's populated.

The `bug.js` file shows the problematic code. The `bugSolution.js` file presents a corrected version that handles the initial `undefined` value gracefully, ensuring smooth app behavior.

## Reproducing the Issue

1. Clone the repository.
2. Navigate to the project directory.
3. Run `npm install` or `yarn install`.
4. Run the app on an emulator or device.
5. Observe the behavior of the `MyComponent` in `bug.js`.

## Solution

The solution involves using a state variable to store the width and updating it only when `Dimensions.get('window').width` is defined. The component renders only after the width is defined. 

See `bugSolution.js` for an effective implementation.