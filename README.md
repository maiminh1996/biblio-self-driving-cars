 <link rel="stylesheet" href="styles.css"> 

# [&larr;](https://maiminh1996.github.io/blog.html)

<p align="center" vertical-align="middle"><img src="doc/fire.png" alt="drawing" width="20"/><img src="doc/fire.png" alt="drawing" width="30"/><img src="doc/fire.png" alt="drawing" width="20"/></p>

# Self-driving cars perception notes

## Contents

1. [3D Object Detection](README.md)
	1. [Evaluation metrics](3d_od/evaluation.md)
	2. [Datasets](3d_od/dataset.md)
	3. [Approaches](3d_od/appro.md)
2. [Depth Estimation](README.md) 
	1. [Evaluation metrics](depth_estimation/evaluation.md)
	2. [Datasets](depth_estimation/dataset.md)
	3. [Approaches](depth_estimation/appro.md)
3. [Segmentation](README.md)
	1. [Evaluation metrics](seg/evaluation.md)
	2. [Datasets](seg/dataset.md)
	3. [Approaches](seg/appro.md)
4. [2D Object Detection](README.md)
	1. [Evaluation metrics](2d_od/evaluation.md)
	2. [Datasets](2d_od/dataset.md)
	3. [Approaches](2d_od/appro.md)
6. [All about self-driving car](all.md)
5. [Other sources](#other-sources)

> **_See this repo from my site: [https://maiminh1996.github.io/biblio-self-driving-cars/](https://maiminh1996.github.io/biblio-self-driving-cars/)_**

> **_Click on [<img src="doc/50.png" width="95">](README.md) which represents the "Reading & Writting" process of each paper to see more details_**  
> **_Synthetic: [Loss function](loss_problem.md), [Network problem](network_problem.md), [Depth limit](depth_estimation/depth_limit.md), [Geometry](geometry.md)_**

> **_[Data preprocessing](dataset/data_preprocessing.md)_**

> **_Update: in the process of adding all the articles i've read before 2021_** ~_~  
> **_Here is [time-list paper](time_list_paper.md)_**




### Other sources

> **_LiDAR:_** [awesome-LiDAR](https://github.com/szenergy/awesome-lidar#datasets), [awesome-point-cloud-analysis](https://github.com/Yochengliu/awesome-point-cloud-analysis), [awesome-point-cloud-deep-learning](https://github.com/dashidhy/awesome-point-cloud-deep-learning)

> **_Others:_** [Learning-Deep-Learning](https://github.com/patrick-llgc/Learning-Deep-Learning), <a href="https://medium.com/swlh/making-a-pseudo-lidar-with-cameras-and-deep-learning-e8f03f939c5f">Making a Pseudo LiDAR With Cameras and Deep Learning</a>


#### Andrej Karpathy'talk - AI for Full-Self Driving at Tesla
[Andrej Karpathy - AI for Full-Self Driving at Tesla](https://www.youtube.com/watch?v=hx7BXih7zx8&feature=youtu.be), [Tesla autopilotAI](https://www.tesla.com/autopilotAI)
<details>
  <summary>Takeaways's Lei Xin!</summary>
1. What is Tesla Autopilot 1:20<br/>
2. <b>Tesla's methods are heavily based on computer vision rather than lidar</b> 5:25<br/>
3. Neural networks in production 6:55<br/>
4. Receive training images for tricky cases from the fleet 8:35
5. For testing, it is not enough to just rely on loss function and mean accuracy of test set 13:00<br/>
6. HydraNet contains 48 networks with shared backbone, 1,000 distinct predictions (Number of output tensors) and it takes 70,000 GPU hours to train 14:12<br/>
7. Neural networks for full self-driving 16:54<br/>
8. <b>Get depth estimation from images directly by using self-supervised techniques</b> 22:54, predict the depth, drive to it and measure the real distance<br/>
9. other uses of <b>self-supervised learning</b> 25:24<br/>
10. Q&A 26:50

</details>

#### Tutorial
- [CVPR 2020 Tutorial](http://cvpr2020.thecvf.com/program/tutorials)
	- [All You Need to Know About Self-Driving](http://www.allaboutselfdriving.com/)
- [NeurIPS 2020 Tutorial](https://nips.cc/virtual/2020/public/e_tutorials.html)

<!--

</br>● 

-->

