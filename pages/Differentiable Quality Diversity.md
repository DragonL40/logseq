alias:: CMA-MEGA, DQD
source:: https://proceedings.neurips.cc/paper/2021/hash/532923f11ac97d3e7cb0130315b067dc-Abstract.html

- Previous [[Quality Diversity]] algorithms ignores gradient information of the objective and the measure function.
- The differentiable quality diversity problem is a special case of [[Quality Diversity]] where both the objective and measure functions are first-order differentiable.
  background-color:: #978626
- ## Main Contribution
	- Introduce and formalize the problem of [[DQD]].
	- Present the algorithm [[Objective and Measure Gradient MAP-Elites via a Gradient Arborescence]], based on [[MAP-Elites]], and which branches based on the measures $m_i$ but ascends based on the objective function $f$.
	- Present the algorithm [[Covariance Matrix Adaptation MAP-Elites via a Gradient Arborescence]], based on the [[CMA-ME]] algorithm, and which branches based on the objective-measure space but ascends based on maximizing the QD objective.
	- Shows that in QD domains linear projection, arm repertoire, and latent space illumination [[DQD]] algorithms significantly outperform state-of-the-art QD algorithms.
- ## Key Concepts
	- [[gradient arborescence]]
- ## Algorithms
	-
-
- what are "end-to-end differentiable neural networks"? #Questions
-