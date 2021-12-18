# Tensorflow.js tf.zeros()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-zeros-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-zeros-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

**tf.zeros()** 函数用于创建所有元素都设置为零的新张量。

**语法:**

```
tf.zeros(shape, dataType)
```

**参数:**

*   **形状:**取我们要生成的张量的形状。
*   **数据类型:**它是结果元素中张量的类型。它可以是' float32 '，' int32 '或' bool '。它默认为“float32”值。这是一个可选参数。

**返回值:**返回给定形状的张量，所有元素设置为零。

**示例 1:** 在本例中，我们使用 tf.zeros()创建了形状 1*1 的张量。

## java 描述语言

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Creating a shape variable
// which stores the shape
var shape = [1,1]

// Creating the tensor
var val = tf.zeros(shape)

// Printing the tensor
val.print()
```

**输出:**

```
Tensor
     [[0],]
```

**示例 2:** 在本例中，我们使用 tf.zeros()和 dataType 参数创建了形状 2*2 的张量。

## java 描述语言

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Creating a shape variable
// which stores the shape
var shape = [2, 2]

// Creating a d_Type variable
// which stores the data-type
var d_Type = 'bool'

// Creating the tensor
var val = tf.zeros(shape, d_Type)

// Printing the tensor
val.print()
```

**输出:**

```
Tensor
    [[false, false],
     [false, false]]
```

**示例 3:** 在本例中，我们使用 tf.zeros()创建了形状 1*1 的张量。

## java 描述语言

```
// Importing the tensorflow.Js library
import * as tf from "@tensorflow/tfjs"

// Creating a shape variable
// which stores the shape
var shape = [3,3]

// Creating the tensor
var val = tf.zeros(shape)

// Printing the tensor
val.print()
```

**输出:**

```
Tensor
    [[0, 0, 0],
     [0, 0, 0],
     [0, 0, 0]]
```

**参考:**T2https://js.tensorflow.org/api/latest/#zeros