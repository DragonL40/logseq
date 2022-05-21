title:: NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis
alias:: NeRF
tag:: #[[Radiance Fields]] #paper

- ## Key Concepts/Related Work
	- Neural 3D shape representations
	- View synthesis and image-based rendering
- A continuous scene is represented as a 5D vector function whose input as a 3D location $\vec{x} = (x,y,z)$ and 2D viewing direction $(\theta, \phi)$ , and whose output is an emitted color $\vec{c} = (r,g,b)$ and volume density $\sigma$ .
	- Let the viewing direction $(\theta, \phi)$ be represented as a 3D Cartesian unit vector $\vec{d}$ .
	- > We approximate this continuous 5D secene representation with an MLP network $F_\Theta : (\vec{x}, \vec{d}) \to (\vec{c}, \sigma)$ and optimize its weights $\Theta$ to map from each input 5D coordinate to its corresponding volume density and directional emitted color.
- ## Main Contributions
	- An approach for representing continuous scenes with complex geometry and materials as 5D neural radiance fields, parameterized as basic MLP networks.
	- A differentiable rendering procedure based on classical volume rendering techniques, which we use to optimize these representations from standard RGB images. This includes a hierarchical sampling strategy to allocate the MLP’s capacity towards space with visible scene content.
	- A positional encoding to map each input 5D coordinate into a higher dimensional space, which enables us to successfully optimize neural radiance fields to represent high-frequency scene content.
- ## Volume Rendering with Radiance Fields
	- We render the color of any ray passing through the scene using principles from ^^classical volume rendering^^.
	  Kajiya, J.T., Herzen, B.P.V.: Ray tracing volume densities. Computer Graphics (SIGGRAPH) (1984)
	- The volume density $\sigma(\vec{x})$ can be interpreted as the differential probability of a ray terminating at an infinitesimal particle at location $\vec{x}$ .
	- The expected color $C(\vec{R})$ of camera ray $\vec{r}(t) = \vec{o} + t\vec{d}$ with near and far bounds $t_n$ and $t_f$ is:
	  $$
	  C(\vec{r}) = \int_{t_n}^{t_f} T(t) \sigma(\vec{r}(t))\vec{c}(\vec{r}(t), \vec{d})dt
	  $$ where $T(t) = \exp\left(- \int^t_{t_n} \sigma(\vec{r}(s))ds\right)$ denotes the probability that the ray travels from $t_n$ to $t$ without hitting any other particle (accumulated transmittance).
- ## Optimizing a Neural Radiance Field
	- We introduce two improvements to enable representing high-resolution complex scenes.
	- The first is a **positional encoding** of the input coordinates that assists the MLP in representing high-frequency functions, and the second is a **hierarchical sampling procedure** that allows us to efficiently sample this high-frequency representation.