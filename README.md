# React Router v6 Catch-All Route Conflict

This repository demonstrates a common issue in React Router v6 where a catch-all route (`/*`) interferes with other defined routes.  The `NotFound` component is incorrectly triggered even when a matching route exists.

## Problem

The issue arises when the catch-all route (`/*`) is placed after other more specific routes.  React Router matches the first route that satisfies the path, and in this case, the catch-all route always matches first, regardless of other potentially matching routes.

## Solution

The solution involves carefully ordering routes.  The catch-all route should always be placed last in the `Routes` component.  This ensures that other, more specific routes are evaluated first.