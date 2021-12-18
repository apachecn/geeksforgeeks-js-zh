# Tensorflow.js tf.ceil()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-CEI-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-ceil-function/)

Tensorflow.js 是一个正在开发的开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。ceil()函数**用于找到所述张量输入的上限，并按元素方式完成。

**语法:**

```
tf.ceil(x)
```

**参数:**

*   **x:** 是要计算其天花板值的张量输入，可以是 *tf 类型。张量*，或*型达瑞*，或*阵列*。

**返回值:**返回 tf。张量对象。

**示例 1:** 在这个示例中，我们定义了一个整数类型的输入张量，然后打印它的天花板值。为了创建输入张量，我们使用 **.tensor1d()** 方法，为了打印输出，我们使用**。print()** 方法。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([9, 10, 19, 12]);

// Calling ceil() method and
// printing output
y.ceil().print();
```

**输出:**

```
Tensor
    [9, 10, 19, 12]
```

**示例 2:** 在本例中，浮点类型值被视为张量输入，参数直接传递给 *ceil* 函数。

## Javascript

```
// Importing the tensorflow.js library 
import * as tf from "@tensorflow/tfjs"

// Defining float values
var val = [.5, 4.9, .275];

// Calling tensor1d method
const y = tf.tensor1d(val);

// Calling ceil() method
var res = tf.ceil(y)

// Printing output
res.print();
```

**输出:**

```
Tensor
    [1, 5, 1]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#ceil