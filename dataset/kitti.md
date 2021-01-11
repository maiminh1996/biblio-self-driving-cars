<!-- CSS -->
<link rel="stylesheet" style="text/css" href="../styles.css">
<!--     -->

## KITTI dataset <img src="../doc/100.png" width="95">
### [<kbd>CVPR 12</kbd> Are we ready for Autonomous Driving?The KITTI Vision Benchmark Suite](http://www.cvlibs.net/publications/Geiger2012CVPR.pdf)
### [<kbd>IJRR 13</kbd> Vision meets Robotics: The KITTI Dataset](http://ww.cvlibs.net/publications/Geiger2013IJRR.pdf)

| Category | Description |
| :--: | -- |
| Overall impression | one of the most used datasets in the driving context |
| Inputs | ● Stereo RGB images<br/> ● LiDAR pcls <br/> ● GPS coordinates<br/>all synchronized in time | 
| Scenes | 56 scenes well-structured highways, complex urban areas and narrow countryside roads ("city", "residential" & "road) categories of the raw data. Splitted into 28 for training and 28 for testing by Eigen et al [<kbd>NIPS 2014</kbd>](https://arxiv.org/pdf/1406.2283.pdf) |
| Condition | lighting conditions: all the measurements were obtained by the same set of sensors during daytimeand mostly under sunny conditions | 
| Tasks | stereo matching, visual odometry, 3D tracking and 3D object detection <br/> ● Object detection dataset: 7481 training & 7518 test frames, which are provided with sensor calibration information and annotated 3D boxes around objects of interest. Naturally we have mask label for the points inside the bbox|
| Gth | ● 3D bbox annotations are categorized in “easy, moderate & hard” cases, according to object size, occlusion & truncation levels <br/>● depth gth: sparse ground  truth  from  the  accumulation  of  lidar point  clouds  with  stereo  consistency  chec |
| Evaluation | ● 3D object detection:  Average Precision. Kitti evaluate onlyfor 3 class: 'Car', 'Pedestrian' & 'Cyclist'. They do not count ’Van’ as false positives for ’Car’ or’Sitting Person’ as false positive for ’Pedestrian’ due to their similarity in appearance. 2D bbox should correspond to the projection of the 3D bbox - this is required to filter objects larger than 25 pixel (height)
| Notes | ● Limitations: limited sensor configuration and lighting conditions <br/> ● Limitations: the classes frequency is highly unbalanced – 75% car,4% cyclist and 15% pedestrians <br/> ● Limitations: most scene objects follow a predominant orientation,facing the ego-vehicle. The lack of variety challenges the evaluation of current methods in more general scenarios, reducing their reliability for real-world applications


### Comment
● a normal size car from 40m has a height of 25 pixels inRGB image et 51m for a pedestrian with the same height.




<!-- TEAMPLATE DATASET-->
<!-- 

## NAME
### [<kbd>---</kbd> ---]()

| Category | Description |
| :--: | -- |
| Overall impression |  |
| Inputs |  | 
| Scenes |  |
| Condition |  | 
| Tasks |  |
| Gth |  |
| Evaluation |  |
| Notes |  |


### Comment
● 

-->