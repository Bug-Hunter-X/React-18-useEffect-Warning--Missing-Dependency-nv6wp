# React 18 useEffect Warning: Missing Dependency

This repository demonstrates a common warning encountered when upgrading to React 18 related to the `useEffect` hook and its dependency array.  The warning arises because the effect function has an implicit dependency on `count`, which is not included in the dependency array.  This can lead to unexpected behavior and performance issues.

## Problem

The `useEffect` hook in the `bug.js` file logs the current value of `count` every time the component renders. However, the dependency array `[count]` is missing, meaning the effect will run even when the value of `count` doesn't change, which might be unintended.

## Solution

The solution in `bugSolution.js` explicitly includes the `count` in the dependency array.   React 18+ might generate warnings that implicitly depend on `count` if it is not in the dependency array.