- #[[University of Southern California (USC)]] #[[B.S. Computer Science]]
- [[Pigeon Hole Principle]]
  collapsed:: true
	- If $f: X \to Y$ and $|X| > |Y|$, then there are elements $x_1, x_2 \in X$ such that $x_1 \ne x_2$ and $f(x_1) = f(x_2)$.
- Extended [[Pigeon Hole Principle]]
  collapsed:: true
	- For any sets $X$, $Y$, and positive integer $k$ such that $|X| > k \cdot |Y|$, if $f: X \to Y$ then there are at least $k+1$ distinct members $x_1, \dots, x_{k+1} \in X$ such that $f(x_1) = \dots = f(x_{k+1})$
- [[Fundamental Theorem of Arithmetic]]
  collapsed:: true
	- There are exactly one way to express an integer $>1$ as a product of distinct prime numbers in increasing order, with positive integer exponents.
# [[Proof]]
	- A **proof** is an argument that is both correct and accepted by your peers.
	- Proving and disproving a claim:
	  collapsed:: true
		- To _prove_ a **general statement** (a for-all statement), you have to supply a general proof.
		- To _disprove_ a general statement, all you need to provide is a counter-example (there exists...).
		- To _prove_ a **specific statement** (such as "$\exists$ an even prime"), all you need is to provide an example.
		- To _disprove_ a **specific statement**, you need to supply a general proof that no such value exists (such as "$\forall$ values, the specific statement doesn't hold").
	- [[Proof by Contraposition]]
	  collapsed:: true
		- Only works on "if...then" statements.
		- Proving "if $x$ then $y$" is equivalent to proving "if not $y$ then not $x$"
		- (The second version is called the [[Contrapositive]] of the first statement)
		- _If the "then" statement is simpler than the "if" statement, it might be worth it to use contraposition._
	- Prove: $\forall$ integers $n$, $n$ is odd if and only if $n^2$ is odd.
	- [[Proof by Contradiction]]
		- When using this method, assume the [[Logical Opposites]] of what you're trying to prove.
		- Then, you derive a logical impossibility (such as $X$ is both true and false simultaneously)
		- This means that your assumption was incorrect, so the [[Logical Opposites]] of your assumption must be correct!
		- **It proceeds very similarly to proof by contraposition, but can be used even if the original statement is not an if-then statement.**
	- Prove: $\forall$ integers $n$, if $3n+2$ is odd, then $n$ is odd.
	- Prove: $\sqrt{2}$ is irrational
# [[Induction]]
	- How to prove by [[Induction]]?
		- Clearly express the statement to be proven
		- Clearly label and prove the base case
		- Clearly state the inductive hypothesis
		- Identify the $(k+1)$st step, $P_{k+1}$.
		- Break $P_{k+1}$ into several pieces, at least one of which the I.H. can apply to.
		- Apply the inductive hypothesis
	- Prove: $\sum^n_{i=0} 2^i = 2^{n+1}-1$
	- Prove: Odd Pie Fight
	  collapsed:: true
		- There are an odd number of people $n\ge 3$ engaged in a pie fight.
		- Each person has one pie.
		- Every pair of people are at a unique distance.
		- Everyone throws their pie at the closest person.
		- **Prove there is someone who doesn't get hit by a pie.**
	- Prove: Any $2^n \times 2^n$ chess board with one squared removed can be tiled by 3-square L-shape pieces, $\forall n \ge 1$
	- What is the difference between strong [[Induction]] and (weak) [[Induction]]?
	  collapsed:: true
		- Instead of only assuming that the previous domino fell over, we will assume that all of the dominos prior to the current on fell over.
		- This is just as valid, because the reason why the $k$th domino fell over is because the $(k+1)$st domino fell over, which fell over because the $(k+2)$nd domino fell over.
		- So, if the $k$th domino fell over, we know it is because all of the dominos before it fell over as well.
		- By assuming this, we have more information available with which to prove that the $(k+1)$st domino will fall over.
	- Prove: All integers $\ge 2$ can be represented as a product of primes.
-