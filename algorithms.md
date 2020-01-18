---
header: Algorithms
description: How to make things work.
---

# Sorting

## Insertion Sort

Sorts the numbers in a non-descending order (lowest to highest).

Efficient for small amount of numbers.

For each entry of the array, place the key in the correct position by starting at the current key and looping backwards. While looping backwards, compare the current position with the previous position, and if `current > previous`, then swap. Continue until the condition `current < previous`; this means it is in the correct position.
