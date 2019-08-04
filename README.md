[TOC]

# Awesome Adversarial Examples for Deep Learning



## Table of Contents

- [Survey](#Survey)
- [Attack](#Attack)
- [Defense](#Defense)
- [Competation](#Competation)
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

  

  



## Defense



## Competation



## ToolBox

* [**advertorch**](https://github.com/BorealisAI/advertorch)
* [**foolbox**](https://github.com/bethgelab/foolbox)
* [**cleverhans**](https://github.com/tensorflow/cleverhans)
* [**Adversarial-Face-Attack**](https://github.com/ppwwyyxx/Adversarial-Face-Attack)
* [**adversarial-robustness-toolbox**](https://github.com/IBM/adversarial-robustness-toolbox)