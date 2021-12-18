# Tensorflow.js tf.rsqrt()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-rsqrt-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-rsqrt-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.rsqrt()** 函数用于返回指定张量元素平方根的倒数。

**语法:**

```
tf.rsqrt (x)
```

**参数:**该函数接受如下所示的参数:

*   **x:** 指定的输入张量。

**返回值:**返回指定张量元素平方根的倒数。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a tensor of some elements
const x = tf.tensor1d([2, 3, 4, 5]);

// Calling the .rsqrt() function over
// the above tensor as its parameter
x.rsqrt().print();
```

**输出:**

```
Tensor
   [0.7071068, 0.5773503, 0.5, 0.4472136]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Using a tensor of some elements
// as the parameter for the .rsqrt() function
tf.tensor1d([0, 1, -2, 1.7, -2.5]).rsqrt().print();
```

**输出:**

```
Tensor
   [Infinity, 1, NaN, 0.766965, NaN]
```