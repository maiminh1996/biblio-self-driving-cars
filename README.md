# Self-driving cars paper notes
## Contents

1. [3D object detection (sorted by sensor type)](#3d-object-detection)
	+ [Evaluation metrics](#evaluation-metrics)
	+ [Datasets](#datasets)
	+ [Approaches](#Approaches)
	+ [Monocular-based methods (RGB)](#monocular-based-methods)
	+ [Binocular-based methods (stereo)](#binocular-based-methods)
	+ [Lidar-based methods](#lidar-based-methods)
	+ [Fusion-based methods](#fusion-based-methods)
	+ [Others](#others)
2. [Depth estimation/ Depth completion](#depth-estimation) 
	+ [Evaluation metrics](#evaluation-metrics)
	+ [Datasets](#datasets)
	+ [Approaches](#Approaches)
3. [Segmentation](#segmentation)
	+ [Evaluation metrics](#evaluation-metrics)
	+ [Datasets](#datasets)
	+ [Approaches](#Approaches)
4. [2D object detection](#2d-object-detection)
5. [Sensors](#sensors)

***


## 3D Dbject Detection
### Evaluation metrics

> **_Metrics:_**  AP 3D, AP BEV

> **_How to calculate:_** [[more]](3d_od/evaluation.md)

### Datasets
| Ref | Highlight description |
| -- | -- | 
| KITTI </br>(3D OD) </br> [[CVPR12]](http://www.cvlibs.net/publications/Geiger2012CVPR.pdf) [[IJRR13]](http://ww.cvlibs.net/publications/Geiger2013IJRR.pdf) | ● Stereo (1224×368) + LiDAR 64 beams </br> ● Real dataset: 7481 training (splitted as 3DOP [[NIPS15]](https://papers.nips.cc/paper/2015/file/6da37dd3139aa4d9aa55b8d237ec5d4a-Paper.pdf) into 3712 training & 3769 validation) & 7518 test samples </br> [[more]](dataset/kitti.md) | <!-- -->
| Weather augmented </br>[[ICCV19]](https://team.inria.fr/rits/computer-vision/weather-augment/) | | Weather Kitti and Weather Cityscapes | <!-- -->
| Seeing Through Fog </br>[[CVPR20]](https://www.cs.princeton.edu/~fheide/AdverseWeatherFusion/) [[ICCV19]](https://github.com/gruberto/Gated2Depth) | <!-- -->
| Canadian Adverse Driving Conditions </br>[[arXiv20]](https://arxiv.org/pdf/2001.10117.pdf) | ●  56,000 camera images, 7,000 LiDAR sweeps, </br> ● Real dataset: 75 scenes of 50-100 frames each </br> ● Adverse weather driving conditions, including snow | 
<!--
### Monocular-based methods

| Ref  | Sensor | Object Type | Sensing Modality Representations and Processing | Net | How to generate Region Proposals (RP) | When to fuse | Fusion Operation and Method | Fusion Level | Data | Note |
| -- |:--:| :--:| --:| --:| --:| --:| --:| --: | --:| --:|
| Pseudo-LiDAR, [[CVPR 2019]](https://openaccess.thecvf.com/content_CVPR_2019/papers/Wang_Pseudo-LiDAR_From_Visual_Depth_Estimation_Bridging_the_Gap_in_3D_CVPR_2019_paper.pdf)| [[more](paper_notes/test.md)] | 
| Pseudo-LiDAR e2e [[ICCV 2019]](https://github.com/xinshuoweng/Mono3DPLiDAR) |

### Binocular-based methods

| Ref | Sensors | Object Type | Sensing Modality Representations and Processing | Network Pipeline | How to generate Region Proposals (RP) | When to fuse | Fusion Operation and Method | Fusion Level | Datasets | Notes |
| -- |:--:| :--:| --:| --:| --:| --:| --:| --: | --:| --:|
| CG-Stereo  [[arXiv 2020]](https://arxiv.org/pdf/2003.05505.pdf) |
| Pseudo-LiDAR, [[CVPR 2019]](https://openaccess.thecvf.com/content_CVPR_2019/papers/Wang_Pseudo-LiDAR_From_Visual_Depth_Estimation_Bridging_the_Gap_in_3D_CVPR_2019_paper.pdf)| [[more](paper_notes/test.md)] | 
| Pseudo-LiDAR V3 E2E [[CVPR 2020]](https://openaccess.thecvf.com/content_CVPR_2020/papers/Qian_End-to-End_Pseudo-LiDAR_for_Image-Based_3D_Object_Detection_CVPR_2020_paper.pdf) |

### LiDAR-based methods

### Fusion-based methods

### Others
| Ref  | Sensors | Object Type | Sensing Modality Representations and Processing | Network Pipeline | How to generate Region Proposals (RP) | When to fuse | Fusion Operation and Method | Fusion Level | Datasets |
| -- |:--:| :--:| --:| --:| --:| --:| --:| --: | --:|
| Pseudo LiDAR ++, [[ICRL 2021]](https://arxiv.org/pdf/1906.06310.pdf)| Stereo, Simulation LiDAR 4 beams |

***
-->


## Depth estimation
### Evaluation metrics

> **_Depth prediction (DP):_** takes only monocular/ stereo as input</br>
> **_Depth completion (DC):_** takes depth sensor (ex: LiDAR, RADAR) as input component</br>

> **_Metrics DP:_** Accu, SILog, sqErrorRel, absErrorRel, iRMSE, thresh δ</br>
> **_Metrics DC:_** Accu, iRMSE, iMAE, RMSE, MAE, thresh δ

> **_How to calculate:_** [[more]](depth_estimation/evaluation.md)



### Datasets
> **_How to obtain depth ground truth:_** 

| Ref | Highlight description |
| -- | -- | 
| KITTI (stereo) </br> [[CVPR12]](http://www.cvlibs.net/publications/Geiger2012CVPR.pdf) [[IJRR13]](http://ww.cvlibs.net/publications/Geiger2013IJRR.pdf) | ● Stereo (1224×368) + LiDAR 64 beams </br> ● Gth: projected LiDAR 64 beams pose for 11 odometry sequences </br> ● the 200 training images of KITTI stereo 2015 **overlap** with thevalidation images of KITTI object detection [[more]](dataset/kitti.md)| <!-- -->
| Scene Flow </br> [[CVPR16]](https://openaccess.thecvf.com/content_cvpr_2016/papers/Mayer_A_Large_Dataset_CVPR_2016_paper.pdf) | ● Stereo (960x540) </br> ● Synthetic dataset: 35454 training & 4370 testing images </br> ● Gth: dense and elaborate disparity maps [[more]](dataset/sceneflow.md) | <!-- -->
| Cityscapes </br> [[CVPR16]](https://www.cityscapes-dataset.com/citation/) | ● Stereo (1024×2048) </br> ● Gth: 22,973 stereo image pairs training  </br> ● Real dataset: 50 cities forseveral months </br> ● 5000 images with fine annotations and 20000 images  with coarse annotations [[more]](dataset/cityscapes.md)| <!-- -->

### Approaches

> **_Type 1:_** monocular (M), stereo (S), LiDAR (L), RADAR (R)</br> 
> **_Type 2:_** supervised (sup), unsupervised (unsup), semi-supervised, (semi-sup), self-supervised (self-sup)


| Ref | Sen+Type | Data | Net | Loss | Note |

| Ref | Type | Data | Highlight description |
| :-- | :--: | -- | -- | 
| Eigen et al [[NIPS14]](https://arxiv.org/pdf/1406.2283.pdf) | M / sup | KITTI | ● Loss: [L2 loss](loss_problem.md)|
| DORN </br> [[CVPR18]](https://openaccess.thecvf.com/content_cvpr_2018/papers/Fu_Deep_Ordinal_Regression_CVPR_2018_paper.pdf) | M / sup | KITTI | |  <!-- -->| Discretized depth bins > direct regression </br> binary classification 80 bins (Pixels with distance>80m) [[more]](https://github.com/patrick-llgc/Learning-Deep-Learning/blob/master/paper_notes/dorn.md) |
| FAL </br> [[NIPS20]](https://proceedings.neurips.cc/paper/2020/file/951124d4a093eeae83d9726a20295498-Paper.pdf) | M / self-sup | KITTI | | Occlusion-free reconstruction loss |  <!-- -->
| PSMNet [[CVPR18]](https://openaccess.thecvf.com/content_cvpr_2018/papers/Chang_Pyramid_Stereo_Matching_CVPR_2018_paper.pdf) | S / sup | ● KITTI </br> ● Scene Flow 

<!--



## Segmentation
### Approaches

***

-->

## 2D object detection
### Evaluation metrics

> **_Metrics:_**  AP 2D

> **_How to calculate:_** [[more]](3d_od/evaluation.md)

| Ref | Des |
| -- | -- |
| OneNet </br> [[arXiv]](https://arxiv.org/pdf/2012.05780.pdf) | |

## Sensors
> **_LiDAR:_** [awesome-LiDAR](https://github.com/szenergy/awesome-lidar#datasets), [awesome-point-cloud-analysis](https://github.com/Yochengliu/awesome-point-cloud-analysis), [awesome-point-cloud-deep-learning](https://github.com/dashidhy/awesome-point-cloud-deep-learning)

| Comp | Camera | LiDAR | RADAR |
| -- | -- | -- | -- | 
| 


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

***

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
  
  ## Heading
  1. A numbered
  2. list
     * With some
     * Sub bullets
</details>

4. list
<ul><li>item1</li><li>item2</li></ul>
5. point boucle ●
-->