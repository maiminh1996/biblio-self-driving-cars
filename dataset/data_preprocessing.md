## LiDAR preprocessing

[<kbd>Sensors 20</kbd> Large-Scale Place Recognition Based onCamera-LiDAR Fused Descriptor](https://www.mdpi.com/1424-8220/20/10/2870/pdf)

- the **quantity of points** in each point cloud is not the same, so we need to **resample** the points in a fixed number
- the **ground points** are **redundant** to form a discriminative descriptor utilizing the structure information of eachframe, reduce the **consumption** of the memory --> how to remove [Fast Segmentation of 3D Point Clouds for Ground Vehicles](https://sci-hub.do/10.1109/ivs.2010.5548059)
    - use downsample API in the PCL Library
    - the leaf size which represents the size of grid cells in the point cloud is set to(0.3, 0.3, 0.1)
    - randomly pickN=6000points as our input of LiDAR to give a slight disturbance to the pcl

![](../doc/resample_pcl.png)

## Downsample LiDAR 64 beams

[<kbd>ICRL 20</kbd> Pseudo-LiDAR ++](https://arxiv.org/pdf/1906.06310.pdf) (Downsample to LiDAR 4 beams) [[Notes](pseudo_lidar++.md)]

![](../doc/downsample_4_2.png)

[<kbd>CRL 20</kbd> Robust Semi-Supervised Monocular Depth Estimation with Reprojected Distances](http://proceedings.mlr.press/v100/guizilini20a/guizilini20a.pdf)

![](../doc/downsample_32_16_8_4.png)

[<kbd>3DV 18</kbd> Sparse and Dense Data with CNNs:Depth Completion and Semantic Segmentation](https://arxiv.org/pdf/1808.00769.pdf)

![](../doc/sparded_subsample.png)

[<kbd>CVPR 19</kbd> Depth Coefficients for Depth Completion](https://arxiv.org/pdf/1903.05421.pdf) [[code](https://github.com/imransai/Depth-Coefficients-4-DepthCompletion/tree/050855a1b616a60eb3af36450f2d2a7edac92f0c)]

[<kbd>arXiv 19</kbd> RefinedMPL: Refined Monocular PseudoLiDAR for 3D Object Detection in Autonomous Driving](https://arxiv.org/abs/1911.09712) Downsampler: downsample uniformly within different distance bins.

[Lidar_Line_Downsample](https://github.com/chengtianle1997/Lidar_Line_Downsample/tree/df95edc73d8d1030a1a4e21d1ba2b46108701dd1)