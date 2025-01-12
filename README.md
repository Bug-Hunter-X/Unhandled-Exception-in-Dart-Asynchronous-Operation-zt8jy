# Unhandled Exception in Dart Asynchronous Operation

This repository demonstrates a common error in Dart asynchronous programming: failing to rethrow exceptions caught within an `async` function's `catch` block.  The provided code fetches data from a remote API and handles potential errors.  However, the original code omits rethrowing the exception, resulting in silent failures and difficulty debugging. The solution shows the correct way to handle exceptions.

## Problem
The original `fetchData` function catches exceptions but doesn't rethrow them. This means that if an error occurs during the API call, the error is printed to the console but not propagated up the call stack, making it harder to handle the error gracefully in the calling function.