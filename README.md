# Unhandled Non-JSON Response in React Fetch

This repository demonstrates a common error in React applications where fetching data fails silently if the server response is not valid JSON.  The `bug.js` file contains the erroneous code, while `bugSolution.js` provides the corrected version.

## Problem

The original code attempts to parse the server response as JSON using `response.json()`.  If the server returns a non-JSON response (e.g., an HTML error page), this will throw an error that is not properly handled, leading to a silent failure or a cryptic error message in the console. 

## Solution

The solution adds a check to ensure the response's content type is JSON before attempting to parse it.  This prevents errors from occurring when the response is not valid JSON.  Additionally, more descriptive error handling provides better user feedback.