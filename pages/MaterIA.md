alias:: MaterIA: Single Image High-Resolution Material Capture in the Wild
tags:: #[[material capture]] #SVBRDF #[[shadow removal]] #[[deep learning]] #[[dataset synthesis]] #[[delighting]]
authors:: Rosalie Martin, Arthur Roullier, Romain Rouffet, Adrien Kaiser, and Tamy Boubekeur

- ### Background
	- Recent development uses a single, uncalibrated smartphone photo of the sample to reverse-engineer the individual components of its [[SVBRDF]].
	- Vast majority of methods (citation needed) requires the photo to be taken with a flash to help a neural architecture drawing cues from the reflectance and mesogeometric properties of the sample
	- **This approach falls short in outdoor scenarios.**
		- Camera flash may have no effect, with lighting being dominated by the sky and/or the sun.
- ## Main Contributions
	- We propose a [[SVBRDF]] acquisition method from a single image that targets highly-irregular materials captured in a natural lighting environment, where self-cast shadows have to be removed.
		- Addresses outdoor material capture scenarios.
		- Relies on a micro-facet [[BRDF]] model based on the GGX normal distribution function.
		- Parameterize appearance with **reflectance** (diffuse albedo, roughness) and **mesogeometric** (normal, height, ambient occlusion)
	- Hybrid method: neural architecture is employed on the most challenging aspects of the problem, and scalable numerical methods are used on easier tasks.
		- Circumvents the **neural dimensionality problem**.
		- Deep neural architecture to resolve the most ambiguous tasks – delighting the input picture and extracting the geometric gradients.
		- Explicit numerical methods to deduce the remaining [[SVBRDF]] channels.
	- **Synthetic dataset generation**
	- **Illumination decomposition**: decompose the delighting problem into the prediction of the irradiance and specular contribution to compute the albedo.
	- **Cascaded neural architecture**: cascaded U-Nets
	- Seamless high-resolution outputs
	-