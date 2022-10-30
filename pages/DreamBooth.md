source:: https://arxiv.org/pdf/2208.12242.pdf
github:: https://github.com/XavierXiao/Dreambooth-Stable-Diffusion

- ## Objective: subject-driven generation
	- Given a few (3-5) casually captured images of a subject, the goal is to synthesize novel renditions of the subject in different contexts, while maintaining high fidelity to its key visual features.
- ## Contributions
	- A new technique for fine-tuning text-to-image diffusion models in a few-shot setting, while preserving the
	  model’s semantic knowledge on the class of the subject.
	- Examples of output variations include: changing the place where the subject is, changing a property of the subject such as color, species, or shape, and modifying the subject’s pose, expression, material, and other semantic modifications.
- ## Method
	- ![image.png](../assets/image_1667054672048_0.png){:height 269, :width 705}
	- ![](https://lh6.googleusercontent.com/myPgm3ieu3I3cG-HULMvmivhlsTLwCyQMDSgwBLkGPbf-j_M25NpAHqysGMP6VMFlQ1JO-9Ar2odooTjBUbw_OSdSOJEgH0N-2eFzZumfNQlgRcGXDnz-aZPucCUep11O9LLeJM-sF0QxKEsV2LOMbEQXN8f4T93sYvPDRsOz4iREqaIEoMTOsIb){:height 346, :width 685}
	-
	- The DreamBooth pipeline mainly consist of the following:
		- **Input**: images of a particular subject + the corresponding class name
		- **Regularization**: generate regularization images of the corresponding class name using pre-trained Text-to-Image model
		- **Fine-tuning**: fine-tune the pre-trained Text-to-Image model based on **regularization** images and **input** images to generate a *personalized* Text-to-Image model
		- **Super-Resolution**
		- **Inference**