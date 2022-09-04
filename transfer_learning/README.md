## Transfer Learning
subdomain:
* domain adaption
* Multi-task Learning
* Unsupervised Transfer Learning
  * 在这个方向可适用于的任务非常有限，比如 Dimension Reduction。由于缺乏 Source Label 因此也无法采用绝大部分的 Deep Learning 方法，（但比如Auto-encoder 是其中一个基于 Deep Learning 的降维方式，但很难归类于 Transfer Learning）


## Concept list

* MMD约束
* Inductive Transfer Learning
* Self-Taught Learning
* 解决 Catastrophic Forgetting
  * Progressive Neural Networks 
  * Full Bayesian posterior distribution
* Cross-Stitch Network ,解决多任务学习分叉问题，提出多任务的线性组合
* unbiased feature representation
  

## Papers
* [2010 (ref17730) (知乎推荐)a survey for TL](https://www3.ntu.edu.sg/home/sinnopan/publications/TLsurvey_0822.pdf) [local](transfer_learning/TLsurvey_0822.pdf)
* Deep Transfer Network: Unsupervised Domain Adaptation
* Learning Transferable Features with Deep Adaptation Networks
* Unsupervised Domain Adaptation by BackpropagationUnsupervised Domain Adaptation with Residual Transfer Networks(这篇文章我特别推荐一下，它打破了传统用一个分类器处理跨域数据，并首次提出用Residual Function来区分source classifier和target classifier)
* [打破catastrophic Forgetting](https://arxiv.org/pdf/1612.00796.pdf)
* [输出网络分叉-2：Zisserman†](transfer_learning/Doersch_Multi-Task_Self-Supervised_Visual_ICCV_2017_paper.pdf)
* [输出网络分叉-1: Cross-Stitch Network](transfer_learning/2016-cross-stitch-network.pdf)
* [transfer_learning/2017-avoid-catatrophical-forgetting.pdf](transfer_learning/2017-avoid-catatrophical-forgetting.pdf)
* [1] Wang B, Yao Y, Viswanath B, et al. With great training comes great vulnerability: Practical attacks against transfer learning[C]//27th {USENIX} Security Symposium ({USENIX} Security 18). 2018: 1281-1297.
* [2] Ji Y, Zhang X, Ji S, et al. Model-reuse attacks on deep learning systems[C]//Proceedings of the 2018 ACM SIGSAC conference on computer and communications security. 2018: 349-363.
* [3] Rezaei S, Liu X. A target-agnostic attack on deep models: Exploiting security vulnerabilities of transfer learning[C]. ICLR 2020.
* [4] Chin T W, Zhang C, Marculescu D. Renofeation: A Simple Transfer Learning Method for Improved Adversarial Robustness[C]//Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition. 2021: 3243-3252.
* [5] Yosinski J, Clune J, Bengio Y, et al. How transferable are features in deep neural networks? NIPS 2014
* [6] Neyshabur B, Sedghi H, Zhang C. What is being transferred in transfer learning? NeurIPS 2020.
* [transfer_learning/focal-loss.pdf](transfer_learning/focal-loss.pdf)
* Unsupervised Domain Adaptation by Backpropagation - 个人很喜欢这篇文章。这篇文章的新颖点是利用 classifier 在 Source 和 Target Domain 的相似性，通过 Source Domain 的 back-propagation 同时算出 Source 和 Target Domain 的 gradient 并将两者梯度结合来更新 feed-forward 的 feature extractor 。这样的设计会将 feature extractor 在没有 Target Label 的情况下也能学会 Target Domain 的 feature。
* Learning Transferable Features with Deep Adaptation Networks - 本文作者是清华大学的 Mingsheng Long 也是 Domain Adaptation 的专家，可从 Google Scholar 上看出他的近乎所有文章都在研究这个问题。这篇文章包括作者后续的文章里都用到了一个叫作 max mean discrepancies  (MMD) 定义为 Source Target Domain 的 feature 距离方式。将此距离包含于 loss function 会有助于网络避免出现 co-variant shift 使得学习到的特征是 domain-invariant。
* [github 迁移学习总结2021](https://github.com/jindongwang/transferlearning)
* [tensorflow 迁移学习教程](https://www.tensorflow.org/tutorials/images/transfer_learning)
* [(已读，尝试先把点云转换到统一的BEV形式，用图像预训练模型来做特征提取，叠加head进行目标检测分割等任务，启发不大。)Transfer Learning Based Semantic Segmentation for 3D ObjectDetection from Point Cloud](transfer_learning/sensors-21-03964-v2-lidar-transfer-learning.pdf)
* [Multisensor Online Transfer Learning for 3D LiDAR-Based Human Detection with a Mobile Robot](https://ieeexplore.ieee.org/document/8593899)
* [Multisensor Online Transfer Learning for 3D LiDAR-Based Human Detection with a Mobile Robot](https://arxiv.org/pdf/1801.04137.pdf)
* [ Efficient Online Transfer Learning for 3D Object Classification in Autonomous Driving](transfer_learning/Efficient_Online_Transfer_Learning_for_3D_Object_C.pdf)
* [Transfer_Learning_for_LiDAR-Based_Lane_Marking_Det](transfer_learning/Transfer_Learning_for_LiDAR-Based_Lane_Marking_Det.pdf)
* [Cross-Domain MLP and CNN Transfer Learning for Biological Signal Processing: EEG and EMG](https://ieeexplore.ieee.org/document/9027853)
* [SpinalNet: Deep Neural Network With Gradual Input](https://ieeexplore.ieee.org/document/9802918)
* [Multisensor Online Transfer Learning for 3D LiDAR-based Human Detection with a Mobile Robot]("transfer_learning/Multisensor Online Transfer Learning for 3D LiDAR-based Human Detection with a Mobile Robot.pdf")
* [(自动驾驶相关)2021-efficient-transfer-learning for lidar det](transfer_learning/2021-efficient-online-learning.pdf)
* [cross-modal-analysis](transfer_learning/linderIROS21-cross-modal-analysis.pdf)
* [transfer_learning/road-surface-det-and-segment.pdf](transfer_learning/road-surface-det-and-segment.pdf)
* [transfer_learning/2018-weight-tasks-2.pdf](transfer_learning/2018-weight-tasks-2.pdf)
* [transfer_learning/2018-weight-tasks-1.pdf](transfer_learning/2018-weight-tasks-1.pdf)
* [2017-unsupervized-domain-transfer-with-residue](transfer_learning/unsupervized-domain-transfer-with-residue.pdf)
* [2015-deep-transfer-net-par1](transfer_learning/2015-deep-transfer-net.pdf)
* [2015-deep-adaption-net-part2](transfer_learning/2015-deep-adaption-net.pdf)
* [gain15-unsupervized-domain-adaption](transfer_learning/ganin15-unsupervized-domain-adaption.pdf)


## structure

[structure](transfer_learning/transfer-learning-graph.jpg)