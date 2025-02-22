alias:: QD

- The quality diversity (QD) problem assumes an objective $f : \mathbb{R}^n \to \mathbb{R}$ in an $n$-dimensional continuous space $\mathbb{R}^n$ and $k$ measures $m_i : \mathbb{R}^n \to \mathbb{R}$ or, as a joint measure, $\bm{m}: \mathbb{R}^n \to \mathbb{R}^k$. Let $S = \bm{m}(\mathbb{R}^n)$ be the measure space formed by the range of $m$. For each $\bm{s} \in S$ the QD objective is to find a solution $\bm{\theta} = \bm{s}$ and $f(\bm{\theta})$ is maximized.
- However, since the measure space in continuous, QD algorithms in the [[MAP-Elites]] family relax the problem by discretizing $S$ via a tesselation method. Let $T$ be the tessellation of $S$ into $M$ cells. We relax the QD objective to find a set of solutions $\bm{\theta_i}$, $i \in \{1, \dots, M\}$, such that each $\bm{\theta_i}$ occupies one unique cell in $T$. The occupants $\bm{\theta_i} of all $M$ cells form an **archive** of solution.
- Each solution $\bm{\theta_i}$ has a position in the archive $\bm{m}(\bm{\theta_i})$, corresponding to one out of $M$ cells, and an objective value $f(\bm{\theta_i})$.
- The objective of this QD relaxation can be rewritten as follows, where the foal is to maximize the objective value for each cell in the archive:
  $$
  \max \sum^M_{i=1} f(\bm{\theta_i})
  $$