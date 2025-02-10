# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  Specifically, the provided code attempts to parse a user ID from the request parameters, but it doesn't handle the case where the ID is not a valid number, potentially resulting in an unexpected error.

## Bug Description
The `bug.js` file contains an Express.js route handler that fetches a user by ID.  However, it lacks error handling for scenarios where the provided ID is not a number or does not correspond to an existing user.  This can lead to an application crash or unexpected behavior.

## Solution
The `bugSolution.js` file demonstrates the correct way to handle such situations. It includes error handling to check if the user ID is a number and to gracefully handle cases where the user is not found, returning appropriate HTTP status codes and messages.