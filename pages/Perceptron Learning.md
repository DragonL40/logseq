- Linear function can be used for classification as well as regression.
- > Given some training data, the task of classification is to learn a hypothesis $h$ that will take new $(x_1, x_2)$ points and return either $0$ for class A and $1$ for class B.
- A **decision boundary** is a line (or a surface, in higher dimensions) that separates the two classes.
- A linear decision boundary is called a **linear separator** and data that admit such a separator are called **linearly separable**. Note that a linear separator is defined by
  $$
  w_0 x_0 + w_1 x_1  + \cdots + w_n x_n = 0
  $$
  where $x_0 = 1$.
- We can write the classification hypothesis as
  $$
  h_w(\vec{x}) = \mathrm{step}(\vec{w} \cdot \vec{x})
  $$
  where $\mathrm{step}(z)$ is $1$ if $z \ge 0$ and $0$ otherwise.
- **Perceptron learning rule**
  $$
  w_i \gets w_i + \alpha (y - h_w(\vec{x})) \times x_i
  $$
-