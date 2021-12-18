# Tensorflow.js tf.sigmoid()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-sigmoid-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-sigmoid-function/)

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。sigmoid()函数**用于找到所述张量输入(即 1 / (1 + exp(-x))的 sigmoid，并按元素进行。

**语法:**

```
tf.sigmoid(x)
```

**参数:**该功能接受单个参数，如下图所示:

*   **x:** 是张量输入，可以是 tf 类型。张量，或类型，或数组。

**返回值:**返回 tf。张量对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([-1, 15, 0, Math.E-1]);

// Calling sigmoid() method and
// printing output
y.sigmoid().print();
```

**输出:**

```
Tensor
    [0.2689414, 0.9999996, 0.5, 0.8479074]
```

**示例 2:** 在本例中，参数直接传递给 sigmoid 函数。

## Javascript

```
// Importing the tensorflow.js library 
import * as tf from "@tensorflow/tfjs"

// Defining float values
var val = [0.5, -1.5, .66];

// Calling tensor1d method
const y = tf.tensor1d(val);

// Calling sigmoid() method
var res = tf.sigmoid(y)

// Printing output
res.print();
```

**输出:**

```
Tensor
    [0.6224594, 0.1824255, 0.6592603]
```