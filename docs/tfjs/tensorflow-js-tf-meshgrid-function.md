# tensorlow . js TF . mesh grid()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-mesh grid-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-meshgrid-function/)

Tensorflow.js 是一个开源库，由谷歌开发，用于在浏览器或节点环境中运行机器学习模型以及深度学习神经网络。

**。meshgrid()函数**用于广播参数，以便在 N-D 网格上进行分析。此外，对于 1D 坐标阵列，即**参数*、，该方法返回用于分析给定 N 的 N-D 网格上的表达式的 N-D 坐标阵列的输出列表

**注意:**该函数支持笛卡尔*【xy】*以及矩阵*【ij】*索引协议。如果索引参数固定为默认值，即*【xy】*，则交换前两次测量的广播命令。

**语法:**

```
tf.meshgrid(x?, y?, __2?)
```

**参数:**

*   **X:** The tensor together with the rank geq is 1\. It is optional and can be of tf type. Tensor, type or array.
*   **Y:** The tensor and rank geq are 1\. It is optional and can be of tf type. Tensor, type or array.
*   **_ _ 2:** is an optional parameter with the type {indexing? : string; }.

**返回值:**返回 tf。张量[]。

**示例 1:** 使用秩为 1 的张量。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Defining first tensor
const t1 = [1, 1, 3];

// Defining second tensor
const t2 = [2, 5, 4];

// Calling meshgrid() function
const res = tf.meshgrid(t1, t2);

// Printing output
console.log(res);
```

**输出:**

```
Tensor
    [[1, 1, 3],
     [1, 1, 3],
     [1, 1, 3]],Tensor
    [[2, 2, 2],
     [5, 5, 5],
     [4, 4, 4]]
```

**示例 2:** 使用浮点值。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Calling meshgrid() function with
// float values
const output = tf.meshgrid(2.1, 3.3);

// Printing output
console.log(output);
```

**输出:**

```
Tensor
     [[2.0999999],],Tensor
     [[3.3],]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#meshgrid