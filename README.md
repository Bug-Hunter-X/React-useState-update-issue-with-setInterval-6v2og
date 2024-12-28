# React useState Update Issue with setInterval

This repository demonstrates a common issue in React applications when using `useState` and `setInterval` together. The problem arises when the callback function within `setInterval` uses a stale closure over the state variable, leading to incorrect updates.

## Bug Description

The component `MyComponent` attempts to increment the `count` state every second. However, due to the closure over the initial value of `count`, the update is not correct. This results in a counter that behaves unpredictably.

## Solution

The solution involves using the functional update form of `setCount`, ensuring that the latest state value is always used in the update logic. 