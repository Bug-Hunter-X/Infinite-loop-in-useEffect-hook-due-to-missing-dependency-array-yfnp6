# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug arises from omitting the dependency array in `useEffect`, leading to an infinite re-render loop.

## Bug Description

The `bug.js` file contains a component that uses the `useEffect` hook to log the current count to the console after every render.  Because the dependency array is missing, the effect runs after every render, causing `count` to update and triggering another render.  This results in an infinite loop and potential browser crashes.

## Solution

The `bugSolution.js` file demonstrates the correct way to use the `useEffect` hook, adding the `count` variable as a dependency in the dependency array. This ensures the effect only runs when the value of `count` changes, resolving the infinite loop.

## How to Reproduce

1. Clone the repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.
5. Observe the console output and the browser's behavior with both `bug.js` and `bugSolution.js` files to understand the difference.

## Lesson Learned

Always include a dependency array in `useEffect` to control when the effect runs.  Omitting it often leads to unexpected behavior and performance issues.