# Tensorflow.js tf.asin()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-asin-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-asin-function/)

Tensorflow.js 是谷歌正在开发的一个开源库，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。asin()函数**用于在元素上找到所述张量的 *asin* 。

**语法:**

```
tf.asin(x) 
```

**参数:**

*   **x:** 是要计算其 *asin* 值的张量输入，可以是 *tf 类型。张量*，或*型达瑞*，或*阵列*。

**返回值:**返回 *tf。张量*对象。

**示例 1:** 在本例中，我们定义了一个整数类型的输入张量，然后将*打印为其*值。为了创建输入张量，我们使用 **.tensor1d()** 方法，为了打印输出，我们使用**。print()** 方法。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining tensor input elements
const y = tf.tensor1d([5, 1, 8, 0]);

// Calling asin() method and
// printing output
y.asin().print();
```

**输出:**

```
Tensor
    [NaN, 1.5707964, NaN, 0.0000676]
```

**示例 2:** 在本例中，浮点类型值被视为张量输入，参数直接传递给函数中的*。*

## *Javascript*

```
*// Importing the tensorflow.js library 
import * as tf from "@tensorflow/tfjs"

// Defining float values
var val = [1.6, .5, .34];

// Calling tensor1d method
const y = tf.tensor1d(val);

// Calling asin() method
var res = tf.asin(y)

// printing output
res.print();*
```

**输出:**

```
Tensor
    [NaN, 0.523645, 0.346944]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#asin