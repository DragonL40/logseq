-
  > In the **weighted interval scheduling** problem, we have $n$ jobs.  Each job $j$ has a start time $s_j$, a finish time $f_j$, and a value $v_j$.  Two jobs are incompatible if their time overlaps.  We want to find the max-valued subset of mutually compatible jobs.
## Recursive Solution
- Suppose we sort jobs by finish time 
  $$ f_1 \le f_2 \le f_3 \dots \le f_n$$
- Let $p(i)$ be last task finishing before $s_i$
- Let $OPT(i)$ be the optimal solution up to and including task $i$
- Either $OPT$ includes $n$ or it doesn't
	- If $n \notin OPT$: $OPT$ is optimal solution for tasks $1, \dots, n-1$
	- If $n \in OPT$:
		- All other tasks in $OPT$ are in $\{1, \dots, p(n)\}$
		- $OPT = OPT' \cup \{n\}$ for some non-overlapping $OPT' \subseteq \{1, \dots, p(n)\}$
		- $OPT'$ must be optimal solution for subproblem $\{1, \dots, p(n)\}$
- Subproblem $i$: Find max value non-overlapping 
  $$S \subseteq \{1, \dots, j\}$$
- $OPT(i) = \max(v_i + OPT(p(i)), OPT(i-1))$
- Proof:
	- Consider subproblem $j$
	- A non-overlapping set $S \subseteq \{1, \dots, j\}$ either includes $j$ or it doesn't
	- Best solution excluding $j$ is the best solution to subproblem $j-1$
	- Solutions that include $j$ are precisely those that choose non-overlapping $S \subseteq \{1, \dots, P(j)\}$ then add $j$
-
  ```cpp
  int WIS(int j)
  	if j < 2 Then return v[j]
  	x = WIS(j-1)
  	y = v[j] + WIS(P(j))
  	return max(x, y)
  ```
- [[Dynamic Programming]] Solution with [[Memoization]]
	-
	  ```
	  int memo-WIS(int j)
	  	If j=0 return 0
	      Else if OPT[j] != null then return OPT[j]
	      Else
	        OPT[j] = max(memo-WIS(j-1), v[j] + memo-WIS(P(j)))
	        return OPT[j]
	      Endif
	  ```
	- Runtime:
		- $O(n \log n)$ for sorting and computing $P$.
		- `memo-WIS`: $O(1)$ per recursive call $\times$ # of recursive calls
		- There are at most $2n$ recursive calls, because each time we recurse, we fill one entry of `OPT`.
		- Total: $O(n\log n) + O(n) = O(n\log n)$
- [[Dynamic Programming]] Solution with iteration
	-
	-
	  ```
	  int dp-WIS(int n)
	    for (int j = 0; j < n; j++) {
	        W[j] = max(W[j-1], v[j] + W[P(j)]);
	    }
	    return W[n-1];
	  ```