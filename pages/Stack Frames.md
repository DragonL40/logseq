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
## Caller & Callee-Saved Convention
- Having to always play it safe and save a register to the stack before using it can decrease performance
- To increase performance, a standard is set to indicate which registers must be **preserved(callee-saved)** and which ones can be **overwritten freely(caller-saved)**
	- Callee-saved: Push values before overwriting them; restore before returning
	- Caller-saved: Push if the register is needed after the function call; callee can freely overwrite; caller will restore upon return
	- ((6165242f-24b9-4e92-9c62-f3a43d604bac))
-