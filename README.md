# Unhandled Error in Asynchronous Express.js Route Handler

This example demonstrates a common error in Node.js applications using Express.js: unhandled errors in asynchronous route handlers.  The error occurs when an exception is thrown within an asynchronous operation (like a setTimeout callback) without proper error handling.

The `bug.js` file contains the buggy code.  The `bugSolution.js` file shows how to fix this using a `try...catch` block or by using async/await.

## How to reproduce

1. Clone this repository.
2. Navigate to the directory
3. Run `npm install express`
4. Run `node bug.js`
5. Observe that the server starts but crashes silently when the error condition is met (randomNumber < 0.5).

## Solution

The solution involves placing the asynchronous operation within a `try...catch` block to gracefully handle potential exceptions.