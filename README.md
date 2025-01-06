# Stale Closure in React's useEffect Hook

This repository demonstrates a common error in React applications: forgetting to include all necessary variables in the dependency array of the `useEffect` hook. This can lead to stale closures, where the effect uses outdated values, resulting in unexpected behavior.

## The Bug
The `bug.js` file contains a React component that uses `useState` and `useEffect`. The `useEffect` hook intends to log the current value of `count` to the console every time it changes. However, the dependency array is missing `count`, causing the effect to use the value of `count` from the initial render, even when the `count` value changes.