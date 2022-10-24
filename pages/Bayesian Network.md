- Bayesian networks can represent essentially any full joint probability distribution and in many cases can do so very concisely.
- A Bayesian network is a directed graph in which each node is annotated with quantitative probability information. The full specification is as follows:
	- 1. Each node corresponds to a random variable, which may be discrete or continuous.
	  2. Directed edges connect pairs of nodes. The graph has no directed cycles and hence is a [[Directed Acyclic Graph (DAG)]]
	  3. Each node $X_i$