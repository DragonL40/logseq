- Bayesian networks can represent essentially any full joint probability distribution and in many cases can do so very concisely.
- A Bayesian network is a directed graph in which each node is annotated with quantitative probability information. The full specification is as follows:
	- 1. Each node corresponds to a random variable, which may be discrete or continuous.
	  2. Directed edges connect pairs of nodes. The graph has no directed cycles and hence is a [[Directed Acyclic Graph (DAG)]]
	  3. Each node $X_i$ has associated probability information $\theta(X_i | \mathrm{Parents}(X_i))$ that quantifies the effect of the parents on the node using a finite number of **parameters**.
- A conditional probability table for a node with $k$ parents contains $2^k$ independently specifiable probabilities.
- Assume that the Bayes net contains $n$ variables, $X_1, \dots, X_n$. A generic entry in the joint distribution is then $P(x_1, \dots, x_n)$. The semantics of Bayes net defines each entry in the joint distribution as follows:
  $$
  P(x_1, \dots, x_n) = \prod_{i=1}^n \theta(x_i | \mathrm{Parents}(X_i))
  $$
-