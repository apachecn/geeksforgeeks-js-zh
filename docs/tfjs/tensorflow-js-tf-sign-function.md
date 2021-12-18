# Tensorflow.js tf.sign()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-sign-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-sign-function/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。符号()功能**用于查找给定数字的所述符号的指示，并且是按元素进行的。

**语法:**

```
tf.sign(x)
```

**参数:**

*   **x:** 是陈述的张量输入，可以是 tf 类型。张量、类型或数组。

**返回值:**返回 tf。张量对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([1, 7.6, 0, NaN, -4, .91]);

// Calling sign() method and
// Printing output
y.sign().print();
```

**输出:**

```
Tensor
    [1, 1, 0, 0, -1, 1]
```

**例二:**

## Javascript

```
// Importing the tensorflow.js library 
import * as tf from "@tensorflow/tfjs"

// Defining tensor input
var val = [1.5, .4, .22, null, 'a'];

// Calling tensor1d method
const y = tf.tensor1d(val);

// Calling sign() method
var res = tf.sign(y)

// Printing output
res.print();
```

**输出:**

```
Tensor
    [1, 1, 1, 0, 0]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#sign