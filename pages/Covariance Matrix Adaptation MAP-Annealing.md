alias:: CMA-MAE
source:: https://arxiv.org/abs/2205.10752

- ## Summary
	- This paper proposes a new [[quality diversity]] algorithm that bridges the gap between single-objective optimization and [[quality diversity]] optimization.
## Main Contributions
	- Propose a new algorithm, [[CMA-MAE]] that smoothly blends between [[CMA-ES]] and [[CMA-ME]] through a single parameter $\alpha$.
	- Prove that [[CMA-MAE]] blends between [[CMA-ES]] and [[CMA-ME]], and that [[CMA-MAE]] becomes a density descent method in measure space for any $0 < \alpha < 1$ when optimizing flat objectives.
	- Show that in three QD benchmark domains (Linear Projection, Arm Repertoire, and Latent Space Illumination) that [[CMA-MAE]] outperforms state-of-the-art QD algorithms, and [[CMA-MAE]] maintains robust performance across different archive resolutions and archive learning rates.
## Key Concepts
	-
- ## Algorithms
	- [[CMA-MAE]] is an algorithm that smoothly blends between [[CMA-ES]] and [[CMA-ME]].
	- Maintains a discount function $f_A(\bm{\theta'})$ and ranks solutions by improvement $f(\bm{\theta'}) - f_A(\bm{\theta'})$, where $f_A(\bm{\theta'}) = t_e$ ($t_e$ is an acceptance threshold maintained for each cell in the archive $A$).
		- When the archive is updated, $t_e \gets (1 - \alpha) t_e + \alpha f(\bm{\theta'})$.
			-
- ## Experiment
	- ### Study Design
		- Independent Variables: between-groups design with two independent variables: the algorithm and the domain.
		- Dependent Variables: [[QD-score]] as a metric for the quality and diversity of solutions, and the coverage, defined as the number of occupied cells in the archive divided by the total number of cells.
			- Note: The [[QD-score]] metric is normalized by the archive size.
	-