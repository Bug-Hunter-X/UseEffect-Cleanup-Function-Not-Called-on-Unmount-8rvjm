# React useEffect Cleanup Not Called on Unmount

This repository demonstrates a bug where the cleanup function in a React 19 `useEffect` hook is not called when the component is unmounted.  This can lead to memory leaks or other unexpected behavior.

## Bug Description:

The `useEffect` hook includes a cleanup function that should run when the component is unmounted. However, in certain scenarios, this cleanup function might not be executed, leading to issues.

## Bug Reproduction:

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the console logs. The 'Cleanup' message should appear when the component unmounts, however it may not be shown.

## Solution:

This specific example is addressed by ensuring that the useEffect only runs when it needs to and is unmounted appropriately. Refer to `bugSolution.js` for a corrected implementation.