# Unexpected toString() Behavior with NaN in JavaScript

This repository demonstrates a subtle bug in JavaScript related to the `toString()` method and the `NaN` value. The provided code intends to convert various input types to strings; however, it behaves unexpectedly when encountering `NaN`.

## Bug Description
The code's primary function, `foo()`, aims to handle `null`, `undefined`, and other data types by converting them into string representations. While it correctly handles `null`, `undefined`, numbers, and objects, the behavior with `NaN` is not as expected.  `NaN`'s `toString()` method returns "NaN", but this isn't always consistent with how one might expect it to behave within this specific context.

## Solution
The solution involves using a more robust approach to handling `NaN` explicitly. Instead of relying solely on `toString()`, it checks for `isNaN()` to provide a consistent and predictable string representation for all cases.

## How to Reproduce
1. Clone this repository.
2. Open `bug.js` and run the JavaScript code.
3. Observe the unexpected output for `NaN`.
4. Then run `bugSolution.js` to see the corrected behavior.