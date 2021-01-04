<!-- CSS -->
<link rel="stylesheet" style="text/css" href="../styles.css">
<!--     -->

## Cityscapes <img src="../doc/25.png" width="95">
### [<kbd>CVPR 16</kbd> The Cityscapes Dataset for Semantic Urban Scene Understanding](https://www.cityscapes-dataset.com/wordpress/wp-content/papercite-data/pdf/cordts2016cityscapes.pdf)
### [<kbd>CVPR Workshop 15</kbd> The Cityscapes Dataset](https://www.cityscapes-dataset.com/wordpress/wp-content/papercite-data/pdf/cordts2015cvprw.pdf)

[Link to web project](https://www.cityscapes-dataset.com/citation/)


| Category | Description |
| :--: | -- |
| Overall impression | mainly focuses on semantic segmentation tasks |
| Inputs |  | 
| Scenes |  |
| Condition |  | 
| Tasks |  |
| Gth |  |
| Evaluation |  |
| Notes |  |

The Cityscapes dataset [42] mainly focuses onsemantic segmentation tasks [37]. There are 5,000 images withfine  annotations  and  20,000  images  with  coarse  annotationsin  this  dataset.  Meanwhile,  this  dataset  consists  of  a  set  ofstereo video sequences, which are collected from 50 cities forseveral months. Since this dataset does not contain the groundtruth  of  depth,  it  is  only  applied  to  the  training  process  ofseveral unsupervised depth estimation methods [13], [15]. Theperformance of depth networks is improved by pre-training thenetworks on the Cityscapes, and the experiments in [43], [15],[13],  [44]  have  proved  the  effectiveness  of  this  joint  trainingmethod. The training data consists of 22,973 stereo image pairswith a resolution of 1024×2048 collected from different cities