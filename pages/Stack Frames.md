---
alias: stack frame
---

- Frame: All data on stack belonging to a procedure / function
	- Space for saved registers
	- Space for local variables (declared in a function)
	- Space for arguments
## Complier Handling of [[Procedures]]
	- When coding in an high level language & using a compiler, certain conventions are followed that may lead to heavier usage of the stack
		- We have to be careful not to **overwrite** registers that have useful data.
	- High level languages (HLL) use the stack:
		- to **save register values** including the return address
		- for storage of **local variables** declared in the precedure
		- to pass **arguments** to a procedure
	- Compilers usually put data on the stack in a certain order, which we call a [[stack frame]]
## Accessing Value on the Stack
	- Stack pointer (`%rsp`) is usually used to access only the top value on the stack
	- To access arguments and local variables, we need to access values buried in the. stack
		- We can simply use an offset from `%rsp` [ e.g. `8(%rsp)`]
-