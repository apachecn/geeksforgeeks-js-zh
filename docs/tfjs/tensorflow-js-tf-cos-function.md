# Tensorflow.js tf.cos()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-cos-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-cos-function/)

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。cos()函数**用于找到所述张量输入的*余弦*值，并且是按元素进行的。

**语法:**

```
tf.cos(x)
```

**参数:**

*   **x:** 是张量输入元素，其 *cos* 值将被计算。

**返回值:**返回 tf。张量对象。

**示例 1:** 在本例中，我们定义了一个整数类型的输入张量，然后打印其 *cos* 值。为了创建输入张量，我们使用 **.tensor1d()** 方法，为了打印输出，我们使用**。print()** 方法。

## Javascript

```
// Importing the tensorflow.js library 
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([1, 4, 0, 11]);

// Calling cos() method and
// printing output
y.cos().print();
```

**输出:**

```
Tensor
    [0.5403116, -0.6536576, 1, 0.0044258]
```

**示例 2:** 在本例中，浮点类型值被视为张量输入，参数直接传递给 *cos* 函数。

## Javascript

```
// Importing the tensorflow.js library 
import * as tf from "@tensorflow/tfjs"

// Defining float values
var val = [1.5, .42, .5];

// Calling tensor1d method
const y = tf.tensor1d(val);

// Calling cos() method
var res = tf.cos(y)

// Printing output
res.print();
```

**输出:**

```
Tensor
    [0.0707384, 0.9131125, 0.8775977]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#cos