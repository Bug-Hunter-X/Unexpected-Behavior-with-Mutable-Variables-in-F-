# F# Mutable Variable Bug

This repository demonstrates an uncommon bug in F# related to the way mutable variables are handled within functions.  In F#, mutable variables are passed by sharing, meaning changes made to the variable inside a function affect the original variable outside the function.

This can lead to unexpected results when you expect pass-by-value semantics.  The example shows how swapping two mutable variables doesn't work as intended due to this behavior.

## Bug Reproduction

1. Clone this repository.
2. Open `bug.fs` in a F# IDE (like Visual Studio or Ionide).
3. Run the code.  Observe that the output is not what you might initially expect.

## Solution

The solution demonstrates how to correctly swap the variables using techniques that avoid the pitfalls of pass-by-sharing for mutable variables.