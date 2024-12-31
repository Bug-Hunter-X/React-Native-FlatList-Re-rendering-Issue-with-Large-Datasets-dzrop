# React Native FlatList Re-rendering Issue

This repository demonstrates a common performance issue in React Native's `FlatList` component when dealing with large datasets.  The problem stems from the incorrect use of the `keyExtractor` prop, leading to unnecessary re-renders and performance degradation.

## Problem

The `FlatList` component re-renders items repeatedly even when the underlying data hasn't changed. This happens when the `keyExtractor` function doesn't return unique keys for each item in the dataset.  This can cause significant performance issues, especially when dealing with hundreds or thousands of items.

## Solution

The solution involves correctly implementing the `keyExtractor` prop to ensure that each item has a unique identifier. This will allow the `FlatList` component to efficiently update only the necessary items and avoid unnecessary re-renders.

## How to reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run the app using your preferred React Native method.
4. Observe the performance issue with the initial implementation in `bug.js`.
5. Compare the performance to the optimized version in `bugSolution.js`.