3D U-Net segmentation using PyTorch Lightning and MONAI.

Brainstorm:
- Brief explanation of the two packages and the problem.
- Need to get MACCAI aorta data to use as examples.
- Visualizations will be important, hopefully I can embed views.
- Explain all code files, and try to minimize them.
- A note on code style to encourage researchers
- A note on who the guide is for:
	- Those who know the basics of PyTorch Lightning and MONAI
	- Should already be comfortable with PyTorch and Python in general (e.g., Numpy, Matplotlib, programming in general)
	- Can make beginning friendly one in future if there's demand
- PyTorch-Lightning excels at automating many routine tasks in PyTorch. For example, can easily activate parallel GPU training, logging, and other features.
	- Link to PyTorch-LIghtning page explaining how it works
- MONAI excels at handling medical images. It's also built on top of PyTorch. It's main feature is the "MetaTensor", an extension of PyTorch Tensor that keeps track of meta data like voxel spacing, volume orientation, etc.

The value:
- MONAI and Lightning are individually amazing. They are both built on top of PyTorch, but weren't exactly built to work with each other.
- MONAI has some tutorials on how to integrate it with Lightning, but they only scratch the surface. Here I expand upon those tutorials and offer the following benefits:
	- More thorough explanations of how the code works.
	- Show how to use multi-GPU single node training.
	- Show how to optimize MONAI's data pipeline to significantly decrease training time.
	- Show how to use Lightning Command Line Interface (CLI).
	- Show how to use MONAI's data pipelines in Lightning's LightningDataModule class.
	- Show how to set-up cross fold validation.
- In short, I'd like to share everything I've learned including the lessons and features of these two great packages.

- All of the code is posted on Github at <link>
- This plan will be to share  a series of blog posts where I focus on one topic or one script at a time.

- The task: Given a CTA scan, segment the aorta and localize 6 anatomical landmarks.
- Method: Multitask learning
- Speed help:
	- Cache Dataset
	- CacheNTransforms / Presistant Dataset
	- Automatic Mixed Percision
	
- Weird things:
	- Using EnsureType too early