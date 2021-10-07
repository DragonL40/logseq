- Modern processors execute multiple instructions at one time.
	- While earlier instructions are executing, the processor can be fetching and decoding later instructions.
	- This overlapped execution is known as [[pipelining]] and is key to obtaining good performance.
- Problem: **Conditional jumps limit [[pipelining]]** because when we reach a jump, the comparison results it relies on may not be computed yet
	- It is unclear which instruction to fetch next
	- To be safe we have to stop and wait for the jump condition to be known
- Solution: When modern processors reach a jump before the comparison condition is known, it will predict whether the jump condition will be true (aka [[branch prediction]]) and "speculatively" execute down the chosen path.
- Potential better solution: Be more **[[pipelining]] friendly** and  compute both results and only store the correct result when the condition is known
	- Allows for pure sequential execution
	- With conditional moves, we only need to choose whether to save or discard a computed result
- Example:
  collapsed:: true
	- ((615ee93d-39ef-4d18-8876-35dc957462d0))
-
  ---
## Conditional Move Instruction
	- Similar to `(cond) ? x : y`
	- Syntax: `cmov[cond] src, reg`
		- `cond =` same