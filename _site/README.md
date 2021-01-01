<p align="center" vertical-align="middle"><img src="doc/fire.png" alt="drawing" width="20"/><img src="doc/fire.png" alt="drawing" width="30"/><img src="doc/fire.png" alt="drawing" width="20"/></p>

# Self-driving cars perception notes

## Contents

- [1. 3D Object Detection]()
	- [1A. Evaluation metrics](3d_od/evaluation.md)
	- [1B. Datasets](3d_od/dataset.md)
	- [1C. Approaches](3d_od/appro.md)
- [2. Depth Estimation]() 
	- [2A. Evaluation metrics](depth_estimation/evaluation.md)
	- [2B. Datasets](depth_estimation/dataset.md)
	- [2C. Approaches](depth_estimation/appro.md)
- [3. Segmentation]()
	+ [3A. Evaluation metrics](seg/evaluation.md)
	+ [3B. Datasets](seg/dataset.md)
	+ [3C. Approaches](seg/appro.md)
- [4. 2D Object Detection]()
	- [4A. Evaluation metrics](2d_od/evaluation.md)
	- [4B. Datasets](2d_od/dataset.md)
	- [4C. Approaches](2d_od/appro.md)
- [5. Others](#5-others)

> **_Click on [<img src="doc/50.png" width="95">](README.md) which represents the "Reading & Writting" process of each paper to see more details_**  
> **_Synthetic: [Loss function](loss_problem.md), [Network problem](network_problem.md), [Depth limit](depth_estimation/depth_limit.md)_**

> **_Update: in the process of adding all the articles i've read before 2021_** ~_~  
> **_Here is [time-list paper](time_list_paper.md)_**








### 5 Others

> **_LiDAR:_** [awesome-LiDAR](https://github.com/szenergy/awesome-lidar#datasets), [awesome-point-cloud-analysis](https://github.com/Yochengliu/awesome-point-cloud-analysis), [awesome-point-cloud-deep-learning](https://github.com/dashidhy/awesome-point-cloud-deep-learning)

#### Comparison
 Comparison | Camera | LiDAR | RADAR 
 -- | -- | -- | -- 
test1 | test2 | | test4

#### Andrej Karpathy - AI for Full-Self Driving at Tesla
[Andrej Karpathy - AI for Full-Self Driving at Tesla](https://www.youtube.com/watch?v=hx7BXih7zx8&feature=youtu.be)

[Tesla autopilotAI](https://www.tesla.com/autopilotAI)

Takeaways's Lei Xin:
1. What is Tesla Autopilot 1:20
2. **Tesla's methods are heavily based on computer vision rather than lidar** 5:25
3. Neural networks in production 6:55
4. Receive training images for tricky cases from the fleet 8:35
5. For testing, it is not enough to just rely on loss function and mean accuracy of test set 13:00
6. HydraNet contains 48 networks with shared backbone, 1,000 distinct predictions (Number of output tensors) and it takes 70,000 GPU hours to train 14:12
7. Neural networks for full self-driving 16:54
8. **Get depth estimation from images directly by using self-supervised techniques** 22:54, predict the depth, drive to it and measure the real distance
9. other uses of **self-supervised learning** 25:24
10. Q&A 26:50

#### Other sources

> **_[Learning-Deep-Learning](https://github.com/patrick-llgc/Learning-Deep-Learning)_**


