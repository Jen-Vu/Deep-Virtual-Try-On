# Worlds first API for Deep Virtual Try On and android implementation
[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/)
[![license](https://img.shields.io/github/license/DAVFoundation/captain-n3m0.svg?style=flat-square)](https://github.com/kishorkuttan/Deep-Virtual-Try-On/blob/master/LICENSE)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1rlk-nOgIJa14UDNQLJyRxh3McoRLo3b0?usp=sharing)
# Demo
Google colab link:
https://colab.research.google.com/drive/1rlk-nOgIJa14UDNQLJyRxh3McoRLo3b0?usp=sharing

## API
![alt text](https://github.com/kishorkuttan/Deep-Virtual-Try-On/blob/master/flask_demo.gif)

## Android Application
![alt text](https://github.com/kishorkuttan/Deep-Virtual-Try-On/blob/master/dvtron_android.gif)
## Results
![alt text](https://github.com/kishorkuttan/Deep-Virtual-Try-On/blob/master/demo_1.jpeg)
![alt text](https://github.com/kishorkuttan/Deep-Virtual-Try-On/blob/master/demo_2.jpeg)
![alt text](https://github.com/kishorkuttan/Deep-Virtual-Try-On/blob/master/demo_3.jpeg)
![alt text](https://github.com/kishorkuttan/Deep-Virtual-Try-On/blob/master/demo_4.jpg)
![alt text](https://github.com/kishorkuttan/Deep-Virtual-Try-On/blob/master/demo_5.jpeg)
# Training
## Download the dataset
### Download the MPV dataset from Image-based Multi-pose Virtual Try On and put the dataset under "./dataset/images/".
### Select postive perspective images, create dataset split file 'data_pair.txt', and put it under "./dataset/".
## Dataset preprocessing
### Pose keypoints. Use the Openpose, and put the keypoints file in "./dataset/pose_coco".
### Semantic parsing. Use the CIHP_PGN, and put the parsing results in "./dataset/parse_cihp".
### Cloth mask. Use the removebg api or holistically-nested-edge-detection for the cloth mask, and put the mask in "./dataset/cloth_mask".
## Coarse-to-fine training
### Download the VGG19 pretrained checkpoint
### cd vgg_model/
### wget https://download.pytorch.org/models/vgg19-dcbb9e9d.pth
### Set different configuration based on the "config.py". Then run
``` sh train.sh ```
# Reference
* https://github.com/JDAI-CV/Down-to-the-Last-Detail-Virtual-Try-on-with-Detail-Carving
* https://github.com/CMU-Perceptual-Computing-Lab/openpose
* https://www.pyimagesearch.com/2019/03/04/holistically-nested-edge-detection-with-opencv-and-deep-learning/
* https://www.remove.bg/
