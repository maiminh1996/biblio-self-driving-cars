### Overview
| Category | Description |
| :--: | -- |
| **Cityscapes** | mainly focuses on semantic segmentation tasks |
| Inputs |  | 
| Scenes |  |
| Condition |  | 
| Tasks |  |
| Gth |  |
| Evaluation |  |
| Notes |  |


### Comment
● 

The Cityscapes dataset [42] mainly focuses onsemantic segmentation tasks [37]. There are 5,000 images withfine  annotations  and  20,000  images  with  coarse  annotationsin  this  dataset.  Meanwhile,  this  dataset  consists  of  a  set  ofstereo video sequences, which are collected from 50 cities forseveral months. Since this dataset does not contain the groundtruth  of  depth,  it  is  only  applied  to  the  training  process  ofseveral unsupervised depth estimation methods [13], [15]. Theperformance of depth networks is improved by pre-training thenetworks on the Cityscapes, and the experiments in [43], [15],[13],  [44]  have  proved  the  effectiveness  of  this  joint  trainingmethod. The training data consists of 22,973 stereo image pairswith a resolution of 1024×2048 collected from different cities