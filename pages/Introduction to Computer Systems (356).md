- How to convert **unsigned** binary number to and from decimal?
- How to convert [[2's complement]] binary number to and from decimal
- How many **combinations** can be made with $n$ bits?
- What are the **range** of C types?
- How to convert bit sequences to and from **hexadecimal**?
-
## [[2's Complement]] System
- How does 2's Complement System represent numbers?
	- Normal binary place values except MSB has negative weight
- How to extend [[2's complement]]? (Sign Extension)
	- For positive numbers, add leading zeros
	- For negative numbers, add leading ones
- How to truncate [[2's complement]]? (Sign Truncation)
  collapsed:: true
	- Remove copies of sign bit
	-
	  $$[00]011010 = 011010 \\ 11110011 = 10011$$
- How to take the [[2's Complement]] of a number?
- How to add in [[2's complement]] ?
- How to subtract in [[2's complement]]?
- How to detect overflow?
	- If **positive + positive = negative** or **negative + negative = positive**
- What is the difference between [[logical shift]] and [[arithmetic shift]]?
- How to multiply/divide by power of 2?
	- Left shift = multiply by power of 2
	- Right shift = divide by power of 2
- What if I need to multiply a number by a non-power of 2?
	- $17x = 16x + 1x$
- When does dividing by $2^k$ with `x >> k` works and doesn't work?
	- Works if $x \ge 0$ OR ($x <0$ AND $x$ is a multiple of $2^k$)
	- Doesn't work if $x < 0$ AND $x$ is NOT a multiple of $2^k$
- How to compensate for the extra 0.5 when rounding a negative number in the [[2's complement]] system? (Biasing)
	- Add $2^k-1$, the sequence of $k$ ones, to $x$ before shifting.
# Unit 3: Floating Point
- ![CS356Unit03_FP.pdf](../assets/CS356Unit03_FP_1631175822688_0.pdf)
- Why use floating point value?
	- It can be used to represent very small numbers and very large numbers.
- How does floating point numbers represent more range than int with the same amount of bits (32/64)?
	- It uses a digit to represent the exponent
	- We subtract a bias number of 4 from the exponent to convert the range of $[0,9]$ to $[-4, 5]$
- What is a fixed point number?
	- the position of the decimal point is fixed (presumed)
	- Unsigned and [[2's complement]] fall under this category
- Perils of Floating Point: What is the result of $123450 + 0.10000$?
- Trade-off of floating point value:
	- Many fraction digits limit the range
	- Few fraction digits increase the representation error
- How is floating-point number normalized?
- What does the Excess-N exponent representation mean?
- Why put the exponent field before the fraction?
	- We should look at the exponent first to compare FP values; only look at the fraction if the exponents are equal
	- By placing the exponent field first we can compare entire FP values as single bit strings (i.e., as if they were unsigned numbers)
- ((6139cb9b-f361-4306-be11-b80e79b34ec7))
-
  > Visualization tool: http://evanw.github.io/float-toy/
- Single-Precision Example #numlist
	- `1 | 1000 0010 | 110 0110 0000 0000 0000 0000`
	- `+0.6875 = +0.1011`
-
  > For the purpose of this class, we will use ((6139cfd8-1b14-4500-8267-ccab23163649))
- #Example #numlist
	- `1 | 10100 | 101101`
	- `+21.75 = +10101.11`
	- `1 | 01101 | 100000`
	- `+3.625 = +11.101`
## ((6139d454-8a31-425d-9c5d-8dba2b2ed88f))
- What are the methods of rounding?
  collapsed:: true
	- [[Round to Nearest]]
	- [[Round towards 0 (Chopping)]]
	- ((6139d546-3c42-4d8e-9a5d-0e63110b86c7))
	- ((6139d554-df27-471f-8156-d1bcdc2898db))
-
  > ((6139d5e7-baa4-416b-bc67-b299e0140249))
- #[[Round to Nearest]] What does "exactly" half-way correspond to in binary?
  collapsed:: true
	- Hardware will keep some additional bits beyond what can be stored to help with rounding. (GRS)
	- ((6139d70e-db9a-4873-ae85-a68458f451bd))
- #Example Run to Nearest, Base 2,  (the last three bits are GRS): #numlist
  collapsed:: true
	- $1.001100110 \times 2^4$
	- $1.111111101 \times 2^4$
	- $1.001101001 \times 2^4$
	- $1.001100100 \times 2^4$
	- $1.111111100 \times 2^4$
	- $1.001101100 \times 2^4$
- How to implement the Guard, Round, and Sticky bit (GRS)?
  collapsed:: true
	- **Guard bits**: bits immediately after LSB of fraction (many HW implementations keep up to 16 additional guard bits)
	- **Round bit**: bit to the right of the guard bits
	- **Sticky bit**: Logical OR of all other bits after Guard & R bits
	- ((6139da49-8156-4abb-a711-c0de3281f813))
## Major Implications for Programmers
- ((6139da92-5ec9-4877-862a-7fef27fd0ee2))
  collapsed:: true
	-
	  > Add similar, small magnitude numbers first
- FP MUL/DIV is...
  collapsed:: true
	- also not associative
	- Doesn't distribute over addition ($a \times (b + c) \ne a \times b + a \times c$)
# Unit 4: x86 Instruction Set
- ![CS356Unit04_x86_ISA.pdf](../assets/CS356Unit04_x86_ISA_1631297676910_0.pdf)
- Compling and Disassembling
	- From C to assembly code: `gcc -0g -c -s file1.c`
	- Looking at binary files: `gcc -0g -c file1.c`, `hexdump -C file1.o`
	- From binary to assembly: `gcc -0g -c file1.c`, `objdump -d file1.o`
- How to refer to a chuck of memory?
	- The starting address + the size (B, W, L, Q)
- What are the rules for valid starting addresses?
	- A valid starting address should be a multiple of the data size
- What is endian-ness?
	- refers to the two alternate methods of ordering the [[byte]] in a larger unit
	- [[Big-Endian]]
		- PPC, Sparc, TCP/IP
	- [[Little-Endian]]
		- used by Intel processors / original PCI bus
	- **Some processors and busses can be configured for either big- or little-endian**
- What is the issue when transferring data between different systems? #Big-Endian #Little-Endian
	- ((614d6c5e-cff7-4259-8257-58b96c9aee4e))
- {{embed [[x86-64 Data Sizes]]}}
- x86-64 Register Names
  collapsed:: true
	- ((614d72b1-6cab-4451-8b04-1d579eb033c5))
- x86-64 Instruction Classes
	- **Data Transfer**
		- `movq %rax,%rbx` means _"move rax into rbx"_ akin to _"rbx = rax"_
		- Moves data **between registers**, or between **registers and memory** (one operand must be a processor register).
		- Specifices **size via a suffix** on the instruction (`movb,movw,movl,movq`)
	- **ALU Operations**
		- `addq %rax,%rbx` means _"add rax to rbx"_ akin to _"rbx += rax"_
		- One operand must be a processor register or a constant
		- Size and operation specified by instruction (`add1,orq,andb,subw`)
	- **Control / Program Flow**
		- `cmp %rax,%rbx` followed by `jl L1` means _"jump to lab L if rbx < rax"_
		- Unconditional (`jmp L1`)
		- Conditional Branch (`cmpq/test x,y` followed by `he,hne,jl,jge L1`)
		- Subroutine Calls (`call procedure, ret`)
-
- **Source** operands must be in one of the following 3 locations:
	- a register value (e.g. `%rax`) `addq %rax, ...`
	- a value in a memory location (e,g, value at address `0x0200e8`) `addq 0x0200e8, ...`
	- A constant stored in the instruction iteself (known as "immediate value")
	  `addq $1, ...`
	  `addq $0x0200e8, ...`
	  (`$` indicates the constant/immediate)
- **Destination** operands must be
	- A register: `addq ...,%rax`
	- A memory location: `addq ...,  0x0200e8`
	  (specified by its address `0x0200e8`)
- ## Data Transfer Instructions `mov` Instruction
	- **Moves data between memory and processor register**
	- Always provide the **LS-Byte address (little-endian)** of the desired data
	- Size is explicitly defined by the instruction suffix ('mov[bwlq]') used
	- ((614d7e19-03fb-4d7f-8c85-7deee7f11cd7))
	- `movl` zeros the upper bits
	  background-color:: #978626
	- `move[b,w,l,q] src, dst`
	- ### Variations on the `mov` instruction: Zero / Sign Extension
		- `movzxy` will zero-extend the upper portion (up to size `y`)
			- `movzbw` (move a byte from the source but zero-extend it to a word in the destination register)
			- `movzbw, movzbl, movzbq, movzwl, movzwq` (but no `movzlq`!)
		- `movsxy` will sign-extend the upper portion (up to size `y`)
			- `movsbw` (move a byte from the source but sign-extend it to a word in the destination register)
			- `movsbw, movsbl, movsbq, movswl, movswq, movslq`
- ## Addressing Modes
	- What is Addressing Modes?
		- Ways to specify operand locations
	- Different ways to specify source values and output location:
		- **Immediate**: `$imm` to use a constant input value
		- **Register**: `%reg` to use the value contained in a register
		- **Memory reference**
			- **Absolute**: `addr`, use a fixed address
			- **Indirect**: `(%reg)`, use address contained in a **q register**
			- **Base+displacement**: `imm(%reg)`, add a displacement
			- **Indexed**: `(%reg1, %reg2)`, add another register
			- **Indexed+displacement**: `imm(%reg1,%reg2)` add both
			- **Scaled indexed**: `imm(%reg1,%reg2,c)` use address: `imm+reg1+reg2*c`
			  Restriction: $c$ must be one of 1, 2, 4, 8
			  Variants: omit `imm` or `reg1` or `both`.
	- Limits on Addressing Modes:
		- **Not allowed:** memory locations for both operands
			- To avoid `mem->mem` use two move instructions with a register as the intermediate storage location
- ## Arithmetic Instruction
	- ((61511e11-30f5-432d-a412-807cd41319a9))
	- What is the format of ALU Instructions?
		- Restriction: Both operands cannot be memory
		- Format: `add[b,w,l,q] src2, src1/dst`
	- The `lea` Instruction
		- `lea` = Load Effective Address
		- `leaq 80(%rdx,%rcx,2),%rax`
		- Computes the address and just puts it in the destination for later
## Multiplication and Division
	- Since the product of a multiplication may result in twice as many bits as the input operands, the x86 architecture splits the output across two registers (`%rdx` and `%rax`)
	- **Format**: `mul[l,q] src` (Unsigned multiply)
	  `imul[l,q] src` (Signed multiply)
	- **Operation**: Long `%edx:%eax = %eax * src` (`mull`)
	  Quad `%rdx:%rax = %rax * src` (`mulq`)
		- Implicit 2nd operand is `%eax` or `%rax`
		- Results is split across `%edx:%eax` (or `%rdx:%rax`)
			- MSBs (Upper half) are saved to `%edx` (or `%rdx`)
			- LSBs (Lower half) are saved in `%eax` (or `%rax`)
	- For the same reason, the output of division is split across two registers
	- **Format**: `div[l,q] src` (Unsigned divide)
	  `idiv[l,q] src` (Signed divide)
	- **Operation**: `%eax = %edx:%eax / src` (`divl`)
	  `%edx = %edx:%eax % src`
	  `%rax = %rdx:%rax / src` (`divq`)
	  `%rdx = %rdx:%rax % src`
		- **Implicit dividend** is in `%edx:%eax` (or `%rdx:%rax`)
		- **Divisor** is specified as src 32-bit (or 64 bits)
		- **Quotient** goes in `%eax` (%rax), remainder in `%edx` (`%rdx`)
- ![CS356Unit05_x86_Control.pdf](../assets/CS356Unit05_x86_Control_1632720904597_0.pdf)
- Arguments and Return Values
	- ((615159aa-9ff9-4e02-901e-1bbb5ac091c2))
## Jump/Branching Overview
	- Assembly is executed in sequential order by default
	- Jump instruction (aka "branches") cause execution to skip ahead or back to some other location
	- Jumps are used to implement control structures like if statements & loops
	- ### Conditional and Unconditional Jumps
	  collapsed:: true
		- **Conditional**
			- Jump only if a condition is true, otherwise continue sequentially
			- x86 instructions: `je, jne, jge, ...`
		- **Unconditional**
			- Always jump to a new location
			- x86 instruction: `jmp label`
	- Condition Codes (Flags)
		- The FLAGS register in the process
		- **SF** = Sign Flag
		- **ZF** = Zero Flag
		- **OF** = 2's complement Overflow Flag
		- **CF** = Carry Flag (Unsigned Overflow)
	- `cmp` [bwql] src1, src2
		- Performs (`src2 - src1`) and sets the condition codes based on the result
		- `src1` and `src2` are not changed
	- `test[bwql] src1, src2`
		- Performs (`src1 & src2`) and sets condition codes
		- `src1` and `src2` are not changed, OF and CF always set to 0
		- Often used with the `src1 = src2` to check if a value is 0 or negative (through ZF and SF)
	- `mov` and `lea` instructions leave the condition codes unaffected
	- Logical instructions such as `and`, `or`, `xor`
		- update only `SF` and `ZF` based on the result and clear `CF` and `OF` to 0.
		- `not` does not affect the condition codes in any way.
	- All shift instructions
		- Set `SF` (copy of MSB) and `ZF` (true if result is 0)
		- `CF` is always set with the last bit shifted out of the input
		- `OF = undef` for shifts of more than 1 bit; shifts by 1-bit work as follows..
		- **Left shifts (Logical or Arithmetic) by 1-bit**
			- `OF = 1` if MSB (sign bit) changed; 0 otherwise
		- **Right shifts by 1-bit**
			- **Logical**: `OF` is set with the ORIGINAL MSB of the input value
			- **Arithmetic**: `OF` is always set to 0
	- ### Conditional Jump Instructions
	  id:: 61515e50-4294-45fa-98d2-8fe2e8ce7b0b
	  collapsed:: true
		- ((61515fae-c12d-4af3-bddf-96407d40c744))
		  id:: 61515fa0-352a-4f97-a6ef-e1c9f794a403
	- Branch Displacements ((615ee5fc-2b09-4e77-9da8-8d00e7e20735))
	  collapsed:: true
		- Jumps perform `PC = PC + displacement`
		- Assembler converts jumps and labels to appropriate displacements
		- Displacements are in the 2nd byte of the instruction
		- `PC` increments to point at next instruction while jump is fetched and **BEFORE** the jump is executed
		- ((615ee643-39c4-4366-99bb-22faa69f2ea9))
## Conditional Moves
	-