# Tensorflow.js tf.tan()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-tan-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-tan-function/)

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。tan()函数**用于找到所述张量输入的切线，并按元素方式进行。

**语法:**

```
tf.tan(x)
```

**参数:**该功能接受单个参数，如下图所示:

*   **x:** 是要计算 tan 值的张量输入元素。

**返回值:**返回 **tf。张量**对象。

**示例 1:** 在本例中，我们定义了一个整数类型的输入张量，然后打印它的 tan 值。为了创建输入张量，我们使用 **.tensor1d()** 方法，为了打印输出，我们使用**。print()** 方法。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([1, 4, 0, 11]);

// Calling tan() method and
// printing output
y.tan().print();
```

**输出:**

```
Tensor
   [1.5573809, 1.1578585, 0, -225.9478302]
```

**示例 2:** 在本例中，浮点类型值被视为张量输入，参数直接传递给 tan 函数。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining float values
var val = [1.5, .42, .5];

// Calling tensor1d method
const y = tf.tensor1d(val);

// Calling tan() method
var res = tf.tan(y)

// printing output
res.print();
```

**输出:**

```
Tensor
   [14.1011724, 0.4465817, 0.546293]
```