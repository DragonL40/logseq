- Notice that to call our exploit code we have to know the exact address on the stack where out exploit code starts and make that our return address
- The stack usually starts at the same address when each program runs so it might be fairly easy to predict
- Idea: Randomize where the stack will start
### How does the OS randomizes the layout?
	- The OS can allocate a random amount of space on the stack each time a program is executed to make it harder for an attacker to succeed in an exploit
- [[nop sleds]]
-