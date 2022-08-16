<p align="center">
<img src="./img/tools.svg" alt="logo" width="20%">
</p>
<h1 align="center">Toolkit</h1>

<p align="center">
该工具包提供了一系列高性能图像处理功能 如模糊、混合和调整大小。已弃用的RenderScript Intrinsics函数的完美替代品。
</p>

## 使用方法
- [Gradle引入](#Gradle引入)

## 包含功能
- [混合模式](## 混合模式)
- [高斯模糊](##高斯模糊)
- [颜色矩阵滤镜](#颜色矩阵滤镜)
- [盲卷积](#盲卷积)
- [直方图和直方图点](#直方图和直方图点)
- [LUT和LUT3D](#LUT和LUT3D)
- [调整大小](#调整大小)
- [YUV to RGB](#YUV to RGB)

该工具包提供了一个C++和一个Java/Kotlin接口。它被打包为Android 可以添加到项目中的库。
这些函数在CPU上执行多线程。他们利用霓虹灯/AdvSimd ，在Arm处理器和英特尔的SSE上。
与RenderScript Intrinsics相比，该工具包使用更简单，当在CPU上执行时，速度是前者的两倍。但是，
RenderScript内部函数允许更大的灵活性 支持的分配类型。该工具包不支持浮动分配；
大多数函数支持字节数组和位图。

您应该实例化工具箱一次，并在整个应用程序中重用它。
在实例化时，工具箱创建一个线程池，用于处理所有函数。
您可以通过构造函数限制工具箱使用的池线程数。池线程中在完成任何未决工作后，一旦工具包被销毁，就会被销毁。

此库是线程安全的。您可以从不同的池线程调用方法。这些功能将： 按顺序执行。

## Gradle引入

```groovy
   
```

## 混合模式

## 高斯模糊

## 颜色矩阵滤镜

## 盲卷积

## 直方图和直方图点

## 直方图和直方图点

## LUT 和 LUT 3D

## 调整大小

## YUV to RGB