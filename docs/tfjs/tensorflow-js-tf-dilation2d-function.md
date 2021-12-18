# tensorflow . js TF . explot 2d()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-explot 2d-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-dilation2d-function/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**膨胀 2d()函数**用于评估所述输入张量的灰度膨胀。

**语法:**

```
tf.dilation2d(x, filter, strides, pad, dilations?, dataFormat?)
```

**参数:**

*   **x:** 所述的输入张量，其或者是等级 3 或者是等级 4，并且具有形状:【批次、高度、宽度、英寸通道】。此外，在等级为 3 的情况下，则假定批量大小为 1。它可以是 tf 类型。张量 3D，tf。张量 4D、TypedArray 或数组。
*   **滤波器:**所述的秩 3 的滤波器张量和形状:【滤波器高度、滤波器宽度、深度】。它可以是 tf 类型。张量 3D、类型数据或数组。
*   **步幅:**给定形状输入张量的每个尺寸的滑动窗口的规定步幅:【strideh8，strideWidth】。在这种情况下，规定的步幅是一个单一的数字，那么 strideHeight = = strideWidth。它可以是类型[数字，数字]或数字。
*   **填充:**所述的填充算法类型。它可以是有效类型或相同类型。
    1.  这里，对于相同和步长 1，输出将具有与输入相同的大小，而与滤波器大小无关。
    2.  对于“有效”，在滤波器尺寸大于 1*1×1 的情况下，输出应小于输入。
*   **扩张:**规定的扩张速率:【扩张高度，扩张宽度】输入值在高度和宽度维度上进行采样，以利于萎缩形态扩张。默认值为[1，1]。此外，如果膨胀是一个单一的数字，那么膨胀高度==膨胀宽度。如果它大于 1，那么步幅的所有值都应该是 1。它是可选的，类型为[数字，数字]，数字。
*   **数据格式:**指定所述输入和输出数据的数据格式。默认值为“NHWC”。而且，这里的数据是按照【批次、高度、宽度、通道】的顺序存储的。它是可选的，类型为“NHWC”。

**返回值:**返回 tf。张量 3D 或 tf .张量 4D。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining input tensor
const x = tf.tensor3d([1, 2, 3, 4], [2, 2, 1]);

// Defining filter tensor
const y = tf.tensor3d([1, 1, 0, 4], [1, 1, 4]);

// Calling dilation2d() method
const result = tf.dilation2d(x, y, 2, 'valid');

// Printing output
result.print();
```

**输出:**

```
Tensor
     [ [[2],]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling dilation2d() method with 
// all its parameters
tf.tensor3d([1.1, 2.2, 3.3, 4.4], [2, 2, 1]).dilation2d(
 tf.tensor3d([1.3, 1.2, null, -4], [1, 1, 4]),
             2, 'valid', [3, 2], 'NHWC').print();
```

**输出:**

```
Tensor
     [ [[2.4000001],]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#dilation2d