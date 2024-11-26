---
title: 使用 Aspose.PSD 在C#中处理蒙板
weight: 100
type: docs
description: 关于如何在PSD文件中处理剪贴蒙板、光栅蒙板和矢量蒙板的示例
keywords: [蒙板, 图层蒙板, 矢量蒙板, 剪贴蒙板, psd, psd api, C#, csharp, 代码示例]
url: zh/net/update-create-layer-mask/
---

## 概述

PSD 文件中有三种类型的蒙板：
1. 剪贴蒙板
2. 光栅蒙板
3. 矢量蒙板

本文涵盖了这三种类型的蒙板。

### 剪贴蒙板

剪贴蒙板是图形设计和图像编辑软件中强大的功能，可以基于另一图层的形状和内容控制某一图层的可见性。实质上，剪贴蒙板将一个图层的可见性限制在另一个位于其下方的图层定义的形状内。

要创建剪贴蒙板，您需要两个图层：基本图层和剪贴图层。基本图层定义了将可见的形状或区域，而剪贴图层包含将被限制在基本图层形状内的内容。

应用剪贴蒙板时，剪贴图层的内容仅在基本图层边界内可见。基本图层边界外的任何内容将被隐藏或裁剪。

剪贴蒙板特别适用于将效果（如纹理或图案）应用于图像或艺术作品的特定区域。通过使用剪贴蒙板，您可以确保效果被限制在所需区域内，而不会影响图像的其余部分。

### 光栅蒙板

PSD 文件中的光栅蒙板对于控制图层内特定区域的可见性至关重要。与使用数学形状定义蒙板区域的矢量蒙板不同，光栅蒙板使用基于像素的信息来确定图层的哪些部分可见或隐藏。

光栅蒙板由应用于图层的灰度图像组成。蒙板的白色区域表示可见部分，黑色区域表示隐藏部分。灰度之间的阴影创建了部分透明或半可见区域。

使用光栅蒙板，您可以实现复杂的蒙板效果，从而根据像素级细节精确控制图层的可见性。此功能特别适用于需要在图像内进行详细编辑和混合的任务。

### 矢量蒙板

PSD 文件中的矢量蒙板是一种用于基于数学形状定义图层特定区域可见性的多功能工具。与使用像素信息的光栅蒙板不同，矢量蒙板利用路径和曲线来创建平滑且可缩放的蒙板区域。

矢量蒙板本质上是应用于图层的路径。路径的形状决定了图层的哪些部分可见，哪些部分隐藏。通过操纵路径的控制点和曲线，您可以创建精确而复杂的蒙板区域。

矢量蒙板特别适用于创建干净、可缩放的蒙板，而且可以轻松调整而无损失质量。此功能非常适合需要在图层内定义可见区域的高精度和灵活性任务。

有关添加矢量蒙板的更多信息，请访问[矢量蒙板页面](zh/psd/net/layer-vector-mask/)。

## 示例
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "WorkingWithMasks-WorkingWithMasks.cs" >}}

有关更详细的信息和示例，请访问[Aspose.PSD for C#文档](https://docs.aspose.com/psd/net/)。