- #[[optimization algorithms]]
- Local search algorithms operate by searching from a start state to neighboring states, without keeping track of the paths, nor the set of states that have been reached.
	- Not systematic — might never explore a portion of the search space where a solution actually resides.
	- Use very little memory.
	- Often find reasonable solutions in large or infinite state spaces for which systematic algorithms are unsuitable.
- [[hill-climbing search]]
	- Greedy; heads in the direction that provides the **steepest ascent**.
	- Terminates when it reaches a "peak" where no neighbor has a higher value.
	- Can get stuck for any of the following reasons:
		- Local maxima
		- Ridges: A sequence of local maxima that are not directly connected to each other.
		  collapsed:: true
			- ![image.png](../assets/image_1666665576616_0.png)
		- Plateaus
	- Variants:
		- Allow a certain number of sideways move
		- Stochastic hill-climbing
		- First-choice hill-climbing
		- Random-restart hill-climbing
- [[simulated annealing]]
	- Similar to [[hill-climbing search]]
	- Instead of picking the *best* move, pick a random move $m$.
		- If $m$ improves the situation, it is always accepted. Otherwise, accept $m$ with some probability less than 1.
		- The probability decreases as $T$ goes down.
- [[gradient descent]]
	- Finding a local minimum of differentiable function $f(x_1, x_2, \dots, x_n)$ with gradient descent (for a small learning rate $\alpha > 0$).
	  $$
	  x_i = x_i - \alpha (\frac{df}{dx_i})
	  $$
	- ```python
	  def GRADIENT_DESCENT(f, alpha):
	    initialize v = (x_1, x_2, ..., x_n) with random values
	    while (v is not local minimum):
	      for x_i in v:
	        x_i = x_i - alpha (derivative of f with respect to x_i)
	  ```
	- Problems and solution approaches
		- Overshooting the local minimum: momentum term
		- Local minima: random restarts, simulated annealing, STAGE
		- Plateaus (one of the issues of threshold activation functions): random restarts
		- Ridges: momentum term
- [[evolutionary algorithms]]
	- There are endless forms of evolutionary algorithms, varying in the following ways:
		- The size of the population
		- The representation of each individual.
			- In [[genetic algorithms]], each individual is a string over a finite alphabet (often a Boolean string).
			- In [[evolution strategies]], an individual is a sequence of real numbers.
			- In [[genetic programming]], an individual is a computer program.
		- The number of parents $\rho$ that come together to form offspring (commonly $\rho = 2$).
			- When $\rho = 1$ we have [[stochastic beam search]], i.e. asexual reproduction.
		- The selection pro