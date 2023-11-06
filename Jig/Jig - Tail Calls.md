---
tags:
  - functions
  - stack
lang: jig
---
Avoid stack overflows

**TCP:** A predicate to check if an expression is in tail call position

- All function bodies are in tail position
- Both the then and else part of an if statement are in tail position
- In a function call, none of the arguments are in tail position

Use new strategy for compiling only if expression in tail position, otherwise compile normally
