alias:: MaterIA: Single Image High-Resolution Material Capture in the Wild
tags:: #[[material capture]] #SVBRDF #[[shadow removal]] #[[deep learning]] #[[dataset synthesis]] #[[delighting]]
authors:: Rosalie Martin, Arthur Roullier, Romain Rouffet, Adrien Kaiser, and Tamy Boubekeur

- ### Background
	- Recent development uses a single, uncalibrated smartphone photo of the sample to reverse-engineer the individual components of its [[SVBRDF]].
	- Vast majority of methods (citation needed) requires the photo to be taken with a flash to help a neural architecture drawing cues from the reflectance and mesogeometric properties of the sample
	- **This approach falls short in outdoor scenarios.**
		- Camera flash may have no effect, with lighting being dominated by the sky and/or the sun.
- ## Main Contributions
	- A single image method to address outdoor material capture scenarios.
		- Relies on a micro-facet [[BRDF]] model based on the GGX normal distribution function.
		- Parameterize appearance with **reflectance** (diffuse albedo, roughness) and **mesogeometric** (normal, height, ambient occlusion)
	- Hybrid method: neural architecture is employed on the most challenging aspects of the problem, and scalable numerical methods are used on easier tasks.
		- Circumvents the neural dimensionality problem.