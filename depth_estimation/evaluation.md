<!-- CSS -->
<link rel="stylesheet" style="text/css" href="../styles.css">
<!--     -->

## Depth Estimation/ Evaluation Metrics <img src="../doc/50.png" width="95">

> **_Depth prediction (DP):_** takes only monocular/ stereo as input 
> **_Depth completion (DC):_** takes depth sensor (ex: LiDAR, RADAR) as input component (converting a sparse depth map Dsparse into a dense depth map Ddense)

> **_Metrics DP:_** Accu, SILog, sqErrorRel, absErrorRel, iRMSE, thresh δ  
> **_Metrics DC:_** Accu, iRMSE, iMAE, RMSE, MAE, thresh δ

https://papers.nips.cc/paper/2014/file/7bccfde7714a1ebadf06c5f4cea752c1-Paper.pdf 

https://arxiv.org/pdf/2003.06620.pdf

http://www.cvlibs.net/datasets/kitti/eval_depth.php?benchmark=depth_prediction

## Depth prediction

| Metric | Description | Unit |
| :-- | -- | :--: |
| Accuracies | | |
| SILog | Scale invariant logarithmic error <br/> ![](../doc/silog.png) | log(m)*100 |
| sqErrorRel | Relative squared error <br/> ![](../doc/sq_rel.png) | % |
| absErrorRel | Relative absolute error<br/> ![](../doc/abs_rel.png) | % |
| iRMSE | Root mean squared error of the inverse depth <br/>![](../doc/irmse.png) | 1/km |
| ● thresh δ <1.25 <br/> ● thresh δ <1.25^2 <br/> ● thresh δ <1.25^3 | δ<threshold error provide a comprehensive comparison among the method <br/> δ<threshold error means the percent of pixels that satisfy δ<threshold, where δ <br/> ![](../doc/dis_pixel_error.png) <br/> (Disp)gt: the gth disparity; (Disp)pred: the predicted disparity |


## Depth completion

| Metric (DC) | Description | Unit |
| :-- | -- | :--: |
| Accuracies | | |
| iRMSE |  Root mean squared error of the inverse depth <br/>![](../doc/irmse.png) | 1/km |
| iMAE | Mean absolute error of the inverse depth <br/>![](../doc/imae.png) | 1/km |
| RMSE | Root mean squared error <br/>![](../doc/rmse.png) | mm |
| MAE | Mean absolute error <br/>![](../doc/mae.png) | mm |
| δi | δi: percentage of predicted pixels where the relative error is within 1.25^i <br/> ![](../doc/teta.png) <br/> where \|.\| denotes  the cardinality of a set. dˆ and d are prediction and associated groundtruth. Most studies adopt i = 1,2,3 | |


