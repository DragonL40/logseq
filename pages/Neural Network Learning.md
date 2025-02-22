- **Feedforward network** has connections only in one direction - [[Directed Acyclic Graph (DAG)]] with designated input and output nodes.
- Each node computes a function of its inputs and passes the result to its successors in the network.
- **Recurrent network** feeds its intermediate of final outputs back into its own inputs.
	- The signal values within the network form a dynamical system that has internal state or memory.
- [[universal approximation theorem]] states that a network with just two layers of computational units, the first nonlinear and the second linear, can approximate any continuous function to an arbitrary degree of accuracy.
- Common activation functions:
	- **Sigmoid:** $\sigma(x) = \frac{1}{1 + e^{-x}}$
	- **ReLU:** $\mathrm{ReLU}(x) = \max(0,x)$
	- **Softplus:** $\mathrm{softplus}(x) = \log(1+e^x)$
		- The derivate of the softplus function is the sigmoid function.
	- **tanh:** $\tanh(x) = \frac{e^{2x}-1}{e^{2x} + 1}$
		- Note that the range of $\tanh$ is $(-1, +1)$. $\tanh$ is a scaled and shifted version of sigmoid, as $\tanh(x) = 2\sigma(2x)-1$.