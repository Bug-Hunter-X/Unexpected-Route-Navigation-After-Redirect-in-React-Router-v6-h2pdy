# Unexpected Route Navigation After Redirect in React Router v6

This repository demonstrates a bug in React Router v6 where redirects unexpectedly navigate to the wrong page.  The redirect ignores the intended route and defaults to the root path ('/') instead.

## Bug Description

After a successful login, the application should redirect to the '/dashboard' route. Instead, the application incorrectly redirects to the '/' (home) route.  The navigation happens *after* a successful authentication action. 

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Attempt to navigate to the protected route without authentication - this triggers the redirect.
5. Observe the unexpected redirection.

## Solution

The solution involves updating the redirect logic to ensure that the correct route is targeted after the successful authentication. 
