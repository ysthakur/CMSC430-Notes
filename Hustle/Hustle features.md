---
tags:
  - hustle
---
Hustle adds `(cons a b)` and `(box v)`, which are both allocated on the heap.

- The C main function now allocates a bunch of memory for the heap and passes the pointer to that to the `entry` function.
- `entry` stores the heap pointer in **`rbx`** (`rbx` holds pointer to next free memory).

Every time you want to allocate more memory from the heap, just add 8 to `rbx`.