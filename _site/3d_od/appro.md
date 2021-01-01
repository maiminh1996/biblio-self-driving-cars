
## 3D Object Detection/ Approaches

> **_Type 1:_** monocular (M), stereo (S), LiDAR 64 beams (L), LiDAR 4 beams (L4), RADAR (R)<br/> 
> **_Type 2:_** supervised (sup), unsupervised (unsup), semi-supervised, (semi-sup), self-supervised (self-sup)

| Ref | Type | Data | Highlight description |
| -- | :--: | :-- | -- | 
|  | <img src="doc/fire.png" alt="drawing" width="20"/>| <img src="doc/fire.png" alt="drawing" width="20"/> |  |<!-- -->
| Pseudo-LiDAR <br/> [<kbd>CVPR 19</kbd>](https://openaccess.thecvf.com/content_CVPR_2019/papers/Wang_Pseudo-LiDAR_From_Visual_Depth_Estimation_Bridging_the_Gap_in_3D_CVPR_2019_paper.pdf) | M / sup | KITTI | ● Pipeline: Depth estimator ➔ convert into pseudo pcl ➔ LiDAR-based detector <br/> ● Contrib: Convert depth into pseudo 3d point clouds [<img src="../doc/100.png" width="95">](pseudo_lidar.md) |
| | | | ● Net: <br/>● Pipeline: <br/>● Loss: <br/> ● Contrib: |
| Pseudo-LiDAR e2e <br/>[<kbd>ICCV 19</kbd>](https://github.com/xinshuoweng/Mono3DPLiDAR) | M / sup | | ● Net: <br/>● Pipeline: <br/>● Loss: <br/> ● Contrib: |
| | | | ● Net: <br/>● Pipeline: <br/>● Loss: <br/> ● Contrib: |
|  | <img src="doc/fire.png" alt="drawing" width="20"/>| <img src="doc/fire.png" alt="drawing" width="20"/> |  |<!-- -->
| Pseudo-LiDAR V3 E2E <br/> [<kbd>CVPR 20</kbd>](https://openaccess.thecvf.com/content_CVPR_2020/papers/Qian_End-to-End_Pseudo-LiDAR_for_Image-Based_3D_Object_Detection_CVPR_2020_paper.pdf) | | | ● Net: <br/>● Pipeline: <br/>● Loss: <br/> ● Contrib: |
| CG-Stereo <br/> [<kbd>arXiv 20</kbd>](https://arxiv.org/pdf/2003.05505.pdf) | S / sup | | ● Net: <br/>● Pipeline: <br/>● Loss: <br/> ● Contrib: |
| Pseudo-LiDAR <br/> [<kbd>CVPR 19</kbd>](https://openaccess.thecvf.com/content_CVPR_2019/papers/Wang_Pseudo-LiDAR_From_Visual_Depth_Estimation_Bridging_the_Gap_in_3D_CVPR_2019_paper.pdf) | S / sup | | [<img src="../doc/100.png" width="95">](pseudo_lidar.md) |
| Pseudo-LiDAR ++<br/> [<kbd>ICRL 20</kbd>](https://arxiv.org/pdf/1906.06310.pdf) | S / sup | | ● Net: <br/>● Pipeline: <br/>● Loss: <br/> ● Contrib: [<img src="../doc/0.png" width="95">](pseudo_lidar++.md) |
| | | | ● Net: <br/>● Pipeline: <br/>● Loss: <br/> ● Contrib: |
| | | | ● Net: <br/>● Pipeline: <br/>● Loss: <br/> ● Contrib:  |
|  | <img src="doc/fire.png" alt="drawing" width="20"/>| <img src="doc/fire.png" alt="drawing" width="20"/> |  |<!-- -->
| PointRCNN | | | ● Net: <br/>● Pipeline: <br/>● Loss: <br/> ● Contrib: |
| | | | ● Net: <br/>● Pipeline: <br/>● Loss: <br/> ● Contrib: |
| | | | ● Net: <br/>● Pipeline: <br/>● Loss: <br/> ● Contrib: |
|  | <img src="doc/fire.png" alt="drawing" width="20"/>| <img src="doc/fire.png" alt="drawing" width="20"/> |  |<!-- -->
| Pseudo-LiDAR ++<br/> [<kbd>ICRL 20</kbd>](https://arxiv.org/pdf/1906.06310.pdf) | S+L4 / sup | | ● Net: <br/>● Pipeline: <br/>● Loss: <br/> ● Contrib: [<img src="../doc/0.png" width="95">](pseudo_lidar++.md) |
| | | | ● Net: <br/>● Pipeline: <br/>● Loss: <br/> ● Contrib: |
| | | | ● Net: <br/>● Pipeline: <br/>● Loss: <br/> ● Contrib: |
