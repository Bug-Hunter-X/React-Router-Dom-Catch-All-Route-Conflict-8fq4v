# React Router Dom Catch-All Route Conflict

This repository demonstrates a common issue in React Router v6 where a catch-all route (`/*`) conflicts with other defined routes.  The `/*` route, intended to handle any unmatched paths, can sometimes interfere with routing if it's not placed correctly within the `Routes` component.

**Problem:**  The catch-all route, when not positioned last, can prematurely capture all paths, preventing other routes from being matched. This typically leads to the catch-all route being rendered even when a specific route should have been matched.

**Solution:**  Ensure that the catch-all route (`/*`) is placed as the last route in the `Routes` definition. This ensures that it only matches paths not handled by other, more specific routes.