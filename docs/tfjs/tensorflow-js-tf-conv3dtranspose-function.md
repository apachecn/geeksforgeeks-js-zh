# tensorlow . js TF . conv 3 dttransverse()函数

> 哎哎哎:# t0]https://www . geeksforgeeks . org/tensorlow-js-TF-conv 3 dttransverse-function/

**简介:** Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型以及深度学习神经网络。

**. ConV3 转置()功能**用于确定体积的转置 3D 卷积。这也称为反卷积。

**语法:**

```
tf.conv3dTranspose(x, filter, outputShape, strides, pad)
```

**参数:**

*   **x:** 所述输入图像，其或者是等级 5 或者是等级 4，并且具有形状:【批次、深度、高度、宽度、深度】。此外，在等级为 4 的情况下，则假定批量大小为 1。它可以是 tf 类型。张量 4D，tf。张量 5D、TypedArray 或数组。
*   **滤波器:**所述的秩为 4 的滤波器张量和形状:【深度、滤波器高度、滤波器宽度、外部深度、内部深度】。其中，inDepth 必须与输入张量中的 inDepth 匹配。它可以是 tf 类型。张量 5D、TypedArray 或数组。
*   **输出形状:**所述的输出形状为等级 5 或等级 4，形状为【批次、深度、高度、宽度、超出深度】。在这种情况下，等级为 3，则假定批次为 1。它可以是[数字，数字，数字，数字，数字]或[数字，数字，数字，数字]类型。
*   **步幅:**形状的原始卷积的规定步幅:【条纹深度，条纹宽度，条纹宽度】。它可以是类型[数字、数字、数字]或数字。
*   **填充:**在运算的非转置形式中有用的填充算法的指定类型。它可以是有效类型，也可以是相同类型。

**返回值:**返回 tf。张量 4D 或 tf .张量 5D

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining input tensor
const x = tf.tensor5d([1, 2, 2, 3], [2, 2, 1, 1, 1]);

// Defining filter tensor
const y = tf.tensor5d([3, 3, 3, 2], [1, 2, 2, 1, 1]);

// Calling conv3dTranspose() method
const result = tf.conv3dTranspose(x, y, [1, 1, 2, 1, 1], 2, 'same');

// Printing output
result.print();
```

**输出:**

```
Tensor
    [[[ [[3],],

        [[3],]]]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling conv3dTranspose() method
tf.conv3dTranspose(tf.tensor5d(
    [1.1, 2.1, 2.2, 3.6], [2, 2, 1, 1, 1]), 
    tf.tensor5d([3.6, 3.1, 3.2, 2.0], [1, 2, 2, 1, 1]), 
    [1, 1, 2, 1, 1], 7, 'valid').print();
```

**输出:**

```
Tensor
    [[[ [[0],],

        [[0],]]]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#conv3dTranspose