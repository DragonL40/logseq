alias:: GSA
source:: http://www.cmap.polytechnique.fr/~nikolaus.hansen/GSAES.pdf

- A mutation step is carried out by adding a normal distributed random vector $z'$ on the object variable vector with
  $$
  z' := \delta \cdot (z_1 b_1 + \dots + z_n b_n)
  $$
  where $n$ is the number of object variables, $\delta$ is the global step size, $z_i \sim N(0,1)$
-