Filamentous Structures in Microscopic images
======
 Image size (1024x1024) filaments width 2 pixels to 5 pixels; intersections is the hardest part
 

Attention
=====
The problem of long sequences 


Types of defect:
 * Textures
 * Objects deformation
 * unexpected patterns
 
Other things that might help:
 Domain adapation 
 Domain Generaziation
 
 


[MVTec AD — A Comprehensive Real-World Dataset for Unsupervised Anomaly Detection](https://openaccess.thecvf.com/content_CVPR_2019/papers/Bergmann_MVTec_AD_--_A_Comprehensive_Real-World_Dataset_for_Unsupervised_Anomaly_CVPR_2019_paper.pdf)

[Explainable Deep One-Class Classification](https://arxiv.org/pdf/2007.01760.pdf)

Traditional methods
=======
Gaussian blur Might help.


Classification of Anomalous Images
=======


Segmentation of Anomalous Regions
=======
* representation learning/contrastive loss
   Uninformed  Students:  Student–Teacher  Anomaly  Detectionwith  Discriminative  Latent  Embeddings
   
* Generative Adversarial Networks

* Generative models/Probablistic models:
   PixelCNN++

* Reconstruction based/Autoencoder:
 * [Improving  Unsupervised  Defect  Segmentationby  Applying  Structural  Similarity  To  Autoencoders](https://arxiv.org/pdf/1807.02011.pdf)
   Structured loss
 * [Explainable Deep One-Class Classification](https://arxiv.org/pdf/2007.01760.pdf)
 

* Features of Pre-trained Convolutional NeuralNetworks
  


* Traditional Methods 

* Explanation approaches:
  * Autoencoders  
  
  * one-class classification methods for deep AD:

     concentrating nominal data in feature space while mapping anomalies to distant locations
     
     interpretation using attention mechanisms
     
  * self-supervision
  
* Patch:
  [Anomaly Detection in Nanofibrous Materials byCNN-Based Self-Similarity](file:///tmp/mozilla_yi0/sensors-18-00209-v2.pdf)
  
Small Object Detection
=======

 * Retina images (512x512):
   object: 30 - 50 pixels and 10 - 20 pixels
   
   Solution:
    1. Sliding window + crop image patch -> binary calssification
    
 * Airea images, remote sensor
  * Faster Rcnn-> big objecT
    FPN might not be able to capture it
    Bounding Box, anchor size might be too big -> modify anchor size 
    Concatenate feature map from different level.
    
    Context Region
    
 * Focal loss?
 
Small object segmentation:
======
Model perspective:
 * uncertainty (Drop out?)
 
From the point of loss
 * Dice loss
   因为dice loss是一个区域相关的loss
   在使用dice loss时，一般正样本为小目标时会产生严重的震荡 (比如只有一个像素点时)
   
 * other weighted loss(higher penalty for positive data samples)
   dice + focal loss
   dice+ce loss
   Median frequency balanc-ing weights the class loss by the ratio of the median classfrequency in the training set and the actual class frequency

其他：

 mIOU一般都是基于类进行计算的，将每一类的IOU计算之后累加，再进行平均，得到的就是基于全局的评价。
 
Fine Grain

Small object Detection

Anomaly detection
