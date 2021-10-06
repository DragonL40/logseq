-
  > In the **weighted interval scheduling** problem, we have $n$ jobs.  Each job $j$ has a start time $s_j$, a finish time $f_j$, and a value $v_j$.  Two jobs are incompatible if their time overlaps.  We want to find the max-valued subset of mutually compatible jobs.
## Recursive Solution
- Suppose we sort jobs by finish time 
  $$ f_1 \le f_2 \le f_3 \dots \le f_n$$
- Let $p(i)$ be last task finishing before $s_i$
-
-
  ```cpp
  int WIS(int i)
  	if i > n Then return 0
  	x = WIS(i+1)
  	y = v[i] + WIS(S)
  	return max(x, y)
  ```