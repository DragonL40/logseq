- A symmetric matrix $C \in \R^{n \times n}$ is positive definite if for all $x \in \R^n \setminus \{0\}$ holds $xCx > 0$.
- The [[Eigendecomposition]] of $C$ obeys $$ C =BD^2B^\intercal$$, where 
  $B$ is an orthogonal matrix, $B^\intercal B = BB^\intercal = I$. Columns of $B$ form an orthonormal basis of eigenvectors.
  $D^2 = DD = \mathrm{diag}(d_1, \dots, d_n)^2 = \mathrm{diag}(d_1^2, \dots, d_n^2)$ is a diagonal matrix with  eigenvalues of $C$ as diagonal elements.
-