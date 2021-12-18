# Tensorflow.js tf .倒数()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-倒数-函数/](https://www.geeksforgeeks.org/tensorflow-js-tf-reciprocal-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf .倒数()**函数用于返回指定张量元素的倒数。

**语法:**

```
tf.reciprocal(x)
```

**参数:**该函数接受如下所示的参数:

*   **x:** 指定的输入张量。

**返回值:**返回指定张量元素的倒数。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a tensor of some elements
const x = tf.tensor1d([2, 3, 4, 5]);

// Calling the .reciprocal() function over
// the above tensor as its parameter
x.reciprocal().print();
```

**输出:**

```
Tensor
   [0.5, 0.3333333, 0.25, 0.2]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Using a tensor of some elements
// as the parameter for the .reciprocal() function
tf.tensor1d([0, 1, -2, 1.7, -2.5]).reciprocal().print();
```

**输出:**

```
Tensor
   [Infinity, 1, -0.5, 0.5882353, -0.4]
```