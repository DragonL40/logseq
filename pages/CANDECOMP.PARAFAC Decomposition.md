title:: CANDECOMP/PARAFAC Decomposition
alias:: CP Decomposition

- Given a 3D tensor $\mathcal{T} \in \mathbb{R}^{I \times J \times K}$, CP decomposition factorizes it into a sum of outer products of vectors:
  $$
  \mathcal{T} = \sum_{r=1}^{R} v_r^1 \circ v_r^2 \circ v_r^3
  $$
  where $v_r^1 \circ v_r^2 \circ v_r^3$ corresponds to a rank-one tensor component, and $v_r^1 \in R^I$, $v_r^2 \in R^J$, $v_r^3 \in R^K$ are factorized vectors of the three modes for the $r$th component.
- [[CP Decomposition]] factorizes a tensor into multiple vectors, expressing multiple compact rank-one components.
- However, because of too high compactness, [[CP Decomposition]] can require many components to model complex scenes, leading to high computational costs in radiance field reconstruction.