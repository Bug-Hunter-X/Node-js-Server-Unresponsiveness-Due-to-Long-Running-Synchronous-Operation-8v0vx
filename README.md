# Node.js Server Unresponsiveness

This repository demonstrates a common performance issue in Node.js applications: unresponsiveness caused by long-running synchronous operations.  The `server.js` file contains a simple HTTP server that simulates a 5-second delay before responding to requests. This can lead to significant performance problems and a poor user experience.

The `serverSolution.js` file provides a solution using asynchronous operations to prevent blocking the event loop.

## How to reproduce the bug:

1. Clone this repository.
2. Run `node server.js`.
3. Make a request to `http://localhost:3000`. Observe the 5-second delay.

## Solution:

The solution involves refactoring the code to use asynchronous operations, preventing the event loop from being blocked.  The improved version is in `serverSolution.js`.