# Do You Need Sharpened Details? Asking MMDC-Net: Multi-layer Multi-scale Dilated Convolution Network For Retinal Vessel Segmentation
<a href="https://pytorch.org/"><img src="https://img.shields.io/badge/PyTorch-v1.9.0-red.svg?logo=PyTorch&style=for-the-badge" /></a>
<a href="#"><img src="https://img.shields.io/badge/python-v3.6+-blue.svg?logo=python&style=for-the-badge" /></a>

<<<<<<< HEAD
![input and output for a random image in the test dataset](/img/16_test.png)![input and output for a random label in the test dataset](/img/16_test_label.png)

>>>>>>> 7e954af8fa9e3d3ede2505e9875cc56cb0809da8


Customized implementation of the [MMDC-Net](https://xxx) in PyTorch

- [Quick start](#quick-start)
- [Description](#description)
- [Usage](#usage)
  - [Training](#training)
  - [Prediction](#prediction)
- [Model](#model)

## Quick start

1. [Install CUDA](https://developer.nvidia.com/cuda-downloads)

2. [Install PyTorch](https://pytorch.org/get-started/locally/)

3. Install dependencies
```bash
pip install -r requirements.txt
```

4. Download the data:
```bash
STARE  http://cecas.clemson.edu/~ahoover/stare/
CHASEDB1  https://blogs.kingston.ac.uk/retinal/chasedb1/
DRIVE  https://drive.grand-challenge.org/
HRF  https://www5.cs.fau.de/fileadmin/research/datasets/fundus-images 
```

## Description
This model is used to complete Binary classification image segmentation task. If you want to use this for multiple classes, modify n_classes.

It can be easily used for multiclass segmentation, portrait segmentation, medical segmentation, ...


## Usage
**Note : Use Python 3.6 or newer**


### Training

```bash

train: main.py 

```
By default, the `batchsize` is 2, so if you wish to obtain better results (but use better hardware), set it to 4/6/8 or more.

### Prediction

After training your model and saving it to `../models/xxx.pth`, you can easily test the output masks on your images.

To predict a single image and save it:

`please use test.py`

You can specify which model file to use with `../models/xxx.pth`.

## Model
If you want to see the detailed code of the model, go to '../core/models' and '../core/unet_parts'.


The input images and target labels of training should be in the `../data/train/image` and `../data/train/label` folders respectively (note that the `image` and `label` folder should not contain any sub-folder or any other files, due to the greedy data-loader). For datasets, images are RGB and labels are black and white.

Similarly,the input images and target labels of testing should be in the `../data/test/image` and `../data/test/label` folders respectively.

You can use your own dataset as long as you make sure it is loaded properly.

---

Original paper by Xiang Zhong, Hongbin Zhang,...:

[Do You Need Sharpened Details? Asking MMDC-Net: Multi-layer Multi-scale Dilated Convolution Network For Retinal Vessel Segmentation](https://xxx)

<<<<<<< HEAD
![network architecture](/img/network.png)
=======
![network architecture](/network.png)
>>>>>>> 7e954af8fa9e3d3ede2505e9875cc56cb0809da8
