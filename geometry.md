## Geometry in Computer Vision?
Ref: [Have We Forgotten about Geometry in Computer Vision?](https://alexgkendall.com/computer_vision/have_we_forgotten_about_geometry_in_computer_vision/)

[End-to-End Learning of Geometry and Context for Deep Stereo Regression](https://arxiv.org/pdf/1703.04309.pdf)

[Unsupervised CNN for Single View Depth Estimation: Geometry to the Rescue](https://arxiv.org/abs/1603.04992)

>**__Geometry (such as depth, volume, shape, pose, disparity, motion or optical flow)__** describes the structure and shape of the world

- **depth from motion** (depth from optical expansion) which do not need to be learned from scratch with deep learning
- observing shape from shading or depth from stereo disparity.
- **semantic representations** are often proprietary to a **human language**, with labels corresponding to a limited set of nouns, which can’t be directly observed. (because semantics are defined by humans, it is also likely that these representations **aren’t optimal**. Learning directly from the observed geometry in the world might be more natural.)
- Geometry is based on continuous quantities
    - depth in metres or disparity in pixels
    - semantic representations are largely discretised quantities or binary labels