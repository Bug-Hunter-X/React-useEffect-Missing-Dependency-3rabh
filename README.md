# React useEffect Missing Dependency Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook: missing dependencies in the dependency array.  The bug results in unexpected re-renders and potential performance issues.

## Bug Description

The `useEffect` hook is used to perform side effects after a component renders. However, if a dependency is omitted from the dependency array, the effect will not be correctly triggered when that dependency changes.

In this case, the effect logs the count to the console. However, the initial render does not include `count` in the dependency array, leading to the effect only running once, and any subsequent changes to the count are not reflected in the console log.

## Solution

The correct solution involves adding `count` to the dependency array of the `useEffect` hook. This ensures the effect runs whenever the value of `count` changes.
