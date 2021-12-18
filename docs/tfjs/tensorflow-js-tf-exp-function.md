# Tensorflow.js tf.exp()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-exp-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-exp-function/)

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。exp()函数**用于寻找所述张量输入的指数值，即(e^x)，并且是按元素方式进行的。

**语法:**

```
tf.exp(x)
```

**参数:**

*   **x:** 是要计算指数值的张量输入，可以是 tf 类型。张量，或类型，或数组。

**返回值:**返回 tf。张量对象。

**示例 1:** 在这个示例中，我们定义了一个整数类型的输入张量，然后打印它的指数值。为了创建输入张量，我们使用 **.tensor1d()** 方法，为了打印输出，我们使用**。print()** 方法。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([5, 1, 8, 0]);

// Calling exp() method and
// printing output
y.exp().print();
```

**输出:**

```
Tensor
    [148.4131622, 2.7182817, 2980.9580078, 1]
```

**示例 2:** 在本例中，浮点类型值被视为张量输入，参数直接传递给 *exp* 函数。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining float values
var val = [8.6, 0.5, .24];

// Calling tensor1d method
const y = tf.tensor1d(val);

// Calling exp() method
var res = tf.exp(y)

// printing output
res.print();
```

**输出:**

```
Tensor
    [5431.6616211, 1.6487212, 1.2712492]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#exp