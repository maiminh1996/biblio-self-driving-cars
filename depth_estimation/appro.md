## Depth Estimation/ Approaches

> **_Type 1:_** monocular (M), stereo (S), LiDAR (L), RADAR (R)<br/> 
> **_Type 2:_** supervised (sup), unsupervised (unsup), semi-supervised, (semi-sup), self-supervised (self-sup)

| Ref | Type | Data | Highlight description |
| -- | :--: | :--: | -- | 
| Eigen et al <br/> [<kbd>NIPS 14</kbd>](https://arxiv.org/pdf/1406.2283.pdf) | M / sup | KITTI | ● Loss: [L2 loss](../loss_problem.md)|
| DORN <br/> [<kbd>CVPR 18</kbd>](https://openaccess.thecvf.com/content_cvpr_2018/papers/Fu_Deep_Ordinal_Regression_CVPR_2018_paper.pdf) | M / sup | KITTI | Discretized depth bins > direct regression <br/> binary classification 80 bins (Pixels with distance>80m) [[more]](https://github.com/patrick-llgc/Learning-Deep-Learning/blob/master/paper_notes/dorn.md) |
| FAL <br/> [<kbd>NIPS 20</kbd>](https://proceedings.neurips.cc/paper/2020/file/951124d4a093eeae83d9726a20295498-Paper.pdf) | M / self-sup | KITTI | Occlusion-free reconstruction loss |  <!-- -->
| PSMNet <br/> [<kbd>CVPR 18</kbd>](https://openaccess.thecvf.com/content_cvpr_2018/papers/Chang_Pyramid_Stereo_Matching_CVPR_2018_paper.pdf) | S / sup | ● KITTI <br/> ● Scene Flow 
