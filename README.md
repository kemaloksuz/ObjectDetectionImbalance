# A Repository of the Papers Addressing Imbalance Problems in Object Detection

Here, we present the list of papers within the scope of imbalance problems in object detection by following our problem-based taxonomy in our paper submitted to IJCV. You can find a preprint in the following link:

# Table of Contents
1. [Class Imbalance](#1)  
    1.1 [Foreground-Backgorund Class Imbalance](#1.1)  
    1.2 [Foreground-Foreground Class Imbalance](#1.2)    
2. [Scale Imbalance](#2)  
    2.1 [Object/box-level Scale Imbalance](#2.1)  
    2.2 [Feature-level Imbalance](#2.2)    
3. [Spatial Imbalance](#3)  
    3.1 [Imbalance in Regression Loss](#3.1)  
    3.2 [IoU Distribution Imbalance](#3.2)  
    3.3 [Object Location Imbalance](#3.3)  
4. [Objective Imbalance](#4)

# 1. Class Imbalance <a name="1"></a>

## 1.1. Foreground-Backgorund Class Imbalance <a name="1.1"></a>
- Hard Sampling Methods
   - Random Sampling  
   - Hard Example Mining  
     - Bootstrapping, NeurIPS 1996, [[paper]](https://papers.nips.cc/paper/1168-human-face-detection-in-visual-scenes.pdf) 
     - SSD, ECCV 2016, [[paper]](http://www.cs.unc.edu/~wliu/papers/ssd.pdf)
     - Online Hard Example Mining, CVPR 2016, [[paper]](https://ieeexplore.ieee.org/document/7780458)
     - IoU-based Sampling, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/papers/Pang_Libra_R-CNN_Towards_Balanced_Learning_for_Object_Detection_CVPR_2019_paper.pdf)
   - Limit Search Space  
     - Two-stage Object Detectors 	
     - IoU-lower Bound, ICCV 2015, [[paper]](https://ieeexplore.ieee.org/document/7410526)
     - Objectness Prior, CVPR 2017, [[paper]](https://ieeexplore.ieee.org/document/8100040)
     - Negative Anchor Filtering, CVPR 2018, [[paper]](https://ieeexplore.ieee.org/document/8578540/footnotes#footnotes)
- Soft Sampling Methods  
   - Focal Loss, ICCV 2017, [[paper]](https://ieeexplore.ieee.org/document/8237586)
   - Gradient Harmonizing Mechanism, AAAI 2019, [[paper]](https://aaai.org/ojs/index.php/AAAI/article/view/4877)
   - Prime Sample Attention, arXiv 2019, [[paper]](https://arxiv.org/pdf/1904.04821.pdf)
   - AP Loss, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/papers/Chen_Towards_Accurate_One-Stage_Object_Detection_With_AP-Loss_CVPR_2019_paper.pdf)
   - DR Loss, arXiv 2019, [[paper]](https://arxiv.org/abs/1907.10156) 
- Generative Methods  
   - Adversarial Faster-RCNN, CVPR 2017, [[paper]](https://ieeexplore.ieee.org/document/8099807) 
   - Task Aware Data Synthesis, CVPR 2019, [[paper]](http://openaccess.thecvf.com/conhttps://ieeexplore.ieee.org/document/7780603https://ieeexplore.ieee.org/document/7780603https://ieeexplore.ieee.org/document/7780603https://ieeexplore.ieee.org/document/7780603https://ieeexplore.ieee.org/document/7780603https://ieeexplore.ieee.org/document/7780603https://ieeexplore.ieee.org/document/7780603https://ieeexplore.ieee.org/document/7780603https://ieeexplore.ieee.org/document/7780603https://ieeexplore.ieee.org/document/7780603tent_CVPR_2019/papers/Tripathi_Learning_to_Generate_Synthetic_Data_via_Compositing_CVPR_2019_paper.pdf)
   - PSIS, arXiv 2019, [[paper]](https://arxiv.org/pdf/1906.00358.pdf) 
   - Bounding Box Generator, WACV 2020 (Under Review)

## 1.2. Foreground-Foreground Class Imbalance  <a name="1.2"></a>
   - Fine-tuning Long Tail Distribution for Obj.Det., CVPR 2016, [[paper]](https://ieeexplore.ieee.org/document/7780469)
   - PSIS, arXiv 2019, [[paper]](https://arxiv.org/pdf/1906.00358.pdf)
   - OFB Sampling, WACV 2020 (Under Review)

# 2. Scale Imbalance <a name="2"></a>

## 2.1. Object/box-level Scale Imbalance <a name="2.1"></a>

- Methods Predicting from the Feature Hierarchy of Backbone Features
  - Scale-dependent Pooling, CVPR 2016, [[paper]](https://ieeexplore.ieee.org/document/7780603)
  - SSD, ECCV 2016, [[paper]](http://www.cs.unc.edu/~wliu/papers/ssd.pdf)
  - Multi Scale CNN, ECCV 2016, [[paper]](https://arxiv.org/abs/1607.07155)
  - Scale Aware Fast R-CNN, IEEE TMM 2017, [[paper]](https://ieeexplore.ieee.org/document/8060595)

- Methods Based on Feature Pyramids
  - FPN
  - See feature-level imbalance methods

- Methods Based on Image Pyramids
  - SNIP
  - SNIPER

- Methods Combining Image and Feature Pyramids
  - Scale Aware Trident Network

## 2.2. Feature-level Imbalance <a name="2.2"></a>

- Methods Using Pyramidal Features as a Basis
  - PANet
  - Libra FPN

- Methods Using Backbone Features as a Basis
  - STDN
  - Parallel-FPN
  - Deep Feature Pyramid Reconf.
  - Zoom Out-and-In
  - Multi-level FPN
  - NAS-FPN
  - Det-NAS

# 3. Spatial Imbalance <a name="3"></a>

## 3.1. Imbalance in Regression Loss <a name="3.1"></a>

- Lp norm based
  - Smooth L1
  - Balanced L1
  - KL Loss
  - Gradient Harmonizing Mechanism 

- IoU based
  - IoU Loss
  - Bounded IoU Loss
  - GIoU Loss
       
## 3.2. IoU Distribution Imbalance <a name="3.2"></a>
- Cascade R-CNN

## 3.3. Object Location Imbalance <a name="3.3"></a>
- Guided Anchoring

# 4. Objective Imbalance <a name="4"></a>
- Task Weighting
- Classification Aware Regression Loss
		
