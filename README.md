# React useEffect setInterval Memory Leak

This example demonstrates a common mistake when using the `setInterval` function within a React `useEffect` hook.  Without proper cleanup, memory leaks occur because the interval continues even after the component is unmounted.

## Bug
The `bug.js` file contains a React component that uses `setInterval` to update a counter every second. However, it lacks the necessary cleanup function to stop the interval when the component is unmounted, leading to a memory leak. 

## Solution
The `bugSolution.js` file provides a corrected version. It uses the return value of `useEffect` to clean up the interval when the component is unmounted. This prevents memory leaks.