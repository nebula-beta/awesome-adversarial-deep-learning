[TOC]

# Awesome Adversarial Examples for Deep Learning



## Table of Contents

- [Adversarial attack](#adversarial attack)
- [Adversarial defense](#Adversarial defense)
- [ToolBox](#ToolBox)





[Threat of Adversarial Attacks on Deep Learning in Computer Vision: A Survey](https://arxiv.org/abs/1801.00553)



## Adversarial attack

### White-box attack

#### Gradient-base method

Intriguing properties of neural networks,

- **Box-constrained L-BFGS :** [Intriguing properties of neural networks](https://arxiv.org/pdf/1312.6199.pdf). Szegedy, Christian, et al. ICLR(Poster) 2014.

* **FGSM :** [Explaining and harnessing adversarial examples](https://arxiv.org/abs/1412.6572). Goodfellow, Ian J., Jonathon Shlens, and Christian Szegedy. ICLR(Poster) 2015. [[code](https://github.com/1Konny/FGSM), ]
* **I-FGSM :**  [Adversarial examples in the physical world](https://arxiv.org/abs/1607.02533). Kurakin, Alexey, Ian Goodfellow, and Samy Bengio. ICLR(Workshop) 2017. [[code](https://github.com/1Konny/FGSM), ]
* **MI-FGSM :** [Boosting Adversarial Attacks with Momentum](http://openaccess.thecvf.com/content_cvpr_2018/html/Dong_Boosting_Adversarial_Attacks_CVPR_2018_paper.html).  Dong Y , Liao F , Pang T , et al. CVPR 2017. [[poster](http://ml.cs.tsinghua.edu.cn/~yinpeng/poster/Attack-CVPR2018.pdf), [code]()]
* **DI^2-FGSM/M-DI^2FGSM :**  [Improving Transferability of Adversarial Examples with Input Diversity](https://arxiv.org/abs/1803.06978). Xie, Cihang, et al. CVPR 2019. [[code](https://github.com/cihangxie/DI-2-FGSM), ]



**Relationships between different attacks：**

![relationship.png](./README.assert/relationship.png)







- **DeepFool :** [DeepFool: a simple and accurate method to fool deep neural networks](https://arxiv.org/abs/1511.04599). S. Moosavi-Dezfooli et al., CVPR 2016. 



**1 Box-constrained L-BFGS**

Szegedy[22] 等人首次证明了可以通过对图像添加小量的人类察觉不到的扰动误导神经网络做出误分类。他们首先尝试求解让神经网络做出误分类的最小扰动的方程。但由于问题的复杂度太高，他们转而求解简化后的问题，即寻找最小的损失函数添加项，使得神经网络做出误分类，这就将问题转化成了凸优化过程。

C. Szegedy, W. Zaremba, I. Sutskever, J. Bruna, D. Erhan, I. Goodfellow, R. Fergus, Intriguing properties of neural networks, arXiv preprint arXiv:1312.6199, 2014.

**2 Fast Gradient Sign Method (FGSM)**

Szegedy 等人发现可以通过对抗训练提高深度神经网络的鲁棒性，从而提升防御对抗样本攻击的能力。GoodFellow[23] 等人开发了一种能有效计算对抗扰动的方法。而求解对抗扰动的方法在原文中就被称为 FGSM。

I. J. Goodfellow, J. Shlens, C. Szegedy, Explaining and Harnessing Adversarial Examples, arXiv preprint arXiv:1412.6572, 2015.

Kurakin[80] 等人提出了 FGSM 的「one-step target class」的变体。通过用识别概率最小的类别（目标类别）代替对抗扰动中的类别变量，再将原始图像减去该扰动，原始图像就变成了对抗样本，并能输出目标类别。

A. Kurakin, I. Goodfellow, S. Bengio, Adversarial Machine Learning at Scale, arXiv preprint arXiv:1611.01236, 2017.

**3 Basic & Least-Likely-Class Iterative Methods**

one-step 方法通过一大步运算增大分类器的损失函数而进行图像扰动，因而可以直接将其扩展为通过多个小步增大损失函数的变体，从而我们得到 Basic Iterative Methods（BIM）[35]。而该方法的变体和前述方法类似，通过用识别概率最小的类别（目标类别）代替对抗扰动中的类别变量，而得到 Least-Likely-Class Iterative Methods[35]。

A. Kurakin, I. Goodfellow, S. Bengio, Adversarial examples in the physical world, arXiv preprint arXiv:1607.02533, 2016.

**4 Jacobian-based Saliency Map Attack (JSMA)**

对抗攻击文献中通常使用的方法是限制扰动的 l_∞或 l_2 范数的值以使对抗样本中的扰动无法被人察觉。但 JSMA[60] 提出了限制 l_0 范数的方法，即仅改变几个像素的值，而不是扰动整张图像。

N. Papernot, P. McDaniel, S. Jha, M. Fredrikson, Z. B. Celik, A. Swami, The Limitations of Deep Learning in Adversarial Settings, In Proceedings of IEEE European Symposium on Security and Privacy, 2016.

**5 One Pixel Attack**

这是一种极端的对抗攻击方法，仅改变图像中的一个像素值就可以实现对抗攻击。Su[68] 等人使用了差分进化算法，对每个像素进行迭代地修改生成子图像，并与母图像对比，根据选择标准保留攻击效果最好的子图像，实现对抗攻击。这种对抗攻击不需要知道网络参数或梯度的任何信息。

J. Su, D. V. Vargas, S. Kouichi, One pixel attack for fooling deep neural networks, arXiv preprint arXiv:1710.08864, 2017.

**6 Carlini and Wagner Attacks (C&W)**

Carlini 和 Wagner[36] 提出了三种对抗攻击方法，通过限制 l_∞、l_2 和 l_0 范数使得扰动无法被察觉。实验证明 defensive distillation 完全无法防御这三种攻击。该算法生成的对抗扰动可以从 unsecured 的网络迁移到 secured 的网络上，从而实现黑箱攻击。

N. Carlini, D. Wagner, Towards Evaluating the Robustness of Neural Networks, arXiv preprint arXiv:1608.04644, 2016.

**7 DeepFool**

Moosavi-Dezfooli 等人 [72] 通过迭代计算的方法生成最小规范对抗扰动，将位于分类边界内的图像逐步推到边界外，直到出现错误分类。作者证明他们生成的扰动比 FGSM 更小，同时有相似的欺骗率。

S. Moosavi-Dezfooli, A. Fawzi, P. Frossard, DeepFool: a simple and accurate method to fool deep neural networks, In Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition, pp. 2574-2582, 2016.

**8 Universal Adversarial Perturbations**

诸如 FGSM [23]、 ILCM [35]、 DeepFool [72] 等方法只能生成单张图像的对抗扰动，而 Universal Adversarial Perturbations[16] 能生成对任何图像实现攻击的扰动，这些扰动同样对人类是几乎不可见的。该论文中使用的方法和 DeepFool 相似，都是用对抗扰动将图像推出分类边界，不过同一个扰动针对的是所有的图像。虽然文中只针对单个网络 ResNet 进行攻击，但已证明这种扰动可以泛化到其它网络上。

S. M. Moosavi-Dezfooli, A. Fawzi, O. Fawzi and P. Frossard, Universal adversarial perturbations. In Proceedings of IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 2017.



**9 UPSET and ANGRI**

Sarkar[146] 等人提出了两个黑箱攻击算法，UPSET 和 ANGRI。UPSET 可以为特定的目标类别生成对抗扰动，使得该扰动添加到任何图像时都可以将该图像分类成目标类别。相对于 UPSET 的「图像不可知」扰动，ANGRI 生成的是「图像特定」的扰动。它们都在 MNIST 和 CIFAR 数据集上获得了高欺骗率。

S. Sarkar, A. Bansal, U. Mahbub, and R. Chellappa, UPSET and ANGRI: Breaking High Performance Image Classifiers, arXiv preprint arXiv:1707.01159, 2017.

**10 Houdini**

Houdini[131] 是一种用于欺骗基于梯度的机器学习算法的方法，通过生成特定于任务损失函数的对抗样本实现对抗攻击，即利用网络的可微损失函数的梯度信息生成对抗扰动。除了图像分类网络，该算法还可以用于欺骗语音识别网络。

M. Cisse, Y. Adi, N. Neverova, and J. Keshet, Houdini: Fooling deep structured prediction models, arXiv preprint arXiv:1707.05373, 2017.

**11 Adversarial Transformation Networks (ATNs)**

Baluja 和 Fischer[42] 训练了多个前向神经网络来生成对抗样本，可用于攻击一个或多个网络。该算法通过最小化一个联合损失函数来生成对抗样本，该损失函数有两个部分，第一部分使对抗样本和原始图像保持相似，第二部分使对抗样本被错误分类。

S. Baluja, I. Fischer, Adversarial Transformation Networks: Learning to Generate Adversarial Examples, arXiv preprint arXiv:1703.09387, 2017.



### Black-box attack



## Adversarial defense 



## Competation



## ToolBox

* [**advertorch**](https://github.com/BorealisAI/advertorch)
* [**foolbox**](https://github.com/bethgelab/foolbox)
* [**cleverhans**](https://github.com/tensorflow/cleverhans)
* [**Adversarial-Face-Attack**](https://github.com/ppwwyyxx/Adversarial-Face-Attack)
* [**adversarial-robustness-toolbox**](https://github.com/IBM/adversarial-robustness-toolbox)