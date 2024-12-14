# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: creating an infinite loop by updating state with a value dependent on the state itself.  The `bug.js` file contains the buggy code.  The solution is provided in `bugSolution.js`.

## Problem

The `useEffect` hook in `bug.js` attempts to increment the `count` state variable on every render. Because the state change triggers a re-render, and the useEffect runs again on each re-render, this causes an infinite loop.