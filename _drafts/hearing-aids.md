---
title: Automatically Quantifying Aortic Growth in Diverse 3D Medical Images
permalink: /projects/seg
layout: single
classes: wide
---
**Context:**  Hearing aids...

[hearing aid picture]

**Challenge:** Filterbanks are a component

[picture]

**Objective:**  Develop a small and low-power filterbank design that meets the requisite 

[picture]

**Method:** Use stochastic computing to implement the filtering directly in hardware. 

**Outcome:** Stochastic computing is an unconventional computing technique that can implement massively parallel operations like those

[picture]

**My Contributions:**
Over a few months I accomplished:
1. **Data preparation:** Prepared 720 new training samples of large 3D CTA scans for training the U-Net. In short, I developed a robust ETL pipeline in Python to clean and organize data into a standardize format.  Final dataset is about 700 GB.
2. **Training optimization:** Improved CNN training speed by a factor of 500 by minimizing data movement, implementing half precision training, utilizing parallel GPU processing on a SLURM cluster, and addressing other bottlenecks.
3. **Prediction optimization:** Improved prediction accuracy by utilizing a sliding window inference function and improved prediction time by a factor of 10 by addressing pipeline bottlenecks like unnecessary data movement.
4. **Performance Validation:** Implemented cross-fold validation and ran statistical paired t-tests to compare different network architectures and training approaches. Found that multitask training improved accuracy compared to traditional single task training approach.
5. **Guard Rails:** Implemented guardrails for when this software is deployed in a clinical setting. Specifically, the pipeline not only outputs diameter measurements, but displays visuals of those measurements that can be easily verified by a physician.
[picture]