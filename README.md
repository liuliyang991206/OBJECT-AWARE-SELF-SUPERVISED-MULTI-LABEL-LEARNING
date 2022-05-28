# Object-Aware-Self-Supervised-Multi-Label-Learning
The official implementation of "OBJECT-AWARE SELF-SUPERVISED MULTI-LABEL LEARNING".

## Citation
- Accepted to ICIP 2022
- Please cite our paper if the code is helpful to your research. [arxiv](https://doi.org/10.48550/arXiv.2205.07028)
```
@misc{https://doi.org/10.48550/arxiv.2205.07028,
  doi = {10.48550/ARXIV.2205.07028},
  url = {https://arxiv.org/abs/2205.07028},
  author = {Kaixin, Xu and Liyang, Liu and Ziyuan, Zhao and Zeng, Zeng and Veeravalli, Bharadwaj},
  keywords = {Computer Vision and Pattern Recognition (cs.CV), FOS: Computer and information sciences, FOS: Computer and information sciences},
  title = {Object-Aware Self-supervised Multi-Label Learning},
  publisher = {arXiv},
  year = {2022},
  copyright = {arXiv.org perpetual, non-exclusive license}
}
```

## Abstract
Multi-label Learning on Image data has been widely exploited with deep learning models. However, supervised training on deep CNN models often cannot discover sufficient discriminative features for classification. As a result, numerous self-supervision methods are proposed to learn more robust image representations. However, most self-supervised approaches focus on single-instance single-label data and fall short on more complex images with multiple objects. Therefore, we propose an Object-Aware Self Supervision (OASS) method to obtain more fine-grained representations for multi-label learning, dynamically generating auxiliary tasks based on object locations. Secondly, the robust representation learned by OASS can be leveraged to efficiently generate Class-Specific Instances (CSI) in a proposal-free fashion to better guide multi-label supervision signal transfer to instances. Extensive experiments on the VOC2012 dataset for multi-label classification demonstrate the effectiveness of the proposed method against the state-of-the-art counterparts.

## Overview
![Overall architecture](./res/figure_2.PNG)

<br>

# Prerequisite
- Python 3.8, PyTorch 1.7.0, and more in requirements.txt
- CUDA 10.1, cuDNN 7.6.5
- 4 x Titan RTX GPUs

# Usage

## Install python dependencies
```bash
python3 -m pip install -r requirements.txt
```

## Download PASCAL VOC 2012 devkit
Follow instructions in http://host.robots.ox.ac.uk/pascal/VOC/voc2012/#devkit

## 1. Train an image classifier for generating CAMs
