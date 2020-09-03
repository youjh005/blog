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

Can we use CNNs w/o 2D-3D projection?
→ Straight-forward idea: **3D native convolution**



1. **Voxelization**: Represent the occupancy of regular 3D grids
2. 3D CNN on Volumetric Data
   - 3D convolutions uses 4D kernels
3. How can resolve **Complexity Issue**?

 

Idea1: Learn to project ([paper](https://openaccess.thecvf.com/content_cvpr_2016/papers/Qi_Volumetric_and_Multi-View_CVPR_2016_paper.pdf), Volumetric and Multi-View CNN)

Idea2: Store only the occupoied grids ([paper](https://dl.acm.org/doi/abs/10.1145/3072959.3073608), O-CNN)

- store the sparse surface signals
- constrain the computation near the surface



Octree의 아이디어에 영감을 받음

※ Octreee: Recursively partition the space

Each internal node has exactly eight childeren neighborhood searching: Hash table



- SparseConvNet
  - [Code](https://github.com/facebookresearch/SparseConvNet) & [Paper](https://arxiv.org/abs/1706.01307)(Submanifold Sparse Convolutional Networks)
  - Uses ResNet architecture
  - State-of-the-art for 3D analysis
  - Takses time to train



## Point Networks























