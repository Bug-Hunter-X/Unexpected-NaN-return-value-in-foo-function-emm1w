# Unexpected NaN return value in foo function

This repository contains a JavaScript code example demonstrating an unexpected behavior of a function when an undefined value is passed as an argument.

The `foo` function is expected to return 0 when a null value is provided. However, it returns `NaN` when an `undefined` value is passed.

## Bug Report
The unexpected behavior lies in the comparison `x == null`. In JavaScript, `null` and `undefined` are loosely equal (`==`), but they are not strictly equal (`===`). The function should handle undefined values correctly.

## Solution
The solution involves using strict equality (`===`) or explicitly checking for both `null` and `undefined`. The provided `bugSolution.js` demonstrates a corrected version of the function that addresses this issue.