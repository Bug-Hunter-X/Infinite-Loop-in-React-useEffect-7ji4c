# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug arises from an incorrectly defined dependency array, leading to an infinite loop. The solution shows how to properly manage dependencies to resolve this issue.

## Bug Description

The provided code implements a simple counter component.  However, the `useEffect` hook attempts to update the `count` state within its own callback.  Because `count` is included in the dependency array, the effect runs continuously, causing an infinite loop and potentially crashing the browser.

## Solution

The solution corrects the dependency array in the `useEffect` hook.  Removing `count` from the dependency array ensures that the effect only runs after the initial render. The component now functions correctly.