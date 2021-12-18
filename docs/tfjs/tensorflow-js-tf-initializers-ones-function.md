# tensorflow . js TF . initializer . one()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-initializer-one-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-initializers-ones-function/)

Tensorflow.js 是一个非常著名的机器学习库，用于使用 JavaScript 开发机器学习模型。使用这个库的主要目的是直接从浏览器或者在 Node.js. Tensorflow.js 中运行和部署一个机器学习模型，是一个开源的硬件加速的 JavaScript 库。在本文中，我们将讨论 Tensorflow.js 中的 tf.ones()函数。

**TF . one()**创建一个所有元素都设置为 1 的张量，或者用值 1 初始化张量。

**语法:**

```
tf.ones (shape, dtype)
```

**参数:**

*   **形状**:表示结果数组的形状。该形状是一个整数数组，表示若干行和列。
*   **数据类型**:这些是返回结果的值的类型。类型的默认值是 float。它可以是 int32、complex64、bool、string 或 float32。

**返回类型:**

这个方法返回 dtype 类型的张量，其形状为 order (row*column)，初始化为 1。

**示例 1:** 在本例中，我们将创建一个 3*4 阶张量，并对其应用 tf.ones()。

## Javascript

```
//import tensorflow.js
const tf=require("@tensorflow/tfjs")
//use tf.ones()
var GFG=tf.ones([3, 4]);

//print tensor
GFG.print()
```

**输出:**

```
Tensor
   [[1, 1, 1, 1],
    [1, 1, 1, 1],
    [1, 1, 1, 1]]
```

**示例 2:** 在本例中，我们将通过给定形状数组中的单个元素来创建 1×4 阶张量。

## Javascript

```
//import tensorflow.js
const tf=require("@tensorflow/tfjs")

//create tensor of shape 1*4
var GFG=tf.ones([3]);

//print tensor
GFG.print()
```

**输出**

```
Tensor
   [1, 1, 1]
```

**例 3:** 不同数据类型的 tf.ones()。

## Javascript

```
//import tensorflow.js
const tf=require("@tensorflow/tfjs")

// create tensor with default dtype as float32
tf.ones([3, 3]).print();

// create tensor with complex values
tf.ones([3, 3],'complex64').print();

// create tensor with boolean values by default all
// values true because initialization by ones
tf.ones([3, 3],'bool').print();

//create tensor with integer values
tf.ones([3, 3],'int32').print();
```

**输出:**

```
Tensor
   [[1, 1, 1],
    [1, 1, 1],
    [1, 1, 1]]
Tensor
   [[1 + 0j, 1 + 0j, 1 + 0j],
    [1 + 0j, 1 + 0j, 1 + 0j],
    [1 + 0j, 1 + 0j, 1 + 0j]]
Tensor
   [[true, true, true],
    [true, true, true],
    [true, true, true]]
Tensor
   [[1, 1, 1],
    [1, 1, 1],
    [1, 1, 1]]
```

**参考**[**:**https://js.tensorflow.org/api/latest/#initializers.ones](https://js.tensorflow.org/api/latest/#initializers.ones)