# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by missing dependencies. The component continuously re-renders because the effect function is always executed.

## Bug

The `bug.js` file contains the buggy component. The `useEffect` hook is missing the `count` variable in its dependency array. This causes the effect to run after every render, regardless of whether the `count` value has actually changed.  This leads to an infinite render loop, resulting in performance issues and potential crashes.

## Solution

The `bugSolution.js` file shows the corrected version. By including `count` in the dependency array, the effect only runs when the `count` value changes. This fixes the infinite loop.