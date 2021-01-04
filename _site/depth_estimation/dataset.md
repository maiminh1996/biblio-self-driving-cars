<!-- CSS -->
<link rel="stylesheet" style="text/css" href="../styles.css">
<!--     -->

## Depth Estimation/ Datasets
> **_How to obtain depth ground truth:_** 


| Ref | Highlight description |
| -- | -- | 
| KITTI (stereo) <br/> [<kbd>CVPR 12</kbd>](http://www.cvlibs.net/publications/Geiger2012CVPR.pdf) [<kbd>IJRR 13</kbd>](http://ww.cvlibs.net/publications/Geiger2013IJRR.pdf) | ● Stereo (1224×368) + LiDAR 64 beams <br/> ● Gth: projected LiDAR 64 beams pose for 11 odometry sequences <br/> ● the 200 training images of KITTI stereo 2015 **overlap** with the validation images of KITTI OD [<img src="../doc/100.png" width="95">](../dataset/kitti.md)| <!-- -->
| Scene Flow <br/> [<kbd>CVPR 16</kbd>](https://openaccess.thecvf.com/content_cvpr_2016/papers/Mayer_A_Large_Dataset_CVPR_2016_paper.pdf) | ● Stereo (960x540) <br/> ● Synthetic dataset: 35454 training & 4370 testing images <br/> ● Gth: dense and elaborate disparity maps [<img src="../doc/25.png" width="95">](../dataset/sceneflow.md) | <!-- <img src="doc/25.png" width="95">-->
| Cityscapes <br/> [<kbd>CVPR 16</kbd>](https://www.cityscapes-dataset.com/citation/) | ● Stereo (1024×2048) <br/> ● Gth: 22,973 stereo image pairs training  <br/> ● Real dataset: 50 cities forseveral months <br/> ● 5000 images with fine annotations and 20000 images  with coarse annotations [<img src="../doc/25.png" width="95">](../dataset/cityscapes.md)| <!-- -->
