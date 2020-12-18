# Self-driving cars paper notes: 
## Contents

1. [3D object detection (sorted by sensor type)](#3d-object-detection)
	+ [Monocular-based methods (RGB)](#monocular-based-methods)
	+ [Binocular-based methods (stereo)](#binocular-based-methods)
	+ [Lidar-based methods](#lidar-based-methods)
	+ [Fusion-based methods](#fusion-based-methods)
	+ [Others](#others)
2. [Segmentation](#segmentation)
3. [Datasets](#datasets)

***
##3D Dbject Detection
### Monocular-based methods

| Ref  | Sensors | Object Type | Sensing Modality Representations and Processing | Network Pipeline | How to generate Region Proposals (RP) | When to fuse | Fusion Operation and Method | Fusion Level | Datasets | Notes |
| -- |:--:| :--:| --:| --:| --:| --:| --:| --: | --:| --:|
| Pseudo-LiDAR e2e [[ICCV 2019]](https://github.com/xinshuoweng/Mono3DPLiDAR) |
| Pseudo-LiDAR, [[CVPR 2019]](https://openaccess.thecvf.com/content_CVPR_2019/papers/Wang_Pseudo-LiDAR_From_Visual_Depth_Estimation_Bridging_the_Gap_in_3D_CVPR_2019_paper.pdf)| [[Notes](paper_notes/test.md)] | 



### Binocular-based methods
| Ref  | Sensors | Object Type | Sensing Modality Representations and Processing | Network Pipeline | How to generate Region Proposals (RP) | When to fuse | Fusion Operation and Method | Fusion Level | Datasets | Notes |
| -- |:--:| :--:| --:| --:| --:| --:| --:| --: | --:| --:|
| CG-Stereo [[arXiv 2020]](https://arxiv.org/pdf/2003.05505.pdf) |
| Pseudo-LiDAR V3 E2E [[CVPR 2020]](https://openaccess.thecvf.com/content_CVPR_2020/papers/Qian_End-to-End_Pseudo-LiDAR_for_Image-Based_3D_Object_Detection_CVPR_2020_paper.pdf) |
| Pseudo-LiDAR, [[CVPR 2019]](https://openaccess.thecvf.com/content_CVPR_2019/papers/Wang_Pseudo-LiDAR_From_Visual_Depth_Estimation_Bridging_the_Gap_in_3D_CVPR_2019_paper.pdf)| [[Notes](paper_notes/test.md)] | 



### LiDAR-based methods

### Fusion-based methods
### Others
| Ref  | Sensors | Object Type | Sensing Modality Representations and Processing | Network Pipeline | How to generate Region Proposals (RP) | When to fuse | Fusion Operation and Method | Fusion Level | Datasets |
| -- |:--:| :--:| --:| --:| --:| --:| --:| --: | --:|
| Pseudo LiDAR ++, [[ICRL 2021]](https://arxiv.org/pdf/1906.06310.pdf)| Stereo, Simulation LiDAR 4 beams |

***
## Segmentation

***
## Datasets
### Popular Datasets
| Ref | Description | Task |
| -- | -- | -- | 
| KITTI [[CVPR 2012]](http://www.cvlibs.net/publications/Geiger2012CVPR.pdf), [[IJRR 2013]](http://ww.cvlibs.net/publications/Geiger2013IJRR.pdf)

### Adverse Weather Dataset
| Ref | Weather | Description | Task |
| -- | -- | -- | -- | 
| Seeing Through Fog [[CVPR 2020]](https://www.cs.princeton.edu/~fheide/AdverseWeatherFusion/) [[ICCV 2019]](https://github.com/gruberto/Gated2Depth) |
| Weather augmented [[ICCV 2019]](https://team.inria.fr/rits/computer-vision/weather-augment/) | | Weather Kitti and Weather Cityscapes |


### Simulation 
| Ref | Weather | Description | Task |
| -- | -- | -- | -- | 
| Seeing Through Fog [[CVPR 2020]](https://www.cs.princeton.edu/~fheide/AdverseWeatherFusion/) [[ICCV 2019]](https://github.com/gruberto/Gated2Depth) |

***

