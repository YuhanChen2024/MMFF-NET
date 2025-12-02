# :fire: MMFF-NET: Multi-layer and multi-scale feature fusion network for low-light infrared image enhancement

- :star: - [PAPER](https://link.springer.com/article/10.1007/s11760-023-02797-4)
- :star: - [DATESET](https://drive.google.com/file/d/1GAB3uGsmAyLgtDBDONbil08vVu5wJcG3/view) FROM [ZERO_DCE](https://github.com/Li-Chongyi/Zero-DCE)
- :star: - Pretrained Models `Epoch99.pth`

## Introduction

<img src="https://i.postimg.cc/13gThy48/1.png" alt="my" width="1000" style="display: block; margin: 0 auto;"/>

Most existing infrared image enhancement algorithms focus on detail and contrast enhancement of ordinary infrared imagesand when applied to low-light infrared images, detail and target texture are often severely lost. The reason is that mostalgorithms process images in a single scale and have difhiculty coping with the degradation of image features while enhancingbrightness. To solve this problem, we propose a multi-layer and multi-scale feature fusion network (MMFF-Net). It caimprove the brightness of low-light infrared images in the absence of normal-light reference samples and keep the imaeedetails consistent with the source image.In this paper, features at different layers of the image are extracted using an adaptivelymodifed deep network, A multi-scale adaptive feature fusion module (MAFF) is designed to preserve and fuse multi-scaleinfommation from different convolutional layer features. The fusion features are passed to the iterative function as pixel-wiseparameters for image brightness enhancement, We also propose the local feature fiusion module (LFFM), which reconstructsimages after fusing multiple features, including brightness enhancement images and source images. Finally, in order toimplement the training of the whole network, a set of loss functions is carefully designed in this paper. After extensiveexperiments, it is shown that the algorithm in this paper can effectively enhance low-light infrared images and perform wellin subjective visual tests and quantitative tests compared to existing methods.

## Getting Started

### Installation

1. Clone MMFF-NET.
```bash
git clone --recursive https://github.com/chenyuhan1997/MMFF-NET
cd MMFF-NET
# git submodule update --init --recursive
```

2. Create the environment, here we show an example using conda.
```bash
conda create -n mmff-net python=3.11
conda activate mmff-net
conda install pytorch torchvision pytorch-cuda=12.1 -c pytorch -c nvidia  # use the correct version of cuda for your system
pip install opencv, PIL, glob
```

### Train & Test

1. Train
```bash
python train.py --lowlight_images_path [dataset folder]
```

1. Test
```bash
python test.py [test_data/]
```

## Results on Low-light Image Enhancement

<img src="https://i.postimg.cc/VkSTQz5d/2.png" alt="my" width="1000" style="display: block; margin: 0 auto;"/>

## Citations

If you find this project helpful, please consider citing the following papers:

```
@article{zhu2023mmff,
  title={MMFF-NET: Multi-layer and multi-scale feature fusion network for low-light infrared image enhancement},
  author={Zhu, Ge and Chen, Yuhan and Wang, Xianquan and Zhang, Yiheng},
  journal={Signal, Image and Video Processing},
  pages={1--9},
  year={2023},
  publisher={Springer}
}
```
