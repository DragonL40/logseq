- #MAP-Elites
- [[MAP-Elites]] (1) illuminates the relationship between performance and dimensions of interest in solutions, (2) returns a set of high-performing, yet diverse solutions, and (3) improves the state-of-the-art for finding a single, best solution, it will catalyze advances throughout all science and engineering fields.
- [[Novelty Search]]: an algorithm that abandons the goal of improving performance altogether, and instead select only for diversity in the feature space.
	- Performs better than performance-driven search on deceptive problems
	- How about standard (non-deceptive) problems? #Questions
	- > The user defines how to measure the distance between behaviors, and then Novelty Search seeks to produce as many different behaviors as possible according to this distance metric. The algorithm stops when an individual in the population solves the objective (i.e. their performance is high enough).
	- Does not work well with very large feature/behavioral spaces.
- ## [[MAP-Elites]]
	- Allowing  users to **create diversity in the dimensions of variation** they choose.
	- Illuminating the fitness potential of the entire feature space, not just the high-performing areas, revealing relationships between dimensions of interest and performance.
	- **Improved optimization performance**; the algorithm often finds a better solution than the current state-of-the-art search algorithms in complex search spaces because it explores more of the feature space, which helps it avoid local optima and thus find different, and often better, fitness peaks.
	- The search for a solution in any single cell is **aided by the simultaneous search for solutions in other cells**.
		- It may be more likely to generate a solution for one cell by mutating a solution to a more distant cell, a phenomenon called “goal switching” in a new paper that uses MAP-Elites
		- It may be more likely to produce a solution to a cell by crossing over two solutions from other cells
	- Returning a large set of diverse, high-performing individuals embedded in a map that describes where they are located in the feature space, which can be used to create new types of algorithms or improve the performance of existing algorithms
- [[optimization algorithms]] are not traditionally designed to report the highest-performing solution possible in an area of the feature space that cannot produce either the highest-performing solution overall, or a solution on the Pareto front.
-