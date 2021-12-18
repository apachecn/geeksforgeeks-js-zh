# Tensorflow.js tf.scalar()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-scalar-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-scalar-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

**。标量()**函数用于创建标量类型的张量均值。缩放器是一个**零维数组**，也被称为一个**秩-0 张量**。使用**创建**标量**。标量()**函数。

**语法:**

```
t.scalar( value, dataType )
```

**参数:**

*   **值:**标量的值。该值可以是**数字、字符串、Uint8Array[ ]、布尔值。**
*   **数据类型[可选]:** 值的数据类型。可以是 **int32** 、 **float32** 、 **bool** 、 **complex64** 或**弦。**

**返回值:**返回张量对象。

**创建一个标量:**在这个例子中，我们正在创建一个新的标量，意味着只有一个值的张量。

**例 1:**

## java 描述语言

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Value of a scalar
var value = 12

// Creating the value of a scalar
var tens = tf.scalar(value)

// Printing the scalar
tens.print();
```

**输出:**

```
Tensor
    12
```

**创建特定数据类型的标量:**在本例中，我们正在创建特定数据类型的标量。请注意，数据类型应该只有 **int32、float32、bool、complex64、**或**字符串。**

**例 2:**

## java 描述语言

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating a scalar using int value
var int_tensor = tf.scalar(12, 'int32')

int_tensor.print()

// Creating a scalar using string value
var str_tensor = tf.scalar("GFG", "string")

str_tensor.print()

// Creating a scalar using float value
var float_tensor = tf.scalar(12.6, "float32")

float_tensor.print();

// Creating a scalar using bool value
var bool_tensor1 = tf.scalar(true, "bool")

bool_tensor1.print()

// Creating a scalar using bool(0 and 1) type
var bool_tensor2 = tf.scalar(0, "bool")

bool_tensor2.print()
```

**输出:**

```
Tensor
    12
Tensor
    GFG
Tensor
    12.600000381469727
Tensor
    true
Tensor
    false
```

**注意:**也可以使用 **tf.tensor()** 函数创建标量。让我们看看这个例子

**使用 tf.tensor()函数创建标量:**

**例 3:**

## java 描述语言

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating a scalar using int tf.tensor()
var tens = tf.tensor(12, [], "int32")

tens.print()
```

这里我们提供了函数的第二个参数一个空数组，因为我们创建了一个标量，标量是秩为 0 的张量。

**输出:**

```
Tensor
    12
```