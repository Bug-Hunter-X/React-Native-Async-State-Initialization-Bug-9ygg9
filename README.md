# React Native Async State Initialization Bug

This repository demonstrates a common bug in React Native: accessing state before it's initialized. The bug is reproduced in `BugAsyncState.js` and the solution is provided in `SolutionAsyncState.js`.

## Bug Description:

When using async functions to fetch data and update state, there's a risk of accessing the state before the asynchronous operation completes, leading to undefined state values and potential crashes. This is a race condition between state update and state access.

## Solution:

The solution utilizes `useEffect` with an empty dependency array to ensure that the state is accessed only after it's fully initialized. The code within the `useEffect` hook runs after the initial render, guaranteeing that the state is ready.

## How to reproduce:

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npx react-native run-android` or `npx react-native run-ios`.
4. Observe the error in the original bug file.
5. Check the correct behaviour in the solution file.

## Contribution:

Feel free to contribute to improve this example or report other common React Native bugs.