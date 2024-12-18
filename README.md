# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug: an infinite loop caused by an incorrectly used `useEffect` hook.  The `useEffect` hook, without proper dependency array management, can lead to unintended re-renders and performance issues, potentially crashing the browser.

## Bug Description
The `bug.js` file contains a component with a `useEffect` hook that's missing a crucial optimization. The `count` variable is not correctly added to the dependencies array. This causes the effect to continuously trigger itself after each render, leading to an infinite loop. 

## Solution
The `bugSolution.js` file demonstrates the correct implementation.  By adding `count` to the dependency array, `useEffect` only runs when the value of `count` changes.