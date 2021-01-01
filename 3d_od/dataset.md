## 3D Object Detection/ Datasets

> **_How to obtain 3D bounding box:_**

Ref | Highlight description
-- | --
KITTI (3D OD) [<kbd>CVPR 12</kbd>](http://www.cvlibs.net/publications/Geiger2012CVPR.pdf) [<kbd>IJRR 13</kbd>](http://ww.cvlibs.net/publications/Geiger2013IJRR.pdf) | ● Stereo (1224×368) + LiDAR 64 beams <br/> ● Real dataset: 7481 training (splitted as 3DOP [<kbd>NIPS 15</kbd>](https://papers.nips.cc/paper/2015/file/6da37dd3139aa4d9aa55b8d237ec5d4a-Paper.pdf) into 3712 training & 3769 validation) & 7518 test samples [<img src="../doc/100.png" width="95">](../dataset/kitti.md) <!-- -->
KITTI-Object-Depth (KOD) [<kbd>AAAI 20</kbd>](https://arxiv.org/pdf/1909.07701.pdf) | Collect the corresponding gth depth map (11 frame) for each image in KITTI (3D OD) training set [<img src="../doc/0.png" width="95">](foresee.md)<!-- -->
Weather augmented [<kbd>ICCV 19</kbd>](https://team.inria.fr/rits/computer-vision/weather-augment/) | ● Weather augmentation of Kitti & Cityscapes  <br/>●  For each sequence, 7+ rain levels (from dizzle to storm conditions) & 7 fog intensities (from light to dense fog) [<img src="../doc/0.png" width="95">](../dataset/weather_augmented.md) <!-- -->
Seeing Through Fog [<kbd>CVPR 20</kbd>](https://www.cs.princeton.edu/~fheide/AdverseWeatherFusion/) [<kbd>ICCV 19</kbd>](https://github.com/gruberto/Gated2Depth) | <!-- -->
Canadian Adverse Driving Conditions [<kbd>arXiv 20</kbd>](https://arxiv.org/pdf/2001.10117.pdf) | ●  56000 camera images, 7000 LiDAR sweeps, <br/> ● Real dataset: 75 scenes of 50-100 frames each <br/> ● Adverse weather driving conditions, including snow <!-- -->
