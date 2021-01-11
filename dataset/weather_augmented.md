<!-- CSS -->
<link rel="stylesheet" style="text/css" href="../styles.css">
<!--     -->

## Weather augmented <img src="../doc/0.png" width="95">
### [<kbd>IJCV 2020</kbd> Rain rendering for evaluating and improving robustness to bad weather](https://arxiv.org/pdf/2009.03683.pdf)
### [<kbd>ICCV 2019</kbd> Physics-Based Rendering for Improving Robustness to Rain](https://team.inria.fr/rits/files/2020/11/2019-iccv-weatheraugment.pdf)

[Link to web project](https://team.inria.fr/rits/computer-vision/weather-augment/): Dev toolkit, Weather Kitti, Weather Cityscapes


| Category | Description |
| :--: | -- |
| Overall impression | weather augmented Kitti and Cityscapes dataset (only for image) |
| Inputs | All together, dataset contains 390k+ images | 
| Scenes | Based on Kitti and on Cityscapes |
| Condition | Weather augmentation on Kitti OD (7481) and Cityscapes for segmentation (2995) <br/> ● 7 types of rain (from dizzle to storm conditions) <br/>R = {0, 1, 5, 17, 25, 50, 100, 200} mm/ hr <br/> ● 7 type of fog (from light to dense fog) <br/>Vmax = {∞, 750, 375, 150, 75, 50, 40, 30} m | 
| Tasks |  |
| Gth |  |
| Evaluation |  |
| Notes |  |

### Rendering fog (image)

For  realistic  physical  simulator and rain streak photometric, intrinsic and extrinsic calibrationare used to replicate the imaging sensor. For Kitti, we usesequence-wise or frame-wise calibration with 6mm focal and 2ms exposure.  As Cityscapes does not provide calibration, we use intrinsic from camera manufacturer with5ms exposure and extrinsic is assumed similar to Kitti.

Our method also requires:
- **the scene geometry (depth map)** to model accurately the light-particle interaction and the fog optical extinction. We estimate Kitti depth maps from RGB+Lidar with [<kbd>ICCV 19</kbd> Spaded](https://openaccess.thecvf.com/content_ICCV_2019/papers/Xu_Depth_Completion_From_Sparse_LiDAR_Data_With_Depth-Normal_Constraints_ICCV_2019_paper.pdf) ,  and  Cityscapes  depth  from  RGB only with [<kbd>CVPR 17</kbd> MonoDepth](https://arxiv.org/abs/1609.03677). Thus depths are post-processed with [a guided-filter](https://arxiv.org/abs/1511.03296) for better RGB-depth alignment.
- **RGB image**

### Rendering train (image)
