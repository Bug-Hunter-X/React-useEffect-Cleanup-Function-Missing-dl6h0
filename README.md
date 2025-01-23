# React useEffect Cleanup Function Missing

This repository demonstrates a common React bug involving missing cleanup functions in `useEffect` hooks.  The bug involves adding an event listener without removing it when the component unmounts, leading to memory leaks.  This example showcases the issue and provides a corrected solution.

## Bug Description

The `MyComponent` component adds an event listener in its `useEffect` hook without including a return statement to remove the listener when the component is unmounted. This causes the listener to remain active even after the component is no longer needed, potentially leading to memory leaks and unexpected behavior.

## Solution

The corrected version utilizes a cleanup function returned by `useEffect` to remove the event listener before the component unmounts, thus preventing the memory leak.