[TOC]

# Awesome Adversarial Examples for Deep Learning



## Table of Contents

- [Survey](#Survey)
- [Attack](#Attack)
- [Defense](#Defense)
- [Competition](#Competition)
- [ToolBox](#ToolBox)





## Survey

[Threat of Adversarial Attacks on Deep Learning in Computer Vision: A Survey](https://arxiv.org/abs/1801.00553)



## Attack

### Gradient-base method

- **Box-constrained L-BFGS :** [Intriguing properties of neural networks](https://arxiv.org/pdf/1312.6199.pdf). Szegedy, Christian, et al. ICLR(Poster) 2014. [[blogs](https://www.cnblogs.com/lainey/p/8552422.html)]

* **FGSM :** [Explaining and harnessing adversarial examples](https://arxiv.org/abs/1412.6572). Goodfellow, Ian J., Jonathon Shlens, and Christian Szegedy. ICLR(Poster) 2015. [[code](https://github.com/1Konny/FGSM), ]
* **I-FGSM :**  [Adversarial examples in the physical world](https://arxiv.org/abs/1607.02533). Kurakin, Alexey, Ian Goodfellow, and Samy Bengio. ICLR(Workshop) 2017. [[code](https://github.com/1Konny/FGSM), ]
* **MI-FGSM :** [Boosting Adversarial Attacks with Momentum](http://openaccess.thecvf.com/content_cvpr_2018/html/Dong_Boosting_Adversarial_Attacks_CVPR_2018_paper.html).  Dong Y , Liao F , Pang T , et al. CVPR 2017. [[poster](http://ml.cs.tsinghua.edu.cn/~yinpeng/poster/Attack-CVPR2018.pdf), [code]()]
* **DI^2-FGSM and M-DI^2FGSM :**  [Improving Transferability of Adversarial Examples with Input Diversity](https://arxiv.org/abs/1803.06978). Xie, Cihang, et al. CVPR 2019. [[code](https://github.com/cihangxie/DI-2-FGSM), ]



**Relationships between above different attacks：**

<img src="./README.assert/relationship.png" width="50%" height="50%">





* **JSMA :** [The limitations of deep learning in adversarial settings](https://ieeexplore.ieee.org/document/7467366). Papernot, Nicolas, et al. (EuroS&P)*. IEEE, 2016.
* **One Pixel Attack :** [One pixel attack for fooling deep neural networks](https://ieeexplore.ieee.org/abstract/document/8601309/).  J. Su, D. V. Vargas, S. Kouichi.  arXiv preprint arXiv:1710.08864, 2017.
* **DeepFool :** [DeepFool: a simple and accurate method to fool deep neural networks](https://arxiv.org/abs/1511.04599). S. Moosavi-Dezfooli et al., CVPR 2016. 
* **C&W :** [Towards Evaluating the Robustness of Neural Networks](https://ieeexplore.ieee.org/abstract/document/7958570).  N. Carlini, D. Wagner. arXiv preprint arXiv:1608.04644, 2016.
* **ATNs :**[Adversarial Transformation Networks: Learning to Generate Adversarial Examples](https://arxiv.org/abs/1703.09387).  S. Baluja, I. Fischer. arXiv preprint arXiv:1703.09387, 2017.
* **UPSET and ANGRI :**  [UPSET and ANGRI: Breaking High Performance Image Classifiers](https://arxiv.org/abs/1707.01159). Sarkar, A. Bansal, U. Mahbub, and R. Chellappa. arXiv preprint arXiv:1707.01159, 2017.





- [Intriguing properties of neural networks](https://arxiv.org/pdf/1312.6199.pdf) Szegedy, Christian, et al.  arXiv preprint arXiv:1312.6199 (2013).
- [Explaining and harnessing adversarial examples](https://arxiv.org/abs/1412.6572) Goodfellow, Ian J., Jonathon Shlens, and Christian Szegedy. arXiv preprint arXiv:1412.6572 (2014).
- [Deep neural networks are easily fooled: High confidence predictions for unrecognizable images](https://www.cv-foundation.org/openaccess/content_cvpr_2015/html/Nguyen_Deep_Neural_Networks_2015_CVPR_paper.html) Nguyen, Anh, Jason Yosinski, and Jeff Clune. Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition. 2015.
- [Adversarial examples in the physical world](https://arxiv.org/abs/1607.02533) Kurakin, Alexey, Ian Goodfellow, and Samy Bengio. arXiv preprint arXiv:1607.02533 (2016).
- [Adversarial diversity and hard positive generation](https://www.cv-foundation.org/openaccess/content_cvpr_2016_workshops/w12/html/Rozsa_Adversarial_Diversity_and_CVPR_2016_paper.html) Rozsa, Andras, Ethan M. Rudd, and Terrance E. Boult. Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition Workshops. 2016.
- [The limitations of deep learning in adversarial settings](http://ieeexplore.ieee.org/abstract/document/7467366/) Papernot, Nicolas, et al. Security and Privacy (EuroS&P), 2016 IEEE European Symposium on. IEEE, 2016.
- [Adversarial manipulation of deep representations](https://arxiv.org/abs/1511.05122) Sabour, Sara, et al. ICLR. 2016.
- [Deepfool: a simple and accurate method to fool deep neural networks](https://www.cv-foundation.org/openaccess/content_cvpr_2016/html/Moosavi-Dezfooli_DeepFool_A_Simple_CVPR_2016_paper.html) Moosavi-Dezfooli, Seyed-Mohsen, Alhussein Fawzi, and Pascal Frossard. Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition. 2016.
- [Universal adversarial perturbations](https://arxiv.org/abs/1610.08401) Moosavi-Dezfooli, Seyed-Mohsen, et al. IEEE Conference on Computer Vision and Pattern Recognition (CVPR). 2017.
- [Towards evaluating the robustness of neural networks](https://arxiv.org/abs/1608.04644) Carlini, Nicholas, and David Wagner. Security and Privacy (S&P). 2017.
- [Machine Learning as an Adversarial Service: Learning Black-Box Adversarial Examples](https://arxiv.org/abs/1708.05207) Hayes, Jamie, and George Danezis. arXiv preprint arXiv:1708.05207 (2017).
- [Zoo: Zeroth order optimization based black-box attacks to deep neural networks without training substitute models](https://arxiv.org/abs/1708.03999) Chen, Pin-Yu, et al. 10th ACM Workshop on Artificial Intelligence and Security (AISEC) with the 24th ACM Conference on Computer and Communications Security (CCS). 2017.
- [Ground-Truth Adversarial Examples](https://arxiv.org/abs/1709.10207) Carlini, Nicholas, et al. arXiv preprint arXiv:1709.10207. 2017.
- [Generating Natural Adversarial Examples](https://arxiv.org/abs/1710.11342) Zhao, Zhengli, Dheeru Dua, and Sameer Singh. arXiv preprint arXiv:1710.11342. 2017.
- [Obfuscated Gradients Give a False Sense of Security: Circumventing Defenses to Adversarial Examples](https://arxiv.org/abs/1802.00420) Anish Athalye, Nicholas Carlini, David Wagner. arXiv preprint arXiv:1802.00420. 2018.





## Defense

### Network Ditillation

- [Distillation as a defense to adversarial perturbations against deep neural networks](http://ieeexplore.ieee.org/abstract/document/7546524/) Papernot, Nicolas, et al.Security and Privacy (SP), 2016 IEEE Symposium on. IEEE, 2016.

### Adversarial (Re)Training
- [Learning with a strong adversary](https://arxiv.org/abs/1511.03034) Huang, Ruitong, et al. arXiv preprint arXiv:1511.03034 (2015).
- [Adversarial machine learning at scale](https://arxiv.org/abs/1611.01236) Kurakin, Alexey, Ian Goodfellow, and Samy Bengio. ICLR. 2017.
- [Ensemble Adversarial Training: Attacks and Defenses](https://arxiv.org/abs/1705.07204) Tramèr, Florian, et al. arXiv preprint arXiv:1705.07204 (2017).
- [Adversarial training for relation extraction](http://www.aclweb.org/anthology/D17-1187) Wu, Yi, David Bamman, and Stuart Russell. Proceedings of the 2017 Conference on Empirical Methods in Natural Language Processing. 2017.
- [Adversarial Logit Pairing](https://arxiv.org/abs/1803.06373) Harini Kannan, Alexey Kurakin, Ian Goodfellow. arXiv preprint arXiv:1803.06373 (2018).

### Adversarial Detecting
- [Detecting Adversarial Samples from Artifacts](https://arxiv.org/abs/1703.00410) Feinman, Reuben, et al. arXiv preprint arXiv:1703.00410 (2017).
- [Adversarial and Clean Data Are Not Twins](https://arxiv.org/abs/1704.04960) Gong, Zhitao, Wenlu Wang, and Wei-Shinn Ku. arXiv preprint arXiv:1704.04960 (2017).
- [Safetynet: Detecting and rejecting adversarial examples robustly](https://arxiv.org/abs/1704.00103) Lu, Jiajun, Theerasit Issaranon, and David Forsyth. ICCV (2017).
- [On the (statistical) detection of adversarial examples](https://arxiv.org/abs/1702.06280) Grosse, Kathrin, et al. arXiv preprint arXiv:1702.06280 (2017).
- [On detecting adversarial perturbations](https://arxiv.org/abs/1702.04267) Metzen, Jan Hendrik, et al. ICLR Poster. 2017.
- [Early Methods for Detecting Adversarial Images](https://openreview.net/forum?id=B1dexpDug&noteId=B1dexpDug) Hendrycks, Dan, and Kevin Gimpel. ICLR Workshop (2017).
- [Dimensionality Reduction as a Defense against Evasion Attacks on Machine Learning Classifiers](https://arxiv.org/abs/1704.02654) Bhagoji, Arjun Nitin, Daniel Cullina, and Prateek Mittal. arXiv preprint arXiv:1704.02654 (2017).
- [Detecting Adversarial Attacks on Neural Network Policies with Visual Foresight](https://arxiv.org/abs/1710.00814) Lin, Yen-Chen, et al. arXiv preprint arXiv:1710.00814 (2017).
- [PixelDefend: Leveraging Generative Models to Understand and Defend against Adversarial Examples](https://arxiv.org/abs/1710.10766) Song, Yang, et al. arXiv preprint arXiv:1710.10766 (2017).

### Input Reconstruction
- [PixelDefend: Leveraging Generative Models to Understand and Defend against Adversarial Examples](https://arxiv.org/abs/1710.10766) Song, Yang, et al. arXiv preprint arXiv:1710.10766 (2017).
- [MagNet: a Two-Pronged Defense against Adversarial Examples](https://arxiv.org/abs/1705.09064) Meng, Dongyu, and Hao Chen. CCS (2017).
- [Towards deep neural network architectures robust to adversarial examples](https://arxiv.org/abs/1412.5068) Gu, Shixiang, and Luca Rigazio. arXiv preprint arXiv:1412.5068 (2014).

### Classifier Robustifying
- [Adversarial Examples, Uncertainty, and Transfer Testing Robustness in Gaussian Process Hybrid Deep Networks](https://arxiv.org/abs/1707.02476) Bradshaw, John, Alexander G. de G. Matthews, and Zoubin Ghahramani.arXiv preprint arXiv:1707.02476 (2017).
- [Robustness to Adversarial Examples through an Ensemble of Specialists](https://arxiv.org/abs/1702.06856) Abbasi, Mahdieh, and Christian Gagné. arXiv preprint arXiv:1702.06856 (2017).

### Network Verification
- [Reluplex: An efficient SMT solver for verifying deep neural networks](https://arxiv.org/abs/1702.01135) Katz, Guy, et al. CAV 2017.
- [Safety verification of deep neural networks](https://link.springer.com/chapter/10.1007/978-3-319-63387-9_1) Huang, Xiaowei, et al. International Conference on Computer Aided Verification. Springer, Cham, 2017.
- [Towards proving the adversarial robustness of deep neural networks](https://arxiv.org/abs/1709.02802) Katz, Guy, et al. arXiv preprint arXiv:1709.02802 (2017).
- [Deepsafe: A data-driven approach for checking adversarial robustness in neural networks](https://arxiv.org/abs/1710.00486) Gopinath, Divya, et al. arXiv preprint arXiv:1710.00486 (2017).
- [DeepXplore: Automated Whitebox Testing of Deep Learning Systems](https://arxiv.org/abs/1705.06640) Pei, Kexin, et al. arXiv preprint arXiv:1705.06640 (2017).

### Others
- [Adversarial Example Defenses: Ensembles of Weak Defenses are not Strong](https://arxiv.org/abs/1706.04701) He, Warren, et al. 11th USENIX Workshop on Offensive Technologies (WOOT 17). (2017).
- [Adversarial Examples Are Not Easily Detected: Bypassing Ten Detection Methods](https://arxiv.org/abs/1705.07263) Carlini, Nicholas, and David Wagner. AISec. 2017.



## Competition

* [NIPS 2017: Defense Against Adversarial Attack](https://www.kaggle.com/c/nips-2017-defense-against-adversarial-attack/data)
* [NIPS 2018 : Adversarial Vision Challenge](https://www.crowdai.org/challenges)
* [GeekPwn CAAD 2018](http://2018.geekpwn.org/en/index.html#4).  [Winners](http://hof.geekpwn.org/caad/en/index2.html)

* [IJCAI-19 Alibaba Adversarial AI Challenge](https://tianchi.aliyun.com/markets/tianchi/ijcai19_en)
* [GeekPwn CAAD 2019](http://www.geekpwn.org/zh/index.html)





## ToolBox

* [**advertorch**](https://github.com/BorealisAI/advertorch)
* [**foolbox**](https://github.com/bethgelab/foolbox)
* [**cleverhans**](https://github.com/tensorflow/cleverhans)
* [**Adversarial-Face-Attack**](https://github.com/ppwwyyxx/Adversarial-Face-Attack)
* [**adversarial-robustness-toolbox**](https://github.com/IBM/adversarial-robustness-toolbox)