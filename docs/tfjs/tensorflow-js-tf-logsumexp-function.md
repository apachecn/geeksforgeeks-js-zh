# Tensorflow.js tf.logSumExp（） 函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-logsumexp-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-logsumexp-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.logSumExp()** 函数用于计算张量元素在其维度上的对数和 Exp。它沿着轴的维度减少给定的输入元素。如果参数“keepDims”为真，则缩减的维度将保留长度 1，否则张量的秩将缩减 1。如果轴参数没有条目，它将返回一个包含所有降维元素的张量。

**语法:**

```
tf.logSumExp (x, axis, keepDims)
```

**参数:**该函数接受三个参数，如下图所示:

*   **x:** 输入张量。
*   **轴:**要减少的指定尺寸。默认情况下，它会缩小所有尺寸。它是可选参数。
*   **保留尺寸:**如果该参数值为真，它将保留长度为 1 的缩减尺寸，否则张量的秩将缩减 1。它也是可选参数。

**返回值:**返回对数和 exp 运算的计算值张量。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a some tensors 
const a = tf.tensor1d([0, 1]);
const b = tf.tensor1d([3, 5]);
const c = tf.tensor1d([2, 4, 7]);

// Calling the .logSumExp() function over 
// the above tensors
a.logSumExp().print();
b.logSumExp().print();
c.logSumExp().print();
```

**输出:**

```
Tensor
   1.31326162815094
Tensor
   5.126927852630615
Tensor
   7.054985046386719
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

// Calling the .logSumExp() function over 
// the above tensors
a.logSumExp(axis1).print();
b.logSumExp(axis2, true).print();
c.logSumExp(axis1, false).print();
b.logSumExp(axis3, false).print();
```

**输出:**

```
Tensor
   1.31326162815094
Tensor
    [[3.3132617, 8.0485878],]
Tensor
   7.054985046386719
Tensor
   [3.3132617, 8.0485878]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#logSumExp