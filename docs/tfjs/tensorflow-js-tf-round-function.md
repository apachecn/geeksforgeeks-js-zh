# Tensorflow.js tf.round()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-round-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-round-function/)

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

那个。 **round()函数**用于寻找所述张量输入的 round 值，并按元素方式进行。此外，它有助于实现银行家舍入。

**语法:**

```
tf.round(x)
```

**参数:**该函数接受如下所示的参数:

*   **x:** 是要计算其整数值的张量输入，可以是 tf 类型。张量，或类型，或数组。

**返回值:**返回 tf。张量对象。

**示例 1:** 在本例中，我们定义了一个 float 类型的输入张量，然后打印它的舍入值。为了创建输入张量，我们使用 **.tensor1d()** 方法，为了打印输出，我们使用**。print()** 方法。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([5.3, 1.4, 4.5, 9.4]);

// Calling round() method and
// printing output
y.round().print();
```

**输出:**

```
Tensor
    [5, 1, 4, 9]
```

**示例 2:** 在此示例中，双类型值被视为张量输入，参数被直接传递给舍入函数。

## Javascript

```
// Importing the tensorflow.js library
//import * as tf from "@tensorflow/tfjs"

// Defining float values
var val = [8.69967679, 0.999999, 78.7823826382];

// Calling tensor1d method
const y = tf.tensor1d(val);

// Calling round() method
var res = tf.round(y)

// printing output
res.print();
```

**输出:**

```
Tensor
    [9, 1, 79]
```