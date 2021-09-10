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
	- $1.001100110 \times 2^4$
	- $1.111111101 \times 2^4$
	- $1.001101001 \times 2^4$
	- $1.001100100 \times 2^4$
	- $1.111111100 \times 2^4$
	- $1.001101100 \times 2^4$
- How to implement the Guard, Round, and Sticky bit (GRS)?
	- **Guard bits**: bits immediately after LSB of fraction (many HW implementations keep up to 16 additional guard bits)
	- **Round bit**: bit to the right of the guard bits
	- **Sticky bit**: Logical OR of all other bits after Guard & R bits
	- ((6139da49-8156-4abb-a711-c0de3281f813))
## Major Implications for Programmers
- ((6139da92-5ec9-4877-862a-7fef27fd0ee2))
	-
	  > Add similar, small magnitude numbers first
- FP MUL/DIV is...
	- also not associative
	- Doesn't distribute over addition ($a \times (b + c) \ne a \times b + a \times c$)
# Unit 4: x86 Instruction Set
- ![CS356Unit04_x86_ISA.pdf](../assets/CS356Unit04_x86_ISA_1631297676910_0.pdf)
- Compling and Disassembling
	- From C to assembly code: `gcc -0g -c -s file1.c`
	- Looking at binary files: `gcc -0g -c file1.c`, `hexdump -C file1.o`