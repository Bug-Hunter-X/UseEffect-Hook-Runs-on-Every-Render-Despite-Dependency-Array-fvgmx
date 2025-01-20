# React useEffect Hook Runs on Every Render Despite Dependency Array

This repository demonstrates a common issue with the React `useEffect` hook where the effect runs on every render, even when a dependency array is provided.

## Problem
The provided `useEffect` hook is intended to only run when the `count` state variable changes.  However, it actually runs on every render, causing unnecessary console logs and potentially performance issues.

## Solution
The solution involves properly managing dependencies within the `useEffect` dependency array and ensuring that no other values used within the effect are changing outside of the dependency array. In this case the issue is resolved and the effect only runs when the count changes. 

## How to reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console logs as you click the button.  You'll see that the log message appears on every render, not just when the count changes.
