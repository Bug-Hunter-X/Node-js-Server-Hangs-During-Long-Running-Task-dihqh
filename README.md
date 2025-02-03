# Node.js Server Hang Issue

This repository demonstrates a common issue in Node.js where a long-running task in the request handler can block the event loop, causing the server to become unresponsive. The `bug.js` file showcases the problem, while `bugSolution.js` provides a solution using asynchronous programming.

## Problem

The problem lies in the synchronous nature of the `while` loop in `bug.js`.  This loop blocks the event loop, preventing the server from handling other requests or gracefully shutting down.

## Solution

`bugSolution.js` demonstrates how to solve this by using asynchronous techniques, such as `setTimeout`, to prevent blocking the event loop. The asynchronous approach ensures that the server remains responsive while handling long-running tasks.