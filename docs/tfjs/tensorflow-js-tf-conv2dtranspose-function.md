# tensorlow . js TF . conv 2 dttransverse()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-conv 2 dttransverse-function/

**简介:** Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型以及深度学习神经网络。

**. conv2 转置()函数**用于确定图像的转置 2D 卷积。这也被认为是一种反卷积。

**语法:**

```
tf.conv2dTranspose(x, filter, outputShape, strides, pad, dimRoundingMode?)
```

**参数:**

*   **x:** 所述输入图像，其或者是等级 3 或者是等级 4，并且具有形状:【批次、高度、宽度、深度】。此外，在等级为 3 的情况下，则假定批量大小为 1。它可以是 tf 类型。张量 3D，tf。张量 4D、TypedArray 或数组。
*   **滤波器:**所述的秩为 4 的滤波器张量和形状:【滤波器高度、滤波器宽度、滤波器外深度、滤波器内深度】。其中，*深度*必须匹配输入张量中的*深度*。它可以是 tf 类型。张量 4D、TypedArray 或数组。
*   **输出形状:**所述的等级为 4 或等级为 3 的输出形状和形状【批次、高度、宽度、超出深度】。在这种情况下，等级为 3，则假定批次为 1。它可以是[数字，数字，数字，数字]或[数字，数字，数字]类型。
*   **步幅:**形状的原始卷积的规定步幅:【strideh8，strideWidth】。它可以是类型[数字，数字]或数字。
*   **填充:**在运算的非转置形式中有用的填充算法的指定类型。它可以是有效类型、相同类型、数字类型或显式填充类型。
*   **圆形模式:**从“天花板”、“圆形”或“地板”中选择的一个指定字符串。在这种情况下，如果没有提供值，则缺省值将被截断。它是可选的，类型有天花板、圆形或地板。

**返回值:**返回 tf。张量 3D 或 tf .张量 4D。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining input tensor
const x = tf.tensor3d([1, 2, 2, 3], [2, 2, 1]);

// Defining filter tensor
const y = tf.tensor4d([3, 3, 3, 2], [1, 2, 2, 1]);

// Calling conv2dTranspose() method
const result = tf.conv2dTranspose(x, y, [1, 1, 2], 2, 'same');

// Printing output
result.print();
```

**输出:**

```
Tensor
     [ [[3, 3],]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling conv2dTranspose() method with 
// all its parameters
tf.tensor3d([1.1, 2.2, 3.3, 4.4], [2, 2, 1]).conv2dTranspose(
 tf.tensor4d([1.3, 1.2, null, -4], [1, 2, 2, 1]),
            [1, 1,  2], 1, 1, 'ceil').print();
```

**输出:**

```
Tensor
     [ [[5.7199998, -7.9199996],]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#conv2dTranspose