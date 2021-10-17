- Key idea: find the attack instructions inside of those that already exist in the code segment
- Find **gadgets** in executable areas.
	- Gadgets: short sequence of instructions followed by `ret (0xc3)`
-
  > Often, it is possible to find useful instructions within the byte encoding of other instructions.
### Using a chain of gadgets
	- The stack contains a sequence of gadget addresses.
	- Each gadget consists of a series of instruction bytes, with the final one being `0xc3`(encoding the `ret` instruction).
	- When the program executes a `ret` instruction starting with this configuration, it will initiate a chain of gadget executions, with the `ret` instruction at the end of each gadget