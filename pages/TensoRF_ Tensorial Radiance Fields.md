public:: true
title:: TensoRF: Tensorial Radiance Fields
alias:: TensoRF
tag:: #paper #[[Radiance Fields]]

- ## Key Concepts/Related Work
	- [[CP Decomposition]]
	- [[Tensor Decomposition]]
- > Both efficient in training time and compact in memory footprint, and at the same time achieves state-of-the-art rendering quality.
- Unlike [[NeRF]] that purely uses MLPs, we model the radiance field of a scene as a 4D tensor, which represents a 3D voxel grid with per-voxel multi-channel features.
- **Beyond superior rendering quality, our models with [[CP Decomposition]] and [[VM Decomposition]] lead to a significantly lower memory footprint in comparison to previous and concurrent works that directly optimize per-voxel features.**
- Our work addresses the inefficiency of voxel grid representations in a principled framework, leading to a family of simple yet effective methods. We leverage the fact that a feature grid can naturally be seen as a 4D tensor, where three of its modes correspond to the XYZ axes of the grid and the fourth mode represents the feature channel dimension. This opens the possibility of exploiting classical tensor decomposition techniques – which have been widely applied to high-dimensional data analysis and compression in various fields [16] – for radiance field modeling. We, therefore, propose to factorize the tensor of radiance fields into multiple low- rank tensor components, leading to an accurate and compact scene representation.
- Our representation supports various types of per-voxel features with different decoding functions, including neural features – depending on an MLP to regress view-dependent colors from the features – and [[spherical harmonics]] (SH) features (coefficients) – allowing for simple color computation from the fixed SH functions and leading to a representation without neural networks.
- ## Main Contributions
- ## Frequency Encoding
  id:: 6284ca61-bcef-4282-8745-7efb80948017
	- Similar to [[NeRF]]  and NSVF, applied frequency encodings on both viewing directions and features.
	- Unlike [[NeRF]] that uses ten different frequencies, [[TensoRF]] use only two.
	- The [[Sine-Cosine Encoding]] encodes scalar positions $x \in \mathbb{R}$ as a
	  multiresolution sequence of $L \in \mathbb{N}$ sine and cosine functions
	  $$
	  \begin{aligned}
	  \mathrm{enc}(x) = (&\sin(2^0 x), \sin(2^1x), \dots, \sin(2^{L-1}x), \\
	  &\cos(2^0 x), \cos(2^1x), \dots, \cos(2^{L-1}x))
	  \end{aligned}
	  $$
	- Higher $L$ leads to more precision in the encoding at the cost of increased model size and, subsequently, increased training time.
	- > What is the optimal $L$ for our model?