---
title: 3D人脸预处理
date: 2017-12-22 08:39:38
tags:
  - 人脸数据库
  - 人脸识别
categories:
  - 这个课题不好搞
---
{% asset_img 1.jpg 预处理过程 %}
<!-- more -->

# 简介
3D人脸预处理是整个算法实现的必不可少的一步，用深度摄像头获取的信息，大部分是点云，多少会有点瑕疵，更何况我们只需要面部区域，所以要对获取的三维点云进行预处理。
实验所用的3D人脸最初是这样的：
{% asset_img original.jpg 原始图像 %}
预处理主要分为三个步骤：
<li> Filling Hole
<li> Face Cropping
<li> Smoothing & Pose Correction

效果如下图所示：
{% asset_img steps.jpg 预处理步骤 %}
