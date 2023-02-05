# ResNet

> [Deep Residual Learning for Image Recognition](https://openaccess.thecvf.com/content_cvpr_2016/html/He_Deep_Residual_Learning_CVPR_2016_paper.html)

<!-- [ALGORITHM] -->

## Introduction

**Residual Networks**, or **ResNets**, learn residual functions with reference to the layer inputs, instead of
learning unreferenced functions. In the mainstream previous works, like VGG, the neural networks are a stack
of layers and every layer attempts to fit a desired underlying mapping. In ResNets, a few stacked layers are
grouped as a block, and the layers in a block attempts to learn a residual mapping.

Formally, denoting the desired underlying mapping of a block as $\mathcal{H}(x)$, split the underlying mapping
into the sum of the identity and the residual mapping as $\mathcal{H}(x) = x + \mathcal{F}(x)$, and let the
stacked non-linear layers fit the residual mapping $\mathcal{F}(x)$.

Many works proved this method makes deep neural networks easier to optimize, and can gain accuracy from
considerably increased depth. Recently, the residual structure is widely used in various models.

<div align=center>
<img src="https://user-images.githubusercontent.com/26739999/142574068-60cfdeea-c4ec-4c49-abb2-5dc2facafc3b.png" width="40%"/>
</div>

## Abstract

<details>

<summary>Show the paper's abstract</summary>

<br>
Deeper neural networks are more difficult to train. We present a residual learning framework to ease the training of networks that are substantially deeper than those used previously. We explicitly reformulate the layers as learning residual functions with reference to the layer inputs, instead of learning unreferenced functions. We provide comprehensive empirical evidence showing that these residual networks are easier to optimize, and can gain accuracy from considerably increased depth. On the ImageNet dataset we evaluate residual nets with a depth of up to 152 layers---8x deeper than VGG nets but still having lower complexity. An ensemble of these residual nets achieves 3.57% error on the ImageNet test set. This result won the 1st place on the ILSVRC 2015 classification task. We also present analysis on CIFAR-10 with 100 and 1000 layers.

The depth of representations is of central importance for many visual recognition tasks. Solely due to our extremely deep representations, we obtain a 28% relative improvement on the COCO object detection dataset. Deep residual nets are foundations of our submissions to ILSVRC & COCO 2015 competitions, where we also won the 1st places on the tasks of ImageNet detection, ImageNet localization, COCO detection, and COCO segmentation.
</br>

</details>

## Results and models

|   Model   | Params(M) | Flops(G) | Top-1 (%) | Top-5 (%) |               Config               |                           Download                           |
| :-------: | :-------: | :------: | :-------: | :-------: | :--------------------------------: | :----------------------------------------------------------: |
| ResNet-50 |   23.518   |   4.109   |   55.9441   |   100   | [config](./resnet50_1xb8_in1k.py) | [model](https://pan.baidu.com/s/1MzDngDnI0fR_8CLJsq7JxQ) \| 提取码: jhol |
