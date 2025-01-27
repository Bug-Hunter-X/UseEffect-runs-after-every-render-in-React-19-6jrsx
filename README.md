# React 19 useEffect Infinite Loop Bug

This repository demonstrates a common bug in React 19 where the `useEffect` hook runs after every render, leading to an infinite loop and application crash.  The issue arises from the absence of a dependency array in the `useEffect` hook.

## Bug Description

The provided `MyComponent` utilizes the `useEffect` hook without specifying a dependency array. As a result, the effect runs after each render, triggering a continuous update cycle.  The `console.log` statement visually confirms this behavior.  This can lead to performance issues and, in more complex scenarios, application crashes.

## Solution

The solution involves adding a dependency array to the `useEffect` hook. This array lists the values that trigger the effect's execution.  By including `count` in the dependency array, the effect only runs when the `count` state variable changes.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the infinite loop in the browser's console and the application crashing (or significant performance issues).