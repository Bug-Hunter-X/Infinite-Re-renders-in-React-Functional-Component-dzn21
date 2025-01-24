# Infinite Re-renders in React Functional Component

This repository demonstrates a common React bug: infinite re-renders caused by incorrectly using the `useEffect` hook. The `bug.js` file contains a component that re-renders infinitely.  The solution is provided in `bugSolution.js`.

## Bug Description
The `useEffect` hook, without proper dependency array management, triggers a re-render each time the component updates, creating an infinite loop. This leads to performance issues and potentially crashes. 

## Bug Solution
The issue is resolved by specifying the dependency array in the `useEffect` hook.  In this case, we only want the effect to run when the `count` changes, hence `[count]` is the correct dependency array.  If the dependency array is empty (`[]`), the effect runs only once after the initial render.