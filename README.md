# React Router Dom v6 Catch-all Route Bug

This repository demonstrates a subtle bug in React Router Dom v6 related to the catch-all route (`/*`).  The issue arises when the catch-all route is defined after more specific routes.  It appears to always match, even if a more specific route should take precedence. 

## Steps to Reproduce
1. Clone this repository
2. Run `npm install`
3. Run `npm start`
4. Navigate to `/about`. Notice it displays the NotFound component even though a route for `/about` exists.

## Solution
The solution involves reordering the routes in the Routes component, placing the catch-all route at the end. This ensures that more specific routes are evaluated before the catch-all route.