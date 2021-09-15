- What is the [[Cut Property]]? #card
-
- The Algorithm
  collapsed:: true
	- $T = \phi$
	- $S = \{s\}$ for arbitrary $s \in V$
	- While $S \ne V$
		- Let $e = <u,v>$ be the min cost edge with $u \in S$ and $v \notin S$
		- Add $e$ to $T$
		- Add $v$ to $S$
- #[[Proof by Induction]] _Prim's Algorithm produces a [[Minimum Spanning Tree (MST)]] of G_
  collapsed:: true
	- I.H.: After iteration $i$, $|S| = i+1$ and $(S,T)$ is a tree.
	- B.C.: True for $i = 0$
	- I.S.: In each iteration, we add one node $v$ to $S$, plus $e$ from $T$ to $v$
		- After $n-1$ iterations, $|S| = n \implies S = V$
		- $(V,T)$ is a tree
		- Therefore, $T$ is a [[Spanning Tree]] of $G$.