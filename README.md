# A Repository of the Papers Addressing Imbalance Problems in Object Detection

This repository provides an up-to-date the list of studies addressing imbalance problems in object detection. It follows the taxonomy provided in the following paper (please cite the paper if you benefit from this repository):

K. Oksuz, B. C. Cam, S. Kalkan, E. Akbas, "Imbalance Problems in Object Detection: A Review", Transactions on Pattern Analysis and Machine Intelligence (TPAMI), 2020.[[preprint]](https://arxiv.org/abs/1909.00169)

BibTeX entry:
```
@ARTICLE{imbalance,
       author = {Kemal Oksuz and Baris Can Cam and Sinan Kalkan and Emre Akbas},
        title = "{Imbalance Problems in Object Detection: A Review}",
      journal = {Transactions on Pattern Analysis and Machine Intelligence (TPAMI)},
         year = "2020",
        pages = {1-1}
        }
```

## How to request addition of a paper
If you know of a paper that addresses an imbalance problem concerning generic object detection and is not on this repository, you are welcome to request the addition of that paper by submitting a pull request. In your pull request please briefly state which section of your paper is related to which problem.  

Following the methodology in our paper, the papers should be designed for the generic object detection problem (i.e. reporting results on generic object detection datasets such as ILSVRC, Pascal VOC, MS-COCO, Open Images, Objects 365 etc.). 

# Table of Contents (Follows the taxonomy in the paper)
1. [Class Imbalance](#1)  
    1.1 [Foreground-Background Class Imbalance](#1.1)  
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

## 1.1. Foreground-Background Class Imbalance <a name="1.1"></a>
- Hard Sampling Methods
   - Random Sampling  
   - Hard Example Mining  
     - Bootstrapping, NeurIPS 1996, [[paper]](https://papers.nips.cc/paper/1168-human-face-detection-in-visual-scenes.pdf) 
     - SSD, ECCV 2016, [[paper]](http://www.cs.unc.edu/~wliu/papers/ssd.pdf)
     - Online Hard Example Mining, CVPR 2016, [[paper]](https://zpascal.net/cvpr2016/Shrivastava_Training_Region-Based_Object_CVPR_2016_paper.pdf)
     - IoU-based Sampling, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/papers/Pang_Libra_R-CNN_Towards_Balanced_Learning_for_Object_Detection_CVPR_2019_paper.pdf)
     - Overlap Sampler, WACV 2020, [[paper]](http://openaccess.thecvf.com/content_WACV_2020/papers/Chen_Overlap_Sampler_for_Region-Based_Object_Detection_WACV_2020_paper.pdf)
   - Limit Search Space  
     - Two-stage Object Detectors 	
     - IoU-lower Bound, ICCV 2015, [[paper]](https://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Girshick_Fast_R-CNN_ICCV_2015_paper.pdf)
     - Objectness Prior, CVPR 2017, [[paper]](http://zpascal.net/cvpr2017/Kong_RON_Reverse_Connection_CVPR_2017_paper.pdf)
     - Negative Anchor Filtering, CVPR 2018, [[paper]](http://openaccess.thecvf.com/content_cvpr_2018/papers/Zhang_Single-Shot_Refinement_Neural_CVPR_2018_paper.pdf)
     - Objectness Module, ICCV 2019, [[paper]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Nie_Enriched_Feature_Guided_Refinement_Network_for_Object_Detection_ICCV_2019_paper.pdf)
- Soft Sampling Methods  
   - Focal Loss, ICCV 2017, [[paper]](http://openaccess.thecvf.com/content_ICCV_2017/papers/Lin_Focal_Loss_for_ICCV_2017_paper.pdf)
   - Gradient Harmonizing Mechanism, AAAI 2019, [[paper]](https://aaai.org/ojs/index.php/AAAI/article/view/4877)
   - Prime Sample Attention, CVPR 2020, [[paper]](https://openaccess.thecvf.com/content_CVPR_2020/papers/Cao_Prime_Sample_Attention_in_Object_Detection_CVPR_2020_paper.pdf)
   - Unified Sample Weighting Network, CVPR 2020, [[paper]](https://openaccess.thecvf.com/content_CVPR_2020/papers/Cai_Learning_a_Unified_Sample_Weighting_Network_for_Object_Detection_CVPR_2020_paper.pdf)
   - Equalization Loss, CVPR 2020, [[paper]](https://arxiv.org/pdf/2003.05176.pdf)
   - Quality Focal Loss, NeurIPS 2020, [[paper]](https://proceedings.neurips.cc/paper/2020/file/f0bda020d2470f2e74990a07a607ebd9-Paper.pdf) 
   - Equalization Loss v2, ArXiv 2020, [[paper]](https://arxiv.org/pdf/2012.08548.pdf)

- Sampling-Free Methods
   - Is Sampling Heuristics Necessary in Training Deep Object Detectors?, arXiv 2019, [[paper]](https://arxiv.org/pdf/1909.04868.pdf)
   - Residual Objectness for Imbalance Reduction, arXiv 2019, [[paper]](https://arxiv.org/pdf/1908.09075.pdf)   
   - AP Loss, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/papers/Chen_Towards_Accurate_One-Stage_Object_Detection_With_AP-Loss_CVPR_2019_paper.pdf)
   - DR Loss, CVPR 2020, [[paper]](https://openaccess.thecvf.com/content_CVPR_2020/papers/Qian_DR_Loss_Improving_Object_Detection_by_Distributional_Ranking_CVPR_2020_paper.pdf)
   - aLRP Loss, NeurIPS 2020, [[paper]](https://papers.nips.cc/paper/2020/file/b2eeb7362ef83deff5c7813a67e14f0a-Paper.pdf)   

- Generative Methods  
   - Adversarial Faster-RCNN, CVPR 2017, [[paper]](http://zpascal.net/cvpr2017/Wang_A-Fast-RCNN_Hard_Positive_CVPR_2017_paper.pdf) 
   - Task Aware Data Synthesis, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/papers/Tripathi_Learning_to_Generate_Synthetic_Data_via_Compositing_CVPR_2019_paper.pdf)
   - PSIS, arXiv 2019, [[paper]](https://arxiv.org/pdf/1906.00358.pdf) 
   - pRoI Generator, WACV 2020, [[paper]](http://openaccess.thecvf.com/content_WACV_2020/papers/Oksuz_Generating_Positive_Bounding_Boxes_for_Balanced_Training_of_Object_Detectors_WACV_2020_paper.pdf)


## 1.2. Foreground-Foreground Class Imbalance  <a name="1.2"></a>
   - Fine-tuning Long Tail Distribution for Obj.Det., CVPR 2016, [[paper]](http://openaccess.thecvf.com/content_cvpr_2016/papers/Ouyang_Factors_in_Finetuning_CVPR_2016_paper.pdf)
   - PSIS, arXiv 2019, [[paper]](https://arxiv.org/pdf/1906.00358.pdf)
   - OFB Sampling, WACV 2020, [[paper]](http://openaccess.thecvf.com/content_WACV_2020/papers/Oksuz_Generating_Positive_Bounding_Boxes_for_Balanced_Training_of_Object_Detectors_WACV_2020_paper.pdf)
   - Large-Scale Object Detection in the Wild from Imbalanced Multi-Labels, CVPR 2020, [[paper]](https://openaccess.thecvf.com/content_CVPR_2020/papers/Peng_Large-Scale_Object_Detection_in_the_Wild_From_Imbalanced_Multi-Labels_CVPR_2020_paper.pdf)
   - Balanced Group Softmax Loss, CVPR 2020, [[paper]](https://openaccess.thecvf.com/content_CVPR_2020/papers/Li_Overcoming_Classifier_Imbalance_for_Long-Tail_Object_Detection_With_Balanced_Group_CVPR_2020_paper.pdf) 
   - SimCal, ECCV 2020,  [[paper]](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123590715.pdf) 

# 2. Scale Imbalance <a name="2"></a>

## 2.1. Object/box-level Scale Imbalance <a name="2.1"></a>

- Methods Predicting from the Feature Hierarchy of Backbone Features
  - Scale-dependent Pooling, CVPR 2016, [[paper]](http://openaccess.thecvf.com/content_cvpr_2016/papers/Yang_Exploit_All_the_CVPR_2016_paper.pdf)
  - SSD, ECCV 2016, [[paper]](http://www.cs.unc.edu/~wliu/papers/ssd.pdf)
  - Multi Scale CNN, ECCV 2016, [[paper]](https://arxiv.org/pdf/1607.07155.pdf)
  - Scale Aware Fast R-CNN, IEEE Transactions on Multimedia, 2018 [[paper]](https://ieeexplore.ieee.org/document/8060595)

- Methods Based on Feature Pyramids
  - FPN, CVPR 2017, [[paper]](https://zpascal.net/cvpr2017/Lin_Feature_Pyramid_Networks_CVPR_2017_paper.pdf)
  - See feature-level imbalance methods

- Methods Based on Image Pyramids
  - SNIP, CVPR 2018, [[paper]](http://openaccess.thecvf.com/content_cvpr_2018/papers/Singh_An_Analysis_of_CVPR_2018_paper.pdf)
  - SNIPER, NeurIPS 2018, [[paper]](https://papers.nips.cc/paper/8143-sniper-efficient-multi-scale-training.pdf)

- Methods Combining Image and Feature Pyramids
  - Efficient Featurized Image Pyramids, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/papers/Pang_Efficient_Featurized_Image_Pyramid_Network_for_Single_Shot_Detector_CVPR_2019_paper.pdf)
  - Enriched Feature Guided Refinement Network, ICCV 2019, [[paper]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Nie_Enriched_Feature_Guided_Refinement_Network_for_Object_Detection_ICCV_2019_paper.pdf)  
  - Super-Resolution for Small Objects, ICCV 2019, [[paper]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Noh_Better_to_Follow_Follow_to_Be_Better_Towards_Precise_Supervision_ICCV_2019_paper.pdf)
  - Scale Aware Trident Network, ICCV 2019, [[paper]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Li_Scale-Aware_Trident_Networks_for_Object_Detection_ICCV_2019_paper.pdf)
  
## 2.2. Feature-level Imbalance <a name="2.2"></a>

- Methods Using Pyramidal Features as a Basis
  - PANet, CVPR 2018, [[paper]](http://openaccess.thecvf.com/content_cvpr_2018/papers/Liu_Path_Aggregation_Network_CVPR_2018_paper.pdf)
  - Libra FPN, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/papers/Pang_Libra_R-CNN_Towards_Balanced_Learning_for_Object_Detection_CVPR_2019_paper.pdf)
  - Representation Sharing for Fast Object Detector Search and Beyond, ECCV 2020, [[paper]](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123640460.pdf)
   - Fine-Grained Dynamic Head for Object Detection, NeurIPS 2020, [[paper]](https://papers.nips.cc/paper/2020/file/7f6caf1f0ba788cd7953d817724c2b6e-Paper.pdf) 

- Methods Using Backbone Features as a Basis
  - STDN, CVPR 2018, [[paper]](http://openaccess.thecvf.com/content_cvpr_2018/CameraReady/1376.pdf)
  - Parallel-FPN, ECCV 2018, [[paper]](http://openaccess.thecvf.com/content_ECCV_2018/papers/Seung-Wook_Kim_Parallel_Feature_Pyramid_ECCV_2018_paper.pdf)
  - Deep Feature Pyramid Reconfiguration, ECCV 2018, [[paper]](https://eccv2018.org/openaccess/content_ECCV_2018/papers/Tao_Kong_Deep_Feature_Pyramid_ECCV_2018_paper.pdf)
  - Zoom Out-and-In, IJCV 2019, [[paper]](https://arxiv.org/pdf/1709.04347.pdf)
  - Multi-level FPN, AAAI 2019, [[paper]](https://arxiv.org/pdf/1811.04533.pdf)
  - NAS-FPN, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/papers/Ghiasi_NAS-FPN_Learning_Scalable_Feature_Pyramid_Architecture_for_Object_Detection_CVPR_2019_paper.pdf)
  - Auto-FPN, ICCV 2019, [[paper]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Xu_Auto-FPN_Automatic_Network_Architecture_Adaptation_for_Object_Detection_Beyond_Classification_ICCV_2019_paper.pdf)
  - AugFPN, CVPR 2020, [[paper]](https://openaccess.thecvf.com/content_CVPR_2020/papers/Guo_AugFPN_Improving_Multi-Scale_Feature_Learning_for_Object_Detection_CVPR_2020_paper.pdf)
  - Hit-Detector, CVPR 2020, [[paper]](https://openaccess.thecvf.com/content_CVPR_2020/papers/Guo_Hit-Detector_Hierarchical_Trinity_Architecture_Search_for_Object_Detection_CVPR_2020_paper.pdf)
  - Pyramid Convolution, CVPR 2020, [[paper]](https://openaccess.thecvf.com/content_CVPR_2020/papers/Wang_Scale-Equalizing_Pyramid_Convolution_for_Object_Detection_CVPR_2020_paper.pdf)

# 3. Spatial Imbalance <a name="3"></a>

## 3.1. Imbalance in Regression Loss <a name="3.1"></a>

- Lp norm based
  - Smooth L1, ICCV 2015, [[paper]](https://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Girshick_Fast_R-CNN_ICCV_2015_paper.pdf)
  - Balanced L1, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/html/Pang_Libra_R-CNN_Towards_Balanced_Learning_for_Object_Detection_CVPR_2019_paper.html)
  - KL Loss, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/papers/He_Bounding_Box_Regression_With_Uncertainty_for_Accurate_Object_Detection_CVPR_2019_paper.pdf)
  - Gradient Harmonizing Mechanism, AAAI 2019, [[paper]](https://aaai.org/ojs/index.php/AAAI/article/view/4877/4750)
  - Dynamic Smooth L1, ECCV 2020, [[paper]](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123600256.pdf)

- IoU based
  - IoU Loss, ACM IMM 2016, [[paper]](https://arxiv.org/pdf/1608.01471.pdf)
  - Bounded IoU Loss, CVPR 2018, [[paper]](http://openaccess.thecvf.com/content_cvpr_2018/CameraReady/0794.pdf)
  - Generalized IoU Loss, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/papers/Rezatofighi_Generalized_Intersection_Over_Union_A_Metric_and_a_Loss_for_CVPR_2019_paper.pdf)
  - Distance IoU Loss, AAAI 2020, [[paper]](https://arxiv.org/pdf/1911.08287.pdf)
  - Complete IoU Loss, AAAI 2020, [[paper]](https://arxiv.org/pdf/1911.08287.pdf)

- Cross entropy based
  - Offset Bin Classiﬁcation Network, CVPR 2020, [[paper]](https://openaccess.thecvf.com/content_CVPR_2020/papers/Qiu_Offset_Bin_Classification_Network_for_Accurate_Object_Detection_CVPR_2020_paper.pdf)
  - Bucketing Scheme, ECCV 2020, [[paper]](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123490392.pdf)
  - Distribution Focal Loss, NeurIPS 2020, [[paper]](https://proceedings.neurips.cc/paper/2020/file/f0bda020d2470f2e74990a07a607ebd9-Paper.pdf) 

## 3.2. IoU Distribution Imbalance <a name="3.2"></a>
- Cascade R-CNN, CVPR 2018, [[paper]](http://openaccess.thecvf.com/content_cvpr_2018/papers/Cai_Cascade_R-CNN_Delving_CVPR_2018_paper.pdf)
- Hierarchical Shot Detector, ICCV 2019, [[paper]](http://openaccess.thecvf.com/content_ICCV_2019/papers/Cao_Hierarchical_Shot_Detector_ICCV_2019_paper.pdf)
- IoU-uniform R-CNN, arXiv 2019, [[paper]](https://arxiv.org/pdf/1912.05190.pdf)
- pRoI Generator, WACV 2020, [[paper]](http://openaccess.thecvf.com/content_WACV_2020/papers/Oksuz_Generating_Positive_Bounding_Boxes_for_Balanced_Training_of_Object_Detectors_WACV_2020_paper.pdf)

## 3.3. Object Location Imbalance <a name="3.3"></a>
- Guided Anchoring, CVPR 2019, [[paper]](http://openaccess.thecvf.com/content_CVPR_2019/html/Wang_Region_Proposal_by_Guided_Anchoring_CVPR_2019_paper.html)
- FreeAnchor, NeurIPS 2019, [[paper]](https://papers.nips.cc/paper/8309-freeanchor-learning-to-match-anchors-for-visual-object-detection.pdf)

# 4. Objective Imbalance <a name="4"></a>
- Task Weighting
- Classification Aware Regression Loss, CVPR 2020, [[paper]](https://openaccess.thecvf.com/content_CVPR_2020/papers/Cao_Prime_Sample_Attention_in_Object_Detection_CVPR_2020_paper.pdf)
- Guided Loss, arXiv 2019, [[paper]](https://arxiv.org/pdf/1909.04868.pdf)
- aLRP Loss, NeurIPS 2020, [[paper]](https://papers.nips.cc/paper/2020/file/b2eeb7362ef83deff5c7813a67e14f0a-Paper.pdf)   

# Contact 
Please contact Kemal Öksüz (kemal.oksuz@metu.edu.tr) for your questions about this webpage.
