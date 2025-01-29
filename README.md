# React useEffect Hook Memory Leak

This example demonstrates a common mistake in React's `useEffect` hook when using `setInterval`.  Forgetting to clear the interval when the component unmounts can lead to memory leaks and unexpected behavior.

The `bug.js` file contains the buggy code, while `bugSolution.js` provides the corrected version.

## How to reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the counter.  Unmounting and remounting the component will show the memory leak.

## Solution

The solution involves using the return value of the `useEffect` hook to add a cleanup function that clears the interval.