# Unhandled Promise Rejection in Express.js Route Handler

This repository demonstrates a common error in Express.js applications: unhandled promise rejections within route handlers.  Unhandled promise rejections can be difficult to track down, as they may not immediately crash the server but can lead to unpredictable behavior and data corruption.

The `bug.js` file shows the problematic code, and `bugSolution.js` provides a corrected version.

## Problem

The issue lies in the asynchronous operation (`someAsyncOperation`) within the route handler.  If the asynchronous operation fails, the error isn't properly handled, resulting in an unhandled promise rejection.  This can lead to the application silently failing or showing unexpected behavior.

## Solution

The solution involves proper error handling using `.catch()` to gracefully handle any exceptions that might occur during the asynchronous operation.  The improved error handling provides clearer feedback, making debugging easier.