# Express.js Route Handler Missing Error Handling

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling for invalid input.  The example shows a route that fetches a user by ID.  If the ID is not a valid integer, the code will fail without providing a user-friendly error message.

## Bug

The `bug.js` file contains the buggy code.  It attempts to parse the user ID as an integer without checking for potential errors (e.g., non-numeric input).  This can lead to unexpected behavior or application crashes.

## Solution

The `bugSolution.js` file shows the corrected code.  It includes robust error handling to check if the ID is a valid integer and gracefully handles the case where a user with the given ID is not found.  The solution provides clear and informative error messages to the client.

## How to Reproduce

1. Clone the repository.
2. Run `npm install` to install the required dependencies.
3. Run `node bug.js` and try accessing the `/users/abc` endpoint. You'll see the application crashing or returning an unexpected error.
4. Run `node bugSolution.js` and try accessing the same endpoint. You'll get a proper 404 error message indicating that the user was not found.