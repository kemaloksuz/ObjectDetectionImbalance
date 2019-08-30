# A Repository of the Papers Addressing Imbalance Problems in Object Detection

This repository provides an up-to-date the list of studies addressing imbalance problems in object detection. It follows the taxonomy provided in the following paper (please cite the paper if you benefit from this repository):

K. Oksuz, B. C. Cam, S. Kalkan, E. Akbas, "Imbalance Problems in Object Detection: A Review", (under review), 2019.
	
If you spot a study missing in the repository, you can directly send a request for adding it.

## How to request addition of a paper
You are welcome to submit a pull request if you think that your paper addresses any imbalance problem concerning object detection. In your pull request please briefly state which section of your paper is related to which problem.

# Table of Contents (Follows the taxonomy in the paper)
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
     - Online Hard Example Mining, CVPR 2016, [[paper]](https://zpascal.net/cvpr2016/Shrivastava_Training_Region-Based_Object_CVPR_2016_paper.pdf)
     - IoU-based Sampling, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/papers/Pang_Libra_R-CNN_Towards_Balanced_Learning_for_Object_Detection_CVPR_2019_paper.pdf)
   - Limit Search Space  
     - Two-stage Object Detectors 	
     - IoU-lower Bound, ICCV 2015, [[paper]](https://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Girshick_Fast_R-CNN_ICCV_2015_paper.pdf)
     - Objectness Prior, CVPR 2017, [[paper]](http://zpascal.net/cvpr2017/Kong_RON_Reverse_Connection_CVPR_2017_paper.pdf)
     - Negative Anchor Filtering, CVPR 2018, [[paper]](http://openaccess.thecvf.com/content_cvpr_2018/papers/Zhang_Single-Shot_Refinement_Neural_CVPR_2018_paper.pdf)
- Soft Sampling Methods  
   - Focal Loss, ICCV 2017, [[paper]](http://openaccess.thecvf.com/content_ICCV_2017/papers/Lin_Focal_Loss_for_ICCV_2017_paper.pdf)
   - Gradient Harmonizing Mechanism, AAAI 2019, [[paper]](https://aaai.org/ojs/index.php/AAAI/article/view/4877)
   - Prime Sample Attention, arXiv 2019, [[paper]](https://arxiv.org/pdf/1904.04821.pdf)
   - AP Loss, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/papers/Chen_Towards_Accurate_One-Stage_Object_Detection_With_AP-Loss_CVPR_2019_paper.pdf)
   - DR Loss, arXiv 2019, [[paper]](https://arxiv.org/pdf/1907.10156.pdf) 
- Generative Methods  
   - Adversarial Faster-RCNN, CVPR 2017, [[paper]](http://zpascal.net/cvpr2017/Wang_A-Fast-RCNN_Hard_Positive_CVPR_2017_paper.pdf) 
   - Task Aware Data Synthesis, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/papers/Tripathi_Learning_to_Generate_Synthetic_Data_via_Compositing_CVPR_2019_paper.pdf)
   - PSIS, arXiv 2019, [[paper]](https://arxiv.org/pdf/1906.00358.pdf) 
   - Bounding Box Generator, WACV 2020 (Under Review)

## 1.2. Foreground-Foreground Class Imbalance  <a name="1.2"></a>
   - Fine-tuning Long Tail Distribution for Obj.Det., CVPR 2016, [[paper]](http://openaccess.thecvf.com/content_cvpr_2016/papers/Ouyang_Factors_in_Finetuning_CVPR_2016_paper.pdf)
   - PSIS, arXiv 2019, [[paper]](https://arxiv.org/pdf/1906.00358.pdf)
   - OFB Sampling, WACV 2020 (Under Review)

# 2. Scale Imbalance <a name="2"></a>

## 2.1. Object/box-level Scale Imbalance <a name="2.1"></a>

- Methods Predicting from the Feature Hierarchy of Backbone Features
  - Scale-dependent Pooling, CVPR 2016, [[paper]](http://openaccess.thecvf.com/content_cvpr_2016/papers/Yang_Exploit_All_the_CVPR_2016_paper.pdf)
  - SSD, ECCV 2016, [[paper]](http://www.cs.unc.edu/~wliu/papers/ssd.pdf)
  - Multi Scale CNN, ECCV 2016, [[paper]](https://arxiv.org/pdf/1607.07155.pdf)
  - Scale Aware Fast R-CNN, IEEE TMM 2017, [[paper]](https://arxiv.org/pdf/1510.08160.pdf)

- Methods Based on Feature Pyramids
  - FPN, CVPR 2017, [[paper]](https://zpascal.net/cvpr2017/Lin_Feature_Pyramid_Networks_CVPR_2017_paper.pdf)
  - See feature-level imbalance methods

- Methods Based on Image Pyramids
  - SNIP, CVPR 2018, [[paper]](http://openaccess.thecvf.com/content_cvpr_2018/papers/Singh_An_Analysis_of_CVPR_2018_paper.pdf)
  - SNIPER, NeurIPS 2018, [[paper]](https://papers.nips.cc/paper/8143-sniper-efficient-multi-scale-training.pdf)

- Methods Combining Image and Feature Pyramids
  - Scale Aware Trident Network, arXiv 2019, [[paper]](https://arxiv.org/pdf/1901.01892.pdf)

## 2.2. Feature-level Imbalance <a name="2.2"></a>

- Methods Using Pyramidal Features as a Basis
  - PANet, CVPR 2018, [[paper]](http://openaccess.thecvf.com/content_cvpr_2018/papers/Liu_Path_Aggregation_Network_CVPR_2018_paper.pdf)
  - Libra FPN, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/papers/Pang_Libra_R-CNN_Towards_Balanced_Learning_for_Object_Detection_CVPR_2019_paper.pdf)

- Methods Using Backbone Features as a Basis
  - STDN, CVPR 2018, [[paper]](http://openaccess.thecvf.com/content_cvpr_2018/CameraReady/1376.pdf)
  - Parallel-FPN, ECCV 2018, [[paper]](http://openaccess.thecvf.com/content_ECCV_2018/papers/Seung-Wook_Kim_Parallel_Feature_Pyramid_ECCV_2018_paper.pdf)
  - Deep Feature Pyramid Reconfiguration, ECCV 2018, [[paper]](https://eccv2018.org/openaccess/content_ECCV_2018/papers/Tao_Kong_Deep_Feature_Pyramid_ECCV_2018_paper.pdf)
  - Zoom Out-and-In, IJCV 2019, [[paper]](https://arxiv.org/pdf/1709.04347.pdf)
  - Multi-level FPN, AAAI 2019, [[paper]](https://arxiv.org/pdf/1811.04533.pdf)
  - NAS-FPN, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/papers/Ghiasi_NAS-FPN_Learning_Scalable_Feature_Pyramid_Architecture_for_Object_Detection_CVPR_2019_paper.pdf)
  - Det-NAS, arXiv 2019, [[paper]](https://arxiv.org/pdf/1903.10979.pdf)

# 3. Spatial Imbalance <a name="3"></a>

## 3.1. Imbalance in Regression Loss <a name="3.1"></a>

- Lp norm based
  - Smooth L1, ICCV 2015, [[paper]](https://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Girshick_Fast_R-CNN_ICCV_2015_paper.pdf)
  - Balanced L1, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/html/Pang_Libra_R-CNN_Towards_Balanced_Learning_for_Object_Detection_CVPR_2019_paper.html)
  - KL Loss, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/papers/He_Bounding_Box_Regression_With_Uncertainty_for_Accurate_Object_Detection_CVPR_2019_paper.pdf)
  - Gradient Harmonizing Mechanism, AAAI 2019, [[paper]](https://aaai.org/ojs/index.php/AAAI/article/view/4877/4750)

- IoU based
  - IoU Loss, ACM IMM 2016, [[paper]](https://arxiv.org/pdf/1608.01471.pdf)
  - Bounded IoU Loss, CVPR 2018, [[paper]](http://openaccess.thecvf.com/content_cvpr_2018/CameraReady/0794.pdf)
  - GIoU Loss, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/papers/Rezatofighi_Generalized_Intersection_Over_Union_A_Metric_and_a_Loss_for_CVPR_2019_paper.pdf)
       
## 3.2. IoU Distribution Imbalance <a name="3.2"></a>
- Cascade R-CNN, CVPR 2018, [[paper]](http://openaccess.thecvf.com/content_cvpr_2018/papers/Cai_Cascade_R-CNN_Delving_CVPR_2018_paper.pdf)

## 3.3. Object Location Imbalance <a name="3.3"></a>
- Guided Anchoring, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/html/Wang_Region_Proposal_by_Guided_Anchoring_CVPR_2019_paper.html)

# 4. Objective Imbalance <a name="4"></a>
- Task Weighting
- Classification Aware Regression Loss, arXiv 2019, [[paper]](https://arxiv.org/pdf/1904.04821.pdf)
		
# Contact 
Please contact with Kemal Öksüz (kemal.oksuz@metu.edu.tr) for your questions about this webpage.