# Tensorflow.js tf.pool()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-pool-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-pool-function/)

**简介:** Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型以及深度学习神经网络。

**。池()功能**用于执行一个 N-D 池功能。

**语法:**

```
tf.pool(input, windowShape, poolingType, pad, dilations?, strides?)
```

**参数:**

*   **输入:**所述输入张量为等级 4 或等级 3，并且具有形状:【批次、高度、宽度、英寸英寸】。此外，在等级为 3 的情况下，则假定批量大小为 1。它可以是 tf 类型。张量 3D，tf。张量 4D、TypedArray 或数组。
*   **窗口形状:**规定的过滤器尺寸:【过滤器高度，过滤器宽度】。它可以是类型[数字，数字]或数字。在这种情况下， *filterSize* 是一个单数，那么 filterHeight == filterWidth。
*   **池类型:**池的指定类型，可以是“最大”或“平均”。
*   **填充:**所述的填充算法类型。它可以是有效类型、相同类型、数字类型或 conv 类型。
    1.  这里，对于相同和步长 1，输出将具有与输入相同的大小，而与滤波器大小无关。
    2.  对于“有效”，在滤波器尺寸大于 1*1×1 的情况下，输出应小于输入。
*   **扩张:**规定的扩张速率:【扩张高度，扩张宽度】在扩张池的高度和宽度维度上对输入值进行采样。默认值为[1，1]。此外，如果膨胀是一个单一的数字，那么膨胀高度==膨胀宽度。如果它大于 1，那么步幅的所有值都应该是 1。它是可选的，类型为[数字，数字]，数字。
*   **步幅:**池的规定步幅:【stridehAnD，strideWidth】。在这种情况下，跨步是一个单数，那么 strideHeight = = strideWidth。它是可选的，类型为[数字，数字]或数字。

**返回值:**返回 tf。张量 3D 或 tf .张量 4D。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining input tensor
const x = tf.tensor3d([1, 2, 3, 4], [2, 2, 1]);

// Calling pool() method
const result = tf.pool(x, 3, 'avg', 'same', [1, 2], 1);

// Printing output
result.print();
```

**输出:**

```
Tensor
    [[[0.4444444],
      [0.6666667]],

     [[0.4444444],
      [0.6666667]]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling pool() method
tf.tensor3d([1.2, 2.1, 3.0, -4], [2, 2, 1]).pool(3,
                    'conv_util.ExplicitPadding', 1, 1).print();
```

**输出:**

```
Tensor
    [[[3],
      [3]],

     [[3],
      [3]]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#pool