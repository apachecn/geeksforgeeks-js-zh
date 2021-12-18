# Tensorflow.js tf.min()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-min-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-min-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.min()** 函数用于计算指定张量在其维度上的最小值。它沿着轴的维度减少给定的输入元素。如果参数“keepDims”为真，则缩减的维度将保留长度 1，否则张量的秩将缩减 1。如果轴参数没有条目，它将返回一个包含所有降维元素的张量。

**语法:**

```
tf.min (x, axis?, keepDims?)
```

**参数:**该函数接受三个参数，如下图所示:

*   **x:** 正在计算最小值的输入张量。
*   **轴:**要减少的指定尺寸。默认情况下，它会缩小所有尺寸。它是可选参数。
*   **保留尺寸:**如果该参数值为真，它将保留长度为 1 的缩减尺寸，否则张量的秩将缩减 1。它也是可选参数。

**返回值:**返回最小值张量。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a some tensors 
const a = tf.tensor1d([0, 1]);
const b = tf.tensor1d([3, 5]);
const c = tf.tensor1d([2, 4, 7]);

// Calling the .min() function over 
// the above tensors
a.min().print();
b.min().print();
c.min().print();
```

**输出:**

```
Tensor
   0
Tensor
   3
Tensor
   2
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a some tensors 
const a = tf.tensor1d([0, 1]);
const b = tf.tensor2d([3, 5, 2, 8], [2, 2]);
const c = tf.tensor1d([2, 4, 7]);

// Initializing a axis parameters
const axis1 = -1;
const axis2 = -2;
const axis3 = 0;

// Calling the .min() function over 
// the above tensors
a.min(axis1).print();
b.min(axis2, true).print();
c.min(axis1, false).print();
b.min(axis3, false).print();
```

**输出:**

```
Tensor
   0
Tensor
    [[2, 5],]
Tensor
   2
Tensor
   [2, 5]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#min