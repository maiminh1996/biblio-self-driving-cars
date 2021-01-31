<!-- CSS -->
<link rel="stylesheet" style="text/css" href="../styles.css">
<!--     -->

## 3D Object Detection/ Datasets

> **_How to obtain 3D bounding box:_**

- [Simulation bad weather theory](../dataset/simulation.md)

- [Downsample LiDAR 64beams](../dataset/data_preprocessing.md)

- [Synchronization and Calibration between LiDAR and Camera](https://yuhuang-63908.medium.com/deep-learning-based-time-synchronization-and-calibration-between-lidar-and-camera-3e87865edf7f)

Ref | Highlight description
-- | --
KITTI (3D OD) [<kbd>CVPR 12</kbd>](http://www.cvlibs.net/publications/Geiger2012CVPR.pdf) [<kbd>IJRR 13</kbd>](http://ww.cvlibs.net/publications/Geiger2013IJRR.pdf) | ● Stereo (1224×368) + LiDAR 64 beams <br/> ● Real dataset: 7481 training (splitted as 3DOP [<kbd>NIPS 15</kbd>](https://papers.nips.cc/paper/2015/file/6da37dd3139aa4d9aa55b8d237ec5d4a-Paper.pdf) into 3712 training & 3769 validation) & 7518 test samples [[Notes](../dataset/kitti.md)] <!-- -->
KITTI-Object-Depth (KOD) [<kbd>AAAI 20</kbd>](https://arxiv.org/pdf/1909.07701.pdf) | Collect the corresponding gth depth map (11 frame) for each image in KITTI (3D OD) training set [[Notes](foresee.md)]<!-- -->
Virtual KITTI | 
Weather augmented [<kbd>ICCV 19</kbd>](https://team.inria.fr/rits/computer-vision/weather-augment/) | ● Weather augmentation of [Kitti](../dataset/kitti.md) & [Cityscapes](../dataset/cityscapes.md)  <br/>●  For each sequence, 7+ rain levels (from dizzle to storm conditions) & 7 fog intensities (from light to dense fog)<br/>● Simulation rain or fog (based on Sakaridis et al. [paper](https://www.trace.ethz.ch/publications/2019/foggy_synscapes/)) [[Notes](../dataset/weather_augmented.md)] <!-- -->
Seeing Through Fog [<kbd>CVPR 20</kbd>](https://www.cs.princeton.edu/~fheide/AdverseWeatherFusion/) [<kbd>ICCV 19</kbd>](https://github.com/gruberto/Gated2Depth) | ● Stereo (1920x1024) + Gated cam + radar + LiDAR (HDL64 & VL32) + FIR cam <br/> ● Real dataset: rare scenarios (heavy fog, heavy snow & severe rain); 10000 km in northern Europe<br/> ● Simulation fog (based on Sakaridis et al. [paper](https://www.trace.ethz.ch/publications/2019/foggy_synscapes/)) [[Notes](../dataset/seeing_through_fog.md)]<!-- -->
Canadian Adverse Driving Conditions [<kbd>arXiv 20</kbd>](https://arxiv.org/pdf/2001.10117.pdf) | ●  56000 camera images, 7000 LiDAR sweeps, <br/> ● Real dataset: 75 scenes of 50-100 frames each <br/> ● Adverse weather driving conditions, including snow <!-- -->
Adverse Weather Dataset <kbd>under review</kbd> |  http://sar-lab.net/adverse-weather-dataset/
