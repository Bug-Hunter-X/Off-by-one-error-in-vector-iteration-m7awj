# Off-by-one error in vector iteration

This repository demonstrates a common off-by-one error in C++ when iterating over a `std::vector`.  The code attempts to access an element beyond the valid range of the vector, leading to undefined behavior. The solution shows how to correct this error.

## Bug
The bug lies in the loop condition `i <= vec.size()`.  Vectors are 0-indexed, so the last valid index is `vec.size() - 1`. Accessing `vec[vec.size()]` results in undefined behavior, potentially crashing the program or producing incorrect results.

## Solution
The solution modifies the loop condition to `i < vec.size()`, ensuring that the loop iterates only up to the last valid index.