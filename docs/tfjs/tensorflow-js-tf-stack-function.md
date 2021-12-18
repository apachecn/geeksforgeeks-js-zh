# Tensorflow.js tf.stack()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-stack-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-stack-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。它帮助开发人员在 JavaScript 中开发 ML 模型，并直接在浏览器或 Node.js 中使用 ML。

**tf.stack()函数**用于将 tf、张量的堆栈创建为 r+1 秩 tf.tensor。

**语法:**

```
tf.stack(tensors, axis)
```

**参数:**该函数接受两个参数，如上所述，讨论如下。

*   **张量:** 要使用的张量对象列表，具有相同的形状和数据类型。
*   **轴:**是堆栈的一个轴。

**返回值:**返回 tf.Tensor

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"
// Making a tensor a
const a = tf.tensor1d([99, 999, 999]);

// Making a tensor b
const b = tf.tensor1d([322, 411, 888]);

// Making a tensor c
const c = tf.tensor1d([523, 622, 666]);

// Printing the stack
tf.stack([a, b, c]).print();
```

**输出:**

```
Tensor
    [[99 , 999, 999],
     [322, 411, 888],
     [523, 622, 666]]
```

**示例 2:** 在本例中，以轴为第二个参数制作堆栈。

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"
// Making a tensor a
const a = tf.tensor1d([99, 999, 999]);

// Making a tensor b
const b = tf.tensor1d([322, 411, 888]);

// Making a tensor c
const c = tf.tensor1d([523, 622, 666]);

// Printing the stack
tf.stack([a, b, c], 1).print();
```

**输出:**

```
Tensor
    [[99 , 322, 523],
     [999, 411, 622],
     [999, 888, 666]]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#stack