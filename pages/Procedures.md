---
alias: subroutines, procedure
---

- Procedures are reusable sections of code that we can call from some location, execute that procedure, and then **return to where we left off**. Although the address to jump to when calling a procedure is **always** the same, the location where a procedure _returns_ will vary.
- To implement procedures in assembly we need to be able to:
  collapsed:: true
	- Jump to the procedure code, leaving a "return link" to know where to return
	- Find the return address and go back to that location
	- ((615ef242-b422-49f8-ade9-19f945f6ff7c))
- The [[system stack]] will be a place where we can store
	- Return addresses another saved register values
	- Local variables of a function
	- Arguments for procedures
- {{embed [[system stack]]}}
-