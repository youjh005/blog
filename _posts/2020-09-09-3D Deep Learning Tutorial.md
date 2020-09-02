---
layout: post
title: "3D Deep Learning Tutorial"
date: 2020-09-03 00:00:00
description: This post deals w/ "3D Object Deep Learning Tutorial"
tags: 
 - 3D Object Deep Learning
---

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

[paper]: https://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Su_Multi-View_Convolutional_Neural_ICCV_2015_paper.pdf











