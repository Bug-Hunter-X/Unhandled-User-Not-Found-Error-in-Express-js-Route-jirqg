# Unhandled User Not Found Error in Express.js Route

This repository demonstrates a common error in Express.js route handling: failing to handle cases where a requested resource (e.g., a user) is not found.

The `bug.js` file shows the problematic code.  The `bugSolution.js` file provides a corrected version with proper error handling.

## Problem

The original code directly attempts to access user data based on the ID passed in the route parameters.  If a user with that ID does not exist, this will lead to an error further down the line, potentially crashing the server or causing unexpected behavior.

## Solution

The solution involves adding a check to see if the user exists before attempting to access its data. If the user is not found, a 404 Not Found status code is returned to the client.