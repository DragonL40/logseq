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
	- Solutions that include $j$ are precisely those that choose non
-
  ```cpp
  int WIS(int i)
  	if i > n Then return 0
  	x = WIS(i+1)
  	y = v[i] + WIS(S)
  	return max(x, y)
  ```