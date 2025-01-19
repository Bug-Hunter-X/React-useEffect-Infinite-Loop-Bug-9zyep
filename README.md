# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications involving the `useEffect` hook: an infinite loop caused by a missing dependency.

## Bug Description
The `MyComponent` component uses `useState` to track a count.  The `useEffect` hook logs the count to the console after every render.  However, because `count` is not listed as a dependency in the `useEffect`'s second argument array, the effect runs on every render, causing the count to update continuously, leading to an infinite loop and an overwhelming amount of console output.

## Bug Solution
The solution involves adding `count` as a dependency to the `useEffect` hook.  This ensures the effect only runs when the value of `count` changes.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the continuous updates in the browser's console.
