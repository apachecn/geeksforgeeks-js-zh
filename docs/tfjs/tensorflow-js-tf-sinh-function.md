# Tensorflow.js tf.sinh()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-sinh-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-sinh-function/)

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。sinh()函数**用于找到所述张量输入的双曲 sin，并按元素进行。

**语法:**

```
tf.sinh(x)
```

**参数:**该函数接受如下所示的参数:

*   **x:** 是要计算 sinh 值的张量输入，可以是 tf 类型。张量，或类型，或数组。

**返回值:**返回 tf。张量对象。

**示例 1:** 在这个示例中，我们定义了一个整数类型的输入张量，然后打印它的 sinh 值。为了创建输入张量，我们使用 **.tensor1d()** 方法，为了打印输出，我们使用**。print()** 方法。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([23, 15, 38, 10]);

// Calling sinh() method and
// printing output
y.sinh().print();
```

**输出:**

```
Tensor
   [4872394752, 1634507.75, 15927956010434560, 11013.2333984]
```

**示例 2:** 在此示例中，浮点类型值被视为张量输入，参数直接传递给 sinh 函数。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining float values
var val = [1.61, 12.5, 55.34];

// Calling tensor1d method
const y = tf.tensor1d(val);

// Calling sinh() method
var res = tf.sinh(y)

// printing output
res.print();
```

**输出:**

```
Tensor
   [2.4014621, 134168.609375, 5.405391049267939e+23]
```