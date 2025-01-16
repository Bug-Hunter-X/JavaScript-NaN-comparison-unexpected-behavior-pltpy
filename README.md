# JavaScript NaN Comparison Bug

This repository demonstrates a subtle bug in JavaScript related to comparing NaN (Not a Number) using loose comparison.  The `foo` function intends to categorize numbers as 0 (null), -1 (negative), or 1 (positive). However, due to the way NaN behaves with loose comparison, the result for NaN is unexpected.

## Bug Description
The loose comparison (`==`) in JavaScript does not behave as expected when comparing with NaN.  Any comparison with NaN will always result in `false`, even `NaN == NaN`. This leads to the unexpected outcome where NaN is treated as a positive number in this code.

## Solution
The solution involves using strict comparison (`===`) to correctly handle NaN comparisons.

## How to Run
1. Clone the repository.
2. Open `bug.js` and `bugSolution.js` in a JavaScript environment (browser console, Node.js).
3. Run the code in each file to observe the differences in the output.
