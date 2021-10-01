-
  > Divide the input into two pieces of equal size; solve the two subproblems on these pieces separately by recursion; and then combine the two results into an overall solution, spending only linear time for the initial division and final recombining.
- B.C.: we stop the recursion and sort the two elements by simply comparing them to each other.
## Finding a Recurrence Relation
	- Supposing that $n$ is even, the algorithm spends $O(n)$ time to divide the input into two pieces of size $n/2$