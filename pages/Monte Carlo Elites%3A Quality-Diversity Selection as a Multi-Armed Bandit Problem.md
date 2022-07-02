title:: Monte Carlo Elites: Quality-Diversity Selection as a Multi-Armed Bandit Problem
source:: https://arxiv.org/pdf/2104.08781.pdf

## Summary
	- This paper proposes an alternative selection rule to use for [[MAP-Elites]].
	- Parent selection methods rank all elites in the feature map based on a selection score, and choose the individual with the highest score **as the parents** .
		- ( #Questions How is this not just a ranker? )
## Main Contributions
	- Explores how parent selection driven by the UCB formula can affect the performance of [[MAP-Elites]]
## Key Concepts
	- [[Multi-Armed Bandit Problem]]