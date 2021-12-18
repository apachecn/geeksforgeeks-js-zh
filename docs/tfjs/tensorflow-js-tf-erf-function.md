# Tensorflow.js tf.erf()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-ERF-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-erf-function/)

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。erf()函数**用于找到所述张量输入的*高斯*误差函数，并按元素进行。

**语法:**

```
tf.erf(x)
```

**参数:**

*   **x:** 是要计算其*高斯*误差函数值的张量输入，可以是 *tf 类型。张量*，或*型达瑞*，或*阵列*。

**返回值:**返回 tf。张量对象。

**示例 1:** 在本例中，我们定义了一个整数类型的输入张量，然后打印其*高斯*误差函数值。为了创建输入张量，我们使用 **.tensor1d()** 方法，为了打印输出，我们使用**。print()** 方法。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([1, 25, 16, 0]);

// Calling erf() method and
// printing output
y.erf().print();
```

**输出:**

```
Tensor
    [0.8427007, 1, 1, 0]
```

**示例 2:** 在本例中，浮点类型值被视为张量输入，参数直接传递给 *erf* 函数。

## Javascript

```
// Importing the tensorflow.js library 
import * as tf from "@tensorflow/tfjs"

// Defining float values
var val = [0.5, 1.5, .66];

// Calling tensor1d method
const y = tf.tensor1d(val);

// Calling erf() method
var res = tf.erf(y)

// printing output
res.print();
```

**输出:**

```
Tensor
    [0.5204999, 0.9661053, 0.6493767]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#erf