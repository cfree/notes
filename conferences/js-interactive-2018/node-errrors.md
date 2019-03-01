# Node.js Error Handling Done Right
- Ruben Bridgewater, NearForm @BridgeAR

Node website?

Nested try/catch

Error class - for the company
Any new error is subclass
- Extends: `class ApplicationError extends Error`
- Abstraction: `class DatabaseError extends ApplicationError`, `class UserFacingError extends ApplicationError`
- Error name and error code methods
- Use cases:
- - Validation
- - Move in indivual module
- - Only source of truth
- - Contain all info for users and devs

Each layer handles specific part of app error handling
- DB, express, outgoing requests, etc.

Express: Async must call next instead of throwing error

Application error - anything not created by yourself
Log everything

Databases - can recover/retry, normally transparent to user

Debugging utils
- Mutiple resolves hook - check if resolve called mutiple times or if called in a Promise contructor
- Promise hooks
- Proper logging
- Stack traces

Rules:
- Use error classes specifically set up for the app
- Always use async/await
- Make errors expressive
- Use promisfy if necessary
- Return proper error statuses and codes
- Make use of promise hooks
