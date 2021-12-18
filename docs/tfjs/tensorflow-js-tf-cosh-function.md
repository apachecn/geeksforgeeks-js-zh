# Tensorflow.js tf.cosh()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-cosh-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-cosh-function/)

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。cosh()函数**用于找到所述张量输入的双曲线 *cos* ，并且是按元素方式完成的。

**语法:**

```
tf.cosh(x)
```

**参数:**

*   **x:** 是要计算其 *cosh* 值的张量输入，可以是 *tf 类型。张量*，或*型达瑞*，或*阵列*。

**返回值:**返回 tf。张量对象。

**示例 1:** 在本例中，我们定义了一个整数类型的输入张量，然后打印它的 *cosh* 值。为了创建输入张量，我们使用 **.tensor1d()** 方法，为了打印输出，我们使用**。print()** 方法。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([1, 7, 0, 3]);

// Calling cosh() method and
// printing output
y.cosh().print();
```

**输出:**

```
Tensor
    [1.5430806, 548.3170776, 1, 10.0676613]
```

**示例 2:** 在本例中，浮点类型值被视为张量输入，参数直接传递给 *cosh* 函数。

## Javascript

```
// Importing the tensorflow.js library 
import * as tf from "@tensorflow/tfjs"

// Defining float values
var val = [1.5, .4, .22];

// Calling tensor1d method
const y = tf.tensor1d(val);

// Calling cosh() method
var res = tf.cosh(y)

// Printing output
res.print();
```

**输出:**

```
Tensor
    [2.3524094, 1.0810723, 1.0242977]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#cosh