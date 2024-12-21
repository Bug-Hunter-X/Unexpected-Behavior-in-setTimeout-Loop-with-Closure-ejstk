# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common error in JavaScript involving closures and the `setTimeout` function within a loop. The issue stems from how JavaScript handles variable scoping and closures.

## The Problem

The provided `bug.js` file contains a function `myFunc` that uses a `for` loop and `setTimeout`. The expected behavior is to log the numbers 0 through 9 with a one-second delay between each. However, due to a closure issue, the code logs 10 ten times.

## The Solution

The `bugSolution.js` file corrects this problem by using an immediately invoked function expression (IIFE) to create a new scope for each iteration of the loop. This ensures that each `setTimeout` callback captures its own unique value of `i`.