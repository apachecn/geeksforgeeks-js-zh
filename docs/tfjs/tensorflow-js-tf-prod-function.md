# Tensorflow.js tf.prod()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-prod-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-prod-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.prod()** 函数用于计算指定张量元素在其维度上的乘积。它沿着轴的维度减少给定的输入元素。如果参数“keepDims”为真，则缩减的维度将保留长度 1，否则张量的秩将缩减 1。如果轴参数没有条目，它将返回一个包含所有降维元素的张量。

**语法:**

```
tf.pord (x, axis?, keepDims?)
```

**参数:**该函数接受三个参数，如下图所示:

*   **x:** 正在计算生产操作的输入张量。如果数据类型是布尔值，它将被转换为 int32，返回的输出也将是 int32。
*   **轴:**要减少的指定尺寸。默认情况下，它会缩小所有尺寸。它是可选参数。
*   **保留尺寸:**如果该参数值为真，它将保留长度为 1 的缩减尺寸，否则张量的秩将缩减 1。它也是可选参数。

**返回值:**返回乘积运算结果的张量。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a some tensors 
const a = tf.tensor1d([0, 1]);
const b = tf.tensor1d([3, 5]);
const c = tf.tensor1d([2, 4, 7]);

// Calling the .prod() function over 
// the above tensors
a.prod().print();
b.prod().print();
c.prod().print();
```

**输出:**

```
Tensor
   0
Tensor
   15
Tensor
   56
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

// Calling the .prod() function over 
// the above tensors
a.prod(axis1).print();
b.prod(axis2, true).print();
c.prod(axis1, false).print();
b.prod(axis3, false).print();
```

**输出:**

```
Tensor
   0
Tensor
    [[6, 40],]
Tensor
   56
Tensor
   [6, 40]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#prod