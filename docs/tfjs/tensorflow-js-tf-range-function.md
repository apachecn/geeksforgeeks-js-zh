# Tensorflow.js tf.range()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-range-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-range-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。

**tf。range()** 用于创建新的 **tf。Tensor1D** 填充了借助**启动**、**停止、**和**数据类型提供的范围内的数字。**

**语法:**

```
tf.range(start, stop, step, dtype)
```

**参数:**

*   **start:** 是表示范围起始数的整数起始值。
*   **stop:** 是表示区间结束数的整数 stop 值，不包含**。**
*   **步:**默认为 1 或-1 的整数增量。这是一个可选参数。
*   **dtype:** 是输出张量的数据类型。默认为“float32”。这是一个可选参数。

**返回值:**返回一个新的张量 1D 对象。

**示例 1:** 在本例中，我们尝试使用默认步骤 1 生成 1 到 9 的数字范围。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating the tensor1D array by tf.range
var val = tf.range(1,10);

// Printing the tensor
val.print()
```

**输出:**

```
Tensor
    [1, 2, 3, 4, 5, 6, 7, 8, 9]
```

**示例 2:** 在本例中，我们尝试使用步长 2 生成 1 到 10 之间的奇数。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating the tensor1D array by tf.range
var val = tf.range(1,10,2);

// Printing the tensor
val.print()
```

**输出:**

```
Tensor
    [1, 3, 5, 7, 9]
```

**示例 3:** 在本例中，我们尝试使用步长 2 生成 0 到 10 之间的偶数。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating the tensor1D array by tf.range
var val = tf.range(0,10,2);

// Printing the tensor
val.print()
```

**输出:**

```
Tensor
    [0, 2, 4, 6, 8],
```

**示例 4:** 在本例中，我们将尝试使用 dtype 参数。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating the tensor1D array by tf.range
var val = tf.range(-1,1,1,'bool');

// Printing the tensor
val.print()
```

**输出:**

```
​Tensor
    [true, false]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#range