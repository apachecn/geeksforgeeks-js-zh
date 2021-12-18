# tensorflow . js TF . randomuniform()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-random uniform-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-randomuniform-function/)

**Tensorflow.js** 是谷歌开发的开源库，用于在浏览器或节点环境下运行机器学习模型和深度学习神经网络。

**tf.randomUniform()** 函数用于创建一个 tf。具有从均匀分布采样的值的张量。

**语法:**

```
tf.randomUniform (shape, minval, maxval, dtype, seed)
```

**参数:**该函数接受五个参数，如下图所示:

*   **形状:**定义输出张量形状的整数数组。
*   **minval:** 是可选参数。均匀分布范围的下限。默认值为 0。
*   **maxval:** 也是可选参数。这是稳定分布范围的上限。它不包括在范围内。默认值为 1。
*   **数据类型:**输出的数据类型。可能的数据类型值有“float32”、“int32”、“bool”、“complex64”、“string”。这也是一个可选的参数。默认值为“float32”
*   **seed:** 是可选参数。随机数生成器的种子。

**返回:**返回 tf.Tensor。

**例 1:**

## Javascript

```
// Importting the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating the tensor with values sampled
// from a uniform distribution
const x=tf.randomUniform([5]);

// Printing the tensor
x.print();
```

**输出:**

```
Tensor
    [0.0008758, 0.3491586, 0.3466536, 0.9614096, 0.7892056]
```

**例二:**

## Javascript

```
// Importting the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating the tensor with values sampled
// from a normal distribution
const x=tf.randomUniform([2, 2]);

// Printing the tensor
x.print();
```

**输出:**

```
Tensor
    [[0.7312108, 0.5003704],
    [0.8552292, 0.082417 ]]
```

**例三:**

## Javascript

```
// Importting the tensorflow.js library
import * as tf from "@tensorflow/tfjs"

// Creating the tensor with values sampled
// from a normal distribution
const x=tf.randomUniform([5], 10, 15, 'int32', 0);

// Printing the tensor
x.print();
```

**输出:**

```
Tensor
    [12, 14, 10, 13, 12]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#randomUniform