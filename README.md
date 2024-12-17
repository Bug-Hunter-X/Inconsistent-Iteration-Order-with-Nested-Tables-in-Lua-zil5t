# Lua Nested Table Iteration Issue

This repository demonstrates a subtle bug related to the iteration order of nested tables in Lua when using the `pairs` iterator.  The `pairs` function does not guarantee any specific order, which can lead to unexpected behavior, especially in recursive functions.

The `bug.lua` file contains code that recursively iterates through a nested table. Due to the unpredictable order of `pairs`, the results might vary between different Lua implementations.

The `bugSolution.lua` file offers a possible solution using a method that ensures a consistent iteration order (e.g. using a sorted table or a different approach).

**Note:** This bug is not necessarily an error in Lua itself, but rather a consequence of the unspecified iteration order of `pairs`. Understanding this behavior is crucial for writing robust and predictable Lua code.