# Tensorflow.js tf.all()函数

> 原文:[https://www . geesforgeks . org/tensorflow-js-TF-all-function/](https://www.geeksforgeeks.org/tensorflow-js-tf-all-function/)

Tensorflow.js 是谷歌开发的开源库，用于在浏览器或节点环境中运行机器学习模型和深度学习神经网络。它还帮助开发人员用 JavaScript 语言开发 ML 模型，并且可以直接在浏览器或 Node.js 中使用 ML。

**tf。** **all()** 函数用于计算跨维度的元素的逻辑与

**语法** :

```
tf.all(x, axis?, keepDims?)
```

**参数**:

*   **x:** 输入张量。
*   **轴:**要减少的维度。
*   **保留尺寸:**如果为真，保留尺寸为 1 的缩小尺寸。

**返回值:**返回 tf。张量

**例 1:**

## Javascript

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"
const gfg = tf.tensor1d([1, 2, 3], 'bool');

gfg.all().print();
```

**输出:**

```
Tensor
    true
```

**例 2:**

## 【JavaScript】

```
// Importing the tensorflow.js library
import * as tf from "@tensorflow/tfjs"
const x = tf.tensor2d([1, 1, 0, 0], [4, 1], 'bool');

// Initialize the axis
const axis = 1;
x.all(axis).print();
```

**输出:**

```
Tensor
   [true, true, false, false]
```

**参考:**T2】https://js.tensorflow.org/api/latest/#all