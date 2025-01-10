# Lua Pairs Iteration Bug

This repository demonstrates a potential issue when using Lua's `pairs` iterator for recursive table traversal.  The `pairs` iterator doesn't guarantee any specific order of iteration, leading to unpredictable behavior if the table is modified during the iteration.  This is particularly problematic in recursive functions where changes in sub-tables can affect subsequent iterations.

## Reproducing the Bug

The `bug.lua` file contains code that recursively iterates a table using `pairs`.  Observe the output; it might differ from what you'd expect due to the unordered iteration.

## Solution

The `bugSolution.lua` file offers a solution that demonstrates a safer approach to recursive table traversal.  The solution addresses this by using techniques that don't rely on the order of iteration provided by `pairs`. 

## Contributing

Contributions are welcome!