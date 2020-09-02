---
layout: post
title: "3D Deep Learning Tutorial"
date: 2020-09-03 00:00:00
description: This post deals w/ "3D Object Deep Learning Tutorial"
tags: 
 - 3D Object Deep Learning
---

This post is summary of video from [3D Deep Learning Tutorial](https://www.youtube.com/watch?v=vfL6uJYFrp4).



# Broad Applications of 3D Data

- Robotics
- Augmented reality
- Autonomous driving
- Medical image processing





# Topics

1. 3D Data
2. Classification
3. Segmentation & Detection
4. Reconstruction





# 3D Data

## The Representation Challenge of 3D Deep Learning

- 오디오나 이미지와 같은 **rasterized form(regular grids)** 을 가진 데이터와 달리, 3D 데이터는 **geometric form (irregular)** 의 형태를 지니고 있음.
- 3D Data는 아래와 같은 형태로 나타낼 수 있음.
  - Point Cloud
  - Mesh (Graph CNN)
  - Volumetric (voxelize)
  - Multi-View



## Datasets

- Datasets for 3D Objects
  - Large-scale Synthetic Objects: ShapeNet
- Datasets for 3D Object Parts
  - Fine-grained Part: PartNet (ShapeNetPart2019)
- Datasets for Indoor 3D Scenes
  - Large-scale Synthetic Scenses: SceneNet
  - Large-scale Scanned Real Scenes: ScanNet
- Datasets for Outdoor 3D Scenes
  - KITTI: LiDAR data, labeled by 3D b.boxes
  - Semantic KITTI: LiDAR data, labeled per point
  - Waymo Open Dataset: LiDAR data, labeled by 3D b.boxes





# Classification

Covered methods:

Volumetric CNN, OctNet, O-CNN, SparseConvNet, PointNet, PointNet++, RS CNN, DGCNN, Point ConvNet, KPConv, Monte Carlo Point Convolution, PConv, Multi-View CNN, Spectral CNN, Synchronized Spectral CNN, Spherical CNN



## Multi-View CNN

You can see paper in here ([paper](https://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Su_Multi-View_Convolutional_Neural_ICCV_2015_paper.pdf))

1. 주어진 3D 입력 이미지에 대해서,
2. 가상의 multi-view camera로 rendring을 시킨 다음,
3. 각각의 rendering된 이미지가 특징점 추출을 위해 각각의 CNN_1을 거치게 된다.
4. 추출된 특징점들은 view pooling을 통해 합쳐지고,
5. 최종적으로 추출된 특징점이 CNN_2를 거친 후 클래스 분류를 수행하게 된다.



- Indeed gives good performance
- Can leverage vast literature of image classification
- Can use pertained features
- Need projection
- What if the input is noisy and/or incomplete?  (e.g., point cloud)



## Volumetric CNN











