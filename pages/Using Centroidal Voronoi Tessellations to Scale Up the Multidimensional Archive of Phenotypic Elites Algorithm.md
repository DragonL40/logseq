alias:: CVT-MAP-Elites
source:: https://ieeexplore.ieee.org/document/8000667

- > Map Elites has the "curse of dimensionality"
-
- ## Main Contributions
	- introduce a new algorithm called [[CVT-MAP-Elites]] and demonstrate its advantage over [[MAP-Elites]] in a maze navigation task and the simulated hexapod locomotion task
	- propose a new methodology for assessing the quality of the archives produced by [[illumination algorithms]]
- ## Key Concepts
	- [[Centroidal Voronoi Tessellations]]
		- A [[Voronoi Tessellation]] is a partitioning of a space into geometric regions based on distance to $k$ prespecified points which are often called _sites_. Each region contains all the points that are closer to the corresponding site than to any other.
		- If the sites are also the centroids of each region (and the space is bounded), then the [[Voronoi Tessellation]] is the [[Centroidal Voronoi Tessellations]] of the space.
		- [[Lloyd's algorithm]] can be used in 2-D space.
		- For higher dimensional space, [[Monte Carlo method]] can be used to obtain a close approximation to a [[Centroidal Voronoi Tessellations]].
- ## Difference from [[MAP-Elites]]
	- [[MAP-Elites]] creates an empty archive based on the desired discretizations per dimension $[n_1, \dots, n_d]$, whereas [[CVT-MAP-Elites]] first performs the [[CVT]] construction and then creates the empty archive of $k$ niches.
	- Note that [[CVT-MAP-Elites]] requires a distance function to calculate the index $c$ of a descriptor $b$, which could take $O(\log k)$ on average.
- ## Evaluation
	- How many solution can $P_i$ find for a test problm?
	- We can use a CDF for a minimization problem
	  $$
	  F_X \sim P_i(x) = P(X \le x)
	  $$
	- Or a CCDF for a maximization problem
	  $$
	  F_X \sim P_i(x) = P(X > x)
	  $$
	-
	-