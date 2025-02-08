# Silent Firestore Write Failure

This repository demonstrates a common issue in Firebase projects where Firestore data writes appear successful on the client-side but fail silently on the server.  The root cause is improper handling of asynchronous operations.

## Problem

The `bug.js` file contains code that attempts to write data to Firestore. While the client-side code might indicate success, the data is not actually written to the database.  This is due to the asynchronous nature of Firebase operations and improper error handling.

## Solution

The `bugSolution.js` file presents the corrected code, addressing the asynchronous nature of the operation and implementing proper error handling.  It waits for the write operation to complete before proceeding.

## Reproduction

1. Clone this repository.
2. Install dependencies: `npm install firebase`
3. Configure your Firebase project.
4. Run `bug.js` to reproduce the error.
5. Run `bugSolution.js` to see the corrected implementation.