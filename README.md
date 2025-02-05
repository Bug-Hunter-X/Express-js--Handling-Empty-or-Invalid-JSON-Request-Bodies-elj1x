# Express.js: Handling Empty or Invalid JSON Request Bodies

This repository demonstrates a common issue in Express.js applications where the server fails to gracefully handle empty or malformed JSON request bodies.  The provided code shows the problem and a solution for robust error handling.

## Bug

The `bug.js` file contains an Express.js application that attempts to parse the JSON request body using `express.json()`. However, it does not include error handling for cases where the request body is empty or not valid JSON. This leads to server-side errors.

## Solution

The `bugSolution.js` file presents an improved version. It uses a middleware function to check for empty requests and handles JSON parsing errors more effectively, providing a better user experience and more robust error reporting. The solution includes checking for `req.body`'s existence and handling errors using `try...catch` for `JSON.parse()` in custom middleware if you decide to handle JSON parsing manually.