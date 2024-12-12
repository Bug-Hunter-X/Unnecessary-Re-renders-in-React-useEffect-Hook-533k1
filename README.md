# Unnecessary Re-renders in React useEffect Hook

This repository demonstrates a common issue with React's `useEffect` hook: unnecessary re-renders due to missing dependency array.

The `bug.js` file shows the problem: the `useEffect` hook runs after every render, leading to excessive logging and potential performance issues.  The `bugSolution.js` file provides a fix by using a dependency array to control when the effect runs.

## How to reproduce the bug

1. Clone the repository
2. Run `npm install`
3. Run `npm start`
4. Observe the console logs - notice they appear after every click, indicating that `useEffect` is firing unnecessarily.

## How to fix the bug

Refer to `bugSolution.js` for the fix. The addition of `[count]` as the dependency array ensures `useEffect` only runs when `count` changes.