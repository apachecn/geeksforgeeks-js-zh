# Tensorflow.js tf.sin()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-sin-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-sin-function/)

**Tensorflow.js** 是谷歌正在开发的开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。sin()函数**用来求所述张量输入的 sin，按元素方式进行。

**语法:**

```
tf.sin(x)
```

**参数:**

*   **x:** 是要计算 sin 值的张量输入，可以是 tf 类型。张量，或类型，或数组。

**返回值:**返回 tf。张量对象。

**示例 1:** 在这个示例中，我们定义了一个整数类型的输入张量，然后打印它的 sin 值。为了创建输入张量，我们使用 **.tensor1d()** 方法，为了打印输出，我们使用**。print()** 方法。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([5, 1, 8, 0]);

// Calling sin() method and
// printing output
y.sin().print();
```

**输出:**

```
Tensor
   [-0.9589252, 0.841471, 0.9893603, 0]
```

**示例 2:** 在此示例中，浮点类型值被视为张量输入，参数直接传递给 sin 函数。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining float values
var val = [8.6, 0.5, .24];

// Calling tensor1d method
const y = tf.tensor1d(val);

// Calling sin() method
var res = tf.sin(y)

// Printing output
res.print();
```

**输出:**

```
Tensor
   [0.7344244, 0.4794255, 0.2377044]
```