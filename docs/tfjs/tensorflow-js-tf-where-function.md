# Tensorflow.js tf.where()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-where-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-where-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.where()** 函数用于根据指定条件返回第一张量或第二张量的元素。如果给定条件为真，则从第一张量中选择，否则从第二张量中选择。

**语法:**

```
tf.where (condition, a, b)
```

**参数:**该函数接受三个参数，如下图所示:

*   **条件:**必须具有布尔数据类型的输入条件。
*   **a:** 维数与条件大小相同的第一个输入张量。
*   **b:** 第二个输入张量，其形状与“a”兼容。它必须具有与“a”相同的数据类型。

**返回值:**根据指定条件返回元素张量，可以是第一张量，也可以是第二张量。

**例 1:**

## java 描述语言

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Initializing a tensor of conditions
const cond = tf.tensor1d([true, false, true, false], 'bool');

// Initializing two tensors
const a = tf.tensor1d([-2 , 4, -6, 8]);
const b = tf.tensor1d([2, -4, 6, -8]);

// Calling the .where() function
a.where(cond, b).print();
```

**输出:**

```
Tensor
   [-2, -4, -6, -8]
```

**例 2:**

## java 描述语言

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Using a tensor of condition along with two tensors of
// same datatype values as the parameters of the .where() function
tf.tensor1d([10, 20, 30, 40]).
where(tf.tensor1d([true, false, true, false], 'bool'),
tf.tensor1d([100, 200, 300, 400])).print();
```

**输出:**

```
Tensor
   [10, 200, 30, 400]
```

**参考:**T2https://js.tensorflow.org/api/1.0.0/#where