# Awesome Adversarial Machine Learning [![Awesome](https://awesome.re/badge-flat.svg)](https://awesome.re)

A curated list of awesome AML attacks and defences frameworks and resources.

Also see [awesome-machine-learning](https://github.com/josephmisiti/awesome-machine-learning).

- [Awesome Adversarial Machine Learning](#awesome-adversarial-machine-learning-)
  - [Terminology](#terminology)
  - [Threat Modeling](#threat-modeling)
  - [Controls Guidelines](#controls-guidelines)
  - [Case Studies](#case-studies)
  - [Attacks based on method](#attacks-based-on-method)
  - [Attacks based on domain](#attacks-based-on-domain)
  - [Attacks based on strategy](#attacks-based-on-strategy)
  - [Defenses](#defenses)
  - [CTF and Hackathons](#ctf-and-hackathons)
  - [Frameworks](#frameworks)

## Terminology
* [NIST: A Taxonomy and Terminology of Adversarial Machine Learning](https://nvlpubs.nist.gov/nistpubs/ir/2019/NIST.IR.8269-draft.pdf)

## Threat Modeling
* [ENISA: Artificial Intelligence Cybersecurity Challenges](https://www.enisa.europa.eu/news/publications/artificial-intelligence-cybersecurity-challenges)
* [MITRE: Adversarial Threat Landscape for Artificial-Intelligence Systems](https://atlas.mitre.org/)
* [The Threat of Offensive AI to Organizations](https://arxiv.org/pdf/2106.15764.pdf)
* [Threat of Adversarial Attacks on Deep Learning in Computer Vision: A Survey](https://arxiv.org/abs/1801.00553)

## Controls Guidelines
* [ENISA: Securing Machine Learning Algorithms](https://www.enisa.europa.eu/publications/securing-machine-learning-algorithms)

## Case Studies
* [MITRE reports on in-the-wild](https://github.com/mitre/advmlthreatmatrix/blob/master/pages/case-studies-page.md#case-studies-page)
* [Avito fights content theft using adversarial noise](https://habr.com/ru/company/avito/blog/452142/)

## Attacks based on method
* [JSMA](https://ieeexplore.ieee.org/document/7467366)
* [One Pixel Attack](https://ieeexplore.ieee.org/abstract/document/8601309/)
* [DeepFool](https://arxiv.org/abs/1511.04599)
* [C&W](https://ieeexplore.ieee.org/abstract/document/7958570)
* [ATNs](https://arxiv.org/abs/1703.09387)
* [UPSET and ANGRI](https://arxiv.org/abs/1707.01159)
* Gradient-based:
  * [FGSM](https://arxiv.org/abs/1412.6572)
  * [Box-constrained L-BFGS](https://arxiv.org/pdf/1312.6199.pdf)
  * [I-FGSM](https://arxiv.org/abs/1607.02533)
  * [MI-FGSM](http://openaccess.thecvf.com/content_cvpr_2018/html/Dong_Boosting_Adversarial_Attacks_CVPR_2018_paper.html)
  * [DI^2-FGSM and M-DI^2FGSM](https://arxiv.org/abs/1803.06978)

Relationships between attacks:

<img src="./README.assert/relationship.png" width="300">

## Attacks based on domain
* Computer Vision
* Speech Recognition
  * Model-specific research
    * [Kaldi](https://github.com/lealeasch/adversarialattacks)
    * [Lingvo](https://github.com/yaq007/cleverhans/tree/master/examples/adversarial_asr)
    * [Deepspeech](https://arxiv.org/pdf/1801.01944)
  * Approaches
    * [Man-in-the-Elevator](https://www.usenix.org/sites/default/files/conference/protected-files/woot15_slides_vaidya.pdf)
  * Noise hiding techniques
    * [DolphinAttack](https://github.com/USSLab/DolphinAttack)
    * [MPEG Compression](https://arxiv.org/pdf/1808.05665)

## Attacks based on strategy
* Information gathering
  * [Membership inference](https://arxiv.org/pdf/1610.05820)
  * [Deanonymization](https://www.cs.utexas.edu/~shmat/shmat_oak08netflix.pdf)
  * [Model inversion](https://dl.acm.org/doi/10.1145/2810103.2813677)
  * [Model stealing](https://arxiv.org/pdf/1805.02628)
  * [Blind-spot detection](https://arxiv.org/pdf/1901.04684)
  * [State prediction](https://ieeexplore.ieee.org/document/8716085)
* Denial of Service
  * [Poisoning DoS](https://arxiv.org/pdf/1708.08689.pdf)
  * [Sponge examples](https://arxiv.org/pdf/2006.03463)


  
## Defenses

* Activation Functions
  * [JumpReLu](https://arxiv.org/pdf/1904.03750.pdf)
  * [BoundedReLu](https://arxiv.org/pdf/1707.06728.pdf)
* Network Distillation
  * [Distillation as a defense to adversarial perturbations against deep neural networks](http://ieeexplore.ieee.org/abstract/document/7546524/) Papernot, Nicolas, et al.Security and Privacy (SP), 2016 IEEE Symposium on. IEEE, 2016.
* Adversarial (Re)Training
  * [Learning with a strong adversary](https://arxiv.org/abs/1511.03034) Huang, Ruitong, et al. arXiv preprint arXiv:1511.03034 (2015).
  * [Adversarial machine learning at scale](https://arxiv.org/abs/1611.01236) Kurakin, Alexey, Ian Goodfellow, and Samy Bengio. ICLR. 2017.
  * [Ensemble Adversarial Training: Attacks and Defenses](https://arxiv.org/abs/1705.07204) Tramèr, Florian, et al. arXiv preprint arXiv:1705.07204 (2017).
  * [Adversarial training for relation extraction](http://www.aclweb.org/anthology/D17-1187) Wu, Yi, David Bamman, and Stuart Russell. Proceedings of the 2017 Conference on Empirical Methods in Natural Language Processing. 2017.
  * [Adversarial Logit Pairing](https://arxiv.org/abs/1803.06373) Harini Kannan, Alexey Kurakin, Ian Goodfellow. arXiv preprint arXiv:1803.06373 (2018).
* Adversarial Detecting
  * [Detecting Adversarial Samples from Artifacts](https://arxiv.org/abs/1703.00410) Feinman, Reuben, et al. arXiv preprint arXiv:1703.00410 (2017).
  * [Adversarial and Clean Data Are Not Twins](https://arxiv.org/abs/1704.04960) Gong, Zhitao, Wenlu Wang, and Wei-Shinn Ku. arXiv preprint arXiv:1704.04960 (2017).
  * [Safetynet: Detecting and rejecting adversarial examples robustly](https://arxiv.org/abs/1704.00103) Lu, Jiajun, Theerasit Issaranon, and David Forsyth. ICCV (2017).
  * [On the (statistical) detection of adversarial examples](https://arxiv.org/abs/1702.06280) Grosse, Kathrin, et al. arXiv preprint arXiv:1702.06280 (2017).
  * [On detecting adversarial perturbations](https://arxiv.org/abs/1702.04267) Metzen, Jan Hendrik, et al. ICLR Poster. 2017.
  * [Early Methods for Detecting Adversarial Images](https://openreview.net/forum?id=B1dexpDug&noteId=B1dexpDug) Hendrycks, Dan, and Kevin Gimpel. ICLR Workshop (2017).
  * [Dimensionality Reduction as a Defense against Evasion Attacks on Machine Learning Classifiers](https://arxiv.org/abs/1704.02654) Bhagoji, Arjun Nitin, Daniel Cullina, and Prateek Mittal. arXiv preprint arXiv:1704.02654 (2017).
  * [Detecting Adversarial Attacks on Neural Network Policies with Visual Foresight](https://arxiv.org/abs/1710.00814) Lin, Yen-Chen, et al. arXiv preprint arXiv:1710.00814 (2017).
  * [PixelDefend: Leveraging Generative Models to Understand and Defend against Adversarial Examples](https://arxiv.org/abs/1710.10766) Song, Yang, et al. arXiv preprint arXiv:1710.10766 (2017).
* Input Reconstruction
  * [PixelDefend: Leveraging Generative Models to Understand and Defend against Adversarial Examples](https://arxiv.org/abs/1710.10766) Song, Yang, et al. arXiv preprint arXiv:1710.10766 (2017).
  * [MagNet: a Two-Pronged Defense against Adversarial Examples](https://arxiv.org/abs/1705.09064) Meng, Dongyu, and Hao Chen. CCS (2017).
  * [Towards deep neural network architectures robust to adversarial examples](https://arxiv.org/abs/1412.5068) Gu, Shixiang, and Luca Rigazio. arXiv preprint arXiv:1412.5068 (2014).
* Classifier Robustifying
  * [Adversarial Examples, Uncertainty, and Transfer Testing Robustness in Gaussian Process Hybrid Deep Networks](https://arxiv.org/abs/1707.02476) Bradshaw, John, Alexander G. de G. Matthews, and Zoubin Ghahramani.arXiv preprint arXiv:1707.02476 (2017).
  * [Robustness to Adversarial Examples through an Ensemble of Specialists](https://arxiv.org/abs/1702.06856) Abbasi, Mahdieh, and Christian Gagné. arXiv preprint arXiv:1702.06856 (2017).
* Network Verification
  * [Reluplex: An efficient SMT solver for verifying deep neural networks](https://arxiv.org/abs/1702.01135) Katz, Guy, et al. CAV 2017.
  * [Safety verification of deep neural networks](https://link.springer.com/chapter/10.1007/978-3-319-63387-9_1) Huang, Xiaowei, et al. International Conference on Computer Aided Verification. Springer, Cham, 2017.
  * [Towards proving the adversarial robustness of deep neural networks](https://arxiv.org/abs/1709.02802) Katz, Guy, et al. arXiv preprint arXiv:1709.02802 (2017).
  * [Deepsafe: A data-driven approach for checking adversarial robustness in neural networks](https://arxiv.org/abs/1710.00486) Gopinath, Divya, et al. arXiv preprint arXiv:1710.00486 (2017).
  * [DeepXplore: Automated Whitebox Testing of Deep Learning Systems](https://arxiv.org/abs/1705.06640) Pei, Kexin, et al. arXiv preprint arXiv:1705.06640 (2017).
* Others
  * [Adversarial Example Defenses: Ensembles of Weak Defenses are not Strong](https://arxiv.org/abs/1706.04701) He, Warren, et al. 11th USENIX Workshop on Offensive Technologies (WOOT 17). (2017).
  * [Adversarial Examples Are Not Easily Detected: Bypassing Ten Detection Methods](https://arxiv.org/abs/1705.07263) Carlini, Nicholas, and David Wagner. AISec. 2017.

## CTF and Hackathons

* [NIPS 2017: Defense Against Adversarial Attack](https://www.kaggle.com/c/nips-2017-defense-against-adversarial-attack/data)
* [NIPS 2018 : Adversarial Vision Challenge](https://www.crowdai.org/challenges)
* [GeekPwn CAAD 2018](http://2018.geekpwn.org/en/index.html#4).
* [IJCAI-19 Alibaba Adversarial AI Challenge](https://tianchi.aliyun.com/markets/tianchi/ijcai19_en)
* [GeekPwn CAAD 2019](http://www.geekpwn.org/zh/index.html)
* [Positive Hack Days 2019: AI CTF](https://2019.phdays.com/en/program/contests/aI-ctf/)
* [UTCTF 2019 (FaceSafe, Bot Protection IV tasks)](https://github.com/utisss/UTCTF-19)
* [vishwaCTF21 (Good Driver Bad Driver task)](https://vishwactf.com/)

## Frameworks
* [**adversarial-robustness-toolbox**](https://github.com/IBM/adversarial-robustness-toolbox)
* [**foolbox**](https://github.com/bethgelab/foolbox)
* [**cleverhans**](https://github.com/tensorflow/cleverhans)
* [**Adversarial-Face-Attack**](https://github.com/ppwwyyxx/Adversarial-Face-Attack)
* [**adversarial.js**](https://github.com/kennysong/adversarial.js)
* [**advertorch**](https://github.com/BorealisAI/advertorch)
