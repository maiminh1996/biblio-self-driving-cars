<!-- CSS -->
<link rel="stylesheet" style="text/css" href="../styles.css">
<!--     -->

## Depth estimation/ pseudo 3D point cloud limitations
- [Depth gth](#depth-gth)
- [long tail](#long-tail)
- [occlusion](#occlusion)
- [depth errors](#depth-errors)
- [uncertainty and confidence maps](#uncertainty-and-confidence-maps)
- [sensors degraded](#sensors-degraded)
- [smoothless depth](#smoothless-depth)
- [Depth Uncertainty](#depth-uncertainty)


### Depth gth

Hard to obtain

### Long tail

Pseudo-lidar is the noise (i.e., depth inaccuracies, long tails) in the reprojected 3d point cloud due to blurry boundaries

ref: [Monocular 3D Object Detection with Pseudo-LiDAR Point Cloud](https://arxiv.org/pdf/1903.09847.pdf)

[FusionMapping: Learning Depth Prediction with Monocular Images and 2D Laser Scans](https://arxiv.org/pdf/1912.00096.pdf)

[Learning-Deep-Learning/ Monocular 3D Object Detection with Pseudo-LiDAR Point Cloud](https://patrick-llgc.github.io/Learning-Deep-Learning/paper_notes/pseudo_lidar_e2e.html)

| LiDAR 64 beam | Depth map generated bt NLSPN |
| -- | -- |
| ![](../doc/lidar_64.png) | ![](../doc/longtail.png) |

### occlusion

[Self-Supervised Scene De-occlusion](https://arxiv.org/abs/2004.02788)


### depth errors

how to remove

### uncertainty and confidence maps

[Conf-Net](https://github.com/hekmak/Conf-net)

### sensors degraded

bad weather

### smoothless depth

Continuous Depth, smoothless depth

### Depth Uncertainty
