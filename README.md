# LabelNoiseMOIT
Official implementation for: "Multi-Objective Interpolation Training for Robustness to Label Noise"

Interpolated supervised contrastive learning and semi-supervised learning for robustness to label noise!
We achieve state-of-the-art results in CIFAR-10, CIFAR-100, Mini-ImageNet and Mini-WebVision!

Important note: Our method is robust in all scenarios with a single parametrization. We only modify typical training parameters (epochs, learning rate scheduling, batch size or memory size).

![plot](https://github.com/DiegoOrtego/LabelNoiseMOIT/blob/main/Overview.png)

Multi-Objective Interpolation Training (MOIT) for improved robustness to label noise. We interpolate samples and impose the same interpolation in the supervised contrastive learning loss (ICL) and the semi-supervised classification loss (SSL) that we jointly use during training. Label noise detection is performed at every epoch and its result is used after training MOIT to fine-tune the encoder and classifier to further boost performance with MOIT+.

CIFAR-10 and CIFAR-100 are downloaded automatically when setting "--download True". The dataset have to be placed in data folder (should be done automatically). We provide all code used to simulate label noise with symmetric and asymmetric distributions and provide example scripts to run our approach with both noises.

Main requirements:

Python 3.7.7
Pytorch 1.0.1 (torchvision 0.2.2)
Numpy 1.18.4
scikit-learn 0.23.2
cudatoolkit 9.0
cudnn 7.6.5




