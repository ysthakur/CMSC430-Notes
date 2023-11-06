---
tags:
  - functions
lang: iniquity
---

**Caller:** Code calling a function (outside the function)
**Callee:** Code being called (inside the function)

Caller is responsible for:
- Telling the callee where to jump back to when it's done executing the function
	- Caller must push the address of some label `label` onto the stack before calling the function so that the function will jump back to that label when it's done executing.

Callee is responsible for:
- Giving back the result
- Jumping back to where the caller told it to go when it's done
- Callee has to reverse arguments, arguments are evaluated left to right (like Racket)