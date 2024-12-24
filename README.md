# React useEffect Hook Not Updating on State Change

This example demonstrates a common issue with the React `useEffect` hook where it doesn't update as expected when a state variable changes. The problem arises from using an empty dependency array `[]`, which causes the effect to run only once when the component mounts, rather than on every state change.

## Bug
The initial `console.log` statement inside `useEffect` will only print the initial value of the `count` variable (0). Subsequent changes to the `count` state will not trigger a re-run of the effect.

## Solution
To fix this, include the `count` state variable in the dependency array: `[count]`.  This ensures that the effect runs whenever `count` changes.