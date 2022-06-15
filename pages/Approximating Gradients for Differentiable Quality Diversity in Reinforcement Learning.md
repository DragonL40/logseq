alias:: DQD-RL
source:: https://dqd-rl.github.io

- ## Main Contributions:
	- formalize the problem of quality diversity for reinforcement learning (QD-RL) and
	  reduce it to an instance of DQD.
	- develop two QD-RL variants of the DQD algorithm [[CMA-MEGA]], where each algorithm approximates objective and measure gradients with a different combination of ES and actor-critic methods.
	- benchmark our variants on four PyBullet locomotion tasks from QDGym.
- ## Key Concepts:
	- [[evolution strategies]]
		- A class of evolutionary algorithms which optimizes the objective by sampling a population of solutions and moving the population towards areas of higher performance.
		- [[Natural Evolution Strategies]] is a type of [[evolution strategies]] which updates the sampling distribution of solutions by taking steps on distribution parameters in the direction of the natural gradient.
		- [[OpenAI-ES]] samples $\lambda_{es}$ solutions from an isotropic Gaussian but only computes a gradient step for the mean $\phi$. Each solution is represented as $\phi + \sigma \epsilon_i$, where $\sigma$ is the fixed standard deviation of the Gaussian and $\epsilon \sim N(0,I)$.
		- [[OpenAI-ES]] estimates the gradient as
		  $$
		  \nabla f(\phi) \approx \frac{1}{\lambda_{es}\sigma} \sum_{i=1}^{\lambda_{es}} f(\phi + \sigma \epsilon_i) \epsilon_i
		  $$
		-
		-
		- #Questions what is a markovian value?
		- [[actor-critic methods]]
			- [[Twin Delayed Deep Deterministic policy gradient]]
		- [[Quality Diversity]] algorithms
			- [[MAP-Elites]]
			- [[Policy Gradient Assisted MAP-Elites]]
			- [[ME-ES]], combines [[MAP-Elites]] with an [[OpenAI-ES]] optimizer
			- [[CMA-MEGA]]
			-
			-