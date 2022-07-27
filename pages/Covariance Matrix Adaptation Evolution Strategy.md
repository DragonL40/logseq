alias:: CMA-ES
source:: https://cma-es.github.io/

- The CMA-ES (Covariance Matrix Adaptation Evolution Strategy) is an evolutionary algorithm for difficult **non-linear non-convex black-box optimization problems** in continuous domain.
  id:: 62e0a252-395f-45b3-b1de-9621a96528bf
- > The method should be applied, if derivative based methods, e.g. quasi-Newton BFGS or conjugate gradient, (supposedly) fail due to a rugged search landscape (e.g. discontinuities, sharp bends or ridges, noise, local optima, outliers).
- Similar to quasi-Newton methods (but not inspired by them), the CMA-ES is a **second order** approach estimating a positive definite matrix within an iterative procedure (more precisely: a covariance matrix, that is, on convex-quadratic functions, closely related to the inverse Hessian).
-