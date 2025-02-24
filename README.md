# JavaScript Closure Issue in setTimeout Loop

This example demonstrates a common issue in JavaScript related to closures and the use of `setTimeout` within loops.

The problem is that the value of `i` is not captured correctly by the closures created within each `setTimeout` call.  By the time the `setTimeout` functions finally execute, the loop has already completed, and `i` will hold its final value (10).  Therefore, instead of logging 0 through 9, all the console logs will print 10.

**bug.js** contains the buggy code. **bugSolution.js** presents a corrected version.

This is a classic example of how closures work in JavaScript and the importance of understanding how variables are scoped and captured within them.