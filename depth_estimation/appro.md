<!-- CSS -->
<link rel="stylesheet" style="text/css" href="../styles.css">
<!--     -->

## Depth Estimation/ Approaches

- [Monocular (depth prediction)](#monocular)
- [Binocular (depth prediction)](#binocular)
- [Depth completion](#depth-completion)

> **_Type 1:_** monocular (M), stereo (S), LiDAR (L), RADAR (R)<br/> 
> **_Type 2:_** supervised (sup), unsupervised (unsup), semi-supervised, (semi-sup), self-supervised (self-sup)

Other sources:
- [Making a Pseudo LiDAR With Cameras and Deep Learning](https://medium.com/swlh/making-a-pseudo-lidar-with-cameras-and-deep-learning-e8f03f939c5f)
- [extract the colors from the image to add to the pcl: XYZRGB --> Meshlab](https://medium.com/analytics-vidhya/depth-sensing-and-3d-reconstruction-512ed121aa60)

<details>
  <summary>General notes!</summary>

- Ref:  <a href="https://medium.com/swlh/making-a-pseudo-lidar-with-cameras-and-deep-learning-e8f03f939c5f">Depth normalization</a><br/> we need to penalize the things that are ‘closer’ more than the things that are far away, because for planning, closer objects would matter more mostly. --> <b>Depth normalization </b> is the idea taking the inverse of the depth-map<br/>
depthNormalized = maxDepth / original_depth_map<br/>;where maxDepth is the max depth value in the whole dataset

</details>

https://github.com/alexklwong/awesome-state-of-depth-completion

## Monocular

#### Supervised

[<kbd>NIPS 14</kbd> Eigen et al](https://arxiv.org/pdf/1406.2283.pdf)

[<kbd>CVPR 18</kbd> DORN](https://openaccess.thecvf.com/content_cvpr_2018/papers/Fu_Deep_Ordinal_Regression_CVPR_2018_paper.pdf) (Discretized depth bins > direct regression; binary classification 80 bins (Pixels with distance>80m)) [[Notes]](https://github.com/patrick-llgc/Learning-Deep-Learning/blob/master/paper_notes/dorn.md)

#### Unsupervised

#### Semi-supervised

#### Self-supervised

[<kbd>NIPS 20</kbd> FAL](https://proceedings.neurips.cc/paper/2020/file/951124d4a093eeae83d9726a20295498-Paper.pdf) (Occlusion-free reconstruction loss)

## Binocular

#### Supervised

[<kbd>CVPR 18</kbd> PSMNet](https://openaccess.thecvf.com/content_cvpr_2018/papers/Chang_Pyramid_Stereo_Matching_CVPR_2018_paper.pdf) () [[Notes](psmnet.md)]

#### Unsupervised

#### Semi-supervised

#### Self-supervised


## Depth completion

#### Supervised

[<kbd>CVPR 19</kbd> DeepLiDAR](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwifkZCW6oDuAhWMURUIHTqwCtYQFjACegQIAxAC&url=http%3A%2F%2Fopenaccess.thecvf.com%2Fcontent_CVPR_2019%2Fpapers%2FQiu_DeepLiDAR_Deep_Surface_Normal_Guided_Depth_Prediction_for_Outdoor_Scene_CVPR_2019_paper.pdf&usg=AOvVaw1bPN7MFbPOOt4Bf7yynGPu) () [[Notes](deeplidar.md)]

#### Unsupervised

#### Semi-supervised

#### Self-supervised

