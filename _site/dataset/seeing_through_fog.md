<!-- CSS -->
<link rel="stylesheet" style="text/css" href="../styles.css">
<!--     -->

## Seeing Through Fog <img src="../doc/0.png" width="95">
### [<kbd>CVPR 20</kbd> Seeing Through Fog Without Seeing Fog: Deep Multimodal Sensor Fusion in Unseen Adverse Weather](https://www.cs.princeton.edu/~fheide/AdverseWeatherFusion/) 

### [<kbd>ICCV 19</kbd> Gated2Depth: Real-time Dense Lidar from Gated Images](https://arxiv.org/pdf/1902.04997.pdf)

[Link to web project](https://www.cs.princeton.edu/~fheide/AdverseWeatherFusion/)


| Category | Description |
| :--: | -- |
| Overall impression | a  multimodal  adverse  weather  datasetcovering camera, lidar, radar, gated NIR, and FIR sensor data which contains rare scenarios, such asheavy fog, heavy snow, and severe rain, during morethan 10,000 km of driving in northern Europe. |
| Inputs | ● Stereo (1920x1024) <br/> ● Gated cam (1280x720) <br/> ● RADAR <br/> ● LiDAR: 1 HDL64 S3D and VLP32C <br/> ● FIR cam<br/> All  sensors  are  time-synchronized and ego-motion corrected using a proprietaryinertial  measurement  unit  (IMU).  The  system  provides  asampling rate of 10 Hz | 
| Scenes | 2 test drives in Feb and Dec 2019 in Germany, Sweden, Denmark, and Finland for twoweeks  each,  covering  a  distance  of  10,000 km  under  different weather and illumination conditions.  A total of 1.4million frames at a frame rate of 10 Hz have been collected |
| Condition | clear weather, dense fog, inlight fog, snow/ rain | 
| Tasks |  |
| Gth | Every 100th frame was manually labeled to balance scenetype coverage. The resulting annotations contain 5,5k clear weather  frames,  1k  captures  in  dense  fog,  1k  captures  inlight fog, and 4k captures in snow/rain |
| Evaluation |  |
| Notes |  |


## Simulation 
Simulated data to the clear training data as an alternative approach to tackle the rare harsh weather conditions.   
Ref: [Seeing Through Fog Without Seeing Fog:Deep Multimodal Sensor Fusion in Unseen Adverse Weather(Supplemental Material)](https://www.cs.princeton.edu/~fheide/AdverseWeatherFusion/figures/AdverseWeatherFusion_Supplement.pdf)