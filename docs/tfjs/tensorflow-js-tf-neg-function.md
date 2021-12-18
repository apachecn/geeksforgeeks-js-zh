# Tensorflow.js tf.neg()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-neg-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-neg-function/)

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。neg()函数**用于计算-1 * x，即输入张量，并按元素方式进行。

**语法:**

```
tf.neg(x)
```

**参数:**

*   **x:** 是张量输入，可以是 tf 类型。张量，或类型，或数组。

**返回值:**返回 tf。张量对象。

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor2d([6, 0, -9, -1], [4, 1]);

// Calling neg() method and
// printing output
y.neg().print();
```

**输出:**

```
Tensor
    [[-6],
     [0 ],
     [9 ],
     [1 ]]
```

**示例 2:** 在本例中，参数直接传递给 neg 函数。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor2d([
    1.4, 0.98, -9.9, -1.5, 2.0, 6.5], [2, 3]);

// Calling neg() method and
var res = tf.neg(y);

// printing output
res.print();
```

**输出:**

```
Tensor
    [[-1.4, -0.98, 9.8999996],
     [1.5 , -2   , -6.5     ]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#neg