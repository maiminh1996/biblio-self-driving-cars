<p align="center" vertical-align="middle"><img src="doc/fire.png" alt="drawing" width="30"/><img src="doc/fire.png" alt="drawing" width="50"/><img src="doc/fire.png" alt="drawing" width="30"/></p>

# <p align="center" vertical-align="middle">Self-driving cars perception notes</p>
## Contents

- [1. 3D Object Detection](#1-3d-object-detection)
	- [1A. Evaluation metrics](#1a-evaluation-metrics)
	- [1B. Datasets](#1b-datasets)
	- [1C. Approaches](#1c-Approaches)
- [2. Depth Estimation](#2-depth-estimation) 
	- [2A. Evaluation metrics](#2a-evaluation-metrics)
	- [2B. Datasets](#2b-datasets)
	- [2C. Approaches](#2c-Approaches)
- [3. Segmentation](#3-segmentation)
	+ [3A. Evaluation metrics](#3a-evaluation-metrics)
	+ [3B. Datasets](#3b-datasets)
	+ [3C. Approaches](#3c-Approaches)
- [4. 2D Object Detection](#4-2d-object-detection)
	- [4A. Evaluation metrics](#4a-evaluation-metrics)
	- [4B. Datasets](#4b-datasets)
	- [4C. Approaches](#4c-Approaches)
- [5. Sensors](#5-sensors)

> **_Click on the "Reading & Writting" process bar to see more details of each paper [![Progress](https://progress-bar.dev/50/?title=done)](README.md)_**

<p align="center" vertical-align="middle"><img src="doc/fire.png" alt="drawing" width="20"/><img src="doc/fire.png" alt="drawing" width="30"/><img src="doc/fire.png" alt="drawing" width="20"/></p>
<!-- --><!-- --><!-- --><!-- --><!-- --><!-- --><!-- -->
<!-- --><!-- --><!-- --><!-- --><!-- --><!-- --><!-- -->
<!-- --><!-- --><!-- --><!-- --><!-- --><!-- --><!-- -->
<!-- --><!-- --><!-- --><!-- --><!-- --><!-- --><!-- -->

## 1 3D Object Detection
### 1A Evaluation metrics

> **_Metrics:_**  AP 3D, AP BEV

> **_How to calculate:_** [![Progress](https://progress-bar.dev/0/?title=done)](3d_od/evaluation.md)

<!-- --><!-- --><!-- --><!-- --><!-- --><!-- --><!-- -->

### 1B Datasets

> **_How to obtain 3D bounding box:_**

<details>
  <summary>Click to expand!</summary>

  | Ref | Highlight description |
  | -- | -- | 
  | KITTI (3D OD) [<kbd>CVPR 12</kbd>](http://www.cvlibs.net/publications/Geiger2012CVPR.pdf) [<kbd>IJRR 13</kbd>](http://ww.cvlibs.net/publications/Geiger2013IJRR.pdf) | ● Stereo (1224×368) + LiDAR 64 beams </br> ● Real dataset: 7481 training (splitted as 3DOP [<kbd>NIPS 15</kbd>](https://papers.nips.cc/paper/2015/file/6da37dd3139aa4d9aa55b8d237ec5d4a-Paper.pdf) into 3712 training & 3769 validation) & 7518 test samples [![Progress](https://progress-bar.dev/100/?title=done)](dataset/kitti.md) | <!-- -->
  | KITTI-Object-Depth (KOD) [<kbd>AAAI 20</kbd>](https://arxiv.org/pdf/1909.07701.pdf) | Collect the corresponding gth depth map (11 frame) for each image in KITTI (3D OD) training set [![Progress](https://progress-bar.dev/0/?title=done)](3d_od/foresee.md)| <!-- -->
  | Weather augmented [<kbd>ICCV 19</kbd>](https://team.inria.fr/rits/computer-vision/weather-augment/) | | Weather Kitti and Weather Cityscapes | <!-- -->
  | Seeing Through Fog [<kbd>CVPR 20</kbd>](https://www.cs.princeton.edu/~fheide/AdverseWeatherFusion/) [<kbd>ICCV 19</kbd>](https://github.com/gruberto/Gated2Depth) | <!-- -->
  | Canadian Adverse Driving Conditions [<kbd>arXiv 20</kbd>](https://arxiv.org/pdf/2001.10117.pdf) | ●  56000 camera images, 7000 LiDAR sweeps, </br> ● Real dataset: 75 scenes of 50-100 frames each </br> ● Adverse weather driving conditions, including snow | 

</details>
<!-- --><!-- --><!-- --><!-- --><!-- --><!-- -->

### 1C Approaches
> **_Type 1:_** monocular (M), stereo (S), LiDAR 64 beams (L), LiDAR 4 beams (L4), RADAR (R)</br> 
> **_Type 2:_** supervised (sup), unsupervised (unsup), semi-supervised, (semi-sup), self-supervised (self-sup)

<details>
  <summary>Click to expand!</summary>

| Ref | Type | Data | Highlight description |
| :-- | :--: | :-- | :-- | 
|  | <img src="doc/fire.png" alt="drawing" width="20"/>| <img src="doc/fire.png" alt="drawing" width="20"/> |  |<!-- -->
| Pseudo-LiDAR </br> [<kbd>CVPR 19</kbd>](https://openaccess.thecvf.com/content_CVPR_2019/papers/Wang_Pseudo-LiDAR_From_Visual_Depth_Estimation_Bridging_the_Gap_in_3D_CVPR_2019_paper.pdf) | M / sup | KITTI | ● Pipeline: Depth estimator ➔ convert into pseudo pcl ➔ LiDAR-based detector </br> ● Contrib: Convert depth into pseudo 3d point clouds [![Progress](https://progress-bar.dev/100/?title=done)](3d_od/pseudo_lidar.md) |
| | | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
| Pseudo-LiDAR e2e </br>[<kbd>ICCV 19</kbd>](https://github.com/xinshuoweng/Mono3DPLiDAR) | M / sup | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
| | | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
|  | <img src="doc/fire.png" alt="drawing" width="20"/>| <img src="doc/fire.png" alt="drawing" width="20"/> |  |<!-- -->
| Pseudo-LiDAR V3 E2E </br> [<kbd>CVPR 20</kbd>](https://openaccess.thecvf.com/content_CVPR_2020/papers/Qian_End-to-End_Pseudo-LiDAR_for_Image-Based_3D_Object_Detection_CVPR_2020_paper.pdf) | | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
| CG-Stereo </br> [<kbd>arXiv 20</kbd>](https://arxiv.org/pdf/2003.05505.pdf) | S / sup | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
| Pseudo-LiDAR </br> [<kbd>CVPR 19</kbd>](https://openaccess.thecvf.com/content_CVPR_2019/papers/Wang_Pseudo-LiDAR_From_Visual_Depth_Estimation_Bridging_the_Gap_in_3D_CVPR_2019_paper.pdf) | S / sup | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
| Pseudo-LiDAR ++</br> [<kbd>ICRL 21</kbd>](https://arxiv.org/pdf/1906.06310.pdf) | S / sup | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
| | | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
| | | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
|  | <img src="doc/fire.png" alt="drawing" width="20"/>| <img src="doc/fire.png" alt="drawing" width="20"/> |  |<!-- -->
| PointRCNN | | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
| | | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
| | | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
|  | <img src="doc/fire.png" alt="drawing" width="20"/>| <img src="doc/fire.png" alt="drawing" width="20"/> |  |<!-- -->
| Pseudo-LiDAR ++</br> [<kbd>ICRL 21</kbd>](https://arxiv.org/pdf/1906.06310.pdf) | S+L4 / sup | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
| | | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
| | | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |

</details>

<p align="center" vertical-align="middle"><img src="doc/fire.png" alt="drawing" width="20"/><img src="doc/fire.png" alt="drawing" width="30"/><img src="doc/fire.png" alt="drawing" width="20"/></p>
<!-- --><!-- --><!-- --><!-- --><!-- --><!-- --><!-- -->
<!-- --><!-- --><!-- --><!-- --><!-- --><!-- --><!-- -->
<!-- --><!-- --><!-- --><!-- --><!-- --><!-- --><!-- -->
<!-- --><!-- --><!-- --><!-- --><!-- --><!-- --><!-- -->

## 2 Depth Estimation
### 2A Evaluation metrics

> **_Depth prediction (DP):_** takes only monocular/ stereo as input  
> **_Depth completion (DC):_** takes depth sensor (ex: LiDAR, RADAR) as input component

> **_Metrics DP:_** Accu, SILog, sqErrorRel, absErrorRel, iRMSE, thresh δ  
> **_Metrics DC:_** Accu, iRMSE, iMAE, RMSE, MAE, thresh δ

> **_How to calculate:_** [![Progress](https://progress-bar.dev/50/?title=done)](depth_estimation/evaluation.md)

<!-- --><!-- --><!-- --><!-- --><!-- --><!-- -->

### 2B Datasets
> **_How to obtain depth ground truth:_** 

<details>
  <summary>Click to expand!</summary>

| Ref | Highlight description |
| -- | -- | 
| KITTI (stereo) </br> [<kbd>CVPR 12</kbd>](http://www.cvlibs.net/publications/Geiger2012CVPR.pdf) [<kbd>IJRR 13</kbd>](http://ww.cvlibs.net/publications/Geiger2013IJRR.pdf) | ● Stereo (1224×368) + LiDAR 64 beams </br> ● Gth: projected LiDAR 64 beams pose for 11 odometry sequences </br> ● the 200 training images of KITTI stereo 2015 **overlap** with the validation images of KITTI OD [![Progress](https://progress-bar.dev/100/?title=done)](dataset/kitti.md)| <!-- -->
| Scene Flow </br> [<kbd>CVPR 16</kbd>](https://openaccess.thecvf.com/content_cvpr_2016/papers/Mayer_A_Large_Dataset_CVPR_2016_paper.pdf) | ● Stereo (960x540) </br> ● Synthetic dataset: 35454 training & 4370 testing images </br> ● Gth: dense and elaborate disparity maps [![Progress](https://progress-bar.dev/30/?title=done)](dataset/sceneflow.md) | <!-- -->
| Cityscapes </br> [<kbd>CVPR 16</kbd>](https://www.cityscapes-dataset.com/citation/) | ● Stereo (1024×2048) </br> ● Gth: 22,973 stereo image pairs training  </br> ● Real dataset: 50 cities forseveral months </br> ● 5000 images with fine annotations and 20000 images  with coarse annotations [![Progress](https://progress-bar.dev/20/?title=done)](dataset/cityscapes.md)| <!-- -->

</details>
<!-- --><!-- --><!-- --><!-- --><!-- --><!-- -->

### 2C Approaches

> **_Type 1:_** monocular (M), stereo (S), LiDAR (L), RADAR (R)</br> 
> **_Type 2:_** supervised (sup), unsupervised (unsup), semi-supervised, (semi-sup), self-supervised (self-sup)

<details>
  <summary>Click to expand!</summary>

| Ref | Type | Data | Highlight description |
| :-- | :--: | -- | -- | 
| Eigen et al </br> [<kbd>NIPS 14</kbd>](https://arxiv.org/pdf/1406.2283.pdf) | M / sup | KITTI | ● Loss: [L2 loss](loss_problem.md)|
| DORN </br> [<kbd>CVPR 18</kbd>](https://openaccess.thecvf.com/content_cvpr_2018/papers/Fu_Deep_Ordinal_Regression_CVPR_2018_paper.pdf) | M / sup | KITTI | |  <!-- -->| Discretized depth bins > direct regression </br> binary classification 80 bins (Pixels with distance>80m) [[more]](https://github.com/patrick-llgc/Learning-Deep-Learning/blob/master/paper_notes/dorn.md) |
| FAL </br> [<kbd>NIPS 20</kbd>](https://proceedings.neurips.cc/paper/2020/file/951124d4a093eeae83d9726a20295498-Paper.pdf) | M / self-sup | KITTI | | Occlusion-free reconstruction loss |  <!-- -->
| PSMNet </br> [<kbd>CVPR 18</kbd>](https://openaccess.thecvf.com/content_cvpr_2018/papers/Chang_Pyramid_Stereo_Matching_CVPR_2018_paper.pdf) | S / sup | ● KITTI </br> ● Scene Flow 

</details>


<p align="center" vertical-align="middle"><img src="doc/fire.png" alt="drawing" width="20"/><img src="doc/fire.png" alt="drawing" width="30"/><img src="doc/fire.png" alt="drawing" width="20"/></p>
<!-- --><!-- --><!-- --><!-- --><!-- --><!-- --><!-- -->
<!-- --><!-- --><!-- --><!-- --><!-- --><!-- --><!-- -->
<!-- --><!-- --><!-- --><!-- --><!-- --><!-- --><!-- -->
<!-- --><!-- --><!-- --><!-- --><!-- --><!-- --><!-- -->

## 3 Segmentation
### 3A Evaluation metrics

> **_Metrics:_** 

> **_How to calculate:_** [![Progress](https://progress-bar.dev/0/?title=done)]()
### 3B Datasets

<details>
  <summary>Click to expand!</summary>

  ![Progress](https://progress-bar.dev/0/?title=done)

</details>

### 3C Approaches
<details>
  <summary>Click to expand!</summary>

  ![Progress](https://progress-bar.dev/0/?title=done)

</details>


<p align="center" vertical-align="middle"><img src="doc/fire.png" alt="drawing" width="20"/><img src="doc/fire.png" alt="drawing" width="30"/><img src="doc/fire.png" alt="drawing" width="20"/></p>
<!-- --><!-- --><!-- --><!-- --><!-- --><!-- --><!-- -->
<!-- --><!-- --><!-- --><!-- --><!-- --><!-- --><!-- -->
<!-- --><!-- --><!-- --><!-- --><!-- --><!-- --><!-- -->
<!-- --><!-- --><!-- --><!-- --><!-- --><!-- --><!-- -->

## 4 2D Object Detection
### 4A Evaluation metrics

> **_Metrics:_**  AP 2D

> **_How to calculate:_** [![Progress](https://progress-bar.dev/0/?title=done)](3d_od/evaluation.md)
### 4B Datasets

<details>
  <summary>Click to expand!</summary>

  ![Progress](https://progress-bar.dev/0/?title=done)

</details>

### 4C Approaches
<details>
  <summary>Click to expand!</summary>

| Ref | Type | Data | Highlight description | 
| -- | -- | -- | -- | 
| OneNet </br> [<kbd>arXiv</kbd>](https://arxiv.org/pdf/2012.05780.pdf) | | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: [![Progress](https://progress-bar.dev/0/?title=done)](2d_od/onenet.md) |

</details>

<p align="center" vertical-align="middle"><img src="doc/fire.png" alt="drawing" width="20"/><img src="doc/fire.png" alt="drawing" width="30"/><img src="doc/fire.png" alt="drawing" width="20"/></p>
<!-- --><!-- --><!-- --><!-- --><!-- --><!-- --><!-- -->
<!-- --><!-- --><!-- --><!-- --><!-- --><!-- --><!-- -->
<!-- --><!-- --><!-- --><!-- --><!-- --><!-- --><!-- -->
<!-- --><!-- --><!-- --><!-- --><!-- --><!-- --><!-- -->

## 5 Sensors

> **_LiDAR:_** [awesome-LiDAR](https://github.com/szenergy/awesome-lidar#datasets), [awesome-point-cloud-analysis](https://github.com/Yochengliu/awesome-point-cloud-analysis), [awesome-point-cloud-deep-learning](https://github.com/dashidhy/awesome-point-cloud-deep-learning)

<details>
  <summary>Click to expand!</summary>

| Comp | Camera | LiDAR | RADAR |
| -- | -- | -- | -- | 
| 

</details>



