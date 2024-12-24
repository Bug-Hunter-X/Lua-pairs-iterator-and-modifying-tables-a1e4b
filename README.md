# Lua pairs iterator and table modification

This repository demonstrates an unusual behavior in Lua related to its `pairs` iterator and modifying tables during iteration.  The `pairs` iterator does not iterate over keys added to the table after the iteration has begun.

The `bug.lua` file contains a function that recursively iterates over a table's elements. While it intends to modify the table, the modification is ineffective due to the limitation of the `pairs` iterator.  The `bugSolution.lua` file provides a corrected approach.

## How to reproduce

1.  Clone this repository.
2.  Run `bug.lua` using a Lua interpreter.
3.  Observe the output (or lack thereof).  The table remains unchanged.

## Solution

The `bugSolution.lua` file presents a solution using an iterative approach to handle the nested tables.  This ensures proper iteration and modification of all table elements.