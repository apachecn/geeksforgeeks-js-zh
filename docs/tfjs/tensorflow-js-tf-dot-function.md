# Tensorflow.js tf.dot()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-dot-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-dot-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.dot()** 函数用于计算两个给定矩阵或向量 T1 和 t2 的点积。

**语法:**

```
tf.dot(t1, t2);
```

**参数:**该函数接受如下所示的参数:

*   **t1:** 是点运算的第一张张量。
*   **t2:** 是点运算的第二张量。

**返回值:**返回两个给定矩阵或向量 T1 和 t2 的点积。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

let geek1 = tf.tensor1d([2, 3]);
let geek2 = tf.tensor2d([[2, 3], [4, 5]]);
let geek3 = tf.tensor2d([[2, 3, 4], [5, 6, 7]]);

let a =geek1.dot(geek2);
let b =geek2.dot(geek1);
let c =geek2.dot(geek3);

a.print();
b.print();
c.print();
```

**输出:**

```
Tensor
    [16, 21]
Tensor
    [13, 23]
Tensor
    [[19, 24, 29],
     [33, 42, 51]]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

let geek1 = tf.tensor1d([3, 4]);
let geek2 = tf.tensor2d([[3, 4], [5, 6]]);

tf.dot(geek1, geek2).print();
```

**输出:**

```
Tensor
    [29, 36]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#dot