# tensorlow . js TF . acosh()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-acosh-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-acosh-function/)

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。acosh()函数**用于求所述张量元素输入的反双曲 cos。

**语法:**

```
tf.acosh(x)
```

**参数:**

*   **x:** 它是张量输入，其 *acosh* 值将被计算，并且它可以是类型 *tf。张量*，或*型达瑞*，或*阵列*。

**返回值:**返回 tf。张量对象。

**示例 1:** 在这个示例中，我们定义了一个整数类型的输入张量，然后打印它的 acosh 值。为了创建输入张量，我们使用 **.tensor1d()** 方法，为了打印输出，我们使用**。print()** 方法。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([1, 4, 0, 11]);

// Calling acosh() method and
// printing output
y.acosh().print();
```

**输出:**

```
Tensor
    [0, 2.063437, NaN, 3.0889697]
```

**示例 2:** 在本例中，浮点类型值被视为张量输入，参数直接传递给 *acosh* 函数。

## Javascript

```
// Importing the tensorflow.js library 
import * as tf from "@tensorflow/tfjs"

// Defining float values
var val = [1.5, .4, .22];

// Calling tensor1d method
const y = tf.tensor1d(val);

// Calling acosh() method
var res = tf.acosh(y)

// printing output
res.print();
```

**输出:**

```
Tensor
    [0.9624236, NaN, NaN]
```

**参考:**[**https://js.tensorflow.org/api/latest/#acosh**](https://js.tensorflow.org/api/latest/#acosh)