-
  > Divide the input into two pieces of equal size; solve the two subproblems on these pieces separately by recursion; and then combine the two results into an overall solution, spending only linear time for the initial division and final recombining.
- B.C.: we stop the recursion and sort the two elements by simply comparing them to each other.
## Finding a Recurrence Relation
	- Supposing that $n$ is even, the algorithm spends $O(n)$ time to divide the input into two pieces of size $n/2$ each; it then spends time $T(n/2)$ to solve each piece; and finally it spends $O(n)$ to combine the solutions from the two recursive calls.
	- For some constant $c$, 
	  $$T(n) \le 2T(n/2) + cn$$
	   when $n>2$, and 
	  $$T(2) \le c$$
	- How to prove this recurrence relation?
		- Solve-by-tree (unrolling the merge-sort recurrence KT p. 212)
		- Guess the solution and prove with induction (KT p. 213)
	-