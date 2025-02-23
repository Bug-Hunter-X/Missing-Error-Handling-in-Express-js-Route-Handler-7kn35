# Express.js Route Handler Error Handling Bug

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling when dealing with user input.  Specifically, the `/users/:id` route does not handle cases where the `id` parameter is not a valid number.

## Bug

The `bug.js` file contains the faulty code.  The route attempts to parse the `id` parameter as an integer using `parseInt()`, but it doesn't handle the case where the parameter is not a number.  This can lead to errors and potentially crashes the application. 

## Solution

The `bugSolution.js` file provides a corrected version of the code that includes comprehensive error handling. It checks if the `id` parameter is a number and handles cases where it's not a number or a valid user ID isn't found.