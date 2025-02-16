# Express.js JSON Parsing Issue

This repository demonstrates a common issue in Express.js applications where JSON request bodies are not parsed correctly when the `Content-Type` header is missing or incorrect.  The issue arises because Express.js's `express.json()` middleware requires the `Content-Type: application/json` header to be present in the request to properly parse the body as JSON.

## Problem
The provided `bug.js` file contains an Express.js server that attempts to handle POST requests with JSON data. However, if a request is sent without the correct `Content-Type` header, the `req.body` will be empty, leading to unexpected behavior or errors.

## Solution
The solution, implemented in `bugSolution.js`, addresses this by adding error handling to gracefully manage requests lacking the necessary header.  Alternatively, one could configure the middleware to accept other content types.