# Unresponsive Node.js Server

This repository demonstrates a common issue in Node.js applications where a long-running synchronous operation blocks the event loop, making the server unresponsive.  The `bug.js` file contains the problematic code, while `bugSolution.js` provides a solution using asynchronous operations.

## Bug

The server in `bug.js` performs a 5-second CPU-bound operation within the request handler.  During this time, no other requests can be processed, leading to unresponsiveness.

## Solution

`bugSolution.js` demonstrates how to use asynchronous operations (in this case, `setTimeout`) to avoid blocking the event loop.  This allows the server to continue handling other requests while the long-running task executes in the background.