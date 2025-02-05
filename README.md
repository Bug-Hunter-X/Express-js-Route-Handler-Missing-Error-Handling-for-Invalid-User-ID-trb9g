# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  Specifically, the example shows a route that fetches a user by ID. If the ID is not a valid number, the code will throw an error.

The `bug.js` file contains the buggy code, while `bugSolution.js` provides the corrected version with robust error handling.

## Bug

The primary issue is the lack of input validation. The code directly attempts to parse the `userId` as an integer using `parseInt()` without checking whether the parameter is actually a number or can be parsed into an integer.  If a non-numeric string is passed as the `userId`, `parseInt()` will return `NaN`, causing subsequent operations to fail or leading to unexpected results.

## Solution

The solution involves adding input validation to check if `userId` is a valid number before attempting to use it.  This prevents errors and enhances the application's resilience.