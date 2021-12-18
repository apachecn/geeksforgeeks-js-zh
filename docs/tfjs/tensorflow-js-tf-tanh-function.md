# Tensorflow.js tf.tanh()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-tanh-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-tanh-function/)

**Tensorflow.js** 是谷歌正在开发的开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。tanh()函数**用于找到所述张量输入的双曲正切，并且是按元素进行的。

**语法:**

```
tf.tanh(x)
```

**参数:**该功能接受单个参数，如下图:

*   **x:** 是要计算 tanh 值的张量输入，可以是 tf 类型。张量，或类型，或数组。

**返回值:**返回 tf。张量对象。

**示例 1:** 在这个示例中，我们定义了一个整数类型的输入张量，然后打印它的 tanh 值。为了创建输入张量，我们使用 **.tensor1d()** 方法，为了打印输出，我们使用**。print()** 方法。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([1, 15, 38, 0]);

// Calling tanh() method and
// printing output
y.tanh().print();
```

**输出:**

```
Tensor
   [0.7615941, 1, 1, 0]
```

**示例 2:** 在此示例中，浮点类型值被视为张量输入，参数直接传递给 tanh 函数。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining float values
var val = [0.5, 1.5, .66];

// Calling tensor1d method
const y = tf.tensor1d(val);

// Calling tanh() method
var res = tf.tanh(y)

// printing output
res.print();
```

**输出:**

```
Tensor
   [0.4621172, 0.9051483, 0.5783634]
```