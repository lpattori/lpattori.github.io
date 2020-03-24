---
layout: default
modal-id: 1
date: 2020-02-24
img: pneumo.png
alt: image-alt
project-date: February 2020
client:
category: Medical Image-Segmentation Deep-Learning
short_description: Pneumothorax Segmentation
url-docs: "https://blog.pattori.com/pneumo"
url-demo: "https://pneumot.herokuapp.com"
is-slow: true
description: From a thorax x-ray the neural network will highlight the pneumothorax affected zone. The model has been trained with images from the <a href="https://www.kaggle.com/vbookshelf/pneumothorax-chest-xray-images-and-masks">SIIM-ACR Pneumothorax Segmentations</a>.
---
# Pneumothorax Segmentation


1. TOC
{:toc}

## Dataset

The Deep Learning neural network module has been trained with images from the [SIIM-ACR Pneumothorax Segmentations](https://www.kaggle.com/vbookshelf/pneumothorax-chest-xray-images-and-masks) from [kaggle](https://www.kaggle.com).

This dataset contains 12,047 chest x-ray images and 12,047 pneumothorax masks. The images and masks are 1024x1024 and are in png format.

## Context[^1]

>A pneumothorax (noo-moe-THOR-aks) is a collapsed lung. A pneumothorax occurs when air leaks into the space between your lung and chest wall. This air pushes on the outside of your lung and makes it collapse. Pneumothorax can be a complete lung collapse or a collapse of only a portion of the lung.

>A pneumothorax can be caused by a blunt or penetrating chest injury, certain medical procedures, or damage from underlying lung disease. Or it may occur for no obvious reason. Symptoms usually include sudden chest pain and shortness of breath. On some occasions, a collapsed lung can be a life-threatening event.

>Treatment for a pneumothorax usually involves inserting a needle or chest tube between the ribs to remove the excess air. However, a small pneumothorax may heal on its own.


## Deep Neural Network training

Image segmentation is very common in the medical field. Is the process of taking an image and segmenting it into multiple regions of pixels. The goal is to simplify the representation of an image into something easier and meaningful to understand.

The architecture used is a Dynamic Unet, deployed on fastai with PyTorch in a [Google Colab](https://colab.research.google.com/) notebook. A quick guide to setup Google Colab with fastai and PyTorch can be found on [Colab & fastai](https://course.fast.ai/start_colab.html).

## Demoing the trained model

The trained model obtained from the previous step has beeing deployed using [Starlette](https://www.starlette.io/) on [Uvicorn](https://www.uvicorn.org/) a brief description can be found on [docs](https://blog.pattori.com/pneumo/), A demo of this model can be found [here](https://pneumot.herokuapp.com/) where you can input an image and get the segmentation (be patient the first time it will take a few seconds to load).


## Source Code

The source code for this project can be found on [GitHub](https://github.com/lpattori/pneumo)


## License

GNU General Public License v3.0. 3.0

Permissions of this strong copyleft license are conditioned on making available complete source code of licensed works and modifications, which include larger works using a licensed work, under the same license. Copyright and license notices must be preserved. Contributors provide an express grant of patent rights.


## Footnotes

[^1]: quote from [Mayo Clinic](https://www.mayoclinic.org/diseases-conditions/pneumothorax/symptoms-causes/syc-20350367).
