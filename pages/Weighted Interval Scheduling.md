-
  > In the **weighted interval scheduling** problem, we have $n$ jobs.  Each job $j$ has a start time $s_j$, a finish time $f_j$, and a value $v_j$.  Two jobs are incompatible if their time overlaps.  We want to find the max-valued subset of mutually compatible jobs.
## Recursive Solution
- max(v_j + rec(j), rec(j-1))
-