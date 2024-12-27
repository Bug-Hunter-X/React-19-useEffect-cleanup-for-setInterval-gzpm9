# React 19 useEffect Cleanup for setInterval
This repository demonstrates a common error in React 19 related to the useEffect hook and setInterval.  Forgetting to clear the interval in the cleanup function leads to memory leaks and unexpected behavior.

## The Bug
The `bug.js` file contains a component that uses `setInterval` to update a counter every second. However, it lacks the necessary cleanup function to clear the interval when the component unmounts or when the dependencies change.

## The Solution
The `bugSolution.js` file provides the correct implementation by clearing the interval in the cleanup function of the `useEffect` hook. This prevents memory leaks and ensures the component behaves as expected. 

## How to reproduce
Clone this repository and run `npm install`. Then, run `npm start` to see the bug in action. Check the browser's developer tools to inspect the potential memory issues when you navigate away from the page. Then, modify to test the fix.