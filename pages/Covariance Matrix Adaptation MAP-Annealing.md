alias:: CMA-MAE
source:: https://arxiv.org/abs/2205.10752

- ## Summary
	- This paper proposes a new [[quality diversity]] algorithm that bridges the gap between single-objective optimization and [[quality diversity]] optimization.
## Main Contributions
	- Propose a new algorithm, [[CMA-MAE]] that smoothly blends between [[CMA-ES]] and [[CMA-ME]] through a single parameter $\alpha$.
	- Prove that [[CMA-MAE]] blends between [[CMA-ES]] and [[CMA-ME]], and that [[CMA-MAE]] becomes a density descent method in measure space for any $0 < \alpha < 1$ when optimizing flat objectives.
	- We show in three QD benchmark domains (Linear Projection, Arm Repertoire, and Latent Space Illumination) that [[CMA-MAE]] outperforms state-of-the-art QD algorithms, and [[CMA-MAE]] maintains robust performance across
## Key Concepts