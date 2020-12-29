<p align="center" vertical-align="middle"><img src="doc/fire.png" alt="drawing" width="30"/><img src="doc/fire.png" alt="drawing" width="50"/><img src="doc/fire.png" alt="drawing" width="30"/></p>

# Self-driving cars perception notes
## Contents

1. [3D Object Detection](#3d-object-detection)
	+ [Evaluation metrics](#evaluation-metrics-3d-od)
	+ [Datasets](#datasets-3d-od)
	+ [Approaches](#Approaches-3d-od)
2. [Depth Estimation](#depth-estimation) 
	+ [Evaluation metrics](#evaluation-metrics-depth)
	+ [Datasets](#datasets-depth)
	+ [Approaches](#Approaches-depth)
3. [Segmentation](#segmentation)
	+ [Evaluation metrics](#evaluation-metrics-seg)
	+ [Datasets](#datasets-seg)
	+ [Approaches](#Approaches-seg)
4. [2D Object Detection](#2d-object-detection)
	+ [Evaluation metrics](#evaluation-metrics-2d-od)
	+ [Datasets](#datasets-2d-od)
	+ [Approaches](#Approaches-2d-od)
5. [Sensors](#sensors)

<p align="center" vertical-align="middle"><img src="doc/fire.png" alt="drawing" width="20"/><img src="doc/fire.png" alt="drawing" width="30"/><img src="doc/fire.png" alt="drawing" width="20"/></p>

## 3D Object Detection
### Evaluation metrics 3D OD

> **_Metrics:_**  AP 3D, AP BEV

> **_How to calculate:_** [[more]](3d_od/evaluation.md)

### Datasets 3D OD

> **_How to obtain 3D bounding box:_**

<details>
  <summary>Click to expand!</summary>

  | Ref | Highlight description |
  | -- | -- | 
  | KITTI </br>(3D OD) </br> [<kbd>CVPR 12</kbd>](http://www.cvlibs.net/publications/Geiger2012CVPR.pdf) [<kbd>IJRR 13</kbd>](http://ww.cvlibs.net/publications/Geiger2013IJRR.pdf) | ● Stereo (1224×368) + LiDAR 64 beams </br> ● Real dataset: 7481 training (splitted as 3DOP [<kbd>NIPS 15</kbd>](https://papers.nips.cc/paper/2015/file/6da37dd3139aa4d9aa55b8d237ec5d4a-Paper.pdf) into 3712 training & 3769 validation) & 7518 test samples </br> [[more]](dataset/kitti.md) | <!-- -->
  | Weather augmented </br>[<kbd>ICCV 19</kbd>](https://team.inria.fr/rits/computer-vision/weather-augment/) | | Weather Kitti and Weather Cityscapes | <!-- -->
  | Seeing Through Fog </br>[<kbd>CVPR 20</kbd>](https://www.cs.princeton.edu/~fheide/AdverseWeatherFusion/) [<kbd>ICCV 19</kbd>](https://github.com/gruberto/Gated2Depth) | <!-- -->
  | Canadian Adverse Driving Conditions </br>[<kbd>arXiv 20</kbd>](https://arxiv.org/pdf/2001.10117.pdf) | ●  56,000 camera images, 7,000 LiDAR sweeps, </br> ● Real dataset: 75 scenes of 50-100 frames each </br> ● Adverse weather driving conditions, including snow | 

</details>

### Approaches 3D OD
> **_Type 1:_** monocular (M), stereo (S), LiDAR 64 beams (L), LiDAR 4 beams (L4), RADAR (R)</br> 
> **_Type 2:_** supervised (sup), unsupervised (unsup), semi-supervised, (semi-sup), self-supervised (self-sup)

<details>
  <summary>Click to expand!</summary>

| Ref | Type | Data | Highlight description |
| :-- | :--: | :-- | :-- | 
| <p align="center" vertical-align="middle"><img src="doc/fire.png" alt="drawing" width="20"/>Monocular<img src="doc/fire.png" alt="drawing" width="20"/> </p> |<p align="center"> <img src="doc/fire.png" alt="drawing" width="20"/> </p>| <p align="center"> <img src="doc/fire.png" alt="drawing" width="20"/> </p> | <p align="center"> <img src="doc/fire.png" alt="drawing" width="20"/> </p> |<!-- -->
| Pseudo-LiDAR </br> [<kbd>CVPR 19</kbd>](https://openaccess.thecvf.com/content_CVPR_2019/papers/Wang_Pseudo-LiDAR_From_Visual_Depth_Estimation_Bridging_the_Gap_in_3D_CVPR_2019_paper.pdf) | M / sup | | ● Pipeline: </br> ● Contrib: convert depth into pseudo 3d point clouds|
| | | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
| Pseudo-LiDAR e2e </br>[<kbd>ICCV 19</kbd>](https://github.com/xinshuoweng/Mono3DPLiDAR) | M / sup | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
| | | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
| <p align="center"> <img src="doc/fire.png" alt="drawing" width="20"/>Binocular<img src="doc/fire.png" alt="drawing" width="20"/> </p> |<p align="center"> <img src="doc/fire.png" alt="drawing" width="20"/> </p>| <p align="center"> <img src="doc/fire.png" alt="drawing" width="20"/> </p> | <p align="center"> <img src="doc/fire.png" alt="drawing" width="20"/> </p> |<!-- -->
| Pseudo-LiDAR V3 E2E </br> [<kbd>CVPR 20</kbd>](https://openaccess.thecvf.com/content_CVPR_2020/papers/Qian_End-to-End_Pseudo-LiDAR_for_Image-Based_3D_Object_Detection_CVPR_2020_paper.pdf) | | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
| CG-Stereo </br> [<kbd>arXiv 20</kbd>](https://arxiv.org/pdf/2003.05505.pdf) | S / sup | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
| Pseudo-LiDAR </br> [<kbd>CVPR 19</kbd>](https://openaccess.thecvf.com/content_CVPR_2019/papers/Wang_Pseudo-LiDAR_From_Visual_Depth_Estimation_Bridging_the_Gap_in_3D_CVPR_2019_paper.pdf) | S / sup | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
| Pseudo-LiDAR ++</br> [<kbd>ICRL 21</kbd>](https://arxiv.org/pdf/1906.06310.pdf) | S / sup | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
| | | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
| | | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
| <p align="center"> <img src="doc/fire.png" alt="drawing" width="20"/>LiDAR<img src="doc/fire.png" alt="drawing" width="20"/> </p> |<p align="center"> <img src="doc/fire.png" alt="drawing" width="20"/> </p>| <p align="center"> <img src="doc/fire.png" alt="drawing" width="20"/> </p> | <p align="center"> <img src="doc/fire.png" alt="drawing" width="20"/> </p> |<!-- -->
| PointRCNN | | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
| | | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
| | | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
| <p align="center"><img src="doc/fire.png" alt="drawing" width="20"/>Fusion<img src="doc/fire.png" alt="drawing" width="20"/> </p> |<p align="center"> <img src="doc/fire.png" alt="drawing" width="20"/> </p>| <p align="center"> <img src="doc/fire.png" alt="drawing" width="20"/> </p> | <p align="center"> <img src="doc/fire.png" alt="drawing" width="20"/> </p> |<!-- -->
| Pseudo-LiDAR ++</br> [<kbd>ICRL 21</kbd>](https://arxiv.org/pdf/1906.06310.pdf) | S+L4 / sup | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
| | | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |
| | | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |

</details>

<p align="center" vertical-align="middle"><img src="doc/fire.png" alt="drawing" width="20"/><img src="doc/fire.png" alt="drawing" width="30"/><img src="doc/fire.png" alt="drawing" width="20"/></p>

## Depth Estimation
### Evaluation metrics depth

> **_Depth prediction (DP):_** takes only monocular/ stereo as input</br>
> **_Depth completion (DC):_** takes depth sensor (ex: LiDAR, RADAR) as input component</br>

> **_Metrics DP:_** Accu, SILog, sqErrorRel, absErrorRel, iRMSE, thresh δ</br>
> **_Metrics DC:_** Accu, iRMSE, iMAE, RMSE, MAE, thresh δ

> **_How to calculate:_** [[more]](depth_estimation/evaluation.md)



### Datasets depth
> **_How to obtain depth ground truth:_** 

<details>
  <summary>Click to expand!</summary>

| Ref | Highlight description |
| -- | -- | 
| KITTI (stereo) </br> [<kbd>CVPR 12</kbd>](http://www.cvlibs.net/publications/Geiger2012CVPR.pdf) [<kbd>IJRR 13</kbd>](http://ww.cvlibs.net/publications/Geiger2013IJRR.pdf) | ● Stereo (1224×368) + LiDAR 64 beams </br> ● Gth: projected LiDAR 64 beams pose for 11 odometry sequences </br> ● the 200 training images of KITTI stereo 2015 **overlap** with thevalidation images of KITTI object detection [[more]](dataset/kitti.md)| <!-- -->
| Scene Flow </br> [<kbd>CVPR 16</kbd>](https://openaccess.thecvf.com/content_cvpr_2016/papers/Mayer_A_Large_Dataset_CVPR_2016_paper.pdf) | ● Stereo (960x540) </br> ● Synthetic dataset: 35454 training & 4370 testing images </br> ● Gth: dense and elaborate disparity maps [[more]](dataset/sceneflow.md) | <!-- -->
| Cityscapes </br> [<kbd>CVPR 16</kbd>](https://www.cityscapes-dataset.com/citation/) | ● Stereo (1024×2048) </br> ● Gth: 22,973 stereo image pairs training  </br> ● Real dataset: 50 cities forseveral months </br> ● 5000 images with fine annotations and 20000 images  with coarse annotations [[more]](dataset/cityscapes.md)| <!-- -->

</details>

### Approaches depth

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

## Segmentation
### Evaluation metrics seg

> **_Metrics:_** 

> **_How to calculate:_** [[more]]()
### Datasets seg

<details>
  <summary>Click to expand!</summary>

  text

</details>

### Approaches seg
<details>
  <summary>Click to expand!</summary>

  Text here

</details>


<p align="center" vertical-align="middle"><img src="doc/fire.png" alt="drawing" width="20"/><img src="doc/fire.png" alt="drawing" width="30"/><img src="doc/fire.png" alt="drawing" width="20"/></p>

## 2D Object Detection
### Evaluation metrics 2D OD

> **_Metrics:_**  AP 2D

> **_How to calculate:_** [[more]](3d_od/evaluation.md)
### Datasets 2D OD

<details>
  <summary>Click to expand!</summary>

  text

</details>

### Approaches 2D OD
<details>
  <summary>Click to expand!</summary>

| Ref | Type | Data | Highlight description | 
| -- | -- | -- | -- | 
| OneNet </br> [<kbd>arXiv</kbd>](https://arxiv.org/pdf/2012.05780.pdf) | | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |

</details>

<p align="center" vertical-align="middle"><img src="doc/fire.png" alt="drawing" width="20"/><img src="doc/fire.png" alt="drawing" width="30"/><img src="doc/fire.png" alt="drawing" width="20"/></p>

## Sensors

> **_LiDAR:_** [awesome-LiDAR](https://github.com/szenergy/awesome-lidar#datasets), [awesome-point-cloud-analysis](https://github.com/Yochengliu/awesome-point-cloud-analysis), [awesome-point-cloud-deep-learning](https://github.com/dashidhy/awesome-point-cloud-deep-learning)

<details>
  <summary>Click to expand!</summary>

| Comp | Camera | LiDAR | RADAR |
| -- | -- | -- | -- | 
| 

</details>


<!--
### Adverse Weather Dataset
| Ref | Weather | Description | Task |
| -- | -- | -- | -- | 
| Weather augmented [[ICCV 2019]](https://team.inria.fr/rits/computer-vision/weather-augment/) | | Weather Kitti and Weather Cityscapes |
| Seeing Through Fog [[CVPR 2020]](https://www.cs.princeton.edu/~fheide/AdverseWeatherFusion/) [[ICCV 2019]](https://github.com/gruberto/Gated2Depth) |



### Simulation 
| Ref | Weather | Description | Task |
| -- | -- | -- | -- | 
| Seeing Through Fog [[CVPR 2020]](https://www.cs.princeton.edu/~fheide/AdverseWeatherFusion/) [[ICCV 2019]](https://github.com/gruberto/Gated2Depth) |



-->


<!-- 
1. quotes notes
> **_Type:_**

2. check box
* [ ] unchecked # [checkbox:unchecked]
* [x] checked   # [checkbox:checked]
* [X] checked   # [checkbox:checked]

3. A collapsible section with markdown
<details>
  <summary>Click to expand!</summary>
  text
</details>

4. list
<ul><li>item1</li><li>item2</li></ul>
5. point boucle ●


6. 
| Ref | Type | Data | Highlight description |
| :-- | :--: | -- | -- | 
| | | | ● Net: </br>● Pipeline: </br>● Loss: </br> ● Contrib: |

7. <p align="center" vertical-align="middle"> <img src="doc/fire.png" alt="drawing" width="20"/> </p>
-->
