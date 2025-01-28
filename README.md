# React Router v6 Nested Route Issue

This repository demonstrates a bug encountered when using nested routes with a wildcard path (*) in React Router v6.  The issue results in unexpected rendering behavior when navigating to nested routes under the wildcard path.

## Steps to Reproduce

1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Navigate to `/contact` - works fine.
5. Navigate to `/contact/something` - Fails to render the expected component, only shows a blank screen.

## Expected Behavior

Navigating to `/contact` or any nested path under `/contact` should render the appropriate components.

## Actual Behavior

Navigating to a nested path under `/contact` (e.g., `/contact/something`) fails to render the Contact component or any nested component.

## Solution

The solution involves removing the wildcard (*) from the path definition in `App.js` and handling nested routes differently.  Details can be found in `bugSolution.js`.