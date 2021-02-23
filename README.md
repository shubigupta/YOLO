# You Only Look Once (YOLO): Pytorch Implementation

The project involved the implementation of the object detection algorithm Yolo defined in the paper: [YOLO](https://arxiv.org/pdf/1506.02640.pdf). YOLO poses the object detection problem as regression problem and uses a single neural network to predict bounding boxes and class probabilities directly from full images in one evaluation.

## Results
<!--![](./Results/1.png)     ![](./Results/1_mask.png)
![](./Results/2.png)     ![](./Results/2_mask.png)
![](./Results/3.png)     ![](./Results/3_mask.png) -->


<table>
  <tr>
      <td align = "center"> <img src="./Results/1. Bounding box before elimination"> </td>
      <td align = "center"> <img src="./Results/2. Bounding box after suppressing low confidence.png"> </td>
      <td align = "center"> <img src="./Results/3. Bounding box after non-max suppression.png"> </td>
  </tr>
  <tr>
      <td align = "center"> Predictions from the network </td>
      <td align = "center"> Suppressing low confidence boxes </td>
      <td align = "center"> Boxes after non-max suppression </td>
  </tr>
</table>

<table>
  <tr>
      <td align = "center"> <img src="./Results/6. Confidence error.png"> </td>
      <td align = "center"> <img src="./Results/7. Localisation and classification error.png"> </td>
  </tr>
  <tr>
      <td align = "center"> Confidence error </td>
      <td align = "center"> Localisation and Classification error </td>
  </tr>
</table>


## Hyperparameters
* Focal Loss
    * alpha = 0.25, gamma = 2
* Mask Loss weight : 3
* Category Threshold:  0.2
* INS Threshold         : 0.5
* IoU Threshold         : 0.3 
* Learning rate           : 0.01 , 0.001 @epoch28, 0.0001 @epoch 34
* Momentum              : 0.9
* Weight Decay          : 0.0001
* Num Epochs            : 40

## Loss Plots
<p float="left">
  <img src="./Results/Dice_loss.png" width = 40%/>
  <img src="./Results/Focal_loss.png" width = 40%/> 
</p>
<p float="center">
  <img src="./Results/Total_loss.png" width = 40%/>
</p>

## Precision vs Recall plot
<p float="center">
  <img src="./Results/download.png" width = 40%/>
</p>
