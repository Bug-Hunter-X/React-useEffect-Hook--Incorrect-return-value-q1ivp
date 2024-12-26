# React useEffect Hook: Incorrect return value
This example demonstrates an uncommon error in React's `useEffect` hook where the return value is not a cleanup function. The return value of a `useEffect` hook *must* be a cleanup function or `undefined`. Attempting to return a value that is not a function will lead to unexpected behavior and likely a silent error. 

The bug is in the `useEffect` hook's return statement. Returning `count * 2` is incorrect; it should return a function to clean up any side effects.