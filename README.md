# React useEffect setInterval Memory Leak

This repository demonstrates a common mistake in React applications: using `setInterval` within the `useEffect` hook without proper cleanup. This leads to a memory leak, as the interval continues to run even after the component unmounts.

## Problem

The `bug.js` file contains a React component that uses `setInterval` to update a counter every second.  The issue is that the `setInterval` function is not properly cleaned up using `clearInterval`. This causes the interval to continue running indefinitely, even if the component is unmounted, leading to a memory leak.

## Solution

The `bugSolution.js` file provides a corrected version of the component.  It uses the return value of `useEffect` to call `clearInterval` when the component unmounts, thereby resolving the memory leak.

## How to run

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install`.
4. Run `npm start`.
