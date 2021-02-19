# Segmenting Objects by Location PyTorch Implementation

The project involved the implementation of the instance segmentation algorithm defined in paper: [SOLO](https://arxiv.org/abs/1912.04488). The main idea behind the paper is that different instance categories can be differentiated by their location and size in an image. The image is divided into SxS grids. Each grid cell is responsible for locating the instance's center which falls in the pixels it corresponds to in the original image. Size is handled by detecting at different levels of Feature Pyramid Network.

## Results
<!--![](./Results/1.png)     ![](./Results/1_mask.png)
![](./Results/2.png)     ![](./Results/2_mask.png)
![](./Results/3.png)     ![](./Results/3_mask.png) -->

<p float="left">
  <img src="./Results/1.png" width = 40%/>
  <img src="./Results/1_mask.png" width = 40%/> 
</p>
<p float="left">
  <img src="./Results/2.png" width = 40%/>
  <img src="./Results/2_mask.png" width = 40%/> 
</p>
<p float="left">
  <img src="./Results/3.png" width = 40%/>
  <img src="./Results/3_mask.png" width = 40%/> 
</p>

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