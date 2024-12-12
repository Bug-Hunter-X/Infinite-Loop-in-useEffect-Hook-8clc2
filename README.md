# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug causes an infinite render loop because the dependency array is missing, leading to the effect running after every render.

## Bug Description

The `MyComponent` component uses `useEffect` to log the current count to the console. However, the `useEffect` hook lacks a dependency array, causing it to re-run on every render, triggering another state update, and subsequently another render - creating an infinite loop.

## Solution

The solution involves adding a dependency array to the `useEffect` hook. The dependency array specifies which values the effect should depend on.  If none of these values change between renders, the effect will not run again. In this case, the effect should only run when the `count` state variable changes.
