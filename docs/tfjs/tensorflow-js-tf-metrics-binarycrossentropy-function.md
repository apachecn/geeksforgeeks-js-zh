# tensorflow . js TF . metrics .binarycross 熵()函数

> 原文:[https://www . geeksforgeeks . org/tensorflow-js-TF-metrics-binarycross 熵-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-metrics-binarycrossentropy-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**. metrics .Binarycross 熵()函数**是使用二进制张量并返回 tf 的二进制交叉熵度量函数。张量对象。

**语法:**

```
tf.metrics.binaryCrossentropy (yTrue, yPred)
```

**参数:**

*   **yTrue:** 是陈述的真值的二元张量输入，可以是 tf.Tensor 类型
*   **yPred:** 是所述预测的二元张量输入，可以是 tf.Tensor 类型

**返回值:**返回 tf。张量对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining binary tensors
const y = tf.tensor2d([[4], [5], [6], [7]]);
const z = tf.tensor2d([[1], [2], [0], [1.8]]);

// Calling metrics.binaryCrossentropy() 
// method
const binry_crsntropy = 
    tf.metrics.binaryCrossentropy(y, z);

// Printing output
binry_crsntropy.print();
```

**输出:**

```
Tensor
    [-27.6301231, -36.8401985, 55.2615433, -55.2603455] 
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling metrics.binaryCrossentropy() 
// method and printing output
tf.metrics.binaryCrossentropy(
    tf.tensor2d([[-13], [-2.787]]), 
    ([[-0.6], [-12]])).print();
```

**输出:**

```
Tensor
    [-119.7330246, -25.6688404]
```

**参考:**T2