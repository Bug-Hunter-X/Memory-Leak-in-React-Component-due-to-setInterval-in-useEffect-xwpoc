# React setInterval Memory Leak

This repository demonstrates a common bug in React applications: memory leaks caused by the improper use of `setInterval` within the `useEffect` hook.

## The Problem

The `bug.js` file shows a React component that uses `setInterval` to update a counter every second.  However, it lacks a cleanup function to stop the interval when the component unmounts. This leads to the interval continuing to run indefinitely, even after the component is no longer visible, consuming resources and potentially causing memory leaks.

## The Solution

The `bugSolution.js` file provides the corrected implementation.  It uses the return value of `useEffect` to provide a cleanup function that calls `clearInterval` to stop the interval when the component unmounts, preventing the memory leak.

## How to Run

1. Clone this repository.
2. Navigate to the repository's directory in your terminal.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.