filters:: {}

-
  > There will be $n$ requests labeled $1, \dots, n$, with each request $i$ specifying a start time $s_i$ and a finish time $f_i$. Naturally, we have $s_i < f_i$ for all $i$. Two requests $i$ and $j$ are _compatible_ if the requested intervals do not overlap. **The goal is to select a compatible subset of requests of maximum possible size.**
- What is the greedy criteria?
	- Earliest Finish Time
	- "I want to finish every tasks ASAP, so I can leave more time for the later tasks"
- The Algorithm
	- $R =T, A = \phi$
	- While $R \ne \phi$
		- $i = \text{argmin} f(j): j \in R$
		- $A = A \cup \{i\}$
		- Remove from $R$ all tasks overlapping $i$.
	- EndWhile
	- Return $A$
- How to prove optimality?
  collapsed:: true
	- $A$ is the solution output by our algorithm
	- $O$ is the optimal solution
	- Denote $k = |A|, m = |O|$, obviously $k \le m$
	- We will show that $k = m$ (our solution is **an** optimal solution)
- Proof: Greedy Stays Ahead
  collapsed:: true
	- Let $A = \{i_1, \dots, i_k\}$ in order by finish time
	- Let $O = \{j_1, \dots. j_m\}$ in order by finish time.
	-
	  > $i_t$ is task added in iteration $t$
	- Lemma (Greedy stays ahead): $f(i_t) \le f(j_t), \forall t = 1, \dots, k$
	- B.C.: $t=1$
	- I.H.: Assume true for $t$
	- I.S.: Prove for $t+1$
		- $S(j_{t+1}) \ge f(j_t) \ge^{IH} f(i_t)$
		- $j_{t+1} \in R$ at iteration $t+1$
		- Since $i_{t+1}$ is earliest finishing tasks in $R$ during iteration $t+1$
		-
		  $$f(i_{t + 1}) \le f(j_{t+1})$$
- Proof: _The greedy algorithm returns an optimal set $A$_
	-