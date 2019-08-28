# Imbalance Problems in Object Detection: A Review

Here, we present the list of papers within the scope of imbalance problems in object detection by following our problem-based taxonomy in our paper submitted to IJCV. You can find a preprint in the following link:

The taxonomy that we consider is as follows. The numbers in the parenthesis indicates the section that the corresponding problem is discussed in the paper.

<<<<<<< Updated upstream
![ProblemTaxonomy](assets/taxonomy.png)
=======
<<<<<<< HEAD
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
=======
![ProblemTaxonomy](assets/taxonomy.png)
>>>>>>> origin/master
>>>>>>> Stashed changes

# Class Imbalance

## Foreground-Backgorund Class Imbalance
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

## Foreground-Foreground Class Imbalance  
   - Fine-tuning Long Tail Distribution for Obj.Det., CVPR 2016, [[paper]](https://ieeexplore.ieee.org/document/7780469)
   - PSIS, arXiv 2019, [[paper]](https://arxiv.org/pdf/1906.00358.pdf)
   - OFB Sampling, WACV 2020 (Under Review)

# Scale Imbalance

<<<<<<< Updated upstream
## Object/box-level Scale Imbalance
=======
<<<<<<< HEAD
## 2.1. Object/box-level Scale Imbalance <a name="2.1"></a>
=======
## Object/box-level Scale Imbalance
>>>>>>> origin/master
>>>>>>> Stashed changes

- Methods Predicting from the Feature Hierarchy of Backbone Features
  - Scale-dependent Pooling, CVPR 2016, [[paper]](https://ieeexplore.ieee.org/document/7780603)
  - SSD, ECCV 2016, [[paper]](http://www.cs.unc.edu/~wliu/papers/ssd.pdf)
  - Multi Scale CNN, ECCV 2016, [[paper]](https://arxiv.org/abs/1607.07155)
  - Scale Aware Fast R-CNN, IEEE TMM 2017, [[paper]](https://ieeexplore.ieee.org/document/8060595)

- Methods Based on Feature Pyramids
  - FPN, CVPR 2017, [[paper]](https://ieeexplore.ieee.org/document/8099589)
  - See feature-level imbalance methods

- Methods Based on Image Pyramids
  - SNIP, CVPR 2018, [[paper]](https://ieeexplore.ieee.org/document/8578475)
  - SNIPER, NeurIPS 2018, [[paper]](https://papers.nips.cc/paper/8143-sniper-efficient-multi-scale-training.pdf)

- Methods Combining Image and Feature Pyramids
  - Scale Aware Trident Network, arXiv 2019, [[paper]](https://arxiv.org/abs/1901.01892)

<<<<<<< Updated upstream
## Feature-level Imbalance
=======
<<<<<<< HEAD
## 2.2. Feature-level Imbalance <a name="2.2"></a>
=======
## Feature-level Imbalance
>>>>>>> origin/master
>>>>>>> Stashed changes
- Methods Using Pyramidal Features as a Basis
  - PANet, CVPR 2018, [[paper]](https://ieeexplore.ieee.org/document/8579011)
  - Libra FPN, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/html/Pang_Libra_R-CNN_Towards_Balanced_Learning_for_Object_Detection_CVPR_2019_paper.html)

- Methods Using Backbone Features as a Basis
  - STDN, CVPR 2018, [[paper]](https://ieeexplore.ieee.org/document/8578160)
  - Parallel-FPN, ECCV 2018, [[paper]](https://link.springer.com/chapter/10.1007/978-3-030-01228-1_15)
  - Deep Feature Pyramid Reconf., ECCV 2018, [[paper]](https://link.springer.com/chapter/10.1007/978-3-030-01228-1_11)
  - Zoom Out-and-In, IJCV 2019, [[paper]](https://arxiv.org/abs/1709.04347)
  - Multi-level FPN, AAAI 2019, [[paper]](https://www.groundai.com/project/m2det-a-single-shot-object-detector-based-on-multi-level-feature-pyramid-network/)
  - NAS-FPN, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/html/Ghiasi_NAS-FPN_Learning_Scalable_Feature_Pyramid_Architecture_for_Object_Detection_CVPR_2019_paper.html)
  - Det-NAS, arXiv 2019, [[paper]](https://arxiv.org/abs/1903.10979)

# Spatial Imbalance

<<<<<<< Updated upstream
## Imbalance in Regression Loss
=======
<<<<<<< HEAD
## 3.1. Imbalance in Regression Loss <a name="3.1"></a>
=======
## Imbalance in Regression Loss
>>>>>>> origin/master
>>>>>>> Stashed changes
- Lp norm based
  - Smooth L1, ICCV 2015, [[paper]](https://ieeexplore.ieee.org/document/7410526)
  - Balanced L1, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/html/Pang_Libra_R-CNN_Towards_Balanced_Learning_for_Object_Detection_CVPR_2019_paper.html)
  - KL Loss, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/papers/He_Bounding_Box_Regression_With_Uncertainty_for_Accurate_Object_Detection_CVPR_2019_paper.pdf)
  - Gradient Harmonizing Mechanism, AAAI 2019, [[paper]](https://aaai.org/ojs/index.php/AAAI/article/view/4877)

- IoU based
  - IoU Loss, ACM IMM 2016, [[paper]](https://dl.acm.org/citation.cfm?id=2967274)
  - Bounded IoU Loss, CVPR 2018, [[paper]](https://arxiv.org/pdf/1711.00164v2.pdf)
  - GIoU Loss, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/papers/Rezatofighi_Generalized_Intersection_Over_Union_A_Metric_and_a_Loss_for_CVPR_2019_paper.pdf)
       
<<<<<<< Updated upstream
## IoU Distribution Imbalance
- Cascade R-CNN, CVPR 2018, [[paper]](https://ieeexplore.ieee.org/document/8578742)

## Object Location Imbalance
=======
<<<<<<< HEAD
## 3.2. IoU Distribution Imbalance <a name="3.2"></a>
- Cascade R-CNN, CVPR 2018, [[paper]](https://ieeexplore.ieee.org/document/8578742)

## 3.3. Object Location Imbalance <a name="3.3"></a>
=======
## IoU Distribution Imbalance
- Cascade R-CNN, CVPR 2018, [[paper]](https://ieeexplore.ieee.org/document/8578742)

## Object Location Imbalance
>>>>>>> origin/master
>>>>>>> Stashed changes
- Guided Anchoring, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/html/Wang_Region_Proposal_by_Guided_Anchoring_CVPR_2019_paper.html)

# Objective Imbalance
- Task Weighting
- Classification Aware Regression Loss, arXiv 2019, [[paper]](https://arxiv.org/pdf/1904.04821.pdf)
		
