## Depth Estimation/ Approaches

> **_Type 1:_** monocular (M), stereo (S), LiDAR (L), RADAR (R)<br/> 
> **_Type 2:_** supervised (sup), unsupervised (unsup), semi-supervised, (semi-sup), self-supervised (self-sup)

> **_Other sources:_** [Making a Pseudo LiDAR With Cameras and Deep Learning](https://medium.com/swlh/making-a-pseudo-lidar-with-cameras-and-deep-learning-e8f03f939c5f)

<details>
  <summary>General notes!</summary>

- Ref:  <a href="https://medium.com/swlh/making-a-pseudo-lidar-with-cameras-and-deep-learning-e8f03f939c5f">Depth normalization</a><br/> we need to penalize the things that are ‘closer’ more than the things that are far away, because for planning, closer objects would matter more mostly. --> <b>Depth normalization </b> is the idea taking the inverse of the depth-map<br/>
depthNormalized = maxDepth / original_depth_map<br/>;where maxDepth is the max depth value in the whole dataset

</details>



| Ref | Type | Data | Highlight description |
| -- | :--: | :--: | -- | 
| Eigen et al <br/> [<kbd>NIPS 14</kbd>](https://arxiv.org/pdf/1406.2283.pdf) | M / sup | KITTI | ● Loss: [L2 loss](../loss_problem.md)|
| DORN <br/> [<kbd>CVPR 18</kbd>](https://openaccess.thecvf.com/content_cvpr_2018/papers/Fu_Deep_Ordinal_Regression_CVPR_2018_paper.pdf) | M / sup | KITTI | Discretized depth bins > direct regression <br/> binary classification 80 bins (Pixels with distance>80m) [[more]](https://github.com/patrick-llgc/Learning-Deep-Learning/blob/master/paper_notes/dorn.md) |
| FAL <br/> [<kbd>NIPS 20</kbd>](https://proceedings.neurips.cc/paper/2020/file/951124d4a093eeae83d9726a20295498-Paper.pdf) | M / self-sup | KITTI | Occlusion-free reconstruction loss |  <!-- -->
| PSMNet <br/> [<kbd>CVPR 18</kbd>](https://openaccess.thecvf.com/content_cvpr_2018/papers/Chang_Pyramid_Stereo_Matching_CVPR_2018_paper.pdf) | S / sup | ● KITTI <br/> ● Scene Flow 
