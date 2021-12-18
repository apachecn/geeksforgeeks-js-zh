# Tensorflow.js tf.pow()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-power-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-pow-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.pow()** 函数用于计算一个指定张量对另一个指定张量的幂。它支持广播。

**语法:**

```
tf.power(base, exp).
```

**参数:**该函数接受两个参数，如下图所示:

*   **基础:**给定张量的指定基础分量元素。
*   **exp:** 给定张量的指定指数分量元素。

**返回值:**返回幂运算计算结果的张量。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing Tensor "a" as base and
// "b" as exponent values
const a = tf.tensor([2])
const b = tf.tensor([3])

// Calling the pow() function over
// the above tensor as its parameters
a.pow(b).print();
```

**输出:**

```
Tensor
   [8]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing Tensor "a" as base and
// "b" as exponent values
const a = tf.tensor([[1, 2], [3, 4]])
const b = tf.tensor([2])

// Calling the pow() function over
// the above tensor as its parameters
a.pow(b).print();
```

**输出:**

```
Tensor
   [[1, 4 ],
    [9, 16]]
```