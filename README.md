# Closure Issue in setTimeout Loop

This repository demonstrates a common JavaScript closure issue that often arises when using `setTimeout` within a loop. The problem lies in how variables are captured by the closure created within the `setTimeout` callback.

## Bug Description

The JavaScript code in `bug.js` attempts to print the values of `i` from 0 to 9 with a one-second delay between each print. However, due to the closure issue, it ends up printing the final value of `i` (which is 10) ten times instead.

## Solution

The `bugSolution.js` file corrects this issue by using an immediately invoked function expression (IIFE) to create a new scope for the `i` variable for each iteration of the loop. This ensures that each `setTimeout` callback captures its own unique value of `i`.

## How to Run

1. Clone this repository.
2. Open `bug.js` and `bugSolution.js` in your preferred JavaScript environment or browser's developer console.
3. Run the code in `bug.js` and observe the incorrect output.
4. Run the code in `bugSolution.js` and observe the corrected output.