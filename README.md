# Image Segmentation and Classification of SAR Water Images

## Introduction
This project focuses on leveraging deep learning models for the classification and segmentation of Synthetic Aperture Radar (SAR) water images. The primary objectives are:

1. **Image Classification**: Determine whether an image contains water using ConvNeXt, Vision Transformer (ViT), and ResNet models.
2. **Image Segmentation**: Segment regions containing water using U-Net, U-Net++, and Vision Transformer (ViT) architectures.

## Data Used
- **Dataset Source**: EUROSAT and kaggle(https://www.kaggle.com/datasets/franciscoescobar/satellite-images-of-water-bodies)
- **Data Description**:
  - SAR images with varying resolutions.
  - Labels for classification: `water` and `non-water`.
  - Masks for segmentation: true binary masks indicating water regions.
- **Preprocessing**:
  - Normalization and augmentation techniques applied to improve model performance.
  - Data split: [80% training and 20% testing].

## Classification Models and Performance
### Models Used
- **ConvNeXt**
- **Vision Transformer (ViT)**
- **ResNet**

### Performance analysis(Loss and Accuracy Curves):
**ConvNeXt (Small)**:

![Classification Loss Curve](classification/conv_small_loss.png)  
![Classification Accuracy Curve](classification/conv_small_acc.png)


**ConvNeXt (Tiny)**:

![Classification Loss Curve](classification/conv_tiny_loss.png)  
![Classification Accuracy Curve](classification/conv_tiny_acc.png)


**ViT**:

![Performance](classification/vit_stats.png)  

**ResNet**:

![Classification Loss Curve](classification/resnet_loss.png)  
![Classification Accuracy Curve](classification/resnet_Acc.png)


## Segmentation Models and Performance
### Models Used
- **U-Net**: A widely used architecture for biomedical image segmentation.
- **U-Net++**: An advanced version of U-Net with nested and dense skip connections.
- **ViT**: Adapted for image segmentation.

### Visualization of Results
Below are examples of true masks and predicted masks:

**UNET results:**
![Result](segmentation_models/unet_demo.png)  

**Unet++ results:**
![Result](segmentation_models/unet++_demo.png)  

**ViT results:**
![Result](segmentation_models/vit_demo.png) 

## Future work
- Exploring additional datasets for generalization.
- Implementing other advanced architectures.
- Fine-tuning hyperparameters for improved performance.

