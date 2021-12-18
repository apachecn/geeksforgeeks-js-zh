# tensorflow . js . TF . resform()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-resform-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-reshape-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**TF . rescale()**函数用于用指定的形状对给定的张量进行整形。

**语法:**

```
tf.reshape(x, shape)
```

**参数:**该功能有以下参数:

*   **x:** 需要整形的是输入张量。
*   **形状:**我们需要通过数字数组来定义输出形状。

**返回值:**返回一个 tf.Tensor

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

const x = tf.tensor1d([10, 15, 16, 24]);

// Print the tensor
x.reshape([2, 2]).print();
```

**输出:**

```
Tensor
    [[10, 15],
     [16, 24]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Using 2d
const x = tf.tensor2d(
  [1, 2, 3, 4, 5, 6, 7, 8, 9], [3, 3]
);
x.reshape([3, 3]).print();

// Using 3d
const y = tf.tensor3d(
  [[[1], [2]], [[3], [4]]]
);
y.reshape([2, 2]).print();

// Using 4d
const z = tf.tensor4d(
  [11, 12, 13, 14], [1, 2, 2, 1]
);
z.reshape([2, 2]).print();
```

**输出:**

```
Tensor
    [[1, 2, 3],
     [4, 5, 6],
     [7, 8, 9]]
Tensor
    [[1, 2],
     [3, 4]]
Tensor
    [[11, 12],
     [13, 14]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#reshape