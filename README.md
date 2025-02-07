# Uncommon React useEffect Bug: Missing Dependency in State Update

This repository demonstrates a subtle yet common bug in React's `useEffect` hook that can lead to unexpected infinite loops.  The issue arises from improperly managing dependencies within the `useEffect`'s second argument (the dependency array).

## The Bug
The provided `MyComponent` uses `useState` to manage a counter.  The `useEffect` hook logs the current count to the console after every render. However, the `useEffect` has a missing dependency, leading to an infinite render loop. 

## The Solution
The solution involves correctly specifying the dependencies in the dependency array. By including `count` in the array, the effect only runs when the value of `count` changes, preventing the infinite loop.

## How to reproduce
1. Clone the repository.
2. Run `npm install` to install the necessary packages.
3. Run `npm start` to start the development server.
4. Observe the infinite console logs in your browser's developer tools.